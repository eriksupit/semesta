---
title: Environment Sheet — E01 Kamar Herman · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e01-kamar, gate-0-env, image-generation]
status: active
created: 2026-06-22
updated: 2026-06-22
aliases: [ev2-e01-kamar, E01-kamar, kamar-herman-env]
---

# Environment Sheet — E01 KAMAR HERMAN · tag E01
> Method, scoped-angle rubric, 3 anchors, prompt-structure standard → [[00-README-ENV]] (§2.6 = prompt structure). Scene truth → [[03-scene-detail]] (SEQ1-SC01 + SEQ6-SC03). Furniture lock-anchors → [[tokens-references/INTERIOR-DESIGN-REFERENCE]] §6.
> **Room:** the parents' private bedroom (Herman + Ratna). Bookend — opens (SEQ1-SC01) and closes (SEQ6-SC03) the film; the coda must match the opener exactly. Empty-room reference plates, neutral grade; warm grade + practical light + characters added at GATE B keyframes.

---

## 1. Room identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E01 angle)
This block stays identical across ALL E01 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E01_kamar_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "private bedroom of an urban middle-class married couple, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "IKEA MALM double bed frame with high headboard, white stained oak veneer, neatly made against rear wall, one side creased one side smooth",
    "subject_material": "oak veneer particleboard, matte cotton bedding muted slate-grey, ceramic-tiled floor",
    "wall_art": "a single dark-wood-framed woodblock print centered on the wall above the headboard reproducing Katsushika Hokusai 'The Great Wave off Kanagawa', Thirty-Six Views of Mount Fuji, surrounding walls plain matte plaster kept clean bare empty, this single framed Hokusai print the only wall-mounted item in the entire room",
    "supporting_objects": {
      "nightstand": "IKEA MALM 2-drawer chest white stained oak veneer as nightstand camera-right, face-down phone dark screen, lamp switched off",
      "chair": "IKEA INGOLF chair solid wood antique stain slatted backrest by the bed, folded dark plain-weave sarong and black brimless velvet cap on it",
      "wife_devotion": "folded white mukena and rolled prayer mat on a low shelf, folded plain headscarf on the same low shelf",
      "storage": "IKEA PAX wardrobe oak-effect doors along the left wall",
      "window_dressing": "IKEA LILL white sheer net curtains on the left-wall window",
      "rug": "IKEA PERSISK HAMADAN handmade oriental wool rug low pile",
      "openings": "closed white door on the right wall",
      "floor": "pair of slippers placed parallel on the rug"
    },
    "human_absence_signal": "unoccupied, still, one side of the bed smooth and undisturbed"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```
**Canonical layout (defined by master, reused by all angles):** bed against rear wall · single Hokusai centered above headboard · nightstand + lamp camera-right · PAX wardrobe + LILL-curtained window camera-left · closed door right wall · PERSISK rug + slippers foreground.

---

## 2. Method (per [[00-README-ENV]] §2.6)
> **⭐ OVERRIDE 2026-06-29 (validated bed4q experiment):** angle derivatives are NOT standalone full-prompt cells re-uploading the master in a fresh window (that resamples → inconsistent — proven across ~6 bed4q renders). **Canonical:** `E01_kamar_master.png` = parent (full prompt, Cell M); every other angle (bed3q, bed4q, nightstand, …) = **EDIT-IN-PLACE child in the SAME context window as the master**, master annotated (1) *recent camera view* + (2) *next/goal camera view* (terse goal-delta). The full-JSON cells below (B / B4 / N) are kept as the **fallback / spec record only**. Within a shot, framing+angle locked. Full law: `prompt-rules-text-image-to-image.md` changelog 2026-06-29.
- **Master generated first, no reference-image.** (Fallback path) Each derivative uploads `E01_kamar_master.png` as reference + rewrites ONLY the `shot` block → same room, new camera (not text-only mirror, not clone). Validated bed3q 2026-06-22; **demoted 2026-06-29.**
- **Branded furniture lock-anchors** keep furniture identical across angles ([[tokens-references/INTERIOR-DESIGN-REFERENCE]] §6).
- **Single named artwork** (Hokusai Great Wave) = strong cross-angle prior.
- **No religious-identity label** in `scene` (keyword-leak — pulled calligraphy over Hokusai); devotion carried by concrete objects + social class only.
- ADDENDUM A1: zero graphics, screens off. Neutral grade (warm at GATE B).

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` shot-list)
Each cell below is a COMPLETE copy-paste-ready prompt (full 6-layer + `subject_anchor` + `shot`), per SOP — zero scaffold, zero "combine with §1". §1 remains the canonical identity-lock reference; the cells are what you paste into the generator. Scoped to E01's shots: SEQ1-SC01 (ECU eyes, CU phone-on-nightstand, MCU Herman+phone, MS side-of-bed) + SEQ6-SC03 (MCU + ECU, bookend). Derivatives upload `E01_kamar_master.png` as reference-image.

### Cell M — MASTER · establishing wide → `E01_kamar_master.png` · ✅ LOCKED
```json
{
  "environment_reference": "E01_kamar_master.png, same bedroom, identical layout, identical furniture, identical materials, faithful room match, new camera per shot block only",
  "mood": "neutral reference clarity, calm, empty, still",
  "color_grade": "neutral, true-to-life, balanced white-point",
  "style": "photorealistic interior reference plate, architectural clarity, ARRI Alexa Mini LF, prime spherical lens, Kodak Portra",
  "scene": "urban middle-class married couple private bedroom, IKEA flat-pack laminate furniture, matte plaster walls, desaturated textiles, lived-in",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet, domestic, calm",
  "subject_anchor": {
    "primary_subject": "IKEA MALM double bed, high headboard, white stained oak veneer, neatly made, against rear wall, one side creased, one side smooth",
    "subject_material": "oak veneer particleboard, matte cotton bedding muted slate-grey, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, centered above headboard, Hokusai 'The Great Wave off Kanagawa', only wall-mounted item, surrounding walls bare matte plaster",
    "supporting_objects": {
      "nightstand": "IKEA MALM 2-drawer chest, white stained oak, camera-right, face-down phone, dark screen, lamp off",
      "chair": "IKEA INGOLF chair, antique-stain wood, slatted back, camera-right, folded dark plain-weave sarong, black velvet peci on seat",
      "wife_devotion": "low shelf, folded white mukena, rolled prayer mat, folded plain headscarf",
      "storage": "IKEA PAX wardrobe, oak-effect doors, camera-left wall",
      "window_dressing": "IKEA LILL sheer net curtains, camera-left window",
      "rug": "IKEA PERSISK HAMADAN oriental wool rug, low pile",
      "openings": "closed white door, camera-right wall",
      "floor": "slippers, parallel, on rug"
    },
    "human_absence_signal": "unoccupied, still, one side smooth"
  },
  "shot": {
    "composition": "full room, bed centered on rear wall, framed print centered above headboard, floor across foreground",
    "framing": "wide establishing, floor bottom 15%, ceiling line top",
    "angle": "eye-level, slight low angle, straight-on, centered",
    "camera_position": "room center axis, wall opposite the bed, equidistant from both side walls",
    "camera_direction": "facing headboard wall, square-on, symmetric, print on central vertical axis",
    "camera": "24mm prime spherical, deep focus",
    "lighting": "soft daylight key, camera-left window, ambient bounce fill, matte",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero, Roma middle-class domestic realism",
  "interior_designer": "Ilse Crawford, warm tactile lived-in materiality"
}
```

### Cell B — BED 3/4 → `E01_kamar_bed3q.png` · ✅ LOCKED
Serves SEQ1-SC01-SH04 (MS side of bed) + SEQ6-SC03 (Herman lying / coda).
```json
{
  "environment_reference": "E01_kamar_master.png, same bedroom, identical layout, identical furniture, identical materials, faithful room match, new camera per shot block only",
  "mood": "neutral reference clarity, calm, empty, still",
  "color_grade": "neutral, true-to-life, balanced white-point",
  "style": "photorealistic interior reference plate, architectural clarity, ARRI Alexa Mini LF, prime spherical lens, Kodak Portra",
  "scene": "urban middle-class married couple private bedroom, IKEA flat-pack laminate furniture, matte plaster walls, desaturated textiles, lived-in",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet, domestic, calm",
  "subject_anchor": {
    "primary_subject": "IKEA MALM double bed, high headboard, white stained oak veneer, neatly made, against rear wall, one side creased, one side smooth",
    "subject_material": "oak veneer particleboard, matte cotton bedding muted slate-grey, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, centered above headboard, Hokusai 'The Great Wave off Kanagawa', only wall-mounted item, surrounding walls bare matte plaster",
    "supporting_objects": {
      "nightstand": "IKEA MALM 2-drawer chest, white stained oak, camera-right, face-down phone, dark screen, lamp off",
      "chair": "IKEA INGOLF chair, antique-stain wood, slatted back, camera-right, folded dark plain-weave sarong, black velvet peci on seat",
      "wife_devotion": "low shelf, folded white mukena, rolled prayer mat, folded plain headscarf",
      "storage": "IKEA PAX wardrobe, oak-effect doors, camera-left wall",
      "window_dressing": "IKEA LILL sheer net curtains, camera-left window",
      "rug": "IKEA PERSISK HAMADAN oriental wool rug, low pile",
      "openings": "closed white door, camera-right wall",
      "floor": "slippers, parallel, on rug"
    },
    "human_absence_signal": "unoccupied, still, one side smooth"
  },
  "shot": {
    "composition": "three-quarter bed, diagonal, bed fills frame, both pillows visible, headboard + Hokusai rear wall, nightstand camera-right, foot toward camera",
    "framing": "tight medium-wide, bed edge to edge, thin foreground rug strip",
    "angle": "eye-level, slight high angle, three-quarter onto bed",
    "camera_position": "room right side, foot end, close to bed",
    "camera_direction": "diagonally across bed to headboard, frame edges as leading lines",
    "camera": "35mm prime spherical, deep focus",
    "lighting": "soft daylight key, camera-left window, ambient bounce fill, matte",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero, Roma middle-class domestic realism",
  "interior_designer": "Ilse Crawford, warm tactile lived-in materiality"
}
```

### Cell N — NIGHTSTAND insert → `E01_kamar_nightstand.png` · ✅ LOCKED
Detail corner for the device area — SEQ1-SC01-SH02 (CU phone on nightstand) + SEQ6-SC03 (phone face-down on nightstand, screen off). Anchors the phone/lamp prop zone.
```json
{
  "environment_reference": "attached reference plate E01_kamar_master.png, same bedroom, identical furniture, identical layout, identical materials, single Hokusai Great Wave print, faithful room match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "private bedroom of an urban middle-class married couple, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "IKEA MALM double bed frame with high headboard, white stained oak veneer, neatly made against rear wall, one side creased one side smooth",
    "subject_material": "oak veneer particleboard, matte cotton bedding muted slate-grey, ceramic-tiled floor",
    "wall_art": "a single dark-wood-framed woodblock print centered on the wall above the headboard reproducing Katsushika Hokusai 'The Great Wave off Kanagawa', Thirty-Six Views of Mount Fuji, surrounding walls plain matte plaster kept clean bare empty, this single framed Hokusai print the only wall-mounted item in the entire room",
    "supporting_objects": {
      "nightstand": "IKEA MALM 2-drawer chest white stained oak veneer as nightstand camera-right, table lamp with fabric shade, and a face-down phone with dark screen on top, otherwise uncluttered surface",
      "chair": "IKEA INGOLF chair solid wood antique stain slatted backrest by the bed, folded dark plain-weave sarong and black brimless velvet cap on it",
      "wife_devotion": "folded white mukena and rolled prayer mat on a low shelf, folded plain headscarf on the same low shelf",
      "storage": "IKEA PAX wardrobe oak-effect doors along the left wall",
      "window_dressing": "IKEA LILL white sheer net curtains on the left-wall window",
      "rug": "IKEA PERSISK HAMADAN handmade oriental wool rug low pile",
      "openings": "closed white door on the right wall",
      "floor": "pair of slippers placed parallel on the rug"
    },
    "human_absence_signal": "unoccupied, still, one side of the bed smooth and undisturbed"
  },
  "shot": {
    "composition": "close detail of the MALM nightstand camera-right of the bed, table lamp with fabric shade, and a face-down phone with dark screen on top, otherwise uncluttered, headboard edge and the lower corner of the framed Hokusai print behind",
    "framing": "CS insert of the nightstand surface and the adjacent headboard edge, props legible",
    "angle": "eye-level slight high angle looking onto the nightstand surface",
    "camera_position": "beside the head of the bed, close to the nightstand",
    "camera_direction": "toward the nightstand top and the headboard corner",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft diffused daylight key from the curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "4:5"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```

### Cell B4 — OPPOSITE foot-corner (camera-move) → `E01_kamar_bed4q.png` · ✅ accepted (ChatGPT negative-variant) · positive-variant ⏳ re-test
Genuine camera-move to the opposite physical foot corner — **furniture stays on its real walls, NO side-swap** (nightstand stays room-right, window/wardrobe room-left, Hokusai un-reversed). Tokens alone don't move the camera; needs the `spatial_lock` + `spatial_integrity` (affirmative) + real-wall anchors. **Attach `E01_kamar_master.png` (handedness/identity lock) + `E01_kamar_bed3q.png` (angle/framing ref, then move camera).** Negatives from the working ChatGPT prompt converted to an affirmative `spatial_integrity` list per the no-negation rule.
```json
{
  "reference_image": [
    "E01_kamar_master.png — locked master layout, true room geometry, correct handedness, furniture positions, Hokusai orientation, faithful bedroom identity",
    "E01_kamar_bed3q.png — existing three-quarter bed vantage, use only as angle and framing reference, then move camera to the true opposite physical foot corner"
  ],
  "spatial_lock": "render a genuine camera move to the opposite physical foot corner, a fresh capture from a new camera position, preserve the real room handedness from E01_kamar_master.png, wardrobe and sheer-curtained window remain on the actual left wall of the room, nightstand and lamp and chair and low shelf and closed white door remain on the actual right wall of the room, Hokusai Great Wave print in its correct original orientation, all furniture remains on its original walls, only the camera position changes",
  "mood": "neutral reference clarity, calm, empty, still",
  "color_grade": "neutral, true-to-life, balanced white-point",
  "style": "photorealistic interior reference plate, architectural clarity, ARRI Alexa Mini LF, prime spherical lens, Kodak Portra",
  "scene": "urban middle-class married couple private bedroom, IKEA flat-pack laminate furniture, matte plaster walls, desaturated textiles, lived-in",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet, domestic, calm",
  "subject_anchor": {
    "primary_subject": "IKEA MALM double bed, high headboard, white stained oak veneer, neatly made, against rear wall, one side creased, one side smooth",
    "subject_material": "oak veneer particleboard, matte cotton bedding muted slate-grey, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, centered above headboard, Hokusai 'The Great Wave off Kanagawa', correct original orientation, only wall-mounted item, surrounding walls bare matte plaster",
    "supporting_objects": {
      "nightstand": "IKEA MALM 2-drawer chest, white stained oak, on the actual room-right side beside the bed, face-down phone, dark screen, lamp off",
      "chair": "IKEA INGOLF chair, antique-stain wood, slatted back, on the actual room-right side, folded dark plain-weave sarong, black velvet peci on seat",
      "wife_devotion": "low shelf on the actual room-right side, folded white mukena, rolled prayer mat, folded plain headscarf",
      "storage": "IKEA PAX wardrobe, oak-effect doors, on the actual room-left wall",
      "window_dressing": "IKEA LILL sheer net curtains, on the actual room-left window",
      "rug": "IKEA PERSISK HAMADAN oriental wool rug, low pile",
      "openings": "closed white door, on the actual room-right wall",
      "floor": "slippers, parallel, on rug"
    },
    "human_absence_signal": "unoccupied, still, one side smooth"
  },
  "shot": {
    "composition": "three-quarter bed view from the true opposite physical foot corner to E01_kamar_bed3q.png, bed fills frame, both pillows visible, headboard and Hokusai rear wall visible, nightstand remains on its real room-right side, foot of bed toward camera",
    "framing": "tight medium-wide, bed edge to edge, thin foreground rug strip",
    "angle": "eye-level, slight high angle, three-quarter onto bed from the opposite near-corner, genuine reverse camera angle as a fresh capture",
    "camera_position": "true opposite physical foot corner from E01_kamar_bed3q.png, close to bed, opposite near-corner camera move, a fresh capture from a new position",
    "camera_direction": "looking diagonally across the bed toward the headboard from the opposite side, fresh parallax, frame edges as leading lines",
    "camera": "35mm prime spherical, deep focus",
    "lighting": "soft daylight key from the actual room-left window, ambient bounce fill, matte",
    "aspect_ratio": "16:9"
  },
  "spatial_integrity": [
    "render as a fresh photographic capture from a new physical camera position",
    "keep the true room handedness identical to the master",
    "Hokusai print in its correct original orientation",
    "wardrobe and window remain on the actual room-left wall",
    "nightstand, lamp, chair, low shelf, and door remain on the actual room-right wall",
    "preserve the identical master bedroom layout",
    "keep identical furniture materials",
    "room remains unoccupied and empty"
  ],
  "production_designer": "Eugenio Caballero, Roma middle-class domestic realism",
  "interior_designer": "Ilse Crawford, warm tactile lived-in materiality"
}
```

---

## 4. Status manifest
| Cell | Angle | File | Status |
|---|---|---|---|
| M | establishing wide | `E01_kamar_master.png` | ✅ LOCKED (clock-free, dinding Hokusai-only, mukena stabil; **straight-on center symmetric** — re-shot 2026-06-26 via env_reference + square/centered camera, ganti off-axis corner) — regenerated 2026-06-23 |
| B | bed 3/4 | `E01_kamar_bed3q.png` | ✅ LOCKED (clock-free, tight bed-filling, dua sisi bantal jelas) — regenerated 2026-06-23 |
| N | nightstand insert | `E01_kamar_nightstand.png` | ✅ LOCKED (clock-free, HP screen-up tepi-depan reachable) — regenerated 2026-06-23 |
| B4 | opposite foot-corner | `E01_kamar_bed4q.png` | ✅ accepted (ChatGPT negative-variant) — opposite-angle, furnitur tetap di dinding nyata (nakas room-right), Hokusai benar. Cell B4 = positive-variant (negatif→`spatial_integrity`) untuk re-test. Method: spatial_lock + real-wall anchors + attach master+bed3q. |
| W | wall-art reverse | `E01_kamar_wallart_reverse.png` | ⏸ DEFERRED — tidak dipakai SEQ1-SC01 (hygiene). Plat lama masih ber-jam + spec sudah dikoreksi (1 nakas, kiri kosong); regen head-on saat ada scene yang memakainya. Jangan dipakai apa adanya. |

> **Clock removal (2026-06-23):** jam weker analog dibuang dari seluruh spec E01 (jarum analog tak andal di t2i, 2 render gagal; waktu subuh tetap via kartu AE `Waktu Subuh · 04.42` di layar HP). Keempat plat lama mengandung jam → regen **master dulu** (clock-free), lalu derivatif attach master baru. SH01 `sc01_sh01_*` yang sudah ACCEPT aman (jam di luar crop CU).

Storage: `environment-images/E01_kamar/` (+ `_rejected/`). Naming: `E01_kamar_<angle>.png`.
Generate W and N via the `shot`-only-rewrite method: upload `E01_kamar_master.png` as reference + paste §1 verbatim + the cell's `shot` block.

---

*E01 Kamar environment sheet v1.0 · Explainer Video 2 · 2026-06-22 · method [[00-README-ENV]] · companion [[08-character-sheet/H-herman]]*
