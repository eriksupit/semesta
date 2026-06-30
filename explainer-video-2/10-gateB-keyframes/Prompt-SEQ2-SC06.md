---
title: GATE B Prompt — SEQ2-SC06 (INT. RUANG BELAJAR — 08.30)
tags: [explainer-video-2, gate-b, prompt, status, SEQ2-SC06]
status: authoring
created: 2026-07-01
updated: 2026-07-01
aliases: [ev2-prompt-seq2-sc06]
---

# GATE B Prompt — SEQ2-SC06
## INT. RUANG BELAJAR — 08.30 WIB *(cross-cut SC05)*

> **Konvensi dua-doc:** prompt GATE B + status. Narasi = `SEQ2-SC06.md`. Env = `E03_ruangbelajar` (**plat SUDAH ADA di disk** ✓).
> **Pola seragam (SC01–SC05):** START full-prompt + attachment → END edit-in-place. Camera-lock: delta gestur in-frame; Ratna stasioner (no entry/transit). Tablet screen = slab polos (A1: kelas daring + "Jawaban Tepat ⭐" = AE). Grade pagi hangat dari jendela (GATE B). **Ratna uncovered** (mahram-only, di-stage di luar cone webcam kelas Andi).

## Manifest attachment (semua di disk ✓)
- **Env E03:** `E03_ruangbelajar_{master,desk,doorway,tablet}.png`.
- **Karakter:** `A_andi_front_{full,medium,closeup}` · `R_ratna_front_medium`.
- **Tanpa aset baru / tanpa PENDING plate** — SC06 siap di-generate kapanpun.

---

## SH01 — Establishing sudut belajar · MWS · 35mm
**START attachments:** `E03_ruangbelajar_doorway.png` + `A_andi_front_full.png`.
- **START** — mode **B** (full master, 1-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E03_ruangbelajar_doorway.png — same study corner, same desk, same window, same layout, same handedness, faithful match"],
    "identity_reference": ["A_andi_front_full.png — same identical boy, matched face, age ten"]
  },
  "mood": "bright warm study morning, attentive child calm, gentle domestic register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "home study corner morning, a child at a small desk, a tablet propped showing a plain neutral glowing slab, warm morning window light, lived-in middle-class home",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "warm morning window light, quiet study calm",
  "scene_depth": {
    "foreground": "desk edge low frame",
    "midground": "Andi seated at the desk, a propped tablet before him",
    "background": "study shelf, window, soft room"
  },
  "subjects": [ { "who": "Andi", "identity_reference": "A_andi_front_full.png" } ],
  "subject_state": "static",
  "action": "Andi seated at his desk attending the online class on the tablet",
  "pose": "Andi seated upright at the small desk, hands resting on the desk, eyes on the propped tablet",
  "gesture": "hands flat on the desk, attentive",
  "expression": "calm attentive listening",
  "grooming": "short neat boy hair",
  "wardrobe": "tidy primary-school uniform, short-sleeve shirt",
  "framing": "medium-wide establishing, the study corner, Andi at the desk, window light",
  "angle": "doorway vantage, eye-level, the room, the desk",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "warm morning daylight from the window camera-left, soft warm key, gentle room fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, warm window wrap, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte fresh child skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat child grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Andi condong sedikit menyimak; stasioner) · STATUS: ✅ authored:
```
Change only Andi posture, position held.

- Andi: now leaned slightly forward toward the tablet, attentive, hands still on the desk
- unchanged: framing unchanged, camera angle unchanged, Andi seated position unchanged, desk unchanged, tablet plain slab unchanged, window unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH02 — Andi menjawab · MEDIUM · 50mm
**START attachments:** `E03_ruangbelajar_desk.png` + `A_andi_front_medium.png`.
- **START** — mode **B** (full master, 1-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E03_ruangbelajar_desk.png — same desk, same tablet, same study corner, faithful match"],
    "identity_reference": ["A_andi_front_medium.png — same identical boy, matched face, age ten"]
  },
  "mood": "engaged warm study morning, a child participating, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a child at a study desk, a propped tablet plain neutral glowing slab, warm morning window light",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "warm morning window light, focused calm",
  "scene_depth": {
    "foreground": "desk surface low frame",
    "midground": "Andi at the desk, the tablet before him",
    "background": "study shelf, window, soft"
  },
  "subjects": [ { "who": "Andi", "identity_reference": "A_andi_front_medium.png" } ],
  "subject_state": "static",
  "action": "Andi at the desk attending, hands on the desk",
  "pose": "Andi seated at the desk facing the tablet, hands on the desk surface, upright attentive",
  "gesture": "hands on the desk, ready",
  "expression": "bright attentive focus",
  "grooming": "short neat boy hair",
  "wardrobe": "tidy primary-school uniform",
  "framing": "medium shot, Andi head to waist, tablet foreground edge",
  "angle": "eye-level at child seated height, facing Andi",
  "camera": "50mm prime spherical, shallow depth of field, focus on Andi",
  "lighting": "warm morning daylight from the window, soft warm key, gentle fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, warm window wrap, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte fresh child skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat child grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Andi angkat tangan + menjawab) · STATUS: ✅ authored:
```
Change only Andi gesture, position held.

- Andi: now one hand raised up beside his head, answering, mouth slightly open speaking, eyes on the tablet
- expression: eager, bright, participating
- unchanged: framing unchanged, camera angle unchanged, Andi seated position unchanged, desk unchanged, tablet plain slab unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH03 — Insert tablet (Jawaban Tepat) · CLOSE · 85mm
**START attachments:** `E03_ruangbelajar_tablet.png`. **A1: layar slab polos; kelas daring + bintang "Jawaban Tepat" = AE.**
- **START** — mode **B** (object insert) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E03_ruangbelajar_tablet.png — same propped tablet, same desk, identical insert geometry, faithful match"]
  },
  "mood": "a small bright study reward moment, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic material rendering",
  "scene": "a propped study tablet, screen a plain bright neutral glowing slab blank featureless, on a small desk, warm morning ambient",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "warm morning ambient, soft",
  "scene_depth": {
    "foreground": "desk surface at the tablet base",
    "midground": "the tablet screen, plain neutral glowing slab, sharp",
    "background": "soft out-of-focus study shelf, warm light"
  },
  "subject_state": "static",
  "action": "the tablet glowing plain, the class in session",
  "framing": "close insert, the tablet screen frame-dominant",
  "angle": "facing the tablet screen, eye-level at desk height",
  "camera": "85mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "plain neutral screen glow as local key, warm morning ambient fill, soft",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity"
}
```
- **END** — minimal-hold (tanda "Jawaban Tepat ⭐" = AE state-change) · STATUS: ✅ authored:
```
Hold identical to START — no still-frame delta. The online class boxes + lesson board + the "Jawaban Tepat ⭐" appreciation badge = After Effects overlays on the plain slab. Keep frame, screen slab, lighting, framing identical.
```

---

## SH04 — Ratna membawa susu · MEDIUM 2-shot · 50mm
**START attachments:** `E03_ruangbelajar_desk.png` + `A_andi_front_medium.png` + `R_ratna_front_medium.png`.
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored. **Ratna stasioner (no entry); uncovered (mahram, di luar cone webcam).**
```json
{
  "attachment_manifest": {
    "environment_reference": ["E03_ruangbelajar_desk.png — same desk, same study corner, same window, faithful match"],
    "identity_reference": ["A_andi_front_medium.png — same identical boy, matched face, age ten", "R_ratna_front_medium.png — same identical woman, matched face, uncovered hair visible, early-forties"]
  },
  "mood": "tender family study morning, a mother caring touch, warm domestic register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a child at a study desk, his mother beside him holding a glass of milk, a propped tablet plain neutral slab, warm morning window light",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "warm morning window light, tender calm",
  "scene_depth": {
    "foreground": "desk edge low frame",
    "midground": "Andi seated camera-left, Ratna beside him camera-right, a glass of milk in her hand",
    "background": "study shelf, window, soft"
  },
  "subjects": [
    { "who": "Andi", "identity_reference": "A_andi_front_medium.png" },
    { "who": "Ratna", "identity_reference": "R_ratna_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "Andi at the desk attending, Ratna beside him holding a glass of milk",
  "pose": "Andi seated camera-left facing the tablet, Ratna standing beside him camera-right, a glass of milk in one hand, the other hand near his shoulder",
  "gesture": "Andi eyes on the screen, Ratna holding the milk, inclined toward him",
  "expression": "Andi attentive, Ratna warm tender",
  "grooming": "Andi short neat hair, Ratna loose uncovered hair",
  "wardrobe": "Andi primary-school uniform, Ratna modest long-sleeve home tunic, uncovered",
  "framing": "medium two-shot, Andi seated camera-left, Ratna head to waist camera-right",
  "angle": "eye-level, from the desk side, both figures, staged clear of the tablet camera",
  "camera": "50mm prime spherical, shallow depth of field, focus on Andi",
  "lighting": "warm morning daylight from the window, soft warm key on both, gentle fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, warm window wrap, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Ratna taruh susu + usap kepala Andi; gestur in-frame) · STATUS: ✅ authored:
```
Change only Ratna gesture, positions held.

- Ratna: the glass of milk now set on the desk beside Andi, her other hand resting softly on his head, a gentle ruffle
- Andi: a flicker of a smile, eyes still on the tablet
- unchanged: framing unchanged, camera angle unchanged, both positions unchanged, desk unchanged, tablet plain slab unchanged, window unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH05 — Andi nyengir · CLOSE-UP · 85mm
**START attachments:** `A_andi_front_closeup.png`. *(CU wajah, ruang tak tampak → tanpa env plate.)*
- **START** — mode **B** (face CU) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "identity_reference": ["A_andi_front_closeup.png — same identical boy, matched face, age ten, fresh child skin"]
  },
  "mood": "proud warm child moment, a small bright joy, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a child face lit by warm morning window light, soft study background, screen glow on his eyes",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "warm morning light, soft",
  "scene_depth": {
    "foreground": "soft out-of-focus desk edge",
    "midground": "Andi face, sharp",
    "background": "soft warm study, out of focus"
  },
  "subjects": [ { "who": "Andi", "identity_reference": "A_andi_front_closeup.png" } ],
  "subject_state": "static",
  "action": "Andi watching the screen, face attentive",
  "pose": "Andi face three-quarter toward the tablet off-frame, eyes fixed on the screen",
  "gesture": "still, watching",
  "expression": "attentive neutral focus, lips closed",
  "grooming": "short neat boy hair",
  "framing": "close-up, Andi face frame-filling, head, a little shoulder",
  "angle": "eye-level close, facing Andi, the screen off-frame",
  "camera": "85mm prime spherical, shallow depth of field, focus on the eyes",
  "lighting": "warm morning daylight key from camera-left window, soft cool screen glow on his eyes from off-frame, warm-cool balance",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, warm window wrap, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte fresh child skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat child grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Andi nyengir bangga, pandang tetap ke layar) · STATUS: ✅ authored:
```
Change only the expression.

- expression: a wide proud grin, teeth showing, cheeks lifted, eyes bright and still on the screen off-frame
- unchanged: framing unchanged, camera angle unchanged, Andi head position unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## Status board
| Shot | START | END | Render |
|---|---|---|---|
| SH01 | ✅ authored | ✅ authored | pending (final batch) |
| SH02 | ✅ authored | ✅ authored | pending (final batch) |
| SH03 | ✅ authored | ✅ hold (AE star) | pending (final batch) |
| SH04 | ✅ authored | ✅ authored | pending (final batch) |
| SH05 | ✅ authored | ✅ authored | pending (final batch) |

**Ladder:** W→M→CU→M→CU. **Grade pagi hangat dari jendela** (GATE B). **Camera-lock:** Ratna stasioner (no entry); delta gestur in-frame. **A1:** tablet = slab polos (kelas daring + "Jawaban Tepat ⭐" = AE). **Modesty:** Ratna uncovered (mahram-only, di-stage di luar cone webcam kelas Andi). **Plates ALL on disk** (E03 + Andi + Ratna) — SC06 siap generate.
