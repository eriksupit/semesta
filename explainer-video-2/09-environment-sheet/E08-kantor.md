---
title: Environment Sheet — E08 Kantor Ekspor-Impor · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e08-kantor, gate-0-env, interior]
status: fase2-prompt-locked
created: 2026-06-30
updated: 2026-07-01
aliases: [ev2-e08-kantor, E08-kantor, kantor-ekspor-impor-env]
---

# Environment Sheet — E08 KANTOR EKSPOR-IMPOR · tag E08
> Method/anchor → [[00-README-ENV]] (§2.6). Scene truth → [[03-scene-detail]] SEQ2-SC05 (morning) **+ SEQ4-SC10** (afternoon — reuse). Shotlists → `10-gateB-keyframes/SEQ2-SC05.md` + `SEQ4-SC10.md`.
> **Room:** a small-to-medium export-import office, busy-calm — desk rows with monitors, a large shipping-route map on the far wall, a large wall-mounted display (the SC10 commodity dashboard, OFF in plate). **Used 2×** (registry = highest-ROI, fullest angle set): SC05 (morning, task-board) + SC10 (afternoon, export permit on a tablet + the wall dashboard). Empty-room reference plates, neutral grade; Herman + Rian (F4) + warm-morning (SC05) / orange-afternoon (SC10) grade + live screens added at GATE B keyframes.

> **Register — declared deviation (NOT a home):** this is a **contract / institutional** office, NOT a family home — the IKEA flat-pack rule + the Hokusai home wall-art rule do NOT apply. Design anchor = `production_designer` **Eugenio Caballero** (corporate working-class realism); furniture = contract office register; the wall "art" is a functional framed shipping-route map, not a decorative woodblock. Discipline that holds: **empty-room** (zero figures in plate), **neutral grade**, **scoped-angle**, token-per-token, positive-only, **ADDENDUM A1** (every screen OFF; the virtual workspace board + commodity dashboard = After Effects).

> **Token discipline (locked):** comma-delimited token clusters, no conjunction glue, zero negation, camera-relative direction. **Fase-2 status:** prompts LOCKED, **generate PENDING (sesi baru)**.

---

## 1. Room identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E08 angle)
This block stays identical across ALL E08 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E08_kantor_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm empty office stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "modern export-import office workspace, contemporary corporate interior, bright minimalist open-plan, sit-stand desks, glass partition accents, large wall-mounted digital displays, recessed LED ceiling, contract-institutional register, lived-in working office",
  "location": "indoor",
  "time_of_day": "day",
  "atmosphere": "quiet lived-in modern office calm",
  "subject_anchor": {
    "primary_subject": "modern export-import office workspace, parallel height-adjustable sit-stand desks, matte white desktops, each desk a slim widescreen monitor screen off dark neutral, modern ergonomic mesh task chairs, front action desk a large ultrawide monitor screen off dark neutral, camera centre, large wall-mounted digital display screen off dark neutral far back wall",
    "subject_material": "painted plaster office walls cool off-white, matte white laminate desktops, brushed aluminium desk legs, grey polished concrete floor, glass partition panels, real lived-in modern office surfaces",
    "back_display": "large wall-mounted digital display screen, far back wall, centered, wide, slim bezel, screen off dark neutral, mounted on a slim bracket",
    "supporting_objects": {
      "big_display": "large wall-mounted flat display screen, camera-RIGHT wall, screen off dark neutral, slim bezel, mounted on a bracket",
      "desks": "parallel height-adjustable sit-stand desks, matte white desktops, slim widescreen monitors screen off dark neutral, slim keyboards, mice, cable-tidy channels, thin document folders, minimalist, otherwise tidy",
      "chairs": "modern ergonomic mesh task chairs, dark frame, one at each desk",
      "hero_desk": "front action work desk, matte white desktop, a large ultrawide monitor screen off dark neutral, slim keyboard, mouse, thin document folder",
      "storage": "low modern credenza storage units, matte white, camera-LEFT wall, closed cabinet doors, minimalist",
      "glass_partition": "frosted glass partition panel, brushed aluminium frame, camera-LEFT mid-room, modern divider",
      "window_dressing": "wide floor-to-ceiling office window, camera-LEFT wall, slim roller shade, daylight",
      "pantry": "modern pantry nook, camera-LEFT foreground, matte water dispenser, compact espresso machine, minimalist counter",
      "writeboard": "slim frameless glass writeboard, far back wall, camera-RIGHT of the back display, clean",
      "plant": "tall leafy office plant, modern matte planter, beneath the camera-RIGHT wall display",
      "ceiling": "recessed LED ceiling light panels, bright even",
      "floor": "grey polished concrete floor, tidy"
    },
    "human_absence_signal": "unoccupied, still, chairs tucked, all screens dark, office quiet, room empty"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "small-to-medium export-import office, contract-institutional realism, class-accurate working register"
}
```
**Canonical layout (defined by master, directions FROM THE MASTER CAMERA's POV, camera at the back of the office facing the desk rows + back-display wall):** parallel sit-stand desks (matte white) down the centre (each a slim widescreen monitor screen OFF + modern mesh task chair), the front action desk carrying a large ultrawide monitor (OFF) · far BACK wall = large wall-mounted digital display (OFF in plate; live shipping-route map = AE), slim frameless glass writeboard camera-RIGHT of it (NO wall clock — removed) · camera-RIGHT wall = the large wall-mounted display (OFF in plate; the SC10 dashboard), tall office plant beneath it · camera-LEFT wall = wide floor-to-ceiling window with a slim roller shade + low white credenza, a frosted glass partition mid-room, a modern pantry nook (water dispenser + espresso machine) in the camera-LEFT foreground · grey polished concrete floor, recessed LED ceiling. **Perimeter filled (back-display wall, display camera-right, window + credenza camera-left); the desk rows occupy the centre, the front action desk the focal point. TWO wall displays (back = live map, camera-right = SC10 dashboard), both OFF in plate.**

**ADDENDUM A1:** every screen renders OFF / dark / neutral in the plate — the desk monitors, the front ultrawide monitor, the back-wall digital display, AND the camera-RIGHT wall display. All UI is composited in After Effects: back-wall display = the live modern shipping-route map (animated); SC05 = the virtual-workspace board (documents, container schedule, team channel, B2B placements) on the front monitor; SC10 = the commodity-market dashboard on the camera-RIGHT wall display. **no-coal:** the SC10 dashboard content (in AE) = sector / mineral / nickel-downstream level, NEVER coal. There is NO paper wall map anymore (replaced by the digital display) and NO wall clock.

---

## 2. Method (per [[00-README-ENV]] §2.6 + civic deviation)
- **Master generated first, no reference-image.** MEJA + DASBOR derivatives upload `E08_kantor_master.png` as reference + rewrite ONLY the `shot` block → same office, new camera. (Generate = separate session; at authoring time the derivative only carries the `environment_reference` token.)
- **Civic/contract register declared:** no IKEA home furniture, no Hokusai home wall-art. Caballero corporate realism + named contract-office types (laminate desks, ergonomic mesh task chairs, brushed-metal filing) + a functional framed shipping-route map as the wall feature.
- **Big wall display is FIXED dressing** present in both uses — OFF in plate; SC10 dashboard = AE. The DASBOR cell is the SC10 angle that features it.
- **Empty-room, neutral grade:** Herman + Rian + live screens + warm-morning / orange-afternoon grade = GATE B.
- **No readable brands** (brand-safe); any logo/text = AE.
- **Token-per-token values** — no conjunctions inside JSON token values (b.119); comma-delimited clusters only. Negation ban absolute.

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` SEQ2-SC05 + SEQ4-SC10 shot-lists)
Each cell is a COMPLETE copy-paste-ready prompt, zero scaffold. §1 is the canonical identity-lock. Scoped to E08's three plates: MASTER (establishing WIDE, serves SC05-SH01) · MEJA (front-desk MS, serves SC05-SH02/03/04/05) · DASBOR (wall-display angle, serves SC10-SH01/02/03/05). MEJA/DASBOR upload `E08_kantor_master.png` as reference-image at generate time.

### Cell M — MASTER · establishing WIDE → `E08_kantor_master.png` · ✅ GENERATED + ACCEPTED (2026-07-01, modernized v2)
Full modern office geography — the anchor plate. Establishes the sit-stand desk rows centre, back-wall digital display (OFF) far back, wall display camera-RIGHT, floor-to-ceiling window + credenza camera-LEFT. **Modernized per Erik: dated register → contemporary open-plan; wall clock removed; paper shipping-route map → large wall-mounted digital display (screen OFF in plate, live map = AE). Full-prompt regen, not edit-in-place.**
```json
{
  "mood": "neutral reference clarity, calm empty office stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "modern export-import office workspace, contemporary corporate interior, bright minimalist open-plan, sit-stand desks, glass partition accents, large wall-mounted digital displays, recessed LED ceiling, contract-institutional register, lived-in working office",
  "location": "indoor",
  "time_of_day": "day",
  "atmosphere": "quiet lived-in modern office calm",
  "subject_anchor": {
    "primary_subject": "modern export-import office workspace, parallel height-adjustable sit-stand desks, matte white desktops, each desk a slim widescreen monitor screen off dark neutral, modern ergonomic mesh task chairs, front action desk a large ultrawide monitor screen off dark neutral, camera centre, large wall-mounted digital display screen off dark neutral far back wall",
    "subject_material": "painted plaster office walls cool off-white, matte white laminate desktops, brushed aluminium desk legs, grey polished concrete floor, glass partition panels, real lived-in modern office surfaces",
    "back_display": "large wall-mounted digital display screen, far back wall, centered, wide, slim bezel, screen off dark neutral, mounted on a slim bracket",
    "supporting_objects": {
      "big_display": "large wall-mounted flat display screen, camera-RIGHT wall, screen off dark neutral, slim bezel, mounted on a bracket",
      "desks": "parallel height-adjustable sit-stand desks, matte white desktops, slim widescreen monitors screen off dark neutral, slim keyboards, mice, cable-tidy channels, thin document folders, minimalist, otherwise tidy",
      "chairs": "modern ergonomic mesh task chairs, dark frame, one at each desk",
      "hero_desk": "front action work desk, matte white desktop, a large ultrawide monitor screen off dark neutral, slim keyboard, mouse, thin document folder",
      "storage": "low modern credenza storage units, matte white, camera-LEFT wall, closed cabinet doors, minimalist",
      "glass_partition": "frosted glass partition panel, brushed aluminium frame, camera-LEFT mid-room, modern divider",
      "window_dressing": "wide floor-to-ceiling office window, camera-LEFT wall, slim roller shade, daylight",
      "pantry": "modern pantry nook, camera-LEFT foreground, matte water dispenser, compact espresso machine, minimalist counter",
      "writeboard": "slim frameless glass writeboard, far back wall, camera-RIGHT of the back display, clean",
      "plant": "tall leafy office plant, modern matte planter, beneath the camera-RIGHT wall display",
      "ceiling": "recessed LED ceiling light panels, bright even",
      "floor": "grey polished concrete floor, tidy"
    },
    "human_absence_signal": "unoccupied, still, chairs tucked, all screens dark, office quiet, room empty"
  },
  "shot": {
    "composition": "full modern office geography, one frame, parallel sit-stand desks centre, monitors screen off, large wall-mounted digital display screen off far back wall, large wall display camera-RIGHT wall screen off, floor-to-ceiling window camera-LEFT wall, low white credenza camera-LEFT, glass partition camera-LEFT mid-room, pantry nook camera-LEFT foreground, office plant camera-RIGHT, recessed LED ceiling, polished concrete floor, legible",
    "framing": "WS establishing, desk rows receding, ceiling line visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "at the back of the office, looking toward the far back-display wall, window side camera-left, wall-display side camera-right",
    "camera_direction": "down the desk rows, toward the far back digital display wall, wall display camera-right, window camera-left",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "bright even modern office light, cool-neutral white, recessed LED wash, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "small-to-medium export-import office, contract-institutional realism, class-accurate working register"
}
```

### Cell MEJA — FRONT-DESK MS → `E08_kantor_meja.png` · ✅ prompt LOCKED · generate PENDING (modernized v2)
Serves SEQ2-SC05-SH02/03/04/05 (Herman + Rian at the front desk, the large monitor; 50mm mediums + 85mm screen insert + 35mm MW). The action desk at a seated office height, the ultrawide monitor the focal mid-ground, screen OFF (UI in AE). **Modern register (v2): sit-stand white desk, back-wall digital display OFF, no clock.**
```json
{
  "environment_reference": "attached reference plate E08_kantor_master.png, same modern export-import office, identical sit-stand desks, identical back-wall digital display, identical camera-RIGHT wall display, identical layout, identical materials, faithful office match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty office stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "modern export-import office workspace, contemporary corporate interior, bright minimalist open-plan, sit-stand desks, glass partition accents, large wall-mounted digital displays, recessed LED ceiling, contract-institutional register, lived-in working office",
  "location": "indoor",
  "time_of_day": "day",
  "atmosphere": "quiet lived-in modern office calm",
  "subject_anchor": {
    "primary_subject": "front action work desk, matte white desktop, a large ultrawide monitor screen off dark neutral, modern ergonomic mesh task chair, slim keyboard, mouse, thin document folder, camera centre, large wall-mounted digital display screen off dark neutral far back wall",
    "subject_material": "painted plaster office walls cool off-white, matte white laminate desktops, brushed aluminium desk legs, grey polished concrete floor, glass partition panels, real lived-in modern office surfaces",
    "back_display": "large wall-mounted digital display screen, far back wall, centered, wide, slim bezel, screen off dark neutral",
    "supporting_objects": {
      "big_display": "large wall-mounted flat display screen, camera-RIGHT background wall, screen off dark neutral, slim bezel",
      "neighbour_desks": "neighbouring sit-stand desks, matte white desktops, slim widescreen monitors screen off dark neutral, camera-LEFT, soft background",
      "chairs": "modern ergonomic mesh task chairs, dark frame, at the desks",
      "storage": "low white credenza storage units, camera-LEFT background, minimalist",
      "window_dressing": "wide floor-to-ceiling office window, camera-LEFT background wall, slim roller shade, daylight",
      "floor": "grey polished concrete floor, tidy"
    },
    "human_absence_signal": "unoccupied, still, chair tucked, all screens dark, office quiet, room empty"
  },
  "shot": {
    "composition": "medium framing on the front action desk, matte white desktop, a large ultrawide monitor screen off dark neutral, modern task chair, thin document folder, dominant centre, back-wall digital display screen off behind, compressed back wall, neighbouring sit-stand desks soft camera-LEFT",
    "framing": "MS, desk station fills frame, seated office height, room compressed behind",
    "angle": "eye-level, seated office height",
    "camera_position": "in front of the action desk, pushed in from establishing wide, seated office height",
    "camera_direction": "toward the action desk, the ultrawide monitor, the back-wall digital display, far back wall",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "bright even modern office light, cool-neutral white, recessed LED wash, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "small-to-medium export-import office, contract-institutional realism, class-accurate working register"
}
```

### Cell DASBOR — WALL-DISPLAY ANGLE → `E08_kantor_dasbor.png` · ✅ prompt LOCKED · generate PENDING (modernized v2)
Serves SEQ4-SC10-SH01/02/03/05 (afternoon; the wall dashboard + the action desk; 24mm WIDE + 50mm mediums). The large camera-RIGHT wall-mounted display the focal element, OFF/polos (commodity dashboard = AE; no-coal). Orange-afternoon grade = GATE B. **Modern register (v2): sit-stand white desks, back-wall digital display OFF, no clock.**
```json
{
  "environment_reference": "attached reference plate E08_kantor_master.png, same modern export-import office, identical sit-stand desks, identical back-wall digital display, identical camera-RIGHT wall display, identical layout, identical materials, faithful office match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty office stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "modern export-import office workspace, contemporary corporate interior, bright minimalist open-plan, sit-stand desks, glass partition accents, large wall-mounted digital displays, recessed LED ceiling, contract-institutional register, lived-in working office",
  "location": "indoor",
  "time_of_day": "day",
  "atmosphere": "quiet lived-in modern office calm",
  "subject_anchor": {
    "primary_subject": "large wall-mounted flat display screen, camera-RIGHT wall, screen off dark neutral, slim bezel, mounted on a bracket, prominent, front action desk below in the mid-ground, large ultrawide monitor screen off dark neutral",
    "subject_material": "painted plaster office walls cool off-white, matte white laminate desktops, brushed aluminium desk legs, grey polished concrete floor, glass partition panels, real lived-in modern office surfaces",
    "back_display": "large wall-mounted digital display screen, far back wall, centered, wide, slim bezel, screen off dark neutral",
    "supporting_objects": {
      "hero_desk": "front action work desk, matte white desktop, a large ultrawide monitor screen off dark neutral, modern ergonomic mesh task chair, thin document folder, mid-ground below the wall display",
      "desks": "neighbouring sit-stand desks, matte white desktops, slim widescreen monitors screen off dark neutral, soft background",
      "plant": "tall leafy office plant, modern matte planter, beneath the wall display, camera-RIGHT",
      "window_dressing": "wide floor-to-ceiling office window, camera-LEFT background wall, slim roller shade, daylight",
      "floor": "grey polished concrete floor, tidy"
    },
    "human_absence_signal": "unoccupied, still, chair tucked, all screens dark, office quiet, room empty"
  },
  "shot": {
    "composition": "office angle favouring the camera-RIGHT wall, large wall-mounted display screen off dark neutral prominent, front action desk below in the mid-ground, ultrawide monitor screen off, back-wall digital display screen off far back wall, office plant beneath the display, legible",
    "framing": "WS, wall display dominant, action desk in the frame, standing eye-level",
    "angle": "eye-level",
    "camera_position": "from the back of the office, angled toward the camera-RIGHT wall display, the action desk in the mid-ground",
    "camera_direction": "toward the large camera-RIGHT wall display, the action desk, back-wall digital display far back wall",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral interior office light, balanced neutral white, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "small-to-medium export-import office, contract-institutional realism, class-accurate working register"
}
```

---

## 4. Status manifest
| Cell | Angle | File | Serves | Status |
|---|---|---|---|---|
| M | establishing WIDE | `E08_kantor_master.png` | SC05-SH01 | ✅ **GENERATED + ACCEPTED (2026-07-01, modernized v2)** |
| MEJA | front-desk MS | `E08_kantor_meja.png` | SC05-SH02/03/04/05 | ✅ **GENERATED + ACCEPTED (2026-07-01, modernized v2)** |
| DASBOR | wall-display angle | `E08_kantor_dasbor.png` | SC10-SH01/02/03/05 | ✅ **GENERATED + ACCEPTED (2026-07-01, modernized v2)** |

**E08 COMPLETE (3 plates: M + MEJA + DASBOR, all modernized v2 accepted 2026-07-01).**

Storage: `environment-images/E08_kantor/` (+ `_rejected/`). Naming: `E08_kantor_<angle>.png`.
Generate M first (no reference-image). Then MEJA / DASBOR via the `shot`-only-rewrite method: upload `E08_kantor_master.png` as reference + paste §1 verbatim + the cell's `shot` block. Verify each element against the master before locking. Every screen OFF/polos (A1); virtual-workspace board + commodity dashboard = After Effects; no-coal on the dashboard content.

---

*E08 Kantor Ekspor-Impor environment sheet — Fase-2 prompts LOCKED (generate PENDING, sesi baru) · Explainer Video 2 · 2026-07-01 · INT contract-institutional (declared deviation: no IKEA/Hokusai, Caballero corporate realism) · used 2× (SC05 morning + SC10 afternoon) · all screens OFF (A1) · no-coal dashboard (AE) · token-per-token · camera-relative direction.*
