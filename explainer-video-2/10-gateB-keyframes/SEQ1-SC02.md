---
title: GATE B Keyframes — SEQ1-SC02 (INT. RUANG KELUARGA, 04.43)
tags: [explainer-video-2, gate-b, keyframe, seq1-sc02]
status: prompts-empty-awaiting-author
created: 2026-06-24
updated: 2026-06-26
aliases: [ev2-gateB-seq1-sc02]
---

# GATE B Keyframes — SEQ1-SC02

> **⚠️ PROMPTS EMPTIED 2026-06-26 — to be re-authored under the new method.** The previous prompts followed the now-**RETRACTED** build-asset-first / 4-mat doctrine that failed to converge (double carpet, swapped 4-figure blocking — see `scene-images/sc02/` rejects). Cleared to avoid being treated as truth. Old prompts recoverable from git.

## Canonical references (do not duplicate here — point only)
- **Scene truth (prose + shot list):** [[03-scene-detail]] § SEQ1-SC02.
- **Prompting method (BINDING):** [[prompt-rules-text-image-to-image]] — Part II 3-mode grammar + camera-lock, Part III shot-design (subject-count, **iterative-build Rule 8a**), Part V JSON templates, enforcement G0–G6. Built on [[prompt-rules-image-generation]].
- **Attachment sourcing:** [[explainer-video-2/ATTACHMENT-PRODUCTION-BACKLOG]] (covered-prayer plates: Herman/Andi peci, Ratna/Lisa mukena).
- **Identity plates:** `character-images/`. **Room plates:** `environment-images/E02_ruangkeluarga/`. **Generated images saved to:** `scene-images/sc02/`.
- **Review rubric:** [[REVIEW-CHECKLIST]].

## Method reminder (one screen — full rules in the method doc)
- **3 modes:** A from-scratch · B identity-anchored (manifest env+identity, L3→`subjects[]`, composition in text) · C composition-anchored (manifest +`composition_reference`, minimal delta).
- **START/END = camera-lock:** identical framing/angle/camera; only Lapis-4 changes; END = Mode C on the accepted START render. A deliberate camera move = explicit L6-DELTA that forfeits the consistency guarantee.
- **Plate-state law:** never attach a plate containing an object the action "creates". **Subject-count ≤1 face-locked (+1 soft); ≥3 collapse** → a 4-figure saf must be **built** (Rule 8a: seed ≤1 → add one figure per Mode C generation), never authored in one pass.
- **Accept → rename:** accepted render → `sc02_sh0N_{start,end}.png`; proven prompt replaces the empty slot.

## Scene constants
- **Room:** E02 Ruang Keluarga (`environment-images/E02_ruangkeluarga/` — `reverse_prayer` + `reverse_prayer_subuh` plates already accepted, single plain green carpet). **On-screen:** Ratna, Herman, Lisa, Andi.
- **Prayer FACES the camera** (locked decision 2026-06-26; supersedes the old profile/qibla-camera-left blocking in git) → covered-prayer plates (peci/mukena) required; the saf is the prime **iterative-build** test.
- **Bersih Saat Sakral:** from SH02 (sajadah) → ZERO graphics/screens; VO silent. Subuh: window dark; interior warm-practical once the ceiling lamp is ON; warm grade via `color_grade`, cool-blue subuh only outside the window.
- **3 shots / 6 keyframes** (SH04 sujud DELETED — i2v can't sync 4-body motion).

---

## SEQ1-SC02-SH01 — WS ruang keluarga, jendela gelap · 35mm
- **Intent (03):** start = ruang gelap, Ratna meraih saklar (only faint blue from the dark window). end = ceiling lamp ON + desktop all-in-one (generic, unbranded) wakes from sleep showing her shop browser as a **neutral lit blank panel** (order list + packaging ad composited in After Effects, A1); Ratna melirik, senyum tipis. Large screen = safe from melt.
- **Attachments (TBD):** env `E02_ruangkeluarga_reverse.png`; identity Ratna (hijab — broadcast/public-facing per modesty) full+closeup.
- **START** — mode: ___ · STATUS: ⬜ TO AUTHOR
- **END** — mode: C · STATUS: ⬜ TO AUTHOR

## SEQ1-SC02-SH02 — MS · prep beat (Bersih Saat Sakral begins)
- **Intent (03):** start = Ratna memunggungi layar (desktop dimming in background), Herman lays out the prayer surface. end = keluarga berkumpul membentuk saf di belakangnya. Payoff: advertised sarong worn by the imam.
- **⚠️ Plate-state check (G0):** if the action is "unroll/lay the carpet," attach a **bare-floor** plate (carpet absent) — NOT a plate with the carpet already laid (double-carpet trap proven here). If the accepted plate already shows the carpet laid, recast the beat as "smoothing / kneeling on" it, not "unrolling".
- **Attachments (TBD):** env E02 reverse-prayer plate; identity Herman (peci) + Ratna (mukena). Multi-figure → build / decompose, not one-pass.
- **START** — mode: ___ · STATUS: ⬜ TO AUTHOR
- **END** — mode: ___ · STATUS: ⬜ TO AUTHOR

## SEQ1-SC02-SH03 — WS saf qiyam (4 orang, faces toward camera) · sacred zone
- **Intent (03):** qiyam bersedekap ditahan, 4 orang satu saf (imam Herman → Andi → Ratna, Lisa). start = qiyam, eye-level frontal-off-axis. end = qiyam pose identik, soft high-angle ~45°. Zero graphics.
- **⚠️ camera-lock conflict:** 03 specifies start=eye-level, end=high-angle → that is a **camera MOVE** (L6-DELTA), which forfeits the start/end consistency guarantee under the new rule. RE-DECIDE at author: either (a) camera-locked pair (same angle, only the held breath/micro-pose changes), or (b) accept the move as a deliberate exception and expect the END to be a near-fresh composition.
- **⚠️ 4 face-locked figures = Rule 8a iterative-build** (the prime PENDING test): seed ≤1 figure (Mode B) → add one figure per Mode C generation onto the accepted render. Each figure: own covered-prayer identity plate + distinct position (canvas coordinates).
- **Attachments (TBD):** env `E02_ruangkeluarga_reverse_prayer_subuh.png`; identity Herman peci + Andi peci + Ratna mukena + Lisa mukena (full, per backlog).
- **START** — mode: B→build · STATUS: ⬜ TO AUTHOR
- **END** — mode: C · STATUS: ⬜ TO AUTHOR
