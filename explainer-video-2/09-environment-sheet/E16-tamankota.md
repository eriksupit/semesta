---
title: Environment Sheet — E16 Taman Kota (EXT) · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e16-tamankota, gate-0-env, exterior]
status: fase2-prompt-locked
created: 2026-06-30
updated: 2026-07-01
aliases: [ev2-e16-tamankota, E16-tamankota, taman-kota-env]
---

# Environment Sheet — E16 TAMAN KOTA (EXT) · tag E16
> Method/anchor → [[00-README-ENV]] (§2.6). Scene truth → [[03-scene-detail]] SEQ4-SC11. Shotlist → `10-gateB-keyframes/SEQ4-SC11.md`.
> **Room (EXT):** a public city park in the late afternoon — open green space, a footpath, benches. The humane-tech contrast scene (people glued to phones on the bench vs Ratna + Andi present for each other on the path). 1× use (SC11). Empty of NAMED foreground figures (Ratna/Andi = GATE B); the **heads-down bench crowd IS soft ambient plate dressing** (not face-locked, `lessons` b.58). Neutral grade; golden-hour grade + named figures = GATE B.

> **EXTERIOR — declared anchor deviation:** no IKEA home furniture, no Hokusai home wall-art. Register = an Indonesian public city park. Anchor = `production_designer` **Eugenio Caballero** (realism). Discipline that holds: NAMED foreground figures absent (bench crowd = soft ambient only), **neutral grade**, **scoped-angle**, token-per-token, positive-only, A1 (device screens OFF; the step/fitness UI = After Effects).

> **Token discipline (locked):** comma-delimited clusters, no conjunction glue, zero negation, camera-relative direction. **Fase-2 status:** prompts LOCKED, **generate PENDING (sesi baru)**.

---

## 1. Scene identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E16 angle)
This block stays identical across ALL E16 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E16_tamankota_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm open-park stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "public city park, open green space, paved footpath, park bench, leafy shade trees, mown grass lawn, calm urban park afternoon",
  "location": "outdoor",
  "time_of_day": "afternoon",
  "atmosphere": "quiet open-park calm",
  "subject_anchor": {
    "primary_subject": "city public park scene, paved footpath centre, park bench camera-LEFT, soft anonymous seated figures on the bench, heads bowed to plain handheld devices screens off, leafy shade trees, green lawn, open park",
    "subject_material": "grey paved footpath, weathered timber-slat steel-frame park bench, leafy tree canopy, mown grass lawn, real lived-in park surfaces",
    "supporting_objects": {
      "bench": "park bench, weathered timber slats, steel frame, camera-LEFT, soft anonymous seated figures, heads bowed to plain handheld devices screens off, blurred faces",
      "path": "paved footpath, grey paving, centre, leading through the park",
      "trees": "leafy shade trees, broad canopy, dappled light, around the path",
      "lawn": "green mown grass lawn, either side of the path",
      "lamp": "plain park lamp post, camera-RIGHT",
      "bin": "plain park rubbish bin, beside the bench",
      "shrubs": "low leafy shrubs, planting beds, along the path edges",
      "background_feature": "faint distant park feature, small fountain, far background",
      "floor": "grey paved footpath, green grass edges"
    },
    "human_absence_signal": "foreground path clear, soft anonymous seated crowd on the bench only, blurred, still"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian public city park exterior realism, class-mixed, lived-in"
}
```
**Canonical layout (defined by master, directions FROM THE MASTER CAMERA's POV):** a park bench on the camera-LEFT where a soft anonymous crowd sits in a row, heads bowed to handheld devices (screens OFF, faces blurred, NOT face-locked — the contrast crowd) · a paved footpath running through the centre (where Ratna + Andi stand/walk at GATE B) · leafy shade trees with a broad dappled canopy around the path, green mown lawn either side, a park lamp post camera-RIGHT, low shrubs + planting beds along the path edges, a faint distant fountain in the far background. **The bench crowd (camera-left) + the open path (centre) co-present in one WIDE = the scene's core contrast; the foreground path stays clear for the named figures at GATE B.**

**ADDENDUM A1:** every device screen renders OFF / dark / neutral — the bench crowd's handheld devices in the plate, and (at GATE B) Andi's phone. All UI is composited in After Effects: the step/fitness summary ("8.000 langkah hari ini" + target icon). The bench crowd is soft dressing (no locked faces); the two named figures (Ratna hijab + Andi) are added at GATE B.

---

## 2. Method (per [[00-README-ENV]] §2.6 + EXT deviation)
- **Master generated first, no reference-image.** JLR derivative uploads `E16_tamankota_master.png` as reference + rewrites ONLY the `shot` block → same park, new camera. (Generate = separate session; at authoring time the derivative only carries the `environment_reference` token.)
- **EXT anchor deviation declared:** no IKEA, no Hokusai. Caballero realism + concrete enumerated park elements (footpath, timber-slat bench, shade trees, lawn).
- **Heads-down bench crowd IS plate dressing** (soft, blurred, anonymous, screens off) — the contrast lives in the plate; the NAMED figures (Ratna/Andi) are GATE B. The locomotion scene is staged as beat-pauses at GATE B (no traverse — `lessons` b.58).
- **Empty foreground path, neutral grade:** named figures + golden-hour grade = GATE B.
- **No readable brands** (brand-safe).
- **Token-per-token values** — no conjunctions inside JSON token values (b.119); comma-delimited clusters only. Negation ban absolute.

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` SEQ4-SC11 shot-list)
Each cell is a COMPLETE copy-paste-ready prompt, zero scaffold. §1 is the canonical identity-lock. Scoped to E16's two plates: MASTER (establishing WIDE contrast, serves SC11-SH01/SH05) · JLR (footpath MS, serves SC11-SH02/SH04). JLR uploads `E16_tamankota_master.png` as reference-image at generate time.

### Cell M — MASTER · establishing WIDE → `E16_tamankota_master.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Full park geography — the anchor plate + the contrast wide. Establishes the bench crowd camera-LEFT, the open footpath centre, trees + lawn around.
```json
{
  "mood": "neutral reference clarity, calm open-park stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "public city park, open green space, paved footpath, park bench, leafy shade trees, mown grass lawn, calm urban park afternoon",
  "location": "outdoor",
  "time_of_day": "afternoon",
  "atmosphere": "quiet open-park calm",
  "subject_anchor": {
    "primary_subject": "city public park scene, paved footpath centre, park bench camera-LEFT, soft anonymous seated figures on the bench, heads bowed to plain handheld devices screens off, leafy shade trees, green lawn, open park",
    "subject_material": "grey paved footpath, weathered timber-slat steel-frame park bench, leafy tree canopy, mown grass lawn, real lived-in park surfaces",
    "supporting_objects": {
      "bench": "park bench, weathered timber slats, steel frame, camera-LEFT, soft anonymous seated figures, heads bowed to plain handheld devices screens off, blurred faces",
      "path": "paved footpath, grey paving, centre, leading through the park",
      "trees": "leafy shade trees, broad canopy, dappled light, around the path",
      "lawn": "green mown grass lawn, either side of the path",
      "lamp": "plain park lamp post, camera-RIGHT",
      "bin": "plain park rubbish bin, beside the bench",
      "shrubs": "low leafy shrubs, planting beds, along the path edges",
      "background_feature": "faint distant park feature, small fountain, far background",
      "floor": "grey paved footpath, green grass edges"
    },
    "human_absence_signal": "foreground path clear, soft anonymous seated crowd on the bench only, blurred, still"
  },
  "shot": {
    "composition": "full park geography, one frame, paved footpath centre, park bench camera-LEFT, soft anonymous seated figures heads bowed to devices, leafy shade trees, green lawn either side, park lamp camera-RIGHT, dappled canopy light, faint distant fountain, legible",
    "framing": "WS establishing, path leading into the park, tree canopy visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "facing the footpath, the bench camera-left, the open path centre, trees around",
    "camera_direction": "toward the footpath, bench camera-left, open path centre, leafy park beyond",
    "camera": "28mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, dappled diffused key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian public city park exterior realism, class-mixed, lived-in"
}
```

### Cell JLR — FOOTPATH MS → `E16_tamankota_jalur.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Serves SEQ4-SC11-SH02/SH04 (Ratna + Andi on the path, 50mm 2-shot). A footpath segment at standing height, shade trees behind, the bench crowd soft at the camera-LEFT background.
```json
{
  "environment_reference": "attached reference plate E16_tamankota_master.png, same city park, identical footpath, identical bench, identical trees, identical layout, identical materials, faithful park match, new camera per shot block only",
  "mood": "neutral reference clarity, calm open-park stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "public city park, open green space, paved footpath, park bench, leafy shade trees, mown grass lawn, calm urban park afternoon",
  "location": "outdoor",
  "time_of_day": "afternoon",
  "atmosphere": "quiet open-park calm",
  "subject_anchor": {
    "primary_subject": "park footpath segment, grey paving centre, leafy shade trees behind, green mown lawn either side, low shrubs along the edges, open park depth",
    "subject_material": "grey paved footpath, leafy tree canopy, mown grass lawn, weathered timber-slat steel-frame park bench, real lived-in park surfaces",
    "supporting_objects": {
      "path": "paved footpath, grey paving, dominant centre, leading through the park",
      "trees": "leafy shade trees, broad canopy, dappled light, behind the path",
      "lawn": "green mown grass lawn, either side of the path",
      "bench": "park bench, soft, camera-LEFT background, soft anonymous seated figures, heads bowed to devices screens off, blurred",
      "lamp": "plain park lamp post, soft, camera-RIGHT",
      "shrubs": "low leafy shrubs, planting beds, along the path edges",
      "floor": "grey paved footpath, green grass edges"
    },
    "human_absence_signal": "foreground path clear, soft anonymous bench crowd camera-LEFT background only, blurred, still"
  },
  "shot": {
    "composition": "medium framing on a footpath segment, grey paving centre, dominant mid-ground, leafy shade trees behind, green lawn either side, low shrubs, park lamp soft camera-RIGHT, bench crowd soft camera-LEFT background, open park depth",
    "framing": "MS, footpath segment fills frame, standing eye-level, park compressed behind",
    "angle": "eye-level, standing height",
    "camera_position": "facing a footpath segment, pushed in from establishing wide, standing eye-level",
    "camera_direction": "toward the footpath segment, leafy trees behind, lawn either side, bench crowd soft camera-left background",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, dappled diffused key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian public city park exterior realism, class-mixed, lived-in"
}
```

---

## 4. Status manifest
| Cell | Angle | File | Serves | Status |
|---|---|---|---|---|
| M | establishing WIDE (contrast) | `E16_tamankota_master.png` | SC11-SH01/SH05 | ✅ prompt LOCKED · generate PENDING (sesi baru) |
| JLR | footpath MS | `E16_tamankota_jalur.png` | SC11-SH02/SH04 | ✅ prompt LOCKED · generate PENDING (sesi baru) |

Storage: `environment-images/E16_tamankota/` (+ `_rejected/`). Naming: `E16_tamankota_<angle>.png`.
Generate M first (no reference-image). Then JLR via the `shot`-only-rewrite method: upload `E16_tamankota_master.png` as reference + paste §1 verbatim + the cell's `shot` block. The heads-down bench crowd is soft dressing (screens OFF, faces blurred, no lock); Ratna + Andi + golden-hour grade + step UI = GATE B / After Effects.

---

*E16 Taman Kota environment sheet — Fase-2 prompts LOCKED (generate PENDING, sesi baru) · Explainer Video 2 · 2026-07-01 · EXTERIOR (declared anchor deviation; outside the 14-inventory, swap-in for the cut koperasi) · heads-down bench crowd = soft ambient dressing (not face-locked) · token-per-token · camera-relative direction.*
