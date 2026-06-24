> **REFERENCE MIRROR — bukan skill aktif.** Disalin dari `.claude/skills/tti-prompt-audit/SKILL.md` pada 2026-06-24.
> Source of truth = file asli di atas (terus berevolusi). Ini snapshot; **re-sync manual** bila yang asli berubah.
> Peran: pre-lock gate t2i prompt — 9 grep MEK + walk MATA + verdict; source of truth aturan = PROMPT-AUDIT-CHECKLIST.md.
> Tim dengan setup Claude Code berbeda: adopsi isi di bawah ke setup masing-masing (global skill / project skill / panduan baca).

---

---
name: tti-prompt-audit
description: Use when the user wants to audit a text-to-image (t2i) generation prompt for compliance with the Semesta Digital prompt-rules before locking/generating — triggers include "/tti-prompt-audit", "audit prompt ini", "cek prompt keyframe", "audit plat", "compliant nggak prompt ini", "pre-lock gate", or pasting a 6-layer JSON prompt / pointing at a keyframe file (e.g. 10-gateB-keyframes/SEQ1-SC02.md). Runs the mechanical grep gates from PROMPT-AUDIT-CHECKLIST.md and walks the human-judgment items.
---

# tti-prompt-audit

Pre-lock compliance gate for text-to-image prompts (GATE 0 plat / GATE B keyframe) in the Semesta Digital vault. The canonical rule source is `explainer-video-2/PROMPT-AUDIT-CHECKLIST.md` (52 items, A–L) which itself derives from `prompt-rules-image-generation.md` + `lessons.md`. This skill does NOT restate the rules — it executes the mechanical (MEK) gates with grep and presents the judgment (MATA) gates for the human to verify against the render / scene prose.

## When to run

Run when the user asks to audit/check a t2i prompt before it is locked or generated, or pastes a prompt block, or names a keyframe/plat file. Do NOT run for non-prompt text.

## Input resolution (first step, always)

1. If the user gave a **file path** (e.g. `explainer-video-2/10-gateB-keyframes/SEQ1-SC02.md`, a `09-environment-sheet/*.md`, an `08-character-sheet/*.md`) → that file is the audit target. Use it directly.
2. If the user **pasted a JSON / token block** in the message → write it verbatim to a scratchpad file (`<scratchpad>/tti-audit-target.txt`) and audit that file. (Writing to scratchpad is a temp working file, allowed; do not write into the vault.)
3. If neither is present → ask for one, paired with the default: "Saya audit file atau blok yang mana? Default: file keyframe terakhir yang Anda sebut."

Read the target once before running gates, so line numbers in grep output map to real lines.

## Phase 1 — MEK gates (mechanical, run grep)

Run each gate against the target file with `grep -nE`. Report every hit with `file:line` + the offending token. A gate with zero hits = PASS. Treat the EXEMPT lists as not-a-violation (do not flag them).

| Gate | grep pattern (`grep -nEi` on target) | EXEMPT / note |
|---|---|---|
| A1 negasi | `\b(no|not|without|absent|un-[a-z]|non-[a-z])\b\|not in frame\|zero ` | `zero shine` OK; whole-words `uniformly/uncluttered/unremarkable` OK (negasi = render-instruction, not substring) |
| A2 token-glue | `\b(and\|but\|or\|with\|for\|plus\|bearing\|is\|are\|was\|be)\b` di nilai token | KEEP `of` + spatial prepositions `toward/above/below/from/to/into/over/against/on` (load-bearing, intra-token) |
| A4 keyword-leak | `light-absorbing\|low-sheen\|non-reflective\|devout\|graying\|gradient\|gradation\|falloff` | test setiap token: satu kata diambil sendiri memunculkan hal tak diinginkan? |
| B2 placement | `\b(beside\|behind\|next to\|one side\|side wall\|opposite\|facing\|above\|below)\b\|beside it` | tiap hit WAJIB ber-anchor `camera-LEFT/RIGHT/BACK` atau objek bernama; pronoun `beside it` = haram |
| D1 dua-temperature | cek `color_grade`: `warmer` DAN `cool` co-occur dalam satu nilai | satu temperature token saja |
| D3 warm-leak | `\b(warm\|golden\|amber\|ochre)\b` di `lighting`/`scene_depth` | `warm directness`/`warm expressive` di mood/facial = register emosi, OK |
| E1 etnis | `\bIndonesian\b\|\bBetawi\b` | pakai kota/etnis spesifik atau `Jakartan` |
| E3 facial color | warna di `facial_features`: `golden\|ivory\|olive\|tan\|warm\|brown\|beige` | facial = tekstur saja |
| K1 sensitivitas | `pesantren\|bayangkan` + nama organisasi keagamaan | `sharia`/`Waktu Sholat` = nama fitur/UI, OK |

For each gate, run the grep, then state: `A1 negasi: PASS` or `A1 negasi: 2 hit — line 14 \`no extra items\`, line 22 \`without clutter\``.

Note: grep is coarse (matches inside prose comments too). For any hit, confirm it is inside an actual token VALUE before calling it a violation — a rule-description line that merely mentions the word is a false positive.

## Phase 2 — MATA gates (judgment, present for human)

These cannot be grepped — they need the render or the scene prose `03`. List them as an unchecked checklist for the user to confirm. Pull the current MATA items live from `PROMPT-AUDIT-CHECKLIST.md` (seksi yang ditandai MATA) rather than hardcoding — that doc is the source of truth and may evolve. The high-frequency ones:

- B3/B4/B5 spasial: kedalaman `foreground/midground/background`? lighting relatif-RUANG (bukan camera-left)? arah-hadap karakter dari plat anatomi (nol left/right)?
- C-series struktur 6-lapis: urutan field benar? subjek ditulis di Lapis-3? Lapis-5 dibuang (video)?
- E5 tiap garmen terlihat dispesifikasi afirmatif (anti auto-batik)?
- F1/F2 framing/angle/camera/lighting dari library + off-axis anti-cliché?
- I-series GATE B: triad attachment (karakter+env+start/end-ref) lengkap? END anchor ke render START? orientasi dari plat cocok (nol "3/4")?

## Phase 3 — Verdict

Close with: `COMPLIANT` (semua MEK PASS + MATA dikonfirmasi user) atau `BELUM — N pelanggaran MEK + M item MATA belum dicek`, daftar pelanggaran + nomor baris, lalu ONE rekomendasi perbaikan konkret + gate validasi. Jangan kunci/generate sebelum verdict COMPLIANT.

## Discipline

- Source of truth = `PROMPT-AUDIT-CHECKLIST.md`. Kalau ragu aturannya, baca doc itu, jangan mengarang gate baru.
- Audit ≠ memperbaiki. Laporkan pelanggaran + rekomendasi; edit prompt hanya setelah user approve (Prohibition 1).
- Output bahasa Indonesia formal saya–Anda.
