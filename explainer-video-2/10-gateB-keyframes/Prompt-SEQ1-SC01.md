---
title: GATE B Prompt — SEQ1-SC01 (INT. KAMAR HERMAN — 04.40)
tags: [explainer-video-2, gate-b, prompt, status, SEQ1-SC01]
status: authoring
created: 2026-06-30
updated: 2026-06-30
aliases: [ev2-prompt-seq1-sc01]
---

# GATE B Prompt — SEQ1-SC01
## INT. KAMAR HERMAN — 04.40 WIB

> **Konvensi dua-doc (`06` Langkah 2):** doc ini = **prompt GATE B + status produksi per-shot**. Narasi shot (sumber) ada di **`SEQ1-SC01.md`**. Cerita: `03-scene-detail.md`.
>
> **⚠️ RENDER LAMA SUPERSEDED (2026-06-30):** 8 render lama `scene-images/sc01/sc01_sh0{1..4}_{start,end}.png` dibuat dari prompt lama (struktur **4 shot**, metode heterogen). Breakdown A2 baru = **5 shot** dengan pola seragam → render lama tidak dipakai; SC01 di-generate ulang dari prompt baru di bawah. Prompt lama tetap di git history.

## Acuan kanonik (jangan duplikasi — pointer saja)
- **Metode prompting (BINDING):** `prompt-rules-text-image-to-image.md` (diagnosis · Part I hukum · Part II grammar 3-mode + camera-lock + edit-in-place · Part V struktur + template JSON · enforcement G0–G6). Dibangun di atas 6-lapis `prompt-rules-image-generation.md`.
- **Pre-lock audit:** `PROMPT-AUDIT-CHECKLIST.md` (52 item) via `/tti-prompt-audit`. Tulis baru via `/tti-prompt-creator` (loop sampai COMPLIANT).

## Pola seragam (semua shot)
**START = master full-prompt + attachment → END = derivative edit-in-place (+ attachment bila perlu).** START selalu full prompt (master/angle-child, bukan edit). END = edit-in-place pada render START accepted (nol preamble nama-file; operasi+delta+lock-list). Device screen OFF (ADDENDUM A1; UI di AE). Grade subuh: cool-blue di `lighting`, hangat di `color_grade`. Accept → rename `sc01_sh0N_{start,end}.png` → update status di sini.

## Manifest attachment (plat tersedia di disk)
- **Env E01 kamar:** `E01_kamar_master.png` (layout+handedness) · `E01_kamar_bed3q.png` (angle kanan-diagonal) · `E01_kamar_bed4q.png` (angle kaki-ranjang) · `E01_kamar_nightstand.png` (insert nakas).
- **Herman:** `H_herman_front_{closeup,medium,full}` · `profileA/B_*` · `rear_{closeup,medium,full}`.
- **Ratna:** `R_ratna_front_{closeup,medium,full}` · `profileA/B_*` · `rear_*` (uncovered; hijab set ada tapi TAK dipakai di SC01 — mahram-only).

---

## SH01 — Herman terbangun · CU wajah · overhead/diagonal-atas
**SHOT-CONCEPT:** CU wajah Herman supine, kamera overhead/diagonal-atas; pita mata-wajah dominan; 85mm; 16:9. Kamera diam; HANYA mata berubah START→END. Ratna TIDAK di frame (mustahil terbaca di CU; ia hadir SH04–SH05). Grade pra-subuh very-low-key cool-blue.
**START attachments:** `H_herman_front_closeup.png` (identity-lock wajah). *(Ruang tak tampak di CU → tanpa env plate.)*

**Intent (`03`):** START = mata terpejam, lelap. END = mata terbuka, mengerjap, fokus ke langit-langit.

- **START** — mode **B** (master full-prompt, from-scratch) · STATUS: ✅ **PROVEN** (port dari prompt accepted 2026-06-29; konsep identik di breakdown 5-shot → dipakai ulang sebagai master-pola). Token-per-token (Rule 11):
```json
{
  "attachment_manifest": {
    "identity_reference": ["H_herman_front_closeup.png — same identical man, matched face, matched brow, matched eye region, matched skin texture, clean-shaven"]
  },
  "mood": "tender intimate pre-dawn stillness, hushed private waking, quiet domestic register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "soft cotton pillowcase, rumpled bed linen, intimate bedding surface around upturned sleeping face",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "hushed pre-dawn near-darkness, perfectly still",
  "scene_depth": {
    "foreground": "soft out-of-focus lash tips at lens",
    "midground": "upturned face, closed-eye region sharp",
    "background": "rumpled pillow, dark bed linen, deep shadow falloff"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_closeup.png" }
  ],
  "subject_state": "static",
  "action": "face at rest, both eyelids closed, sleep stillness",
  "pose": "head back on pillow, face fully upturned toward overhead lens",
  "gesture": "facial muscles slack, full rest",
  "expression": "both eyelids fully closed, lashes down on cheeks, brow smooth flat relaxed, lips lightly parted, sleep-calm face",
  "framing": "extreme close-up, two closed eyes, bridge of nose, brow above, upper cheeks below, eyes frame-filling",
  "angle": "directly overhead, top-down, straight-down onto upturned face, face square to lens",
  "camera": "85mm prime spherical, shallow depth of field, focus on lash line",
  "lighting": "very low-key, faint cool pre-dawn ambient from off-frame curtained window, dim soft graze across brow, dim soft graze across nose ridge, eye sockets deep shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft wrap, deep honest shadow",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — method **EDIT-IN-PLACE** pada canvas = render START (NOL preamble nama-file; fidelity High) · STATUS: ✅ **PROVEN** (delta: mata terpejam→terbuka, gaze ke langit-langit). Paste di Describe-edits:
```
Change only the eyes state to open, awake.

- expression: both eyelids open but slightly heavy from just waking, irises visible, pupils visible, steady newly-awake upward gaze toward ceiling, faint cool catchlight on wet eye surface, lashes lifted, subtle morning puffiness under the eyes, faint redness along the waterline, slight bloodshot quality in the whites of the eyes, moist tired eye surface, calm sleepy-alert gaze, freshly awakened but not fully energized
- unchanged: framing unchanged, camera angle unchanged, face position on pillow unchanged, brow unchanged, nose unchanged, mouth unchanged, pillowcase unchanged, bed linen unchanged, lighting unchanged, color grade unchanged
```

---

## SH02 — Ponsel di nakas menyala · CU insert · 50mm
**SHOT-CONCEPT:** CU insert nakas+HP, kamera dekat camera-right sedikit menunduk; HP punggung-ke-kamera (layar OFF, A1); 50mm; 16:9. Kamera diam; END menambah tangan Herman masuk meraih + (glow layar = AE). Grade gelap cool-blue.
**START attachments:** `E01_kamar_nightstand.png` (insert nakas) + `E01_kamar_master.png` (layout/handedness).

- **START** — mode **B** (object insert, from-scratch) · STATUS: ✅ authored. Token-per-token:
```json
{
  "attachment_manifest": {
    "environment_reference": [
      "E01_kamar_nightstand.png — same nightstand, same lamp, same surface, identical insert geometry",
      "E01_kamar_master.png — same bedroom layout, same handedness, window camera-left, nightstand camera-right"
    ]
  },
  "mood": "tender intimate pre-dawn stillness, hushed private waking, quiet domestic register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic material rendering",
  "scene": "bedside nightstand top, dark wood surface, smartphone face-up screen-dark, small bedside lamp switched off behind, pre-dawn dimness",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "hushed pre-dawn near-darkness, perfectly still",
  "scene_depth": {
    "foreground": "near edge of the nightstand top, soft focus",
    "midground": "smartphone face-up, screen off dark neutral, sharp",
    "background": "switched-off lamp base, dark wall, deep shadow"
  },
  "subject_state": "static",
  "action": "objects at rest, phone screen off dark, room still",
  "framing": "close-up insert, nightstand top fills frame, phone centred lower third, lamp base upper background",
  "angle": "high angle, slight tilt down onto the nightstand top, from the bed side camera-right",
  "camera": "100mm macro prime spherical, shallow depth of field, focus on the phone",
  "lighting": "very low-key, faint cool pre-dawn ambient from off-frame curtained window camera-left, dim graze across the nightstand top, phone screen off dark, deep shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft wrap, deep honest shadow",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity"
}
```
- **END** — method **EDIT-IN-PLACE** pada render START (NOL preamble nama-file; fidelity High) · delta: layar HP nyala slab cool-blue + tangan Herman masuk meraih · STATUS: ✅ authored:
```
Change only two things: the phone screen turns on, and a hand enters to reach for it.

- phone screen: smartphone screen now on, emitting a plain bright cool blue-white glow, blank featureless cool-white slab, illegible uniform brightness, the glow casting cool blue-white light up onto the nightstand surface and the lamp base, cool reflection on the wood
- hand: a relaxed adult hand, forearm, entering from the bed side camera-right lower edge, warm brown Southeast-Asian skin, fingers extended toward the phone, fingertips suspended a breath above the screen glass
- unchanged: framing unchanged, camera angle unchanged, nightstand position unchanged, lamp position unchanged, phone position unchanged, wall unchanged, color grade unchanged, window ambient unchanged
```

---

## SH03 — Menimang ponsel · MEDIUM · bed3q
**SHOT-CONCEPT:** MEDIUM (kepala+dada+lengan) Herman supine, angle kanan-diagonal `bed3q`, eye-level kasur; nakas in-frame camera-right; 50mm; 16:9. Kamera diam; END = lengan terulur taruh HP ke nakas (masih rebah). Herman bangun-tidur (Rule 20). Grade wajah cool-blue HP-key, ruang shadow.
**START attachments:** `E01_kamar_master.png` (layout) + `E01_kamar_bed3q.png` (angle) + `H_herman_front_medium.png` + `R_ratna_front_medium.png` (dua identity).

- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored. Token-per-token:
```json
{
  "attachment_manifest": {
    "environment_reference": [
      "E01_kamar_master.png — same bedroom layout, same handedness, window camera-left, nightstand camera-right",
      "E01_kamar_bed3q.png — right-diagonal bed vantage, camera angle and bed framing, match this vantage"
    ],
    "identity_reference": [
      "H_herman_front_medium.png — same identical man, matched face, clean-shaven, mid-forties",
      "R_ratna_front_medium.png — same identical woman, matched face, uncovered hair visible, early-forties"
    ]
  },
  "mood": "tender intimate pre-dawn stillness, hushed private waking, quiet domestic register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "double bed, rumpled bed linen, two reclining figures, smartphone screen a plain cool blue-white glowing slab blank featureless, bedside nightstand camera-right, curtained window camera-left, pre-dawn bedroom",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "hushed pre-dawn near-darkness, perfectly still",
  "scene_depth": {
    "foreground": "rumpled blanket edge low frame",
    "midground": "Herman reclining, smartphone held flat on his chest, face under-lit by the screen",
    "background": "Ratna reclining asleep camera-left, dark headboard, deep shadow"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_medium.png" },
    { "who": "Ratna", "identity_reference": "R_ratna_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "Herman holding the phone flat on his chest, gazing down at the screen, Ratna asleep beside him",
  "pose": "Herman supine, head on pillow camera-right, both hands holding a smartphone flat on his chest screen-up toward his face, Ratna supine asleep camera-left, head turned away",
  "gesture": "Herman thumbs resting on the phone edges, Ratna settled still",
  "expression": "Herman just-woken, eyes heavy half-open gazing down at the screen, brow soft, faint under-eye puffiness, lips relaxed, Ratna eyelids closed calm sleep",
  "grooming": "Herman tousled just-woken hair, Ratna loose uncovered hair fanned on the pillow, sleep-creased",
  "framing": "medium shot, Herman head, chest, arms, smartphone on chest, Ratna head, shoulder, camera-left",
  "angle": "right-diagonal bed vantage bed3q, eye-level at mattress height, looking along the bed",
  "camera": "50mm prime spherical, shallow depth of field, focus on Herman face",
  "lighting": "face lit ONLY by strong cool blue-white glow from the phone screen below his face, chin, lower cheeks, nose-tip, brow under-lit cool blue, cool-blue catchlights in his eyes, faint cool pre-dawn ambient from the curtained window camera-left, rest of the room deep shadow, Ratna in cool shadow",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft wrap, deep honest shadow",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — method **EDIT-IN-PLACE** pada render START (NOL preamble; fidelity High) · delta: lengan terulur taruh HP ke nakas, glow padam→ambient remang · lock 2 wajah via `+` (`H_herman_front_medium` + `R_ratna_front_medium`) · STATUS: ✅ authored:
```
Change only the right arm and the light: Herman lowers the phone to the nightstand.

- pose: Herman right arm now extended toward the nightstand camera-right, the smartphone in his fingers lowered onto the nightstand top, arm reaching across, still lying flat on his back
- phone screen: screen now dim, dark, the cool blue-white glow extinguished, face settling into soft ambient shadow
- lighting: face and chest settle back into faint cool pre-dawn ambient from the window camera-left, room in deep shadow, even hush
- unchanged: framing unchanged, camera angle unchanged, Herman head and pillow position unchanged, Ratna asleep unchanged with face matching attached plate, nightstand position unchanged, window unchanged, color grade unchanged
```

---

## SH04 — Lampu nakas menyala · WIDE 2-subjek · bed4q
**SHOT-CONCEPT:** WIDE dari sudut kaki ranjang (`bed4q`), dua figur berbaring; Herman camera-right (sisi nakas), Ratna camera-left uncovered; 35mm; 16:9. Kamera diam; END = lampu nyala (gelap→warm). Rule 18 co-present, Rule 19 dual-plate, Rule 20 bangun-tidur.
**START attachments:** `E01_kamar_master.png` (layout) + `E01_kamar_bed4q.png` (angle) + `H_herman_front_full.png` + `R_ratna_front_full.png` (dua identity).

- **START** — mode **B** (full master, 2-subjek) · STATUS: ✅ authored. Token-per-token:
```json
{
  "attachment_manifest": {
    "environment_reference": [
      "E01_kamar_master.png — same bedroom layout, same handedness, window camera-left, nightstand and lamp camera-right",
      "E01_kamar_bed4q.png — foot-of-bed vantage, camera angle and bed framing, match this vantage"
    ],
    "identity_reference": [
      "H_herman_front_full.png — same identical man, matched face, clean-shaven, mid-forties",
      "R_ratna_front_full.png — same identical woman, matched face, uncovered hair visible, early-forties"
    ]
  },
  "mood": "tender intimate pre-dawn stillness, hushed private waking, quiet domestic register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "double bed, rumpled bed linen, two reclining figures side by side, bedside nightstand, switched-off lamp camera-right, curtained window camera-left, pre-dawn bedroom in near-darkness",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "hushed pre-dawn near-darkness, perfectly still",
  "scene_depth": {
    "foreground": "foot of the bed, blanket over the figures legs",
    "midground": "Herman reclining camera-right, right arm extended toward the lamp, Ratna reclining asleep camera-left",
    "background": "headboard, nightstand, lamp camera-right, curtained window camera-left, dark wall"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_full.png" },
    { "who": "Ratna", "identity_reference": "R_ratna_front_full.png" }
  ],
  "subject_state": "static",
  "action": "Herman right arm extended toward the nightstand lamp switch, fingers at the switch, Ratna asleep beside him",
  "pose": "Herman supine camera-right, head on pillow, right arm extended toward the lamp switch on the nightstand, Ratna supine asleep camera-left, head turned toward the window",
  "gesture": "Herman fingers at the lamp switch, Ratna settled still under the blanket",
  "expression": "Herman just-woken, eyes heavy half-open, brow soft, Ratna eyelids closed calm sleep",
  "grooming": "Herman tousled just-woken hair, Ratna loose uncovered hair fanned on the pillow, sleep-creased",
  "framing": "wide shot, full bed, both reclining figures head to waist, nightstand camera-right, window camera-left",
  "angle": "foot-of-bed vantage bed4q, slightly elevated, looking up the bed toward the headboard",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "very low-key cool pre-dawn ambient from the curtained window camera-left, the room in deep cool-blue near-darkness, the nightstand lamp switched off, dim cool wash over the blanket",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft wrap, deep honest shadow",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — method **EDIT-IN-PLACE** pada render START (NOL preamble; fidelity High) · delta: lampu nakas ON warm dominan camera-right (jendela tetap cool-blue, kontras warm-cool); Ratna mulai menggeliat · lock 2 wajah via `+` (`H_herman_front_full` + `R_ratna_front_full`) · STATUS: ✅ authored:
```
Change only the lamp light and Ratna waking: the nightstand lamp turns on.

- lighting: the nightstand lamp camera-right now on, casting a warm amber glow that fills the room from camera-right, warm key across Herman and the blanket and the bed, the curtained window camera-left staying cool pre-dawn blue, warm-cool contrast across the room
- Ratna: beginning to stir under the blanket, shoulders shifting slightly, eyelids still closed, head turning faintly, face matching attached plate R_ratna_front_full
- Herman: hand resting at the switched-on lamp, face matching attached plate H_herman_front_full, eyes heavy half-open
- unchanged: framing unchanged, camera angle unchanged, both figures positions on the bed unchanged, nightstand position unchanged, window position unchanged, color grade unchanged
```

---

## SH05 — Ratna bangun · MEDIUM · sisi camera-left
**SHOT-CONCEPT:** MEDIUM Ratna, sisi camera-left ranjang, eye-level; warm lamp glow (grade ← SH04-END); 50mm; 16:9. Kamera diam; END = Ratna bangkit duduk + menoleh senyum ke camera-right. Ratna uncovered, rambut tergerai.
**START attachments:** `E01_kamar_master.png` (layout) + `R_ratna_front_medium.png` (identity) + grade-ref `sc01_sh04_end.png` (warm, **dependency final-batch:** SH04-END harus di-generate dulu; saat author = token grade-ref dinamai, di-attach saat generate). *(Generate-order: SH04 sebelum SH05.)*

- **START** — mode **B** (full master, 1-subjek) · framing-by-union (cukup tinggi utk rebah→duduk, Rule 6a/22) · STATUS: ✅ authored. Token-per-token:
```json
{
  "attachment_manifest": {
    "environment_reference": [
      "E01_kamar_master.png — same bedroom layout, same handedness, window camera-left, nightstand and lamp camera-right"
    ],
    "identity_reference": [
      "R_ratna_front_medium.png — same identical woman, matched face, uncovered hair visible, early-forties"
    ],
    "grade_reference": [
      "sc01_sh04_end.png — warm lamp-lit night grade only, warm key from camera-right, match this warmth, ignore its composition, ignore its objects"
    ]
  },
  "mood": "tender intimate waking warmth, hushed private morning, quiet domestic register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",
  "scene": "double bed, rumpled bed linen, one reclining woman camera-left side, bedside lamp glow from camera-right off-frame, curtained window camera-left, warm-lit night bedroom",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "warm lamp-lit hush, settled calm",
  "scene_depth": {
    "foreground": "rumpled blanket low frame",
    "midground": "Ratna reclining on the pillow, head, shoulders, eyes just opening",
    "background": "headboard, dark wall, curtained window camera-left in cool blue"
  },
  "subjects": [
    { "who": "Ratna", "identity_reference": "R_ratna_front_medium.png" }
  ],
  "subject_state": "static",
  "action": "Ratna lying on her pillow, eyes just opening under the warm light",
  "pose": "Ratna supine on the pillow camera-left side of the bed, head resting, face toward the ceiling, blanket to her shoulders",
  "gesture": "one hand resting on the blanket, settling",
  "expression": "eyes just opening, heavy, soft from sleep, faint under-eye puffiness, lips relaxed, calm newly-awake gaze",
  "grooming": "loose uncovered hair fanned across the pillow, sleep-creased, soft",
  "framing": "medium shot framed tall, Ratna head, shoulders, reclining low in frame, generous headroom above the pillow, seated-pose clearance, bed, pillow visible",
  "angle": "camera-left side of the bed, eye-level at mattress height, facing Ratna",
  "camera": "50mm prime spherical, shallow depth of field, focus on Ratna face",
  "lighting": "warm amber lamp glow keying from camera-right off-frame, warm wrap across her face, across the pillow, the curtained window camera-left staying cool pre-dawn blue, gentle warm-cool contrast",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft wrap, deep honest shadow",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic matte lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic neat working-class grooming"
}
```
- **END** — method **EDIT-IN-PLACE** pada render START (NOL preamble; fidelity High) · **big-delta** rebah→duduk (Rule 27: attach `R_ratna_front_medium` via `+` utk wajah duduk + spec koheren; gagal→decompose) · delta: Ratna bangkit duduk + menoleh senyum ke camera-right · STATUS: ✅ authored:
```
Change only Ratna pose: she sits up and turns to smile.

- pose: Ratna now sitting upright against the headboard, torso raised off the pillow, blanket falling to her lap, head turned toward camera-right, face matching attached plate R_ratna_front_medium
- expression: awake and soft, a gentle warm smile toward her husband camera-right, eyes open calm and tender
- grooming: loose uncovered hair falling around her shoulders, sleep-soft
- unchanged: framing unchanged, camera angle unchanged, camera-left bed side unchanged, headboard position unchanged, window position unchanged, warm lamp lighting unchanged, color grade unchanged
```

---

## Status board
| Shot | START | END | Render |
|---|---|---|---|
| SH01 | ✅ PROVEN | ✅ PROVEN | regen pending (final batch) |
| SH02 | ✅ authored | ✅ authored | pending (final batch) |
| SH03 | ✅ authored | ✅ authored | pending (final batch) |
| SH04 | ✅ authored | ✅ authored | pending (final batch) |
| SH05 | ✅ authored | ✅ authored | pending (final batch) |

**Generate-order (final batch):** SH01→SH02→SH03→SH04→SH05 (SH05 grade-ref = `sc01_sh04_end`, so SH04 before SH05). Plates needed = `E01_kamar_{master,bed3q,bed4q,nightstand}` + `H_herman_front_{closeup,medium,full}` + `R_ratna_front_{medium,full}` — all on disk.
