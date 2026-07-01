---
title: Environment Sheet — E13 Terminal TransJakarta (INT peron) · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e13-terminal, gate-0-env, interior, ooh]
status: fase2-prompt-locked
created: 2026-06-30
updated: 2026-07-01
aliases: [ev2-e13-terminal, E13-terminal, terminal-transjakarta-env]
---

# Environment Sheet — E13 TERMINAL TRANSJAKARTA · tag E13
> Method/anchor → [[00-README-ENV]] (§2.6). Scene truth → [[03-scene-detail]] SEQ5-SC12. Shotlist → `10-gateB-keyframes/SEQ5-SC12.md`.
> **Room:** a city rapid-transit bus terminal platform at dusk — a large covered public concourse, the **hero surface = a giant wall-mounted OOH digital screen** (OFF in plate; moving ads = AE). 1× use (SC12). Empty of NAMED figures (Lisa/bapak desa = GATE B); a **soft anonymous ambient passenger crowd IS part of the plate dressing** (not face-locked, per the crowd-ambient rule `lessons` b.58) so the space reads as a busy hub. Neutral grade; dusk grade + OOH glow + named figures = GATE B.

> **Register — declared deviation (public transit, not a home):** no IKEA home furniture, no Hokusai home wall-art. Register = a generic TransJakarta-style city rapid-transit platform (no readable operator brand). Anchor = `production_designer` **Eugenio Caballero** (public realism). Discipline that holds: NAMED figures absent (ambient crowd only), **neutral grade**, **scoped-angle**, token-per-token, positive-only, **ADDENDUM A1** (every screen OFF — the giant OOH, the digital schedule board, the phone; ads + schedule = After Effects).

> **Token discipline (locked):** comma-delimited clusters, no conjunction glue, zero negation, camera-relative direction. **Fase-2 status:** prompts LOCKED, **generate PENDING (sesi baru)**.

---

## 1. Scene identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E13 angle)
This block stays identical across ALL E13 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E13_terminal_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm busy-hub stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "modern city rapid-transit bus terminal platform, large bright covered concourse, sleek steel-and-glass architecture, giant wall-mounted OOH digital screen, digital arrival schedule board, glass platform-edge gates, clean columns, recessed LED ceiling, soft ambient passenger crowd, contemporary well-maintained urban transit hub",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "quiet busy-hub calm",
  "subject_anchor": {
    "primary_subject": "modern rapid-transit bus terminal platform, giant wall-mounted OOH digital screen off dark neutral, far wall, digital arrival schedule board camera-LEFT, glass platform-edge gates camera-RIGHT, waiting lane centre, soft anonymous ambient passenger figures scattered along the platform",
    "subject_material": "polished stone concourse floor, brushed-steel and glass columns, glass platform-edge gates, contemporary benches, clean well-maintained modern transit surfaces",
    "wall_screen": "giant wall-mounted OOH digital screen, far wall, screen off dark neutral, slim bezel, hero display surface, mounted high",
    "supporting_objects": {
      "schedule_board": "digital arrival schedule board, camera-LEFT, screen off dark neutral, mounted on a column",
      "gates": "glass platform-edge gates, sliding doors, camera-RIGHT, yellow safety line along the platform edge",
      "ticket_gates": "row of modern ticket-gate turnstiles, brushed steel, mid-ground",
      "benches": "contemporary waiting benches, timber-and-steel, along the platform",
      "columns": "clean brushed-steel and glass platform columns, structural roof beams above",
      "wayfinding_totem": "modern freestanding wayfinding totem, slim vertical sign pillar, blank faces, brushed metal",
      "kiosk": "small modern retail kiosk, glass front, screen off, plain, camera-LEFT background",
      "planters": "modern planters with leafy greenery, along the concourse",
      "signs": "plain generic direction signs, blank, hanging overhead",
      "ceiling": "recessed LED ceiling light strips, bright even",
      "crowd": "soft anonymous ambient passenger figures, blurred, distant, scattered waiting along the platform",
      "bus": "modern rapid-transit bus, faint, beyond the platform-edge gates camera-RIGHT",
      "sky": "dusk sky, faint, through the platform openings",
      "bin": "sleek modern platform rubbish bin, camera-LEFT",
      "floor": "polished stone concourse floor, yellow edge line"
    },
    "human_absence_signal": "foreground spot clear, soft anonymous ambient crowd only, distant, still"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "modern city rapid-transit terminal, contemporary well-maintained public transit, clean steel-and-glass architecture"
}
```
**Canonical layout (defined by master, directions FROM THE MASTER CAMERA's POV, camera along the platform):** a large bright modern concourse — a giant wall-mounted OOH digital screen on the far wall (the hero surface, OFF in plate), a digital arrival schedule board on the camera-LEFT (mounted on a column, OFF), glass platform-edge gates on the camera-RIGHT (a faint modern rapid-transit bus + dusk sky beyond), a row of brushed-steel ticket-gate turnstiles mid-ground, contemporary timber-and-steel waiting benches + brushed-steel-and-glass columns + a wayfinding totem + planters + a small glass-front kiosk (OFF) along the concourse, recessed LED ceiling strips, a yellow safety line at the platform edge · a soft anonymous ambient passenger crowd (blurred, distant, faces NOT detailed) scattered along the platform as dressing. **The OOH wall + ambient crowd give the dense-hub read; the schedule-board spot (camera-LEFT) is where the named figures stand at GATE B; the foreground waiting spot stays clear.**

**ADDENDUM A1:** every screen renders OFF / dark / neutral in the plate — the giant OOH wall screen, the digital arrival schedule board, AND (at GATE B) Lisa's phone. All content is composited in After Effects: the moving OOH ad slots (hero surface), the "Kedatangan [jam]" schedule, the phone UI. The ambient crowd is soft dressing (no locked faces); the two named figures (Lisa + bapak desa) are added at GATE B.

---

## 2. Method (per [[00-README-ENV]] §2.6 + public-transit deviation)
- **Master generated first, no reference-image.** PRN derivative uploads `E13_terminal_master.png` as reference + rewrites ONLY the `shot` block → same platform, new camera. (Generate = separate session; at authoring time the derivative only carries the `environment_reference` token.)
- **Public-transit register declared:** no IKEA, no Hokusai. Caballero public realism + named transit elements (OOH screen, platform-edge gates, schedule board, steel columns) — strong real-world types for consistency.
- **Ambient crowd IS plate dressing** (soft, blurred, anonymous, distant) — the only exception to empty-room, justified for a busy hub (`lessons` b.58 crowd-ambient-not-face-locked). The NAMED figures (Lisa/bapak) are still GATE B.
- **Hero OOH screen OFF** in plate; ads = AE (the densest inventory surface in the film).
- **Empty foreground, neutral grade:** named figures + dusk grade + OOH glow = GATE B.
- **No readable operator brand / livery / ad** (brand-safe; all = AE).
- **Token-per-token values** — no conjunctions inside JSON token values (b.119); comma-delimited clusters only. Negation ban absolute.

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` SEQ5-SC12 shot-list)
Each cell is a COMPLETE copy-paste-ready prompt, zero scaffold. §1 is the canonical identity-lock. Scoped to E13's two plates: MASTER (establishing WIDE, serves SC12-SH01/SH05) · PRN (schedule-board spot MS, serves SC12-SH02/SH04). PRN uploads `E13_terminal_master.png` as reference-image at generate time.

### Cell M — MASTER · establishing WIDE → `E13_terminal_master.png` · ✅ GENERATED + ACCEPTED (2026-07-01, modern-dignified)
Full modern platform geography — the anchor plate. Establishes the giant OOH screen (OFF), digital schedule board camera-LEFT, glass platform-edge gates camera-RIGHT, ticket-gate turnstiles, contemporary benches, LED ceiling, ambient crowd along the platform. **Register modernized preemptively per token-dignity (lessons 2026-07-01): steel-and-glass + LED + ticket-gates + wayfinding totem + kiosk + planters; dropped "painted steel / class-mixed / lived-in". A1: every screen OFF (OOH + schedule + kiosk); ads/schedule/UI = AE.**
```json
{
  "mood": "neutral reference clarity, calm busy-hub stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "modern city rapid-transit bus terminal platform, large bright covered concourse, sleek steel-and-glass architecture, giant wall-mounted OOH digital screen, digital arrival schedule board, glass platform-edge gates, clean columns, recessed LED ceiling, soft ambient passenger crowd, contemporary well-maintained urban transit hub",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "quiet busy-hub calm",
  "subject_anchor": {
    "primary_subject": "modern rapid-transit bus terminal platform, giant wall-mounted OOH digital screen off dark neutral, far wall, digital arrival schedule board camera-LEFT, glass platform-edge gates camera-RIGHT, waiting lane centre, soft anonymous ambient passenger figures scattered along the platform",
    "subject_material": "polished stone concourse floor, brushed-steel and glass columns, glass platform-edge gates, contemporary benches, clean well-maintained modern transit surfaces",
    "wall_screen": "giant wall-mounted OOH digital screen, far wall, screen off dark neutral, slim bezel, hero display surface, mounted high",
    "supporting_objects": {
      "schedule_board": "digital arrival schedule board, camera-LEFT, screen off dark neutral, mounted on a column",
      "gates": "glass platform-edge gates, sliding doors, camera-RIGHT, yellow safety line along the platform edge",
      "ticket_gates": "row of modern ticket-gate turnstiles, brushed steel, mid-ground",
      "benches": "contemporary waiting benches, timber-and-steel, along the platform",
      "columns": "clean brushed-steel and glass platform columns, structural roof beams above",
      "wayfinding_totem": "modern freestanding wayfinding totem, slim vertical sign pillar, blank faces, brushed metal",
      "kiosk": "small modern retail kiosk, glass front, screen off, plain, camera-LEFT background",
      "planters": "modern planters with leafy greenery, along the concourse",
      "signs": "plain generic direction signs, blank, hanging overhead",
      "ceiling": "recessed LED ceiling light strips, bright even",
      "crowd": "soft anonymous ambient passenger figures, blurred, distant, scattered waiting along the platform",
      "bus": "modern rapid-transit bus, faint, beyond the platform-edge gates camera-RIGHT",
      "sky": "dusk sky, faint, through the platform openings",
      "bin": "sleek modern platform rubbish bin, camera-LEFT",
      "floor": "polished stone concourse floor, yellow edge line"
    },
    "human_absence_signal": "foreground spot clear, soft anonymous ambient crowd only, distant, still"
  },
  "shot": {
    "composition": "full modern platform geography, one frame, giant OOH digital screen off far wall, digital arrival schedule board camera-LEFT, glass platform-edge gates camera-RIGHT, yellow edge line, ticket-gate turnstiles mid-ground, contemporary benches, brushed-steel and glass columns, wayfinding totem, planters, recessed LED ceiling, soft anonymous ambient passenger figures scattered along the platform, dusk sky beyond the gates, legible",
    "framing": "WS establishing, platform receding to background, roof beams visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "along the platform, looking down the concourse, schedule-board wall camera-left, platform-edge gates camera-right",
    "camera_direction": "down the platform, OOH screen far wall, schedule board camera-left, platform-edge gates camera-right, dusk sky beyond",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral interior platform light, balanced neutral white, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "modern city rapid-transit terminal, contemporary well-maintained public transit, clean steel-and-glass architecture"
}
```

### Cell PRN — SCHEDULE-BOARD SPOT MS → ⛔ **DROPPED (2026-07-01)** · SC12 uses master as env-ref
**DROPPED (reference-dominance recompose, tighter-same-scene).** PRN (50mm push-in on the schedule-board spot) recomposed the camera-LEFT area instead of faithfully re-framing the master — the render (`a767c326…`, in `_rejected/`) drifted (freestanding board totem vs master's wall-mount, different bench/column placement). Same failure class as GTE / BGK2 / E06 MEJA. Edit-in-place is NOT a fix either: it is reliable only for subject-delta at LOCKED framing, not a wide→medium reframe (which resamples/invents → drift). **SC12-SH02/SH04 therefore attach `E13_terminal_master.png` (same master as SH01/SH05); the 50mm schedule-board framing + figures (bapak + Lisa) are composed at the GATE-B keyframe. Using ONE master for every SC12 shot guarantees cut-to-cut consistency.** Prompt below retained for reference only (do NOT generate).
```json
{
  "environment_reference": "attached reference plate E13_terminal_master.png, same modern terminal platform, identical OOH screen, identical digital schedule board, identical glass platform-edge gates, identical layout, identical materials, faithful platform match, new camera per shot block only",
  "mood": "neutral reference clarity, calm busy-hub stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "modern city rapid-transit bus terminal platform, large bright covered concourse, sleek steel-and-glass architecture, giant wall-mounted OOH digital screen, digital arrival schedule board, glass platform-edge gates, clean columns, recessed LED ceiling, soft ambient passenger crowd, contemporary well-maintained urban transit hub",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "quiet busy-hub calm",
  "subject_anchor": {
    "primary_subject": "platform waiting spot near the digital arrival schedule board, schedule board screen off dark neutral camera-LEFT, a contemporary timber-and-steel waiting bench, a brushed-steel-and-glass column, giant OOH screen soft in the background",
    "subject_material": "polished stone concourse floor, brushed-steel and glass columns, glass platform-edge gates, contemporary benches, clean well-maintained modern transit surfaces",
    "wall_screen": "giant wall-mounted OOH digital screen, background, screen off dark neutral, soft",
    "supporting_objects": {
      "schedule_board": "digital arrival schedule board, camera-LEFT, screen off dark neutral, mounted on a column",
      "bench": "contemporary timber-and-steel waiting bench, near the schedule board",
      "column": "a brushed-steel and glass platform column, structural roof beam above",
      "crowd": "soft anonymous ambient passenger figures, blurred, distant, background",
      "floor": "polished stone concourse floor, yellow edge line"
    },
    "human_absence_signal": "foreground spot clear, soft anonymous ambient crowd only, distant, still"
  },
  "shot": {
    "composition": "medium framing on the waiting spot near the digital arrival schedule board, schedule board screen off camera-LEFT, a contemporary waiting bench, a platform column, dominant mid-ground, giant OOH screen soft in the background, soft anonymous ambient crowd distant, compressed platform",
    "framing": "MS, schedule-board waiting spot fills frame, standing eye-level, platform compressed behind",
    "angle": "eye-level",
    "camera_position": "facing the schedule-board waiting spot, pushed in from establishing wide, standing eye-level",
    "camera_direction": "toward the arrival schedule board, waiting bench, platform column, OOH screen soft behind",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral interior platform light, balanced neutral white, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "modern city rapid-transit terminal, contemporary well-maintained public transit, clean steel-and-glass architecture"
}
```

---

## 4. Status manifest
| Cell | Angle | File | Serves | Status |
|---|---|---|---|---|
| M | establishing WIDE | `E13_terminal_master.png` | SC12-SH01/SH05 | ✅ **GENERATED + ACCEPTED (2026-07-01, modern-dignified)** |
| PRN | schedule-board spot MS | ~~`E13_terminal_peron.png`~~ | SC12-SH02/SH04 | ⛔ **DROPPED** — SC12 uses master (reference-dominance recompose; cf. GTE, BGK2, E06 MEJA) |

**E13 COMPLETE (1 plate: M).** PRN dropped — all SC12 shots attach `E13_terminal_master.png`; framing at keyframe.

Storage: `environment-images/E13_terminal/` (+ `_rejected/`). Naming: `E13_terminal_<angle>.png`.
Generate M first (no reference-image). Then PRN via the `shot`-only-rewrite method: upload `E13_terminal_master.png` as reference + paste §1 verbatim + the cell's `shot` block. Every screen OFF/polos (A1); OOH ads + schedule + phone UI = After Effects. Ambient crowd is soft dressing (no locked faces); Lisa + bapak desa = GATE B.

---

*E13 Terminal TransJakarta environment sheet — Fase-2 prompts LOCKED (generate PENDING, sesi baru) · Explainer Video 2 · 2026-07-01 · INT public transit (declared deviation: no IKEA/Hokusai, Caballero realism) · giant OOH = hero surface OFF (AE) · ambient crowd dressing (not face-locked) · token-per-token · camera-relative direction.*
