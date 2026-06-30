---
title: Environment Sheet — E07 Gerbang Kompleks + Warung Darto · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e07-gerbangwarung, gate-0-env, exterior]
status: fase2-prompt-locked
created: 2026-06-30
updated: 2026-07-01
aliases: [ev2-e07-gerbangwarung, E07-gerbangwarung, gerbang-warung-env]
---

# Environment Sheet — E07 GERBANG KOMPLEKS + WARUNG DARTO · tag E07
> Method/anchor → [[00-README-ENV]] (§2.6). Scene truth → [[03-scene-detail]] SEQ2-SC03. Shotlist → `10-gateB-keyframes/SEQ2-SC03.md`.
> **Room (EXT):** the entrance gate of a middle-class Indonesian housing complex at morning, with Pak Darto's kelontong warung beside the guard post — the cross-profession meeting point that opens SEQ2 (vendor · student · ojek rider). 1× use (SC03). Empty-EXT reference plates, neutral grade; figures (Darto/Lisa/ojek) + warm-morning grade + long soft shadows added at GATE B keyframes.

> **EXTERIOR — declared anchor deviation (NOT an error):** the indoor home rule (IKEA flat-pack furniture + named public-domain Hokusai wall-art, E1–E6) **does NOT apply here.** Register = realism of a middle-class Indonesian residential complex. Design anchor = `production_designer` **Eugenio Caballero** (Roma realism, class-accurate, lived-in street) — no interior designer, no IKEA, no Hokusai. Discipline that DOES hold: **empty-EXT** (zero figures + zero vehicles in the plate), **neutral grade** (warm morning + figures at GATE B), **scoped-angle** (shot-driven, not 360), token-per-token (no conjunction glue in token values), positive-only.

> **Token discipline (locked):** every JSON token value below is a comma-delimited token cluster, NOT a sentence. **Fase-2 status:** prompts LOCKED, **generate PENDING (sesi baru)**.

---

## 1. Scene identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E07 angle)
This block stays identical across ALL E07 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E07_gerbangwarung_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm empty street stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "residential complex gate entrance, Indonesian middle-class housing complex, morning street, painted concrete guard post, kelontong warung stall, steel boom-gate barrier, paving-block road, mango tree, lived-in working-class neighbourhood",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in street calm",
  "subject_anchor": {
    "primary_subject": "complex gate entrance, steel boom-gate barrier, plain complex name signboard over the gate, paving-block entry road, camera centre, road receding into the housing complex",
    "subject_material": "grey concrete-paver road, painted concrete guard post, galvanized-zinc warung roof, painted brick boundary wall, real lived-in street surfaces",
    "supporting_objects": {
      "guard_post": "small painted concrete security guard post, camera-LEFT, glass window, plain plastic chair, small info board, beside the boom gate",
      "warung": "kelontong warung stall, camera-LEFT, abutting the guard post, weathered timber-zinc stall, glass-front display case, snack sachet strips hung across the front, bottled drinks, thermos, plain unbranded cloth banner, front display table",
      "boundary_wall": "low painted brick boundary wall, camera-RIGHT, potted plants along the top",
      "tree": "large leafy mango tree, camera-RIGHT edge, dappled canopy over the road",
      "lamp": "plain steel street lamp post, camera-RIGHT",
      "gate_forecourt": "open paving forecourt, foreground outside the gate, clear flat waiting space",
      "bin": "plain street rubbish bin, camera-LEFT, beside the warung",
      "floor": "grey concrete paving-block road, thin grass strip along the edges"
    },
    "human_absence_signal": "unoccupied, still, gate quiet, warung unattended, road clear, street empty, quiet"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class housing-complex exterior realism, class-accurate dressing, lived-in street"
}
```
**Canonical layout (defined by master, reused by all angles — directions are FROM THE MASTER CAMERA's point of view, camera outside the gate facing IN):** steel boom-gate barrier + plain complex-name signboard at centre, paving-block road receding into the complex · painted concrete guard post on the camera-LEFT, the kelontong warung abutting it on the camera-LEFT (weathered timber-zinc stall, glass display case, hung snack sachets, front display table) · low brick boundary wall on the camera-RIGHT with potted plants on top, a large mango tree at the camera-RIGHT edge with dappled canopy, a street lamp post camera-RIGHT · an open paving forecourt in the foreground outside the gate (the ojek waiting space, SH05) · grey paving-block road with grass-strip edges. **Perimeter filled (post + warung camera-left, wall + mango camera-right); the centre entry road stays open** so figures can stand at the warung and at the gate mouth without crowding.

**ADDENDUM A1:** NO device in the empty plate — Darto's phone + Lisa's phone arrive with them at GATE B. When they appear, screens render OFF/neutral and all UI (Darto's "Pesanan baru masuk" notification, Lisa's "Ojek tiba · menunggu di gerbang" confirmation) is composited in After Effects. The complex name signboard renders as a plain blank board (any text = AE). No vehicles in the plate (the ojek motorcycle = GATE B).

---

## 2. Method (per [[00-README-ENV]] §2.6 + EXT deviation)
- **Master generated first, no reference-image.** Each derivative (WAR / GTE) uploads `E07_gerbangwarung_master.png` as reference + rewrites ONLY the `shot` block → same street, new camera. (Generate = separate session; at authoring time the derivative only carries the `environment_reference` token.)
- **EXT anchor deviation declared:** no IKEA, no interior designer, no Hokusai wall-art. Realism via Caballero + concrete enumerated streetscape objects (guard post, kelontong warung, boom gate, mango tree, paving road) — each a strong-silhouette real-world type, named so it reproduces consistently across angles.
- **Empty-EXT, neutral grade:** zero figures + zero vehicles in the plate; warm morning grade + long soft shadows + the ojek motorcycle = GATE B.
- **No readable brands** on the warung (plain unbranded banner) — product brands inside the display case stay unreadable at this scale; only generic types.
- **Token-per-token values** — no conjunctions inside JSON token values (b.119); comma-delimited clusters only. Negation ban absolute. Camera-relative direction (camera-LEFT/RIGHT) anchored to named objects.

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` SEQ2-SC03 shot-list)
Each cell is a COMPLETE copy-paste-ready prompt, zero scaffold. §1 is the canonical identity-lock; the cells are what you paste. Scoped to E07's three plates: MASTER (establishing WIDE, serves SH01 + SH04 background) · WAR (warung-front MS, serves SH02 + SH03 background) · GTE (gate-mouth WIDE, serves SH05). WAR/GTE upload `E07_gerbangwarung_master.png` as reference-image at generate time.

### Cell M — MASTER · establishing WIDE → `E07_gerbangwarung_master.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Full gate-entrance geography — the anchor plate. Establishes the gate centre, guard-post + warung camera-LEFT, boundary wall + mango tree camera-RIGHT, road receding in.
```json
{
  "mood": "neutral reference clarity, calm empty street stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "residential complex gate entrance, Indonesian middle-class housing complex, morning street, painted concrete guard post, kelontong warung stall, steel boom-gate barrier, paving-block road, mango tree, lived-in working-class neighbourhood",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in street calm",
  "subject_anchor": {
    "primary_subject": "complex gate entrance, steel boom-gate barrier, plain complex name signboard over the gate, paving-block entry road, camera centre, road receding into the housing complex",
    "subject_material": "grey concrete-paver road, painted concrete guard post, galvanized-zinc warung roof, painted brick boundary wall, real lived-in street surfaces",
    "supporting_objects": {
      "guard_post": "small painted concrete security guard post, camera-LEFT, glass window, plain plastic chair, small info board, beside the boom gate",
      "warung": "kelontong warung stall, camera-LEFT, abutting the guard post, weathered timber-zinc stall, glass-front display case, snack sachet strips hung across the front, bottled drinks, thermos, plain unbranded cloth banner, front display table",
      "boundary_wall": "low painted brick boundary wall, camera-RIGHT, potted plants along the top",
      "tree": "large leafy mango tree, camera-RIGHT edge, dappled canopy over the road",
      "lamp": "plain steel street lamp post, camera-RIGHT",
      "gate_forecourt": "open paving forecourt, foreground outside the gate, clear flat waiting space",
      "bin": "plain street rubbish bin, camera-LEFT, beside the warung",
      "floor": "grey concrete paving-block road, thin grass strip along the edges"
    },
    "human_absence_signal": "unoccupied, still, gate quiet, warung unattended, road clear, street empty, quiet"
  },
  "shot": {
    "composition": "full gate-entrance geography, one frame, steel boom-gate barrier centre, plain complex name signboard over the gate, paving-block road receding in, guard post camera-LEFT, kelontong warung abutting the guard post camera-LEFT, low brick boundary wall camera-RIGHT, mango tree camera-RIGHT edge, street lamp camera-RIGHT, open forecourt foreground, legible",
    "framing": "WS establishing, road receding to background, sky band visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "outside the gate, looking in toward the complex, warung side camera-left, mango-tree side camera-right",
    "camera_direction": "through the gate into the complex, warung camera-left, mango tree camera-right, paving road receding",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, flat overcast-neutral key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class housing-complex exterior realism, class-accurate dressing, lived-in street"
}
```

### Cell WAR — WARUNG-FRONT MS → `E07_gerbangwarung_warung.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Serves SEQ2-SC03-SH02 (M Darto at the warung, 50mm) + background for the SH03 phone CU (85mm). The warung front at standing eye-level, the display case the focal mid-ground.
```json
{
  "environment_reference": "attached reference plate E07_gerbangwarung_master.png, same complex gate entrance, identical guard post, identical warung, identical layout, identical materials, faithful street match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty street stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "residential complex gate entrance, Indonesian middle-class housing complex, morning street, painted concrete guard post, kelontong warung stall, steel boom-gate barrier, paving-block road, mango tree, lived-in working-class neighbourhood",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in street calm",
  "subject_anchor": {
    "primary_subject": "kelontong warung stall front, weathered timber-zinc stall, glass-front display case, snack sachet strips hung across the front, front display table, camera-LEFT of the gate, painted concrete guard post adjacent",
    "subject_material": "grey concrete-paver road, painted concrete guard post, galvanized-zinc warung roof, painted brick boundary wall, real lived-in street surfaces",
    "supporting_objects": {
      "guard_post": "small painted concrete security guard post, glass window, plain plastic chair, small info board, beside the warung",
      "warung": "kelontong warung stall, weathered timber-zinc stall, glass-front display case, snack sachet strips hung across the front, bottled drinks, thermos, plain unbranded cloth banner, front display table",
      "boundary_wall": "low painted brick boundary wall, camera-RIGHT background, potted plants along the top",
      "tree": "large leafy mango tree, camera-RIGHT background edge, dappled canopy",
      "gate_forecourt": "open paving forecourt, foreground",
      "floor": "grey concrete paving-block road, thin grass strip along the edges"
    },
    "human_absence_signal": "unoccupied, still, warung unattended, display case stocked, street empty, quiet"
  },
  "shot": {
    "composition": "medium framing on the kelontong warung front, weathered timber-zinc stall, glass-front display case, snack sachet strips hung across the front, front display table, dominant centre, guard post camera-LEFT, sliver of boom gate camera-RIGHT, compressed background",
    "framing": "MS, warung front fills frame, standing eye-level, street compressed behind",
    "angle": "eye-level",
    "camera_position": "in front of the warung, pushed in from establishing wide, standing eye-level",
    "camera_direction": "toward the warung front, display case, guard post camera-left, gate camera-right",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, flat overcast-neutral key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class housing-complex exterior realism, class-accurate dressing, lived-in street"
}
```

### Cell GTE — GATE-MOUTH WIDE → `E07_gerbangwarung_gerbang.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Serves SEQ2-SC03-SH05 (WIDE Lisa + ojek at the portal, 35mm). The gate mouth + open forecourt waiting space, the boom gate the focal mid-ground (the ojek motorcycle + figures = GATE B).
```json
{
  "environment_reference": "attached reference plate E07_gerbangwarung_master.png, same complex gate entrance, identical guard post, identical warung, identical layout, identical materials, faithful street match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty street stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "residential complex gate entrance, Indonesian middle-class housing complex, morning street, painted concrete guard post, kelontong warung stall, steel boom-gate barrier, paving-block road, mango tree, lived-in working-class neighbourhood",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in street calm",
  "subject_anchor": {
    "primary_subject": "complex gate mouth, steel boom-gate barrier, plain complex name signboard over the gate, open paving forecourt foreground, clear flat waiting space, camera centre",
    "subject_material": "grey concrete-paver road, painted concrete guard post, galvanized-zinc warung roof, painted brick boundary wall, real lived-in street surfaces",
    "supporting_objects": {
      "guard_post": "small painted concrete security guard post, camera-LEFT, glass window, beside the boom gate",
      "warung": "kelontong warung stall, camera-LEFT background, glass-front display case, plain unbranded cloth banner",
      "boundary_wall": "low painted brick boundary wall, camera-RIGHT, potted plants along the top",
      "tree": "large leafy mango tree, camera-RIGHT edge, dappled canopy over the road",
      "lamp": "plain steel street lamp post, camera-RIGHT",
      "gate_forecourt": "open paving forecourt, foreground outside the gate, clear flat waiting space",
      "floor": "grey concrete paving-block road, thin grass strip along the edges"
    },
    "human_absence_signal": "unoccupied, still, gate quiet, forecourt clear, road clear, street empty, quiet"
  },
  "shot": {
    "composition": "wider framing on the gate mouth, steel boom-gate barrier, plain complex name signboard over the gate, open paving forecourt foreground, clear waiting space, guard post camera-LEFT, mango tree camera-RIGHT, paving road through the gate beyond, legible",
    "framing": "WS, gate-mouth forecourt fills frame, road beyond visible, standing eye-level",
    "angle": "eye-level",
    "camera_position": "near the gate portal, framing the open forecourt waiting space, guard-post side camera-left, mango side camera-right",
    "camera_direction": "toward the gate mouth, open forecourt foreground, paving road through the gate beyond",
    "camera": "35mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, flat overcast-neutral key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class housing-complex exterior realism, class-accurate dressing, lived-in street"
}
```

---

## 4. Status manifest
| Cell | Angle | File | Serves | Status |
|---|---|---|---|---|
| M | establishing WIDE | `E07_gerbangwarung_master.png` | SC03-SH01 + SH04 bg | ✅ prompt LOCKED · generate PENDING (sesi baru) |
| WAR | warung-front MS | `E07_gerbangwarung_warung.png` | SC03-SH02 + SH03 bg | ✅ prompt LOCKED · generate PENDING (sesi baru) |
| GTE | gate-mouth WIDE | `E07_gerbangwarung_gerbang.png` | SC03-SH05 | ✅ prompt LOCKED · generate PENDING (sesi baru) |

Storage: `environment-images/E07_gerbangwarung/` (+ `_rejected/`). Naming: `E07_gerbangwarung_<angle>.png`.
Generate M first (no reference-image). Then WAR / GTE via the `shot`-only-rewrite method: upload `E07_gerbangwarung_master.png` as reference + paste §1 verbatim + the cell's `shot` block. Verify each element against the master before locking. Empty-EXT (no figures, no vehicles, no device in plate); figures + ojek motorcycle + UI + warm-morning grade = GATE B / After Effects.

---

*E07 Gerbang+Warung environment sheet — Fase-2 prompts LOCKED (generate PENDING, sesi baru) · Explainer Video 2 · 2026-07-01 · EXTERIOR (declared anchor deviation: no IKEA/Hokusai, Caballero realism, empty-EXT, neutral grade) · token-per-token · camera-relative direction.*
