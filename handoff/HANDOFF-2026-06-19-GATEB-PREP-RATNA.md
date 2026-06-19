---
title: Handoff — GATE 0 Herman Complete (9/9), next character Ratna
tags: [handoff, explainer-video-2, gate-0, character-sheet, session-transition]
status: active
created: 2026-06-19
updated: 2026-06-19
aliases: [handoff-2026-06-19-gateb-prep-ratna]
---

# HANDOFF — 2026-06-19 (GATE B Prep session → Ratna session)

Orientation: This session ran O4 sync + GATE 0 (Character & Wardrobe Sheet). Herman is fully done (9/9 reference plates generated, validated, approved, renamed). The next session authors Ratna's character sheet using the now-locked pattern. All token rules discovered this session are persisted in canonical docs — read them, do not re-decide them.

## Goal
- **Session Goal:** `explainer-video-2/08-character-sheet/R-ratna.md` exists with: Ratna identity lock (FIXED block), 9 full t2i plate prompts (3 view × 3 shot) compliant with all 9 locked token rules below, and a per-scene wardrobe table covering Ratna's 8 scenes; folder `explainer-video-2/character-images/R_ratna/` created. Check: `grep -c '"hair"' R-ratna.md` ≥ 10 and `grep -cE "no |not in frame|high-key|graying|light-absorbing|non-reflect" R-ratna.md` = 0. Constraint: every rule in "Locked token rules" stays unchanged.
- **Ultimate Goal:** A 5-minute explainer film + scene assets that an ad-provider watches to see the natural ad inventory across a family's full day — sales tool for pre-development funding.
- **Linkage:** Ratna is the 2nd of 4 main characters in GATE 0; completing all character sheets unlocks GATE B (per-shot keyframe prompt authoring), then GATE C (keyframes) → storyboard → film.

## TL;DR
Herman GATE 0 = DONE (9 plates approved in `character-images/H_herman/`). `07-style-reference.md` + `08-character-sheet/` (00-README + H-herman.md) authored. 9 token rules locked across `prompt-rules` + `lessons.md` + memory + `00-README`. Next: author `R-ratna.md` (hijabi, hardest character) then Lisa/Andi/figurans, then WORKLOG close, then GATE B.

## Current state (verify by reading; do not trust this summary alone)
- `explainer-video-2/character-images/H_herman/` — 9 canonical plates: `H_herman_{front,profileA,profileB}_{full,medium,closeup}.png`, all approved. NOTE: a 10th file `Herman Model.png` exists, unexplained, untouched — ask user.
- `explainer-video-2/08-character-sheet/00-README.md` — method, 9-cell template, aspect-per-shot, direction protocol, positive-only + keyword-leak + matte-plate-standard.
- `explainer-video-2/08-character-sheet/H-herman.md` — identity lock + 9 full t2i prompts + per-scene wardrobe (clean template, all rules applied).
- `explainer-video-2/07-style-reference.md` — wardrobe/hair/makeup/footwear catalogs + artist anchors (incl. new hair anchors) + hijab/child/mature/warm deltas + anchor→character map.
- `explainer-video-2/03-scene-detail.md` — GATE A locked, 6 babak / 19 scene / 57 shot. Ratna appears in: SEQ1-SC02, SEQ2-SC03, SEQ3-SC01, SEQ3-SC02, SEQ4-SC03, SEQ5-SC02, SEQ6-SC01, SEQ6-SC02.

## Locked token rules (READ; do NOT re-decide — all in `prompt-rules`/`lessons.md`/memory `semesta-gate0-character-pipeline`/`00-README`)
1. **Multi-angle = 9 separate images** (3 view × 3 shot), not 3-in-one-frame.
2. **Aspect per shot:** full body `9:16`, medium `2:3`, close-up `4:5` (GPT Image 2 supports all natively).
3. **Camera-relative direction** (screen/frame, audience POV; NOT subject): Profile A = faces `camera-left`, Profile B = faces `camera-right`, generated as **mirror of Profile A via reference-image upload**. Compare plates **full-res side-by-side** before judging direction (thumbnails deceive).
4. **Positive-only:** never `no X`/`not in frame`/`without`; write positive or OMIT a field when the element is cropped out (footwear in close-up → delete `footwear` field).
5. **Keyword-leak:** avoid any token whose dominant word drags an unwanted concept — `light-absorbing` leaks `light`, `non-reflective` leaks `reflective`, `low-sheen` leaks `sheen` (GPT Image 2 autoregressive, cannot back-correct).
6. **Uniform, not gradient:** `salt-and-pepper graying temples` → `uniformly salt-and-pepper hair, even grey distribution throughout`. State the rule positively, never `no gradient`.
7. **Matte plate standard (anti-sheen):** hair `dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural`; lighting `flat even soft diffused three-point studio key … matte skin and hair rendering` (drop `high-key`).
8. **Plate baseline:** scene `plain solid white background, subject isolated` (NOT "cyclorama studio"); photostock style tokens; neutral true-to-life grade (warm grade comes later at GATE B keyframes); render-age below real age (e.g. 50→`46 years old`).
9. **Plate deviations (declared, valid):** prime spherical lens (not anamorphic), omit scene_depth/on_screen_graphic, crew scoped to costume/makeup/hair, portrait aspect.

## Per-plate validation flow (agreed)
User generates externally → saves to `character-images/<TAG>_<char>/` → model reads + aligns full-res + scores rubric (aspect/view-direction/identity/wardrobe/background/sheen) → user "setuju/approve" → model renames to `<TAG>_<char>_<view>_<shot>.png`. Error <5% accepted (e.g. Herman close-up hair sheen). Failures → `_rejected/`. Profile B generated as mirror of Profile A via reference image.

## Ratna specifics (next character)
- Identity: Ratna, 45, hijabi UMKM kuliner. Hair = COVERED (Camille Friend anchor for hairline framing); use hijab/modest catalog in `07 §3.1/§3.2`. Makeup = Eryn Krueger Mekash naturalistic mature. Costume = Deborah Hopper.
- 9 plates: hijab worn in ALL (baseline = standard everyday hijab); profile plates show hijab drape in profile. Apply matte standard to any visible hairline + skin.
- 8 scenes for the per-scene wardrobe table (see scene list above); wardrobe varies per scene, hijab style per `07`.

## Anti-pitfalls (corrections made this session)
- Do NOT write negation tokens (cost: `"footwear": "not in frame"` had to be purged).
- Do NOT use gradient tokens in plate sets (cost: Herman close-up hair sheen inconsistency).
- Do NOT use keyword-leaking tokens (`light-absorbing`, `non-reflective`).
- Do NOT judge profile direction from a thumbnail — align full-res first (model mislabeled direction once).
- Do NOT touch `Herman Model.png` without user clarification.

## Next steps (ordered)
1. Author `08-character-sheet/R-ratna.md` (identity + 9 full prompts + per-scene wardrobe), create `character-images/R_ratna/`.
2. Drive per-plate validation flow for Ratna (9 plates).
3. Then `L-lisa.md`, `A-andi.md`, `F-figurans.md`.
4. WORKLOG entry closing GATE 0 authoring.
5. GATE B: per-shot keyframe prompts (WARM video grade).

## Acceptance criteria
- `R-ratna.md` passes the Session Goal grep checks.
- All 9 Ratna plates approved + renamed in `R_ratna/`.
- No token rule altered.
