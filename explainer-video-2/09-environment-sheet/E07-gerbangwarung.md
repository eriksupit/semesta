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
  "scene": "residential complex gate entrance, Indonesian middle-class housing complex, morning street, painted concrete guard post, kelontong warung stall, steel boom-gate barrier, simple exposed steel gate frame without signboard, paving-block road, mango tree, soft overcast morning sky, lived-in working-class neighbourhood",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in street calm, soft overcast daylight",
  "subject_anchor": {
    "primary_subject": "complex gate entrance, steel boom-gate barrier, simple exposed horizontal steel beam over the gate with no signboard, paving-block entry road, camera centre, road receding into the housing complex",
    "subject_material": "grey concrete-paver road, painted concrete guard post, weathered timber-zinc warung stall, galvanized-zinc warung roof, painted brick boundary wall, exposed painted steel gate posts and single horizontal beam, real lived-in street surfaces",
    "supporting_objects": {
      "gate_frame": "minimal exposed steel gate frame, dark vertical steel posts, one single clean horizontal steel beam across the top, no residential signboard, no lettering, no blank panel, no secondary lower horizontal support beam",
      "boom_gate": "lowered white steel boom-gate barrier with subtle red reflective segments, centre of frame, spanning across the paving-block road",
      "guard_post": "small painted concrete security guard post, camera-LEFT, glass window, plain plastic chair, small info board, beside the boom gate",
      "warung": "kelontong warung stall, camera-LEFT, abutting the guard post, weathered timber-zinc stall, glass-front display case, snack sachet strips hung across the front, bottled drinks, thermos, plain unbranded cloth banner, front display table",
      "boundary_wall": "low painted brick boundary wall, camera-RIGHT, potted plants along the top",
      "tree": "large leafy mango tree, camera-RIGHT edge, dappled canopy over the road",
      "lamp": "plain steel street lamp post, camera-RIGHT",
      "gate_forecourt": "open paving forecourt, foreground outside the gate, clear flat waiting space",
      "bin": "plain street rubbish bin, camera-LEFT, beside the warung",
      "sky": "soft overcast morning sky, gentle grey to pale-blue gradient, diffused cloud texture, natural photographic depth, neutral true-to-life tone",
      "floor": "grey concrete paving-block road, thin grass strip along the edges"
    },
    "human_absence_signal": "unoccupied, still, gate quiet, warung unattended, road clear, street empty, quiet"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class housing-complex exterior realism, class-accurate dressing, lived-in street"
}
```
**Canonical layout (defined by master, reused by all angles — directions are FROM THE MASTER CAMERA's point of view, camera outside the gate facing IN):** steel boom-gate barrier at centre spanning the road, a minimal exposed steel gate frame above (dark vertical posts + one single horizontal beam, NO signboard, no lettering), paving-block road receding into the complex · painted concrete guard post on the camera-LEFT, the kelontong warung abutting it on the camera-LEFT (weathered timber-zinc stall, glass display case, hung snack sachets, front display table) · low brick boundary wall on the camera-RIGHT with potted plants on top, a large mango tree at the camera-RIGHT edge with dappled canopy, a street lamp post camera-RIGHT · an open paving forecourt in the foreground outside the gate (the ojek waiting space, SH05) · grey paving-block road with grass-strip edges. **Perimeter filled (post + warung camera-left, wall + mango camera-right); the centre entry road stays open** so figures can stand at the warung and at the gate mouth without crowding.

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

### Cell M — MASTER · establishing WIDE → `E07_gerbangwarung_master.png` · ✅ GENERATED + ACCEPTED (2026-07-01)
Full gate-entrance geography — the anchor plate. Establishes the gate centre (exposed steel beam, NO signboard), guard-post + warung camera-LEFT, boundary wall + mango tree camera-RIGHT, road receding in, textured overcast sky. **Accepted render = `E07_gerbangwarung_master.png`.** (Regenerated full-prompt, not edit-in-place: signboard removal + sky texture were fundamental changes → from-scratch regen; see lessons.)
```json
{
  "mood": "neutral reference clarity, calm empty street stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "residential complex gate entrance, Indonesian middle-class housing complex, morning street, painted concrete guard post, kelontong warung stall, steel boom-gate barrier, simple exposed steel gate frame without signboard, paving-block road, mango tree, soft overcast morning sky, lived-in working-class neighbourhood",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in street calm, soft overcast daylight",
  "subject_anchor": {
    "primary_subject": "complex gate entrance, steel boom-gate barrier, simple exposed horizontal steel beam over the gate with no signboard, paving-block entry road, camera centre, road receding into the housing complex",
    "subject_material": "grey concrete-paver road, painted concrete guard post, weathered timber-zinc warung stall, galvanized-zinc warung roof, painted brick boundary wall, exposed painted steel gate posts and single horizontal beam, real lived-in street surfaces",
    "supporting_objects": {
      "gate_frame": "minimal exposed steel gate frame, dark vertical steel posts, one single clean horizontal steel beam across the top, no residential signboard, no lettering, no blank panel, no secondary lower horizontal support beam",
      "boom_gate": "lowered white steel boom-gate barrier with subtle red reflective segments, centre of frame, spanning across the paving-block road",
      "guard_post": "small painted concrete security guard post, camera-LEFT, glass window, plain plastic chair, small info board, beside the boom gate",
      "warung": "kelontong warung stall, camera-LEFT, abutting the guard post, weathered timber-zinc stall, glass-front display case, snack sachet strips hung across the front, bottled drinks, thermos, plain unbranded cloth banner, front display table",
      "boundary_wall": "low painted brick boundary wall, camera-RIGHT, potted plants along the top",
      "tree": "large leafy mango tree, camera-RIGHT edge, dappled canopy over the road",
      "lamp": "plain steel street lamp post, camera-RIGHT",
      "gate_forecourt": "open paving forecourt, foreground outside the gate, clear flat waiting space",
      "bin": "plain street rubbish bin, camera-LEFT, beside the warung",
      "sky": "soft overcast morning sky, gentle grey to pale-blue gradient, diffused cloud texture, natural photographic depth, neutral true-to-life tone",
      "floor": "grey concrete paving-block road, thin grass strip along the edges"
    },
    "human_absence_signal": "unoccupied, still, gate quiet, warung unattended, road clear, street empty, quiet"
  },
  "shot": {
    "composition": "full gate-entrance geography, one frame, steel boom-gate barrier centre, simple exposed steel gate frame above with only one horizontal beam and no signboard, paving-block road receding in, guard post camera-LEFT, kelontong warung abutting the guard post camera-LEFT, low brick boundary wall camera-RIGHT, mango tree camera-RIGHT edge, street lamp camera-RIGHT, open forecourt foreground, soft overcast sky band top, legible",
    "framing": "WS establishing, road receding to background, textured overcast sky band visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "outside the gate, looking in toward the complex, warung side camera-left, mango-tree side camera-right",
    "camera_direction": "through the gate into the complex, warung camera-left, mango tree camera-right, paving road receding",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, diffused overcast key, gentle sky luminance gradient, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class housing-complex exterior realism, class-accurate dressing, lived-in street"
}
```

### Cell WAR — WARUNG-FRONT MS → `E07_gerbangwarung_warung.png` · ✅ GENERATED + ACCEPTED (2026-07-01)
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
    "composition": "medium framing on the kelontong warung front, weathered timber-zinc stall, glass-front display case, snack sachet strips hung across the front, front display table, dominant centre, painted concrete guard post camera-RIGHT toward the gate, compressed background",
    "framing": "MS, warung front fills frame, standing eye-level, street compressed behind",
    "angle": "eye-level",
    "camera_position": "in front of the warung, pushed in from establishing wide, standing eye-level",
    "camera_direction": "toward the warung front, display case, guard post camera-right toward the gate",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, flat overcast-neutral key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class housing-complex exterior realism, class-accurate dressing, lived-in street"
}
```

### Cell GTE — GATE-MOUTH WIDE → ⛔ **DROPPED (2026-07-01)** · SH05 uses `E07_gerbangwarung_master.png` as env-reference
**DROPPED (reference-dominance, same-angle zoom).** GTE was a 35mm zoom on the SAME angle as the 24mm master; two generate attempts (`dbff1af5`, `7cdbe9c8`, both in `_rejected/`) both returned ≈ the master, only mildly tighter, and would not resolve into a distinct "forecourt-dominant portal" framing — text nudges lose to the master reference on an identical angle. Same failure mode as **E06 cell MEJA** (dropped 2026-07-01b). **SH05 (WIDE Lisa + ojek at the portal) therefore attaches `E07_gerbangwarung_master.png` as its environment-reference, and the portal/forecourt framing + ojek + figures are composed at the SH05 GATE-B keyframe prompt, not chased as a plate.** Prompt below retained for reference only (do NOT generate).
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
| M | establishing WIDE | `E07_gerbangwarung_master.png` | SC03-SH01 + SH04 bg | ✅ **GENERATED + ACCEPTED (2026-07-01)** |
| WAR | warung-front MS | `E07_gerbangwarung_warung.png` | SC03-SH02 + SH03 bg | ✅ **GENERATED + ACCEPTED (2026-07-01)** |
| GTE | gate-mouth WIDE | ~~`E07_gerbangwarung_gerbang.png`~~ | SC03-SH05 | ⛔ **DROPPED** — SH05 uses master as env-ref (reference-dominance, same-angle zoom; cf. E06 MEJA) |

**E07 COMPLETE (2 plates: M + WAR).** GTE dropped — SC03-SH05 attaches `E07_gerbangwarung_master.png`.

Storage: `environment-images/E07_gerbangwarung/` (+ `_rejected/`). Naming: `E07_gerbangwarung_<angle>.png`.
Generate M first (no reference-image). Then WAR / GTE via the `shot`-only-rewrite method: upload `E07_gerbangwarung_master.png` as reference + paste §1 verbatim + the cell's `shot` block. Verify each element against the master before locking. Empty-EXT (no figures, no vehicles, no device in plate); figures + ojek motorcycle + UI + warm-morning grade = GATE B / After Effects.

---

*E07 Gerbang+Warung environment sheet — Fase-2 prompts LOCKED (generate PENDING, sesi baru) · Explainer Video 2 · 2026-07-01 · EXTERIOR (declared anchor deviation: no IKEA/Hokusai, Caballero realism, empty-EXT, neutral grade) · token-per-token · camera-relative direction.*
