---
title: Skills Reference — Semesta Digital prompt toolkit
tags: [skills-reference, prompt-toolkit, shareable]
status: active
created: 2026-06-24
updated: 2026-06-24
---

# Skills Reference

Folder ini berisi **salinan reference** (snapshot markdown) dari skill yang dipakai pipeline prompt t2i Semesta Digital, supaya **ikut ter-commit git dan bisa dibagikan ke tim** yang setup Claude Code-nya berbeda.

## Kenapa folder ini ada (bukan di `.claude/skills/`)

`.gitignore:9` meng-ignore `.claude/` — jadi skill aktif di `.claude/skills/` **tidak ikut ter-share** via git. Folder `skills-reference/` ada di luar `.claude/` → ter-track → sampai ke tim saat clone repo. Ini **dokumen reference**, bukan skill aktif: tim mengadopsi isinya ke setup masing-masing (pasang sebagai global skill, project skill, atau sekadar panduan baca).

## Isi

| File | Asal | Peran di toolkit |
|---|---|---|
| `research-before-dispatch.md` | `~/.claude/skills/` (global) | Gerbang masuk: baca bahan sebelum menulis token; jangan mengarang. |
| `brave.md` | `~/.claude/skills/` (global) | Mesin loop: pantang berhenti sebelum COMPLIANT. |
| `anti-sycophancy.md` | `~/.claude/skills/` (global) | Gerbang kejujuran: audit = wasit; no self-sikofansi. |
| `tti-prompt-audit.md` | `.claude/skills/` (project) | Pre-lock gate t2i: 9 grep MEK + walk MATA + verdict. |
| `tti-prompt-creator.md` | `.claude/skills/` (project) | Penulis prompt 6-lapis yang loop dengan audit sampai COMPLIANT. |

## Disiplin sync (WAJIB, anti-drift)

- Tiap file punya header provenance: file asal + tanggal mirror. **Source of truth = file asal, bukan salinan ini.**
- File asal terus berevolusi; salinan ini snapshot. Bila yang asal berubah, **re-sync manual** (regenerate salinan + perbarui tanggal). Jangan edit salinan sebagai sumber kebenaran kedua.
- Aturan prompt t2i yang kanonik tetap di `prompt-rules-image-generation.md` + `explainer-video-2/PROMPT-AUDIT-CHECKLIST.md`; `tti-prompt-audit.md` di sini hanya menjalankan gate, bukan mendefinisikannya.

## Cara tim memakai

1. Baca file reference untuk memahami metodologi.
2. Untuk menjalankan sebagai skill: salin `tti-prompt-audit.md` (dan creator saat sudah ada) ke `.claude/skills/<nama>/SKILL.md` di setup masing-masing; tiga disiplin global bisa dipasang ke `~/.claude/skills/` atau project sesuai preferensi.
3. Pakai `prompt-rules-image-generation.md` + `PROMPT-AUDIT-CHECKLIST.md` sebagai aturan kanonik.
