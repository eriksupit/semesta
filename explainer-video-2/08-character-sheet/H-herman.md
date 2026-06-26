---
title: Character Sheet — Herman (46) · GATE 0
tags: [explainer-video-2, character-sheet, herman, gate-0]
status: draft
created: 2026-06-19
updated: 2026-06-26
aliases: [ev2-herman-sheet, H-herman]
---

# Character Sheet — HERMAN (46) · tag H
> Method, 9-cell template, direction protocol, naming → [[00-README]]. Style tokens + anchors → [[07-style-reference]]. Scene truth → [[03-scene-detail]].
>
> **PLATES STATUS: 12/12 generated + accepted 2026-06-26** (clean-shaven, age-token 41 ~46, DAG-chained from `front_closeup` master; on disk `character-images/H_herman/`).

---

## 1. Identity lock (FIXED — paste verbatim into Lapis 3 of every Herman prompt)
```json
"character_identity": {
  "role": "Jakarta middle-class export-import office supervisor, modest mature man",
  "ethnicity": "modern Jakartan features, Javanese urban descent",
  "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
  "age": "41 years old",
  "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
  "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
}
```
*Never changes scene-to-scene:* dark hair greying lightly at the temples, clean-shaven (no moustache, fully shaved upper lip), calm eyes. Render-age `41` to land real ~46 (TTI ages up ~5y, validated 2026-06-26 — prior `46`-token landed ~52 reading "too old"). Herman token 41 (~46 real), Ratna token 37 (~42 real) — Herman ~4y older in canon.

**Fixed Lapis-6 anchors (Herman):** `makeup_artist: Eryn Krueger Mekash` · `hair_stylist: Tim Muir` · `costume_designer: Deborah Hopper` (child-style tokens in [[07-style-reference]] §2).

---

## 2. Baseline style for plates (neutral reference outfit)
Used for ALL 12 plate cells — the consistent look the reference-lock learns. Per-scene wardrobe (§4) differs and belongs to GATE B keyframes, NOT the plates.
```json
"character_style": {
  "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
  "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar relaxed fit muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
  "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural",
  "footwear": "plain leather loafers soft sole muted"
}
```

---

## 3. Plate matrix — 12 full t2i prompts (4 view × 3 shot: front · profileA · profileB · rear)
Authored on the `prompt-rules-image-generation.md` 6-layer pattern + token discipline + banned-list. Each is copy-paste ready (no placeholders, per vault standard).

> **🔗 IDENTITY-PROPAGATION DAG + GENERATION ORDER (BINDING — Erik, 2026-06-26).** All 12 plates = FULL prompt each (never edit-in-place; each is a different view/shot). `CU Front` = root master (face), generated from scratch. Every other plate attaches earlier-accepted plates as identity/framing reference. **Generate in this exact order — each step needs the prior ones accepted on disk:**
>
> | # | Plate | File | Attach (reference images) |
> |---|-------|------|----------------------------|
> | 1 | CU Front | `H_herman_front_closeup.png` | — (from scratch · MASTER) |
> | 2 | CU ProfileA | `H_herman_profileA_closeup.png` | front_closeup |
> | 3 | CU ProfileB | `H_herman_profileB_closeup.png` | front_closeup + profileA_closeup |
> | 4 | CU Rear | `H_herman_rear_closeup.png` | front_closeup + profileA_closeup + profileB_closeup |
> | 5 | Medium Front | `H_herman_front_medium.png` | front_closeup |
> | 6 | Medium ProfileA | `H_herman_profileA_medium.png` | front_medium + profileA_closeup |
> | 7 | Medium ProfileB | `H_herman_profileB_medium.png` | profileA_medium + profileB_closeup |
> | 8 | Medium Rear | `H_herman_rear_medium.png` | front_medium + rear_closeup |
> | 9 | FB Front | `H_herman_front_full.png` | front_medium |
> | 10 | FB ProfileA | `H_herman_profileA_full.png` | front_full + profileA_medium |
> | 11 | FB ProfileB | `H_herman_profileB_full.png` | profileA_full + profileB_medium |
> | 12 | FB Rear | `H_herman_rear_full.png` | front_full + rear_closeup |
>
> Per-cell `**Attach:**` line under each header repeats its row. Where a cell's JSON still carries a `reference_image` field, that field is reconciled to this map. The face baseline is clean-shaven, age-token 41 (see §1).

**PLATE DEVIATIONS from prompt-rules (declared, justified — a reference plate is NOT a graded scene):**
1. `color_grade` = neutral true-to-life, NOT the Deakins deck grade — a plate must capture accurate identity for Kling reference-locking, not a stylized look. The WARM video grade is applied later at GATE B keyframes, not here.
2. Clean prime spherical lens, NOT Panavision anamorphic — anamorphic distorts proportion; a turnaround needs undistorted geometry.
3. `scene_depth` + `on_screen_graphic` omitted — plain solid white background, subject isolated.
4. Crew pairs scoped to identity-styling only (costume/makeup/hair); director/lighting/PD/interior dropped — no scene to design.
5. `aspect_ratio` per shot type (GPT Image 2 supports all natively): **full body `9:16`** (tallest, whole figure + headroom + floor), **medium `2:3`**, **close-up `4:5`** (face fills, headshot ratio). Each shot a distinct ratio.
All OTHER rules hold: token strings, zero negation, garment specified affirmatively (anti-auto-batik), facial_features texture-only, identity block verbatim.

**Direction protocol ([[00-README]] §3.1):** generate Front → Profile A → **Profile B as a MIRROR of Profile A via the Profile-A plate uploaded as reference** (image-conditioning bypasses unreliable text left/right). Label by visible cheek/ear; files use `profileA`/`profileB`, never left/right.

---

## Row 1 — Close-up plates (4:5)

### Cell 1 — Front · Close-up → `H_herman_front_closeup.png`
**Generate order #1 · MASTER · Attach: — (from scratch, no reference)**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 41 years old",
    "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey collar visible at neckline",
    "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural"
  },
  "subject_state": "static",
  "action": "head and shoulders still, facing lens",
  "pose": "head level, shoulders squared",
  "gesture": "shoulders relaxed level",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens, both eyes open even",
  "framing": "CU close-up, face fills frame, head and top of shoulders",
  "angle": "eye-level straight-on, front view, both eyes visible symmetric, nose centered",
  "camera": "100mm portrait prime spherical, soft background separation",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "4:5",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic register, dark hair greying lightly at the temples, neat working-class grooming"
}
```

### Cell 2 — Profile A · Close-up → `H_herman_profileA_closeup.png`
**Generate order #2 · Attach: front_closeup**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": ["H_herman_front_closeup.png — same identical man, locked face identity to rotate into this profile"],
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 41 years old",
    "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, muted slate-grey collar visible at neckline",
    "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural"
  },
  "subject_state": "static",
  "action": "head and shoulders still in full profile",
  "pose": "head level, turned ninety degrees sideways",
  "gesture": "shoulders relaxed",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "CU close-up, profile face fills frame, head and top of shoulder",
  "angle": "eye-level, full profile view, subject facing camera-left frame-left audience POV, head rotated ninety degrees, single ear and single eye visible, nose and lips in clean silhouette against white, near cheek toward camera",
  "camera": "100mm portrait prime spherical, soft background separation",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "4:5",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic register, dark hair greying lightly at the temples, neat working-class grooming"
}
```

### Cell 3 — Profile B · Close-up → `H_herman_profileB_closeup.png`
**Generate order #3 · Attach: front_closeup + profileA_closeup**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": ["H_herman_front_closeup.png — same identical man, locked face", "H_herman_profileA_closeup.png — the profileA side to mirror to the opposite profile"],
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 41 years old",
    "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, muted slate-grey collar visible at neckline",
    "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural"
  },
  "subject_state": "static",
  "action": "head and shoulders still in opposite full profile",
  "pose": "head level, turned ninety degrees to the opposite side",
  "gesture": "shoulders relaxed",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "CU close-up, opposite profile face fills frame, head and top of shoulder",
  "angle": "eye-level, opposite full profile view, subject facing camera-right frame-right audience POV, head rotated ninety degrees the other way, previously hidden ear and single eye now visible, nose and lips in clean silhouette pointing opposite direction against white, near cheek toward camera",
  "camera": "100mm portrait prime spherical, soft background separation",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "4:5",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic register, dark hair greying lightly at the temples, neat working-class grooming"
}
```

---

### Cell 4 — Rear · Close-up → `H_herman_rear_closeup.png`
**Generate order #4 · Attach: front_closeup + profileA_closeup + profileB_closeup**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": ["H_herman_front_closeup.png — same identical man, locked face and hairline", "H_herman_profileA_closeup.png — the left head shape", "H_herman_profileB_closeup.png — the right head shape; rotate to show the back of the head, face turned fully away from camera"],
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 41 years old",
    "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, muted slate-grey collar visible at neckline",
    "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural"
  },
  "subject_state": "static",
  "action": "back of the head and top of shoulders still, face away from the lens",
  "pose": "head level, back of the head squared to camera",
  "gesture": "shoulders relaxed",
  "expression": "face fully turned away from camera, hidden from the lens, only the back of the head and nape shown",
  "framing": "CU close-up from behind, the back of the head fills the frame, nape and hairline and both ear edges, top of shoulders",
  "angle": "eye-level straight-on from directly behind, rear view, occiput and nape toward the lens, hair part visible from the back, both ears at the sides, face away from the lens",
  "camera": "100mm portrait prime spherical, soft background separation",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "4:5",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic register, dark hair greying lightly at the temples, neat working-class grooming"
}
```

---

## Row 2 — Medium plates (2:3)

### Cell 5 — Front · Medium → `H_herman_front_medium.png`
**Generate order #5 · Attach: front_closeup**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": ["H_herman_front_closeup.png — same identical man, locked face identity"],
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 41 years old",
    "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural",
    "footwear": "plain leather loafers soft sole muted, low clean profile"
  },
  "subject_state": "static",
  "action": "standing still, torso squared to camera, arms relaxed at sides",
  "pose": "upright relaxed, shoulders squared level",
  "gesture": "shoulders relaxed level, arms at sides out of frame",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "MS medium shot, waist up, subject centered",
  "angle": "eye-level straight-on, front view, both ears symmetric, nose centered",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic register, dark hair greying lightly at the temples, neat working-class grooming"
}
```

### Cell 6 — Profile A · Medium → `H_herman_profileA_medium.png`
**Generate order #6 · Attach: front_medium + profileA_closeup**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": ["H_herman_front_medium.png — medium framing and build anchor", "H_herman_profileA_closeup.png — the profileA face identity to carry"],
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 41 years old",
    "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural"
  },
  "subject_state": "static",
  "action": "standing still in full profile, torso turned ninety degrees, arms relaxed",
  "pose": "upright relaxed, body sideways to camera",
  "gesture": "arms relaxed at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "MS medium shot, waist up, profile",
  "angle": "eye-level, full profile view, subject facing camera-left frame-left audience POV, head rotated ninety degrees sideways, single ear visible, nose in clean silhouette, near cheek toward camera",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic register, dark hair greying lightly at the temples, neat working-class grooming"
}
```

### Cell 7 — Profile B · Medium → `H_herman_profileB_medium.png`
**Generate order #7 · Attach: profileA_medium + profileB_closeup**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": ["H_herman_profileA_medium.png — same identical man, medium framing and build anchor, mirror to the opposite profile", "H_herman_profileB_closeup.png — the profileB face identity to carry"],
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 41 years old",
    "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural"
  },
  "subject_state": "static",
  "action": "standing still in opposite full profile, torso turned ninety degrees the other way, arms relaxed",
  "pose": "upright relaxed, body sideways to camera opposite direction",
  "gesture": "arms relaxed at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "MS medium shot, waist up, opposite profile",
  "angle": "eye-level, opposite full profile view, subject facing camera-right frame-right audience POV, head rotated ninety degrees the other way, previously hidden ear and cheek now toward camera, nose in clean silhouette pointing opposite direction",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic register, dark hair greying lightly at the temples, neat working-class grooming"
}
```

### Cell 8 — Rear · Medium → `H_herman_rear_medium.png`
**Generate order #8 · Attach: front_medium + rear_closeup**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": ["H_herman_front_medium.png — same identical man, medium framing and build and wardrobe anchor", "H_herman_rear_closeup.png — the locked back-of-head, rotate the body to show the back, face turned fully away from camera"],
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 41 years old",
    "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural"
  },
  "subject_state": "static",
  "action": "standing still seen from directly behind, torso squared away from camera, arms relaxed at sides",
  "pose": "upright relaxed, back squared to camera, body facing fully away",
  "gesture": "shoulders relaxed level, arms at sides",
  "expression": "face fully turned away from camera, hidden from the lens, only the back of the head shown",
  "framing": "MS medium shot from behind, waist up, back of the head and shoulders centered",
  "angle": "eye-level straight-on from directly behind, rear view, back of the head and shoulders squared to camera, the nape and hairline toward the lens, both ears just visible at the sides, face away from the lens",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic register, dark hair greying lightly at the temples, neat working-class grooming"
}
```

## Row 3 — Full-body plates (9:16)

### Cell 9 — Front · Full body → `H_herman_front_full.png`
**Generate order #9 · Attach: front_medium**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": ["H_herman_front_medium.png — same identical man, framing and build and face anchor"],
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 41 years old",
    "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural",
    "footwear": "plain leather loafers soft sole muted, low clean profile"
  },
  "subject_state": "static",
  "action": "standing still upright for reference, weight even both feet, arms relaxed straight at sides",
  "pose": "neutral standing feet shoulder-width, shoulders squared to camera",
  "gesture": "both arms relaxed straight at sides, hands open natural",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "full body shot, crown to loafer sole visible, floor line visible, generous headroom above crown",
  "angle": "eye-level straight-on, front view, subject squared facing camera, both ears symmetric, nose centered",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic register, dark hair greying lightly at the temples, neat working-class grooming"
}
```

### Cell 10 — Profile A · Full body → `H_herman_profileA_full.png`
**Generate order #10 · Attach: front_full + profileA_medium**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": ["H_herman_front_full.png — full-body build and framing anchor", "H_herman_profileA_medium.png — the profileA identity at medium"],
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 41 years old",
    "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural",
    "footwear": "plain leather loafers soft sole muted, low clean profile"
  },
  "subject_state": "static",
  "action": "standing still rotated to full profile, near shoulder toward camera, arms relaxed at sides",
  "pose": "neutral standing feet together, body turned ninety degrees sideways",
  "gesture": "both arms relaxed straight at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "full body shot, crown to loafer sole visible, floor line visible, generous headroom",
  "angle": "eye-level, full profile view, subject facing camera-left frame-left audience POV, head and torso rotated ninety degrees sideways, single ear visible, nose in clean silhouette against white background, near cheek fully toward camera",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic register, dark hair greying lightly at the temples, neat working-class grooming"
}
```

### Cell 11 — Profile B · Full body → `H_herman_profileB_full.png`
**Generate order #11 · Attach: profileA_full + profileB_medium**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": ["H_herman_profileA_full.png — same identical man, full-body build and framing anchor, mirror to the opposite profile", "H_herman_profileB_medium.png — the profileB identity at medium"],
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 41 years old",
    "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural",
    "footwear": "plain leather loafers soft sole muted, low clean profile"
  },
  "subject_state": "static",
  "action": "standing still in opposite full profile, the other shoulder now toward camera, arms relaxed at sides",
  "pose": "neutral standing feet together, body turned ninety degrees to the opposite side",
  "gesture": "both arms relaxed straight at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "full body shot, crown to loafer sole visible, floor line visible, generous headroom",
  "angle": "eye-level, opposite full profile view, subject facing camera-right frame-right audience POV, head and torso rotated ninety degrees the other way, the previously hidden ear and cheek now fully toward camera, nose in clean silhouette pointing opposite direction against white",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic register, dark hair greying lightly at the temples, neat working-class grooming"
}
```

### Cell 12 — Rear · Full body → `H_herman_rear_full.png`
**Generate order #12 · Attach: front_full + rear_medium**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": ["H_herman_front_full.png — same identical man, full-body build and wardrobe and framing anchor", "H_herman_rear_closeup.png — the locked back-of-head, rotate the body to show the back, face turned fully away from camera"],
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 41 years old",
    "facial_features": "luminous healthy complexion, smooth even skin texture, faint expression lines only at the eye corners, clean-shaven smooth bare upper lip and jaw, fully shaved, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, dark hair greying only lightly at the temples, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural",
    "footwear": "plain leather loafers soft sole muted, low clean profile"
  },
  "subject_state": "static",
  "action": "standing still seen from directly behind, back toward camera, arms relaxed at sides",
  "pose": "neutral standing feet shoulder-width, back squared to camera, body facing fully away",
  "gesture": "both arms relaxed straight at sides, hands open natural",
  "expression": "face fully turned away from camera, hidden from the lens, only the back of the head shown",
  "framing": "full body shot from behind, crown to loafer sole visible, floor line visible, generous headroom above crown",
  "angle": "eye-level straight-on from directly behind, rear view, back of the head and shoulders and back squared to camera, the nape and hairline toward the lens, both ears just visible at the sides, face away from the lens",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic register, dark hair greying lightly at the temples, neat working-class grooming"
}
```

## 4. Per-scene wardrobe (Herman in 6 scenes)
Hair (Tim Muir dark side-part greying lightly at the temples) + makeup (Eryn Krueger Mekash lived-in, smoother skin) FIXED throughout; covered by peci only in sholat. Only wardrobe/footwear vary.

| Scene | Look | Wardrobe tokens | Footwear | Note |
|---|---|---|---|---|
| SEQ1-SC01 | W1 sleep→sarung | `plain cotton crew-neck sleep tee muted, then solid plain-weave sarong dark muted colorway wrapped waist` | barefoot | wakes, dons advertised sarong (diegetic payoff) |
| SEQ1-SC02 | W2 sholat | `long-sleeve plain koko shirt stand-collar muted off-white, solid plain-weave sarong dark muted, black velvet peci cap` | barefoot | imam; hair under peci; sakral SH02+ |
| SEQ2-SC02 | W3 workday | `plain short-sleeve cotton-poplin shirt soft collar muted slate-grey, pressed cotton-twill trousers charcoal solid` | `plain leather loafers soft sole muted` | continuity across workday |
| SEQ3-SC03 | W3 workday | *(identical to SEQ2-SC02 — same day; lock token string identical)* | same | trading break, teaches Rian |
| SEQ4-SC01 | W3 workday | *(identical W3, late-afternoon orange side-light via color_grade)* | same | government-as-tenant |
| SEQ6-SC01 | W4 evening home | `same poplin shirt now untucked relaxed, sleeves unrolled, collar loosened, charcoal trousers` | flat house slippers | family dinner, opt-in syariah |
| SEQ6-SC03 | W1 sleep | `plain cotton crew-neck sleep tee muted` (bookend SEQ1-SC01) | barefoot | coda screen-off; identity + room locked to SEQ1-SC01 |

*Continuity:* W3 = ONE outfit across SEQ2-SC02 → SEQ3-SC03 → SEQ4-SC01 (same day, identical token string). SEQ6-SC03 mirrors SEQ1-SC01 exactly (bookend).

---

*Herman sheet v0.4 (12 full t2i plate prompts incl. rear view; clean-shaven, age-token 41) · Explainer Video 2 · 2026-06-26 · cites [[07-style-reference]] · method [[00-README]]*
