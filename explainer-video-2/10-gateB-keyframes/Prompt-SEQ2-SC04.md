---
title: GATE B Prompt — SEQ2-SC04 (EXT/INT. RUMAH RATNA — 07.30)
tags: [explainer-video-2, gate-b, prompt, status, SEQ2-SC04]
status: authoring
created: 2026-07-01
updated: 2026-07-01
aliases: [ev2-prompt-seq2-sc04]
---

# GATE B Prompt — SEQ2-SC04
## EXT/INT. RUMAH RATNA — 07.30 WIB

> **Konvensi dua-doc:** prompt GATE B + status. Narasi = `SEQ2-SC04.md`. Env = `E15-depanrumah.md`. Figuran `F7 kurir`.
> **Pola seragam (SC01–SC03):** START full-prompt + attachment → END edit-in-place (operasi+delta+lock-list). Camera-lock: angle+framing identik, delta subjek-saja; **3-subjek hanya di WIDE**; Ratna NO pop-in (hadir START); **mobil TIDAK melaju keluar** (SH05). Device screen OFF/polos (A1: daftar/"Dijemput"=AE). Grade **pagi hangat** (GATE B). **Ratna berhijab+celemek** (kurir non-mahram).

## Manifest attachment
- **Env E15 (⚠ PENDING final-batch):** `E15_depanrumah_master.png` (depan rumah + ruang mobil-boks) · `E15_depanrumah_pintu.png` (ambang pintu, glimpse dapur).
- **Karakter:** `R_ratna_hijab_front_{full,medium}` (di disk ✓) · `F_kurir_front_{full,medium}` (⚠ PENDING — figuran F7).
- **Generate-order final-batch:** E15 master+pintu + F_kurir plate **sebelum** keyframe SC04.

---

## SH01 — Establishing depan rumah · WIDE · 28mm
**START attachments:** `E15_depanrumah_master.png` (PENDING) + `F_kurir_front_full.png` (PENDING) + `R_ratna_hijab_front_full.png`.
- **START** — mode **B** (full master, 3-subjek WIDE) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E15_depanrumah_master.png — same house front, same yard, same door, same layout, same handedness, faithful match"],
    "identity_reference": ["R_ratna_hijab_front_full.png — same identical woman, matched face, headscarf, early-forties", "F_kurir_front_full.png — same identical courier man, matched face, uniform cap"]
  },
  "mood": "busy lived-in working morning, small-business dispatch, warm ordinary register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "front of a modest middle-class house morning, a parked box delivery van at the curb rear doors open, open house doorway, cardboard parcels, warm low morning sun",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "warm early-morning light, long soft shadows, working bustle",
  "scene_depth": {
    "foreground": "curb paving, cardboard parcels low frame",
    "midground": "a courier standing by the parcels camera-right, the box van rear open camera-right",
    "background": "the house front, open doorway, Ratna at the threshold camera-left"
  },
  "subjects": [
    { "who": "Ratna", "identity_reference": "R_ratna_hijab_front_full.png" },
    { "who": "courier", "identity_reference": "F_kurir_front_full.png" }
  ],
  "subject_state": "static",
  "action": "the van parked rear open, Ratna at the threshold, a courier ready by the parcels",
  "pose": "Ratna standing camera-left at the open house doorway, a tablet in her hands, a courier standing camera-right beside a stack of cardboard parcels at the van rear, a second courier behind near the van",
  "gesture": "Ratna looking at the tablet, the courier ready at the parcels",
  "expression": "Ratna calm working focus, the courier neutral ready",
  "grooming": "Ratna neat headscarf, the courier short hair under a cap",
  "wardrobe": "Ratna headscarf, modest long-sleeve tunic, work apron, the couriers plain delivery uniform, caps",
  "framing": "wide establishing, the house front, the box van, three small figures, parcels",
  "angle": "eye-level, from the street side facing the house front",
  "camera": "28mm prime spherical, deep focus front to back",
  "lighting": "warm low morning sun raking from camera-left, long soft shadows across the yard, warm golden key, soft sky fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural daylight realism, warm directional sun, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class residential exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: kurir angkat kardus pertama ke mobil, Ratna menoleh; Ratna NO pop-in) · STATUS: ✅ authored:
```
Change only the gestures, positions held.

- courier: now holding the first cardboard parcel raised toward the open van rear, mid-load, arms up
- Ratna: now turned toward the van camera-right, eyes lifted from the tablet to the couriers
- unchanged: framing unchanged, camera angle unchanged, Ratna threshold position unchanged, van position unchanged, house unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH02 — Kurir memuat kardus · MEDIUM · 50mm
**START attachments:** `E15_depanrumah_master.png` (PENDING) + `F_kurir_front_medium.png` (PENDING).
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E15_depanrumah_master.png — same house front, same van, same curb, faithful match"],
    "identity_reference": ["F_kurir_front_medium.png — same identical courier man, matched face, uniform cap"]
  },
  "mood": "busy lived-in working morning, dispatch in motion, warm ordinary register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "beside a box delivery van morning, a courier loading parcels, a second courier scanning a parcel, phone in hand, cardboard boxes, warm morning sun",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "warm early-morning light, soft long shadows",
  "scene_depth": {
    "foreground": "cardboard parcel stack low frame",
    "midground": "courier-one camera-left holding a parcel toward the van",
    "background": "courier-two soft behind, a phone in hand scanning, van side"
  },
  "subjects": [ { "who": "courier-one", "identity_reference": "F_kurir_front_medium.png" } ],
  "subject_state": "static",
  "action": "courier-one holding a parcel at the van, courier-two scanning behind",
  "pose": "courier-one standing camera-left, a cardboard parcel held in both arms at chest height, turned toward the open van, courier-two soft behind holding a phone up, scanning a parcel",
  "gesture": "courier-one arms around the parcel, courier-two phone up at a box",
  "expression": "both neutral working focus",
  "grooming": "short hair under caps",
  "wardrobe": "plain delivery uniform, caps",
  "framing": "medium shot, courier-one head to waist camera-left, courier-two soft background",
  "angle": "eye-level, facing the couriers beside the van",
  "camera": "50mm prime spherical, shallow depth of field, focus on courier-one",
  "lighting": "warm low morning sun from camera-left, warm key, soft shadow side, soft sky fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural daylight realism, warm directional sun, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class residential exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: kurir-1 masukkan kardus ke mobil, kurir-2 selesai scan) · STATUS: ✅ authored:
```
Change only the load progress, positions held.

- courier-one: the parcel now set into the open van rear, arms extended into the van, mid-placement
- courier-two: the phone lowered, the scan complete, a small nod
- unchanged: framing unchanged, camera angle unchanged, both standing positions unchanged, van position unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH03 — Insert tablet Ratna (status dijemput) · CLOSE · 85mm
**START attachments:** `R_ratna_hijab_front_medium.png` (tangan/identitas). **A1: layar OFF/polos; daftar + "Dijemput" = AE.**
- **START** — mode **B** (insert tangan+tablet) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "identity_reference": ["R_ratna_hijab_front_medium.png — same identical woman hand, matched skin tone, sleeve cuff"]
  },
  "mood": "small working-morning moment, an order picked up, warm ordinary register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a woman hands holding a tablet, screen off dark neutral blank slab, work apron edge, warm morning daylight",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "warm morning daylight, soft",
  "scene_depth": {
    "foreground": "thumb at the tablet edge",
    "midground": "tablet in two hands, screen off dark neutral, sharp",
    "background": "soft out-of-focus apron, doorway shade"
  },
  "subjects": [ { "who": "Ratna hands", "identity_reference": "R_ratna_hijab_front_medium.png" } ],
  "subject_state": "static",
  "action": "two hands holding the tablet, screen off, a thumb near the surface",
  "pose": "Ratna two warm brown Southeast-Asian hands holding a tablet upright, the right thumb hovering near the lower screen",
  "gesture": "thumb a breath above the screen, ready",
  "framing": "close-up insert, the hands, the tablet, screen frame-dominant",
  "angle": "downward onto the tablet, eye-level lowered",
  "camera": "85mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "warm morning daylight soft on the hands, even key, tablet screen off dark neutral, faint warm reflection on the glass",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural daylight realism, warm soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class exterior realism"
}
```
- **END** — EDIT-IN-PLACE (delta: jempol menyentuh satu baris) · STATUS: ✅ authored:
```
Change only the thumb: Ratna taps one row.

- pose: the right thumb now pressed onto a row on the tablet screen, a single tap contact, the other hand steady on the tablet
- unchanged: framing unchanged, camera angle unchanged, hands position unchanged, tablet position unchanged, screen off dark neutral unchanged, background unchanged, lighting unchanged, color grade unchanged
```

---

## SH04 — Ratna di ambang pintu (dapur tampak) · MEDIUM · 50mm
**START attachments:** `E15_depanrumah_pintu.png` (ambang, glimpse dapur, PENDING) + `R_ratna_hijab_front_medium.png`.
- **START** — mode **B** (full master, 1-subjek + glimpse dapur) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E15_depanrumah_pintu.png — same doorway threshold, same open door, same kitchen glimpse behind, faithful match"],
    "identity_reference": ["R_ratna_hijab_front_medium.png — same identical woman, matched face, headscarf, early-forties"]
  },
  "mood": "proud quiet working morning, a small business humming, warm ordinary register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a woman at her open house doorway holding a tablet, behind her through the door a busy home kitchen, a stack of labeled frozen-food boxes on a counter, warm morning outside, shaded interior",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "warm morning at the door, cooler shaded kitchen behind",
  "scene_depth": {
    "foreground": "doorframe edge low frame",
    "midground": "Ratna at the threshold, tablet in hands, headscarf, apron",
    "background": "open door, kitchen glimpse, labeled frozen-food boxes on a counter, shaded"
  },
  "subjects": [ { "who": "Ratna", "identity_reference": "R_ratna_hijab_front_medium.png" } ],
  "subject_state": "static",
  "action": "Ratna at the threshold looking at her tablet, the kitchen busy behind",
  "pose": "Ratna standing at the open doorway, a tablet held in both hands at chest height, eyes down on the screen, the kitchen visible through the door behind her",
  "gesture": "fingers on the tablet, attention on the list",
  "expression": "calm content working focus",
  "grooming": "neat headscarf framing her face",
  "wardrobe": "headscarf, modest long-sleeve tunic, work apron",
  "framing": "medium shot, Ratna head to waist centre, kitchen glimpse behind through the door",
  "angle": "eye-level, facing the doorway, kitchen behind",
  "camera": "50mm prime spherical, shallow depth of field, focus on Ratna",
  "lighting": "warm morning daylight on Ratna from camera side, cooler shaded interior kitchen behind, gentle indoor-outdoor contrast",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural daylight realism, soft fill, honest shade",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class home realism, lived-in working kitchen",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Ratna angkat pandang ke kurir/mobil, mengangguk) · STATUS: ✅ authored:
```
Change only Ratna gaze and head, position held.

- pose: Ratna now lifting her eyes from the tablet toward the couriers off-frame camera-right, a small acknowledging nod, tablet lowered slightly
- expression: warm satisfied nod, content
- unchanged: framing unchanged, camera angle unchanged, Ratna threshold position unchanged, kitchen glimpse unchanged, door unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH05 — Mobil siap berangkat (payoff) · WIDE · 35mm
**START attachments:** `E15_depanrumah_master.png` (PENDING) + `F_kurir_front_full.png` (PENDING) + `R_ratna_hijab_front_full.png`. **END: mobil TIDAK melaju keluar (camera-lock).**
- **START** — mode **B** (full master, 3-subjek WIDE) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E15_depanrumah_master.png — same house front, same van, same curb, faithful match"],
    "identity_reference": ["R_ratna_hijab_front_full.png — same identical woman, matched face, headscarf, early-forties", "F_kurir_front_full.png — same identical courier man, matched face, uniform cap"]
  },
  "mood": "a quiet payoff, the morning dispatch done, warm ordinary register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "front of the house morning, the loaded box van at the curb, a courier at the rear doors, Ratna at the threshold, warm morning sun",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "warm early-morning light, long soft shadows, settled",
  "scene_depth": {
    "foreground": "curb paving low frame",
    "midground": "the box van at the curb camera-right, a courier at the rear door",
    "background": "the house front, Ratna at the threshold camera-left"
  },
  "subjects": [
    { "who": "Ratna", "identity_reference": "R_ratna_hijab_front_full.png" },
    { "who": "courier", "identity_reference": "F_kurir_front_full.png" }
  ],
  "subject_state": "static",
  "action": "a courier closing the van rear door, Ratna at the threshold seeing them off",
  "pose": "the courier standing camera-right at the van rear, both hands on the rear door swinging it closed, Ratna standing camera-left at the doorway watching",
  "gesture": "the courier hands on the door, Ratna watching",
  "expression": "the courier neutral, Ratna calm content",
  "grooming": "Ratna neat headscarf, the courier cap",
  "wardrobe": "Ratna headscarf, tunic, apron, the courier delivery uniform, cap",
  "framing": "wide shot, the house, the box van camera-right, two small figures",
  "angle": "eye-level, from the street side, the van, the house",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "warm low morning sun from camera-left, long soft shadows, warm key, soft sky fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "natural daylight realism, warm directional sun, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class residential exterior realism, lived-in",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: mobil siap berangkat MASIH di tempat, Ratna mengangguk; mobil TIDAK melaju) · STATUS: ✅ authored:
```
Change only readiness, the van stays in place.

- courier: the van rear door now shut, the courier stepping to the cab side, one hand on the door
- van: stationary at the curb, engine idling, held in place, ready, still fully in frame at the same position
- Ratna: a parting nod from the doorway, calm
- unchanged: framing unchanged, camera angle unchanged, van position at the curb unchanged, the van still in frame unchanged, house unchanged, Ratna threshold position unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
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

**Ladder:** W→M→CU→M→W. **Grade pagi hangat** (GATE B). **Camera-lock:** 3-subjek hanya WIDE (SH01/SH05); Ratna NO pop-in (hadir START); **mobil tak melaju** (SH05 END held in place). **A1:** SH03 screen OFF/polos (daftar/"Dijemput"=AE). **Modesty:** Ratna berhijab+celemek (kurir non-mahram). **⚠ PENDING plates:** `E15_depanrumah_{master,pintu}` + `F_kurir_front_{full,medium}` (figuran F7).
