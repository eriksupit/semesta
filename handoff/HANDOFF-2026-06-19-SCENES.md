# HANDOFF — Writing scene-detail for Explainer Video 2 ("Satu Keluarga, Satu Hari Penuh")

**Date:** 2026-06-19 | **Worktree:** /Users/eriksupit/Desktop/superapps (Obsidian vault, not a git repo) | **Branch:** n/a | **HEAD:** n/a — no git; treat `explainer-video-2/00-WORKLOG.md` Decision Log as the authoritative change record.

This is a DESIGN/WRITING session. The task is authoring the per-scene script (`explainer-video-2/03-scene-detail.md`) for the rebooted explainer video, sequence by sequence, each validated by the user before the next. This session does NOT generate images, does NOT touch production cost docs (RAB/pipeline) beyond linking, and does NOT pour clean prose into `01-storyline.md` yet (that happens only after all sequences are validated). The immediate open item is a pending creative decision on SEQ3-SC02; everything after it is unwritten.

## Goal

- **Session Goal:** In `explainer-video-2/03-scene-detail.md`, resolve the pending SEQ3-SC02 decision (convert to "digital bank room"), then write SEQ4 (Sore) and SEQ5 (Malam) in full SEQ→SC→SH form. Done when: (a) SEQ3-SC02 is rewritten or explicitly kept, with the choice logged in `00-WORKLOG.md`; (b) `03-scene-detail.md` contains SEQ1–SEQ5 complete; (c) every scene obeys the locked conventions (1 location+1 time, camera-bound prose, mandatory interaction, 4-beat grammar, "Bersih Saat Sakral", numbering reset per parent); (d) total runtime budget stays ≈300s (SEQ1 40 + SEQ2 55 + SEQ3 70 leaves ~135s for SEQ4+SEQ5); (e) each sequence is user-validated before the next is written. Constraint that must not change: no real brand/organisation names in-video (mock/generic only); single male VO explicit on meaning, silent on feature mechanics; word "bayangkan" banned.
- **Ultimate Goal:** A finished 5-minute explainer film + scene assets that an ad provider watches and sees natural ad-inventory across the family's day — the sales tool that funds pre-development.
- **Linkage:** Scene-detail is the GATE-A source that feeds image-prompt authoring (GATE B), keyframe generation (GATE C), and the storyboard; without it locked, nothing downstream can start.

## TL;DR

Concept reboot from "7-archetype gallery" to one Jakarta middle-class family across a full day is locked and underway. Narrative hierarchy is fixed as Sequence→Scene→Shot (canonical in `06-konvensi-naratif.md`). `03-scene-detail.md` holds **SEQ1 (Subuh) and SEQ2 (Pagi) complete and validated; SEQ3 (Siang) has SC01/SC03/SC04 validated and SC02 pending a decision.** SEQ4 and SEQ5 are unwritten. A non-negotiable OPERATING CONTRACT was added to `CLAUDE.md` this session — read it first; it changes how the next session must close turns (conviction, no ritual approve/override/amend tag on discussion turns, mutation-gate only).

## Context & Decisions

**Reboot recap.** New theme: one family — Herman (50, ekspor-impor supervisor + saham), Ratna (45, home-culinary/frozen-food UMKM), Lisa (20, student + content creator), Andi (10, online-school SD) — followed dawn→night, crossing paths with different-class neighbours. Audience = ad providers.

**What changed this session.** (1) New folder discipline already existed; this session wrote the conventions doc, the production pipeline, and SEQ1–SEQ3 of scene-detail. (2) Narrative hierarchy locked: Sequence (by message) → Scene (1 location + 1 time) → Shot (1 camera setup = 1 keyframe-pair = 1 Kling 5s segment). (3) Two cross-cutting rules added after user corrections: **camera-bound prose** (no omniscient narration crossing locations) and **mandatory interaction in activity scenes** (face-to-face or on-screen; favour cross-class/demographic). (4) Numbering rule clarified: scene resets to SC01 per sequence, shot resets to SH01 per scene; full ID `SEQ<n>-SC<nn>-SH<nn>`. (5) **OPERATING CONTRACT** (Erik mandate) written into `CLAUDE.md`.

**Decision this session.** Marketplace is over-represented in SEQ3 (≥4 selling beats); user direction is to dial it down and surface the virtual-office/bank-as-tenant differentiator. Proposed (NOT yet approved): convert SEQ3-SC02 to a "digital bank room".

**Mandatory references:**
- `/Users/eriksupit/Desktop/superapps/CLAUDE.md` (OPERATING CONTRACT at top)
- `explainer-video-2/00-WORKLOG.md` (full Decision Log — authoritative chronology)
- `explainer-video-2/06-konvensi-naratif.md` (canonical hierarchy + rules)
- `explainer-video-2/05-pipeline-produksi.md` (stack + 3-gate cycle + 4 corrections)
- `prompt-rules-image-generation.md` + `explainer-video/08-investor-deck-brief.md` (prompt authoring reference for GATE B)
- memory: `semesta-operating-contract.md`, `semesta-video-concept-rebuild.md`

## Current State

- Vault is not a git repo → no commit SHAs; change record lives in `explainer-video-2/00-WORKLOG.md` Decision Log.
- `explainer-video-2/03-scene-detail.md`: SEQ1 (≈40s, 2 scene / 8 shot) DONE; SEQ2 (≈55s, 4 scene / 11 shot) DONE; SEQ3 (≈70s, 4 scene / 14 shot) — SC01/SC03/SC04 validated, **SC02 PENDING**.
- `explainer-video-2/01-storyline.md`: clean-output skeleton only (5 act headers, "menunggu pengisian") — NOT yet filled.
- `explainer-video-2/02-storyboard.md`, `04-ad-inventory-map.md`: stubs.
- `explainer-video-2/scene-images/` exists with `sc01`–`sc15` subfolders + README; no images yet.
- `CLAUDE.md`, `scope.md`, `context.md`, `lessons.md` updated this session; memory files `semesta-operating-contract.md` + `semesta-video-concept-rebuild.md` written/updated.
- Test/build status: not applicable (documents, no code).
- Uncommitted work: not applicable (no git).

## SEQ-by-SEQ Status

- **SEQ1 — Subuh (DONE).** SC01 INT kamar 04.40: wake → phone (Subuh reminder + sarung "Cap Gajah" ad + stock chart) → don sarung (4-beat canonical). SC02 INT ruang keluarga 04.43: dark window (subuh is dark — sunrise ~05.55), lamp + all-in-one desktop wakes showing Ratna's shop browser (overnight orders + packaging ad, pre-sacred teaser) → congregational prayer, commercial-zero from takbir ("Bersih Saat Sakral").
- **SEQ2 — Pagi (DONE).** SC01 EXT gate cross-class (anchor LISA leaving, not Herman); SC02 INT office Herman virtual-office; SC03 INT study Andi online-school (+ warm Ratna beat, cross-cut SC02); SC04 INT café Lisa (lecture → ends → business module → record creator clip, sequenced).
- **SEQ3 — Siang (SC01/03/04 validated; SC02 PENDING).** SC01 Ratna LIVE-SELLING (live audience + Tika teen helper); SC02 = pending decision; SC03 Herman trading + mentors young colleague Rian (anti-judi); SC04 Lisa TEACHES a creator workshop to UMKM mothers + youth (student→teacher).
- **SEQ4 — Sore: UNWRITTEN.** Skeleton intent: cross-class transaction (e.g. courier delivers to upper-class neighbour / neighbour interactions), worship/sharia opt-in moment (Bersih Saat Sakral), kids home/finished studying.
- **SEQ5 — Malam: UNWRITTEN.** Skeleton intent: family gathers (app as the day's connecting thread) + reflection/invitation (VO meaning checkpoint) + dim down/sleep + tagline.

## Next Steps

1. **Resolve SEQ3-SC02 (do this first).** Ask the user once (natural phrasing, per OPERATING CONTRACT) whether to convert SC02 from "B2B selling" to a **"digital bank room"**: Ratna, at her kitchen table at home, enters a generic unbranded bank's virtual branch (virtual-office tenant) and discusses business capital with a bank officer over video — feels like visiting a bank branch though online. Rationale: cut "just another marketplace" perception (marketplace ≥4 beats); surface the bank-as-tenant differentiator (`CLAUDE.md` PROJECT CONTEXT) which is currently absent; assign to Ratna (NOT Herman, who already holds virtual-office SEQ2-SC02 + trading SEQ3-SC03); generic bank, home setting to keep warm tone, Ratna↔officer interaction. On approval, rewrite SEQ3-SC02 in `03-scene-detail.md` and log it.
2. **Write SEQ4 (Sore, ≈65s)** in full SEQ4-SC0x-SH0x form: cross-class transaction + worship/sharia opt-in (Bersih Saat Sakral) + kids returning/finishing. All scenes interactive + camera-bound. Validate with user before SEQ5.
3. **Write SEQ5 (Malam, ≈70s)**: family gathering + reflection/invitation VO + sleep + tagline. Validate.
4. **After all SEQ validated:** pour clean prose into `01-storyline.md`; update the per-scene status table in `05-pipeline-produksi.md`.
5. Log every decision into `00-WORKLOG.md` as it happens.

### (NO Phase) — do NOT in the next session
- Do NOT generate any images / write GATE-B prompts yet (scene-detail must be validated first).
- Do NOT rewrite SEQ1/SEQ2 or re-open locked conventions absent a user request.
- Do NOT touch RAB (`03`/`03-a`) or pipeline cost numbers; they are inherited, link-only.

## Branch-Specific Anti-Pitfalls

- Do NOT write omniscient prose that crosses locations (e.g. "rumah mulai hidup" while scene is locked to one room) — user correction this session; rule now in `06-konvensi-naratif.md` (camera-bound).
- Do NOT number scenes/shots globally/continuously — they RESET per parent (SEQ2 starts at SEQ2-SC01, shots at SH01); user correction this session.
- Do NOT leave activity scenes mono-actor — interaction is mandatory (face-to-face or on-screen); user correction this session.
- Do NOT show daylight at subuh — Indonesian subuh (~04.42) is fully dark, sunrise ~05.55; user correction this session.
- Do NOT over-expose Herman — balance across family members; SEQ2 was rebalanced to anchor the gate scene on Lisa for this reason.
- Do NOT close discussion turns with a ritual "approve/override/amend" tag or "bilang lanjut maka saya kerjakan" — OPERATING CONTRACT bind #5 (conviction, not deference); the validation gate is ONLY for mutation actions, asked once in natural language.

## Acceptance Criteria for This Session

1. SEQ3-SC02 decision made and reflected in `03-scene-detail.md` + logged in `00-WORKLOG.md`.
2. `03-scene-detail.md` contains SEQ1 through SEQ5, every scene with header (location + time), camera-bound prose, a shot list with full `SEQ-SC-SH` IDs, and a "Catatan produksi" block.
3. Every activity scene has at least one interaction; commercial beats follow 4-beat grammar; worship beats obey "Bersih Saat Sakral".
4. Numbering resets correctly per sequence (scene) and per scene (shot).
5. Total runtime across SEQ1–SEQ5 ≈300s (±10%).
6. `00-WORKLOG.md` Decision Log updated for each new/changed scene.
