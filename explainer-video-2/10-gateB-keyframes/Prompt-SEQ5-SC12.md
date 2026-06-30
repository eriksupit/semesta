---
title: GATE B Prompt — SEQ5-SC12 (INT. TERMINAL TRANSJAKARTA — 17.30)
tags: [explainer-video-2, gate-b, prompt, status, SEQ5-SC12]
status: authoring
created: 2026-07-01
updated: 2026-07-01
aliases: [ev2-prompt-seq5-sc12]
---

# GATE B Prompt — SEQ5-SC12
## INT. TERMINAL TRANSJAKARTA — 17.30 WIB *(SEQ5, 1 scene)*

> **Konvensi dua-doc:** prompt GATE B + status. Narasi = `SEQ5-SC12.md`. Env = `E13-terminal.md`. Figuran `F10 bapak desa`. Arus penumpang = ambient crowd (tak face-locked).
> **Pola seragam (SC01–SC11):** START full-prompt + attachment → END edit-in-place. Camera-lock: Lisa no-transit (hadir di-START), bapak stasioner bersandar tongkat, delta gestur in-frame. **OOH digital raksasa dinding = hero surface tapi OFF/polos** (A1: iklan bergerak = AE). Device screen OFF/polos (A1: jadwal = AE). Grade **senja** (GATE B). **Lisa uncovered**; bapak non-mahram → **gestur syukur NON-SENTUH** (mangguk + tangkup tangan), jarak sopan. Bookend transport-pagi SC03.

## Manifest attachment
- **Env E13 (⚠ PENDING final-batch):** `E13_terminal_master.png` (peron + OOH wall + arus, WIDE) · `E13_terminal_peron.png` (peron MS).
- **Karakter:** `L_lisa_front_{full,medium}` (✓) · `F_bapakdesa_front_{full,medium}` (⚠ PENDING — figuran F10; **verify aged ~early-sixties, jangan de-aged, plat-pertama**).
- **Generate-order final-batch:** E13 master+peron + F_bapakdesa plate **sebelum** keyframe SC12.

---

## SH01 — Establishing terminal + OOH · WIDE · 24mm
**START attachments:** `E13_terminal_master.png` (PENDING) + `L_lisa_front_full.png` + `F_bapakdesa_front_full.png` (PENDING).
- **START** — mode **B** (full master, 2-subjek fg + OOH + crowd ambient) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E13_terminal_master.png — same rapid-transit terminal platform, same giant wall display, same schedule board, same layout, same handedness, faithful match"],
    "identity_reference": ["L_lisa_front_full.png — same identical young woman, matched face, uncovered hair, early-twenties", "F_bapakdesa_front_full.png — same identical elderly village man, matched face, early-sixties, lined weathered face, gray hair, peci"]
  },
  "mood": "warm dusk transit hub, equal-to-all calm, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a rapid-transit bus terminal platform at dusk, platform lights on, a giant digital wall display glowing a plain neutral slab above the passenger flow, a schedule board, anonymous commuters moving",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "dusk platform light, warm lamps, busy quiet",
  "scene_depth": {
    "foreground": "platform floor low frame",
    "midground": "Lisa, the elderly village man near the schedule board",
    "background": "the giant wall display plain neutral slab, soft anonymous commuter flow, dusk beyond"
  },
  "subjects": [
    { "who": "Lisa", "identity_reference": "L_lisa_front_full.png" },
    { "who": "bapak desa", "identity_reference": "F_bapakdesa_front_full.png" }
  ],
  "subject_state": "static",
  "action": "the elderly man near the schedule board, Lisa nearby, commuters moving, the giant display glowing",
  "pose": "the elderly man standing camera-right near the schedule board, one hand on a wooden cane, peci on his head, Lisa standing camera-left a polite distance away, soft anonymous commuters moving behind",
  "gesture": "the man steadying on his cane, Lisa near, the background commuters in motion",
  "expression": "the man patient squinting, Lisa attentive kind, the crowd anonymous",
  "grooming": "the man gray hair under a peci, lined face, Lisa loose uncovered hair",
  "wardrobe": "the man modest village clothes, peci, a wooden cane, Lisa casual long-sleeve top, jeans, shoulder bag",
  "framing": "wide establishing, the platform, the giant wall display, two foreground figures, commuter flow",
  "angle": "eye-level, along the platform, the OOH wall in frame",
  "camera": "24mm prime spherical, deep focus front to back",
  "lighting": "dusk platform light, warm overhead lamps, soft glow from the wall display, cool dusk beyond the openings, warm-cool balance",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, mixed lamp dusk, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian transit terminal realism, lived-in public space",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: bapak menengadah ke papan, Lisa menoleh; crowd ambient) · STATUS: ✅ authored:
```
Change only the two foreground figures, the background crowd held in soft motion.

- bapak desa: now his head tilted up toward the schedule board, squinting
- Lisa: now turned toward the elderly man, a kind attentive look
- unchanged: framing unchanged, camera angle unchanged, both standing positions unchanged, the polite distance between them unchanged, the giant wall display plain slab unchanged, schedule board unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH02 — Bapak memicingkan mata ke papan jadwal · MEDIUM · 50mm
**START attachments:** `E13_terminal_peron.png` (PENDING) + `F_bapakdesa_front_medium.png` (PENDING).
- **START** — mode **B** (full master, 1-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E13_terminal_peron.png — same terminal platform, same schedule board, faithful match"],
    "identity_reference": ["F_bapakdesa_front_medium.png — same identical elderly village man, matched face, early-sixties, lined weathered face, gray hair, peci"]
  },
  "mood": "an older man straining to read, quiet patience, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "an elderly village man on a transit platform squinting at a distant schedule board, one hand on a cane, dusk platform light",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "dusk platform light, warm lamps",
  "scene_depth": {
    "foreground": "platform floor low frame",
    "midground": "the elderly man, hand on the cane, squinting",
    "background": "the schedule board soft, dusk platform"
  },
  "subjects": [ { "who": "bapak desa", "identity_reference": "F_bapakdesa_front_medium.png" } ],
  "subject_state": "static",
  "action": "the elderly man looking toward the schedule board, hand on the cane",
  "pose": "the elderly man standing, one hand on the wooden cane, head toward the schedule board, peci on his head",
  "gesture": "hand steady on the cane, head toward the board",
  "expression": "patient, eyes beginning to narrow",
  "grooming": "gray hair under a peci, lined weathered face",
  "wardrobe": "modest village clothes, peci, wooden cane",
  "framing": "medium shot, the elderly man head to waist, schedule board soft behind",
  "angle": "eye-level, facing the man, board behind",
  "camera": "50mm prime spherical, shallow depth of field, focus on the man",
  "lighting": "dusk platform light, warm overhead lamps, soft fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, warm lamp dusk, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian transit terminal realism, lived-in public space",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte mature lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat mature grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: bapak memicingkan mata + sedikit condong) · STATUS: ✅ authored:
```
Change only the expression and posture, position held.

- bapak desa: now his eyes squinting hard, his head leaned a little forward toward the board, struggling to read
- unchanged: framing unchanged, camera angle unchanged, standing position unchanged, cane unchanged, board unchanged, lighting unchanged, color grade unchanged, face matching attached plate
```

---

## SH03 — Insert HP Lisa (jadwal kedatangan) · CLOSE · 85mm
**START attachments:** `L_lisa_front_medium.png` (tangan). **A1: layar slab polos; "Kedatangan [jam]" = AE.**
- **START** — mode **B** (insert tangan+HP) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "identity_reference": ["L_lisa_front_medium.png — same identical young woman hand, matched skin tone, sleeve cuff"]
  },
  "mood": "a small helpful answer, a way home in a tap, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a young woman hand holding a smartphone tilted toward an older man, screen off dark neutral blank slab, dusk platform light",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "dusk platform light, soft",
  "scene_depth": {
    "foreground": "thumb at the phone edge",
    "midground": "smartphone tilted in hand, screen off dark neutral, sharp",
    "background": "soft out-of-focus platform, dusk lamps"
  },
  "subjects": [ { "who": "Lisa hand", "identity_reference": "L_lisa_front_medium.png" } ],
  "subject_state": "static",
  "action": "a hand holding the phone tilted, screen off, showing",
  "pose": "Lisa hand holding a smartphone tilted toward the older man, thumb at the lower screen",
  "gesture": "thumb at the screen edge, presenting",
  "framing": "close-up insert, the hand, the tilted smartphone, screen frame-dominant",
  "angle": "downward onto the tilted screen, eye-level lowered",
  "camera": "85mm prime spherical, shallow depth of field, focus on the screen plane",
  "lighting": "dusk platform light soft on the hand, even key, phone screen off dark neutral, faint warm reflection",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, warm lamp dusk, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian transit terminal realism"
}
```
- **END** — minimal-hold ("Kedatangan [jam]" = AE; jempol diam) · STATUS: ✅ authored:
```
Hold near-identical to START — the thumb stays steady at the screen edge, presenting. The bus arrival schedule "Kedatangan [jam]" = After Effects overlay on the plain slab. Keep frame, hand, screen slab, lighting, framing identical.
```

---

## SH04 — Lisa menunjukkan jadwal ke bapak · MEDIUM 2-shot · 50mm
**START attachments:** `E13_terminal_peron.png` (PENDING) + `L_lisa_front_medium.png` + `F_bapakdesa_front_medium.png` (PENDING). **Jarak sopan non-sentuh.**
- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E13_terminal_peron.png — same terminal platform, same schedule board, faithful match"],
    "identity_reference": ["L_lisa_front_medium.png — same identical young woman, matched face, uncovered hair, early-twenties", "F_bapakdesa_front_medium.png — same identical elderly village man, matched face, early-sixties, peci"]
  },
  "mood": "a kind cross-generation help, equal-to-anyone, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "a young woman showing her phone to an elderly man on a transit platform, a polite distance between them, dusk platform light",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "dusk platform light, warm lamps",
  "scene_depth": {
    "foreground": "platform floor low frame",
    "midground": "Lisa holding the phone toward the man, the man reading",
    "background": "schedule board, dusk platform"
  },
  "subjects": [
    { "who": "Lisa", "identity_reference": "L_lisa_front_medium.png" },
    { "who": "bapak desa", "identity_reference": "F_bapakdesa_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "Lisa holding the phone toward the man at a polite distance, the man reading",
  "pose": "Lisa standing camera-left holding the phone tilted toward the man, an arm-length polite gap, the man camera-right leaned toward the screen reading, a hand on his cane",
  "gesture": "Lisa presenting the phone, the man reading, a respectful gap between them",
  "expression": "Lisa kind helpful, the man focused grateful",
  "grooming": "Lisa loose uncovered hair, the man gray hair under a peci",
  "wardrobe": "Lisa casual top, jeans, the man village clothes, peci, cane",
  "framing": "medium two-shot, Lisa head to waist camera-left, the man head to chest camera-right, the phone between, a polite gap",
  "angle": "eye-level, facing the two, polite distance held",
  "camera": "50mm prime spherical, shallow depth of field, focus on the man",
  "lighting": "dusk platform light, warm overhead lamps, soft fill",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, warm lamp dusk, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian transit terminal realism, lived-in public space",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: bapak membaca, Lisa menjelaskan singkat; jarak sopan non-sentuh) · STATUS: ✅ authored:
```
Change only the gestures, the polite distance held, no contact.

- bapak desa: now reading the screen, a small understanding nod
- Lisa: a small open explaining gesture of her free hand, warm
- unchanged: framing unchanged, camera angle unchanged, both standing positions unchanged, the polite arm-length gap between them unchanged with no contact, schedule board unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## SH05 — Bapak berterima kasih (OOH di latar) · WIDE 2-shot · 35mm
**START attachments:** `E13_terminal_master.png` (PENDING) + `L_lisa_front_full.png` + `F_bapakdesa_front_full.png` (PENDING). **Gestur NON-SENTUH; OOH wall latar.**
- **START** — mode **B** (full master, 2-subjek + OOH ambient) · STATUS: ✅ authored:
```json
{
  "attachment_manifest": {
    "environment_reference": ["E13_terminal_master.png — same terminal platform, same giant wall display, faithful match"],
    "identity_reference": ["L_lisa_front_full.png — same identical young woman, matched face, uncovered hair, early-twenties", "F_bapakdesa_front_full.png — same identical elderly village man, matched face, early-sixties, peci"]
  },
  "mood": "warm equal-to-all gratitude, dusk hub, gentle register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "an elderly man thanking a young woman on a transit platform, a polite distance between them, a giant digital wall display glowing plain neutral slab behind, commuter flow, dusk",
  "location": "indoor",
  "time_of_day": "evening",
  "atmosphere": "dusk platform light, soft glow, busy quiet",
  "scene_depth": {
    "foreground": "platform floor low frame",
    "midground": "the elderly man, Lisa standing a polite distance apart",
    "background": "the giant wall display plain neutral slab, commuter flow, dusk"
  },
  "subjects": [
    { "who": "Lisa", "identity_reference": "L_lisa_front_full.png" },
    { "who": "bapak desa", "identity_reference": "F_bapakdesa_front_full.png" }
  ],
  "subject_state": "static",
  "action": "the elderly man nodding to Lisa, a polite gap between them, the giant display glowing behind",
  "pose": "the elderly man standing camera-right, one hand on his cane, a grateful nod toward Lisa, Lisa standing camera-left a polite distance away, the giant wall display behind, soft commuters moving",
  "gesture": "the man a grateful nod, Lisa a warm small nod back, a respectful gap between them",
  "expression": "both warm, the man grateful, Lisa kind",
  "grooming": "the man gray hair under a peci, Lisa loose uncovered hair",
  "wardrobe": "the man village clothes, peci, cane, Lisa casual top, jeans",
  "framing": "wide two-shot, both full figures a polite distance apart, the OOH wall behind, commuter flow",
  "angle": "eye-level, pulled back, both figures, the OOH wall in frame",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "dusk platform light, warm overhead lamps, soft glow from the wall display, cool dusk beyond",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic everyday observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light realism, mixed lamp dusk, soft fill",
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian transit terminal realism, lived-in public space",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat grooming"
}
```
- **END** — EDIT-IN-PLACE (delta: bapak menangkupkan kedua tangan terima kasih NON-SENTUH; OOH bergerak=AE) · STATUS: ✅ authored:
```
Change only the elderly man gesture, the polite distance held, no contact, the background crowd in soft motion.

- bapak desa: now both palms brought together at his chest in a grateful cupped-hands thank-you, a warm bow of the head, no contact with Lisa
- Lisa: a warm small nod, a kind smile, hands at her sides
- unchanged: framing unchanged, camera angle unchanged, both standing positions unchanged, the polite gap between them unchanged with no contact, the giant wall display plain slab unchanged, lighting unchanged, color grade unchanged, faces matching attached plates
```

---

## Status board
| Shot | START | END | Render |
|---|---|---|---|
| SH01 | ✅ authored | ✅ authored | pending (final batch) |
| SH02 | ✅ authored | ✅ authored | pending (final batch) |
| SH03 | ✅ authored | ✅ hold (AE schedule) | pending (final batch) |
| SH04 | ✅ authored | ✅ authored | pending (final batch) |
| SH05 | ✅ authored | ✅ authored | pending (final batch) |

**Ladder:** W→M→CU→M→W. **Grade senja** (GATE B). **Camera-lock:** Lisa no-transit (hadir START), bapak stasioner bersandar tongkat; delta gestur in-frame; crowd + OOH = ambient soft. **A1:** OOH wall raksasa + HP = slab polos (iklan bergerak hero + jadwal = AE). **Modesty:** Lisa↔bapak NON-MAHRAM → **gestur syukur NON-SENTUH** (mangguk + tangkup tangan), jarak sopan dipertahankan tiap shot. **Bookend** transport-pagi SC03. **⚠ PENDING plates:** `E13_terminal_{master,peron}` + `F_bapakdesa_front_{full,medium}` (F10 — verify aged ~early-sixties plat-pertama).
