---
title: GATE B Prompt — SEQ3-SC08 (INT. SUDUT KERJA RUMAH RATNA — 11.00)
tags: [explainer-video-2, gate-b, prompt, status, SEQ3-SC08]
status: authoring
created: 2026-07-01
updated: 2026-07-01
aliases: [ev2-prompt-seq3-sc08]
---

# GATE B Prompt — SEQ3-SC08
## INT. SUDUT KERJA RUMAH RATNA — 11.00 WIB *(pembuka SEQ3)*

> **Konvensi dua-doc:** prompt GATE B + status. Narasi = `SEQ3-SC08.md`. Env = `E05_sudutkerja` (**plat SUDAH JADI** ✓: master+meja). Petugas = `F3 petugasbank` (feed video di AE).
> **⚠ REKONSILIASI DEVICE (kanon 2026-07-01):** narasi `SEQ3-SC08.md` masih menyebut **all-in-one** — itu SUPERSEDED. Kanon final (`03` SC08 + E05 redesign) = **tablet di stand di atas meja prep stainless** (komputer fixed Ratna ada di E02). Ruang E05 = **pojok-kerja frozen-food kitchen-adjacent** (chest freezer + meja prep + vacuum sealer). Keyframe pakai **tablet-on-stand**, bukan all-in-one.
> **Pola seragam (SC01–SC07):** START full-prompt + attachment → END edit-in-place. Camera-lock: Ratna stasioner, delta gestur in-frame. Tablet screen OFF/polos (A1: ruang tunggu + feed petugas + data + kartu pembiayaan + "Diproses" = AE). Grade siang hangat (GATE B). **Ratna berhijab+celemek** (petugas non-mahram via kamera). 1 subjek fisik (petugas = AE feed).

## Manifest attachment (semua di disk ✓)
- **Env E05:** `E05_sudutkerja_master.png` (establishing) · `E05_sudutkerja_meja.png` (prep-worktable + tablet-on-stand).
- **Karakter:** `R_ratna_hijab_front_{full,medium}`. *(F3 petugasbank = AE feed, bukan attachment render.)*
- **Tanpa PENDING plate** — SC08 siap di-generate.

---

## SH01 — Establishing sudut kerja · MW · 35mm
**START attachments:** `E05_sudutkerja_master.png` + `R_ratna_hijab_front_full.png`.
- **START** — mode **B** (full master, 1-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E05_sudutkerja_master.png — same frozen-food home work corner, same prep worktable, same tablet on a stand, same chest freezer, same layout, same handedness, faithful match"],
    "identity_reference": ["R_ratna_hijab_front_full.png — same identical woman, matched face, headscarf, early-forties"]
  },
  "mood": "calm focused working midday, a small business growing, warm domestic register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "home frozen-food work corner midday, a stainless prep worktable, a tablet propped on a small stand screen a plain neutral glowing slab, a chest freezer camera-right, warm window daylight",
  "location": "indoor",
  "time_of_day": "midday",
  "atmosphere": "warm midday window light, quiet working calm",
  "scene_depth": {
    "foreground": "prep worktable edge low frame",
    "midground": "Ratna seated at the worktable before the propped tablet",
    "background": "wall rack, chest freezer camera-right, window"
  },
  "subjects": [ { "who": "Ratna", "identity_reference": "R_ratna_hijab_front_full.png" } ],
  "subject_state": "static",
  "action": "Ratna seated at the prep worktable facing the propped tablet, the virtual bank branch open",
  "pose": "Ratna seated on the stool at the stainless prep worktable, hands near the tablet on its stand, eyes on the screen",
  "gesture": "one hand near the tablet, attention on the screen",
  "expression": "calm working focus, a little hopeful",
  "grooming": "neat headscarf framing her face",
  "wardrobe": "headscarf, modest long-sleeve tunic, work apron",
  "framing": "medium-wide establishing, the work corner, Ratna at the prep worktable, tablet on its stand",
  "angle": "eye-level, facing the worktable",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "warm midday daylight from the window, soft warm key on Ratna, gentle room fill, plain neutral tablet glow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, warm window wrap, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta home, working frozen-food corner",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working grooming under a headscarf"
}
```
- **END** — EDIT-IN-PLACE (delta: Ratna tekan tombol "bicara dengan petugas") · STATUS: ✅ authored:
```
Change only Ratna hand gesture, position held.

- Ratna: now one index finger pressed to the tablet screen, a single tap on the lower screen, the other hand resting on the worktable, eyes on the screen
- unchanged: framing unchanged, camera angle unchanged, Ratna seated position unchanged, tablet on its stand unchanged, prep worktable unchanged, freezer unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH02 — Insert layar: video tersambung · CLOSE · 85mm
**START attachments:** `E05_sudutkerja_meja.png` (latar). **A1: layar slab polos; ruang tunggu + feed petugas (F3) = AE.**
- **START** — mode **B** (object insert) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E05_sudutkerja_meja.png — same prep worktable, same tablet on a stand, identical insert geometry, faithful match"]
  },
  "mood": "a connection opening, a bank coming to her, warm register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic material rendering",
  "scene": "a tablet propped on a small stand, screen a plain bright neutral glowing slab blank featureless, on a stainless prep worktable, warm midday ambient",
  "location": "indoor",
  "time_of_day": "midday",
  "atmosphere": "warm midday ambient, soft",
  "scene_depth": {
    "foreground": "worktable surface at the stand base",
    "midground": "the tablet screen, plain neutral glowing slab, sharp",
    "background": "soft out-of-focus wall rack, warm light"
  },
  "subject_state": "static",
  "action": "the tablet glowing plain, a call connecting",
  "framing": "close insert, the tablet screen frame-dominant, the stand base lower frame",
  "angle": "facing the tablet screen, eye-level at worktable height",
  "camera": "85mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "plain neutral tablet glow as local key, warm midday ambient fill, soft",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta home"
}
```
- **END** — minimal-hold (feed video petugas = AE) · STATUS: ✅ authored:
```
Hold identical to START — no still-frame delta. The digital waiting room, then the connected bank-officer video feed (F3 petugasbank) = After Effects overlays on the plain slab. Keep frame, screen slab, lighting, framing identical.
```

---

## SH03 — Ratna menjelaskan usaha · MEDIUM · 50mm
**START attachments:** `E05_sudutkerja_meja.png` + `R_ratna_hijab_front_medium.png`.
- **START** — mode **B** (full master, 1-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E05_sudutkerja_meja.png — same prep worktable, same tablet on a stand, same work corner, faithful match"],
    "identity_reference": ["R_ratna_hijab_front_medium.png — same identical woman, matched face, headscarf, early-forties"]
  },
  "mood": "earnest explaining moment, warm working register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a woman at her prep worktable facing a propped tablet plain neutral slab, headscarf, apron, warm midday window light",
  "location": "indoor",
  "time_of_day": "midday",
  "atmosphere": "warm midday window light, focused calm",
  "scene_depth": {
    "foreground": "worktable edge low frame",
    "midground": "Ratna at the worktable, the propped tablet before her",
    "background": "wall rack, window, soft"
  },
  "subjects": [ { "who": "Ratna", "identity_reference": "R_ratna_hijab_front_medium.png" } ],
  "subject_state": "static",
  "action": "Ratna at the worktable speaking toward the tablet, explaining",
  "pose": "Ratna seated at the prep worktable facing the propped tablet, upright, hands resting on the worktable, eyes on the screen",
  "gesture": "lips parted speaking, attention on the screen",
  "expression": "warm earnest, explaining her business",
  "grooming": "neat headscarf",
  "wardrobe": "headscarf, modest tunic, work apron",
  "framing": "medium shot, Ratna head to waist, the tablet on its stand foreground edge",
  "angle": "eye-level, facing Ratna at the worktable",
  "camera": "50mm prime spherical, shallow depth of field, focus on Ratna",
  "lighting": "warm midday daylight from the window, soft warm key, gentle fill, plain neutral tablet glow on her front",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, warm window wrap, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta home, working frozen-food corner",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working grooming under a headscarf"
}
```
- **END** — EDIT-IN-PLACE (delta: Ratna gestur tangan ringan menjelaskan) · STATUS: ✅ authored:
```
Change only Ratna gesture, position held.

- Ratna: now one open hand raised in a small explaining gesture near the worktable, mid-sentence, warm, eyes on the screen
- unchanged: framing unchanged, camera angle unchanged, Ratna seated position unchanged, tablet on its stand unchanged, worktable unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH04 — Insert layar: data + kartu pembiayaan · CLOSE · 85mm
**START attachments:** `E05_sudutkerja_meja.png` (latar). **A1: layar slab polos; data + kartu "Pembiayaan UMKM" + feed = AE.**
- **START** — mode **B** (object insert) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E05_sudutkerja_meja.png — same prep worktable, same tablet on a stand, identical insert geometry, faithful match"]
  },
  "mood": "the data coming together, an offer arriving, warm register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic material rendering",
  "scene": "a tablet propped on a stand, screen a plain bright neutral glowing slab blank featureless, on a stainless prep worktable, warm midday ambient",
  "location": "indoor",
  "time_of_day": "midday",
  "atmosphere": "warm midday ambient, soft",
  "scene_depth": {
    "foreground": "worktable surface at the stand base",
    "midground": "the tablet screen, plain neutral glowing slab, sharp",
    "background": "soft out-of-focus wall rack, warm light"
  },
  "subject_state": "static",
  "action": "the tablet glowing plain, data on screen",
  "framing": "close insert, the tablet screen frame-dominant",
  "angle": "facing the tablet screen, eye-level at worktable height",
  "camera": "85mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "plain neutral tablet glow as local key, warm midday ambient fill, soft",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta home"
}
```
- **END** — minimal-hold (riwayat transaksi + kartu pembiayaan + feed = AE) · STATUS: ✅ authored:
```
Hold identical to START — no still-frame delta. The transaction-history summary (credit data), the "Pembiayaan UMKM" financing card sliding in at the corner, and the officer feed = After Effects overlays on the plain slab. Keep frame, screen slab, lighting, framing identical.
```

---

## SH05 — Ratna mengajukan · MEDIUM · 50mm
**START attachments:** `E05_sudutkerja_meja.png` + `R_ratna_hijab_front_medium.png`.
- **START** — mode **B** (full master, 1-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E05_sudutkerja_meja.png — same prep worktable, same tablet on a stand, same work corner, faithful match"],
    "identity_reference": ["R_ratna_hijab_front_medium.png — same identical woman, matched face, headscarf, early-forties"]
  },
  "mood": "a decisive hopeful moment, applying, warm register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a woman at her prep worktable facing a propped tablet plain neutral slab, headscarf, apron, warm midday window light",
  "location": "indoor",
  "time_of_day": "midday",
  "atmosphere": "warm midday window light, hopeful calm",
  "scene_depth": {
    "foreground": "worktable edge low frame",
    "midground": "Ratna at the worktable, the propped tablet before her",
    "background": "wall rack, window, soft"
  },
  "subjects": [ { "who": "Ratna", "identity_reference": "R_ratna_hijab_front_medium.png" } ],
  "subject_state": "static",
  "action": "Ratna at the worktable nodding at the tablet, about to apply",
  "pose": "Ratna seated at the prep worktable facing the tablet, a small nod, one hand near the tablet screen",
  "gesture": "a nod, hand approaching the screen",
  "expression": "warm decided, hopeful",
  "grooming": "neat headscarf",
  "wardrobe": "headscarf, modest tunic, work apron",
  "framing": "medium shot, Ratna head to waist, the tablet on its stand foreground edge",
  "angle": "eye-level, facing Ratna at the worktable",
  "camera": "50mm prime spherical, shallow depth of field, focus on Ratna",
  "lighting": "warm midday daylight from the window, soft warm key, gentle fill, plain neutral tablet glow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, warm window wrap, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta home, working frozen-food corner",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working grooming under a headscarf"
}
```
- **END** — EDIT-IN-PLACE (delta: Ratna tekan "ajukan"; status "diproses"=AE) · STATUS: ✅ authored:
```
Change only Ratna hand gesture, position held.

- Ratna: now one index finger pressed to the tablet screen, a single confirming tap, head lifted from the nod, a small satisfied breath
- unchanged: framing unchanged, camera angle unchanged, Ratna seated position unchanged, tablet on its stand unchanged, worktable unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## Status board
| Shot | START | END | Render |
|---|---|---|---|
| SH01 | ✅ authored | ✅ authored | pending (final batch) |
| SH02 | ✅ authored | ✅ hold (AE feed) | pending (final batch) |
| SH03 | ✅ authored | ✅ authored | pending (final batch) |
| SH04 | ✅ authored | ✅ hold (AE data) | pending (final batch) |
| SH05 | ✅ authored | ✅ authored | pending (final batch) |

**Ladder:** MW→CU→M→CU→M. **Grade siang hangat** (GATE B). **Camera-lock:** Ratna stasioner, delta gestur in-frame. **A1:** tablet = slab polos (ruang tunggu + feed petugas F3 + data kredit + kartu "Pembiayaan UMKM" + "Diproses" = AE). **DEVICE = tablet-on-stand** (rekonsiliasi dari all-in-one; kanon 2026-07-01). **Modesty:** Ratna berhijab+celemek (petugas non-mahram via kamera). 1 subjek fisik. **Plates E05 + Ratna semua di disk** — SC08 siap generate.
