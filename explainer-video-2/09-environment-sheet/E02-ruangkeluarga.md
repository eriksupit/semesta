---
title: Environment Sheet — E02 Ruang Keluarga · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e02-ruangkeluarga, gate-0-env, image-generation]
status: active
created: 2026-06-22
updated: 2026-06-23
aliases: [ev2-e02-ruangkeluarga, E02-ruangkeluarga, ruang-keluarga-env]
---

# Environment Sheet — E02 RUANG KELUARGA · tag E02
> Method, scoped-angle rubric, 3 anchors, prompt-structure standard → [[00-README-ENV]] (§2.6 = prompt structure). Scene truth → [[03-scene-detail]] (SEQ1-SC02 sholat subuh + SEQ6-SC02 ngaji ba'da Maghrib). Furniture lock-anchors → [[tokens-references/INTERIOR-DESIGN-REFERENCE]] §6.
> **Room:** the family's shared living room — both a prayer space (SEQ1-SC02 sholat subuh berjamaah, family forms a saf, Herman as imam) and a floor-seating study space (SEQ6-SC02 ngaji ba'da Maghrib, Ratna + Andi on the floor, digital kitab on a screen). Two sacred/ad-free zones. **Same house as E01** — inherits the §3 architecture anchor + material gestalt. Empty-room reference plates, neutral grade; warm grade + practical light + characters added at GATE B keyframes.

> **Token discipline (locked 2026-06-23):** every JSON token value below is a comma-delimited token cluster, NOT a sentence — conjunctions (`and / for / with / bearing`) and prose connectors are banned inside token values (per `prompt-rules` b.119). The surrounding markdown (this note, canonical layout, method, ADDENDUM) is documentation, not pasted into the generator.

---

## 1. Room identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E02 angle)
This block stays identical across ALL E02 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E02_ruangkeluarga_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "shared living room, urban middle-class family, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, open ceramic-tiled floor kept clear, floor seating, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "open clear ceramic-tiled floor, centre of room, kept free, floor seating, low flat-weave floor mat unrolled, two flat floor cushions, one edge",
    "subject_material": "matte painted plaster walls muted off-white, oak-effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Fine Wind, Clear Morning (Red Fuji)', Thirty-Six Views of Mount Fuji, centered camera-left wall, above the sofa",
    "supporting_objects": {
      "desk": "IKEA MICKE desk oak-effect, far back wall, beside curtained window, generic unbranded all-in-one desktop, screen off dark neutral, slim wireless keyboard, mouse, before the monitor, black swivel office chair tucked at desk, otherwise uncluttered",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, against the wall, rolled prayer mat, closed hardcover book, in the cubes, otherwise tidy",
      "sofa": "IKEA EKTORP two-seat sofa, beige linen-blend slipcover, camera-left wall, beneath the framed Red Fuji print, facing the television on the camera-right wall, open floor between",
      "tv_bench": "IKEA BESTÅ TV bench, white-stained oak-effect, low closed flat-door media cabinet, camera-right wall, directly facing the sofa, open floor between, flat-screen television, screen off dark neutral",
      "seating_zone": "low flat-weave floor mat, two plain floor cushions, on the open floor, seating use",
      "window_dressing": "IKEA LILL white sheer net curtains, far back-wall window",
      "rug": "IKEA PERSISK HAMADAN handmade oriental wool rug, low pile, one side of the open floor",
      "openings": "open doorway, one wall, light switch plate beside it",
      "lighting_fixture": "plain ceiling lamp switched off, modest wall hook, folded plain headscarf"
    },
    "human_absence_signal": "unoccupied, still, floor mat unrolled, cushions waiting, room empty, quiet"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```
**Canonical layout (defined by master, reused by all angles — directions are FROM THE MASTER CAMERA's point of view):** EKTORP sofa on the camera-LEFT wall with the framed Red Fuji print centered above it · BESTÅ TV bench + off-screen TV on the camera-RIGHT wall directly facing the sofa · open clear floor centre between them kept for saf/floor-seating · MICKE desk + swivel chair + all-in-one desktop (screen OFF) + keyboard + mouse on the far BACK wall beside the LILL-curtained window · KALLAX 2x2 cube grid with rolled prayer mat + hardcover kitab in the cubes · open doorway + light switch on one wall · PERSISK rug to one side. **Furniture lines the perimeter; the centre floor stays clear** so the room reads as a normal lived-in family living room AND leaves space for the prayer saf / floor-seating ngaji.

**ADDENDUM A1:** TWO devices appear, BOTH off — the family flat-screen TV on the TV bench, and the all-in-one desktop on the MICKE desk (the desktop = SEQ1-SC02-SH01 order browser AND the SEQ6-SC02 digital-kitab monitor, same device). In every plate every screen renders OFF / dark / neutral. All UI (order browser, packaging ad card, digital kitab with tajwid highlight) is composited in After Effects. Meja makan is NOT here — it belongs to E06_ruangmakan (separate env).

---

## 2. Method (per [[00-README-ENV]] §2.6)
- **Master generated first, no reference-image.** Each derivative uploads `E02_ruangkeluarga_master.png` as reference + rewrites ONLY the `shot` block → same room, new camera.
- **Same house as E01:** inherits the §3 architecture/material anchor (matte plaster, IKEA flat-pack laminate, plain desaturated textiles, ceramic-tiled floor) + the house wall-art register (single Hokusai Red Fuji).
- **Branded furniture lock-anchors** keep furniture identical across angles ([[tokens-references/INTERIOR-DESIGN-REFERENCE]] §6 verbatim where listed; MICKE desk + KALLAX shelf + EKTORP sofa + BESTÅ TV bench = house-register IKEA pieces named for strong prior).
- **One device serves both scenes** — the all-in-one desktop = the digital-kitab monitor; screen OFF, UI in AE.
- **No religious-identity label** in `scene` (keyword-leak — pulled calligraphy over Hokusai on E01; E02 uses a DIFFERENT Hokusai work (Red Fuji) so the two rooms stay distinct); devotion carried by concrete objects (rolled prayer mat, floor seating, kitab, headscarf) + social class only.
- **Token-per-token values** — no conjunctions inside JSON token values (b.119); comma-delimited clusters only.
- ADDENDUM A1: zero graphics, screens off. Neutral grade (warm at GATE B).

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` shot-list)
Each cell below is a COMPLETE copy-paste-ready prompt, per SOP — zero scaffold. §1 is the canonical identity-lock; the cells are what you paste. Scoped to E02's shots: SEQ1-SC02 (WS room + dark window + desktop, MS sajadah, WS saf takbir, WS/high-angle sujud) + SEQ6-SC02 (MS Ratna+Andi floor seating + monitor, CU kitab↔monitor). Derivatives upload `E02_ruangkeluarga_master.png` as reference-image.

### Cell M — MASTER · establishing wide → `E02_ruangkeluarga_master.png` · ✅ LOCKED (v2, token-ified + keyboard/mouse)
Serves SEQ1-SC02-SH01 (WS room, window, desktop) + SH03 (WS saf takbir).
```json
{
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "shared living room, urban middle-class family, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, open ceramic-tiled floor kept clear, floor seating, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "open clear ceramic-tiled floor, centre of room, kept free, floor seating, low flat-weave floor mat unrolled, two flat floor cushions, one edge",
    "subject_material": "matte painted plaster walls muted off-white, oak-effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Fine Wind, Clear Morning (Red Fuji)', Thirty-Six Views of Mount Fuji, centered camera-left wall, above the sofa",
    "supporting_objects": {
      "desk": "IKEA MICKE desk oak-effect, far back wall, beside curtained window, generic unbranded all-in-one desktop, screen off dark neutral, slim wireless keyboard, mouse, before the monitor, black swivel office chair tucked at desk, otherwise uncluttered",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, against the wall, rolled prayer mat, closed hardcover book, in the cubes, otherwise tidy",
      "sofa": "IKEA EKTORP two-seat sofa, beige linen-blend slipcover, camera-left wall, beneath the framed Red Fuji print, facing the television on the camera-right wall, open floor between",
      "tv_bench": "IKEA BESTÅ TV bench, white-stained oak-effect, low closed flat-door media cabinet, camera-right wall, directly facing the sofa, open floor between, flat-screen television, screen off dark neutral",
      "seating_zone": "low flat-weave floor mat, two plain floor cushions, on the open floor, seating use",
      "window_dressing": "IKEA LILL white sheer net curtains, far back-wall window",
      "rug": "IKEA PERSISK HAMADAN handmade oriental wool rug, low pile, one side of the open floor",
      "openings": "open doorway, one wall, light switch plate beside it",
      "lighting_fixture": "plain ceiling lamp switched off, modest wall hook, folded plain headscarf"
    },
    "human_absence_signal": "unoccupied, still, floor mat unrolled, cushions waiting, room empty, quiet"
  },
  "shot": {
    "composition": "full room geography, one frame, EKTORP sofa, framed Red Fuji above it, camera-LEFT side, BESTÅ TV bench, off-screen television, camera-RIGHT side, directly facing the sofa, open floor, unrolled mat, centred between, MICKE desk, off-screen all-in-one desktop, keyboard, mouse, swivel chair, curtained window, far back wall, KALLAX cube shelf, open doorway, legible",
    "framing": "WS establishing, floor visible bottom 20%, ceiling line visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "front of room, looking toward far back curtained-window wall, sofa wall camera-left, TV wall camera-right",
    "camera_direction": "straight down the room, sofa, Red Fuji, camera-left, facing TV bench, camera-right, open floor, mat, centred between, desk, window, far back wall",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "soft diffused daylight key, curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```

### Cell P — PRAYER high-angle wide → `E02_ruangkeluarga_prayer_high.png` · ✅ LOCKED v2
Serves SEQ1-SC02-SH04 (soft high-angle, sujud) — the open floor where the saf forms, seen from above-soft.
```json
{
  "environment_reference": "attached reference plate E02_ruangkeluarga_master.png, same living room, identical furniture, identical layout, identical materials, single Hokusai Red Fuji print, faithful room match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "shared living room, urban middle-class family, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, open ceramic-tiled floor kept clear, floor seating, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "open clear ceramic-tiled floor, centre of room, kept free, floor seating, low flat-weave floor mat unrolled, two flat floor cushions, one edge",
    "subject_material": "matte painted plaster walls muted off-white, oak-effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Fine Wind, Clear Morning (Red Fuji)', Thirty-Six Views of Mount Fuji, centered camera-left wall, above the sofa",
    "supporting_objects": {
      "desk": "IKEA MICKE desk oak-effect, far back wall, beside curtained window, generic unbranded all-in-one desktop, screen off dark neutral, slim wireless keyboard, mouse, before the monitor, black swivel office chair tucked at desk, otherwise uncluttered",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, against the wall, rolled prayer mat, closed hardcover book, in the cubes, otherwise tidy",
      "sofa": "IKEA EKTORP two-seat sofa, beige linen-blend slipcover, camera-left wall, beneath the framed Red Fuji print, facing the television on the camera-right wall, open floor between",
      "tv_bench": "IKEA BESTÅ TV bench, white-stained oak-effect, low closed flat-door media cabinet, camera-right wall, directly facing the sofa, open floor between, flat-screen television, screen off dark neutral",
      "seating_zone": "low flat-weave floor mat, two plain floor cushions, on the open floor, seating use",
      "window_dressing": "IKEA LILL white sheer net curtains, far back-wall window",
      "rug": "IKEA PERSISK HAMADAN handmade oriental wool rug, low pile, one side of the open floor",
      "openings": "open doorway, one wall, light switch plate beside it",
      "lighting_fixture": "plain ceiling lamp switched off, modest wall hook, folded plain headscarf"
    },
    "human_absence_signal": "unoccupied, still, floor mat unrolled, cushions waiting, room empty, quiet"
  },
  "shot": {
    "composition": "elevated downward view, unrolled floor mat, two cushions, prominent, centred, open ceramic floor around them, prayer line, EKTORP sofa, camera-LEFT, BESTÅ TV bench, camera-RIGHT, desk, curtained window, upper back, room read from above standing height",
    "framing": "high-angle WS, floor and mat prominent, modest ceiling strip top",
    "angle": "soft high angle, about forty-five degrees downward onto the open floor",
    "camera_position": "elevated above standing height, near the doorway corner, tilted down forty-five degrees",
    "camera_direction": "tilted down about forty-five degrees across the open floor onto the mat, sofa wall camera-left, TV wall camera-right, back window wall upper frame",
    "camera": "35mm prime spherical, deep focus front to back",
    "lighting": "soft diffused daylight key, curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```

### Cell F — FLOOR-SEATING → `E02_ruangkeluarga_floorseat.png` · ✅ LOCKED v2
Serves SEQ6-SC02-SH01 (MS Ratna + Andi on the floor, monitor beside them) — the floor-seating zone with the desk + screen device adjacent.
```json
{
  "environment_reference": "attached reference plate E02_ruangkeluarga_master.png, same living room, identical furniture, identical layout, identical materials, single Hokusai Red Fuji print, faithful room match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "shared living room, urban middle-class family, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, open ceramic-tiled floor kept clear, floor seating, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "open clear ceramic-tiled floor, centre of room, kept free, floor seating, low flat-weave floor mat unrolled, two flat floor cushions, one edge",
    "subject_material": "matte painted plaster walls muted off-white, oak-effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Fine Wind, Clear Morning (Red Fuji)', Thirty-Six Views of Mount Fuji, centered camera-left wall, above the sofa",
    "supporting_objects": {
      "desk": "IKEA MICKE desk oak-effect, far back wall, beside curtained window, generic unbranded all-in-one desktop, screen off dark neutral, slim wireless keyboard, mouse, before the monitor, black swivel office chair tucked at desk, otherwise uncluttered",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, against the wall, rolled prayer mat, closed hardcover book, in the cubes, otherwise tidy",
      "sofa": "IKEA EKTORP two-seat sofa, beige linen-blend slipcover, camera-left wall, beneath the framed Red Fuji print, facing the television on the camera-right wall, open floor between",
      "tv_bench": "IKEA BESTÅ TV bench, white-stained oak-effect, low closed flat-door media cabinet, camera-right wall, directly facing the sofa, open floor between, flat-screen television, screen off dark neutral",
      "seating_zone": "low flat-weave floor mat, two plain floor cushions, on the open floor, seating use",
      "window_dressing": "IKEA LILL white sheer net curtains, far back-wall window",
      "rug": "IKEA PERSISK HAMADAN handmade oriental wool rug, low pile, one side of the open floor",
      "openings": "open doorway, one wall, light switch plate beside it",
      "lighting_fixture": "plain ceiling lamp switched off, modest wall hook, folded plain headscarf"
    },
    "human_absence_signal": "unoccupied, still, floor mat unrolled, cushions waiting, room empty, quiet"
  },
  "shot": {
    "composition": "tight on floor-seating zone, unrolled floor mat, two cushions, large, dominant, lower half of frame, MICKE desk, off-screen all-in-one desktop, keyboard, mouse, swivel chair, just beyond the mat, mid-ground, screen the seaters face, near edge of EKTORP sofa, camera-LEFT, near edge of BESTÅ TV bench, camera-RIGHT, grazing the frame borders",
    "framing": "tight MS, pushed in much closer than establishing wide, mat, cushions, lower half, room compressed behind, close seated-height medium shot",
    "angle": "very low angle, cushion height, close to the floor",
    "camera_position": "low to the ground, just behind the cushions, pushed in close to seating zone, well forward of establishing-wide position",
    "camera_direction": "skimming low across mat, cushions, toward MICKE desk, off-screen monitor, mid-ground",
    "camera": "50mm prime spherical, seated-height medium shot, deep focus front to back",
    "lighting": "soft diffused daylight key, curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```

### Cell S — SCREEN / DESKTOP insert → `E02_ruangkeluarga_screen.png` · ✅ LOCKED v2 (keyboard+mouse verified)
Detail of the device area — SEQ1-SC02-SH01 (desktop waking) + SEQ6-SC02-SH02 (CU kitab ↔ monitor). Screen renders OFF/neutral per A1; UI (order browser / digital kitab) added in AE.
```json
{
  "environment_reference": "attached reference plate E02_ruangkeluarga_master.png, same living room, identical furniture, identical layout, identical materials, single Hokusai Red Fuji print, faithful room match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "shared living room, urban middle-class family, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, open ceramic-tiled floor kept clear, floor seating, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "generic unbranded all-in-one desktop, IKEA MICKE desk oak-effect, black swivel office chair tucked at it, slim wireless keyboard, mouse, before the monitor, screen off dark neutral, otherwise uncluttered surface",
    "subject_material": "matte painted plaster walls muted off-white, oak-effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Fine Wind, Clear Morning (Red Fuji)', Thirty-Six Views of Mount Fuji, centered camera-left wall, above the sofa",
    "supporting_objects": {
      "desk": "IKEA MICKE desk oak-effect, black swivel office chair tucked at it, off-screen all-in-one desktop, slim wireless keyboard, mouse, before the monitor, closed hardcover book, otherwise uncluttered",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, against the wall, rolled prayer mat in the cubes, otherwise tidy",
      "sofa": "IKEA EKTORP two-seat sofa, beige linen-blend slipcover, camera-left wall, beneath the framed Red Fuji print, facing the television on the camera-right wall, open floor between",
      "tv_bench": "IKEA BESTÅ TV bench, white-stained oak-effect, low closed flat-door media cabinet, camera-right wall, directly facing the sofa, open floor between, flat-screen television, screen off dark neutral",
      "seating_zone": "low flat-weave floor mat, two plain floor cushions, on the open floor, seating use",
      "window_dressing": "IKEA LILL white sheer net curtains, far back-wall window",
      "rug": "IKEA PERSISK HAMADAN handmade oriental wool rug, low pile, one side of the open floor",
      "openings": "open doorway, one wall, light switch plate beside it",
      "lighting_fixture": "plain ceiling lamp switched off, modest wall hook, folded plain headscarf"
    },
    "human_absence_signal": "unoccupied, still, screen dark, room empty, quiet"
  },
  "shot": {
    "composition": "close detail, MICKE desk, off-screen all-in-one desktop, swivel chair, dark neutral screen filling centre, slim wireless keyboard, mouse, before the monitor, closed hardcover book beside it, otherwise uncluttered, sliver of far back wall behind",
    "framing": "CS insert, desktop screen, table surface, dark screen legible as off",
    "angle": "eye-level slight high angle, onto the screen",
    "camera_position": "close in front of the desk, sitting height",
    "camera_direction": "toward off all-in-one screen, table top",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft diffused daylight key, curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "4:5"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```

### Cell R — REVERSE establishing wide (prayer master) → `E02_ruangkeluarga_reverse.png` · ✅ LOCKED (2026-06-24)
Serves SEQ1-SC02 prayer (SH02 + SH03) — a NEW camera axis, the reverse of the master, so the scene gains a real angle change after the lamp comes on and the family can pray facing the window/camera (no makmum cramming into the TV wall).
> **Deviasi sadar dari SOP "paste §1 verbatim":** ini sudut 180° berbalik, jadi arah camera-relatif §1 (sofa camera-LEFT, TV camera-RIGHT) **dibalik** di sel ini (sofa→camera-RIGHT, TV→camera-LEFT) supaya konsisten dengan kamera baru. Identitas objek + materi + Red Fuji tetap; konsistensi dijamin oleh upload `E02_ruangkeluarga_master.png` sebagai reference-image. Generate: upload master sebagai reference + paste sel ini.
```json
{
  "environment_reference": "attached reference plate E02_ruangkeluarga_master.png, same living room, identical furniture, identical layout, identical materials, single Hokusai Red Fuji print, faithful room match, NEW reverse camera shooting back from the window-desk wall toward the front doorway side of the room, the master's camera-left and camera-right sides therefore mirrored",
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "shared living room, urban middle-class family, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, open ceramic-tiled floor kept clear, floor seating, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "open clear ceramic-tiled floor, centre of room, the PERSISK HAMADAN oriental wool rug low pile laid flat as the central floor covering, the open prayer floor, kept clear",
    "subject_material": "matte painted plaster walls muted off-white, oak-effect laminate furniture, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Fine Wind, Clear Morning (Red Fuji)', Thirty-Six Views of Mount Fuji, above the sofa on the camera-right wall",
    "supporting_objects": {
      "sofa": "IKEA EKTORP two-seat sofa, beige linen-blend slipcover, camera-right wall, beneath the framed Red Fuji print",
      "tv_bench": "IKEA BESTÅ TV bench, white-stained oak-effect, low closed flat-door media cabinet, camera-left wall, flat-screen television, screen off dark neutral, two plain floor cushions set beside the TV bench",
      "doorway": "open doorway, light switch plate beside it, on the far front wall ahead of the camera",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, against a side wall, rolled prayer mat, closed hardcover book, in the cubes",
      "behind_camera": "the MICKE desk, all-in-one desktop screen off, the LILL-curtained window, on the wall the camera backs onto, out of frame",
      "lighting_fixture": "plain ceiling lamp switched off"
    },
    "human_absence_signal": "unoccupied, still, rug laid flat, room empty, quiet"
  },
  "shot": {
    "composition": "reverse establishing view across the open floor, PERSISK rug, centre, foreground, EKTORP sofa, framed Red Fuji, camera-RIGHT, BESTÅ TV bench, off-screen television, two cushions, camera-LEFT, open doorway, light switch, far front wall ahead, KALLAX cube shelf, side wall, legible",
    "framing": "WS establishing, floor and rug prominent bottom third, ceiling line visible top, the front doorway wall across the background",
    "angle": "eye-level slight low angle",
    "camera_position": "near the back window-desk wall, back to the curtained window, looking across the open floor toward the front doorway wall",
    "camera_direction": "from the window-desk wall across the open floor toward the doorway wall, sofa wall camera-right, TV wall camera-left",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "soft diffused daylight key, the curtained window wall behind the camera, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```

---

### Cell R2 — REVERSE prayer plate WITH four colour-tagged mats → `E02_ruangkeluarga_reverse_prayer.png` · ✅ LOCKED (2026-06-24)
Derived from **Cell R** (same room, same reverse camera, upload `E02_ruangkeluarga_master.png` as reference) with four plain colour-tagged prayer mats baked onto the PERSISK rug in a 1-1-2 saf, placed by canvas coordinates + membujur (long-axis-toward-camera) orientation. Serves SEQ1-SC02 prayer (SH02 + SH03); keyframes reference the mats by colour instead of conjuring them in text. **Identical to Cell R except: (a) add the `prayer_mats` object below into `subject_anchor.supporting_objects`; (b) `primary_subject` & `shot.composition` mention "four plain prayer mats, each a different muted colour, 1-1-2 formation receding in depth"; (c) filename `…_reverse_prayer.png`.** Mat ownership for keyframe placement: **sage-green front = Herman (imam) · dusty-blue middle = Andi · terracotta back-left = Lisa · warm-taupe back-right = Ratna.** (Validated 2026-06-24, render (3), Erik — count + 1-1-2 depth + membujur all correct; basis for `prompt-rules` changelog: colour-tagging, canvas y-depth, membujur, build-asset-first.)
```json
"prayer_mats": "four separate plain single-person prayer mats on the PERSISK rug, each a different muted solid colour, placed by camera-frame canvas coordinates on the 16:9 frame at 1920x1080 reference, a family prayer formation receding in depth, EVERY mat a tall narrow rectangle oriented lengthwise toward the camera, its long axis running front-to-back from the foreground toward the doorway and its short axis left-to-right, each mat clearly longer front-to-back than it is wide side-to-side, about 70cm wide by 115cm long with the 115cm length pointing toward the camera, all four mats oriented the same lengthwise way, the imam's muted sage-green mat centred at x 960 y 920 in the near foreground lowest in frame, the muted dusty-blue lone middle-row mat centred at x 960 y 780 in its own row, the back row two mats highest and furthest a muted terracotta mat centred at x 800 y 640 toward camera-left and a muted warm-taupe mat centred at x 1120 y 640 toward camera-right, the blue middle mat clearly between the green front mat and the back pair, all four mats within the central horizontal band from x 680 to x 1240 of 1920 with at least 430px to each side edge, the EKTORP sofa beyond x 1500 at camera-right and the BESTÅ TV bench before x 420 at camera-left both kept outside the mats band, each mat a plain solid-colour rectangle with a smooth unpatterned surface, spaced apart with rug showing between them"
```

---

## 4. Status manifest
| Cell | Angle | File | Status |
|---|---|---|---|
| M | establishing wide | `E02_ruangkeluarga_master.png` | ✅ LOCKED v2 (2026-06-23, token-ified + keyboard/mouse) |
| P | prayer high-angle wide | `E02_ruangkeluarga_prayer_high.png` | ✅ LOCKED v2 (2026-06-23, soft high-angle ~45°) |
| F | floor-seating | `E02_ruangkeluarga_floorseat.png` | ✅ LOCKED v2 (2026-06-23, tight-MS seated-height) |
| S | screen / desktop insert | `E02_ruangkeluarga_screen.png` | ✅ LOCKED v2 (2026-06-23, keyboard+mouse verified) |
| R | REVERSE establishing (prayer master, no mats) | `E02_ruangkeluarga_reverse.png` | ✅ LOCKED (2026-06-24, kamera membelakangi jendela → sholat menghadap kamera; sofa→camera-right, TV→camera-left, pintu+KALLAX latar, karpet PERSISK tengah — geometri terbalik terverifikasi) |
| R2 | REVERSE prayer plate + 4 colour-tagged mats | `E02_ruangkeluarga_reverse_prayer.png` | ✅ LOCKED (2026-06-24, 4 mat polos warna-beda, 1-1-2 saf via canvas x/y, membujur; sage-green=Herman/dusty-blue=Andi/terracotta=Lisa/warm-taupe=Ratna) |

Storage: `environment-images/E02_ruangkeluarga/` (+ `_rejected/`). Naming: `E02_ruangkeluarga_<angle>.png`.
Generate M first (no reference-image). Then P / F / S via the `shot`-only-rewrite method: upload `E02_ruangkeluarga_master.png` as reference + paste §1 verbatim + the cell's `shot` block. Verify each prop against the master image before locking.

---

*E02 Ruang Keluarga environment sheet v1.1 · Explainer Video 2 · 2026-06-23 · method [[00-README-ENV]] · same house as [[E01-kamar]] · token-per-token values + keyboard/mouse locked*
</content>
