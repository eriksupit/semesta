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
- **Master generated first, no reference-image.** Each derivative uploads `E01_kamar_master.png` as reference + rewrites ONLY the `shot` block → same room, new camera (not text-only mirror, not clone). Validated bed3q 2026-06-22.
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
  "shot": {
    "composition": "full room geography in one frame, bed centred on rear wall, single framed print centered above the headboard, devotional items legible, floor spanning foreground",
    "framing": "WS establishing, floor visible bottom 15%, ceiling line visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "room corner opposite the bed",
    "camera_direction": "looking across the floor toward the headboard wall, off-axis, furniture edges as gentle leading lines",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "soft diffused daylight key from the curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```

### Cell B — BED 3/4 → `E01_kamar_bed3q.png` · ✅ LOCKED
Serves SEQ1-SC01-SH04 (MS side of bed) + SEQ6-SC03 (Herman lying / coda).
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
  "shot": {
    "composition": "three-quarter view of the bed, the bed dominantly fills most of the frame at a diagonal, both pillow sides clearly visible, headboard and single framed Hokusai print along the rear wall, nightstand camera-right beside the headboard, foot of the bed toward camera",
    "framing": "tight MWS of the bed, the bed fills the frame edge to edge, only a thin strip of foreground rug, minimal wall above the headboard, surrounding room kept mostly out of frame",
    "angle": "eye-level slight high angle, three-quarter onto the bed",
    "camera_position": "pushed in close at the foot-left corner of the bed, much closer than the master, the bed surface dominant in frame",
    "camera_direction": "looking diagonally across the bed toward the headboard wall, bed frame edges as leading lines to the headboard",
    "camera": "35mm prime spherical, deep focus front to back",
    "lighting": "soft diffused daylight key from the curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```

### Cell W — WALL-ART REVERSE → `E01_kamar_wallart_reverse.png` · ✅ LOCKED
Reverse angle, headboard wall head-on; locks the Hokusai anchor + the single nightstand on the right (left side empty — room has only one nightstand).
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
  "shot": {
    "composition": "reverse angle facing the headboard wall head-on, single framed Hokusai print centered and dominant above the headboard, headboard and pillows across the lower frame, only the single nightstand on the right side of the headboard, the left side of the headboard kept clear and empty plain floor",
    "framing": "MWS of the headboard wall, full framed print visible with wall margin around it, headboard and pillow tops across the bottom",
    "angle": "eye-level straight-on, square to the headboard wall",
    "camera_position": "at the foot of the bed centered, looking back toward the headboard",
    "camera_direction": "facing the rear headboard wall directly, symmetrical, framed Hokusai print as the central subject",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft diffused daylight key from the curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
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

---

## 4. Status manifest
| Cell | Angle | File | Status |
|---|---|---|---|
| M | establishing wide | `E01_kamar_master.png` | ✅ LOCKED (clock-free, dinding Hokusai-only, mukena stabil) — regenerated 2026-06-23 |
| B | bed 3/4 | `E01_kamar_bed3q.png` | ✅ LOCKED (clock-free, tight bed-filling, dua sisi bantal jelas) — regenerated 2026-06-23 |
| N | nightstand insert | `E01_kamar_nightstand.png` | ✅ LOCKED (clock-free, HP screen-up tepi-depan reachable) — regenerated 2026-06-23 |
| W | wall-art reverse | `E01_kamar_wallart_reverse.png` | ⏸ DEFERRED — tidak dipakai SEQ1-SC01 (hygiene). Plat lama masih ber-jam + spec sudah dikoreksi (1 nakas, kiri kosong); regen head-on saat ada scene yang memakainya. Jangan dipakai apa adanya. |

> **Clock removal (2026-06-23):** jam weker analog dibuang dari seluruh spec E01 (jarum analog tak andal di t2i, 2 render gagal; waktu subuh tetap via kartu AE `Waktu Subuh · 04.42` di layar HP). Keempat plat lama mengandung jam → regen **master dulu** (clock-free), lalu derivatif attach master baru. SH01 `sc01_sh01_*` yang sudah ACCEPT aman (jam di luar crop CU).

Storage: `environment-images/E01_kamar/` (+ `_rejected/`). Naming: `E01_kamar_<angle>.png`.
Generate W and N via the `shot`-only-rewrite method: upload `E01_kamar_master.png` as reference + paste §1 verbatim + the cell's `shot` block.

---

*E01 Kamar environment sheet v1.0 · Explainer Video 2 · 2026-06-22 · method [[00-README-ENV]] · companion [[08-character-sheet/H-herman]]*
