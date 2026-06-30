---
title: GATE B Prompt — SEQ4-SC10 (INT. KANTOR EKSPOR-IMPOR — 16.00)
tags: [explainer-video-2, gate-b, prompt, status, SEQ4-SC10]
status: authoring
created: 2026-07-01
updated: 2026-07-01
aliases: [ev2-prompt-seq4-sc10]
---

# GATE B Prompt — SEQ4-SC10
## INT. KANTOR EKSPOR-IMPOR — 16.00 WIB *(pembuka SEQ4)*

> **Konvensi dua-doc:** prompt GATE B + status. Narasi = `SEQ4-SC10.md`. Env = `E08_kantor` (cell `dasbor` = angle dinding-layar-besar). Rekan = `F4 Rian`.
> **Pola seragam (SC01–SC09):** START full-prompt + attachment → END edit-in-place. Camera-lock: Rian stasioner, delta gestur in-frame. **Gawai = tablet (aksi)** + **layar besar dinding = ambient**, keduanya OFF/polos (A1: dasbor komoditas + loket + status = AE; aman melt). **no-coal:** dasbor = sektor/mineral/**nikel-hilirisasi**, BUKAN batubara (konten = AE). Grade **sore jingga** (bedakan dari SC05 pagi). VO = beat fairness.

## Manifest attachment
- **Env E08 (⚠ PENDING final-batch):** `E08_kantor_dasbor.png` (angle dinding-layar-besar + meja Herman).
- **Karakter:** `H_herman_front_{full,medium}` (✓) · `F_rian_front_medium` (✓).
- **Generate-order final-batch:** E08 dasbor cell **sebelum** keyframe SC10. (E08 master+meja juga dipakai SC05.)

---

## SH01 — Establishing kantor sore + dasbor dinding · WIDE · 24mm
**START attachments:** `E08_kantor_dasbor.png` (PENDING) + `H_herman_front_full.png` + `F_rian_front_medium.png`.
- **START** — mode **B** (full master, 2-subjek + layar besar) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E08_kantor_dasbor.png — same export-import office, same large wall display, same desk, same layout, same handedness, faithful match"],
    "identity_reference": ["H_herman_front_full.png — same identical man, matched face, clean-shaven, mid-forties", "F_rian_front_medium.png — same identical colleague man, matched face"]
  },
  "mood": "warm late-afternoon competence, an unhurried close of business, professional register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "export-import office late afternoon, a large wall display glowing a plain neutral slab, a slanting orange sunset through the windows, a man at a desk holding a tablet, a colleague beside him",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "warm orange late-afternoon light, slanting sun, calm",
  "scene_depth": {
    "foreground": "near desk edge low frame",
    "midground": "Herman seated at the desk holding a tablet, Rian standing beside him",
    "background": "the large wall display plain neutral slab, route-map wall, orange windows"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_full.png" },
    { "who": "Rian", "identity_reference": "F_rian_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "Herman seated holding a tablet, Rian standing beside him, the wall display glowing",
  "pose": "Herman seated centre at the desk, a tablet in his hands, Rian standing camera-right beside the desk, a pen in one hand, both facing toward the desk",
  "gesture": "Herman holding the tablet, Rian a pen in hand ready",
  "expression": "both calm, attentive, professional",
  "grooming": "both neat short hair",
  "wardrobe": "Herman collared work shirt, Rian collared work shirt",
  "framing": "wide establishing, the office, the large wall display, the desk, two figures",
  "angle": "eye-level, from the back of the room toward the wall-display wall",
  "camera": "24mm prime spherical, deep focus front to back",
  "lighting": "warm orange low late-afternoon sun slanting through the windows camera-left, warm key, long soft shadows, plain neutral wall-display glow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "naturalistic workplace observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, warm directional sun, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "contract-institutional office realism, lived-in workplace",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Herman menatap tablet, Rian condong menunjuk) · STATUS: ✅ authored:
```
Change only the gestures, positions held.

- Herman: now both eyes down on the tablet, intent
- Rian: now inclined slightly toward the desk, the pen tip lowered toward the tablet
- unchanged: framing unchanged, camera angle unchanged, both positions unchanged, wall display plain slab unchanged, desk unchanged, windows unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH02 — Insert layar besar (dasbor komoditas) · CLOSE · 50mm
**START attachments:** `E08_kantor_dasbor.png` (latar dinding, PENDING). **A1: layar slab polos; dasbor = AE. no-coal: sektor/mineral/nikel-hilirisasi.**
- **START** — mode **B** (object insert) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E08_kantor_dasbor.png — same large wall display, same office wall, identical insert geometry, faithful match"]
  },
  "mood": "an information surface humming, market data at a glance, professional register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic material rendering",
  "scene": "a large wall display, screen a plain bright neutral glowing slab blank featureless, mounted on the office wall, warm orange late-afternoon ambient",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "warm orange ambient, soft",
  "scene_depth": {
    "foreground": "office wall edge",
    "midground": "the large wall display, plain neutral glowing slab, sharp",
    "background": "soft out-of-focus office, warm orange light"
  },
  "subject_state": "static",
  "action": "the wall display glowing plain, market data on screen",
  "framing": "close insert, the wall display frame-dominant",
  "angle": "slightly up toward the wall display, eye-level lifted",
  "camera": "50mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "plain neutral display glow as local key, warm orange ambient fill, soft",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "naturalistic workplace observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "contract-institutional office realism"
}
```
- **END** — minimal-hold (dasbor komoditas = AE; no-coal) · STATUS: ✅ authored:
```
Hold identical to START — no still-frame delta. The commodity-market dashboard "Pasar komoditas hari ini" + shifting mineral price figures + sector headlines = After Effects overlays on the plain slab. NO-COAL: sector / mineral / nickel-downstream content only, never coal. Keep frame, screen slab, lighting, framing identical.
```

---

## SH03 — Rekan menunjuk tablet Herman · MEDIUM 2-shot · 50mm
**START attachments:** `E08_kantor_dasbor.png` (PENDING) + `H_herman_front_medium.png` + `F_rian_front_medium.png`. **Rian stasioner.**
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E08_kantor_dasbor.png — same office, same desk, same wall display, faithful match"],
    "identity_reference": ["H_herman_front_medium.png — same identical man, matched face, mid-forties", "F_rian_front_medium.png — same identical colleague man, matched face"]
  },
  "mood": "a focused work exchange, one container ready, professional register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a seated man holding a tablet, a colleague beside him, a pen in hand, warm orange late-afternoon office",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "warm orange late-afternoon light, calm",
  "scene_depth": {
    "foreground": "desk edge low frame",
    "midground": "Herman seated camera-left holding the tablet, Rian standing camera-right, a pen in hand",
    "background": "wall display plain slab soft, orange windows"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_medium.png" },
    { "who": "Rian", "identity_reference": "F_rian_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "Herman holding the tablet, Rian beside him, a pen toward it",
  "pose": "Herman seated camera-left, a tablet held up in both hands, Rian standing camera-right, a pen in hand near the tablet",
  "gesture": "Herman holding the tablet, Rian pen near the screen",
  "expression": "both attentive, focused",
  "grooming": "both neat short hair",
  "wardrobe": "both collared work shirts",
  "framing": "medium two-shot, Herman head to chest seated camera-left, Rian head to waist camera-right",
  "angle": "eye-level, from the desk side, both figures, tablet between",
  "camera": "50mm prime spherical, shallow depth of field, focus on the tablet",
  "lighting": "warm orange late-afternoon sun from camera-left, warm key, soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "naturalistic workplace observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, warm directional sun, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "contract-institutional office realism, lived-in workplace",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: rekan menunjuk satu baris di tablet, Herman ikuti) · STATUS: ✅ authored:
```
Change only the gestures, positions held.

- Rian: now the pen tip touched to a line on the tablet, pointing
- Herman: eyes following the pen to the tablet, a small nod
- unchanged: framing unchanged, camera angle unchanged, both positions unchanged, tablet unchanged, wall display plain slab unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH04 — Insert tablet (loket izin → ajukan) · CLOSE · 85mm
**START attachments:** `H_herman_front_medium.png` (tangan/tablet). **A1: layar slab polos; loket + "Ajukan dokumen" + status = AE.**
- **START** — mode **B** (insert tangan+tablet) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "identity_reference": ["H_herman_front_medium.png — same identical man hands, matched skin tone, sleeve cuff"]
  },
  "mood": "a permit from the palm of the hand, fairness in a tap, professional register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "two hands holding a tablet, screen off dark neutral blank slab, warm orange late-afternoon ambient",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "warm orange ambient, soft",
  "scene_depth": {
    "foreground": "thumb at the tablet edge",
    "midground": "the tablet in two hands, screen off dark neutral, sharp",
    "background": "soft out-of-focus desk, orange office light"
  },
  "subjects": [ { "who": "Herman hands", "identity_reference": "H_herman_front_medium.png" } ],
  "subject_state": "static",
  "action": "two hands holding the tablet, screen off, a permit ready",
  "pose": "Herman two hands holding the tablet upright, the right thumb near the lower screen",
  "gesture": "thumb near the screen, ready",
  "framing": "close-up insert, the hands, the tablet, screen frame-dominant",
  "angle": "downward onto the tablet, eye-level lowered",
  "camera": "85mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "warm orange ambient soft on the hands, even key, tablet screen off dark neutral, faint warm reflection",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "naturalistic workplace observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, warm soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "contract-institutional office realism"
}
```
- **END** — EDIT-IN-PLACE (delta: jempol Herman mengetuk "ajukan"; status=AE) · STATUS: ✅ authored:
```
Change only the thumb: Herman taps "ajukan".

- pose: Herman right thumb now pressed onto the lower tablet screen, a single confirming tap, the other hand steady on the tablet
- unchanged: framing unchanged, camera angle unchanged, hands position unchanged, tablet screen off dark neutral unchanged, background unchanged, lighting unchanged, color grade unchanged
```

---

## SH05 — Terverifikasi + tepuk bahu · MEDIUM 2-shot · 50mm
**START attachments:** `E08_kantor_dasbor.png` (PENDING) + `H_herman_front_medium.png` + `F_rian_front_medium.png`.
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E08_kantor_dasbor.png — same office, same desk, same wall display, faithful match"],
    "identity_reference": ["H_herman_front_medium.png — same identical man, matched face, mid-forties", "F_rian_front_medium.png — same identical colleague man, matched face"]
  },
  "mood": "quiet satisfaction, a job cleared, warm professional register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a seated man, a tablet in hand, a colleague beside him, warm orange late-afternoon office, an approval just landed",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "warm orange late-afternoon light, settled",
  "scene_depth": {
    "foreground": "desk edge low frame",
    "midground": "Herman seated camera-left, the tablet in hand, Rian standing camera-right",
    "background": "wall display plain slab soft, orange windows"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_medium.png" },
    { "who": "Rian", "identity_reference": "F_rian_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "Herman looking at the tablet, the status changed, Rian beside him",
  "pose": "Herman seated camera-left looking at the tablet, a small satisfied look, Rian standing camera-right upright beside him",
  "gesture": "Herman eyes on the tablet, Rian about to reach over",
  "expression": "both pleased, warm",
  "grooming": "both neat short hair",
  "wardrobe": "both collared work shirts",
  "framing": "medium two-shot, Herman head to chest seated camera-left, Rian head to waist camera-right",
  "angle": "eye-level, from the desk side, both figures",
  "camera": "50mm prime spherical, shallow depth of field, focus split on the two",
  "lighting": "warm orange late-afternoon sun from camera-left, warm key, soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "naturalistic workplace observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, warm directional sun, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "contract-institutional office realism, lived-in workplace",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: rekan menepuk bahu Herman; sama-gender OK) · STATUS: ✅ authored:
```
Change only the gesture, positions held.

- Rian: now one hand laid on Herman shoulder in a warm collegial pat, a small congratulating smile
- Herman: a satisfied smile, head lifted from the tablet
- unchanged: framing unchanged, camera angle unchanged, both positions unchanged, desk unchanged, wall display plain slab unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## Status board
| Shot | START | END | Render |
|---|---|---|---|
| SH01 | ✅ authored | ✅ authored | pending (final batch) |
| SH02 | ✅ authored | ✅ hold (AE dasbor) | pending (final batch) |
| SH03 | ✅ authored | ✅ authored | pending (final batch) |
| SH04 | ✅ authored | ✅ authored | pending (final batch) |
| SH05 | ✅ authored | ✅ authored | pending (final batch) |

**Ladder:** W→CU→M→CU→M. **Grade sore jingga** (GATE B; bedakan dari SC05 pagi). **Camera-lock:** Rian stasioner, delta gestur in-frame. **A1:** tablet + layar besar dinding = slab polos (dasbor komoditas + loket + status = AE; aman melt). **no-coal:** dasbor = sektor/mineral/nikel-hilirisasi, BUKAN batubara. **Gov-as-tenant** diferensiator. **Touch OK** (Rian↔Herman sama-gender, tepuk bahu). **⚠ PENDING plate:** `E08_kantor_dasbor` (cell baru). VO fairness.
