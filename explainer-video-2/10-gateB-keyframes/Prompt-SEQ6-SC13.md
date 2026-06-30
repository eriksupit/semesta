---
title: GATE B Prompt — SEQ6-SC13 (INT. RUANG MAKAN — 19.00) · FINALE
tags: [explainer-video-2, gate-b, prompt, status, SEQ6-SC13, finale]
status: authoring
created: 2026-07-01
updated: 2026-07-01
aliases: [ev2-prompt-seq6-sc13]
---

# GATE B Prompt — SEQ6-SC13 · FINALE
## INT. RUANG MAKAN — 19.00 WIB *(SCENE TERAKHIR film)*

> **Konvensi dua-doc:** prompt GATE B + status. Narasi = `SEQ6-SC13.md`. Env = `E06_ruangmakan` (**master JADI** ✓; **MEJA DROPPED** → SH02/SH04 frame-M di-stage off the master).
> **Pola seragam (SC01–SC12):** START full-prompt + attachment → END edit-in-place. Camera-lock: keluarga duduk (stasioner natural), delta gestur/ekspresi in-frame; 4-subjek hanya WIDE. Device screen OFF/polos (A1: "Mode Syariah · aktif" + redup = AE, **grafis komersial TERAKHIR film**; sejak SH04 nol grafis). Grade **hangat malam** (GATE B — pendant ON + jendela malam gelap). **Ratna uncovered** (mahram-only malam). Hidangan **tak dilabeli**. Azan Isya (audio). **FINALE — gambar terakhir = kehangatan keluarga (bukan ponsel).**

## Manifest attachment (semua di disk ✓)
- **Env E06:** `E06_ruangmakan_master.png` (establishing WIDE + finale; MEJA dropped → M-frame off master).
- **Karakter:** `H_herman_front_{full,medium}` · `R_ratna_front_{full,medium}` (uncovered) · `L_lisa_front_full` · `A_andi_front_full`.
- **Tanpa PENDING plate** — SC13 siap di-generate.

---

## SH01 — Establishing: keluarga di meja makan · WIDE 4-subjek · 24mm
**START attachments:** `E06_ruangmakan_master.png` + `H_herman_front_full.png` + `R_ratna_front_full.png` + `L_lisa_front_full.png` + `A_andi_front_full.png`. ⚠ shot tersulit (4-subjek).
- **START** — mode **B** (full master, 4-subjek WIDE) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E06_ruangmakan_master.png — same family dining room, same EKEDALEN table, same HAVSTA sideboard, same layout, same handedness, faithful match"],
    "identity_reference": ["H_herman_front_full.png — same identical man, matched face, clean-shaven, mid-forties", "R_ratna_front_full.png — same identical woman, matched face, uncovered hair visible, early-forties", "L_lisa_front_full.png — same identical young woman, matched face, uncovered hair, early-twenties", "A_andi_front_full.png — same identical boy, matched face, age ten"]
  },
  "mood": "warm intimate family night, a full table, the day come home, tender register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a family dining room at night, a warm pendant lamp glowing over the table, dark night window, four family members around the EKEDALEN table, steaming dishes at the centre, plates being passed, a HAVSTA sideboard behind",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "warm lamp-lit night, dark window, intimate hush",
  "scene_depth": {
    "foreground": "near table edge, a plate low frame",
    "midground": "Herman, Ratna, Lisa, Andi seated around the table, steaming dishes at the centre",
    "background": "the sideboard, plain plaster back wall, dark night window camera-left"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_full.png" },
    { "who": "Ratna", "identity_reference": "R_ratna_front_full.png" },
    { "who": "Lisa", "identity_reference": "L_lisa_front_full.png" },
    { "who": "Andi", "identity_reference": "A_andi_front_full.png" }
  ],
  "subject_state": "static",
  "action": "the family seated around the table, dishes steaming, a plate passing hands",
  "pose": "Herman seated at the head camera-right, Ratna seated camera-left, Lisa, Andi seated along the sides, one plate held mid-pass between two of them, all settled at the table",
  "gesture": "hands at plates, one plate passing, easy together",
  "expression": "all warm, content, at ease",
  "grooming": "Herman neat short hair, Ratna loose uncovered hair, Lisa loose hair, Andi short hair",
  "wardrobe": "relaxed modest home clothes, long sleeves, plain",
  "framing": "wide establishing, the full table, four seated figures, the warm pendant overhead, the dishes centre",
  "angle": "eye-level slight high angle, from the end of the table over the dishes",
  "camera": "24mm prime spherical, deep focus front to back",
  "lighting": "warm pendant lamp key over the table centre, warm wrap on the four faces, deep warm falloff to the room, dark cool night window camera-left, cosy warm-cool balance",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, warm practical lamp, deep honest shadow",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat family grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: keluarga menata/menerima piring, mengobrol; 4 duduk stasioner) · STATUS: ✅ authored:
```
Change only the gestures and expressions, all four seated positions held.

- the family: the passed plate now received and set down, two of them mid-chat, soft smiles around the table, easy warmth
- unchanged: framing unchanged, camera angle unchanged, all four seated positions unchanged, the table unchanged, dishes unchanged, pendant lamp unchanged, window unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH02 — Herman aktifkan opt-in syariah · MEDIUM · 50mm
**START attachments:** `E06_ruangmakan_master.png` (env lock; MEJA dropped → M-frame off master) + `H_herman_front_medium.png`.
- **START** — mode **B** (full master, 1-subjek; keluarga soft) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E06_ruangmakan_master.png — same dining room, same table, same warm night, faithful match, medium framing on Herman at the table"],
    "identity_reference": ["H_herman_front_medium.png — same identical man, matched face, clean-shaven, mid-forties"]
  },
  "mood": "a quiet threshold, the call to prayer near, tender register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a man at the family dinner table at night, a smartphone in his hand, warm pendant light, family soft around him",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "warm lamp-lit night, intimate",
  "scene_depth": {
    "foreground": "table edge, a dish low frame",
    "midground": "Herman seated holding a smartphone, plain slab screen",
    "background": "family soft around the table, sideboard, dark window"
  },
  "subjects": [ { "who": "Herman", "identity_reference": "H_herman_front_medium.png" } ],
  "subject_state": "static",
  "action": "Herman at the table holding the phone, the call to prayer beginning",
  "pose": "Herman seated at the table, a smartphone held up in one hand, the other resting on the table, family soft around him",
  "gesture": "Herman holding the phone, attention on the screen",
  "expression": "calm reverent, a small pause",
  "grooming": "neat short hair, clean-shaven",
  "wardrobe": "relaxed modest home shirt",
  "framing": "medium shot, Herman head to chest at the table, family soft behind",
  "angle": "eye-level, facing Herman at the table",
  "camera": "50mm prime spherical, shallow depth of field, focus on Herman",
  "lighting": "warm pendant lamp key from above, warm wrap, plain neutral phone glow on his face, dark window behind",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, warm practical lamp, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Herman mengetuk satu pilihan di layar) · STATUS: ✅ authored:
```
Change only Herman thumb gesture, position held.

- Herman: now his thumb pressed to the phone screen, a single tap selecting an option, eyes calm on the screen
- unchanged: framing unchanged, camera angle unchanged, Herman seated position unchanged, phone position unchanged, family soft behind unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH03 — Insert HP (mode syariah → app meredup) · CLOSE · 85mm
**START attachments:** `H_herman_front_medium.png` (tangan). **A1: layar slab polos; "Mode Syariah · aktif" + redup = AE — grafis komersial TERAKHIR film.**
- **START** — mode **B** (insert tangan+HP) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "identity_reference": ["H_herman_front_medium.png — same identical man hand, matched skin tone, sleeve cuff"]
  },
  "mood": "technology giving way, a sacred quiet beginning, tender register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a hand holding a smartphone at the dinner table, screen off dark neutral blank slab, warm pendant night light",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "warm lamp-lit night, soft",
  "scene_depth": {
    "foreground": "thumb at the phone edge",
    "midground": "smartphone in hand, screen off dark neutral, sharp",
    "background": "soft out-of-focus warm table, dishes"
  },
  "subjects": [ { "who": "Herman hand", "identity_reference": "H_herman_front_medium.png" } ],
  "subject_state": "static",
  "action": "a hand holding the phone, a choice selected, screen off",
  "pose": "Herman hand holding the smartphone upright, thumb at the lower screen",
  "gesture": "thumb at the screen, settling",
  "framing": "close-up insert, the hand, the smartphone, screen frame-dominant",
  "angle": "downward onto the screen, eye-level lowered",
  "camera": "85mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "warm pendant night light soft on the hand, even key, phone screen off dark neutral, faint warm reflection",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, warm soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity"
}
```
- **END** — minimal-hold (Mode Syariah → app meredup = AE; grafis komersial TERAKHIR) · STATUS: ✅ authored:
```
Hold near-identical to START — the thumb settles. The "Mode Syariah · aktif" opt-in choice, then the app display dimming calm = After Effects on the plain slab — the film's LAST commercial graphic. From the next shot on, zero graphics (Bersih Saat Sakral). Keep frame, hand, screen slab, lighting, framing identical.
```

---

## SH04 — Herman telungkupkan ponsel (app diam) · MEDIUM · 50mm
**START attachments:** `E06_ruangmakan_master.png` (env lock; M-frame off master) + `H_herman_front_medium.png`.
- **START** — mode **B** (full master, 1-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E06_ruangmakan_master.png — same dining room, same table, same warm night, faithful match, medium framing on Herman at the table"],
    "identity_reference": ["H_herman_front_medium.png — same identical man, matched face, clean-shaven, mid-forties"]
  },
  "mood": "technology set aside, family first, warm tender register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a man at the family dinner table at night about to set his phone down, warm pendant light, family soft around",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "warm lamp-lit night, intimate",
  "scene_depth": {
    "foreground": "table edge, a dish low frame",
    "midground": "Herman seated, the phone in hand near the table",
    "background": "family soft around the table, sideboard, dark window"
  },
  "subjects": [ { "who": "Herman", "identity_reference": "H_herman_front_medium.png" } ],
  "subject_state": "static",
  "action": "Herman lowering the phone toward the table, about to set it down",
  "pose": "Herman seated at the table, the smartphone in one hand lowering toward the table surface, head beginning to lift toward the family",
  "gesture": "the phone lowering to the table, attention leaving the screen",
  "expression": "calm content, returning to the room",
  "grooming": "neat short hair, clean-shaven",
  "wardrobe": "relaxed modest home shirt",
  "framing": "medium shot, Herman head to chest at the table, the table surface, family soft behind",
  "angle": "eye-level, facing Herman at the table",
  "camera": "50mm prime spherical, shallow depth of field, focus on Herman",
  "lighting": "warm pendant lamp key from above, warm wrap, dark window behind, soft warm fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, warm practical lamp, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Herman telungkupkan ponsel di meja, menoleh ke keluarga; app diam) · STATUS: ✅ authored:
```
Change only Herman gesture and gaze, position held.

- Herman: now the phone laid face-down flat on the table, his hand off it, his head turned toward the family, a warm smile
- unchanged: framing unchanged, camera angle unchanged, Herman seated position unchanged, the table unchanged, family soft behind unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH05 — FINALE: kehangatan keluarga · WIDE 4-subjek · 28mm
**START attachments:** `E06_ruangmakan_master.png` + `H_herman_front_full.png` + `R_ratna_front_full.png` + `L_lisa_front_full.png` + `A_andi_front_full.png`. **Gambar terakhir film = keluarga (bukan ponsel).** ⚠ 4-subjek.
- **START** — mode **B** (full master, 4-subjek WIDE) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E06_ruangmakan_master.png — same family dining room, same EKEDALEN table, same warm night, faithful match"],
    "identity_reference": ["H_herman_front_full.png — same identical man, matched face, clean-shaven, mid-forties", "R_ratna_front_full.png — same identical woman, matched face, uncovered hair visible, early-forties", "L_lisa_front_full.png — same identical young woman, matched face, uncovered hair, early-twenties", "A_andi_front_full.png — same identical boy, matched face, age ten"]
  },
  "mood": "the day come home, family warmth above all, tender final register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a family dining room at night, four family members around the table chatting, a smartphone lying face-down on the table off to the side, a warm pendant lamp, dark night window, steaming dishes",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "warm lamp-lit night, intimate, the phone forgotten on the table",
  "scene_depth": {
    "foreground": "table edge, the face-down phone off to one side low frame",
    "midground": "Herman, Ratna, Lisa, Andi seated chatting around the table",
    "background": "the sideboard, plain plaster wall, dark night window camera-left"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_full.png" },
    { "who": "Ratna", "identity_reference": "R_ratna_front_full.png" },
    { "who": "Lisa", "identity_reference": "L_lisa_front_full.png" },
    { "who": "Andi", "identity_reference": "A_andi_front_full.png" }
  ],
  "subject_state": "static",
  "action": "the family chatting around the table, the phone face-down off to the side",
  "pose": "Herman at the head camera-right turned to the family, Ratna camera-left, Lisa, Andi along the sides, all leaned a little toward each other in talk, the smartphone face-down on the table off to one side",
  "gesture": "easy talking hands, warmth around the table, the phone untouched",
  "expression": "all warm, smiling, together",
  "grooming": "Herman neat short hair, Ratna loose uncovered hair, Lisa loose hair, Andi short hair",
  "wardrobe": "relaxed modest home clothes, long sleeves, plain",
  "framing": "wide finale, the full table, four seated figures together, the warm pendant overhead, the dishes centre, the face-down phone a small detail",
  "angle": "eye-level slight high angle, from the end of the table",
  "camera": "28mm prime spherical, deep focus front to back",
  "lighting": "warm pendant lamp key over the table centre, warm wrap on the four faces, deep warm falloff, dark cool night window camera-left, cosy warm-cool balance",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, warm practical lamp, deep honest shadow",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat family grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: keluarga tertawa kecil bersama, hangat; gambar terakhir = keluarga) · STATUS: ✅ authored:
```
Change only the expressions, all four seated positions held, the phone face-down untouched.

- the family: now a shared soft laugh around the table, warm faces turned to each other, the day come home, the phone face-down forgotten on the table
- unchanged: framing unchanged, camera angle unchanged, all four seated positions unchanged, the table unchanged, the face-down phone position unchanged, pendant lamp unchanged, window unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## Status board
| Shot | START | END | Render |
|---|---|---|---|
| SH01 | ✅ authored | ✅ authored | pending (final batch) |
| SH02 | ✅ authored | ✅ authored | pending (final batch) |
| SH03 | ✅ authored | ✅ hold (AE syariah/dim) | pending (final batch) |
| SH04 | ✅ authored | ✅ authored | pending (final batch) |
| SH05 | ✅ authored | ✅ authored | pending (final batch) |

**Ladder:** W→M→CU→M→W. **Grade hangat malam** (GATE B — pendant ON + jendela malam). **Camera-lock:** keluarga duduk stasioner, delta gestur/ekspresi in-frame; 4-subjek hanya WIDE (SH01/SH05). **A1:** HP = slab polos ("Mode Syariah · aktif" + redup = AE, **grafis komersial TERAKHIR film**; sejak SH04 nol grafis). **Modesty:** Ratna uncovered (mahram-only malam). Hidangan tak dilabeli. **MEJA dropped** → SH02/SH04 M-frame off master. **★ FINALE — gambar terakhir = kehangatan keluarga (bukan ponsel).** Plates E06 master + 4 family semua di disk — SC13 siap generate. ⚠ 4-subjek WIDE = shot tersulit (staging hati-hati saat generate).
