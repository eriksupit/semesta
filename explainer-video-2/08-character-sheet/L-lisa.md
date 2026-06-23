---
title: Character Sheet — Lisa (20, mahasiswi + content creator) · GATE 0
tags: [explainer-video-2, character-sheet, lisa, gate-0]
status: draft
created: 2026-06-20
updated: 2026-06-20
aliases: [ev2-lisa-sheet, L-lisa]
---

# Character Sheet — LISA (20, mahasiswi + content creator) · tag L
> Method, 9-cell template, direction protocol, naming → [[00-README]]. Style tokens + anchors → [[07-style-reference]]. Scene truth → [[03-scene-detail]].

---

## 0. Notes (read first)
- **Not hijabi → 9 uncovered plates only.** Lisa's head stays uncovered in every scene; the representative-covered-plate rule (Ratna/Herman) does not apply.
- **Reference plates show hair LOOSE & down** (`lessons.md` 2026-06-20): the plate's job is to lock full hair identity — length + texture + hairline. Lisa's scene looks (half-up clip on campus, low ponytail on-camera) are **GATE B** wardrobe/hair, NOT plates.
- **Plate hair finish = matte (anti-sheen plate standard, [[00-README]]:43).** Lisa's `glossy healthy young finish` ([[07-style-reference]] §3.2) is a GATE B grade attribute; on the neutral reference plate we render matte to lock geometry without specular blowout on dark hair. Gloss returns at GATE B keyframes.
- **Render-age `19` (OPEN — verify on first plate).** Real age 20; a flat −4 → 16 risks reading too teen. Set `19`, check the first generated plate, lock or adjust then.
- **Keyword-leak guard:** `role` is kept free of any token that drags an unwanted concept (the `hijabi` leak that forced a headscarf on Ratna). Lisa's role = clean contemporary descriptors only.

---

## 1. Identity lock (FIXED — paste verbatim into Lapis 3 of every Lisa prompt)
```json
"character_identity": {
  "role": "Jakarta young urban woman, university student and content creator, contemporary bright confident presence",
  "ethnicity": "modern Jakartan features, Javanese urban descent",
  "beauty": "fresh youthful attractive, contemporary middle-class register, on-camera polished, approachable",
  "age": "woman 19 years old",
  "facial_features": "luminous youthful complexion, smooth clear skin texture, full softly defined brows, bright lively steady eyes, soft youthful cheeks, clean even jawline",
  "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 162cm frame, upright relaxed posture"
}
```
*Never changes scene-to-scene:* facial identity, full softly defined brows, bright lively eyes, soft youthful cheeks. Render-age `19` to land real 20 (model ages up); verify on first plate. Hair colour/shape fixed (uniformly dark, worn loose and down past the shoulders on all plates).

**Fixed Lapis-6 anchors (Lisa):** `makeup_artist: Judy Chin` · `hair_stylist: Camille Friend` · `costume_designer: Michael Wilkinson` (child-style tokens in [[07-style-reference]] §2 + §5).

---

## 2. Baseline style for plates (neutral reference outfit — hair LOOSE & down)
Used for ALL 9 plate cells — the consistent look the reference-lock learns. Per-scene wardrobe (§4) differs and belongs to GATE B keyframes, NOT the plates.
```json
"character_style": {
  "makeup": "medium-coverage satin foundation poreless, softly defined brows lash mascara, nude soft-matte lip, light bronzer, baked setting powder matte finish zero shine, youthful skin texture preserved",
  "wardrobe": "fitted crew-neck cotton tee soft jersey muted sage, mid-rise straight-leg denim jeans solid washed indigo desaturated",
  "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
  "footwear": "clean white low-top canvas sneakers, rubber sole"
}
```
*Plate makeup note:* on-camera-ready register per [[07-style-reference]] §3.3 but finish stays matte zero-shine (anti-sheen plate standard). No `HD makeup` / `HD setting powder` (specular trigger).

---

## 3. Plate matrix — 9 full t2i prompts (3 view × 3 shot)
Authored on the `prompt-rules-image-generation.md` 6-layer pattern + token discipline + banned-list. Each is copy-paste ready (zero placeholders).

**PLATE DEVIATIONS from prompt-rules (declared, justified — a reference plate is NOT a graded scene):**
1. `color_grade` = neutral true-to-life, NOT the Deakins deck grade — a plate must capture accurate identity for Kling reference-locking. The WARM video grade is applied later at GATE B keyframes.
2. Clean prime spherical lens, NOT Panavision anamorphic — anamorphic distorts proportion; a turnaround needs undistorted geometry.
3. `scene_depth` + `on_screen_graphic` omitted — plain solid white background, subject isolated.
4. Crew pairs scoped to identity-styling only (costume/makeup/hair); director/lighting/PD/interior dropped (plate background plain white, nothing to design).
5. `aspect_ratio` per shot type: **full body `9:16`**, **medium `2:3`**, **close-up `4:5`**.
6. Hair worn **loose & down** per §0; styling (half-up clip / low ponytail) is a GATE B layer.
All OTHER rules hold: token strings, zero negation (positive-only), garment specified affirmatively (anti-auto-batik), facial_features texture-only, identity block verbatim.

**Direction protocol ([[00-README]] §3.1):** generate Front → Profile A → **Profile B as a MIRROR of Profile A via the Profile-A plate uploaded as reference**. Label by visible cheek/ear; files use `profileA`/`profileB`, never left/right. Profile A = subject faces `camera-left`; Profile B = `camera-right`.

---

### Cell 1 — Front · Full body → `L_lisa_front_full.png`
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
    "role": "Jakarta young urban woman, university student and content creator, contemporary bright confident presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh youthful attractive, contemporary middle-class register, on-camera polished, approachable",
    "age": "woman 19 years old",
    "facial_features": "luminous youthful complexion, smooth clear skin texture, full softly defined brows, bright lively steady eyes, soft youthful cheeks, clean even jawline",
    "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 162cm frame, upright relaxed posture"
  },
  "character_style": {
    "makeup": "medium-coverage satin foundation poreless, softly defined brows lash mascara, nude soft-matte lip, light bronzer, baked setting powder matte finish zero shine, youthful skin texture preserved",
    "wardrobe": "fitted crew-neck cotton tee soft jersey muted sage, mid-rise straight-leg denim jeans solid washed indigo desaturated",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "clean white low-top canvas sneakers, rubber sole"
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
  "costume_designer": "Michael Wilkinson", "costume_style": "contemporary urban wardrobe, precise class register, modern professional polish",
  "makeup_artist": "Judy Chin", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish",
  "hair_stylist": "Camille Friend", "hair_style": "contemporary young-woman framing, smooth matte dark hair, fresh natural grooming, worn loose past the shoulders"
}
```

### Cell 2 — Front · Medium → `L_lisa_front_medium.png`
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
    "role": "Jakarta young urban woman, university student and content creator, contemporary bright confident presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh youthful attractive, contemporary middle-class register, on-camera polished, approachable",
    "age": "woman 19 years old",
    "facial_features": "luminous youthful complexion, smooth clear skin texture, full softly defined brows, bright lively steady eyes, soft youthful cheeks, clean even jawline",
    "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 162cm frame, upright relaxed posture"
  },
  "character_style": {
    "makeup": "medium-coverage satin foundation poreless, softly defined brows lash mascara, nude soft-matte lip, light bronzer, baked setting powder matte finish zero shine, youthful skin texture preserved",
    "wardrobe": "fitted crew-neck cotton tee soft jersey muted sage, mid-rise straight-leg denim jeans solid washed indigo desaturated",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "clean white low-top canvas sneakers, rubber sole"
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
  "costume_designer": "Michael Wilkinson", "costume_style": "contemporary urban wardrobe, precise class register, modern professional polish",
  "makeup_artist": "Judy Chin", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish",
  "hair_stylist": "Camille Friend", "hair_style": "contemporary young-woman framing, smooth matte dark hair, fresh natural grooming, worn loose past the shoulders"
}
```

### Cell 3 — Front · Close-up → `L_lisa_front_closeup.png`
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
    "role": "Jakarta young urban woman, university student and content creator, contemporary bright confident presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh youthful attractive, contemporary middle-class register, on-camera polished, approachable",
    "age": "woman 19 years old",
    "facial_features": "luminous youthful complexion, smooth clear skin texture, full softly defined brows, bright lively steady eyes, soft youthful cheeks, clean even jawline",
    "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 162cm frame, upright relaxed posture"
  },
  "character_style": {
    "makeup": "medium-coverage satin foundation poreless, softly defined brows lash mascara, nude soft-matte lip, light bronzer, baked setting powder matte finish zero shine, youthful skin texture preserved",
    "wardrobe": "fitted crew-neck cotton tee soft jersey muted sage collar visible at neckline",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural"
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
  "costume_designer": "Michael Wilkinson", "costume_style": "contemporary urban wardrobe, precise class register, modern professional polish",
  "makeup_artist": "Judy Chin", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish",
  "hair_stylist": "Camille Friend", "hair_style": "contemporary young-woman framing, smooth matte dark hair, fresh natural grooming, worn loose past the shoulders"
}
```

### Cell 4 — Profile A · Full body → `L_lisa_profileA_full.png`
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
    "role": "Jakarta young urban woman, university student and content creator, contemporary bright confident presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh youthful attractive, contemporary middle-class register, on-camera polished, approachable",
    "age": "woman 19 years old",
    "facial_features": "luminous youthful complexion, smooth clear skin texture, full softly defined brows, bright lively steady eyes, soft youthful cheeks, clean even jawline",
    "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 162cm frame, upright relaxed posture"
  },
  "character_style": {
    "makeup": "medium-coverage satin foundation poreless, softly defined brows lash mascara, nude soft-matte lip, light bronzer, baked setting powder matte finish zero shine, youthful skin texture preserved",
    "wardrobe": "fitted crew-neck cotton tee soft jersey muted sage, mid-rise straight-leg denim jeans solid washed indigo desaturated",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "clean white low-top canvas sneakers, rubber sole"
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
  "costume_designer": "Michael Wilkinson", "costume_style": "contemporary urban wardrobe, precise class register, modern professional polish",
  "makeup_artist": "Judy Chin", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish",
  "hair_stylist": "Camille Friend", "hair_style": "contemporary young-woman framing, smooth matte dark hair, fresh natural grooming, worn loose past the shoulders"
}
```

### Cell 5 — Profile A · Medium → `L_lisa_profileA_medium.png`
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
    "role": "Jakarta young urban woman, university student and content creator, contemporary bright confident presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh youthful attractive, contemporary middle-class register, on-camera polished, approachable",
    "age": "woman 19 years old",
    "facial_features": "luminous youthful complexion, smooth clear skin texture, full softly defined brows, bright lively steady eyes, soft youthful cheeks, clean even jawline",
    "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 162cm frame, upright relaxed posture"
  },
  "character_style": {
    "makeup": "medium-coverage satin foundation poreless, softly defined brows lash mascara, nude soft-matte lip, light bronzer, baked setting powder matte finish zero shine, youthful skin texture preserved",
    "wardrobe": "fitted crew-neck cotton tee soft jersey muted sage, mid-rise straight-leg denim jeans solid washed indigo desaturated",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural"
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
  "costume_designer": "Michael Wilkinson", "costume_style": "contemporary urban wardrobe, precise class register, modern professional polish",
  "makeup_artist": "Judy Chin", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish",
  "hair_stylist": "Camille Friend", "hair_style": "contemporary young-woman framing, smooth matte dark hair, fresh natural grooming, worn loose past the shoulders"
}
```

### Cell 6 — Profile A · Close-up → `L_lisa_profileA_closeup.png`
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
    "role": "Jakarta young urban woman, university student and content creator, contemporary bright confident presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh youthful attractive, contemporary middle-class register, on-camera polished, approachable",
    "age": "woman 19 years old",
    "facial_features": "luminous youthful complexion, smooth clear skin texture, full softly defined brows, bright lively steady eyes, soft youthful cheeks, clean even jawline",
    "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 162cm frame, upright relaxed posture"
  },
  "character_style": {
    "makeup": "medium-coverage satin foundation poreless, softly defined brows lash mascara, nude soft-matte lip, light bronzer, baked setting powder matte finish zero shine, youthful skin texture preserved",
    "wardrobe": "fitted crew-neck cotton tee soft jersey muted sage collar visible at neckline",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural"
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
  "costume_designer": "Michael Wilkinson", "costume_style": "contemporary urban wardrobe, precise class register, modern professional polish",
  "makeup_artist": "Judy Chin", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish",
  "hair_stylist": "Camille Friend", "hair_style": "contemporary young-woman framing, smooth matte dark hair, fresh natural grooming, worn loose past the shoulders"
}
```

### Cells 7–9 — Profile B (opposite side)
**Generate each as a MIRROR of the matching Profile-A plate: upload `L_lisa_profileA_<shot>.png` as a reference image, instruct "same identical character and outfit, flip to the opposite full profile — the cheek hidden in the reference now faces camera, nose silhouette points the opposite direction."** Do NOT rely on a text left/right token. The JSON below describes the target by anatomy; the reference image enforces the mirror.

### Cell 7 — Profile B · Full body → `L_lisa_profileB_full.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": "L_lisa_profileA_full.png — same identical character and outfit, mirrored to opposite profile",
  "character_identity": {
    "role": "Jakarta young urban woman, university student and content creator, contemporary bright confident presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh youthful attractive, contemporary middle-class register, on-camera polished, approachable",
    "age": "woman 19 years old",
    "facial_features": "luminous youthful complexion, smooth clear skin texture, full softly defined brows, bright lively steady eyes, soft youthful cheeks, clean even jawline",
    "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 162cm frame, upright relaxed posture"
  },
  "character_style": {
    "makeup": "medium-coverage satin foundation poreless, softly defined brows lash mascara, nude soft-matte lip, light bronzer, baked setting powder matte finish zero shine, youthful skin texture preserved",
    "wardrobe": "fitted crew-neck cotton tee soft jersey muted sage, mid-rise straight-leg denim jeans solid washed indigo desaturated",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "clean white low-top canvas sneakers, rubber sole"
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
  "costume_designer": "Michael Wilkinson", "costume_style": "contemporary urban wardrobe, precise class register, modern professional polish",
  "makeup_artist": "Judy Chin", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish",
  "hair_stylist": "Camille Friend", "hair_style": "contemporary young-woman framing, smooth matte dark hair, fresh natural grooming, worn loose past the shoulders"
}
```

### Cell 8 — Profile B · Medium → `L_lisa_profileB_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": "L_lisa_profileA_medium.png — same identical character and outfit, mirrored to opposite profile",
  "character_identity": {
    "role": "Jakarta young urban woman, university student and content creator, contemporary bright confident presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh youthful attractive, contemporary middle-class register, on-camera polished, approachable",
    "age": "woman 19 years old",
    "facial_features": "luminous youthful complexion, smooth clear skin texture, full softly defined brows, bright lively steady eyes, soft youthful cheeks, clean even jawline",
    "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 162cm frame, upright relaxed posture"
  },
  "character_style": {
    "makeup": "medium-coverage satin foundation poreless, softly defined brows lash mascara, nude soft-matte lip, light bronzer, baked setting powder matte finish zero shine, youthful skin texture preserved",
    "wardrobe": "fitted crew-neck cotton tee soft jersey muted sage, mid-rise straight-leg denim jeans solid washed indigo desaturated",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural"
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
  "costume_designer": "Michael Wilkinson", "costume_style": "contemporary urban wardrobe, precise class register, modern professional polish",
  "makeup_artist": "Judy Chin", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish",
  "hair_stylist": "Camille Friend", "hair_style": "contemporary young-woman framing, smooth matte dark hair, fresh natural grooming, worn loose past the shoulders"
}
```

### Cell 9 — Profile B · Close-up → `L_lisa_profileB_closeup.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": "L_lisa_profileA_closeup.png — same identical character and outfit, mirrored to opposite profile",
  "character_identity": {
    "role": "Jakarta young urban woman, university student and content creator, contemporary bright confident presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh youthful attractive, contemporary middle-class register, on-camera polished, approachable",
    "age": "woman 19 years old",
    "facial_features": "luminous youthful complexion, smooth clear skin texture, full softly defined brows, bright lively steady eyes, soft youthful cheeks, clean even jawline",
    "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 162cm frame, upright relaxed posture"
  },
  "character_style": {
    "makeup": "medium-coverage satin foundation poreless, softly defined brows lash mascara, nude soft-matte lip, light bronzer, baked setting powder matte finish zero shine, youthful skin texture preserved",
    "wardrobe": "fitted crew-neck cotton tee soft jersey muted sage collar visible at neckline",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural"
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
  "costume_designer": "Michael Wilkinson", "costume_style": "contemporary urban wardrobe, precise class register, modern professional polish",
  "makeup_artist": "Judy Chin", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish",
  "hair_stylist": "Camille Friend", "hair_style": "contemporary young-woman framing, smooth matte dark hair, fresh natural grooming, worn loose past the shoulders"
}
```

---

## 4. Per-scene wardrobe (Lisa in 6 scenes)
Makeup (Judy Chin on-camera-ready) FIXED throughout. **Hair worn loose on all plates; per-scene styling below is a GATE B hair layer (half-up clip / low ponytail / loose), NOT a plate.** Single contemporary day-outfit across the public day (morning commute → evening transit bookend); home dinner relaxes it. Garment colorway desaturated; warmth via `color_grade` only (GATE B).

| Scene | Context | Wardrobe tokens | Footwear | Hair look (GATE B) | Note |
|---|---|---|---|---|---|
| SEQ2-SC01 | Berangkat pagi, gerbang kompleks, ransel, sapa Pak Darto | `fitted crew-neck cotton tee soft jersey muted sage, mid-rise straight-leg denim jeans washed indigo, light canvas backpack` | white low-top canvas sneakers | half-up clip | day base outfit established |
| SEQ2-SC04 | Kafe 10.00, kuliah daring + rekam klip konten | day base *(identical — same day, backpack set aside)* | same | low ponytail (on-camera) | records to camera → tidier creator hair |
| SEQ3-SC04 | Coworking 14.00, Lisa MENGAJAR kreator | day base + `light unstructured overshirt soft cotton muted, worn open` | same | low ponytail (on-camera) | teaching/presenting register; light layer adds polish |
| SEQ4-SC02 | Komunitas kreator 16.30, Lisa jadi murid | day base *(overshirt removed)* | same | half-up clip | attendee, relaxed again |
| SEQ5-SC01 | Terminal TransJakarta 17.30, transit pulang | day base *(identical — bookend of SEQ2-SC01 morning, lock token string)* | same | half-up clip | same outfit closes the commute bookend |
| SEQ6-SC01 | Makan malam keluarga 18.30, di rumah | `comfortable home crew-neck tee soft muted, relaxed lounge trousers cotton desaturated` | flat house slippers | hair loose down | home, four mahram in frame; relaxed home look |

*Continuity:* SEQ2-SC01 = day base established → SEQ2-SC04 / SEQ4-SC02 / SEQ5-SC01 reuse it (SEQ5 is the explicit evening bookend of the SEQ2 morning, lock token string identical). SEQ3-SC04 adds an open overshirt for the teaching beat. SEQ6-SC01 changes to a home look at dinner. Backpack appears only in commute scenes (SEQ2-SC01, SEQ5-SC01).

---

*Lisa sheet v0.1 (9 t2i plate prompts, uncovered baseline, hair worn LOOSE & down past shoulders per ref-plate standard; not hijabi → 9 uncovered plates only; render-age 19 OPEN — verify on first plate; on-camera-ready makeup at matte plate finish) · Explainer Video 2 · 2026-06-20 · cites [[07-style-reference]] · method [[00-README]]*
