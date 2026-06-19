---
title: Handoff — Lisa Character Sheet session (GATE 0 continues)
tags: [handoff, explainer-video-2, character-sheet, gate-0, lisa]
status: active
created: 2026-06-20
updated: 2026-06-20
aliases: [handoff-2026-06-20-lisa]
---

# Handoff — Lisa Character Sheet (successor to GATE-0-Ratna-complete)

Next session authors `08-character-sheet/L-lisa.md` and validates Lisa's reference plates, replicating the now-locked GATE 0 pattern. Do NOT re-decide the locked rules — replicate from `H-herman.md` + `R-ratna.md`.

---

## Goal
- **Session Goal:** `explainer-video-2/08-character-sheet/L-lisa.md` exists with: Lisa identity lock (FIXED block), **9 full t2i plate prompts** (3 view × 3 shot, uncovered baseline, hair worn LOOSE & down), and a per-scene wardrobe table covering Lisa's 6 scenes; folder `explainer-video-2/character-images/L_lisa/` (+ `_rejected/`) created. Check: `grep -c '"hair"' L-lisa.md` ≥ 10 AND `grep -cE "no |not in frame|high-key|graying|light-absorbing|non-reflect" L-lisa.md` = 0. Constraint: no locked token-rule changes; reference plates show hair loose (styling deferred to GATE B).
- **Ultimate Goal:** 5-minute explainer film + scene assets for ad-providers → pre-development funding sales tool.
- **Linkage:** Lisa is character 3 of 4 in GATE 0; finishing all 4 character sheets unlocks GATE B (per-shot keyframe prompts) → GATE C → storyboard → film.

---

## TL;DR
Herman + Ratna GATE 0 COMPLETE. Ratna closed this session at **12/12 plates** (`character-images/R_ratna/`): 9 uncovered turnaround (hair loose) + 3 hijab reference. Lisa is next — **9 plates only** (not hijabi, no covered plates needed). Replicate the pattern; Lisa's anchors and scene list are below.

---

## Current State
- **Herman:** COMPLETE. 9 plates in `character-images/H_herman/`. Sheet `08-character-sheet/H-herman.md`.
- **Ratna:** COMPLETE 2026-06-20. 12 plates in `character-images/R_ratna/` (9 uncovered + 3 hijab). Sheet `R-ratna.md` v0.3. Manifest `00-README.md` marks her COMPLETE. WORKLOG entry 2026-06-20 logs the closure.
- **Lisa / Andi / Figurans:** todo.
- **No git:** the vault is NOT a git repository — `commit` is not yet possible. If versioning is wanted, `git init` is an open user decision (flagged below).

## Locked token rules (DO NOT re-decide — replicate from H-herman.md / R-ratna.md)
1. Multi-angle = 9 separate images (3 view × 3 shot). Aspect per shot: full `9:16`, medium `2:3`, close-up `4:5`.
2. Camera-relative direction: Profile A = camera-left, Profile B = camera-right (mirror of A via reference-image upload). Compare full-res before judging. Files: `front`/`profileA`/`profileB`, never left/right.
3. Positive-only tokens (zero negation). Omit a field if its element is cropped out (no `"not in frame"`).
4. Keyword-leak ban — including inside `character_identity.role` (the `hijabi` leak that forced a headscarf on Ratna's uncovered plates; for Lisa watch any token that drags an unwanted concept).
5. Uniform, not gradient. Matte plate standard (hair `dry matte hair, velvety matte strands, chalky matte finish`; lighting `flat even soft diffused three-point studio key … matte skin and hair rendering`, no `high-key`).
6. Plate deviations declared (neutral grade, prime lens, plain white bg, crew scoped to costume/makeup/hair, portrait aspect).
7. **Reference plates show hair LOOSE & down** (lock full hair identity); styling (Lisa's half-up clip / low ponytail) is deferred to GATE B scene keyframes. (User correction 2026-06-20, applies to all characters.)
8. Render-age below real age (Herman 50→46, Ratna 45→41). **Lisa render-age is an OPEN decision** — real 20; a flat −4 → 16 risks reading too teen. Recommend setting ~19 and verifying against the first generated plate before locking.

## Lisa specifics (from `07-style-reference.md` §5 + §3.2 + `00-README` manifest)
- Tag **L**. 20, mahasiswi + content creator, young urban Jakartan woman, contemporary styled. **Not hijabi → 9 plates only, no covered plates.**
- Anchors: `costume_designer: Michael Wilkinson` · `makeup_artist: Judy Chin` · `hair_stylist: Camille Friend`.
- Hair (07 §3.2): on-camera ready, glossy young finish. **Baseline plate = loose & down** (not the half-up clip / low-ponytail — those are scene looks).
- Makeup (07 §3.3): `medium-coverage satin foundation poreless, defined brows lash mascara nude glossy lip soft bronzer, baked setting powder matte finish zero shine` (on-camera ready, more polished than Ratna's natural register).
- Wardrobe (07 §3.1 + §8 base): contemporary urban, desaturated colorway; warmth via grade only.
- Footwear (07 §3.4): `clean white low-top canvas sneakers, rubber sole`.
- Scenes (6): SEQ2-SC01, SEQ2-SC04, SEQ3-SC04, SEQ4-SC02, SEQ5-SC01, SEQ6-SC01.

## Per-plate validation flow (unchanged)
User generates externally → saves to `character-images/L_lisa/` as `Content <W>x<H>.png` → you read + score rubric (aspect / view-direction / identity / wardrobe / hair-loose / background-matte) → user "setuju" → you rename to `L_lisa_<view>_<shot>.png`. Profile B = mirror of Profile A via reference upload. Error <5% accepted. Failures → `L_lisa/_rejected/`.

## Next Steps
1. Read bootstrap files (see initial-prompt). Read `R-ratna.md` as the clean template + `03-scene-detail.md` for Lisa's 6 scenes' prose.
2. Decide Lisa render-age (recommend ~19), then author `L-lisa.md` (identity lock + 9 plate prompts + 6-scene wardrobe table). Get per-action "ya" before the Write.
3. Create folder `character-images/L_lisa/_rejected/`.
4. Validate plates as the user generates them; rename on approval.
5. On Lisa complete → mark COMPLETE in `00-README` + WORKLOG, then `A-andi.md`.

## Anti-pitfalls (this session's lessons — also in lessons.md + memory)
- Modesty axis is non-mahram-exposure, not indoor/outdoor (Ratna). N/A to Lisa's covering but the mahram logic governs any veiled figuran.
- `hijabi`/covering trigger in `role` forces a headscarf — keep identity role clean of unwanted-concept triggers.
- Reference plates = hair loose/down to lock identity; tying deferred to GATE B.
- Canonical-source tokens can still contain negation (`no visible…`) — audit before pasting.

## Open / Deferred
- **Lisa render-age** (recommend ~19, verify on first plate).
- **`git init`** — vault is not a repo; user must authorize versioning if wanted.
- Runtime ~312s vs 300s (raised at GATE B, not now).
- `Herman Model.png` 10th file — still unexplained, do not touch without user clarification.
