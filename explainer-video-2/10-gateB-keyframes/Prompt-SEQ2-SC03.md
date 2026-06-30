---
title: GATE B Prompt — SEQ2-SC03 (EXT. GERBANG KOMPLEKS — 06.45)
tags: [explainer-video-2, gate-b, prompt, status, SEQ2-SC03]
status: authoring
created: 2026-07-01
updated: 2026-07-01
aliases: [ev2-prompt-seq2-sc03]
---

# GATE B Prompt — SEQ2-SC03
## EXT. GERBANG KOMPLEKS — 06.45 WIB

> **Konvensi dua-doc:** doc ini = prompt GATE B + status. Narasi = `SEQ2-SC03.md`. Cerita = `03` SEQ2-SC03. Env = `09-environment-sheet/E07-gerbangwarung.md`.
> **Pola seragam (sama SC01/SC02):** START = master full-prompt + attachment → END = edit-in-place (NOL preamble; operasi+delta+lock-list). Camera-lock: angle+framing identik, delta subjek-saja in-frame (Lisa stasioner, NO transit/traverse). Device screen OFF/polos (A1: notif/konfirmasi = AE). Grade **pagi hangat** (warm = GATE B, plate-nya netral). Audit `/tti-prompt-audit` per START.

## Manifest attachment
- **Env E07 (⚠ PENDING final-batch generate):** `E07_gerbangwarung_master.png` (gerbang+warung+pos+mango) · `E07_gerbangwarung_warung.png` (warung-front MS) · `E07_gerbangwarung_gerbang.png` (gate-mouth WIDE).
- **Karakter:** `F_darto_front_{full,medium}` (di disk ✓) · `L_lisa_front_full` (✓) · `F_ojek_front_full` (⚠ PENDING — figuran F6, belum di-generate).
- **Generate-order final-batch:** E07 master→warung→gerbang + F_ojek plate **sebelum** keyframe SC03.

---

## SH01 — Establishing gerbang · WIDE · 28mm
**START attachments:** `E07_gerbangwarung_master.png` (PENDING) + `F_darto_front_full.png`.
- **START** — mode **B** (full master, 1-subjek + ruang) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E07_gerbangwarung_master.png — same complex gate entrance, same guard post, same kelontong warung, same layout, same handedness, faithful street match"],
    "identity_reference": ["F_darto_front_full.png — same identical warung vendor man, matched face, middle-aged, distinctive features"]
  },
  "mood": "bright lived-in morning street, neighbourly everyday calm, warm ordinary register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "residential complex gate entrance morning, steel boom-gate barrier centre, painted concrete guard post camera-left, kelontong warung beside it, paving-block road receding in, mango tree camera-right, warm low morning sun",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "warm early-morning light, long soft shadows, quiet street",
  "scene_depth": {
    "foreground": "open paving forecourt low frame",
    "midground": "Darto at the warung front camera-left, goods set out, mid-arrangement",
    "background": "boom gate centre, paving road receding into the complex, mango tree camera-right"
  },
  "subjects": [ { "who": "Darto", "identity_reference": "F_darto_front_full.png" } ],
  "subject_state": "static",
  "action": "Darto at his warung front, goods set out on the display table, mid-arrangement",
  "pose": "Darto standing camera-left at the warung display table, torso angled slightly toward the goods, one hand resting on a stack of snack sachets",
  "gesture": "one hand on the goods, the other at his side",
  "expression": "calm everyday morning focus, faint content half-smile",
  "grooming": "middle-aged neat short hair, plain working vendor look",
  "wardrobe": "plain short-sleeve collared shirt, dark trousers, simple sandals",
  "framing": "wide establishing, full gate entrance, Darto small at the warung camera-left, road receding",
  "angle": "eye-level slight low angle, from outside the gate facing in",
  "camera": "28mm prime spherical, deep focus front to back",
  "lighting": "warm low morning sun raking from camera-right, long soft shadows across the paving, warm golden key, soft sky fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural daylight realism, warm directional sun, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class housing-complex exterior realism, lived-in street",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Darto selesai menata, berdiri tegak di warung) · STATUS: ✅ authored:
```
Change only Darto pose: he finishes arranging and stands.

- pose: Darto now standing upright at the warung front, both hands lowered at his sides, settled, surveying the goods, calm
- unchanged: framing unchanged, camera angle unchanged, Darto standing position unchanged, warung unchanged, gate unchanged, mango tree unchanged, lighting unchanged, color grade unchanged, face matching attached plate F_darto_front_full
```

---

## SH02 — Darto cek pesanan · MEDIUM · 50mm
**START attachments:** `E07_gerbangwarung_warung.png` (PENDING) + `F_darto_front_medium.png`.
- **START** — mode **B** (full master, 1-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E07_gerbangwarung_warung.png — same warung front, same guard post, same display case, faithful match"],
    "identity_reference": ["F_darto_front_medium.png — same identical vendor man, matched face, middle-aged"]
  },
  "mood": "bright lived-in morning street, neighbourly everyday calm, warm ordinary register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "kelontong warung front morning, glass display case, hung snack sachet strips, vendor at the stall, warm low morning sun",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "warm early-morning light, soft long shadows",
  "scene_depth": {
    "foreground": "warung display table edge low frame",
    "midground": "Darto at the stall, a smartphone in his hand",
    "background": "guard post, hung sachets, soft daylight"
  },
  "subjects": [ { "who": "Darto", "identity_reference": "F_darto_front_medium.png" } ],
  "subject_state": "static",
  "action": "Darto at the stall, a smartphone just lifted in one hand",
  "pose": "Darto standing at the warung front, one hand holding a smartphone up at chest height, head tilted toward it, other hand on the display table",
  "gesture": "fingers around the phone, attention on the screen",
  "expression": "morning calm shifting to a faint pleased smile",
  "grooming": "middle-aged neat short hair",
  "wardrobe": "plain short-sleeve collared shirt, dark trousers",
  "framing": "medium shot, Darto head to waist, warung display behind",
  "angle": "eye-level, facing Darto at the stall",
  "camera": "50mm prime spherical, shallow depth of field, focus on Darto",
  "lighting": "warm low morning sun from camera-right, warm key on his face, soft shadow side, soft sky fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural daylight realism, warm directional sun, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class housing-complex exterior realism, lived-in street",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Darto menatap layar, tersenyum) · STATUS: ✅ authored:
```
Change only Darto attention and expression.

- pose: Darto now holding the phone steady before his face, both eyes on the screen, head lowered toward it
- expression: a warm pleased smile, a good order arrived, content
- unchanged: framing unchanged, camera angle unchanged, Darto standing position unchanged, warung unchanged, lighting unchanged, color grade unchanged, face matching attached plate F_darto_front_medium
```

---

## SH03 — Insert HP Darto (notif pesanan) · CLOSE · 85mm
**START attachments:** `E07_gerbangwarung_warung.png` (latar, PENDING) + `F_darto_front_medium.png` (tangan/identitas).
- **START** — mode **B** (insert tangan+HP) · STATUS: ✅ authored. **A1: layar OFF/polos; notif "Pesanan baru masuk" = AE.**
```json
{
  "attachment_manifest": {
    "environment_reference": ["E07_gerbangwarung_warung.png — same warung front background, soft, faithful match"],
    "identity_reference": ["F_darto_front_medium.png — same identical vendor man, matched hand, matched skin tone"]
  },
  "mood": "bright lived-in morning street, a small good-news moment, warm ordinary register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a vendor hand holding a smartphone, screen off dark neutral blank slab, warm morning daylight, soft warung background",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "warm morning daylight, soft",
  "scene_depth": {
    "foreground": "fingertips at the phone edge",
    "midground": "smartphone in hand, screen off dark neutral, sharp",
    "background": "soft out-of-focus warung front, warm daylight"
  },
  "subjects": [ { "who": "Darto hand", "identity_reference": "F_darto_front_medium.png" } ],
  "subject_state": "static",
  "action": "a hand holding the smartphone up, screen off, waiting",
  "pose": "Darto warm brown Southeast-Asian hand holding a smartphone upright, fingers around the body, thumb resting at the lower bezel",
  "gesture": "thumb at the lower edge, ready",
  "framing": "close-up insert, the hand, the smartphone, screen frame-dominant",
  "angle": "over-shoulder downward onto the screen, eye-level lowered",
  "camera": "85mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "warm morning daylight soft on the hand, even soft key, phone screen off dark neutral, faint warm reflection on the glass",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural daylight realism, warm soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class exterior realism"
}
```
- **END** — EDIT-IN-PLACE (delta: jempol Darto menyentuh layar cek) · STATUS: ✅ authored:
```
Change only the thumb: Darto taps the screen.

- pose: Darto thumb now pressed onto the lower portion of the phone screen, a single tap contact, the rest of the hand steady
- unchanged: framing unchanged, camera angle unchanged, hand position unchanged, phone position unchanged, screen off dark neutral unchanged, background unchanged, lighting unchanged, color grade unchanged
```

---

## SH04 — Lisa menyapa Darto · MEDIUM 2-shot · 50mm
**START attachments:** `E07_gerbangwarung_master.png` (jalan masuk, PENDING) + `L_lisa_front_full.png` + `F_darto_front_medium.png`.
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored. **Lisa stasioner (no transit).**
```json
{
  "attachment_manifest": {
    "environment_reference": ["E07_gerbangwarung_master.png — same gate entry road, same warung, same layout, same handedness, faithful match"],
    "identity_reference": ["L_lisa_front_full.png — same identical young woman, matched face, uncovered loose hair, early-twenties", "F_darto_front_medium.png — same identical vendor man, matched face, middle-aged"]
  },
  "mood": "bright lived-in morning street, warm neighbourly exchange, everyday register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "complex gate entry road morning, kelontong warung camera-left, a young woman paused at the stall greeting the vendor, warm low morning sun",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "warm early-morning light, long soft shadows",
  "scene_depth": {
    "foreground": "paving road low frame",
    "midground": "Lisa standing foreground camera-right facing the warung, Darto at the stall camera-left",
    "background": "boom gate, mango tree, paving road"
  },
  "subjects": [
    { "who": "Lisa", "identity_reference": "L_lisa_front_full.png" },
    { "who": "Darto", "identity_reference": "F_darto_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "Lisa paused at the warung greeting Darto, Darto at the stall",
  "pose": "Lisa standing camera-right foreground, turned toward the warung camera-left, a small shoulder bag on her shoulder, Darto standing at the stall camera-left facing her",
  "gesture": "Lisa a light greeting nod, Darto a returned nod",
  "expression": "Lisa friendly fresh morning smile, Darto warm neighbourly smile",
  "grooming": "Lisa loose uncovered hair, light natural, Darto neat short hair",
  "wardrobe": "Lisa modest casual long-sleeve top, jeans, small shoulder bag, Darto plain collared shirt",
  "framing": "medium two-shot, Lisa head to thigh camera-right, Darto head to waist camera-left",
  "angle": "eye-level, from the entry road side, both figures",
  "camera": "50mm prime spherical, shallow depth of field, focus on Lisa",
  "lighting": "warm low morning sun from camera-right, warm key across both, soft shadows, soft sky fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural daylight realism, warm directional sun, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class housing-complex exterior realism, lived-in street",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Lisa angkat HP buka app, Darto balas sapa; posisi tetap) · STATUS: ✅ authored:
```
Change only the gestures, positions unchanged.

- Lisa: now holding her smartphone up at chest height in one hand, eyes shifting down to the screen, opening the app
- Darto: a warm returned wave, hand raised in greeting
- unchanged: framing unchanged, camera angle unchanged, both standing positions unchanged, warung unchanged, gate unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH05 — Ojek menunggu di gerbang · WIDE · 35mm
**START attachments:** `E07_gerbangwarung_gerbang.png` (angle portal, PENDING) + `L_lisa_front_full.png` + `F_ojek_front_full.png` *(⚠ PENDING — figuran F6)*.
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored. **Lisa+ojek stasioner (no traverse).**
```json
{
  "attachment_manifest": {
    "environment_reference": ["E07_gerbangwarung_gerbang.png — same gate mouth, same open forecourt, same boom gate, faithful match"],
    "identity_reference": ["L_lisa_front_full.png — same identical young woman, matched face, uncovered loose hair, early-twenties", "F_ojek_front_full.png — same identical motorbike-taxi rider man, matched face, helmet, riding jacket"]
  },
  "mood": "bright lived-in morning street, a ride arriving, everyday register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "complex gate mouth morning, open paving forecourt, a motorbike-taxi rider waiting on his motorcycle near the portal, a young woman standing near the boom gate, warm low morning sun",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "warm early-morning light, long soft shadows",
  "scene_depth": {
    "foreground": "open forecourt paving low frame",
    "midground": "Lisa standing near the boom gate camera-left, the rider on his motorcycle camera-right",
    "background": "gate mouth, paving road through the gate, mango tree"
  },
  "subjects": [
    { "who": "Lisa", "identity_reference": "L_lisa_front_full.png" },
    { "who": "ojek rider", "identity_reference": "F_ojek_front_full.png" }
  ],
  "subject_state": "static",
  "action": "the rider waiting astride his motorcycle, Lisa standing near the gate checking her phone",
  "pose": "Lisa standing camera-left near the boom gate, smartphone held up in one hand, eyes on the screen, the rider seated astride a parked motorcycle camera-right, feet down, waiting",
  "gesture": "Lisa eyes on the confirmation screen, the rider steady on the bike",
  "expression": "Lisa reading, calm, the rider patient neutral",
  "grooming": "Lisa loose uncovered hair, the rider in a helmet",
  "wardrobe": "Lisa modest casual long-sleeve top, jeans, shoulder bag, the rider riding jacket, helmet, on a plain motorcycle",
  "framing": "wide shot, Lisa full height camera-left, the rider on the motorcycle camera-right, gate mouth around them",
  "angle": "eye-level, near the portal, both figures, gate beyond",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "warm low morning sun from camera-right, long soft shadows across the forecourt, warm key, soft sky fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural daylight realism, warm directional sun, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class housing-complex exterior realism, lived-in street",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Lisa menoleh + angkat tangan/angguk mengenali ojek; gestur in-frame, no traverse) · STATUS: ✅ authored:
```
Change only Lisa gesture: she recognizes the rider.

- Lisa: now turned toward the rider camera-right, one hand raised in a small acknowledging wave, a recognizing nod, phone lowered to her side
- unchanged: framing unchanged, camera angle unchanged, Lisa standing position unchanged, the rider and motorcycle unchanged, gate unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## Status board
| Shot | START | END | Render |
|---|---|---|---|
| SH01 | ✅ authored | ✅ authored | pending (final batch) |
| SH02 | ✅ authored | ✅ authored | pending (final batch) |
| SH03 | ✅ authored | ✅ authored | pending (final batch) |
| SH04 | ✅ authored | ✅ authored | pending (final batch) |
| SH05 | ✅ authored | ✅ authored | pending (final batch) |

**Ladder:** W→M→CU→M→W. **Grade pagi hangat** (warm = GATE B). **Camera-lock:** Lisa stasioner SH04/SH05 (delta gestur in-frame, no transit/traverse). **A1:** SH03 screen OFF/polos (notif=AE). **⚠ PENDING plates (final-batch, generate BEFORE keyframes):** `E07_gerbangwarung_{master,warung,gerbang}` + `F_ojek_front_full` (figuran F6).
