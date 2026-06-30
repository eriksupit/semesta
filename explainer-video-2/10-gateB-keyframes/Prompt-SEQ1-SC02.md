---
title: GATE B Prompt — SEQ1-SC02 (INT. RUANG KELUARGA — 04.43)
tags: [explainer-video-2, gate-b, prompt, status, SEQ1-SC02]
status: authoring
created: 2026-07-01
updated: 2026-07-01
aliases: [ev2-prompt-seq1-sc02]
---

# GATE B Prompt — SEQ1-SC02
## INT. RUANG KELUARGA — 04.43 WIB

> **Konvensi dua-doc (`06` Langkah 2):** doc ini = **prompt GATE B + status per-shot**. Narasi sumber = `SEQ1-SC02.md`. Cerita = `03-scene-detail.md` SEQ1-SC02.
> **Pola seragam (sama SC01):** START = master full-prompt + attachment → END = edit-in-place pada render START (NOL preamble; operasi+delta+lock-list). Camera-lock: START/END angle+framing identik, delta subjek/praktis saja. Device screen OFF→glow (A1: slab polos, konten UI=AE). Grade: interior lampu HANGAT ON + jendela subuh gelap-biru. **Bersih Saat Sakral** sejak SH05 (nol grafis). Audit `/tti-prompt-audit` per START.

## Manifest attachment (plat tersedia di disk — verified)
- **Env E02:** `E02_ruangkeluarga_master.png` (layout: sofa camera-left, window centre, **desktop camera-right-behind**, TV far camera-right) · `E02_ruangkeluarga_screen.png` (sudut desktop) · `E02_ruangkeluarga_reverse_prayer_subuh.png` (saf subuh, 4 sajadah ter-bake).
- **Karakter:** `L_lisa_front_{full,medium}` · `A_andi_front_{full,medium}` · `H_herman_front_closeup` · `H/A/R/L_rear_full` (saf rear).

---

## SH01 — Establishing: ruang + Lisa & Andi + desktop · MW · 35mm
**SHOT-CONCEPT:** MW establishing, vantage master (sisi sofa menghadap jendela); Lisa+Andi kepala uncovered di tengah, desktop glow camera-right-behind (anchor SH02), jendela subuh gelap. Kamera diam; END = mulai kenakan mukena/peci. Grade warm interior + cool window.
**START attachments:** `E02_ruangkeluarga_master.png` + `L_lisa_front_full.png` + `A_andi_front_full.png`.

- **START** — mode **B** (full master, 2-subjek + ruang) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E02_ruangkeluarga_master.png — same family living room layout, same handedness, sofa camera-left, window centre, desktop camera-right-behind near the window, TV far camera-right"],
    "identity_reference": ["L_lisa_front_full.png — same identical young woman, matched face, uncovered loose hair, early-twenties", "A_andi_front_full.png — same identical boy, matched face, age ten"]
  },
  "mood": "reverent intimate pre-dawn family devotion, hushed sacred preparation, quiet domestic register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "family living room, warm interior lamplight on, dark pre-dawn window centre, corner desktop screen glowing camera-right-behind, prayer area centre floor, lived-in middle-class Jakarta home",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "warm-lit interior calm, dark blue pre-dawn beyond the window",
  "scene_depth": {
    "foreground": "prayer area floor, soft focus low frame",
    "midground": "Lisa, Andi standing centre facing the lens, Lisa holding a folded mukena, Andi holding a peci cap",
    "background": "dark pre-dawn window centre, corner desktop screen glowing camera-right-behind, sofa camera-left"
  },
  "subjects": [
    { "who": "Lisa", "identity_reference": "L_lisa_front_full.png" },
    { "who": "Andi", "identity_reference": "A_andi_front_full.png" }
  ],
  "subject_state": "static",
  "action": "Lisa, Andi standing together facing the lens, calm before prayer",
  "pose": "Lisa standing centre-left, folded white mukena held at her waist, uncovered loose hair, Andi standing centre-right, black peci cap held in both hands, both upright, settled",
  "gesture": "Lisa fingers on the folded mukena, Andi fingers on the peci",
  "expression": "Lisa soft just-woken calm, faint sleepy eyes, Andi fresher alert calm, both serene",
  "grooming": "Lisa loose uncovered hair, sleep-soft, Andi short neat boy hair",
  "wardrobe": "Lisa modest long-sleeve home tunic, loose trousers, Andi plain long-sleeve home shirt, loose trousers",
  "framing": "medium-wide establishing, Lisa, Andi upper body centre, prayer area, desktop corner, window visible",
  "angle": "eye-level, master vantage from the sofa side facing the window wall",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "warm interior ceiling lamp key, soft warm wrap on the two figures, cool blue pre-dawn ambient through the dark window centre, cool desktop screen glow camera-right-behind, warm-cool balance",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft wrap, deep honest shadow",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: keduanya mulai kenakan mukena/peci) · STATUS: ✅ authored:
```
Change only the two figures gesture: they begin to put on prayer wear.

- Lisa: arms raised, white mukena held over her head at her crown, partly draped over her hair
- Andi: both hands raised, black peci held at the crown of his head, partly seated
- unchanged: framing unchanged, camera angle unchanged, both standing positions unchanged, desktop corner unchanged, window unchanged, sofa unchanged, lighting unchanged, color grade unchanged
```

---

## SH02 — Desktop lapak Ratna (insert ter-anchor, pra-sakral) · CLOSE · 50mm
**SHOT-CONCEPT:** CLOSE insert sudut desktop; layar glow cool slab (lapak/kartu = AE, A1); 0-subjek; ter-anchor oleh SH01. Kamera diam; **insert ambient statik** (delta minimal, sah — shimmer layar + ambient di Kling/AE, bukan cacat camera-lock).
**START attachments:** `E02_ruangkeluarga_screen.png` (sudut desktop) + `E02_ruangkeluarga_master.png` (layout).

- **START** — mode **B** (object insert) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E02_ruangkeluarga_screen.png — same desktop corner, same monitor, same desk, identical insert geometry", "E02_ruangkeluarga_master.png — same living room layout, same handedness, desktop camera-right-behind near the window"]
  },
  "mood": "quiet pre-dawn domestic hush, a glowing screen left alone",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic material rendering",
  "scene": "corner desktop monitor on a small desk, screen a plain bright cool blue-white glowing slab blank featureless, warm room lamplight around, dark pre-dawn window beside",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "warm-lit interior hush, cool screen glow",
  "scene_depth": {
    "foreground": "near desk edge, soft focus",
    "midground": "desktop monitor, screen a plain cool blue-white glowing slab, sharp",
    "background": "warm-lit wall, dark window edge camera-right, deep shadow"
  },
  "subject_state": "static",
  "action": "monitor glowing, room still, screen left on",
  "framing": "close insert, desktop monitor fills frame, glowing slab centred",
  "angle": "slight angle onto the screen, from the room side, eye-level at desk height",
  "camera": "50mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "cool blue-white screen glow as local key on the desk, warm interior lamp ambient fill around, cool window edge camera-right, warm-cool contrast",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft wrap, deep honest shadow",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity"
}
```
- **END** — minimal-hold (insert ambient statik) · STATUS: ✅ authored:
```
Hold identical to START — no still-frame delta. The screen shimmer + faint room settle = Kling i2v motion / After Effects (UI ledger overlays the lapak + supplier card). Keep frame, lighting, screen slab, framing identical.
```

---

## SH03 — Mengenakan mukena & peci · MEDIUM · 50mm
**SHOT-CONCEPT:** MEDIUM, Lisa fokus (mukena) + Andi sekunder (peci); eye-level. Kamera diam; END = Lisa bermukena rapi, Andi berpeci, siap sholat. Grade warm interior.
**START attachments:** `E02_ruangkeluarga_master.png` + `L_lisa_front_medium.png` + `A_andi_front_medium.png`.

- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E02_ruangkeluarga_master.png — same living room layout, same handedness, sofa camera-left, window centre, desktop camera-right-behind"],
    "identity_reference": ["L_lisa_front_medium.png — same identical young woman, matched face, early-twenties", "A_andi_front_medium.png — same identical boy, matched face, age ten"]
  },
  "mood": "reverent intimate pre-dawn family devotion, hushed sacred preparation, quiet domestic register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "family living room, warm interior lamplight on, dark pre-dawn window behind, prayer-wear dressing moment",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "warm-lit interior calm, sacred preparation",
  "scene_depth": {
    "foreground": "soft room edge low frame",
    "midground": "Lisa, white mukena half-draped over her head, Andi, black peci half-seated",
    "background": "warm-lit wall, dark window, soft shadow"
  },
  "subjects": [
    { "who": "Lisa", "identity_reference": "L_lisa_front_medium.png" },
    { "who": "Andi", "identity_reference": "A_andi_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "Lisa mid-dressing, mukena half-draped over her head, Andi mid-dressing, peci half-seated on his head",
  "pose": "Lisa centre, arms raised at her crown, white mukena half over her hair, partly draped, Andi camera-right, both hands at his crown, black peci half-seated",
  "gesture": "Lisa fingers settling the mukena edge, Andi fingers settling the peci",
  "expression": "Lisa calm focused soft, Andi calm focused",
  "grooming": "Lisa hair partly covered by the half-draped mukena, Andi short neat hair under the peci",
  "wardrobe": "Lisa white prayer mukena half-draped, modest tunic beneath, Andi plain home shirt, black peci",
  "framing": "medium shot, Lisa head to waist centre, Andi head to chest camera-right",
  "angle": "eye-level, facing Lisa, slightly toward Andi camera-right",
  "camera": "50mm prime spherical, shallow depth of field, focus on Lisa",
  "lighting": "warm interior ceiling lamp key, soft warm wrap, cool window ambient behind, gentle warm-cool balance",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft wrap, deep honest shadow",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: mukena/peci terpasang rapi, siap) · STATUS: ✅ authored:
```
Change only the prayer wear to fully worn.

- Lisa: white mukena now fully draped over her head, framing her face, covering her hair, hands lowered, settled
- Andi: black peci now fully seated on his head, hands lowered at his sides, settled
- expression: both calm, ready, serene before prayer
- unchanged: framing unchanged, camera angle unchanged, both standing positions unchanged, window unchanged, lighting unchanged, color grade unchanged
```

---

## SH04 — Saf terbentuk · WIDE 4-subjek REAR-VIEW · 35mm
**SHOT-CONCEPT:** WIDE dari belakang saf, menghadap kiblat/jendela; 4-subjek **rear-view** (punggung ke kamera → hindari face-lock collapse). Herman imam depan + Andi (peci), Ratna+Lisa saf perempuan (mukena). Plat saf subuh mem-bake sajadah. Kamera diam; **delta = settle in-frame** (saf SUDAH di posisi sejak START — no lokomosi formasi). ⚠ shot tersulit TTI.
**START attachments:** `E02_ruangkeluarga_reverse_prayer_subuh.png` (saf+sajadah) + `H_herman_rear_full.png` + `A_andi_rear_full.png` + `R_ratna_rear_full.png` + `L_lisa_rear_full.png`.

- **START** — mode **B** (full master, 4-subjek rear) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E02_ruangkeluarga_reverse_prayer_subuh.png — same living room reverse view toward the window, same four prayer mats baked on the floor, same handedness, faithful match"],
    "identity_reference": ["H_herman_rear_full.png — same man back view, matched build, matched hair", "A_andi_rear_full.png — same boy back view, age ten", "R_ratna_rear_full.png — same woman back view, matched build", "L_lisa_rear_full.png — same young woman back view, matched build"]
  },
  "mood": "reverent hushed family prayer, sacred stillness, devotional register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "family living room prayer formation seen from behind, four figures standing on four prayer mats facing the dark pre-dawn window, warm interior lamplight, sacred congregation",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "warm-lit reverent hush, dark blue window ahead",
  "scene_depth": {
    "foreground": "near prayer mat edge low frame",
    "midground": "Herman standing front as imam, Andi a row behind, Ratna, Lisa in the women row behind",
    "background": "dark pre-dawn window ahead, warm-lit wall"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_rear_full.png" },
    { "who": "Andi", "identity_reference": "A_andi_rear_full.png" },
    { "who": "Ratna", "identity_reference": "R_ratna_rear_full.png" },
    { "who": "Lisa", "identity_reference": "L_lisa_rear_full.png" }
  ],
  "subject_state": "static",
  "action": "the family standing in prayer rows facing the qibla, backs to the lens, settling into stillness",
  "pose": "Herman front centre as imam upright facing the window, Andi one step behind on his mat, Ratna, Lisa side by side in the women row behind, all upright backs to the camera facing the dark window",
  "gesture": "arms resting at sides, settling still",
  "expression": "faces away from the lens, unseen, heads bowed slightly forward",
  "grooming": "Herman black peci, Andi black peci, Ratna white mukena full drape, Lisa white mukena full drape",
  "wardrobe": "Herman sarong, long-sleeve shirt, peci, Andi home shirt, peci, Ratna full white mukena, Lisa full white mukena",
  "framing": "wide shot, four figures full height from behind, prayer mats, window ahead",
  "angle": "reverse view from behind the rows, eye-level, facing the window wall",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "warm interior ceiling lamp key from above, soft warm wrap on the backs, cool blue pre-dawn ambient from the dark window ahead, warm-cool depth",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft wrap, deep honest shadow",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: saf settle diam-rapi; lock 4 punggung via plat rear `+`) · STATUS: ✅ authored:
```
Change only the settling: the rows go fully still.

- pose: all four figures now perfectly still, upright, arms resting at their sides, hands settled, backs square to the camera facing the window, calm ready before takbir
- unchanged: framing unchanged, camera angle unchanged, all four positions on their mats unchanged, prayer mats unchanged, window unchanged, lighting unchanged, color grade unchanged, each figure back matching its attached rear plate
```

---

## SH05 — Takbiratul ihram (CU tangan) · CLOSE-UP · 85mm
**SHOT-CONCEPT:** CU rapat ke tangan Herman terangkat takbir setinggi telinga; wajah/peci soft di atas frame; 1-subjek (makmum tak di-frame; kebersamaan sudah di SH04 WIDE). **Bersih Saat Sakral aktif** (nol grafis sejak shot ini). Kamera diam; END = telapak terangkat setinggi telinga.
**START attachments:** `E02_ruangkeluarga_reverse_prayer_subuh.png` (latar saf soft) + `H_herman_front_closeup.png` (wajah/peci soft top).

- **START** — mode **B** (full master, 1-subjek rapat) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E02_ruangkeluarga_reverse_prayer_subuh.png — same prayer setting, soft background, warm interior, faithful match"],
    "identity_reference": ["H_herman_front_closeup.png — same identical man, matched face, clean-shaven, mid-forties, black peci"]
  },
  "mood": "reverent sacred threshold, hushed devotional focus, quiet awe",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "imam hands at the start of prayer, warm interior lamplight, soft prayer setting behind, sacred moment",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "warm-lit reverent hush",
  "scene_depth": {
    "foreground": "soft sleeve cuff low frame",
    "midground": "Herman two hands at his sides beginning the raise, forearms sharp",
    "background": "Herman face, peci soft at top of frame, warm-lit prayer setting, soft focus"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_closeup.png" }
  ],
  "subject_state": "static",
  "action": "Herman hands at his sides at the threshold of takbir, stillness",
  "pose": "Herman standing, both hands resting at his sides palms inward, forearms relaxed, face, black peci soft at the upper frame",
  "gesture": "fingers relaxed together, ready",
  "expression": "soft at the top of frame, eyes lowered, serene devotional calm",
  "grooming": "black peci, clean-shaven, neat hair",
  "wardrobe": "long-sleeve shirt cuffs, sarong waist soft below",
  "framing": "close-up, Herman two hands, forearms, lower face, peci soft at top, hands frame-dominant",
  "angle": "eye-level close, from Herman side, hands central",
  "camera": "85mm prime spherical, shallow depth of field, focus on the hands",
  "lighting": "warm interior ceiling lamp key, soft warm wrap on the hands, gentle falloff to the soft background",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft wrap, deep honest shadow",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: kedua telapak terangkat setinggi telinga, takbiratul ihram) · STATUS: ✅ authored:
```
Change only the hands raise into takbir.

- pose: Herman both hands now raised to ear height, palms open facing forward, fingers loosely together, elbows out, the classic takbiratul ihram posture, face, peci soft above the hands at the top of frame
- expression: eyes lowered, serene, reverent
- unchanged: framing unchanged, camera angle unchanged, Herman position unchanged, background unchanged, lighting unchanged, color grade unchanged, face matching attached plate H_herman_front_closeup
```

---

## Status board
| Shot | START | END | Render |
|---|---|---|---|
| SH01 | ✅ authored | ✅ authored | pending (final batch) |
| SH02 | ✅ authored | ✅ hold (ambient) | pending (final batch) |
| SH03 | ✅ authored | ✅ authored | pending (final batch) |
| SH04 | ✅ authored | ✅ authored | pending (final batch) |
| SH05 | ✅ authored | ✅ authored | pending (final batch) |

**Generate-order:** SH01→SH02→SH03→SH04→SH05. Plates needed = `E02_ruangkeluarga_{master,screen,reverse_prayer_subuh}` + `L_lisa_front_{full,medium}` + `A_andi_front_{full,medium}` + `H_herman_{front_closeup,rear_full}` + `A/R/L_rear_full` — all on disk.
**Ladder:** MW→CU→M→W→CU (selang-seling). **Bersih Saat Sakral** sejak SH05. **⚠ SH04 = 4-subjek rear** (tersulit; rear + plat saf mem-bake sajadah meredam risiko).
