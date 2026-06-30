---
title: GATE B Prompt — SEQ2-SC05 (INT. KANTOR EKSPOR-IMPOR — 08.30)
tags: [explainer-video-2, gate-b, prompt, status, SEQ2-SC05]
status: authoring
created: 2026-07-01
updated: 2026-07-01
aliases: [ev2-prompt-seq2-sc05]
---

# GATE B Prompt — SEQ2-SC05
## INT. KANTOR EKSPOR-IMPOR — 08.30 WIB

> **Konvensi dua-doc:** prompt GATE B + status. Narasi = `SEQ2-SC05.md`. Env = `E08-kantor.md` (dipakai 2× SC05+SC10).
> **Pola seragam (SC01–SC04):** START full-prompt + attachment → END edit-in-place. Camera-lock: angle+framing identik, delta gestur in-frame; Rian stasioner (no transit). **Monitor besar = slab polos** (A1: papan kerja/dokumen/kontainer/kanban + placement B2B = AE; aman dari melt). Grade pagi terang kantor (GATE B). Figuran-first.

## Manifest attachment
- **Env E08 (⚠ PENDING final-batch):** `E08_kantor_master.png` (deret meja + dinding peta rute) · `E08_kantor_meja.png` (meja Herman + monitor besar).
- **Karakter:** `H_herman_front_{full,medium}` (✓) · `F_rian_front_medium` (✓ figuran F4).
- **Generate-order final-batch:** E08 master+meja **sebelum** keyframe SC05.

---

## SH01 — Establishing kantor · WIDE · 24mm
**START attachments:** `E08_kantor_master.png` (PENDING) + `H_herman_front_full.png`.
- **START** — mode **B** (full master, 1-subjek fokus + figuran latar) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E08_kantor_master.png — same export-import office, same desk rows, same route-map wall, same layout, same handedness, faithful match"],
    "identity_reference": ["H_herman_front_full.png — same identical man, matched face, clean-shaven, mid-forties"]
  },
  "mood": "calm busy professional morning, quiet competence, ordinary workplace register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "export-import office morning, rows of work desks, monitors glowing plain neutral slabs, a shipping route map on the wall, staff at work, bright office daylight",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "bright morning office light, calm working hum",
  "scene_depth": {
    "foreground": "near desk edge low frame",
    "midground": "Herman seated at his desk centre, a large monitor before him",
    "background": "desk rows, soft background staff, route-map wall"
  },
  "subjects": [ { "who": "Herman", "identity_reference": "H_herman_front_full.png" } ],
  "subject_state": "static",
  "action": "Herman seated at his desk, the office working around him",
  "pose": "Herman seated centre at his desk, hands on the desk before a large monitor, upright, soft background staff at their desks",
  "gesture": "Herman hands resting at the keyboard, attention on the monitor",
  "expression": "calm focused professional",
  "grooming": "neat short hair, clean-shaven",
  "wardrobe": "plain collared work shirt, dark trousers",
  "framing": "wide establishing, desk rows, Herman small at his desk centre, route-map wall background",
  "angle": "eye-level, from the back of the room facing the desk rows",
  "camera": "24mm prime spherical, deep focus front to back",
  "lighting": "bright morning daylight from office windows camera-left, even cool-neutral office fill, soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "naturalistic workplace observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, soft even fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "contract-institutional office realism, lived-in workplace",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Herman membuka tampilan ruang kerja di monitor; staf latar stasioner) · STATUS: ✅ authored:
```
Change only Herman gesture, background staff held still.

- Herman: now one hand on the mouse, the other at the keyboard, leaned slightly toward the monitor, the large monitor glowing a brighter plain neutral slab
- unchanged: framing unchanged, camera angle unchanged, Herman seated position unchanged, desk rows unchanged, background staff positions unchanged, route-map wall unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH02 — Rekan menunjuk layar · MEDIUM 2-shot · 50mm
**START attachments:** `E08_kantor_meja.png` (PENDING) + `H_herman_front_medium.png` + `F_rian_front_medium.png`.
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored. **Rian stasioner.**
```json
{
  "attachment_manifest": {
    "environment_reference": ["E08_kantor_meja.png — same desk, same large monitor, same office, faithful match"],
    "identity_reference": ["H_herman_front_medium.png — same identical man, matched face, mid-forties", "F_rian_front_medium.png — same identical colleague man, matched face, distinctive features"]
  },
  "mood": "collegial professional morning, a small work exchange, ordinary workplace register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a work desk, a large monitor glowing plain neutral slab, a seated man, a standing colleague holding a coffee cup, bright office daylight",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "bright morning office light, calm",
  "scene_depth": {
    "foreground": "desk edge low frame",
    "midground": "Herman seated camera-left, Rian standing camera-right beside the desk",
    "background": "office desks soft, route-map wall"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_medium.png" },
    { "who": "Rian", "identity_reference": "F_rian_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "Herman seated at the monitor, Rian standing beside the desk holding coffee",
  "pose": "Herman seated camera-left facing the monitor, Rian standing camera-right at the desk side, a coffee cup in one hand, the other hand at his side",
  "gesture": "Herman eyes on the screen, Rian holding the cup, ready to point",
  "expression": "both calm, attentive, collegial",
  "grooming": "Herman neat short hair, Rian neat short hair",
  "wardrobe": "Herman collared work shirt, Rian collared work shirt",
  "framing": "medium two-shot, Herman head to chest seated camera-left, Rian head to waist standing camera-right",
  "angle": "eye-level, from the desk side, both figures, monitor between",
  "camera": "50mm prime spherical, shallow depth of field, focus on Herman",
  "lighting": "bright morning daylight from office windows, even neutral fill, soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "naturalistic workplace observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, soft even fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "contract-institutional office realism, lived-in workplace",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: Rian menunjuk sebaris di layar, Herman ikuti telunjuk) · STATUS: ✅ authored:
```
Change only the gestures, positions held.

- Rian: now one arm extended toward the monitor, index finger pointing at a line on the screen, the coffee cup in the other hand
- Herman: eyes following Rian finger to the screen, a small nod
- unchanged: framing unchanged, camera angle unchanged, both positions unchanged, desk unchanged, monitor unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH03 — Insert monitor (ruang kerja virtual) · CLOSE · 85mm
**START attachments:** `E08_kantor_meja.png` (latar, PENDING) + `H_herman_front_medium.png` (tangan). **A1: layar slab polos; papan kerja=AE.**
- **START** — mode **B** (insert layar+tangan) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E08_kantor_meja.png — same desk, same large monitor, soft, faithful match"],
    "identity_reference": ["H_herman_front_medium.png — same identical man hand, matched skin tone, sleeve cuff"]
  },
  "mood": "focused work moment, a board coming together, ordinary workplace register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a large desktop monitor screen, plain neutral glowing slab blank featureless, a hand on a mouse at the desk edge, bright office ambient",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "bright office ambient, soft",
  "scene_depth": {
    "foreground": "hand on the mouse low frame",
    "midground": "the large monitor screen, plain neutral glowing slab, sharp",
    "background": "soft out-of-focus desk, office"
  },
  "subjects": [ { "who": "Herman hand", "identity_reference": "H_herman_front_medium.png" } ],
  "subject_state": "static",
  "action": "the monitor glowing plain, a hand resting on the mouse",
  "pose": "Herman warm brown Southeast-Asian hand resting on a mouse at the desk edge, the large monitor a plain neutral glowing slab above",
  "gesture": "fingers on the mouse, ready",
  "framing": "close insert, the monitor screen frame-dominant, the hand on the mouse lower frame",
  "angle": "from behind-side onto the screen, eye-level at desk height",
  "camera": "85mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "plain neutral monitor glow as local key, bright office ambient fill, soft",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "naturalistic workplace observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, soft even fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "contract-institutional office realism"
}
```
- **END** — EDIT-IN-PLACE (delta: kursor/tangan Herman menyentuh satu kartu) · STATUS: ✅ authored:
```
Change only the hand: Herman clicks a card.

- pose: Herman index finger now pressing the mouse button, the hand steady, a small click action, the cursor at a card on the plain slab
- unchanged: framing unchanged, camera angle unchanged, hand position unchanged, monitor plain neutral slab unchanged, desk unchanged, lighting unchanged, color grade unchanged
```

---

## SH04 — Herman geser kartu tugas · MEDIUM · 50mm
**START attachments:** `E08_kantor_meja.png` (PENDING) + `H_herman_front_medium.png`.
- **START** — mode **B** (full master, 1-subjek, Rian soft tepi) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E08_kantor_meja.png — same desk, same large monitor, same office, faithful match"],
    "identity_reference": ["H_herman_front_medium.png — same identical man, matched face, mid-forties"]
  },
  "mood": "focused collaborative morning, ordinary workplace register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a man at his desk before a large monitor glowing plain neutral slab, a colleague soft at the frame edge, bright office daylight",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "bright morning office light, calm",
  "scene_depth": {
    "foreground": "desk edge low frame",
    "midground": "Herman seated facing the monitor, one hand on the mouse",
    "background": "Rian soft at the camera-right edge, office desks"
  },
  "subjects": [ { "who": "Herman", "identity_reference": "H_herman_front_medium.png" } ],
  "subject_state": "static",
  "action": "Herman at the monitor, a nod, hand on the mouse",
  "pose": "Herman seated facing the monitor, head in a small nod, one hand on the mouse, the other on the desk, Rian soft partial at the camera-right edge",
  "gesture": "Herman nodding, hand on the mouse",
  "expression": "calm agreeing focus",
  "grooming": "neat short hair, clean-shaven",
  "wardrobe": "collared work shirt",
  "framing": "medium shot, Herman head to chest centre, monitor camera-right, Rian soft edge",
  "angle": "eye-level, facing Herman at the desk",
  "camera": "50mm prime spherical, shallow depth of field, focus on Herman",
  "lighting": "bright morning daylight, even neutral office fill, soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "naturalistic workplace observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, soft even fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "contract-institutional office realism, lived-in workplace",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: tangan Herman menggeser kartu; kartu pindah=AE) · STATUS: ✅ authored:
```
Change only the hand gesture.

- Herman: now the mouse hand moved across to the side, a drag gesture on the desk, eyes on the monitor, head lifted from the nod
- unchanged: framing unchanged, camera angle unchanged, Herman seated position unchanged, monitor plain neutral slab unchanged, Rian soft edge unchanged, desk unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH05 — Keduanya membaca papan yang sama · MEDIUM-WIDE 2-shot · 35mm
**START attachments:** `E08_kantor_meja.png` (PENDING) + `H_herman_front_medium.png` + `F_rian_front_medium.png`.
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E08_kantor_meja.png — same desk, same large monitor, same office, faithful match"],
    "identity_reference": ["H_herman_front_medium.png — same identical man, matched face, mid-forties", "F_rian_front_medium.png — same identical colleague man, matched face"]
  },
  "mood": "shared focus collaboration, quiet competence, ordinary workplace register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a desk, a large monitor glowing plain neutral slab, a seated man, a standing colleague, both facing the same screen, bright office daylight",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "bright morning office light, calm focus",
  "scene_depth": {
    "foreground": "desk edge low frame",
    "midground": "Herman seated camera-left, Rian standing camera-right, the monitor between them",
    "background": "office desks soft, route-map wall"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_medium.png" },
    { "who": "Rian", "identity_reference": "F_rian_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "both turned toward the monitor, reading the same board",
  "pose": "Herman seated camera-left turned to the monitor, Rian standing camera-right leaned toward the same screen, both gazes on the monitor",
  "gesture": "both attention on the screen",
  "expression": "both focused, engaged, collegial",
  "grooming": "both neat short hair",
  "wardrobe": "both collared work shirts",
  "framing": "medium-wide two-shot, Herman seated camera-left, Rian standing camera-right, monitor centre, desk",
  "angle": "eye-level, pulled back, both figures, monitor centre",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "bright morning daylight from office windows, even neutral fill, soft shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "naturalistic workplace observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, soft even fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "contract-institutional office realism, lived-in workplace",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: keduanya fokus baca, Herman menunjuk balik) · STATUS: ✅ authored:
```
Change only the gestures, positions held.

- Herman: now one hand raised toward the monitor, index finger pointing back at a spot on the board, eyes on the screen
- Rian: leaned in, gaze following Herman point, a small nod
- unchanged: framing unchanged, camera angle unchanged, both positions unchanged, monitor plain neutral slab unchanged, desk unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
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

**Ladder:** W→M→CU→M→MW. **Grade pagi terang kantor** (GATE B). **Camera-lock:** Rian stasioner; delta gestur in-frame; bg staff stasioner. **A1:** monitor = slab polos (papan kerja/dokumen/kontainer/kanban + B2B placement = AE; monitor besar aman melt). **⚠ PENDING plates:** `E08_kantor_{master,meja}` (dipakai 2× SC05+SC10).
