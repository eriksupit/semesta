---
title: Environment Sheet — E03 Ruang Belajar · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e03-ruangbelajar, gate-0-env, image-generation]
status: active
created: 2026-06-23
updated: 2026-06-23
aliases: [ev2-e03-ruangbelajar, E03-ruangbelajar, ruang-belajar-env]
---

# Environment Sheet — E03 RUANG BELAJAR · tag E03
> Method, scoped-angle rubric, 3 anchors, prompt-structure standard → [[00-README-ENV]] (§2.6 = prompt structure). Scene truth → [[03-scene-detail]] (SEQ2-SC03, cross-cut dengan SEQ2-SC02). Furniture lock-anchors → [[tokens-references/INTERIOR-DESIGN-REFERENCE]] §6.
> **Room:** Andi's study room (anak 10) — a child's study corner where he follows an online class on a tablet (SEQ2-SC03-SH01 MS Andi+tablet, SH02 CU layar tablet, SH03 MWS Ratna masuk bawa nampan+susu, mengusap kepala Andi). 1× use. **Same house as E01/E02** — inherits the §3 architecture anchor + material gestalt (matte plaster, IKEA flat-pack laminate, plain desaturated textiles). Empty-room reference plates, neutral grade; warm grade + practical light + characters added at GATE B keyframes.

> **Token discipline (locked 2026-06-23):** every JSON token value below is a comma-delimited token cluster, NOT a sentence — conjunctions (`and / for / with / bearing`) and prose connectors are banned inside token values (per `prompt-rules` b.119). Surrounding markdown is documentation, not pasted into the generator.

---

## 1. Room identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E03 angle)
This block stays identical across ALL E03 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E03_ruangbelajar_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "child study room, urban middle-class family home, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, soft small floor rug, low tidy shelving, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "child study station, IKEA PÅHL desk white-stained pine top, far back wall, centered, generic unbranded tablet on a folding stand, screen off dark neutral, centred on the desk, small child desk chair tucked at it",
    "subject_material": "matte painted plaster walls muted off-white, white-stained pine effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Kajikazawa in Kai Province', Thirty-Six Views of Mount Fuji, centered above the desk, far back wall",
    "supporting_objects": {
      "desk": "IKEA PÅHL desk white-stained pine effect, far back wall, centered, generic unbranded tablet on a folding stand, screen off dark neutral, slim closed exercise book, short pencil cup, Rubik's Cube 3x3 colour cube, otherwise uncluttered",
      "chair": "small child desk chair, plain white frame, plain pale seat, tucked at the desk",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, camera-RIGHT wall, closed hardcover storybooks, LEGO Classic small colourful brick build, LEGO brick storage box, small educational desk globe, in the cubes, otherwise tidy",
      "display_figure": "Schleich Tyrannosaurus rex toy figure, museum-realistic sculpt, posed standing, on top of the KALLAX unit, prominent, single hero display piece",
      "rug": "small soft pale grey low-pile child rug, on the open ceramic floor, centre",
      "window_dressing": "IKEA LILL white sheer net curtains, far back wall, camera-right of the desk",
      "pinboard": "small cork pinboard, camera-RIGHT wall, above the KALLAX shelf, educational world map poster pinned, otherwise plain",
      "openings": "open doorway, camera-LEFT wall, light switch plate beside the doorway",
      "lighting_fixture": "plain ceiling lamp switched off, small clip reading lamp clamped at the desk edge, switched off",
      "wall_hook": "modest wall hook, camera-LEFT wall, beside the doorway, plain cloth tote bag"
    },
    "human_absence_signal": "unoccupied, still, chair tucked in, tablet screen dark, room empty, quiet"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```
**Canonical layout (defined by master, reused by all angles — directions are FROM THE MASTER CAMERA's point of view):** PÅHL study desk (centered on the far BACK wall) + tablet-on-stand (screen OFF) + child chair + clip lamp, the LILL-curtained window on the far BACK wall to the desk's camera-RIGHT, framed Kajikazawa print centered above the desk · KALLAX 2x2 cube grid with storybooks + LEGO Classic brick build + LEGO storage box + small desk globe on the camera-RIGHT wall, a Schleich Tyrannosaurus rex toy figure (museum-realistic sculpt; a real-animal subject = public-domain, zero character-IP, after both a named Marvel token AND a de-branded robot still rendered an Iron-Man likeness that tripped the image-similarity guardrail) as the single hero display piece on TOP of the unit, cork pinboard (educational world map poster) above the shelf on the same camera-RIGHT wall · Rubik's Cube on the desk · open doorway + light switch + wall hook (cloth tote) on the camera-LEFT wall (Ratna's entry path) · small soft child rug on the open floor centre. **Furniture lines the perimeter; the centre floor stays clear** so the room reads as a normal child's study room and leaves a clean path for the MWS entry.

**ADDENDUM A1:** ONE device appears, OFF — the tablet on its folding stand (the SEQ2-SC03 online-class tablet). In every plate the screen renders OFF / dark / neutral. All UI (online-class board, "Jawaban Tepat" + star sponsor mark, side ad card, floating screen-preview when the screen faces away) is composited in After Effects.

---

## 2. Method (per [[00-README-ENV]] §2.6)
- **Master generated first, no reference-image.** Each derivative uploads `E03_ruangbelajar_master.png` as reference + rewrites ONLY the `shot` block → same room, new camera.
- **Same house as E01/E02:** inherits the §3 architecture/material anchor (matte plaster, IKEA flat-pack laminate, plain desaturated textiles, ceramic-tiled floor). Child-tier dressing (PÅHL kids desk + child chair + storybooks + named strong-prior toys: a hero Schleich Tyrannosaurus rex figure on the KALLAX top (real-animal subject = public-domain, zero character-IP; a Marvel token AND a de-branded robot both still produced an Iron-Man likeness that tripped the image-similarity guardrail), LEGO build, LEGO storage box, Rubik's Cube, desk globe + educational world map poster) differentiates function without breaking the house gestalt.
- **Branded furniture lock-anchors** keep furniture identical across angles — PÅHL kids desk + KALLAX shelf + LILL curtains = house-register IKEA pieces named for strong prior. PÅHL (child desk) chosen so the silhouette reads distinct from E02's adult MICKE desk.
- **One device, screen OFF** — the tablet on a stand; UI in AE.
- **Third distinct named artwork** — Hokusai *Kajikazawa in Kai Province* (E01 = Great Wave, E02 = Red Fuji); same *Thirty-Six Views* register, distinct image so the three rooms stay individually recognizable (§2.6(7) single-work rule).
- **No religious / strong-identity label** in `scene` — devotion-free room; class + concrete child objects carry the read.
- **Token-per-token values** — no conjunctions inside JSON token values (b.119); comma-delimited clusters only. Negation ban absolute.
- ADDENDUM A1: zero graphics, screen off. Neutral grade (warm at GATE B).

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` SEQ2-SC03 shot-list)
Each cell is a COMPLETE copy-paste-ready prompt, zero scaffold. §1 is the canonical identity-lock; the cells are what you paste. Scoped to E03's three shots: SH01 (MS Andi+tablet, 50mm) · SH02 (CU layar tablet) · SH03 (MWS Ratna enters, doorway path). Derivatives upload `E03_ruangbelajar_master.png` as reference-image.

### Cell M — MASTER · establishing wide → `E03_ruangbelajar_master.png` · ✅ LOCKED v2 (2026-06-23; Schleich T-Rex hero)
Full room geography — the anchor plate. Establishes desk-on-back-wall, shelf camera-RIGHT, doorway camera-LEFT.
```json
{
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "child study room, urban middle-class family home, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, soft small floor rug, low tidy shelving, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "child study station, IKEA PÅHL desk white-stained pine top, far back wall, centered, generic unbranded tablet on a folding stand, screen off dark neutral, centred on the desk, small child desk chair tucked at it",
    "subject_material": "matte painted plaster walls muted off-white, white-stained pine effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Kajikazawa in Kai Province', Thirty-Six Views of Mount Fuji, centered above the desk, far back wall",
    "supporting_objects": {
      "desk": "IKEA PÅHL desk white-stained pine effect, far back wall, centered, generic unbranded tablet on a folding stand, screen off dark neutral, slim closed exercise book, short pencil cup, Rubik's Cube 3x3 colour cube, otherwise uncluttered",
      "chair": "small child desk chair, plain white frame, plain pale seat, tucked at the desk",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, camera-RIGHT wall, closed hardcover storybooks, LEGO Classic small colourful brick build, LEGO brick storage box, small educational desk globe, in the cubes, otherwise tidy",
      "display_figure": "Schleich Tyrannosaurus rex toy figure, museum-realistic sculpt, posed standing, on top of the KALLAX unit, prominent, single hero display piece",
      "rug": "small soft pale grey low-pile child rug, on the open ceramic floor, centre",
      "window_dressing": "IKEA LILL white sheer net curtains, far back wall, camera-right of the desk",
      "pinboard": "small cork pinboard, camera-RIGHT wall, above the KALLAX shelf, educational world map poster pinned, otherwise plain",
      "openings": "open doorway, camera-LEFT wall, light switch plate beside the doorway",
      "lighting_fixture": "plain ceiling lamp switched off, small clip reading lamp clamped at the desk edge, switched off",
      "wall_hook": "modest wall hook, camera-LEFT wall, beside the doorway, plain cloth tote bag"
    },
    "human_absence_signal": "unoccupied, still, chair tucked in, tablet screen dark, room empty, quiet"
  },
  "shot": {
    "composition": "full room geography, one frame, PÅHL desk, tablet on stand, framed Kajikazawa above it, far back wall, curtained window camera-right of the desk, KALLAX cube shelf, camera-RIGHT wall, Schleich Tyrannosaurus rex toy figure on top of the shelf, open doorway, light switch, camera-LEFT wall, small child rug, open floor centre, legible",
    "framing": "WS establishing, floor visible bottom 20%, ceiling line visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "front of room, looking toward far back curtained-window wall, shelf wall camera-right, doorway wall camera-left",
    "camera_direction": "straight down the room, desk, Kajikazawa, window, far back wall, shelf camera-right, doorway camera-left, open floor centre",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "soft diffused daylight key from the curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```

### Cell D — DESK / study-station MS → `E03_ruangbelajar_desk.png` · ✅ LOCKED (2026-06-23)
Serves SEQ2-SC03-SH01 (MS Andi + tablet) — the desk station at a seated child's height, tablet-on-stand the focal mid-ground.
```json
{
  "environment_reference": "attached reference plate E03_ruangbelajar_master.png, same child study room, identical furniture, identical layout, identical materials, single Hokusai Kajikazawa print, faithful room match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "child study room, urban middle-class family home, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, soft small floor rug, low tidy shelving, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "child study station, IKEA PÅHL desk white-stained pine top, far back wall, centered, generic unbranded tablet on a folding stand, screen off dark neutral, centred on the desk, small child desk chair tucked at it",
    "subject_material": "matte painted plaster walls muted off-white, white-stained pine effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Kajikazawa in Kai Province', Thirty-Six Views of Mount Fuji, centered above the desk, far back wall",
    "supporting_objects": {
      "desk": "IKEA PÅHL desk white-stained pine effect, far back wall, centered, generic unbranded tablet on a folding stand, screen off dark neutral, slim closed exercise book, short pencil cup, Rubik's Cube 3x3 colour cube, otherwise uncluttered",
      "chair": "small child desk chair, plain white frame, plain pale seat, tucked at the desk",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, camera-RIGHT wall, closed hardcover storybooks, LEGO Classic small colourful brick build, LEGO brick storage box, small educational desk globe, in the cubes, otherwise tidy",
      "display_figure": "Schleich Tyrannosaurus rex toy figure, museum-realistic sculpt, posed standing, on top of the KALLAX unit, prominent, single hero display piece",
      "rug": "small soft pale grey low-pile child rug, on the open ceramic floor, centre",
      "window_dressing": "IKEA LILL white sheer net curtains, far back wall, camera-right of the desk",
      "pinboard": "small cork pinboard, camera-RIGHT wall, above the KALLAX shelf, educational world map poster pinned, otherwise plain",
      "openings": "open doorway, camera-LEFT wall, light switch plate beside the doorway",
      "lighting_fixture": "plain ceiling lamp switched off, small clip reading lamp clamped at the desk edge, switched off",
      "wall_hook": "modest wall hook, camera-LEFT wall, beside the doorway, plain cloth tote bag"
    },
    "human_absence_signal": "unoccupied, still, chair tucked in, tablet screen dark, room empty, quiet"
  },
  "shot": {
    "composition": "medium framing on the desk station, PÅHL desk, tablet on stand, screen off dark neutral, child chair tucked at it, dominant centre, framed Kajikazawa above, curtained window behind, sliver of KALLAX shelf, camera-RIGHT edge, compressed back wall",
    "framing": "MS, desk station fills frame, seated child height, room compressed behind",
    "angle": "eye-level, seated child height",
    "camera_position": "in front of the desk, pushed in from establishing wide, seated child height",
    "camera_direction": "toward the desk, tablet on stand, framed Kajikazawa, curtained window, far back wall",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft diffused daylight key from the curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "2:3"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```

### Cell T — TABLET screen insert CS → `E03_ruangbelajar_tablet.png` · ✅ LOCKED (2026-06-23)
Serves SEQ2-SC03-SH02 (CU layar tablet) — detail of the tablet-on-stand; screen renders OFF/neutral per A1, online-class UI + sponsor star added in AE.
```json
{
  "environment_reference": "attached reference plate E03_ruangbelajar_master.png, same child study room, identical furniture, identical layout, identical materials, single Hokusai Kajikazawa print, faithful room match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "child study room, urban middle-class family home, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, soft small floor rug, low tidy shelving, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "generic unbranded tablet on a folding stand, screen off dark neutral, IKEA PÅHL desk white-stained pine top, slim closed exercise book, short pencil cup, beside the tablet stand, otherwise uncluttered surface",
    "subject_material": "matte painted plaster walls muted off-white, white-stained pine effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Kajikazawa in Kai Province', Thirty-Six Views of Mount Fuji, centered above the desk, far back wall",
    "supporting_objects": {
      "desk": "IKEA PÅHL desk white-stained pine effect, tablet on a folding stand, screen off dark neutral, slim closed exercise book, short pencil cup, Rubik's Cube 3x3 colour cube, otherwise uncluttered",
      "chair": "small child desk chair, plain white frame, plain pale seat, tucked at the desk",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, camera-RIGHT wall, closed hardcover storybooks, LEGO Classic small colourful brick build, small educational desk globe, in the cubes, otherwise tidy",
      "display_figure": "Schleich Tyrannosaurus rex toy figure, museum-realistic sculpt, posed standing, on top of the KALLAX unit, prominent, single hero display piece",
      "rug": "small soft pale grey low-pile child rug, on the open ceramic floor, centre",
      "window_dressing": "IKEA LILL white sheer net curtains, far back wall, camera-right of the desk",
      "pinboard": "small cork pinboard, camera-RIGHT wall, above the KALLAX shelf, educational world map poster pinned, otherwise plain",
      "openings": "open doorway, camera-LEFT wall, light switch plate beside the doorway",
      "lighting_fixture": "small clip reading lamp clamped at the desk edge, switched off",
      "wall_hook": "modest wall hook, camera-LEFT wall, beside the doorway, plain cloth tote bag"
    },
    "human_absence_signal": "unoccupied, still, tablet screen dark, room empty, quiet"
  },
  "shot": {
    "composition": "close detail, tablet on a folding stand, dark neutral screen filling centre, PÅHL desk top, slim closed exercise book, short pencil cup beside the tablet stand, otherwise uncluttered, sliver of curtained window behind",
    "framing": "CS insert, tablet screen, desk surface, dark screen legible as off",
    "angle": "eye-level slight high angle, onto the tablet screen",
    "camera_position": "close in front of the desk, seated child height",
    "camera_direction": "toward the off tablet screen, desk top",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft diffused daylight key from the curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "4:5"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```

### Cell W — DOORWAY MWS → `E03_ruangbelajar_doorway.png` · ✅ LOCKED (2026-06-23)
Serves SEQ2-SC03-SH03 (MWS, Ratna enters with the tray) — wider plate keeping the camera-LEFT doorway + the clear floor path to the desk visible.
```json
{
  "environment_reference": "attached reference plate E03_ruangbelajar_master.png, same child study room, identical furniture, identical layout, identical materials, single Hokusai Kajikazawa print, faithful room match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "child study room, urban middle-class family home, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, soft small floor rug, low tidy shelving, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "open clear floor path, room centre, kept free, soft small child rug, centre, leading from the camera-LEFT doorway to the PÅHL desk station, far back wall",
    "subject_material": "matte painted plaster walls muted off-white, white-stained pine effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Kajikazawa in Kai Province', Thirty-Six Views of Mount Fuji, centered above the desk, far back wall",
    "supporting_objects": {
      "desk": "IKEA PÅHL desk white-stained pine effect, far back wall, centered, generic unbranded tablet on a folding stand, screen off dark neutral, slim closed exercise book, short pencil cup, Rubik's Cube 3x3 colour cube, otherwise uncluttered",
      "chair": "small child desk chair, plain white frame, plain pale seat, tucked at the desk",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, camera-RIGHT wall, closed hardcover storybooks, LEGO Classic small colourful brick build, LEGO brick storage box, small educational desk globe, in the cubes, otherwise tidy",
      "display_figure": "Schleich Tyrannosaurus rex toy figure, museum-realistic sculpt, posed standing, on top of the KALLAX unit, prominent, single hero display piece",
      "rug": "small soft pale grey low-pile child rug, on the open ceramic floor, centre",
      "window_dressing": "IKEA LILL white sheer net curtains, far back wall, camera-right of the desk",
      "pinboard": "small cork pinboard, camera-RIGHT wall, above the KALLAX shelf, educational world map poster pinned, otherwise plain",
      "openings": "open doorway, camera-LEFT wall, light switch plate beside the doorway, hallway beyond",
      "lighting_fixture": "plain ceiling lamp switched off, small clip reading lamp clamped at the desk edge, switched off",
      "wall_hook": "modest wall hook, camera-LEFT wall, beside the doorway, plain cloth tote bag"
    },
    "human_absence_signal": "unoccupied, still, doorway open, chair tucked in, tablet screen dark, room empty, quiet"
  },
  "shot": {
    "composition": "wider framing, open doorway prominent, camera-LEFT, light switch beside the doorway, clear floor path, room centre, leading to the PÅHL desk, tablet on stand, framed Kajikazawa, far back wall, KALLAX shelf, camera-RIGHT, Schleich Tyrannosaurus rex toy figure on top of the shelf, child rug on the floor",
    "framing": "MWS, doorway visible, floor path visible, desk station mid-ground, standing eye-level",
    "angle": "eye-level",
    "camera_position": "set back near the camera-RIGHT shelf wall, angled across the room toward the camera-LEFT doorway, back-wall desk",
    "camera_direction": "across the open floor, toward the camera-LEFT doorway, back-wall desk station, shelf camera-right foreground",
    "camera": "35mm prime spherical, deep focus front to back",
    "lighting": "soft diffused daylight key from the curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```

---

## 4. Status manifest
| Cell | Angle | File | Status |
|---|---|---|---|
| M | establishing wide | `E03_ruangbelajar_master.png` | ✅ LOCKED (2026-06-23 v2; Schleich T-Rex hero — green dino, zero character-IP; camera-anchored layout + A1 screens-off verified. Derivative-D guardrail pass = final confirmation pending) |
| D | desk / study-station MS | `E03_ruangbelajar_desk.png` | ✅ LOCKED (2026-06-23; reference-locked to master, T-Rex + props consistent; PROVES the image-similarity guardrail now passes after the subject-category swap) |
| T | tablet screen insert | `E03_ruangbelajar_tablet.png` | ✅ LOCKED (2026-06-23; tablet screen-OFF A1-compliant, Rubik's Cube verified in tight framing, consistent with master) |
| W | doorway MWS | `E03_ruangbelajar_doorway.png` | ✅ LOCKED (2026-06-23; doorway camera-LEFT + shelf/T-Rex camera-RIGHT + back-wall desk — camera-relative audit re-validated; consistent with master) |

Storage: `environment-images/E03_ruangbelajar/` (+ `_rejected/`). Naming: `E03_ruangbelajar_<angle>.png`.
Generate M first (no reference-image). Then D / T / W via the `shot`-only-rewrite method: upload `E03_ruangbelajar_master.png` as reference + paste §1 verbatim + the cell's `shot` block. Verify each prop against the master image before locking.

---

*E03 Ruang Belajar environment sheet v1.0 (COMPLETE 4/4) · Explainer Video 2 · 2026-06-23 · method [[00-README-ENV]] · same house as [[E01-kamar]] / [[E02-ruangkeluarga]] · token-per-token values · third distinct Hokusai (Kajikazawa) · Schleich T-Rex hero (subject-swap after Iron-Man IP/likeness block) · camera-relative direction audited*
