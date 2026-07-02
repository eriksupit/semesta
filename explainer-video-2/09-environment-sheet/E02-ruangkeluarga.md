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

### Cell M — MASTER · establishing wide (GRADED, subuh lamp-ON) → `E02_ruangkeluarga_master.png` · ✅ ACCEPTED 2026-07-02
> **RESET method (2026-07-01d, corrected 2026-07-02):** master = full-prompt from-scratch, **grade BAKED** for the scene time-of-day (subuh 04.43: warm ceiling-lamp ON + cool-blue dark window), **attachment: NONE**. Single grade state — E02 needs only ONE master (no lamp-off variant) because SC02 plays entirely with the room already lit ("lampu sudah menyala terang", `SEQ1-SC02.md:21`). This is the accepted prompt (Erik-authored, first roll). Key wins baked: restrained localized-falloff grade (no global yellow-wash, neutral plaster preserved, warm-cool separation) · window fully visible between KALLAX + desk · desk pushed flush camera-right, square to wall · all screens OFF (A1) · handedness locked. Serves SEQ1-SC02-SH01 (MW establishing) + SH03 (M, same vantage). ⚠ minor non-blocking: KALLAX rendered ~1×2 low rather than 2×2 (background only, no shot features it closely — accepted).
```json
{
  "mood": "pre-dawn subuh domestic calm, quiet intimate stillness, room already lit by a warm ceiling lamp against a dark blue dawn window, cinematic but natural, restrained practical warmth, gentle warm-cool separation, unoccupied and still",
  "color_grade": "cinematic restrained practical grade, warm amber ceiling-lamp highlights only where the light naturally falls, neutral off-white plaster walls preserved, no beige-yellow wall wash, no caramel ceiling, natural oak laminate furniture tones, subtle cool blue-gray dawn ambient bleeding from the window onto the back wall, desk side, floor near the curtains, under-sofa shadows, TV-bench side, and room corners, controlled warm-cool separation, gentle contrast, lifted but shaped blacks, clean exposure, soft matte falloff, slightly warmer Deakins midtones, Lubezki-style observational naturalism, no overall yellow wash, no orange cast, no sepia, no catalog-style even warmth, no exaggerated teal-orange look",
  "style": "photorealistic cinematic interior, architectural clarity, ARRI Alexa Mini LF, 24mm prime spherical lens, deep focus front to back, Kodak Portra natural rendering, Roger Deakins-inspired restrained practical-light naturalism, Emmanuel Lubezki-style observational domestic realism",
  "scene": "shared living room of a modern urban middle-class family, clean well-maintained contemporary IKEA flat-pack laminate furniture, matte painted plaster walls, tidy plain textiles, open ceramic-tiled floor kept clear, floor seating, warm domestic realism",
  "location": "indoor",
  "time_of_day": "pre-dawn subuh around 04.43",
  "atmosphere": "quiet intimate domestic calm, interior gently warmed by the ceiling lamp while cool dawn remains visible and active through the window, tender and natural, unoccupied and still",

  "subject_anchor": {
    "primary_subject": "open clear ceramic-tiled floor, centre of room, kept free, floor seating, low flat-weave floor mat unrolled, two flat floor cushions along the near edge",
    "subject_material": "neutral muted off-white matte painted plaster walls, natural oak-effect laminate furniture, plain desaturated woven textiles, clean ceramic-tiled floor with subtle warm and cool reflections",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Fine Wind, Clear Morning (Red Fuji)', centered on the camera-left wall above the sofa, correct orientation",
    "supporting_objects": {
      "desk": "IKEA MICKE desk oak-effect, placed on the far back wall and pushed fully to the camera-right side, square to the wall, not angled, generic unbranded all-in-one desktop on top facing directly toward the camera, screen off dark neutral, slim wireless keyboard and mouse before the monitor, black swivel office chair tucked at the desk",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, placed on the far back wall to the camera-left of the window, with a rolled prayer mat and a closed hardcover book in the cubes, otherwise tidy",
      "sofa": "IKEA EKTORP two-seat sofa, beige linen-blend slipcover, on the camera-left wall beneath the framed Red Fuji print, facing the television on the camera-right wall, open floor between",
      "tv_bench": "IKEA BESTÅ TV bench, white-stained oak-effect, low closed flat-door media cabinet, on the camera-right wall, directly facing the sofa, flat-screen television on top, screen off dark neutral",
      "seating_zone": "low flat-weave floor mat on the open floor, two plain flat floor cushions along the near edge, arranged for quiet domestic floor seating",
      "window_dressing": "one normal-proportioned rectangular window set into the far back wall between the KALLAX shelf and the desk, fully visible, not cropped, fitted with IKEA LILL sheer net curtains, cool deep blue pre-dawn light beyond, no daylight",
      "rug": "IKEA PERSISK HAMADAN handmade oriental wool rug, low pile, placed on one side of the open floor toward the TV-bench side",
      "openings": "open doorway on the far back wall toward the camera-left side, light switch plate beside it",
      "lighting_fixture": "plain ceiling lamp switched ON, warm glow visible overhead, modest wall hook near the doorway, folded plain headscarf hanging from it"
    },
    "human_absence_signal": "unoccupied, still, floor mat unrolled, cushions waiting, room empty, quiet before morning prayer"
  },

  "shot": {
    "composition": "full room geography in one frame: EKTORP sofa and framed Red Fuji on the camera-left wall, BESTÅ TV bench and off-screen television on the camera-right wall directly facing the sofa, open floor and unrolled flat-weave mat centred between, PERSISK HAMADAN rug on one side, MICKE desk pushed to the far back camera-right side with the all-in-one desktop facing camera, normal-proportioned sheer-curtained window fully visible between the KALLAX shelf and the desk, KALLAX cube shelf to the left of the window, open doorway on the left side of the back wall, all legible",
    "framing": "WS establishing, floor visible bottom 20%, ceiling line visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "front of room, looking toward the far back wall",
    "camera_direction": "straight down the room toward the far back wall, sofa and Red Fuji on camera-left, TV bench on camera-right, open floor and mat centred between",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "ceiling lamp ON as a warm motivated practical, but with localized falloff rather than a global yellow wash; sofa wall, Red Fuji wall, and central floor receive soft amber warmth; plaster walls remain neutral off-white; the far back wall around the window, desk side, curtains, floor near the window, under-sofa shadows, TV-bench side, and room corners retain cool blue-gray pre-dawn ambient; clean exposure, gently lit not low-key, soft cinematic shadow shape, lifted blacks, no black crush, restrained saturation",
    "aspect_ratio": "16:9"
  },

  "layout_continuity": {
    "do_not_change": "do not alter sofa position, Red Fuji print position or orientation, TV bench, desk, KALLAX shelf, doorway, rug, floor mat, cushions, ceramic floor, or straight-down-the-room framing; keep the desk flush to the far back wall and fully pushed to the camera-right side; keep the window fully visible between the KALLAX shelf and the desk",
    "do_not_mirror": "do not mirror or flip the room, preserve room handedness: sofa camera-left, TV bench camera-right, back wall with doorway at left side, KALLAX shelf left of window, window between shelf and desk, desk at far back camera-right"
  },

  "negative_prompt": {
    "screen_errors": "no glowing screens, no lit television, no lit desktop monitor, all screens off dark neutral",
    "grade_errors": "no daylight through the window, no bright daytime sky, window stays deep dark blue pre-dawn, no overall yellow wash, no beige-yellow wall cast, no caramel ceiling, no orange cast, no sepia, no overly saturated amber, no catalog-style even warmth, no flat interior showroom lighting, no exaggerated teal-orange blockbuster grading, no crushed blacks",
    "layout_errors": "do not mirror the room, do not move the sofa or TV bench, do not move the KALLAX shelf or doorway, do not angle the desk, do not place the desk in front of the window, do not crop or block the window, do not make the window a narrow vertical slit, do not add extra wall art, do not add people"
  },

  "production_designer": "Eugenio Caballero, modern middle-class domestic realism, clean well-maintained dressing",
  "interior_designer": "Ilse Crawford, warm human-centred tactile, unpretentious contemporary materiality"
}
```

### Cell M2 — SCREEN insert (SH02, edit-in-place) → `E02_ruangkeluarga_screen.png` · ✅ ACCEPTED 2026-07-02
Serves SEQ1-SC02-SH02 (desktop insert, screen OFF slab; lapak Ratna UI = AE). **Method = edit-in-place on the accepted `E02_ruangkeluarga_master.png` render** (canvas = master render; old disk plates legacy, NOT the canvas). Consistency vs master verified at pixel level (grade, handedness, oak desk, blue-window continuity, keyboard/mouse/chair). Accepted prompt verbatim:
```text
Edit-in-place (canvas = render E02_ruangkeluarga_master):
Reframe into a close insert of the camera-right-back corner desktop. Fill the frame with the MICKE oak-effect desk and the all-in-one desktop monitor centred, its screen OFF as a dark neutral slab — no UI, no icons, no glow. Show the slim wireless keyboard and mouse on the desk before the monitor, the black swivel office chair, and behind them a sliver of the far back wall with the edge of the sheer-curtained deep-blue pre-dawn window. Camera at sitting height, a slight angle onto the screen, 50mm feel.
Keep the same subuh grade exactly: warm ceiling-lamp ambient with localized falloff, cool blue-gray dawn bleed from the window, neutral off-white plaster, lifted blacks, no yellow wash, no glowing screen. Everything else unchanged — same desk, same all-in-one, same keyboard and mouse, same wall, same window, same room identity and handedness. Do not turn the screen on, do not add UI, do not add people, do not mirror. Keep 16:9.
```
> Render reads as a desk-wide insert (monitor + keyboard + mouse + chair + window edge) rather than a pure screen-CU — accepted: screen stays clearly visible/large for AE UI, plus work-desk context. Device reads as a standalone monitor vs "all-in-one" — immaterial for a standalone insert shot (no i2v morph from master).

### Cell M3 — SAF / prayer floor (SH04 + SH05, edit-in-place) → `E02_ruangkeluarga_saf.png` · ✅ ACCEPTED 2026-07-02
Serves SEQ1-SC02-SH04 (WIDE rear-view saf, 4 subjects) + SH05 (CU takbir, crop at keyframe). **Method = edit-in-place on the accepted `E02_ruangkeluarga_master.png` render** (canvas = master render; old disk plates legacy, NOT the canvas). Empty room — the 4 rear-view figures are composited at keyframe. Set-change: central floor becomes ONE contiguous muted-green prayer carpet (per old R2 lesson — a single contiguous textile renders reliably; 4 separate mats were disproven), enlarged toward camera-right; PERSISK rug rolled beside the TV bench; cushions to sofa. Pixel-verified vs master: carpet single/contiguous, rolled rug placed camera-right, grade + handedness + screens-OFF held. Accepted prompt verbatim (Erik-authored):
```text
Edit-in-place (canvas = render E02_ruangkeluarga_master):
Replace the centre floor arrangement so that the main prayer surface becomes one single plain solid muted-green prayer carpet, smooth and unpatterned, laid flat across the central ceramic-tiled floor. Enlarge this green prayer carpet further toward camera-right so it occupies most of the open centre floor and extends close to the TV-bench side, while still reading as one clean contiguous textile. Its long edge runs left-to-right, parallel to the back window-desk wall, forming a broad prayer floor facing the window.
Remove the patterned PERSISK oriental rug from its flat position on the floor. Roll it up tightly and place the rolled rug on the floor directly beside the BESTÅ TV bench on the camera-right side, pushed close against the TV bench, aligned lengthwise in the same front-to-back direction it currently occupies. The roll should sit neatly along the edge of the green carpet, with the rug's patterned outer layer still visible.
Move the two flat floor cushions off the floor and place them neatly on the EKTORP sofa seat. Keep the same establishing wide shot and the same room layout exactly: sofa and framed Red Fuji on camera-left, BESTÅ TV bench and off television on camera-right, MICKE desk and off desktop pushed to the far back camera-right wall, KALLAX shelf to the left of the back window, open doorway on the back-left side, all room handedness preserved.
Keep the same subuh grade exactly: warm ceiling-lamp ambient with localized falloff, cool blue-gray dawn bleed from the sheer-curtained back window, neutral off-white plaster walls, natural oak laminate furniture tones, lifted blacks, restrained contrast, no yellow wash, no orange cast, no sepia, all screens OFF dark neutral. The room remains empty and still, with no people.
Everything else unchanged. Do not mirror the room, do not move the furniture, do not add objects beyond the enlarged green prayer carpet and the rolled patterned rug repositioning. Keep 16:9.
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

### Cell R2 — REVERSE prayer plate, single plain prayer carpet + two stored rug rolls → `E02_ruangkeluarga_reverse_prayer.png` · ✅ LOCKED (2026-06-25, REPLACES the disproven 4-mat plate)
**Pivot 2026-06-25 (Erik):** the four colour-tagged mats DISPROVEN — standing-makmum mats dropped in render, and a mat baked onto the PERSISK rug mismatched the small PERSISK size in `sc02_sh01_end.png` (continuity anomaly). **New surface = ONE single plain solid muted-green prayer carpet** laid flat over the central tiled floor (no pattern, `tanpa corak`), distinct from the PERSISK. The PERSISK + the flat-weave floor mat are **rolled up and stored against the far front wall** (the camera-right roll = the wider tan flat-weave mat, a tall thick cylinder; the camera-left roll = the narrower PERSISK, shorter/slimmer) — they are out of use, so the everyday rugs are accounted for without crowding the prayer floor. The two EKTORP cushions sit on the sofa seat. Derived from **Cell R** (same reverse camera, upload `E02_ruangkeluarga_master.png`). Serves SEQ1-SC02 prayer (SH02 + SH03). Render-reliability rationale: one large contiguous floor object renders dependably (proven by the PERSISK behaviour); the carpet under standing makmum is still verified per keyframe render. **Identical to Cell R except: (a) replace the `rug` object with the `prayer_carpet` + `stored_rug_rolls` objects below; (b) cushions moved onto the sofa; (c) `primary_subject` & `shot.composition` name the green carpet + the two wall rolls; (d) filename `…_reverse_prayer.png`.** (Validated 2026-06-25, render `Content 1672x941 (1)` → renamed, Erik — green carpet + rolls + sofa cushions all correct.)
```json
"prayer_carpet": "one single plain solid muted-green prayer carpet, smooth even unpatterned wool surface, uniform solid green throughout, clean plain edges, about 200cm wide, laid flat across the central tiled floor, a single contiguous textile",
"stored_rug_rolls": "two everyday floor rugs rolled into tight upright cylinders, stood flush against the far front wall ahead beside the KALLAX shelf, the camera-right roll a wide tan flat-weave striped-pattern mat rolled into a tall thick cylinder standing higher, the camera-left roll a narrower PERSISK oriental-pattern rug rolled into a shorter slimmer cylinder, both set aside out of use"
```

---

## 4. Status manifest
| Cell | Angle | File | Status |
|---|---|---|---|
| M | establishing wide (GRADED subuh lamp-ON) | `E02_ruangkeluarga_master.png` | ✅ ACCEPTED 2026-07-02 · **RESET graded** (warm ceiling-lamp ON + cool-blue dark window, attachment NONE) · restrained localized-falloff grade (no yellow-wash) · window fully visible between KALLAX+desk · desk pushed flush camera-right · screens OFF · single-grade (no lamp-off variant) · supersedes neutral master · ⚠ KALLAX rendered ~1×2 (background, accepted) |
| M2 screen insert | SH02 desktop CU | `E02_ruangkeluarga_screen.png` | ✅ ACCEPTED 2026-07-02 — edit-in-place from master render; screen OFF slab (UI=AE), grade+handedness consistent, keyboard+mouse+chair, blue-window continuity; supersedes legacy `_screen.png` |
| M3 saf / prayer floor | SH04 WIDE rear-saf + SH05 CU takbir | `E02_ruangkeluarga_saf.png` | ✅ ACCEPTED 2026-07-02 — edit-in-place from master render; ONE contiguous muted-green prayer carpet enlarged camera-right, PERSISK rolled beside TV bench, cushions to sofa, grade+handedness held, screens OFF, empty room; = **rear-view (facing window) prayer angle, canon** per SEQ1-SC02 SH04/SH05. On-disk renamed 2026-07-02 (matches doc). ⚠ keyframe attach-ref (`SEQ1-SC02.md` SH04/SH05 Teknis) still names `_reverse_prayer_subuh` → repoint to `_saf` at Fase-3 keyframe. |

> **⚠ E02 reset status — CORRECTED 2026-07-02 (my earlier "3 plates / done" claim was premature = careless; retracted).** E02 needs **5 graded plates**, all edit-in-place from the master render: `master` ✅ · `screen` ✅ · `saf` rear-view ✅ · **`prayer_high`** high-angle (⬜ PENDING regen) · **`reverse_prayer`** facing-camera (⬜ PENDING regen). **Kiblat decision (Erik 2026-07-02): BOTH prayer angles are canon — rear-view facing the window (`saf`) stays, AND a facing-camera reverse prayer (`reverse_prayer`) is added** (distinct shots use each). The legacy neutral plates below are **NOT superseded** except `screen`/`floorseat` — they mark angles still to be regenerated under the graded method. **Do NOT move/rename/delete any legacy plate until its graded replacement lands (Erik 2026-07-02, "jangan pindah dulu").** E02 serves SEQ1-SC02 subuh only (ngaji SEQ6-SC02 cut; SC13 finale uses `E06_ruangmakan`). ⚠ current 5-shot narrative uses only master/screen/saf — `prayer_high` + `reverse_prayer` imply added prayer shots to be slotted at Fase-3 shotlist.

| Cell | Angle | File | Status |
|---|---|---|---|
| P → regen | prayer high-angle (~45° down, sujud beat) | `E02_ruangkeluarga_prayer_high.png` | ⬜ PENDING regen graded — edit-in-place from master (high-angle onto green prayer floor, subuh grade); legacy neutral plate INTACT on disk until replaced, do not move |
| R/R2 → regen | REVERSE facing-camera prayer (green carpet) | `E02_ruangkeluarga_reverse_prayer.png` | ⬜ PENDING regen graded — 180° reverse (camera at back window-desk wall → doorway; sofa→camera-right, TV→camera-left; green carpet; subuh); collapses legacy `_reverse`/`_reverse_prayer`/`_reverse_prayer_subuh` into ONE graded plate; legacy plates INTACT, do not move |
| F | floor-seating | `E02_ruangkeluarga_floorseat.png` | 🗄 OBSOLETE — ngaji scene (SEQ6-SC02) cut, not reused; leave on disk, do not move |
| S | screen insert (old) | `E02_ruangkeluarga_screen.png` | superseded by reset M2 (same filename overwritten on accept) |

Storage: `environment-images/E02_ruangkeluarga/` (+ `_rejected/`). Naming: `E02_ruangkeluarga_<angle>.png`.
**Reset workflow:** master accepted (graded, attachment NONE) → each derivative = **edit-in-place on the accepted master render** (canvas = master render; old disk plates are legacy, NOT the canvas) + the angle/grade delta.

---

*E02 Ruang Keluarga environment sheet v1.1 · Explainer Video 2 · 2026-06-23 · method [[00-README-ENV]] · same house as [[E01-kamar]] · token-per-token values + keyboard/mouse locked*
</content>
