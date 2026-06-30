---
title: GATE B Prompt — SEQ3-SC09 (EXT. SELASAR KAMPUS — 13.00)
tags: [explainer-video-2, gate-b, prompt, status, SEQ3-SC09]
status: authoring
created: 2026-07-01
updated: 2026-07-01
aliases: [ev2-prompt-seq3-sc09]
---

# GATE B Prompt — SEQ3-SC09
## EXT. SELASAR KAMPUS — 13.00 WIB *(penutup SEQ3)*

> **Konvensi dua-doc:** prompt GATE B + status. Narasi = `SEQ3-SC09.md`. Env = `E09_selasarkampus` (cell `bangku2`, spot/angle beda dari SC07 + siang). Figuran `F9 ibu petugas kebersihan`.
> **Pola seragam (SC01–SC08):** START full-prompt + attachment → END edit-in-place. Camera-lock: delta gestur in-frame; Lisa duduk di-START (no transit). Device screen OFF/polos (A1: alur dokter = AE). Grade siang teduh (GATE B). Lisa + ibu uncovered (faith not imposed). 2 subjek (lean). **Touch OK (Lisa↔ibu sama-gender).**

## Manifest attachment
- **Env E09 (⚠ PENDING final-batch):** `E09_selasarkampus_bangku2.png` (spot/angle SC09 — bedakan dari SC07 master/bangku).
- **Karakter:** `L_lisa_front_{full,medium}` (✓) · `F_ibupetugas_front_{full,medium}` (⚠ PENDING — figuran F9; **verify aged ~mid-fifties, jangan de-aged, plat-pertama**).
- **Generate-order final-batch:** E09 bangku2 + F_ibupetugas plate **sebelum** keyframe SC09.

---

## SH01 — Establishing: ibu petugas di bangku · MWS · 35mm
**START attachments:** `E09_selasarkampus_bangku2.png` (PENDING) + `F_ibupetugas_front_full.png` (PENDING).
- **START** — mode **B** (full master, 1-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E09_selasarkampus_bangku2.png — same shaded campus colonnade, a different bench spot, same handedness, faithful match"],
    "identity_reference": ["F_ibupetugas_front_full.png — same identical middle-aged woman, matched face, mid-fifties, lined face, gray-streaked hair"]
  },
  "mood": "quiet tired midday, a hard-working older woman resting, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "shaded campus colonnade bench past midday, a campus cleaner resting, soft filtered daylight, calm",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "shaded midday light, bright beyond the shade, quiet",
  "scene_depth": {
    "foreground": "colonnade paving low frame",
    "midground": "the older woman seated on the bench, hands at her knee",
    "background": "colonnade columns, soft greenery, bright sun beyond the shade"
  },
  "subjects": [ { "who": "ibu petugas", "identity_reference": "F_ibupetugas_front_full.png" } ],
  "subject_state": "static",
  "action": "the older woman seated resting, hands at her knee",
  "pose": "the middle-aged cleaner seated on the bench, both hands pressed to one knee, shoulders a little rounded from tiredness",
  "gesture": "hands at the knee, resting",
  "expression": "tired, a faint discomfort, patient",
  "grooming": "gray-streaked hair tied back, lined mature face",
  "wardrobe": "campus cleaner work uniform, plain, practical",
  "framing": "medium-wide establishing, the bench, the woman, the colonnade",
  "angle": "eye-level, facing the bench, a different spot from SC07",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "soft shaded daylight, gentle filtered light, bright sun beyond, even fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural shaded daylight realism, soft even fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian campus exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte mature lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat mature grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: ibu memijit lutut + sedikit meringis) · STATUS: ✅ authored:
```
Change only the gesture and expression, position held.

- ibu petugas: now one hand pressing into her knee in a small massage, the other steadying it, a faint wince
- expression: a slight grimace of knee discomfort, patient
- unchanged: framing unchanged, camera angle unchanged, seated position on the bench unchanged, colonnade unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH02 — Lisa duduk membuka app · MEDIUM 2-shot · 50mm
**START attachments:** `E09_selasarkampus_bangku2.png` (PENDING) + `L_lisa_front_full.png` + `F_ibupetugas_front_full.png` (PENDING). **Lisa sudah duduk (no transit).**
- **START** — mode **B** (full master, 2-subjek duduk) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E09_selasarkampus_bangku2.png — same bench spot, same shaded colonnade, faithful match"],
    "identity_reference": ["L_lisa_front_full.png — same identical young woman, matched face, uncovered hair, early-twenties", "F_ibupetugas_front_full.png — same identical middle-aged woman, matched face, mid-fifties, lined face"]
  },
  "mood": "a kind sitting-down, generations side by side, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "two women on a shaded campus bench, a young student beside an older cleaner, a phone in the young woman hand, soft filtered daylight",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "shaded midday light, calm",
  "scene_depth": {
    "foreground": "bench edge low frame",
    "midground": "Lisa seated camera-left, the older woman camera-right",
    "background": "colonnade, soft greenery"
  },
  "subjects": [
    { "who": "Lisa", "identity_reference": "L_lisa_front_full.png" },
    { "who": "ibu petugas", "identity_reference": "F_ibupetugas_front_full.png" }
  ],
  "subject_state": "static",
  "action": "Lisa seated beside the older woman, a phone in her hand, the woman resting",
  "pose": "Lisa seated camera-left on the bench, a smartphone in her hands, turned slightly toward the older woman camera-right, the woman seated hands at her knee",
  "gesture": "Lisa holding the phone, attention toward the woman, the woman resting",
  "expression": "Lisa warm helpful, the older woman tired grateful",
  "grooming": "Lisa loose uncovered hair, the woman gray-streaked hair tied back",
  "wardrobe": "Lisa casual long-sleeve top, jeans, the woman cleaner uniform",
  "framing": "medium two-shot, both seated head to thigh on the bench",
  "angle": "eye-level, facing the bench, both figures",
  "camera": "50mm prime spherical, shallow depth of field, focus split on the two",
  "lighting": "soft shaded daylight, even fill, soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural shaded daylight realism, soft even fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian campus exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Lisa membuka app di ponsel) · STATUS: ✅ authored:
```
Change only Lisa gesture, positions held.

- Lisa: now holding the phone up between them, one thumb on the screen, opening the app, turned toward the older woman
- unchanged: framing unchanged, camera angle unchanged, both seated positions unchanged, bench unchanged, colonnade unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH03 — Insert HP: pilih jadwal dokter · CLOSE · 85mm
**START attachments:** `L_lisa_front_medium.png` (tangan). **A1: layar slab polos; alur dokter = AE.**
- **START** — mode **B** (insert tangan+HP) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "identity_reference": ["L_lisa_front_medium.png — same identical young woman hand, matched skin tone, sleeve cuff"]
  },
  "mood": "a small helpful act, a doctor a tap away, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a young woman hand holding a smartphone tilted toward an older woman, screen off dark neutral blank slab, shaded daylight",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "shaded midday light, soft",
  "scene_depth": {
    "foreground": "thumb at the phone edge",
    "midground": "smartphone tilted in hand, screen off dark neutral, sharp",
    "background": "soft out-of-focus bench, a hint of the older woman"
  },
  "subjects": [ { "who": "Lisa hand", "identity_reference": "L_lisa_front_medium.png" } ],
  "subject_state": "static",
  "action": "a hand holding the phone tilted, screen off, a choice in progress",
  "pose": "Lisa hand holding a smartphone tilted toward the older woman, thumb at the lower screen",
  "gesture": "thumb at the screen, mid-selection",
  "framing": "close-up insert, the hand, the tilted smartphone, screen frame-dominant",
  "angle": "downward onto the tilted screen, eye-level lowered",
  "camera": "85mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "soft shaded daylight on the hand, even key, phone screen off dark neutral, faint reflection",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural shaded daylight realism, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian campus exterior realism"
}
```
- **END** — minimal-hold (konfirmasi janji = AE; ketukan terakhir) · STATUS: ✅ authored:
```
Hold near-identical to START — the thumb completes one final tap. The doctor-scheduling flow "Pilih jadwal dokter" → "Janji dokter — terjadwal" = After Effects overlays on the plain slab. Keep frame, hand, screen slab, lighting, framing identical.
```

---

## SH04 — Ibu membaca, lega · MEDIUM 2-shot · 50mm
**START attachments:** `E09_selasarkampus_bangku2.png` (PENDING) + `L_lisa_front_medium.png` + `F_ibupetugas_front_medium.png` (PENDING).
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E09_selasarkampus_bangku2.png — same bench spot, same shaded colonnade, faithful match"],
    "identity_reference": ["L_lisa_front_medium.png — same identical young woman, matched face, early-twenties", "F_ibupetugas_front_medium.png — same identical middle-aged woman, matched face, mid-fifties, lined face"]
  },
  "mood": "quiet relief, a burden lifted, tender register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "the older woman reading a phone held toward her, the young woman beside her, shaded campus bench, soft daylight",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "shaded midday light, tender calm",
  "scene_depth": {
    "foreground": "bench edge low frame",
    "midground": "the older woman reading the screen, Lisa beside her holding the phone",
    "background": "colonnade, soft greenery"
  },
  "subjects": [
    { "who": "Lisa", "identity_reference": "L_lisa_front_medium.png" },
    { "who": "ibu petugas", "identity_reference": "F_ibupetugas_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "the older woman reading the screen, a long breath, Lisa beside her",
  "pose": "the older woman camera-right leaned toward the phone reading, Lisa camera-left holding the phone toward her, both seated",
  "gesture": "the woman reading, Lisa steadying the phone",
  "expression": "the woman relieved, a long exhale, Lisa warm",
  "grooming": "the woman gray-streaked hair, Lisa loose hair",
  "wardrobe": "the woman cleaner uniform, Lisa casual top",
  "framing": "medium two-shot, both head to chest, the phone between",
  "angle": "eye-level, facing the bench, both figures",
  "camera": "50mm prime spherical, shallow depth of field, focus on the older woman",
  "lighting": "soft shaded daylight, warm gentle fill, soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural shaded daylight realism, soft even fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian campus exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte mature lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: ibu menepuk punggung tangan Lisa) · STATUS: ✅ authored:
```
Change only the gesture, positions held.

- ibu petugas: now one hand reached over to rest on the back of Lisa hand, a gentle pat, a grateful look toward Lisa
- Lisa: a warm soft smile back
- unchanged: framing unchanged, camera angle unchanged, both seated positions unchanged, bench unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH05 — Tangan ibu menepuk tangan Lisa (detail) · CLOSE-UP · 100mm
**START attachments:** `F_ibupetugas_front_medium.png` (tangan ibu, PENDING) + `L_lisa_front_medium.png` (tangan Lisa).
- **START** — mode **B** (detail 2-tangan) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "identity_reference": ["F_ibupetugas_front_medium.png — same older woman hand, matched mature skin, lined", "L_lisa_front_medium.png — same young woman hand, matched young skin"]
  },
  "mood": "warm cross-generation gratitude, a quiet thank-you, tender register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "two hands on a bench, an older lined hand over a young hand, shaded warm daylight",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "shaded midday light, warm",
  "scene_depth": {
    "foreground": "bench surface at the hands",
    "midground": "the older hand over the young hand, sharp",
    "background": "soft out-of-focus uniform, jeans"
  },
  "subjects": [
    { "who": "ibu hand", "identity_reference": "F_ibupetugas_front_medium.png" },
    { "who": "Lisa hand", "identity_reference": "L_lisa_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "an older hand resting onto a young hand on the bench",
  "pose": "the older lined hand laid over the back of Lisa young hand on the bench, fingers settling",
  "gesture": "the older hand a gentle pat, settling",
  "framing": "close-up, two hands frame-dominant on the bench",
  "angle": "downward onto the hands, eye-level lowered",
  "camera": "100mm prime spherical, shallow depth of field, focus on the hands",
  "lighting": "soft shaded daylight, warm gentle key, soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural shaded daylight realism, soft warm fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian campus exterior realism"
}
```
- **END** — EDIT-IN-PLACE (delta: tepukan lembut berhenti, tangan diam) · STATUS: ✅ authored:
```
Change only the settling.

- ibu hand: the pat now come to rest, the older hand settled fully over the young hand, still, warm
- unchanged: framing unchanged, camera angle unchanged, both hands positions unchanged, bench unchanged, lighting unchanged, color grade unchanged, hands matching attached plates
```

---

## Status board
| Shot | START | END | Render |
|---|---|---|---|
| SH01 | ✅ authored | ✅ authored | pending (final batch) |
| SH02 | ✅ authored | ✅ authored | pending (final batch) |
| SH03 | ✅ authored | ✅ hold (AE flow) | pending (final batch) |
| SH04 | ✅ authored | ✅ authored | pending (final batch) |
| SH05 | ✅ authored | ✅ authored | pending (final batch) |

**Ladder:** MWS→M→CU→M→CU. **Grade siang teduh** (GATE B). **Camera-lock:** Lisa duduk di-START (no transit); delta gestur in-frame. **A1:** SH03 screen OFF/polos (alur dokter = AE). **Touch OK** (Lisa↔ibu sama-gender, lintas-generasi). **⚠ PENDING plates:** `E09_selasarkampus_bangku2` + `F_ibupetugas_front_{full,medium}` (figuran F9 — verify aged ~mid-fifties plat-pertama). **Penutup SEQ3.**
