# HANDOFF — EV2 family plates COMPLETE → next: SC01 scene production (RESTART, hardened)

**Date:** 2026-06-26 (hardened 2026-06-28 after a failed restart) | **Worktree:** /Users/eriksupit/Desktop/superapps | **Branch:** master | **HEAD:** `c53bfc7` (verify: `git log -1 --oneline`)

## What we are building (orientation — do not skip)
A ~5-minute explainer FILM "Satu Keluarga, Satu Hari Penuh" for the Semesta Digital superapp. One family, one day. The film is produced as STILL keyframe images — a START frame + an END frame per shot — which Kling later animates. **Erik generates every image in ChatGPT; Claude only authors prompts + reviews + (on "ya") renames the accepted file. Claude NEVER generates.** Family mains: Herman (~46, clean-shaven), Ratna (~42, hijab in public), Lisa (~20), Andi (~10). All four characters' reference plate sets are DONE + committed. The next job is producing the FIRST scene, SEQ1-SC01 (family waking, pre-dawn 04.40, Herman's bedroom).

## Why the previous restart failed (and the guardrail)
A session was started from the earlier version of this package and FAILED: the model was indecisive, drifted out of context, and "didn't understand what was being built." Root cause: the first instruction was too open-ended ("rewrite the scene immediately") and the package lacked a crisp big-picture anchor → thrashing. **Guardrail now baked into the initial-prompt:** work ONE bounded step per turn; the very first output is ONLY the 7-shot table for approval (nothing else); if unsure what to build, RE-READ `SEQ1-SC01-RESTRUCTURE-2026-06-26.md` instead of improvising. That failed work was rolled back (`git stash`, recoverable); HEAD is clean at c53bfc7.

## Goal
- **Session Goal:** SEQ1-SC01 rewritten to the 7-shot multi-angle grammar in `explainer-video-2/03-scene-detail.md` (`grep -E "SEQ1-SC01-SH0[1-7]" explainer-video-2/03-scene-detail.md` shows SH01–SH07, no "sarong" line); `10-gateB-keyframes/SEQ1-SC01.md` carries master→derivative prompts for SH03 re-authored against the NEW family DAG plates; `E01_kamar_bed4q.png` env-plate prompt authored; SH03 START+END regenerated, accepted, renamed → `scene-images/sc01/sc01_sh03_{start,end}.png`. Constraints unchanged: Claude never generates; image-only (no Kling); within-shot camera-lock (only subject moves, START→END edit-in-place); angle+framing varied across cuts; master=START full-prompt+attachment, derivative=END edit-in-place; report location+attachments after every prompt; commit only on "ya".
- **Ultimate Goal:** finished ~5-min explainer — all keyframes under the locked method, story order, then Kling i2v + VO/AE + assemble.
- **Linkage:** SC01 is the pilot scene proving the CUT-grammar + master→derivative pipeline with the new plates.

## Current State
- Commits: `c53bfc7 Andi 12 DONE` · `9319837 Lisa 12 + Ratna hijab 5/5` · `71e7df8 Ratna base 12` · `ee06892 Herman 12 + family DAG`. Pushed to origin.
- Plates (committed, on disk): H_herman 12 · R_ratna 12 base + 5 hijab · L_lisa 12 · A_andi 12 (53 PNG total).
- Working tree: clean at c53bfc7. The failed restart's edits are in `git stash` (drop with `git stash drop` once confirmed unneeded). Untracked `scene-images/sc02/*.png` rejects + a deleted `E01_kamar_wallart_reverse.png` are pre-existing — leave them; do not commit without asking.
- Test/build: n/a (asset+doc project; validation = visual render review).

## The method (READ `SEQ1-SC01-RESTRUCTURE-2026-06-26.md` for full detail)
- **Principle:** "Subject may move, but framing+angle stay locked within a shot." Richness comes from CUTS, not camera motion.
- **Within a shot (START→END):** angle+framing LOCKED; only subject changes; END = edit-in-place on the accepted START render.
- **Across cuts:** vary ANGLE (right-diag `bed3q` ↔ left-diag `bed4q` ↔ overhead ↔ top-down) + FRAMING (long/medium/close). Grade of each END → next shot's ref; lamp turns ON at SH04-END (warm propagates SH05–SH07).
- **7 shots:** SH01 overhead ECU eyes · SH02 top-down CU phone · SH03 right-diag medium (places phone, stays reclining) · SH04 left-diag long rear-view (lamp on) · SH05 left-diag long (Ratna sits up) · SH06 right-diag long (Herman stands, looks back) · SH07 right-diag close (Ratna smiles).
- **Execution order:** regen SH03 → author+accept `E01_kamar_bed4q.png` (HARD dep before SH04) → pilot SH04 rear-view → SH05→SH06→SH07.

## Next Steps (one bounded step per turn)
1. Output the SC01 7-shot table for Erik's "ya" (from RESTRUCTURE §2). STOP.
2. On approval → rewrite SC01 in `03-scene-detail.md` (lines ~30–42, old 4-shot) to 7-shot.
3. Translate to `10-gateB-keyframes/SEQ1-SC01.md`; re-author SH03 master(START)→derivative(END) vs new plates.
4. Author `E01_kamar_bed4q.png` prompt (mirror of bed3q from `E01_kamar_master.png`).
5. Hand to Erik → generate → review → on "ya" rename → next.

## Branch-Specific Anti-Pitfalls
- Do NOT generate images (Erik's job). Do NOT touch Kling/i2v.
- Do NOT author SH04 before bed4q is accepted (hard dependency).
- Do NOT bulk-edit a sheet's `reference_image` with a block-spanning regex — PER-CELL only + `json.loads` audit (greedy regex corrupted Cell 6/7 once).
- Do NOT commit the E01 wallart deletion / sc02 rejects without explicit instruction.
- Do NOT do all 5 steps in one turn — one bounded artifact, present, wait.

## Acceptance Criteria (the next session demonstrates these)
1. `grep -cE "SEQ1-SC01-SH0[1-7]" explainer-video-2/03-scene-detail.md` = 7; no "sarong" payoff line in SC01.
2. `SEQ1-SC01.md` has master→derivative SH03 prompts (new plates) + an authored `E01_kamar_bed4q.png` prompt.
3. `ls scene-images/sc01/sc01_sh03_{start,end}.png` exists (new-face), accepted + renamed.
4. Every authored prompt reported with location + attachment list; nothing generated by Claude.
