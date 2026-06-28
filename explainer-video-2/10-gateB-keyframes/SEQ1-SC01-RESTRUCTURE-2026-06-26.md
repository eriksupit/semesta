---
title: SEQ1-SC01 Restructure + Method Changelog (4→7 shots, multi-angle CUT grammar)
tags: [explainer-video-2, gate-b, changelog, seq1-sc01, method]
status: active-design-locked-pending-render
created: 2026-06-26
updated: 2026-06-26
aliases: [ev2-sc01-restructure, sc01-7shot-changelog]
---

# SEQ1-SC01 Restructure + Method Changelog — 2026-06-26

> **Purpose:** context-window survival anchor. If this session's context fills, READ THIS FIRST to stay consistent on the SC01 redesign and the new multi-angle method. Authored from Erik's spec this session, validated against the 4 key renders (SH03 start/end, `E01_kamar_master.png`, `E01_kamar_bed3q.png`). **No render produced yet — design locked, prompts pending.**

## 1b. METHOD OVERRIDE (2026-06-29, validated bed4q experiment) — read first
- **Every scene/asset has ONE MASTER image (parent, full from-scratch prompt). Every other ANGLE = EDIT-IN-PLACE child of that master, in the SAME context window** (master annotated *recent camera view* + *next/goal camera view*, terse delta) — NOT a separate full-prompt with the master re-uploaded in a fresh window (resamples → inconsistent; proven across ~6 bed4q renders).
- Within a shot, framing+angle stay LOCKED, only the subject moves START→END (the §1 principle below — UNCHANGED, still holds). Two edit-in-place uses: (a) between cuts = move angle; (b) within shot = subject moves.
- `E01_kamar_bed4q` is therefore NOT a standalone full-prompt plate — it is an in-lane edit-in-place child of the kamar master. Full law: `prompt-rules-text-image-to-image.md` changelog 2026-06-29 "MASTER-PARENT + EDIT-IN-PLACE-ANGLE".

## 1. Method change (NEW — applies to all shots/scenes from here)

**Principle (Erik, #lessons):** *"Subyek boleh berubah / asumsi bergerak, tapi framing dan angle ajeg + konsisten."*

- **Within a shot (START→END):** camera angle + framing are LOCKED. Only the subject changes (pose/gesture/light-state). This is the already-validated Rule 22 (camera-lock). END = edit-in-place on the accepted START render.
- **Between shots (CUT):** angle AND framing MAY change. The bed is the spatial axis; the scene is cut as shot-reverse-shot around it, alternating:
  - **Right-diagonal** = camera vantage `E01_kamar_bed3q.png` (window/curtain camera-LEFT, nightstand+lamp camera-RIGHT, Great Wave above headboard).
  - **Left-diagonal** = camera vantage `E01_kamar_bed4q.png` (TO BE GENERATED — true mirror of bed3q: nightstand camera-LEFT, window camera-RIGHT).
- **Mood/color/lighting chain:** each shot references the PREVIOUS shot's END for grade. Lighting STATE propagates forward — critically, **lamp turns ON at SH04-END**, so SH05/SH06/SH07 are lamp-lit (warmer) while SH01–SH04-START are pre-dawn dark (screen/ambient only).
- **180°-line note:** alternating diagonals crosses the screen-axis each cut. Acceptable as DISCRETE CUTS of static keyframe pairs (reverse angles), NOT as continuous camera moves. Requires `bed4q` to be a faithful mirror so the room reads as one space.

## 2. SC01 shot restructure (4 shots → 7 shots)

Old SC01 = SH01–SH04 (waking → stand + sarong). **Sarong/standing/prayer-prep beats are DEFERRED**; prayer scene (old SEQ1-SC02) shifts downstream. New SC01 = an expanded tender waking sequence:

| Shot | Angle (vantage) | Framing | Δ START→END | Char refs | Grade ref |
|------|-----------------|---------|-------------|-----------|-----------|
| **SH01** | overhead | ECU eyes | eyes closed→open | H front_closeup | — (DONE, accepted) |
| **SH02** | top-down | CU macro | phone screen→thumb | env nightstand | SH01 (DONE) |
| **SH03** | right-diag `bed3q` | **medium** (was long) | Herman places phone on nightstand (stays RECLINING; sit-up elided at cut) | H+R current plates | **SH02-END** |
| **SH04** | left-diag `bed4q` | long | lamp turns ON | H+R **REAR-VIEW** fullbody (from front_full masters) | SH03-END |
| **SH05** | left-diag `bed4q` | long | Ratna wakes, sits up, looks at Herman | H+R rear-view fullbody | SH04-END |
| **SH06** | right-diag `bed3q` | long | Herman stands, turns to look at Ratna | H+R faces visible (front/profileB full) | SH05-END |
| **SH07** | right-diag `bed3q` | close | Ratna smiles | Herman blur FG + Ratna focus BG (closeup plates) | SH06-END |

**Action chain:** places phone (SH03) → seen from behind, lamp on (SH04) → Ratna sits up (SH05) → Herman stands, looks back (SH06) → Ratna smiles, close (SH07) → CUT to prayer.

**Per-shot START/END method:**
- SH03: START = full-prompt regenerate (Mode B, like current). END = edit-in-place (place phone on nightstand).
- SH04: START = full-prompt (rear-view, `bed4q`). END = edit-in-place (lamp on).
- SH05: START = full-prompt (rear-view, pose ref = SH04-END). END = edit-in-place (Ratna sits up).
- SH06: START = full-prompt (right-diag, faces revealed, pose ref = SH05-END — CANNOT be edit-in-place, angle changed). END = edit-in-place (Herman stands).
- SH07: START = full-prompt (close, Herman blur FG / Ratna focus BG, pose ref = SH06-END). END = edit-in-place (Ratna smiles).

## 3. Reference plates

- **Characters (current, on disk):** `character-images/H_herman/` + `R_ratna/` — front/profileA/profileB × full/medium/closeup; Ratna also 3 hijab plates. SC01 = Ratna UNCOVERED (private bedroom, mahram; R-ratna §0).
- **Env (current):** `environment-images/E01_kamar/` = master, bed3q, nightstand, wallart_reverse.
- **Env (TO GENERATE):** `E01_kamar_bed4q.png` — left-diagonal mirror of bed3q, from master `E01_kamar_master.png`. **Hard dependency: must exist + be accepted BEFORE SH04 can be authored.**
- **Grade chain:** SH03←SH02-END, SH04←SH03-END, SH05←SH04-END, SH06←SH05-END, SH07←SH06-END.

## 4. Open risks / watch-items (ranked)

1. **REAR-VIEW — now backed by DEDICATED rear plates (mitigated 2026-06-26).** Originally SH04/SH05 forced back-of-head from frontal masters (N=0 risk). RESOLVED: `H-herman.md` Cells 10–12 add `H_herman_rear_{full,medium,closeup}.png` (generated from the matching new front plate as `reference_image`, rotated to the back, face hidden affirmatively). SH04/SH05 attach these rear plates instead of forcing rear from frontal. Dependency: rear plates reference the REGENERATED fronts → generate rear only after fronts accepted. (Ratna rear plates DONE 2026-06-26 — `R-ratna.md` now carries the same 12-cell DAG incl. `R_ratna_rear_{full,medium,closeup}`, age-token 37 ~42 real.) Still pilot SH04 to confirm the rear plate holds in-scene.
2. **SH03-END posture must be pinned = Herman stays RECLINING when placing phone** (small delta fits medium framing). The bangkit-duduk is ELIDED in the cut SH03→SH04; SH04 picks him up already seated, seen from behind. Do NOT inherit a vague "like SH03-END" — state seated explicitly in SH04-START.
3. **`bed4q` must be a true mirror of `bed3q`** (same furniture, opposite vantage: nightstand→camera-left, window→camera-right) or the room reads as two different spaces.
4. **SH04-END "lamp on" needs diegetic motivation** — name which lamp (nightstand lamp, OFF until now) and the agent (Herman's hand to the switch), not a magic state-change.
5. **Plate selection for face-revealing shots** SH06 (front_full/profileB_full) + SH07 (closeup) — Erik's spec left "sesuaikan referensi"; Claude pins at authoring time.

## 5. Execution order (locked sequencing — closes risk #1 before scaling)

1. Regenerate **SH03 START+END** (lowest risk; validates medium-framing on existing angle).
2. Author + generate + accept **`E01_kamar_bed4q.png`** (env dependency).
3. Pilot **SH04 rear-view** = decisive test of rear-from-frontal-plate. If it holds → continue; if it fails → adapt (e.g. build a dedicated rear character plate) before SH05–SH07.
4. Then SH05 → SH06 → SH07.

## 6. Downstream doc-sync owed (after design renders out — NOT yet done)

- `03-scene-detail.md` § SEQ1-SC01 — rewrite shot list 4→7, edit storyline/narration per shot.
- Total shot count `56` → recount (SC01 +3 shots; prayer scene renumbered).
- Runtime estimate (~307s) — re-tally.
- `04-ad-inventory-map` + deck `11` — ad-surface beats moved.
- `SEQ1-SC01.md` — SH04 slot replaced by SH04–SH07 slots under new method.
- `prompt-rules-text-image-to-image.md` — add the multi-angle CUT grammar + rear-view rule (once rear-view validated on SH04).
- Auto-memory + lessons/context/scope.

## 7. Procedure (unchanged this session)

Claude authors prompt in the relevant doc → Erik copies → pastes in ChatGPT → generates → review → on "ya/terbaik" Claude renames accepted PNG to `scene-images/sc01/sc01_shNN_{start,end}.png` → updates governance docs. Claude never generates. Image-only (no Kling).

**BINDING report rule (Erik, 2026-06-26):** every time Claude finishes writing/updating a prompt, Claude MUST immediately report, unprompted: (a) **WHERE** the prompt lives (file → section → START/END), and (b) the **full ATTACHMENT list** (each filename + role). Erik needs both to copy the right block and attach the right plates. Canonical in `lessons.md` + auto-memory `semesta-prompt-report-rule`.
