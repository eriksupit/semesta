---
title: GATE B Prompt — SEQ2-SC07 (EXT. SELASAR KAMPUS — 10.00)
tags: [explainer-video-2, gate-b, prompt, status, SEQ2-SC07]
status: authoring
created: 2026-07-01
updated: 2026-07-01
aliases: [ev2-prompt-seq2-sc07]
---

# GATE B Prompt — SEQ2-SC07
## EXT. SELASAR KAMPUS — 10.00 WIB *(penutup SEQ2)*

> **Konvensi dua-doc:** prompt GATE B + status. Narasi = `SEQ2-SC07.md`. Env = `E09-selasarkampus.md` (2× SC07+SC09). Figuran `F8 peer-mentor`.
> **Pola seragam (SC01–SC06):** START full-prompt + attachment → END edit-in-place. Camera-lock: delta gestur/gaze in-frame; Lisa stasioner (no entry/transit; duduk di-START SH04, "menghampiri" disiratkan). Device screen OFF/polos (A1: kartu profil komunitas = AE). Grade siang teduh (GATE B). Lisa + mentor uncovered (faith not imposed). 2 subjek (lean).

## Manifest attachment
- **Env E09 (⚠ PENDING final-batch):** `E09_selasarkampus_master.png` (selasar + bangku WIDE) · `E09_selasarkampus_bangku.png` (bangku MS). *(⚠ E09 dipakai 2× SC07+SC09 — bedakan spot/komposisi dari SC09.)*
- **Karakter:** `L_lisa_front_{full,medium,closeup}` (✓) · `F_mentor_front_{full,medium}` (⚠ PENDING — figuran F8).
- **Generate-order final-batch:** E09 master+bangku + F_mentor plate **sebelum** keyframe SC07.

---

## SH01 — Establishing selasar + mentor melambai · WIDE · 28mm
**START attachments:** `E09_selasarkampus_master.png` (PENDING) + `L_lisa_front_full.png` + `F_mentor_front_full.png` (PENDING).
- **START** — mode **B** (full master, 2-subjek WIDE) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E09_selasarkampus_master.png — same shaded campus colonnade, same bench, same layout, same handedness, faithful match"],
    "identity_reference": ["L_lisa_front_full.png — same identical young woman, matched face, uncovered loose hair, early-twenties", "F_mentor_front_full.png — same identical senior female student, matched face, uncovered, early-twenties"]
  },
  "mood": "calm bright campus mid-morning, easy student warmth, everyday register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "shaded campus colonnade walkway mid-morning, a bench along the side, soft filtered daylight, calm student setting",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "soft shaded daylight, dappled filtered light, quiet calm",
  "scene_depth": {
    "foreground": "colonnade paving low frame",
    "midground": "the mentor seated on the bench camera-right, Lisa standing in the walkway camera-left",
    "background": "colonnade columns receding, soft greenery"
  },
  "subjects": [
    { "who": "Lisa", "identity_reference": "L_lisa_front_full.png" },
    { "who": "mentor", "identity_reference": "F_mentor_front_full.png" }
  ],
  "subject_state": "static",
  "action": "the mentor seated on the bench, Lisa standing in the colonnade",
  "pose": "the mentor seated on the bench camera-right, a tote bag beside her, Lisa standing camera-left in the walkway, a small shoulder bag, both turned slightly toward each other",
  "gesture": "the mentor settled on the bench, Lisa standing at ease",
  "expression": "both calm, friendly, anticipatory",
  "grooming": "Lisa loose uncovered hair, the mentor loose uncovered hair",
  "wardrobe": "Lisa modest casual long-sleeve top, jeans, the mentor modest casual blouse, trousers",
  "framing": "wide establishing, the colonnade, the bench camera-right, two small figures",
  "angle": "eye-level, along the colonnade walkway",
  "camera": "28mm prime spherical, deep focus front to back",
  "lighting": "soft shaded daylight, gentle dappled filtered light through the colonnade, even cool-neutral fill, soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural shaded daylight realism, soft even fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian campus exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte fresh young skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat young grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: mentor melambai, Lisa menoleh mengenali) · STATUS: ✅ authored:
```
Change only the gestures, positions held.

- mentor: now one hand raised in a small wave toward Lisa, a warm smile
- Lisa: now turned toward the mentor, a smile of recognition, head lifted
- unchanged: framing unchanged, camera angle unchanged, both positions unchanged, bench unchanged, colonnade unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH02 — Insert HP Lisa (profil mentor) · CLOSE · 85mm
**START attachments:** `L_lisa_front_medium.png` (tangan/identitas). **A1: layar slab polos; kartu profil = AE.**
- **START** — mode **B** (insert tangan+HP) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "identity_reference": ["L_lisa_front_medium.png — same identical young woman hand, matched skin tone, sleeve cuff"]
  },
  "mood": "a quiet checking moment, a connection about to happen, everyday register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a young woman hand holding a smartphone, screen off dark neutral blank slab, soft shaded campus daylight",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "soft shaded daylight, calm",
  "scene_depth": {
    "foreground": "thumb at the phone edge",
    "midground": "smartphone in hand, screen off dark neutral, sharp",
    "background": "soft out-of-focus colonnade, shaded greenery"
  },
  "subjects": [ { "who": "Lisa hand", "identity_reference": "L_lisa_front_medium.png" } ],
  "subject_state": "static",
  "action": "a hand holding the phone up, screen off, reading",
  "pose": "Lisa hand holding a smartphone upright, fingers around the body, thumb resting at the lower edge",
  "gesture": "thumb steady at the screen edge, reading",
  "framing": "close-up insert, the hand, the smartphone, screen frame-dominant",
  "angle": "downward onto the screen, eye-level lowered",
  "camera": "85mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "soft shaded daylight on the hand, even cool-neutral key, phone screen off dark neutral, faint reflection on the glass",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural shaded daylight realism, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian campus exterior realism"
}
```
- **END** — minimal-hold (kartu profil = AE; jempol diam) · STATUS: ✅ authored:
```
Hold near-identical to START — the thumb stays steady at the screen edge, reading. The community-feature mentor profile card (photo + name "Janji temu mentor · [nama]") = After Effects overlay on the plain slab. Keep frame, hand, screen slab, lighting, framing identical.
```

---

## SH03 — Lisa mencocokkan wajah · MEDIUM · 50mm
**START attachments:** `E09_selasarkampus_bangku.png` (PENDING) + `L_lisa_front_medium.png`.
- **START** — mode **B** (full master, 1-subjek; mentor soft) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E09_selasarkampus_bangku.png — same bench, same shaded colonnade, faithful match"],
    "identity_reference": ["L_lisa_front_medium.png — same identical young woman, matched face, uncovered hair, early-twenties"]
  },
  "mood": "a recognizing moment, warm anticipation, everyday register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a young woman in the shaded colonnade holding a phone, a seated figure soft behind, filtered daylight",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "soft shaded daylight, calm",
  "scene_depth": {
    "foreground": "colonnade paving low frame",
    "midground": "Lisa standing, a phone in her hand",
    "background": "the mentor soft on the bench, colonnade"
  },
  "subjects": [ { "who": "Lisa", "identity_reference": "L_lisa_front_medium.png" } ],
  "subject_state": "static",
  "action": "Lisa standing looking at her phone, the mentor soft behind",
  "pose": "Lisa standing centre, a smartphone held up at chest height in one hand, eyes on the screen, the mentor soft on the bench behind",
  "gesture": "Lisa eyes on the screen, reading",
  "expression": "focused, about to recognize",
  "grooming": "loose uncovered hair",
  "wardrobe": "modest casual long-sleeve top, jeans, shoulder bag",
  "framing": "medium shot, Lisa head to waist centre, the mentor soft background",
  "angle": "eye-level, facing Lisa, the bench behind",
  "camera": "50mm prime spherical, shallow depth of field, focus on Lisa",
  "lighting": "soft shaded daylight, even cool-neutral key, gentle fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural shaded daylight realism, soft even fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian campus exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte fresh young skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat young grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Lisa angkat pandang ke mentor + kantongi ponsel) · STATUS: ✅ authored:
```
Change only Lisa gaze and the phone, position held.

- Lisa: now her eyes lifted from the screen toward the mentor off-frame, a warm recognizing smile, the phone lowered to her side, slipped toward her bag
- unchanged: framing unchanged, camera angle unchanged, Lisa standing position unchanged, the mentor soft background unchanged, bench unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH04 — Duduk berdampingan · MEDIUM-WIDE 2-shot · 35mm
**START attachments:** `E09_selasarkampus_bangku.png` (PENDING) + `L_lisa_front_full.png` + `F_mentor_front_full.png` (PENDING). **Lisa sudah duduk (no transit).**
- **START** — mode **B** (full master, 2-subjek duduk) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E09_selasarkampus_bangku.png — same bench, same shaded colonnade, faithful match"],
    "identity_reference": ["L_lisa_front_full.png — same identical young woman, matched face, uncovered hair, early-twenties", "F_mentor_front_full.png — same identical senior female student, matched face, uncovered, early-twenties"]
  },
  "mood": "warm real connection, two students side by side, everyday register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "two young women seated side by side on a shaded campus bench, soft filtered daylight, calm colonnade",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "soft shaded daylight, warm calm",
  "scene_depth": {
    "foreground": "colonnade paving low frame",
    "midground": "Lisa, the mentor seated side by side on the bench",
    "background": "colonnade columns, soft greenery"
  },
  "subjects": [
    { "who": "Lisa", "identity_reference": "L_lisa_front_full.png" },
    { "who": "mentor", "identity_reference": "F_mentor_front_full.png" }
  ],
  "subject_state": "static",
  "action": "Lisa, the mentor, seated side by side on the bench, settling to talk",
  "pose": "Lisa seated camera-left on the bench, the mentor seated camera-right, both upright, bags beside them, turned slightly toward each other",
  "gesture": "both hands settled in laps, easing into conversation",
  "expression": "both warm, open, friendly",
  "grooming": "Lisa loose uncovered hair, the mentor loose uncovered hair",
  "wardrobe": "Lisa casual long-sleeve top, jeans, the mentor casual blouse, trousers",
  "framing": "medium-wide two-shot, both seated head to knee on the bench",
  "angle": "eye-level, facing the bench, both figures",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "soft shaded daylight, gentle dappled filtered light, even fill, soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural shaded daylight realism, soft even fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian campus exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte fresh young skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat young grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: keduanya menoleh saling mengobrol) · STATUS: ✅ authored:
```
Change only the gestures, positions held.

- Lisa: now turned toward the mentor, mid-sentence, a small hand gesture, warm
- mentor: now turned toward Lisa, attentive, a listening smile
- unchanged: framing unchanged, camera angle unchanged, both seated positions on the bench unchanged, colonnade unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH05 — Mengobrol hangat (tatap muka) · MEDIUM 2-shot · 50mm
**START attachments:** `E09_selasarkampus_bangku.png` (PENDING) + `L_lisa_front_medium.png` + `F_mentor_front_medium.png` (PENDING).
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E09_selasarkampus_bangku.png — same bench, same shaded colonnade, faithful match"],
    "identity_reference": ["L_lisa_front_medium.png — same identical young woman, matched face, uncovered hair, early-twenties", "F_mentor_front_medium.png — same identical senior female student, matched face, uncovered"]
  },
  "mood": "warm face-to-face talk, real human connection, everyday register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "two young women on a shaded bench talking face to face, phones away, soft filtered daylight",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "soft shaded daylight, warm calm",
  "scene_depth": {
    "foreground": "bench edge low frame",
    "midground": "Lisa, the mentor talking face to face",
    "background": "soft colonnade, greenery"
  },
  "subjects": [
    { "who": "Lisa", "identity_reference": "L_lisa_front_medium.png" },
    { "who": "mentor", "identity_reference": "F_mentor_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "the two talking face to face, one speaking",
  "pose": "Lisa camera-left turned toward the mentor speaking, the mentor camera-right facing her listening, both seated close",
  "gesture": "Lisa a small open hand gesture mid-sentence, the mentor attentive",
  "expression": "Lisa warm animated, the mentor warm listening",
  "grooming": "both loose uncovered hair",
  "wardrobe": "Lisa casual top, the mentor casual blouse",
  "framing": "medium two-shot, both head to chest, turned to each other",
  "angle": "eye-level, closer on the two faces, the bench",
  "camera": "50mm prime spherical, shallow depth of field, focus split on the two faces",
  "lighting": "soft shaded daylight, warm gentle fill, soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural shaded daylight realism, soft even fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian campus exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte fresh young skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat young grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: yang lain merespons senyum/mengangguk) · STATUS: ✅ authored:
```
Change only the response, positions held.

- mentor: now responding, a warm nod, a smile, a small hand gesture back
- Lisa: listening now, a warm smile, settled
- unchanged: framing unchanged, camera angle unchanged, both seated positions unchanged, bench unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## Status board
| Shot | START | END | Render |
|---|---|---|---|
| SH01 | ✅ authored | ✅ authored | pending (final batch) |
| SH02 | ✅ authored | ✅ hold (AE card) | pending (final batch) |
| SH03 | ✅ authored | ✅ authored | pending (final batch) |
| SH04 | ✅ authored | ✅ authored | pending (final batch) |
| SH05 | ✅ authored | ✅ authored | pending (final batch) |

**Ladder:** W→CU→M→MW→M. **Grade siang teduh** (GATE B). **Camera-lock:** Lisa stasioner (no transit; duduk di-START SH04). **A1:** SH02 screen OFF/polos (kartu profil komunitas = AE). **Wasilah/tatap-muka** tesis. **⚠ PENDING plates:** `E09_selasarkampus_{master,bangku}` (2× SC07+SC09) + `F_mentor_front_{full,medium}` (figuran F8). **Penutup SEQ2.**
