---
title: Character Sheet — Ratna (45, hijabi) · GATE 0
tags: [explainer-video-2, character-sheet, ratna, gate-0]
status: draft
created: 2026-06-20
updated: 2026-06-20
aliases: [ev2-ratna-sheet, R-ratna]
---

# Character Sheet — RATNA (45, hijabi) · tag R
> Method, 9-cell template, direction protocol, naming → [[00-README]]. Style tokens + anchors → [[07-style-reference]]. Scene truth → [[03-scene-detail]].

---

## 0. Modesty axis (Ratna-specific — READ FIRST, governs §4 wardrobe)
Ratna's head-covering is **not** a fixed look; it is governed by **non-mahram exposure**, not by indoor/outdoor. Mahram present in this film = Herman (husband), Andi (son), Lisa (daughter). Hair may be uncovered ONLY when everyone present is mahram or female. The moment a non-mahram man can see her — **physically OR through a camera/broadcast** — hijab is worn. Three states result:
1. **Uncovered (hair visible):** family/mahram-only scenes — SEQ1-SC01 (asleep in the private bedroom, husband-only present), SEQ2-SC03, SEQ6-SC01, SEQ6-SC02.
2. **Hijab covered:** public exposure, including two **at-home** scenes that broadcast/video to non-mahram — SEQ3-SC01 (live-selling to public), SEQ3-SC02 (bank video call), plus outdoors SEQ4-SC03, SEQ5-SC02.
3. **Mukena (prayer garment):** SEQ1-SC02 sholat subuh.

**Plate consequence (general principle — applies to ALL characters):** every character's baseline plates are shot **uncovered (hair visible)** — a plate's job is to lock face + hair + proportion at maximum information. A character who covers their head in some scenes (Ratna's hijab; Herman's peci in sholat) ALSO gets a **few representative covered plates** as reference anchors, because the covering changes head/face framing + silhouette and the locking set needs a covered-head anchor for those scenes. For Ratna that is **9 uncovered (§3) + 3 hijab (§3.A) = 12 plates**.

**Keyword-leak guard (firm — `lessons.md`).** The word `hijabi` / any head-covering trigger is BANNED from `character_identity.role` on the **uncovered** plates: `character_identity` is read first by the model and a covering word there forces a headscarf even when the wardrobe field carries none. Role token on uncovered plates = `modest mature Muslim woman` (zero covering trigger). The hijab is introduced ONLY where a hijab garment token is explicitly present (§3.A + GATE B hijab scenes).

Supported by [[07-style-reference]]:99 (`minimal front hairline visible under loose hijab`) + Camille Friend hair anchor already assigned to Ratna.

---

## 1. Identity lock (FIXED — paste verbatim into Lapis 3 of every Ratna prompt)
```json
"character_identity": {
  "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
  "ethnicity": "modern Jakartan features, Javanese urban descent",
  "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
  "age": "woman 41 years old",
  "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
  "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
}
```
*Never changes scene-to-scene:* facial identity, full soft brows, calm warm eyes, gentle full cheeks. Render-age `41` to land real 45 (model ages up). Hair colour/shape is fixed too (uniformly dark, worn loose and down past the shoulders on uncovered plates) but is **covered** in hijab/mukena scenes.

**Fixed Lapis-6 anchors (Ratna):** `makeup_artist: Eryn Krueger Mekash` · `hair_stylist: Camille Friend` · `costume_designer: Deborah Hopper` (child-style tokens in [[07-style-reference]] §2 + §5).

---

## 2. Baseline style for plates (neutral reference outfit, UNCOVERED — hair visible)
Used for ALL 9 plate cells — the consistent look the reference-lock learns. Per-scene wardrobe (§4) differs (hijab/mukena/uncovered) and belongs to GATE B keyframes, NOT the plates.
```json
"character_style": {
  "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
  "wardrobe": "long-sleeve tunic blouse relaxed modest cut mid-thigh length plain weave muted slate-blue, wide-leg modest trousers cotton twill full-length solid charcoal",
  "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
  "footwear": "flat slip-on mules matte leather minimal muted"
}
```

---

## 3. Plate matrix — 9 full t2i prompts (3 view × 3 shot)
Authored on the `prompt-rules-image-generation.md` 6-layer pattern + token discipline + banned-list. Each is copy-paste ready (zero placeholders, per vault standard).

**PLATE DEVIATIONS from prompt-rules (declared, justified — a reference plate is NOT a graded scene):**
1. `color_grade` = neutral true-to-life, NOT the Deakins deck grade — a plate must capture accurate identity for Kling reference-locking. The WARM video grade is applied later at GATE B keyframes.
2. Clean prime spherical lens, NOT Panavision anamorphic — anamorphic distorts proportion; a turnaround needs undistorted geometry.
3. `scene_depth` + `on_screen_graphic` omitted — plain solid white background, subject isolated.
4. Crew pairs scoped to identity-styling only (costume/makeup/hair); director/lighting/PD/interior dropped (plate background plain white, nothing to design).
5. `aspect_ratio` per shot type: **full body `9:16`**, **medium `2:3`**, **close-up `4:5`**.
6. Plates shot **uncovered** (hair visible) per §0; hijab/mukena are GATE B wardrobe layers.
All OTHER rules hold: token strings, zero negation (positive-only), garment specified affirmatively (anti-auto-batik), facial_features texture-only, identity block verbatim.

**Direction protocol ([[00-README]] §3.1):** generate Front → Profile A → **Profile B as a MIRROR of Profile A via the Profile-A plate uploaded as reference**. Label by visible cheek/ear; files use `profileA`/`profileB`, never left/right. Profile A = subject faces `camera-left`; Profile B = `camera-right`.

---

### Cell 1 — Front · Full body → `R_ratna_front_full.png`
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
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
    "wardrobe": "long-sleeve tunic blouse relaxed modest cut mid-thigh length plain weave muted slate-blue, wide-leg modest trousers cotton twill full-length solid charcoal",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "flat slip-on mules matte leather minimal muted"
  },
  "subject_state": "static",
  "action": "standing still upright for reference, weight even both feet, arms relaxed straight at sides",
  "pose": "neutral standing feet shoulder-width, shoulders squared to camera",
  "gesture": "both arms relaxed straight at sides, hands open natural",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "full body shot, crown to mule sole visible, floor line visible, generous headroom above crown",
  "angle": "eye-level straight-on, front view, subject squared facing camera, both ears symmetric, nose centered",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual modest wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Camille Friend", "hair_style": "culturally authentic framing, smooth matte dark hair, dignified mature grooming, worn loose past the shoulders"
}
```

### Cell 2 — Front · Medium → `R_ratna_front_medium.png`
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
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
    "wardrobe": "long-sleeve tunic blouse relaxed modest cut plain weave muted slate-blue, wide-leg modest trousers cotton twill solid charcoal",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "flat slip-on mules matte leather minimal muted"
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
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual modest wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Camille Friend", "hair_style": "culturally authentic framing, smooth matte dark hair, dignified mature grooming, worn loose past the shoulders"
}
```

### Cell 3 — Front · Close-up → `R_ratna_front_closeup.png`
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
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
    "wardrobe": "long-sleeve tunic blouse soft neckline, muted slate-blue collar visible at neckline",
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
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual modest wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Camille Friend", "hair_style": "culturally authentic framing, smooth matte dark hair, dignified mature grooming, worn loose past the shoulders"
}
```

### Cell 4 — Profile A · Full body → `R_ratna_profileA_full.png`
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
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
    "wardrobe": "long-sleeve tunic blouse relaxed modest cut mid-thigh length plain weave muted slate-blue, wide-leg modest trousers cotton twill full-length solid charcoal",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "flat slip-on mules matte leather minimal muted"
  },
  "subject_state": "static",
  "action": "standing still rotated to full profile, near shoulder toward camera, arms relaxed at sides",
  "pose": "neutral standing feet together, body turned ninety degrees sideways",
  "gesture": "both arms relaxed straight at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "full body shot, crown to mule sole visible, floor line visible, generous headroom",
  "angle": "eye-level, full profile view, subject facing camera-left frame-left audience POV, head and torso rotated ninety degrees sideways, single ear visible, nose in clean silhouette against white background, near cheek fully toward camera",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual modest wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Camille Friend", "hair_style": "culturally authentic framing, smooth matte dark hair, dignified mature grooming, worn loose past the shoulders"
}
```

### Cell 5 — Profile A · Medium → `R_ratna_profileA_medium.png`
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
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
    "wardrobe": "long-sleeve tunic blouse relaxed modest cut plain weave muted slate-blue, wide-leg modest trousers cotton twill solid charcoal",
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
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual modest wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Camille Friend", "hair_style": "culturally authentic framing, smooth matte dark hair, dignified mature grooming, worn loose past the shoulders"
}
```

### Cell 6 — Profile A · Close-up → `R_ratna_profileA_closeup.png`
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
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
    "wardrobe": "long-sleeve tunic blouse soft neckline, muted slate-blue collar visible at neckline",
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
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual modest wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Camille Friend", "hair_style": "culturally authentic framing, smooth matte dark hair, dignified mature grooming, worn loose past the shoulders"
}
```

### Cells 7–9 — Profile B (opposite side)
**Generate each as a MIRROR of the matching Profile-A plate: upload `R_ratna_profileA_<shot>.png` as a reference image, instruct "same identical character and outfit, flip to the opposite full profile — the cheek hidden in the reference now faces camera, nose silhouette points the opposite direction."** Do NOT rely on a text left/right token. The JSON below describes the target by anatomy; the reference image enforces the mirror.

### Cell 7 — Profile B · Full body → `R_ratna_profileB_full.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": "R_ratna_profileA_full.png — same identical character and outfit, mirrored to opposite profile",
  "character_identity": {
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
    "wardrobe": "long-sleeve tunic blouse relaxed modest cut mid-thigh length plain weave muted slate-blue, wide-leg modest trousers cotton twill full-length solid charcoal",
    "hair": "long uniformly dark hair even tone throughout, center part, hair worn loose and down, falling straight past the shoulders, dry matte hair, velvety matte strands, chalky matte finish, neatly combed natural",
    "footwear": "flat slip-on mules matte leather minimal muted"
  },
  "subject_state": "static",
  "action": "standing still in opposite full profile, the other shoulder now toward camera, arms relaxed at sides",
  "pose": "neutral standing feet together, body turned ninety degrees to the opposite side",
  "gesture": "both arms relaxed straight at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "full body shot, crown to mule sole visible, floor line visible, generous headroom",
  "angle": "eye-level, opposite full profile view, subject facing camera-right frame-right audience POV, head and torso rotated ninety degrees the other way, the previously hidden ear and cheek now fully toward camera, nose in clean silhouette pointing opposite direction against white",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual modest wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Camille Friend", "hair_style": "culturally authentic framing, smooth matte dark hair, dignified mature grooming, worn loose past the shoulders"
}
```

### Cell 8 — Profile B · Medium → `R_ratna_profileB_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": "R_ratna_profileA_medium.png — same identical character and outfit, mirrored to opposite profile",
  "character_identity": {
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
    "wardrobe": "long-sleeve tunic blouse relaxed modest cut plain weave muted slate-blue, wide-leg modest trousers cotton twill solid charcoal",
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
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual modest wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Camille Friend", "hair_style": "culturally authentic framing, smooth matte dark hair, dignified mature grooming, worn loose past the shoulders"
}
```

### Cell 9 — Profile B · Close-up → `R_ratna_profileB_closeup.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "reference_image": "R_ratna_profileA_closeup.png — same identical character and outfit, mirrored to opposite profile",
  "character_identity": {
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
    "wardrobe": "long-sleeve tunic blouse soft neckline, muted slate-blue collar visible at neckline",
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
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual modest wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Camille Friend", "hair_style": "culturally authentic framing, smooth matte dark hair, dignified mature grooming, worn loose past the shoulders"
}
```

---

## 3.A Supplementary hijab reference plates (3 representative angles)
Covered-head anchors for Ratna's 4 hijab scenes (SEQ3-SC01/02, SEQ4-SC03, SEQ5-SC02) + mukena scene reference. NOT a full turnaround — the uncovered §3 plates already lock the face; these add the hijab drape + covered-head framing the hijab scenes need. Everyday `square voile hijab` (the SEQ4/SEQ5 standard); jersey-snug variant (SEQ3 cooking) is a minor GATE-B adjustment. Here a hijab garment token IS present, so the covered look is rendered by the wardrobe, not by a role trigger.

### Cell HA — Hijab · Front · Medium → `R_ratna_hijab_front_medium.png`
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
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
    "wardrobe": "square voile hijab neatly pinned, opaque matte weave, draped over shoulders, muted dusty-teal, long-sleeve tunic blouse relaxed modest cut muted slate-blue beneath",
    "hair": "hair fully covered by neatly pinned voile hijab, smooth covered crown, hairline fully concealed, matte fabric drape framing the face",
    "footwear": "flat slip-on mules matte leather minimal muted"
  },
  "subject_state": "static",
  "action": "standing still, torso squared to camera, arms relaxed at sides",
  "pose": "upright relaxed, shoulders squared level",
  "gesture": "shoulders relaxed level, arms at sides out of frame",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "MS medium shot, waist up, subject centered, hijab drape over shoulders visible",
  "angle": "eye-level straight-on, front view, both ears area covered by hijab, nose centered, full face oval framed by headscarf",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and fabric rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic modest wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Camille Friend", "hair_style": "hijab-framed hairline, smooth covered crown, dignified modest grooming"
}
```

### Cell HB — Hijab · Front · Close-up → `R_ratna_hijab_front_closeup.png`
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
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
    "wardrobe": "square voile hijab neatly pinned, opaque matte weave, muted dusty-teal, framing the face at the hairline and jaw",
    "hair": "hair fully covered by neatly pinned voile hijab, smooth covered crown, hairline fully concealed, matte fabric drape framing the face"
  },
  "subject_state": "static",
  "action": "head and shoulders still, facing lens",
  "pose": "head level, shoulders squared",
  "gesture": "shoulders relaxed level",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens, both eyes open even",
  "framing": "CU close-up, face fills frame, head and top of shoulders, hijab framing the face oval",
  "angle": "eye-level straight-on, front view, both eyes visible symmetric, nose centered, hijab edge along hairline and jaw",
  "camera": "100mm portrait prime spherical, soft background separation",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and fabric rendering, white seamless evenly lit",
  "aspect_ratio": "4:5",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic modest wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Camille Friend", "hair_style": "hijab-framed hairline, smooth covered crown, dignified modest grooming"
}
```

### Cell HC — Hijab · Profile A · Medium → `R_ratna_hijab_profileA_medium.png`
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
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style": {
    "makeup": "light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine, fine mature texture preserved",
    "wardrobe": "square voile hijab neatly pinned, opaque matte weave, draped over shoulders, muted dusty-teal, long-sleeve tunic blouse muted slate-blue beneath",
    "hair": "hair fully covered by neatly pinned voile hijab, smooth covered crown, hairline fully concealed, matte fabric drape over the nape and shoulder"
  },
  "subject_state": "static",
  "action": "standing still in full profile, torso turned ninety degrees, arms relaxed",
  "pose": "upright relaxed, body sideways to camera",
  "gesture": "arms relaxed at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "MS medium shot, waist up, profile, hijab drape over nape and shoulder visible",
  "angle": "eye-level, full profile view, subject facing camera-left frame-left audience POV, head rotated ninety degrees sideways, near cheek toward camera, hijab edge along the face profile, nose in clean silhouette against white",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and fabric rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic modest wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Camille Friend", "hair_style": "hijab-framed hairline, smooth covered crown, dignified modest grooming"
}
```

---

## 4. Per-scene wardrobe (Ratna in 8 scenes) — modesty-state per §0
Makeup (Eryn Krueger Mekash natural hijabi) FIXED throughout. **Head-covering state varies by non-mahram exposure (§0), NOT by indoor/outdoor.** Hair anchor Camille Friend renders visible hair only in uncovered scenes; hijab/mukena cover it otherwise.

| Scene | Modesty state | Wardrobe tokens | Footwear | Hijab/cover | Note |
|---|---|---|---|---|---|
| SEQ1-SC02 | **Mukena** | `two-piece white mukena prayer set, opaque cotton, full head-and-body cover, plain matte weave` | barefoot | full mukena | makmum behind imam Herman; sakral SH02+ |
| SEQ2-SC03 | **Uncovered** | `long-sleeve tunic blouse relaxed modest muted slate-blue, wide-leg modest trousers charcoal` | flat slip-on mules | hair visible, low bun (Camille Friend) | brings susu tray to Andi; family-only (mahram) |
| SEQ3-SC01 | **Hijab** | W-day base + `cooking apron over tunic, plain muted, waist-tied` | flat slip-on mules | `instant-jersey hijab snug soft matte knit, hairline fully concealed` | live-selling broadcast → public non-mahram → covered despite being at home |
| SEQ3-SC02 | **Hijab** | W-day base *(identical to SEQ3-SC01 minus apron — same day)* | same | same jersey hijab | bank video call → on-camera non-mahram → covered |
| SEQ4-SC03 | **Hijab** | `loose cardigan over tunic hip-length soft knit, wide-leg modest trousers charcoal` | flat slip-on mules | `square voile hijab neatly pinned opaque matte weave draped over shoulders, muted dusty-teal` | balai warga, public venue |
| SEQ5-SC02 | **Hijab** | *(identical to SEQ4-SC03 — same afternoon→evening, lock token string)* | same | same voile hijab | warung tetangga, public + male owner |
| SEQ6-SC01 | **Uncovered** | `comfortable home tunic relaxed muted, modest trousers charcoal` | flat house slippers | hair visible, low bun (Camille Friend) | family dinner, four mahram in frame |
| SEQ6-SC02 | **Uncovered** | *(identical to SEQ6-SC01 — same evening)* | same | hair visible, low bun | ngaji, teaches Andi (son, mahram) |

*Continuity:* SEQ3-SC01→SC02 = ONE outfit same day (apron removed in SC02). SEQ4-SC03→SEQ5-SC02 = ONE community outfit, lock token string identical. SEQ6-SC01→SC02 = ONE evening home look, uncovered. Garment colorway desaturated; warmth via `color_grade` only (GATE B).

---

*Ratna sheet v0.3 (12 t2i plate prompts: 9 uncovered baseline §3 + 3 hijab reference §3.A; uncovered hair worn LOOSE & down past shoulders per ref-plate; 3-state modesty axis; "hijabi" keyword-leak removed from uncovered role) · Explainer Video 2 · 2026-06-20 · cites [[07-style-reference]] · method [[00-README]]*
