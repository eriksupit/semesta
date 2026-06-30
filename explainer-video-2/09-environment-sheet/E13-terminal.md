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
  "scene": "city rapid-transit bus terminal platform, large covered public concourse, giant wall-mounted OOH digital screen, arrival schedule board, platform-edge gates, painted steel columns, soft ambient passenger crowd, generic urban transit hub",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "quiet busy-hub calm",
  "subject_anchor": {
    "primary_subject": "rapid-transit bus terminal platform, giant wall-mounted OOH digital screen off dark neutral, far wall, arrival schedule board camera-LEFT, platform-edge gates camera-RIGHT, waiting lane centre, soft anonymous ambient passenger figures scattered along the platform",
    "subject_material": "polished concrete platform floor, painted steel columns, glass platform-edge gates, brushed-metal benches, real lived-in transit surfaces",
    "wall_screen": "giant wall-mounted OOH digital screen, far wall, screen off dark neutral, slim bezel, hero display surface, mounted high",
    "supporting_objects": {
      "schedule_board": "arrival schedule board, camera-LEFT wall, screen off dark neutral, mounted on a column",
      "gates": "platform-edge gates, glass sliding doors, camera-RIGHT, yellow safety line along the platform edge",
      "benches": "brushed-metal waiting benches, along the platform, plain",
      "columns": "painted steel platform columns, structural roof beams above",
      "signs": "plain generic direction signs, hanging overhead",
      "crowd": "soft anonymous ambient passenger figures, blurred, distant, scattered waiting along the platform",
      "bus": "rapid-transit bus, faint, beyond the platform-edge gates camera-RIGHT",
      "sky": "dusk sky, faint, through the platform openings",
      "bin": "plain platform rubbish bin, camera-LEFT",
      "floor": "polished concrete platform floor, yellow edge line"
    },
    "human_absence_signal": "foreground spot clear, soft anonymous ambient crowd only, distant, still"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "city rapid-transit terminal, public-transit realism, class-mixed, lived-in"
}
```
**Canonical layout (defined by master, directions FROM THE MASTER CAMERA's POV, camera along the platform):** a large covered concourse — a giant wall-mounted OOH digital screen on the far wall (the hero surface, OFF in plate), an arrival schedule board on the camera-LEFT wall (mounted on a column, OFF), glass platform-edge gates on the camera-RIGHT (a faint rapid-transit bus + dusk sky beyond), brushed-metal waiting benches + painted steel columns + overhead direction signs along the platform, a yellow safety line at the platform edge · a soft anonymous ambient passenger crowd (blurred, distant, faces NOT detailed) scattered along the platform as dressing. **The OOH wall + ambient crowd give the dense-hub read; the schedule-board spot (camera-LEFT) is where the named figures stand at GATE B; the foreground waiting spot stays clear.**

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

### Cell M — MASTER · establishing WIDE → `E13_terminal_master.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Full platform geography — the anchor plate. Establishes the OOH screen far wall, schedule board camera-LEFT, platform-edge gates camera-RIGHT, ambient crowd along the platform.
```json
{
  "mood": "neutral reference clarity, calm busy-hub stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "city rapid-transit bus terminal platform, large covered public concourse, giant wall-mounted OOH digital screen, arrival schedule board, platform-edge gates, painted steel columns, soft ambient passenger crowd, generic urban transit hub",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "quiet busy-hub calm",
  "subject_anchor": {
    "primary_subject": "rapid-transit bus terminal platform, giant wall-mounted OOH digital screen off dark neutral, far wall, arrival schedule board camera-LEFT, platform-edge gates camera-RIGHT, waiting lane centre, soft anonymous ambient passenger figures scattered along the platform",
    "subject_material": "polished concrete platform floor, painted steel columns, glass platform-edge gates, brushed-metal benches, real lived-in transit surfaces",
    "wall_screen": "giant wall-mounted OOH digital screen, far wall, screen off dark neutral, slim bezel, hero display surface, mounted high",
    "supporting_objects": {
      "schedule_board": "arrival schedule board, camera-LEFT wall, screen off dark neutral, mounted on a column",
      "gates": "platform-edge gates, glass sliding doors, camera-RIGHT, yellow safety line along the platform edge",
      "benches": "brushed-metal waiting benches, along the platform, plain",
      "columns": "painted steel platform columns, structural roof beams above",
      "signs": "plain generic direction signs, hanging overhead",
      "crowd": "soft anonymous ambient passenger figures, blurred, distant, scattered waiting along the platform",
      "bus": "rapid-transit bus, faint, beyond the platform-edge gates camera-RIGHT",
      "sky": "dusk sky, faint, through the platform openings",
      "bin": "plain platform rubbish bin, camera-LEFT",
      "floor": "polished concrete platform floor, yellow edge line"
    },
    "human_absence_signal": "foreground spot clear, soft anonymous ambient crowd only, distant, still"
  },
  "shot": {
    "composition": "full platform geography, one frame, giant OOH digital screen off far wall, arrival schedule board camera-LEFT, platform-edge gates camera-RIGHT, yellow edge line, waiting benches, painted columns, soft anonymous ambient passenger figures scattered along the platform, dusk sky beyond the gates, legible",
    "framing": "WS establishing, platform receding to background, roof beams visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "along the platform, looking down the concourse, schedule-board wall camera-left, platform-edge gates camera-right",
    "camera_direction": "down the platform, OOH screen far wall, schedule board camera-left, platform-edge gates camera-right, dusk sky beyond",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral interior platform light, balanced neutral white, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "city rapid-transit terminal, public-transit realism, class-mixed, lived-in"
}
```

### Cell PRN — SCHEDULE-BOARD SPOT MS → `E13_terminal_peron.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Serves SEQ5-SC12-SH02/SH04 (the bapak + Lisa at the schedule-board spot, 50mm). The waiting spot near the arrival schedule board at standing height, the OOH screen soft in the background.
```json
{
  "environment_reference": "attached reference plate E13_terminal_master.png, same terminal platform, identical OOH screen, identical schedule board, identical platform-edge gates, identical layout, identical materials, faithful platform match, new camera per shot block only",
  "mood": "neutral reference clarity, calm busy-hub stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "city rapid-transit bus terminal platform, large covered public concourse, giant wall-mounted OOH digital screen, arrival schedule board, platform-edge gates, painted steel columns, soft ambient passenger crowd, generic urban transit hub",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "quiet busy-hub calm",
  "subject_anchor": {
    "primary_subject": "platform waiting spot near the arrival schedule board, schedule board screen off dark neutral camera-LEFT, a brushed-metal waiting bench, a painted steel column, giant OOH screen soft in the background",
    "subject_material": "polished concrete platform floor, painted steel columns, glass platform-edge gates, brushed-metal benches, real lived-in transit surfaces",
    "wall_screen": "giant wall-mounted OOH digital screen, background, screen off dark neutral, soft",
    "supporting_objects": {
      "schedule_board": "arrival schedule board, camera-LEFT, screen off dark neutral, mounted on a column",
      "bench": "brushed-metal waiting bench, plain, near the schedule board",
      "column": "a painted steel platform column, structural roof beam above",
      "crowd": "soft anonymous ambient passenger figures, blurred, distant, background",
      "floor": "polished concrete platform floor, yellow edge line"
    },
    "human_absence_signal": "foreground spot clear, soft anonymous ambient crowd only, distant, still"
  },
  "shot": {
    "composition": "medium framing on the waiting spot near the arrival schedule board, schedule board screen off camera-LEFT, a waiting bench, a platform column, dominant mid-ground, giant OOH screen soft in the background, soft anonymous ambient crowd distant, compressed platform",
    "framing": "MS, schedule-board waiting spot fills frame, standing eye-level, platform compressed behind",
    "angle": "eye-level",
    "camera_position": "facing the schedule-board waiting spot, pushed in from establishing wide, standing eye-level",
    "camera_direction": "toward the arrival schedule board, waiting bench, platform column, OOH screen soft behind",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral interior platform light, balanced neutral white, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "city rapid-transit terminal, public-transit realism, class-mixed, lived-in"
}
```

---

## 4. Status manifest
| Cell | Angle | File | Serves | Status |
|---|---|---|---|---|
| M | establishing WIDE | `E13_terminal_master.png` | SC12-SH01/SH05 | ✅ prompt LOCKED · generate PENDING (sesi baru) |
| PRN | schedule-board spot MS | `E13_terminal_peron.png` | SC12-SH02/SH04 | ✅ prompt LOCKED · generate PENDING (sesi baru) |

Storage: `environment-images/E13_terminal/` (+ `_rejected/`). Naming: `E13_terminal_<angle>.png`.
Generate M first (no reference-image). Then PRN via the `shot`-only-rewrite method: upload `E13_terminal_master.png` as reference + paste §1 verbatim + the cell's `shot` block. Every screen OFF/polos (A1); OOH ads + schedule + phone UI = After Effects. Ambient crowd is soft dressing (no locked faces); Lisa + bapak desa = GATE B.

---

*E13 Terminal TransJakarta environment sheet — Fase-2 prompts LOCKED (generate PENDING, sesi baru) · Explainer Video 2 · 2026-07-01 · INT public transit (declared deviation: no IKEA/Hokusai, Caballero realism) · giant OOH = hero surface OFF (AE) · ambient crowd dressing (not face-locked) · token-per-token · camera-relative direction.*
