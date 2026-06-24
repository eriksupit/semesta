> **REFERENCE MIRROR — bukan skill aktif.** Disalin dari `.claude/skills/tti-prompt-creator/SKILL.md` pada 2026-06-24.
> Source of truth = file asli di atas (terus berevolusi). Ini snapshot; **re-sync manual** bila yang asli berubah.
> Peran: penulis prompt t2i 6-lapis yang loop dengan tti-prompt-audit sampai COMPLIANT; research-before-dispatch (entry) + brave (loop) + confidence (gerbang numerik exit, scoped sumbu terukur) + anti-sycophancy (honesty gate).
> Tim dengan setup Claude Code berbeda: adopsi isi di bawah ke setup masing-masing.

---

---
name: tti-prompt-creator
description: Use when the user wants to author a text-to-image (t2i) generation prompt — a GATE 0 plate or a GATE B keyframe (6-layer JSON) — for a named shot in the Semesta Digital vault. Triggers include "/tti-prompt-creator", "tulis prompt keyframe", "buatkan prompt plat", "author SEQ-x-SC-y shot", "bikin prompt 6-lapis untuk shot ini". Reads the scene prose + character/env plates + rules, drafts the prompt, then LOOPS with tti-prompt-audit until the draft is COMPLIANT before handing it over.
---

# tti-prompt-creator

Authors a compliant 6-layer t2i prompt for a named shot, then self-loops with `tti-prompt-audit` until the draft passes. Pairs with [[tti-prompt-audit]] (the gate). Canonical rules live in `prompt-rules-image-generation.md` + `explainer-video-2/PROMPT-AUDIT-CHECKLIST.md` — this skill does NOT redefine them, it produces a draft that satisfies them.

The four global disciplines bind at named stages (mirrored read-only in `skills-reference/` for the team): `research-before-dispatch` at the entry gate, `brave`/`loop-until-confidence` at the loop engine, `confidence` as the mandatory numeric exit gate, `anti-sycophancy` at the honesty gate. Cite and follow them — do not skip a stage.

## Stage 1 — Entry gate (research-before-dispatch): read the bahan BEFORE writing any token

Authoring from memory is the #1 documented failure (`lessons.md:67` — env prompt "disusun dari kepala, tidak meng-audit field ke prompt-rules" = research-before-dispatch violation). Read, do not assume:

1. `explainer-video-2/03-scene-detail.md` — the prose + shot list for THIS shot (action, framing, who/what is in frame). This is the scene truth.
2. `prompt-rules-image-generation.md` — the 6-layer template + per-field rules + BANNED list.
3. `explainer-video-2/07-style-reference.md` — wardrobe/hair/makeup/footwear catalog + crew anchors.
4. `08-character-sheet/<tokoh>.md` for every person in frame — the FIXED `character_identity`/`character_style` block + the plate file names (`identity_reference`).
5. `09-environment-sheet/E*.md` for the room — the env plate file names (`environment_reference`).
6. `tokens-references/` (TOKENS / CREW / INTERIOR-DESIGN) — framing/angle/camera/lighting/material token libraries.
7. `10-gateB-keyframes/README.md` — keyframe governance (triad attachment, START/END anchor, start/end pair).
8. `lessons.md` — validated gotchas (auto-batik, keyword-leak, modesty axis, etc.).

If the shot, character, or room is not yet specified in these files, STOP and report the gap — do not invent it.

## Stage 2 — Draft the prompt

Write the prompt as a complete 6-layer JSON unit following the template in `prompt-rules` and the shape of existing `10-gateB-keyframes/SEQ1-SC0*.md`:

- Keyframe = a start/end PAIR = TWO complete standalone prompts, identical except Lapis-4 (`subject_state`/`action`/`pose`/`expression`); each REPEATS its own attachment lines.
- Every unit carries the **triad attachment** in-prompt: `character_identity.identity_reference` (per person) + `environment_reference` (room) + START/END-ref (`composition_reference` for END = the START render file; direction plate for START).
- END anchors on the START render (minimal-change), never generated from plates alone.
- Lapis 5 (graphics) dropped — ADDENDUM A1; device present, screen comp-aware.
- Subject MUST live in Lapis-3 (attachment cannot inject an omitted subject).
- Warm grade only in `color_grade` (`slightly warmer midtones`); garments desaturated + every visible garment specified affirmatively.

Write the draft to a scratchpad working file (`<scratchpad>/tti-creator-draft.md`) — not into the vault yet.

## Stage 3 — Loop engine (brave / loop-until-confidence): create ↔ audit until COMPLIANT

Run `tti-prompt-audit` on the scratchpad draft. Then:

1. Read the audit verdict + every MEK violation (file:line) + unmet prose-checkable MATA items.
2. Patch the draft to clear each violation at the ROOT (de-negate, comma-glue, specify the garment, anchor the placement token, etc.) — never paper over with a banned negation.
3. Re-run `tti-prompt-audit`. Repeat.
4. Stop when verdict = COMPLIANT on all MEK + prose-checkable MATA, or after a named blocker (max ~4 iterations) — if still failing, report the specific residual, do NOT declare done. Looping is the skill; "good enough" is forbidden (`brave`; `lessons.md:73` defeatism = violation).

## Stage 4 — Honesty gate (anti-sycophancy): audit is the arbiter

- Do NOT declare the draft COMPLIANT from your own reading — only the `tti-prompt-audit` verdict counts. Confidence in your own draft without the audit run is self-sycophancy (anti-sycophancy Prohibition 2).
- Render-dependent MATA gates CANNOT close pre-generation (no render exists yet): eyeline-vs-camera, framing-drift-wider, real screen-glow, frontal-vs-profile orientation. Mark these **PENDING post-render** explicitly — spec them correctly, but never claim they passed. After the user generates, run `tti-prompt-audit` on the image for the second pass.

## Stage 4b — Confidence gate (MANDATORY, `confidence` + `loop-until-confidence`)

After the audit returns COMPLIANT, emit an explicit `Confidence: NN%` (integer) on the **verifiable axis only**: (a) compliance per the audit verdict + (b) spec-fidelity — does the prompt faithfully encode THIS shot per `03-scene-detail.md` (right action, framing, who/what in frame, cultural term, garment)? This is a SECOND axis above COMPLIANT: a prompt can pass every grep gate yet still be <95% certain it captures the shot (ambiguous cultural token, framing token that may land wide, an abu-abu MATA judgment).

- **If ≤95%:** do NOT hand over. Invoke `loop-until-confidence` — name the specific gap (which token, which scene-prose detail unmatched), patch, re-run `tti-prompt-audit`, re-check against `03`, re-assess. Loop until >95% or a named blocker.
- **Scope the number to the verifiable axis ONLY.** Render-dependent gates (Stage 4 list) are a DECLARED CAP, never part of the pre-render number and never a loop target — gating confidence on them would spin the loop forever (no render exists to verify against). Carry them as `PENDING post-render`. Emit e.g. `Confidence: 96% (compliance + spec-fidelity) · render-dependent gates PENDING post-render`.
- Claiming high confidence that the IMAGE will be good is self-sycophancy about an unknowable — forbidden. Confidence is about the spec, not the render.

## Stage 5 — Handover

Present the COMPLIANT prompt (start/end pair) stamped `COMPLIANT (MEK + prose-MATA)` + `Confidence: NN%` (verifiable axis, >95% required to hand over) + the list of `PENDING post-render` gates. Writing the final prompt into a vault doc (e.g. `10-gateB-keyframes/SEQ*-SC*.md`) is a mutation — propose it and wait for explicit approval (Prohibition 1). Do not auto-write to the vault.

## Discipline

- Audit ≠ author: this skill writes; `tti-prompt-audit` judges. Keep them separate so the gate stays honest.
- Rules are canonical in `prompt-rules` + `PROMPT-AUDIT-CHECKLIST.md`; if unsure, read them, do not invent a token convention.
- Output bahasa Indonesia formal saya–Anda; the prompt JSON itself stays in English token strings.
