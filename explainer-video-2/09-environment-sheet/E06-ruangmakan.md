---
title: Environment Sheet — E06 Ruang Makan Keluarga · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e06-ruangmakan, gate-0-env, interior]
status: fase2-prompt-locked
created: 2026-06-30
updated: 2026-07-01
aliases: [ev2-e06-ruangmakan, E06-ruangmakan, ruang-makan-env]
---

# Environment Sheet — E06 RUANG MAKAN KELUARGA · tag E06
> Method, scoped-angle rubric, 3 anchors, prompt-structure standard → [[00-README-ENV]] (§2.6). Scene truth → [[03-scene-detail]] SEQ6-SC13 (FINALE). Shotlist → `10-gateB-keyframes/SEQ6-SC13.md`. Furniture lock-anchors → [[tokens-references/INTERIOR-DESIGN-REFERENCE]] §6.
> **Room:** the family dining room — finale convergence (Herman, Ratna, Lisa, Andi at one table; SC13-SH01/SH05 WIDE 4-subjek establishing, SH02/SH04 M Herman at the table, SH03 CU phone insert). 1× use (SC13, last scene of the film). **Same house as E01/E02/E03** — inherits the §3 architecture anchor + material gestalt (matte plaster, IKEA flat-pack laminate, plain desaturated textiles, ceramic floor). Empty-room reference plates, neutral grade; the four family members (Ratna **uncovered**, mahram-only night) + food + warm pendant light + night mood added at GATE B keyframes.

> **Token discipline (locked):** every JSON token value below is a comma-delimited token cluster, NOT a sentence — conjunctions (`and / for / with / bearing`) and prose connectors are banned inside token values (`prompt-rules` b.119). Surrounding markdown is documentation, not pasted into the generator. **Fase-2 status:** prompts LOCKED, **generate PENDING (sesi baru)** — generate is a separate session per the author-all-then-generate workflow.

---

## 1. Room identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E06 angle)
This block stays identical across ALL E06 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E06_ruangmakan_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "family dining room, urban middle-class family home, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, low sideboard, lived-in working-family",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "family dining table, IKEA EKEDALEN oak effect dining table, room centre, four matching EKEDALEN dining chairs around the table, four clean place settings, plain white plates, plain bowls, clear drinking glasses, simple cutlery, plain desaturated table runner, empty serving platter, empty serving bowl, centre",
    "subject_material": "matte painted plaster walls muted off-white, oak effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Rainstorm Beneath the Summit', Thirty-Six Views of Mount Fuji, centered above the sideboard, far back wall",
    "supporting_objects": {
      "sideboard": "IKEA HAVSTA low sideboard buffet, white-stained oak effect, far back wall, beneath the framed print, plain closed cabinet, otherwise tidy",
      "chairs": "four IKEA EKEDALEN dining chairs, oak effect, plain pale seats, around the dining table",
      "window_dressing": "IKEA LILL white sheer net curtains, camera-LEFT wall, drawn",
      "wall_clock": "plain round wall clock, plain white face, camera-RIGHT wall",
      "pendant": "warm-toned pendant lamp, over the table centre, switched off",
      "openings": "open doorway, camera-RIGHT wall, light switch plate beside the doorway",
      "floor": "ceramic-tiled floor, open beneath the table",
      "plant": "small potted leafy green plant, plain terracotta pot, on the sideboard top, camera-RIGHT end"
    },
    "human_absence_signal": "unoccupied, still, chairs tucked, table set clean, serving ware empty, room empty, quiet"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```
**Canonical layout (defined by master, reused by all angles — directions are FROM THE MASTER CAMERA's point of view):** EKEDALEN dining table centered in the room with four matching chairs, set with four clean place settings + empty serving platter/bowl (food + steam = GATE B) · low HAVSTA sideboard on the far BACK wall, framed Hokusai *Rainstorm Beneath the Summit (Black Fuji)* centered above the sideboard, a small potted plant on the sideboard's camera-RIGHT end · LILL-curtained window on the camera-LEFT wall · plain round wall clock + open doorway + light switch on the camera-RIGHT wall · warm pendant lamp over the table (switched off in the neutral plate; warm-ON at GATE B) · ceramic floor open beneath the table. **The 4-chair table is the centre focus; perimeter = sideboard + window + doorway.**

**ADDENDUM A1:** NO device in the empty plate — Herman's phone arrives with him at GATE B. When it appears, its screen renders OFF/neutral and all UI ("Mode Syariah · aktif" opt-in, then the app dimming — the film's LAST commercial graphic) is composited in After Effects. The warm pendant + night grade are GATE B; the plate renders neutral, evenly lit.

**Modesty / wardrobe note:** Ratna is **uncovered** in this scene (mahram-only, night at home) — but plates are empty-room, so no figure appears here; modesty is staged at GATE B.

---

## 2. Method (per [[00-README-ENV]] §2.6)
- **Master generated first, no reference-image.** The MEJA derivative uploads `E06_ruangmakan_master.png` as reference + rewrites ONLY the `shot` block → same room, new camera. (Generate = separate session; at authoring time the derivative only carries the `environment_reference` token.)
- **Same house as E01/E02/E03:** inherits the §3 architecture/material anchor. Dining dressing (EKEDALEN table + 4 chairs + HAVSTA sideboard) differentiates function without breaking the house gestalt.
- **Branded furniture lock-anchors** keep furniture identical across angles — EKEDALEN dining set + HAVSTA sideboard + LILL curtains = house-register IKEA pieces named for strong prior; distinct silhouettes from the other rooms' furniture.
- **Empty plate, no device** — the family + food + phone arrive at GATE B; the plate is a clean, neutrally-lit empty dining room.
- **Fifth distinct named artwork** — Hokusai *Rainstorm Beneath the Summit (Black Fuji)* (E01 = Great Wave, E02 = Red Fuji, E03 = Kajikazawa, E05 = Ejiri); same *Thirty-Six Views* register, distinct image (stormy dark Fuji + lightning at the base, clearly distinguishable from E02's serene Red Fuji) so the rooms stay individually recognizable (§2.6(7) single-work rule). Swappable at Session-B revision.
- **No religious / strong-identity label** in `scene` — class + concrete objects carry the read (`lessons` b.51).
- **Token-per-token values** — no conjunctions inside JSON token values (b.119); comma-delimited clusters only. Negation ban absolute.
- ADDENDUM A1: zero graphics, no device in plate. Neutral grade (warm night at GATE B).

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` SEQ6-SC13 shot-list)
Each cell is a COMPLETE copy-paste-ready prompt, zero scaffold. §1 is the canonical identity-lock; the cells are what you paste. Scoped to E06's two plates: MASTER (establishing WIDE, serves SH01 + SH05 finale) · MEJA (table-end MS, serves SH02/SH04 — Herman at the table; the SH03 phone CU crops tight on hand+phone, no env plate needed). The MEJA derivative uploads `E06_ruangmakan_master.png` as reference-image at generate time.

### Cell M — MASTER · establishing WIDE → `E06_ruangmakan_master.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Full dining-room geography — the anchor plate + the finale wide. Establishes the 4-chair table centre, sideboard + Black Fuji far back wall, window camera-LEFT, doorway camera-RIGHT.
```json
{
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "family dining room, urban middle-class family home, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, low sideboard, lived-in working-family",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "family dining table, IKEA EKEDALEN oak effect dining table, room centre, four matching EKEDALEN dining chairs around the table, four clean place settings, plain white plates, plain bowls, clear drinking glasses, simple cutlery, plain desaturated table runner, empty serving platter, empty serving bowl, centre",
    "subject_material": "matte painted plaster walls muted off-white, oak effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Rainstorm Beneath the Summit', Thirty-Six Views of Mount Fuji, centered above the sideboard, far back wall",
    "supporting_objects": {
      "sideboard": "IKEA HAVSTA low sideboard buffet, white-stained oak effect, far back wall, beneath the framed print, plain closed cabinet, otherwise tidy",
      "chairs": "four IKEA EKEDALEN dining chairs, oak effect, plain pale seats, around the dining table",
      "window_dressing": "IKEA LILL white sheer net curtains, camera-LEFT wall, drawn",
      "wall_clock": "plain round wall clock, plain white face, camera-RIGHT wall",
      "pendant": "warm-toned pendant lamp, over the table centre, switched off",
      "openings": "open doorway, camera-RIGHT wall, light switch plate beside the doorway",
      "floor": "ceramic-tiled floor, open beneath the table",
      "plant": "small potted leafy green plant, plain terracotta pot, on the sideboard top, camera-RIGHT end"
    },
    "human_absence_signal": "unoccupied, still, chairs tucked, table set clean, serving ware empty, room empty, quiet"
  },
  "shot": {
    "composition": "full dining room geography, one frame, EKEDALEN dining table centered, four matching chairs around the table, clean place settings, empty serving platter centre, low HAVSTA sideboard far back wall, framed Hokusai Black Fuji above the sideboard, LILL-curtained window camera-LEFT wall, plain round wall clock camera-RIGHT wall, open doorway camera-RIGHT wall, pendant lamp over the table switched off, ceramic floor, legible",
    "framing": "WS establishing, floor visible bottom 20%, ceiling line visible top, pendant overhead",
    "angle": "eye-level slight low angle",
    "camera_position": "from the end of the room, looking toward far back sideboard wall, night-window wall camera-left, doorway wall camera-right",
    "camera_direction": "down the room over the dining table, toward the sideboard, Hokusai Black Fuji, far back wall, window camera-left, doorway camera-right",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral ambient interior fill, balanced neutral white, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```

### Cell MEJA — TABLE-END MS → `E06_ruangmakan_meja.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Serves SEQ6-SC13-SH02/SH04 (M Herman at the table + phone, 50mm). One end of the dining table at a seated adult's height, the place setting + chair the focal mid-ground, sideboard + Black Fuji behind.
```json
{
  "environment_reference": "attached reference plate E06_ruangmakan_master.png, same family dining room, identical furniture, identical layout, identical materials, single Hokusai Black Fuji print, faithful room match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "family dining room, urban middle-class family home, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, low sideboard, lived-in working-family",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "family dining table, IKEA EKEDALEN oak effect dining table, room centre, four matching EKEDALEN dining chairs around the table, four clean place settings, plain white plates, plain bowls, clear drinking glasses, simple cutlery, plain desaturated table runner, empty serving platter, empty serving bowl, centre",
    "subject_material": "matte painted plaster walls muted off-white, oak effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Rainstorm Beneath the Summit', Thirty-Six Views of Mount Fuji, centered above the sideboard, far back wall",
    "supporting_objects": {
      "sideboard": "IKEA HAVSTA low sideboard buffet, white-stained oak effect, far back wall, beneath the framed print, plain closed cabinet, otherwise tidy",
      "chairs": "four IKEA EKEDALEN dining chairs, oak effect, plain pale seats, around the dining table",
      "window_dressing": "IKEA LILL white sheer net curtains, camera-LEFT wall, drawn",
      "wall_clock": "plain round wall clock, plain white face, camera-RIGHT wall",
      "pendant": "warm-toned pendant lamp, over the table centre, switched off",
      "openings": "open doorway, camera-RIGHT wall, light switch plate beside the doorway",
      "floor": "ceramic-tiled floor, open beneath the table",
      "plant": "small potted leafy green plant, plain terracotta pot, on the sideboard top, camera-RIGHT end"
    },
    "human_absence_signal": "unoccupied, still, chairs tucked, table set clean, serving ware empty, room empty, quiet"
  },
  "shot": {
    "composition": "medium framing on one end of the dining table, EKEDALEN table edge, one clean place setting, a dining chair at the table-end, dominant centre, low HAVSTA sideboard behind, framed Hokusai Black Fuji above the sideboard, compressed back wall, pendant lamp above switched off",
    "framing": "MS, table-end seat fills frame, seated adult height, room compressed behind",
    "angle": "eye-level, seated adult height",
    "camera_position": "across the table from one seat, pushed in from establishing wide, seated adult height",
    "camera_direction": "toward one end of the dining table, the seat, sideboard, framed Hokusai Black Fuji, far back wall",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral ambient interior fill, balanced neutral white, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```

---

## 4. Status manifest
| Cell | Angle | File | Serves | Status |
|---|---|---|---|---|
| M | establishing WIDE | `E06_ruangmakan_master.png` | SC13-SH01/SH05 (finale) | ✅ prompt LOCKED · generate PENDING (sesi baru) |
| MEJA | table-end MS | `E06_ruangmakan_meja.png` | SC13-SH02/SH04 | ✅ prompt LOCKED · generate PENDING (sesi baru) |

Storage: `environment-images/E06_ruangmakan/` (+ `_rejected/`). Naming: `E06_ruangmakan_<angle>.png`.
Generate M first (no reference-image). Then MEJA via the `shot`-only-rewrite method: upload `E06_ruangmakan_master.png` as reference + paste §1 verbatim + the cell's `shot` block. Verify each prop against the master before locking. No device in the plate; phone + UI + warm night grade = GATE B / After Effects.

---

*E06 Ruang Makan environment sheet — Fase-2 prompts LOCKED (generate PENDING, sesi baru) · Explainer Video 2 · 2026-07-01 · INT same house E01–E03 · FINALE convergence (4 figures + food = GATE B) · fifth distinct Hokusai (Black Fuji) · empty plate no-device (A1) · token-per-token · camera-relative direction.*
