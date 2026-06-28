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
>
> **PLATES STATUS: 12/12 generated + accepted 2026-06-26** (age-token 10 KEPT, DAG-chained; CU Front master = blend of parent faces H+R front_closeup → reads ~10, NO age-up — pilot risk falsified; incl. rear; identity consistent across angles; on disk `character-images/A_andi/`).

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
Used for ALL 12 plate cells — the consistent look the reference-lock learns. Per-scene wardrobe (§4) differs and belongs to GATE B keyframes, NOT the plates.
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

## 3. Plate matrix — 12 full t2i prompts (4 view × 3 shot: front · profileA · profileB · rear)
Authored on the `prompt-rules-image-generation.md` 6-layer pattern + token discipline + banned-list. Each is copy-paste ready (zero placeholders).

> **🔗 IDENTITY-PROPAGATION DAG + GENERATION ORDER (BINDING — Erik, 2026-06-26).** All 12 plates = FULL prompt each (never edit-in-place). **CU Front = the child's face derived from BOTH parents** (attach `H_herman_front_closeup.png` + `R_ratna_front_closeup.png` — generate the parents' CU Front FIRST). Every later plate attaches the child's own earlier-accepted plates. **Generate in this exact order:**
>
> | # | Plate | File | Attach (reference images) |
> |---|-------|------|----------------------------|
> | 1 | CU Front | `A_andi_front_closeup.png` | H_herman_front_closeup + R_ratna_front_closeup (PARENTS · from-scratch face blend · MASTER) |
> | 2 | CU ProfileA | `A_andi_profileA_closeup.png` | front_closeup |
> | 3 | CU ProfileB | `A_andi_profileB_closeup.png` | front_closeup + profileA_closeup |
> | 4 | CU Rear | `A_andi_rear_closeup.png` | front_closeup + profileA_closeup + profileB_closeup |
> | 5 | Medium Front | `A_andi_front_medium.png` | front_closeup |
> | 6 | Medium ProfileA | `A_andi_profileA_medium.png` | front_medium + profileA_closeup |
> | 7 | Medium ProfileB | `A_andi_profileB_medium.png` | profileA_medium + profileB_closeup |
> | 8 | Medium Rear | `A_andi_rear_medium.png` | front_medium + rear_closeup |
> | 9 | FB Front | `A_andi_front_full.png` | front_medium |
> | 10 | FB ProfileA | `A_andi_profileA_full.png` | front_full + profileA_medium |
> | 11 | FB ProfileB | `A_andi_profileB_full.png` | profileA_full + profileB_medium |
> | 12 | FB Rear | `A_andi_rear_full.png` | front_full + rear_closeup |
> 
> FB-profile attaches the **medium** profile (closer framing than closeup). Child age token kept as-is (verify on the CU Front pilot — two adult refs may age the child up; Andi is the higher-risk pilot). Same DAG as `H-herman.md`/`R-ratna.md`.


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

## Row 1 — Close-up plates (4:5)

### Cell 1 — Front · Close-up → `A_andi_front_closeup.png`
**Generate order #1 · Attach: H_herman_front_closeup + R_ratna_front_closeup (PARENTS) · MASTER**
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": ["H_herman_front_closeup.png — the father, locked face for familial resemblance", "R_ratna_front_closeup.png — the mother, locked face for familial resemblance, blend both parents into this child face"],
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "mix H_herman_front_closeup.png + R_ratna_front_closeup.png",
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

### Cell 2 — Profile A · Close-up → `A_andi_profileA_closeup.png`
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
  "reference_image": ["A_andi_front_closeup.png — same identical child, locked face identity to rotate into this profile"],
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "A_andi_front_closeup.png",
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

### Cell 3 — Profile B · Close-up → `A_andi_profileB_closeup.png`
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
  "reference_image": ["A_andi_front_closeup.png — same identical child, locked face", "A_andi_profileA_closeup.png — the profileA side to mirror to the opposite profile"],
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "A_andi_front_closeup.png",
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

### Cell 4 — Rear · Close-up → `A_andi_rear_closeup.png`
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
  "reference_image": ["A_andi_front_closeup.png — face and hairline", "A_andi_profileA_closeup.png — the left head shape", "A_andi_profileB_closeup.png — the right head shape; rotate to show the back of the head, face away"],
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "A_andi_front_closeup.png",
    "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
  },
  "character_style": {
    "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "child crew-neck cotton tee soft jersey relaxed fit muted solid slate, child elastic-waist shorts cotton twill knee-length desaturated navy",
    "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural"
  },
  "subject_state": "static",
  "action": "back of the head and top of shoulders still, face away from the lens",
  "pose": "neutral standing, back squared to camera, body facing fully away",
  "gesture": "both arms relaxed straight at sides",
  "expression": "face fully turned away from camera, hidden from the lens, only the back of the head and the short dark crop shown",
  "framing": "CU close-up from behind, the back of the head fills the frame, nape and hairline and top of shoulders",
  "angle": "eye-level straight-on from directly behind, rear view, occiput and nape toward the lens, face away from the lens",
  "camera": "100mm portrait prime spherical, soft background separation",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "4:5",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual child wear, fabric worn laundered, class-accurate daily register",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday child hair, real-texture straight black, short crop side parting, unstyled lived-in matte finish"
}
```

## Row 2 — Medium plates (2:3)

### Cell 5 — Front · Medium → `A_andi_front_medium.png`
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
  "reference_image": ["A_andi_front_closeup.png — same identical child, locked face identity"],
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "A_andi_front_closeup.png",
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

### Cell 6 — Profile A · Medium → `A_andi_profileA_medium.png`
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
  "reference_image": ["A_andi_front_medium.png — medium framing and build anchor", "A_andi_profileA_closeup.png — the profileA face identity to carry"],
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "A_andi_front_medium.png",
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

### Cell 7 — Profile B · Medium → `A_andi_profileB_medium.png`
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
  "reference_image": ["A_andi_profileA_medium.png — medium framing, mirror to the opposite profile", "A_andi_profileB_closeup.png — the profileB face identity to carry"],
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "A_andi_profileA_medium.png",
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

### Cell 8 — Rear · Medium → `A_andi_rear_medium.png`
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
  "reference_image": ["A_andi_front_medium.png — medium framing and build", "A_andi_rear_closeup.png — the locked back-of-head, face away"],
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "A_andi_front_medium.png",
    "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
  },
  "character_style": {
    "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "child crew-neck cotton tee soft jersey relaxed fit muted solid slate, child elastic-waist shorts cotton twill knee-length desaturated navy",
    "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural"
  },
  "subject_state": "static",
  "action": "standing still seen from directly behind, torso squared away from camera, arms relaxed at sides",
  "pose": "neutral standing, back squared to camera, body facing fully away",
  "gesture": "both arms relaxed straight at sides",
  "expression": "face fully turned away from camera, hidden from the lens, only the back of the head and the short dark crop shown",
  "framing": "MS medium shot from behind, waist up, back of the head and shoulders centered",
  "angle": "eye-level straight-on from directly behind, rear view, back of the head and shoulders squared to camera, face away from the lens",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual child wear, fabric worn laundered, class-accurate daily register",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday child hair, real-texture straight black, short crop side parting, unstyled lived-in matte finish"
}
```

## Row 3 — Full-body plates (9:16)

### Cell 9 — Front · Full body → `A_andi_front_full.png`
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
  "reference_image": ["A_andi_front_medium.png — same identical child, framing and build and face anchor"],
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "A_andi_front_medium.png",
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

### Cell 10 — Profile A · Full body → `A_andi_profileA_full.png`
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
  "reference_image": ["A_andi_front_full.png — full-body build and framing anchor", "A_andi_profileA_medium.png — the profileA identity at medium"],
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "A_andi_front_full.png",
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

### Cell 11 — Profile B · Full body → `A_andi_profileB_full.png`
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
  "reference_image": ["A_andi_profileA_full.png — full-body framing, mirror to the opposite profile", "A_andi_profileB_medium.png — the profileB identity at medium"],
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "A_andi_front_full.png",
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

### Cell 12 — Rear · Full body → `A_andi_rear_full.png`
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
  "reference_image": ["A_andi_front_full.png — full-body build and framing", "A_andi_rear_medium.png"],
  "character_identity": {
    "role": "Jakarta primary-school boy, online-learning student, bright cheerful everyday presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "healthy cheerful child, contemporary middle-class register, natural everyday grooming, approachable",
    "age": "boy 10 years old",
    "facial_features": "A_andi_front_full.png",
    "body_features": "slim healthy child build, age-appropriate proportions, 138cm frame, upright relaxed natural posture"
  },
  "character_style": {
    "makeup": "bare healthy child skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "child crew-neck cotton tee soft jersey relaxed fit muted solid slate, child elastic-waist shorts cotton twill knee-length desaturated navy",
    "hair": "child short natural crop, side parting, uniformly dark even tone throughout, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "child velcro canvas sneakers, white rubber sole, plain"
  },
  "subject_state": "static",
  "action": "standing still seen from directly behind, back toward camera, arms relaxed at sides",
  "pose": "neutral standing, back squared to camera, body facing fully away",
  "gesture": "both arms relaxed straight at sides",
  "expression": "face fully turned away from camera, hidden from the lens, only the back of the head and the short dark crop shown",
  "framing": "full body shot from behind, crown to sneaker sole visible, floor line visible, generous headroom above crown",
  "angle": "eye-level straight-on from directly behind, rear view, back of the head and shoulders and back squared to camera, face away from the lens",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual child wear, fabric worn laundered, class-accurate daily register",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday child hair, real-texture straight black, short crop side parting, unstyled lived-in matte finish"
}
```

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

*Andi sheet v0.2 (12 t2i plate prompts, DAG-ordered closeup→medium→fullbody incl. rear; CU Front master = blend of parent faces H_herman_front_closeup + R_ratna_front_closeup; reference_image in body+header+master-table; FB-profile attaches medium-profile; render-age 10 KEPT — verify on CU Front pilot, two adult refs may age up, Andi=higher-risk pilot) · Explainer Video 2 · 2026-06-26 · cites [[07-style-reference]] · method [[00-README]]*
