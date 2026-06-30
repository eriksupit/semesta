---
title: GATE B Prompt — SEQ4-SC11 (EXT. TAMAN KOTA — 16.45)
tags: [explainer-video-2, gate-b, prompt, status, SEQ4-SC11]
status: authoring
created: 2026-07-01
updated: 2026-07-01
aliases: [ev2-prompt-seq4-sc11]
---

# GATE B Prompt — SEQ4-SC11
## EXT. TAMAN KOTA — 16.45 WIB *(penutup SEQ4)*

> **Konvensi dua-doc:** prompt GATE B + status. Narasi = `SEQ4-SC11.md`. Env = `E16-tamankota.md`. Orang-tertunduk-layar = **ambient crowd** (tak face-locked, no plate).
> **Pola seragam (SC01–SC10):** START full-prompt + attachment → END edit-in-place. **Scene lokomosi → beat-jeda:** subjek PAUSED/santai di jalur tiap shot, delta = gestur/cerita/tunjuk-HP, **BUKAN menyeberang frame** (camera-lock i2v). Device screen OFF/polos (A1: langkah harian = AE). Grade **sore keemasan golden-hour** (GATE B). **Ratna berhijab** (taman publik non-mahram); Andi uncovered (mahram). **Bingkai tech-as-tool** (app sebentar lalu dikantongi). Latar scroller = soft, tak face-locked.

## Manifest attachment
- **Env E16 (⚠ PENDING final-batch):** `E16_tamankota_master.png` (taman + bangku + jalur, kontras) · `E16_tamankota_jalur.png` (jalur MS).
- **Karakter:** `R_ratna_hijab_front_{full,medium}` (✓) · `A_andi_front_{full,medium}` (✓). *(Latar scroller = ambient, tak ada plate figuran.)*
- **Generate-order final-batch:** E16 master+jalur **sebelum** keyframe SC11.

---

## SH01 — Establishing kontras · WIDE · 28mm
**START attachments:** `E16_tamankota_master.png` (PENDING) + `R_ratna_hijab_front_full.png` + `A_andi_front_full.png`.
- **START** — mode **B** (full master, 2-subjek fg + crowd ambient) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E16_tamankota_master.png — same city park, same bench, same path, same layout, same handedness, faithful match"],
    "identity_reference": ["R_ratna_hijab_front_full.png — same identical woman, matched face, headscarf, early-forties", "A_andi_front_full.png — same identical boy, matched face, age ten"]
  },
  "mood": "warm golden late-afternoon, present-together calm against the scrolling crowd, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a city park late afternoon, golden light filtering through the trees, a bench of anonymous people heads down on their phones thumbs scrolling, a mother in a headscarf, her son, standing relaxed on the path",
  "location": "outdoor",
  "time_of_day": "evening",
  "atmosphere": "warm golden-hour light, dappled through trees, calm",
  "scene_depth": {
    "foreground": "path paving low frame",
    "midground": "Ratna, Andi standing relaxed on the path",
    "background": "a bench of soft anonymous figures heads down on phones, trees, golden light"
  },
  "subjects": [
    { "who": "Ratna", "identity_reference": "R_ratna_hijab_front_full.png" },
    { "who": "Andi", "identity_reference": "A_andi_front_full.png" }
  ],
  "subject_state": "static",
  "action": "Ratna, Andi standing relaxed on the path, a bench crowd heads down behind",
  "pose": "Ratna standing on the path camera-left, a single shopping bag in one hand, headscarf, Andi standing beside her camera-right, both paused, the background bench people seated heads down on their phones",
  "gesture": "Ratna relaxed holding the bag, Andi beginning a story, the background figures thumbs on their screens",
  "expression": "Ratna, Andi warm content, the background crowd absorbed in screens",
  "grooming": "Ratna neat headscarf, Andi short neat hair",
  "wardrobe": "Ratna headscarf, modest long-sleeve tunic, the shopping bag, Andi casual t-shirt, shorts",
  "framing": "wide establishing, the path, the two foreground figures, the bench crowd background, trees",
  "angle": "eye-level, facing the bench, the path, contrast in one frame",
  "camera": "28mm prime spherical, deep focus front to back",
  "lighting": "warm golden-hour sun filtering through the trees from camera-right, warm key, long soft dappled shadows, soft fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural golden-hour realism, warm directional sun, dappled soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian city park exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Andi mulai bercerita, Ratna menoleh tersenyum; scrollers tetap tertunduk; paused) · STATUS: ✅ authored:
```
Change only the two foreground figures, the background crowd held still heads-down.

- Andi: now mid-story, one hand in a small telling gesture, looking up at his mother
- Ratna: now turned toward Andi, a warm soft smile, listening
- unchanged: framing unchanged, camera angle unchanged, both standing positions on the path unchanged, the background bench crowd still heads-down on phones unchanged, trees unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH02 — Ratna & Andi (hadir untuk satu sama lain) · MEDIUM 2-shot · 50mm
**START attachments:** `E16_tamankota_jalur.png` (PENDING) + `R_ratna_hijab_front_medium.png` + `A_andi_front_medium.png`.
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E16_tamankota_jalur.png — same park path, same trees, faithful match"],
    "identity_reference": ["R_ratna_hijab_front_medium.png — same identical woman, matched face, headscarf, early-forties", "A_andi_front_medium.png — same identical boy, matched face, age ten"]
  },
  "mood": "warm present-together moment, a mother-son time, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a mother in a headscarf, her son, standing relaxed on a park path, golden afternoon light, trees behind",
  "location": "outdoor",
  "time_of_day": "evening",
  "atmosphere": "warm golden-hour light, dappled, calm",
  "scene_depth": {
    "foreground": "path low frame",
    "midground": "Ratna, Andi standing relaxed facing each other",
    "background": "soft trees, golden light"
  },
  "subjects": [
    { "who": "Ratna", "identity_reference": "R_ratna_hijab_front_medium.png" },
    { "who": "Andi", "identity_reference": "A_andi_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "Andi telling a story, Ratna listening, both paused on the path",
  "pose": "Ratna standing camera-left, the shopping bag in one hand, turned toward Andi, Andi standing camera-right looking up telling a story",
  "gesture": "Andi a lively telling gesture, Ratna a warm listening lean",
  "expression": "Andi animated happy, Ratna warm amused",
  "grooming": "Ratna neat headscarf, Andi short neat hair",
  "wardrobe": "Ratna headscarf, modest tunic, shopping bag, Andi casual t-shirt",
  "framing": "medium two-shot, Ratna head to waist camera-left, Andi head to chest camera-right",
  "angle": "eye-level, facing the two on the path",
  "camera": "50mm prime spherical, shallow depth of field, focus split on the two",
  "lighting": "warm golden-hour sun from camera-right, warm key, dappled soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural golden-hour realism, warm directional sun, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian city park exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: keduanya tertawa kecil; paused) · STATUS: ✅ authored:
```
Change only the expressions, positions held.

- Andi: now a wide laugh, delighted, eyes up at his mother
- Ratna: now a soft warm laugh, looking down at him
- unchanged: framing unchanged, camera angle unchanged, both standing positions on the path unchanged, trees unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH03 — Insert HP Andi (langkah harian) · CLOSE · 85mm
**START attachments:** `A_andi_front_medium.png` (tangan). **A1: layar slab polos; "8.000 langkah" = AE.**
- **START** — mode **B** (insert tangan+HP) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "identity_reference": ["A_andi_front_medium.png — same identical boy hand, matched young skin, t-shirt cuff"]
  },
  "mood": "a small proud check-in, a healthy day, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a child hand holding a smartphone, screen off dark neutral blank slab, warm golden-hour daylight",
  "location": "outdoor",
  "time_of_day": "evening",
  "atmosphere": "warm golden-hour light, soft",
  "scene_depth": {
    "foreground": "thumb at the phone edge",
    "midground": "smartphone in a small hand, screen off dark neutral, sharp",
    "background": "soft out-of-focus park, golden light"
  },
  "subjects": [ { "who": "Andi hand", "identity_reference": "A_andi_front_medium.png" } ],
  "subject_state": "static",
  "action": "a small hand holding the phone up, screen off, checking",
  "pose": "Andi small hand holding a smartphone upright, thumb at the lower edge",
  "gesture": "thumb at the screen edge, looking",
  "framing": "close-up insert, the small hand, the smartphone, screen frame-dominant",
  "angle": "downward onto the screen, eye-level lowered",
  "camera": "85mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "warm golden-hour daylight soft on the hand, even key, phone screen off dark neutral, faint warm reflection",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural golden-hour realism, warm soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian city park exterior realism"
}
```
- **END** — minimal-hold ("8.000 langkah hari ini" + ikon target = AE) · STATUS: ✅ authored:
```
Hold near-identical to START — the thumb stays at the screen edge, looking. The daily-steps summary "8.000 langkah hari ini" + target icon (fitness feature) = After Effects overlays on the plain slab. Keep frame, hand, screen slab, lighting, framing identical.
```

---

## SH04 — Andi nyengir tunjuk ibunya · MEDIUM 2-shot · 50mm
**START attachments:** `E16_tamankota_jalur.png` (PENDING) + `R_ratna_hijab_front_medium.png` + `A_andi_front_medium.png`.
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E16_tamankota_jalur.png — same park path, same trees, faithful match"],
    "identity_reference": ["R_ratna_hijab_front_medium.png — same identical woman, matched face, headscarf, early-forties", "A_andi_front_medium.png — same identical boy, matched face, age ten"]
  },
  "mood": "a proud little share, warm together, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a boy showing his phone to his mother on a park path, golden afternoon light",
  "location": "outdoor",
  "time_of_day": "evening",
  "atmosphere": "warm golden-hour light, dappled, calm",
  "scene_depth": {
    "foreground": "path low frame",
    "midground": "Andi holding the phone up toward Ratna, Ratna inclined to look",
    "background": "soft trees, golden light"
  },
  "subjects": [
    { "who": "Ratna", "identity_reference": "R_ratna_hijab_front_medium.png" },
    { "who": "Andi", "identity_reference": "A_andi_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "Andi holding the phone up toward his mother, about to share",
  "pose": "Andi standing camera-right holding the phone up toward Ratna, Ratna standing camera-left turned toward it, the shopping bag in her other hand",
  "gesture": "Andi presenting the phone, Ratna inclining to look",
  "expression": "Andi proud eager, Ratna warm attentive",
  "grooming": "Ratna neat headscarf, Andi short neat hair",
  "wardrobe": "Ratna headscarf, modest tunic, shopping bag, Andi casual t-shirt",
  "framing": "medium two-shot, Ratna head to waist camera-left, Andi head to chest camera-right, the phone between",
  "angle": "eye-level, facing the two on the path",
  "camera": "50mm prime spherical, shallow depth of field, focus on Andi",
  "lighting": "warm golden-hour sun from camera-right, warm key, dappled soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural golden-hour realism, warm directional sun, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian city park exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Ratna lihat layar + tersenyum, Andi nyengir) · STATUS: ✅ authored:
```
Change only the expressions, positions held.

- Ratna: now her eyes on the phone screen, a warm proud smile
- Andi: a wide proud grin up at her
- unchanged: framing unchanged, camera angle unchanged, both standing positions unchanged, the phone position unchanged, trees unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH05 — Ponsel dikantongi, kembali bercerita (tesis) · WIDE 2-shot · 35mm
**START attachments:** `E16_tamankota_master.png` (PENDING) + `R_ratna_hijab_front_full.png` + `A_andi_front_full.png`. **No traverse keluar frame; latar scrollers kontras.**
- **START** — mode **B** (full master, 2-subjek + crowd ambient) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E16_tamankota_master.png — same city park, same bench, same path, faithful match"],
    "identity_reference": ["R_ratna_hijab_front_full.png — same identical woman, matched face, headscarf, early-forties", "A_andi_front_full.png — same identical boy, matched face, age ten"]
  },
  "mood": "the thesis landing, technology as a tool put away, warm gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a mother, son, on a park path putting a phone away, a bench of anonymous people still heads down on screens behind, warm golden afternoon",
  "location": "outdoor",
  "time_of_day": "evening",
  "atmosphere": "warm golden-hour light, dappled, calm contrast",
  "scene_depth": {
    "foreground": "path paving low frame",
    "midground": "Ratna, Andi standing on the path, the phone going into a pocket",
    "background": "the bench crowd still heads down on phones, trees, golden light"
  },
  "subjects": [
    { "who": "Ratna", "identity_reference": "R_ratna_hijab_front_full.png" },
    { "who": "Andi", "identity_reference": "A_andi_front_full.png" }
  ],
  "subject_state": "static",
  "action": "Andi slipping the phone into his pocket, Ratna beside him, the bench crowd heads down behind",
  "pose": "Andi standing camera-right, one hand slipping the phone into his shorts pocket, Ratna standing camera-left holding the shopping bag, the background bench people seated heads down on phones",
  "gesture": "Andi pocketing the phone, Ratna relaxed, the background figures on their screens",
  "expression": "Ratna, Andi warm content, the background crowd absorbed",
  "grooming": "Ratna neat headscarf, Andi short neat hair",
  "wardrobe": "Ratna headscarf, modest tunic, shopping bag, Andi casual t-shirt, shorts",
  "framing": "wide two-shot, Ratna, Andi full on the path, the bench crowd background",
  "angle": "eye-level, facing the path, the bench behind",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "warm golden-hour sun filtering through the trees, warm key, long soft dappled shadows",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural golden-hour realism, warm directional sun, dappled soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian city park exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: keduanya berpaling melanjutkan satu langkah, ponsel sudah tak di tangan; tetap di frame, no traverse) · STATUS: ✅ authored:
```
Change only the two foreground figures, the background crowd held still heads-down.

- Andi: the phone now away in his pocket, both hands free, turned back toward his mother resuming the story, one foot a small step forward, still fully in frame
- Ratna: turned alongside him, a warm smile, resuming the walk in place, still fully in frame
- unchanged: framing unchanged, camera angle unchanged, both still within the same frame positions, the background bench crowd still heads-down on phones unchanged, trees unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## Status board
| Shot | START | END | Render |
|---|---|---|---|
| SH01 | ✅ authored | ✅ authored | pending (final batch) |
| SH02 | ✅ authored | ✅ authored | pending (final batch) |
| SH03 | ✅ authored | ✅ hold (AE steps) | pending (final batch) |
| SH04 | ✅ authored | ✅ authored | pending (final batch) |
| SH05 | ✅ authored | ✅ authored | pending (final batch) |

**Ladder:** W→M→CU→M→W. **Grade sore keemasan golden-hour** (GATE B). **Camera-lock:** scene lokomosi → **beat-jeda** (subjek paused, no traverse out of frame); latar scroller = ambient soft, tak face-locked, heads-down held. **A1:** SH03 screen OFF/polos (langkah harian = AE). **Tech-as-tool** tesis (HP dikantongi). **Modesty:** Ratna berhijab (taman publik); Andi uncovered (mahram). **⚠ PENDING plates:** `E16_tamankota_{master,jalur}`. **Penutup SEQ4.**
