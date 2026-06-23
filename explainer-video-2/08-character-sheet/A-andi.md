---
title: Character Sheet — Andi (10, SD-daring student) · GATE 0
tags: [explainer-video-2, character-sheet, andi, gate-0]
status: draft
created: 2026-06-21
updated: 2026-06-21
aliases: [ev2-andi-sheet, A-andi]
---

# Character Sheet — ANDI (10, primary-school boy) · tag A
> Method, 9-cell template, direction protocol, naming → [[00-README]]. Style tokens + anchors → [[07-style-reference]]. Scene truth → [[03-scene-detail]].

---

## 0. Notes (read first)
- **Boy, head uncovered in every scene → 9 uncovered plates only.** SEQ6-SC02 (ngaji ba'da Maghrib) prose ([[03-scene-detail]]:268/276) shows Andi facing a kitab under warm light — **head bare for Andi, zero peci/koko**. The representative-covered-plate rule (Ratna hijab / Herman peci) does NOT apply here. 9 plates total.
- **Render-age `10` LOCKED (verified 2026-06-21 on `A_andi_front_full.png`).** The "render-age below real age" rule was validated for ADULTS (Herman 50→46, Ratna 45→41, Lisa 20→19); for a child the ageing-up bias did NOT appear — `boy 10 years old` rendered a plausible 10-year-old, no teen drift. No age compensation needed for children; lock at real age.
- **No body-feminization tokens.** Andi is a boy: plain child build, normal child garment fit. The `34C bustline` / `womanly` / `fitted` tokens were Lisa-specific fixes — they do NOT carry here ([[lessons.md]] 2026-06-21).
- **Makeup = bare child skin, written POSITIVE.** Canonical anchor [[07-style-reference]] §3.3 negates the makeup layer with a `no`-token that violates positive-only + fails the grep-gate. Rewritten positive: `bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine`. (`zero shine` is the locked makeup finish token, used + approved across Herman 9/9 + Lisa 9/9; the banned keyword-leak token is `sheen`, not `shine`.)
- **Plate hair finish = matte (anti-sheen plate standard, [[00-README]]:43).** Hair worn in its natural short crop on all plates; styling stays GATE B.
- **Keyword-leak guard:** `role` kept free of any environment- or covering-trigger token (the `hijabi` leak that forced a headscarf on Ratna). Andi's role = clean child descriptors only.

---

## 1. Identity lock (FIXED — paste verbatim into Lapis 3 of every Andi prompt)
```json
"character_identity": {
  "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
  "ethnicity": "modern Jakartan features, Javanese urban descent",
  "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
  "age": "boy 10 years old",
  "facial_features": "smooth clear child complexion, soft rounded cheeks, bright lively steady eyes, full soft natural brows, small even features, smooth even skin texture",
  "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
}
```
*Never changes scene-to-scene:* child facial identity, soft rounded cheeks, bright lively eyes, full soft brows. Render-age `10` (verify on first plate). Hair colour/shape fixed (uniformly dark, short natural crop, side parting on all plates).

**Fixed Lapis-6 anchors (Andi):** `hair_stylist: Anissa Salazar` · `costume_designer: Deborah Hopper`. *(No makeup_artist pair — bare child skin, makeup layer is none.)*

---

## 2. Baseline style for plates (neutral reference outfit — hair in natural crop)
Used for ALL 9 plate cells — the consistent look the reference-lock learns. Per-scene wardrobe (§4) differs and belongs to GATE B keyframes, NOT the plates.
```json
"character_style": {
  "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
  "wardrobe": "child crew-neck cotton tee soft jersey relaxed fit muted solid slate, child elastic-waist shorts cotton twill knee-length desaturated navy",
  "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
  "footwear": "child velcro canvas sneakers, white rubber sole, plain"
}
```
*Plate makeup note:* bare child skin per [[07-style-reference]] §3.3, finish matte zero shine (anti-sheen plate standard). No cosmetic layer; `HD makeup` / `HD setting powder` never used (specular trigger).

---

## 3. Plate matrix — 9 full t2i prompts (3 view × 3 shot)
Authored on the `prompt-rules-image-generation.md` 6-layer pattern + token discipline + banned-list. Each is copy-paste ready (zero placeholders).

**PLATE DEVIATIONS from prompt-rules (declared, justified — a reference plate is NOT a graded scene):**
1. `color_grade` = neutral true-to-life, NOT the Deakins deck grade — a plate must capture accurate identity for Kling reference-locking. The WARM video grade is applied later at GATE B keyframes.
2. Clean prime spherical lens, NOT Panavision anamorphic — anamorphic distorts proportion; a turnaround needs undistorted geometry.
3. `scene_depth` + `on_screen_graphic` omitted — plain solid white background, subject isolated.
4. Crew pairs scoped to identity-styling only (costume/hair); director/lighting/PD/interior dropped (plate background plain white, nothing to design). Makeup pair dropped — bare child skin.
5. `aspect_ratio` per shot type: **full body `9:16`**, **medium `2:3`**, **close-up `4:5`**.
6. Hair worn in natural short crop per §0.
All OTHER rules hold: token strings, zero negation (positive-only), garment specified affirmatively (anti-auto-batik), facial_features texture-only, identity block verbatim.

**Direction protocol ([[00-README]] §3.1):** generate Front → Profile A → **Profile B as a MIRROR of Profile A via the Profile-A plate uploaded as reference**. Label by visible cheek/ear; files use `profileA`/`profileB`, never left/right. Profile A = subject faces `camera-left`; Profile B = `camera-right`.

---

### Cell 1 — Front · Full body → `A_andi_front_full.png`
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
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "smooth clear child complexion, soft rounded cheeks, bright lively steady eyes, full soft natural brows, small even features, smooth even skin texture",
    "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
  },
  "character_style": {
    "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "child crew-neck cotton tee soft jersey relaxed fit muted solid slate, child elastic-waist shorts cotton twill knee-length desaturated navy",
    "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "child velcro canvas sneakers, white rubber sole, plain"
  },
  "subject_state": "static",
  "action": "standing still upright for reference, weight even both feet, arms relaxed straight at sides",
  "pose": "neutral standing feet shoulder-width, shoulders squared to camera",
  "gesture": "both arms relaxed straight at sides, hands open natural",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "full body shot, crown to sneaker sole visible, floor line visible, generous headroom above crown",
  "angle": "eye-level straight-on, front view, subject squared facing camera, both ears symmetric, nose centered",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual child wear, fabric worn laundered, class-accurate daily register",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday child hair, real-texture straight black, short crop side parting, unstyled lived-in matte finish"
}
```

### Cell 2 — Front · Medium → `A_andi_front_medium.png`
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
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "smooth clear child complexion, soft rounded cheeks, bright lively steady eyes, full soft natural brows, small even features, smooth even skin texture",
    "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
  },
  "character_style": {
    "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "child crew-neck cotton tee soft jersey relaxed fit muted solid slate, child elastic-waist shorts cotton twill knee-length desaturated navy",
    "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "child velcro canvas sneakers, white rubber sole, plain"
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
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual child wear, fabric worn laundered, class-accurate daily register",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday child hair, real-texture straight black, short crop side parting, unstyled lived-in matte finish"
}
```

### Cell 3 — Front · Close-up → `A_andi_front_closeup.png`
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
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "smooth clear child complexion, soft rounded cheeks, bright lively steady eyes, full soft natural brows, small even features, smooth even skin texture",
    "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
  },
  "character_style": {
    "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "child crew-neck cotton tee soft jersey muted solid slate collar visible at neckline",
    "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural"
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
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual child wear, fabric worn laundered, class-accurate daily register",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday child hair, real-texture straight black, short crop side parting, unstyled lived-in matte finish"
}
```

### Cell 4 — Profile A · Full body → `A_andi_profileA_full.png`
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
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "smooth clear child complexion, soft rounded cheeks, bright lively steady eyes, full soft natural brows, small even features, smooth even skin texture",
    "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
  },
  "character_style": {
    "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "child crew-neck cotton tee soft jersey relaxed fit muted solid slate, child elastic-waist shorts cotton twill knee-length desaturated navy",
    "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "child velcro canvas sneakers, white rubber sole, plain"
  },
  "subject_state": "static",
  "action": "standing still rotated to full profile, near shoulder toward camera, arms relaxed at sides",
  "pose": "neutral standing feet together, body turned ninety degrees sideways",
  "gesture": "both arms relaxed straight at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "full body shot, crown to sneaker sole visible, floor line visible, generous headroom",
  "angle": "eye-level, full profile view, subject facing camera-left frame-left audience POV, head and torso rotated ninety degrees sideways, single ear visible, nose in clean silhouette against white background, near cheek fully toward camera",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual child wear, fabric worn laundered, class-accurate daily register",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday child hair, real-texture straight black, short crop side parting, unstyled lived-in matte finish"
}
```

### Cell 5 — Profile A · Medium → `A_andi_profileA_medium.png`
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
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "smooth clear child complexion, soft rounded cheeks, bright lively steady eyes, full soft natural brows, small even features, smooth even skin texture",
    "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
  },
  "character_style": {
    "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "child crew-neck cotton tee soft jersey relaxed fit muted solid slate, child elastic-waist shorts cotton twill knee-length desaturated navy",
    "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural"
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
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual child wear, fabric worn laundered, class-accurate daily register",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday child hair, real-texture straight black, short crop side parting, unstyled lived-in matte finish"
}
```

### Cell 6 — Profile A · Close-up → `A_andi_profileA_closeup.png`
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
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "smooth clear child complexion, soft rounded cheeks, bright lively steady eyes, full soft natural brows, small even features, smooth even skin texture",
    "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
  },
  "character_style": {
    "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "child crew-neck cotton tee soft jersey muted solid slate collar visible at neckline",
    "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural"
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
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual child wear, fabric worn laundered, class-accurate daily register",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday child hair, real-texture straight black, short crop side parting, unstyled lived-in matte finish"
}
```

### Cells 7–9 — Profile B (opposite side)
**Generate each as a MIRROR of the matching Profile-A plate: upload `A_andi_profileA_<shot>.png` as a reference image, instruct "same identical character and outfit, flip to the opposite full profile — the cheek hidden in the reference now faces camera, nose silhouette points the opposite direction."** Do NOT rely on a text left/right token. The JSON below describes the target by anatomy; the reference image enforces the mirror.

### Cell 7 — Profile B · Full body → `A_andi_profileB_full.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": "A_andi_profileA_full.png — same identical character and outfit, mirrored to opposite profile",
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "smooth clear child complexion, soft rounded cheeks, bright lively steady eyes, full soft natural brows, small even features, smooth even skin texture",
    "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
  },
  "character_style": {
    "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "child crew-neck cotton tee soft jersey relaxed fit muted solid slate, child elastic-waist shorts cotton twill knee-length desaturated navy",
    "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "child velcro canvas sneakers, white rubber sole, plain"
  },
  "subject_state": "static",
  "action": "standing still in opposite full profile, the other shoulder now toward camera, arms relaxed at sides",
  "pose": "neutral standing feet together, body turned ninety degrees to the opposite side",
  "gesture": "both arms relaxed straight at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "full body shot, crown to sneaker sole visible, floor line visible, generous headroom",
  "angle": "eye-level, opposite full profile view, subject facing camera-right frame-right audience POV, head and torso rotated ninety degrees the other way, the previously hidden ear and cheek now fully toward camera, nose in clean silhouette pointing opposite direction against white",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual child wear, fabric worn laundered, class-accurate daily register",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday child hair, real-texture straight black, short crop side parting, unstyled lived-in matte finish"
}
```

### Cell 8 — Profile B · Medium → `A_andi_profileB_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": "A_andi_profileA_medium.png — same identical character and outfit, mirrored to opposite profile",
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "smooth clear child complexion, soft rounded cheeks, bright lively steady eyes, full soft natural brows, small even features, smooth even skin texture",
    "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
  },
  "character_style": {
    "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "child crew-neck cotton tee soft jersey relaxed fit muted solid slate, child elastic-waist shorts cotton twill knee-length desaturated navy",
    "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural"
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
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual child wear, fabric worn laundered, class-accurate daily register",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday child hair, real-texture straight black, short crop side parting, unstyled lived-in matte finish"
}
```

### Cell 9 — Profile B · Close-up → `A_andi_profileB_closeup.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": "A_andi_profileA_closeup.png — same identical character and outfit, mirrored to opposite profile",
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "smooth clear child complexion, soft rounded cheeks, bright lively steady eyes, full soft natural brows, small even features, smooth even skin texture",
    "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
  },
  "character_style": {
    "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "child crew-neck cotton tee soft jersey muted solid slate collar visible at neckline",
    "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural"
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
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual child wear, fabric worn laundered, class-accurate daily register",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday child hair, real-texture straight black, short crop side parting, unstyled lived-in matte finish"
}
```

---

## 4. Per-scene wardrobe (Andi in 4 scenes)
Makeup (bare child skin) + hair (short natural crop, Anissa Salazar) FIXED throughout. Garment colorway desaturated; warmth via `color_grade` only (GATE B). Two looks: a school-day look (study + ekskul, same day) and a home look (dinner + ngaji, same evening).

| Scene | Context | Wardrobe tokens | Footwear | Note |
|---|---|---|---|---|
| SEQ2-SC03 | Ruang belajar rumah 08.30, kelas daring, "seragam SD rapi" | `child school polo soft pique knit plain solid, child school shorts cotton twill desaturated` | child velcro canvas sneakers *(or barefoot/socks at home desk — GATE B)* | school-day uniform established |
| SEQ4-SC04 | Ruang ekskul sekolah 16.00, edutainment literasi anak | school-day uniform *(identical — same school day)* | child velcro canvas sneakers | at school → uniform continues |
| SEQ6-SC01 | Ruang makan 18.30, makan malam keluarga | `child home crew-neck cotton tee soft jersey muted solid slate, child elastic-waist shorts cotton twill knee-length desaturated navy` | flat house slippers | home, four mahram in frame; relaxed home look |
| SEQ6-SC02 | Ruang keluarga 18.50, ngaji ba'da Maghrib (head uncovered) | home look *(identical — same evening)* | flat house slippers | sacred zone, head uncovered per prose; same home clothes |

*Continuity:* school-day uniform spans SEQ2-SC03 → SEQ4-SC04 (same school day). Home look spans SEQ6-SC01 → SEQ6-SC02 (same evening, identical wardrobe). Head uncovered in every scene.

---

*Andi sheet v0.1 (9 t2i plate prompts, uncovered, hair in natural short crop per ref-plate standard; boy → 9 plates only, head uncovered [SEQ6-SC02 prose]; render-age 10 LOCKED (verified on front_full); bare child skin at matte plate finish; zero body-feminization tokens) · Explainer Video 2 · 2026-06-21 · cites [[07-style-reference]] · method [[00-README]]*
