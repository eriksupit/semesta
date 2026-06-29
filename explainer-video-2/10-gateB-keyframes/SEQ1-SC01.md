---
title: GATE B Keyframes — SEQ1-SC01 (INT. KAMAR HERMAN, 04.40)
tags: [explainer-video-2, gate-b, keyframe, seq1-sc01]
status: prompts-empty-awaiting-author
created: 2026-06-23
updated: 2026-06-26
aliases: [ev2-gateB-seq1-sc01]
---

# GATE B Keyframes — SEQ1-SC01

> **⚠️ PROMPTS EMPTIED 2026-06-26 — to be re-authored under the new method.** The previous prompts (old format: suffixed `character_identity_*` keys, no attachment-manifest, no mode declaration, medium plates, Kling-pilot framing) were **non-compliant** with the current method and were cleared to avoid being treated as truth. Old prompts recoverable from git; the 8 accepted renders (`scene-images/sc01/sc01_sh0{1..4}_{start,end}.png`) remain on disk as the prior-method output.

## Canonical references (do not duplicate here — point only)
- **Scene truth (prose + shot list):** [[03-scene-detail]] § SEQ1-SC01.
- **Prompting method (BINDING):** [[prompt-rules-text-image-to-image]] — diagnosis, Part I laws, Part II 3-mode grammar + camera-lock, Part V structure + **JSON templates (manifest / Mode A / B / C)**, enforcement G0–G6. Built on the 6-layer canon [[prompt-rules-image-generation]].
- **Attachment sourcing:** [[explainer-video-2/ATTACHMENT-PRODUCTION-BACKLOG]] (which env + character plates to attach; full+closeup standard, no medium).
- **Identity plates:** `character-images/`. **Room plates:** `environment-images/E01_kamar/`. **Generated images saved to:** `scene-images/sc01/`.
- **Review rubric:** [[REVIEW-CHECKLIST]].

## Method reminder (one screen — full rules in the method doc)
- **3 modes:** A from-scratch (full 6-layer) · B identity-anchored (manifest env+identity, L3→`subjects[]`, composition in text) · C composition-anchored (manifest +`composition_reference`, minimal delta, locked layers NOT re-written).
- **START/END = camera-lock:** identical framing/angle/camera; only Lapis-4 changes. END = Mode C anchored on the accepted START render.
- **Plate-state law:** never attach a plate containing an object the action must "create". Subject-count: ≤1 face-locked (+1 soft). ADDENDUM A1: device screens OFF, graphics in After Effects.
- **Accept → rename:** an accepted render is renamed to `sc01_sh0N_{start,end}.png` (the done-marker); the proven prompt then replaces the empty slot below.

## Scene constants
- **Room:** E01 Kamar Herman (`environment-images/E01_kamar/`). **On-screen:** Herman (Herman alone except SH01 where Ratna sleeps beside him, uncovered — private bedroom, mahram only).
- **Time/grade:** pre-dawn 04.40; warm Deakins grade via `color_grade`, subuh ambient cool-blue in `lighting`.

---

## SEQ1-SC01-SH01 — ECU/CU mata Herman · overhead · 85mm  *(regen 2026-06-29, master-parent method)*
- **Intent (03):** start = mata terpejam, lelap. end = mata terbuka, mengerjap, fokus ke langit-langit. Bookend ke coda SEQ6-SC03.
- **SHOT-CONCEPT (FIX — Rule 6a framing-by-union, identik dua frame):** overhead vantage, kamera di atas wajah supine; pita mata–wajah dominan; 85mm; 16:9. Kamera diam; HANYA mata yang berubah START→END. **Ratna TIDAK di frame** (mustahil terbaca di CU; ia hadir di SH04). **Render aktual:** vantage mendarat diagonal-atas hampir frontal (bukan top-down murni), framing CU wajah penuh (drift-wider Rule 4) — keduanya diterima.
- **Attachments:** identity `H_herman_front_closeup.png` SAJA. Env TIDAK dilampirkan (ECU tak menampilkan ruang; lampiran env memicu drift-wider Rule 4).
- **START** — mode: **B** (master-parent, full from-scratch) · STATUS: ✅ **ACCEPTED 2026-06-29 (regen, supersedes prior 50mm version)** → `scene-images/sc01/sc01_sh01_start.png`. Review: identitas Herman cocok plat ✓; render mendarat **CU wajah** (lebih lebar dari ECU spec — drift-wider Rule 4 figur-berbaring, mata+wajah dominan, diterima); vantage **diagonal-atas hampir frontal** (bukan top-down murni) → END gaze diarahkan ke langit-langit bukan ke lensa; grade very-low-key subuh. Proven prompt (token-per-token, Rule 11):
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
- **END** — method: **EDIT-IN-PLACE** pada canvas yang sudah memuat `sc01_sh01_start.png` (**NOL preamble nama-file** — canvas itu = render START; validated 2026-06-29) · STATUS: ✅ **ACCEPTED 2026-06-29** → `scene-images/sc01/sc01_sh01_end.png`. Review: framing + posisi-wajah **identik START by construction** (edit-in-place — geometri di luar mata = piksel asli); mata terbuka, gaze ke atas/langit-langit (cocok vantage diagonal), identitas konsisten. Fidelity dropdown → High. Proven edit-instruction (paste langsung di Describe-edits, NOL nama-file, NOL preamble):
```
Change only the eye state to open, awake.
- expression: both eyelids open, alert, irises visible, pupils visible, steady awake upward gaze toward ceiling, faint cool catchlight on wet eye surface, lashes lifted
- unchanged: framing unchanged, camera angle unchanged, face position on pillow unchanged, brow unchanged, nose unchanged, mouth unchanged, pillowcase unchanged, bed linen unchanged, lighting unchanged, color grade unchanged
```
> Metode baku start/end **delta-kecil = edit-in-place** (kanonik: `prompt-rules-text-image-to-image` Part II EDIT-IN-PLACE §178: nol preamble nama-file, operasi+delta+lock-list saja). Generate-from-attachment (Mode C) = fallback bila tool tak punya edit mode.

## SEQ1-SC01-SH02 — CU ponsel di nakas · top-down insert · 50mm macro
- **Intent (03):** start = layar menyala (`Waktu Subuh 04.42` + kartu iklan sarung — **rendered OFF, UI in After Effects**). end = ibu jari menyentuh "matikan". Insert top-down, screen OFF (A1).
- **SHOT-CONCEPT (FIX — Rule 6a, identik dua frame):** top-down CU/macro insert HP di nakas; kamera di atas permukaan menatap ke bawah; HP dominan; 50mm macro; 16:9. Kamera diam; END hanya menambah ibu jari.
- **Konsistensi antar-shot (BUKAN attach render shot-lain):** token-block `mood/color_grade/style/inti-lighting` disamakan **verbatim ke SH01** + env plate bersama + grade post. Attach render SH01 dilarang (reference-dominance impor komposisi wajah).
- **Attachments:** env `E01_kamar_nightstand.png` SAJA.
- **START** — mode: **B** (master-parent, object shot) · STATUS: ✅ **ACCEPTED 2026-06-29** → `scene-images/sc01/sc01_sh02_start.png`. Review: layar OFF (A1) ✓; nakas+base-lampu+tepi-ranjang cocok plat, nol halusinasi ✓; lampu belum-nyala (logika SH04 aman) ✓. Menyimpang-diterima: framing **drift-wider** (ponsel ~25% frame, bukan macro-tight — beri ruang END) + angle oblique-high (bukan top-down murni) + **grade lebih hangat/terang dari SH01** (gap token-copy: resep sama, nilai-render beda → unify di grade post AE). Konsistensi: `mood/color_grade/style` verbatim SH01; UI di AE. Prompt:
```json
{
  "attachment_manifest": {
    "environment_reference": "E01_kamar_nightstand.png — same nightstand, same phone, same lamp, identical light-oak wood, identical materials, identical layout, new camera only"
  },
  "mood": "tender intimate pre-dawn stillness, hushed private waking, quiet domestic register",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinematic frame, ARRI Alexa Mini LF, 100mm macro prime spherical lens, Kodak 2383 film emulation, naturalistic rendering",
  "scene": "top-down insert, smartphone flat face-up on light-oak nightstand surface, dark dormant black glass screen, table lamp base camera-side edge, headboard edge nearby",
  "location": "indoor",
  "time_of_day": "night",
  "atmosphere": "hushed pre-dawn near-darkness, perfectly still",
  "scene_depth": {
    "foreground": "smartphone flat face-up, dark dormant black glass screen, frame-dominant",
    "midground": "matte light-oak nightstand surface around phone",
    "background": "soft dark, table lamp base at frame edge"
  },
  "subject_anchor": {
    "primary_subject": "smartphone flat face-up on nightstand, dark dormant matte black glass screen",
    "supporting_objects": { "nightstand": "matte light-oak nightstand surface", "lamp": "table lamp base at frame edge, off, dark" },
    "human_absence_signal": "phone resting alone, surface around it clear, still"
  },
  "subject_state": "static",
  "action": "phone at rest on nightstand, screen dark dormant",
  "framing": "macro insert close-up, phone frame-filling, tight on device",
  "angle": "top-down, straight-down onto nightstand surface, phone square to lens",
  "camera": "100mm macro prime spherical, shallow depth of field, focus on phone face",
  "lighting": "very low-key pre-dawn near-darkness, faint cool ambient from off-frame curtained window, nightstand lamp dormant dark, deep soft shadow across nightstand surface",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalistic domestic observation, patient stillness",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "available-light naturalism, soft directional",
  "production_designer": "Eugenio Caballero", "production_design_style": "lived-in middle-class Jakarta domestic authenticity",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in"
}
```
- **END** — method: **EDIT-IN-PLACE** + 1 extra-ref (`H_herman_front_full.png` via `+`, skin+hand) · STATUS: ✅ **ACCEPTED 2026-06-29 (final: tangan dari KIRI, HP MELINTANG, framing dikunci)** → `scene-images/sc01/sc01_sh02_end.png`. Delta: lengan Herman masuk dari **camera-left** (sisi ia tidur) meraih HP → HP **terputar dari membujur (portrait) ke melintang (landscape)** tergenggam. Review: lengan-dari-kiri ✓, HP landscape ✓, **framing IDENTIK START** ✓ (edit-in-place menahan geometri walau delta besar: putar-orientasi + tambah-lengan), layar OFF ✓, skin cocok plat ✓. Edit-instruction final (token-per-token, NOL preamble, attach `front_full` via `+`, fidelity High):
```
Edit: the phone is now grasped by a hand and turned landscape.
- hand: single mature male hand, skin tone and hand from attached plate H_herman_front_full, reference for skin and hand only, bare forearm in from the camera-left frame edge from the bed, fingers wrapped under the phone, thumb resting on the screen face
- phone: same phone, now turned landscape with its long axis horizontal, grasped in the hand, lifted just clear of the nightstand surface, screen still dark dormant black glass
- unchanged: framing unchanged, crop unchanged, camera angle unchanged, nightstand surface unchanged, lamp unchanged camera-right, bed and dark bedding unchanged camera-left, lighting unchanged, color grade unchanged
```
> **⭐ PELAJARAN KUNCI (validated 2026-06-29, 4 re-roll SH02-END):** (1) **MODEL ADEGAN FISIK dulu, jangan token-swap parsial** — arah-masuk anggota tubuh WAJIB ikut posisi karakter di frame (Herman bed-left → lengan dari KIRI, bukan "from bottom" sembarang; Rule 24). (2) **Objek yang digenggam BERUBAH ORIENTASI** mengikuti aksi (HP portrait→landscape saat diraih dari samping) — sebut eksplisit; jangan biarkan kontradiksi "lengan horizontal vs HP vertikal". (3) **edit-in-place MENAHAN framing bahkan untuk DELTA BESAR** (putar-orientasi objek + tambah-lengan) — mematahkan hipotesis lama "big-delta hand → resample framing"; akar kegagalan lama = spec INKOHEREN/PARSIAL, BUKAN ukuran delta. (4) Prompt harus **utuh-koheren**: lengan + grip + orientasi-objek + lock saling konsisten. Perjalanan re-roll: jempol(beat keliru) → genggam-dari-bawah(spasial salah, grip tak diubah) → dari-kiri+landscape(benar). Akar perilaku: "menulis tanpa berpikir" (token-emit tanpa model 3D).
> **A/B negasi (N=1, 2026-06-29):** Versi B `negative_spatial_instructions` ("do not mirror / do not add second hand") **TIDAK backfire** di edit-model ChatGPT baru (single-hand, layar OFF, nol mirror); affirmative tetap default (lebih ringkas + tervalidasi panjang). Re-test di kasus layout-kritis (bed4q mirror) sebelum ubah aturan no-negation GPT-Image-2 lama.

## SEQ1-SC01-SH03 — Herman + ponsel: rebah → duduk-samping taruh HP · 50mm
- **Intent (03, restructured 2026-06-26 — 7-shot · lihat [[SEQ1-SC01-RESTRUCTURE-2026-06-26]]):** start = Herman **rebah** nyandar bantal lihat layar (grafik saham; UI di After Effects, layar = slab **cool blue-white** Rule 21). end = Herman **TETAP rebah, menurunkan/menaruh HP face-down ke nakas di sisi kanannya** (delta-KECIL, reach-and-place). Beat **bangkit-duduk DIELIPSIS di cut SH03→SH04** (SH04 menangkapnya sudah duduk, tampak belakang).
- **SHOT-CONCEPT (FIX — Rule 22 + metode multi-angle CUT):** framing **MEDIUM** (diketatkan dari medium-wide lama; sit-up tak lagi perlu ditampung, hanya reach-and-place). Angle = **kanan-diagonal `bed3q`**. Satu frame DIAM menampung rebah-lihat-HP (START) DAN rebah-taruh-HP-ke-nakas (END) — nakas WAJIB in-frame camera-right. Pasangan di ranjang (Rule 18): Herman camera-right, Ratna camera-left uncovered (R-ratna §0). Layout (Rule 19): jendela camera-left redup biru-pekat (Rule 10), nakas+lampu-OFF camera-right, Great Wave tengah. Herman bangun-tidur (Rule 20).
- **START attachments (5):** `E01_kamar_master.png` (layout) + `E01_kamar_bed3q.png` (angle) + `H_herman_front_medium.png` + `R_ratna_front_medium.png` + `sc01_sh02_end.png` (grade). Plat **medium** (Rule 23: plat lebih lebar → frame lebih jauh).
- **START** — mode: **B (one-shot)** · STATUS: ✅ **ACCEPTED (regen) 2026-06-26** → `scene-images/sc01/sc01_sh03_start.png` (supersedes prior `2a91a36c`). Review: framing MEDIUM mendarat (pasangan rebah dominan, lebih ketat dari long lama); **nakas+lampu in-frame camera-right** (syarat END reach-and-place ✓); angle `bed3q` ✓; Rule 21 layar slab biru-dingin under-light wajah, nol UI ✓; identitas Herman+Ratna cocok plat ✓; grade hangat+cool-screen konsisten SH02-END ✓; nol halusinasi. Watch utk END: permukaan nakas di tepi-kanan → taruh-HP harus mendarat di permukaan terlihat, tangan tak keluar frame. Proven prompt:
```json
{
  "attachment_manifest": {
    "environment_layout_reference": "E01_kamar_master.png — big-picture room layout, the curtained window and wardrobe on the camera-left, the nightstand and table lamp on the camera-right, the framed Great Wave print above the headboard, identical materials, identical layout",
    "environment_angle_reference": "E01_kamar_bed3q.png — the camera angle and bed framing for this shot, three-quarter view of the bed, match this vantage",
    "identity_reference": [
      "H_herman_front_medium.png — Herman, same man, match face shape, grey moustache, salt-and-pepper hair, mature skin, match proportions",
      "R_ratna_front_medium.png — Ratna, same woman, match face shape, dark hair, soft full brows, match proportions"
    ],
    "mood_color_lighting_reference": "sc01_sh02_end.png — previous shot of this scene, warm room grade and tonality reference only"
  },
  "reference_binding": "E01_kamar_master.png sets the big-picture room layout ONLY, the curtained window at camera-left, the nightstand and lamp at camera-right; E01_kamar_bed3q.png sets the camera angle ONLY; sc01_sh02_end.png sets the warm room colour grade and tonality ONLY, do not reproduce its composition, do not reproduce its top-down angle, do not reproduce its objects",
  "mood": "intimate pre-dawn stillness, the first breath after waking, hushed sacred quiet",
  "color_grade": "warm Deakins-style grade on the room, midtones slightly warm, gentle filmic contrast, one warm temperature, matched to the attached mood_color_lighting_reference sc01_sh02_end.png",
  "style": "photorealistic cinematic still, ARRI Alexa Mini LF, 50mm prime spherical lens, Kodak Portra rendering, fine film grain",
  "scene": "private bedroom in pre-dawn dark, a married couple in their shared bed, a mature man on the right side of the bed propped against a matte slate-grey cotton pillow holding a smartphone aloft at his chest, the smartphone screen a cool blue-white luminous slab with no legible interface, his wife asleep on the left side beside him hair uncovered and loose, a curtained window on the wife's side at camera-left dim and deep pre-dawn blue near-dark, a nightstand with a switched-off unlit table lamp on the man's side at camera-right, the framed Great Wave print centred on the wall above the headboard",
  "location": "indoor",
  "time_of_day": "pre-dawn",
  "atmosphere": "dark hushed pre-dawn dimness, barely-there ambient",
  "scene_depth": {
    "foreground": "the smartphone aloft at the man's chest, a cool blue-white luminous slab, the man's right hand wrapped around its lower edge",
    "midground": "the man's face and upper chest, the focal centre, lit cool blue-white from the phone below",
    "background": "the wife asleep on the pillow at camera-left, dark hair loose uncovered, face relaxed; the dim deep pre-dawn blue curtained window near-dark further to camera-left; the framed Great Wave print centred above the headboard; the switched-off lamp and nightstand at camera-right"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_medium.png", "wardrobe": "plain dark muted crew-neck cotton sleep t-shirt, plain dark muted pyjama trousers", "grooming": "hair tousled and messy from sleep, dishevelled" },
    { "who": "Ratna", "identity_reference": "R_ratna_front_medium.png", "wardrobe": "light muted sleep clothing, dark hair uncovered, worn loose and down across the pillow", "state": "asleep, eyes closed, lying turned slightly toward him, not the focus" }
  ],
  "subject_state": "static",
  "action": "the man watching the phone screen aloft at his chest, his wife lying still asleep beside him",
  "pose": "the man propped against the pillow, head and shoulders raised, leaning back, right arm raised holding the phone at his chest, the wife supine beside him turned slightly toward him head on the pillow",
  "gesture": "the man's right hand wrapped around the lower edge of the phone, fingers along the right long side, thumb along the left long side, the screen face angled up toward his face",
  "expression": "the man just woken, eyes open but heavy and tired, lower lids slightly puffy, gaze down on the screen, face creased and sleep-rumpled, brows relaxed, mouth slightly slack, sleep-worn; the wife's eyes closed, features soft at rest",
  "framing": "medium two-shot measured on a 1920 by 1080 canvas, fixed camera, the reclining man's head centred around x 1150 with his head-top near y 250 and his torso filling down toward the lower frame, the phone he holds aloft at his chest around x 980 to 1140 and y 430 to 590, the nightstand at camera-right spanning about x 1500 to 1840 with its surface near y 640 to 840 fully in frame within his reach so he can lower the phone onto it without the camera moving, the sleeping wife's head at camera-left around x 320 to 560 and y 360 to 540, framing tight on the reclining couple, no sit-up to contain since the man stays reclining and only lowers the phone",
  "angle": "three-quarter vantage from the man's camera-right side of the bed matching the camera angle of the attached environment_angle_reference E01_kamar_bed3q.png, camera slightly above eye level, both heads on the pillows held in frame",
  "camera": "50mm prime spherical, shallow focus on the man's face, the wife softer in the same plane",
  "lighting": "very-low-key pre-dawn darkness, the only key light a cool blue-white glow rising from the smartphone screen below the man's face, cool blue-white under-light grazing his chin, lower cheeks, nose-tip, brow, and his hands, a dim deep pre-dawn blue light barely passing through the curtained window at camera-left, near-dark window, the table lamp switched off and unlit, no warm sun risen yet, the rest of the room in dim soft warm-neutral ambient, strong warm-cool contrast, shadows soft not crushed",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalist realism",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light, soft directional",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic lived-in skin, real-person feel"
}
```
> **Catatan grade (validated):** cool-screen + dim-blue-window + warm-room dari grade-ref `sc01_sh02_end.png` + token Rule 21/10. (Look ini di-reverse-engineer jadi prompt one-shot — Rule 25.) Framing kini **MEDIUM** (tighter) karena END tak lagi memuat sit-up.
- **END** — method: **EDIT-IN-PLACE delta-KECIL** pada render `sc01_sh03_start.png` (reach-and-place HP ke nakas, Herman **tetap rebah**) · STATUS: 🟨 **PROMPT READY — awaiting generate**. Prior sit-up END (`1e9f76d3`) di-retire — beat bangkit-duduk pindah ke cut SH04 (tampak belakang). Lihat [[SEQ1-SC01-RESTRUCTURE-2026-06-26]].
  - **Attachment:** TANPA lampiran baru — edit dilakukan di atas render `sc01_sh03_start.png` yang dimuat di edit-view (nakas sudah ada in-frame pada sudut benar; melampirkan plat top-down `E01_kamar_nightstand.png` justru memicu konflik-sudut, jadi tidak dipakai). Set input-fidelity **High**. Edit-instruction (token-per-token, nol pronoun redundan, lock-list penuh — Rules 11/12/13/14):
```
the smartphone now resting face-down flat on the visible nightstand surface at camera-right near the lamp base, dark screen, screen off, no screen glow, the man's right arm extended toward the nightstand, the man's right hand resting flat beside the face-down phone, the cool blue-white glow gone from the face and chest, the man still reclining propped against the pillow, the man's head turned down toward the nightstand, the face now lit only by dim cool deep pre-dawn ambient, the sleeping wife unchanged, the headboard unchanged, the curtained window unchanged, the table lamp unchanged, the nightstand unchanged, the framed Great Wave artwork unchanged, the bed unchanged, framing unchanged, crop unchanged, camera unchanged, colour grade unchanged, composition unchanged
```

## SEQ1-SC01-SH04 — MS samping ranjang · 35mm
- **Intent (03):** start = Herman menelungkupkan ponsel, bangkit duduk. end = berdiri mengenakan sarung (`solid plain-weave sarong, dark muted colorway`). Payoff diegetik dimulai.
- **Attachments (TBD):** env `E01_kamar_bed3q.png` (+ `E01_kamar_master.png` regen); identity Herman full (+ profileA if side-of-bed).
- **START** — mode: ___ · STATUS: ⬜ TO AUTHOR
- **END** — mode: C · STATUS: ⬜ TO AUTHOR
