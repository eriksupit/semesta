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

- **START** — mode **B** (object shot) · STATUS: ⬜ PENDING author
- **END** — method **EDIT-IN-PLACE** (delta: tangan Herman masuk dari ranjang menyentuh HP) · STATUS: ⬜ PENDING

---

## SH03 — Menimang ponsel · MEDIUM · bed3q
**SHOT-CONCEPT:** MEDIUM (kepala+dada+lengan) Herman supine, angle kanan-diagonal `bed3q`, eye-level kasur; nakas in-frame camera-right; 50mm; 16:9. Kamera diam; END = lengan terulur taruh HP ke nakas (masih rebah). Herman bangun-tidur (Rule 20). Grade wajah cool-blue HP-key, ruang shadow.
**START attachments:** `E01_kamar_master.png` (layout) + `E01_kamar_bed3q.png` (angle) + `H_herman_front_medium.png` (identity).

- **START** — mode **B** (full master) · STATUS: ⬜ PENDING author
- **END** — method **EDIT-IN-PLACE** (delta: place-phone ke nakas, glow padam→ambient) · STATUS: ⬜ PENDING

---

## SH04 — Lampu nakas menyala · WIDE 2-subjek · bed4q
**SHOT-CONCEPT:** WIDE dari sudut kaki ranjang (`bed4q`), dua figur berbaring; Herman camera-right (sisi nakas), Ratna camera-left uncovered; 35mm; 16:9. Kamera diam; END = lampu nyala (gelap→warm). Rule 18 co-present, Rule 19 dual-plate, Rule 20 bangun-tidur.
**START attachments:** `E01_kamar_master.png` (layout) + `E01_kamar_bed4q.png` (angle) + `H_herman_front_full.png` + `R_ratna_front_full.png` (dua identity).

- **START** — mode **B** (full master, 2-subjek) · STATUS: ⬜ PENDING author
- **END** — method **EDIT-IN-PLACE** (delta: lampu nakas ON, warm glow dominan camera-right; Ratna mulai menggeliat; lock 2 wajah via `+`) · STATUS: ⬜ PENDING

---

## SH05 — Ratna bangun · MEDIUM · sisi camera-left
**SHOT-CONCEPT:** MEDIUM Ratna, sisi camera-left ranjang, eye-level; warm lamp glow (grade ← SH04-END); 50mm; 16:9. Kamera diam; END = Ratna bangkit duduk + menoleh senyum ke camera-right. Ratna uncovered, rambut tergerai.
**START attachments:** `E01_kamar_master.png` (layout) + `R_ratna_front_medium.png` (identity) + `sc01_sh04_end.png`→ (grade-ref warm, setelah SH04 baru di-gen). *(Catatan: SH04 harus jadi dulu untuk grade-ref SH05.)*

- **START** — mode **B** (full master) · STATUS: ⬜ PENDING author
- **END** — method **EDIT-IN-PLACE** (delta: rebah→duduk + menoleh senyum) · STATUS: ⬜ PENDING

---

## Status board
| Shot | START | END | Render |
|---|---|---|---|
| SH01 | ✅ PROVEN | ✅ PROVEN | regen pending |
| SH02 | ⬜ PENDING | ⬜ PENDING | — |
| SH03 | ⬜ PENDING | ⬜ PENDING | — |
| SH04 | ⬜ PENDING | ⬜ PENDING | — |
| SH05 | ⬜ PENDING | ⬜ PENDING | — |
