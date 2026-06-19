---
title: Character Sheet — Herman (50) · GATE 0
tags: [explainer-video-2, character-sheet, herman, gate-0]
status: draft
created: 2026-06-19
updated: 2026-06-19
aliases: [ev2-herman-sheet, H-herman]
---

# Character Sheet — HERMAN (50) · tag H
> Method, 9-cell template, direction protocol, naming → [[00-README]]. Style tokens + anchors → [[07-style-reference]]. Scene truth → [[03-scene-detail]].

---

## 1. Identity lock (FIXED — paste verbatim into Lapis 3 of every Herman prompt)
```json
"character_identity": {
  "role": "Jakarta middle-class export-import office supervisor, modest mature man",
  "ethnicity": "modern Jakartan features, Javanese urban descent",
  "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
  "age": "46 years old",
  "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
  "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
}
```
*Never changes scene-to-scene:* uniformly salt-and-pepper hair (even grey distribution), trimmed moustache, calm eyes. Render-age `46` to land real 50 (model ages up).

**Fixed Lapis-6 anchors (Herman):** `makeup_artist: Eryn Krueger Mekash` · `hair_stylist: Tim Muir` · `costume_designer: Deborah Hopper` (child-style tokens in [[07-style-reference]] §2).

---

## 2. Baseline style for plates (neutral reference outfit)
Used for ALL 9 plate cells — the consistent look the reference-lock learns. Per-scene wardrobe (§4) differs and belongs to GATE B keyframes, NOT the plates.
```json
"character_style": {
  "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
  "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar relaxed fit muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
  "hair": "short side-part, uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural",
  "footwear": "plain leather loafers soft sole muted"
}
```

---

## 3. Plate matrix — 9 full t2i prompts (3 view × 3 shot)
Authored on the `prompt-rules-image-generation.md` 6-layer pattern + token discipline + banned-list. Each is copy-paste ready (no placeholders, per vault standard).

**PLATE DEVIATIONS from prompt-rules (declared, justified — a reference plate is NOT a graded scene):**
1. `color_grade` = neutral true-to-life, NOT the Deakins deck grade — a plate must capture accurate identity for Kling reference-locking, not a stylized look. The WARM video grade is applied later at GATE B keyframes, not here.
2. Clean prime spherical lens, NOT Panavision anamorphic — anamorphic distorts proportion; a turnaround needs undistorted geometry.
3. `scene_depth` + `on_screen_graphic` omitted — plain solid white background, subject isolated.
4. Crew pairs scoped to identity-styling only (costume/makeup/hair); director/lighting/PD/interior dropped — no scene to design.
5. `aspect_ratio` per shot type (GPT Image 2 supports all natively): **full body `9:16`** (tallest, whole figure + headroom + floor), **medium `2:3`**, **close-up `4:5`** (face fills, headshot ratio). Each shot a distinct ratio.
All OTHER rules hold: token strings, zero negation, garment specified affirmatively (anti-auto-batik), facial_features texture-only, identity block verbatim.

**Direction protocol ([[00-README]] §3.1):** generate Front → Profile A → **Profile B as a MIRROR of Profile A via the Profile-A plate uploaded as reference** (image-conditioning bypasses unreliable text left/right). Label by visible cheek/ear; files use `profileA`/`profileB`, never left/right.

---

### Cell 1 — Front · Full body → `H_herman_front_full.png`
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
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural",
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
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, neat working-class grooming"
}
```

### Cell 2 — Front · Medium → `H_herman_front_medium.png`
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
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural",
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
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, neat working-class grooming"
}
```

### Cell 3 — Front · Close-up → `H_herman_front_closeup.png`
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
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey collar visible at neckline",
    "hair": "short side-part, uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural"
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
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, neat working-class grooming"
}
```

### Cell 4 — Profile A · Full body → `H_herman_profileA_full.png`
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
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural",
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
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, neat working-class grooming"
}
```

### Cell 5 — Profile A · Medium → `H_herman_profileA_medium.png`
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
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural"
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
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, neat working-class grooming"
}
```

### Cell 6 — Profile A · Close-up → `H_herman_profileA_closeup.png`
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
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, muted slate-grey collar visible at neckline",
    "hair": "short side-part, uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural"
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
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, neat working-class grooming"
}
```

### Cells 7–9 — Profile B (opposite side)
**Generate each as a MIRROR of the matching Profile-A plate: upload `H_herman_profileA_<shot>.png` as a reference image, instruct "same identical character and outfit, flip to the opposite full profile — the cheek hidden in the reference now faces camera, nose silhouette points the opposite direction."** Do NOT rely on a text "left/right" token. The JSON below describes the target by anatomy; the reference image enforces the mirror.

### Cell 7 — Profile B · Full body → `H_herman_profileB_full.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": "H_herman_profileA_full.png — same identical character and outfit, mirrored to opposite profile",
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural",
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
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, neat working-class grooming"
}
```

### Cell 8 — Profile B · Medium → `H_herman_profileB_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": "H_herman_profileA_medium.png — same identical character and outfit, mirrored to opposite profile",
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, relaxed fit, muted slate-grey, pressed cotton-twill trousers mid-rise straight charcoal solid",
    "hair": "short side-part, uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural"
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
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, neat working-class grooming"
}
```

### Cell 9 — Profile B · Close-up → `H_herman_profileB_closeup.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": "H_herman_profileA_closeup.png — same identical character and outfit, mirrored to opposite profile",
  "character_identity": {
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved",
    "wardrobe": "plain short-sleeve cotton-poplin shirt soft collar, muted slate-grey collar visible at neckline",
    "hair": "short side-part, uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural"
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
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, neat working-class grooming"
}
```

---

## 4. Per-scene wardrobe (Herman in 6 scenes)
Hair (Tim Muir uniformly salt-and-pepper side-part) + makeup (Eryn Krueger Mekash mature lived-in) FIXED throughout; covered by peci only in sholat. Only wardrobe/footwear vary.

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

*Herman sheet v0.3 (9 full t2i plate prompts) · Explainer Video 2 · 2026-06-19 · cites [[07-style-reference]] · method [[00-README]]*
