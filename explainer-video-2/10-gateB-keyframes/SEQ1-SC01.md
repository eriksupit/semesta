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
Change only the eyes state to open, awake.

- expression: both eyelids open but slightly heavy from just waking, irises visible, pupils visible, steady newly-awake upward gaze toward ceiling, faint cool catchlight on wet eye surface, lashes lifted, subtle morning puffiness under the eyes, faint redness along the waterline, slight bloodshot quality in the whites of the eyes, moist tired eye surface, calm sleepy-alert gaze, freshly awakened but not fully energized
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
"scene": "top-down insert, smartphone flat face-up on light-oak nightstand surface, rotated horizontally in landscape orientation, dark dormant black glass screen, table lamp base camera-side edge, headboard edge nearby",  
"location": "indoor",  
"time_of_day": "night",  
"atmosphere": "hushed pre-dawn near-darkness, perfectly still",  
"scene_depth": {  
"foreground": "smartphone flat face-up, rotated horizontally in landscape orientation, dark dormant black glass screen, frame-dominant",  
"midground": "matte light-oak nightstand surface around phone",  
"background": "soft dark, table lamp base at frame edge"  
},  
"subject_anchor": {  
"primary_subject": "smartphone flat face-up on nightstand, rotated horizontally in landscape orientation, dark dormant matte black glass screen",  
"supporting_objects": {  
"nightstand": "matte light-oak nightstand surface",  
"lamp": "table lamp base at frame edge, off, dark"  
},  
"human_absence_signal": "phone resting alone, surface around it clear, still"  
},  
"subject_state": "static",  
"action": "phone at rest on nightstand, screen dark dormant, placed horizontally across the nightstand surface rather than lengthwise",  
"framing": "macro insert close-up, phone frame-filling, tight on device, horizontal landscape phone orientation clearly visible",  
"angle": "top-down, straight-down onto nightstand surface, phone square to lens, phone lying melintang in landscape orientation",  
"camera": "100mm macro prime spherical, shallow depth of field, focus on phone face",  
"lighting": "very low-key pre-dawn near-darkness, faint cool ambient from off-frame curtained window, nightstand lamp dormant dark, deep soft shadow across nightstand surface",  
"aspect_ratio": "16:9",  
"director": "Alfonso Cuarón",  
"directing_style": "intimate naturalistic domestic observation, patient stillness",  
"lighting_director": "Emmanuel Lubezki",  
"lighting_style": "available-light naturalism, soft directional",  
"production_designer": "Eugenio Caballero",  
"production_design_style": "lived-in middle-class Jakarta domestic authenticity",  
"interior_designer": "Ilse Crawford",  
"interior_design_style": "warm human-centred tactile lived-in"  
}
```
- **END** — method: **EDIT-IN-PLACE** + 1 extra-ref (`H_herman_front_full.png` via `+`, skin+hand) · STATUS: ✅ **ACCEPTED 2026-06-29 (final: tangan dari KIRI, HP MELINTANG, framing dikunci)** → `scene-images/sc01/sc01_sh02_end.png`. Delta: lengan Herman masuk dari **camera-left** (sisi ia tidur) meraih HP → HP **terputar dari membujur (portrait) ke melintang (landscape)** tergenggam. Review: lengan-dari-kiri ✓, HP landscape ✓, **framing IDENTIK START** ✓ (edit-in-place menahan geometri walau delta besar: putar-orientasi + tambah-lengan), layar OFF ✓, skin cocok plat ✓. Edit-instruction final (token-per-token, NOL preamble, attach `front_full` via `+`, fidelity High):
```
Edit: the phone is now grasped by a hand and turned landscape, with the hand emerging from the annotated point “tangan muncul menyodor dari sini.”

- hand: single mature male hand, skin tone and hand from attached plate H_herman_front_full, reference for skin and hand only, bare forearm enters from the extreme camera-left frame edge at the annotated point around x: 0.8%, y: 58.2%, emerging from the bed side as if reaching in from that exact spot, forearm extending naturally toward the phone, fingers wrapped under the phone, thumb resting on the screen face
    
- phone: same phone, now turned landscape with its long axis horizontal, grasped in the hand, lifted just clear of the nightstand surface, screen still dark dormant black glass
    
- hand_position: reposition the hand and forearm so the point of entry clearly matches the annotation “tangan muncul menyodor dari sini”; the arm should originate from that lower-left camera-edge point and reach diagonally toward the phone without changing the phone’s landscape orientation
    
- unchanged: framing unchanged, crop unchanged, camera angle unchanged, nightstand surface unchanged, lamp unchanged camera-right, bed and dark bedding unchanged camera-left, lighting unchanged, color grade unchanged
```
> **⭐ PELAJARAN KUNCI (validated 2026-06-29, 4 re-roll SH02-END):** (1) **MODEL ADEGAN FISIK dulu, jangan token-swap parsial** — arah-masuk anggota tubuh WAJIB ikut posisi karakter di frame (Herman bed-left → lengan dari KIRI, bukan "from bottom" sembarang; Rule 24). (2) **Objek yang digenggam BERUBAH ORIENTASI** mengikuti aksi (HP portrait→landscape saat diraih dari samping) — sebut eksplisit; jangan biarkan kontradiksi "lengan horizontal vs HP vertikal". (3) **edit-in-place MENAHAN framing bahkan untuk DELTA BESAR** (putar-orientasi objek + tambah-lengan) — mematahkan hipotesis lama "big-delta hand → resample framing"; akar kegagalan lama = spec INKOHEREN/PARSIAL, BUKAN ukuran delta. (4) Prompt harus **utuh-koheren**: lengan + grip + orientasi-objek + lock saling konsisten. Perjalanan re-roll: jempol(beat keliru) → genggam-dari-bawah(spasial salah, grip tak diubah) → dari-kiri+landscape(benar). Akar perilaku: "menulis tanpa berpikir" (token-emit tanpa model 3D).
> **A/B negasi (N=1, 2026-06-29):** Versi B `negative_spatial_instructions` ("do not mirror / do not add second hand") **TIDAK backfire** di edit-model ChatGPT baru (single-hand, layar OFF, nol mirror); affirmative tetap default (lebih ringkas + tervalidasi panjang). Re-test di kasus layout-kritis (bed4q mirror) sebelum ubah aturan no-negation GPT-Image-2 lama.

## SEQ1-SC01-SH03 — Herman + ponsel: rebah → duduk-samping taruh HP · 50mm
- **Intent (03, restructured 2026-06-26 — 7-shot · lihat [[SEQ1-SC01-RESTRUCTURE-2026-06-26]]):** start = Herman **rebah** nyandar bantal lihat layar (grafik saham; UI di After Effects, layar = slab **cool blue-white** Rule 21). end = Herman **TETAP rebah, menurunkan/menaruh HP face-down ke nakas di sisi kanannya** (delta-KECIL, reach-and-place). Beat **bangkit-duduk DIELIPSIS di cut SH03→SH04** (SH04 menangkapnya sudah duduk, tampak belakang).
- **SHOT-CONCEPT (FIX — Rule 22 + metode multi-angle CUT):** framing **MEDIUM** (diketatkan dari medium-wide lama; sit-up tak lagi perlu ditampung, hanya reach-and-place). Angle = **kanan-diagonal `bed3q`**. Satu frame DIAM menampung rebah-lihat-HP (START) DAN rebah-taruh-HP-ke-nakas (END) — nakas WAJIB in-frame camera-right. Pasangan di ranjang (Rule 18): Herman camera-right, Ratna camera-left uncovered (R-ratna §0). Layout (Rule 19): jendela camera-left redup biru-pekat (Rule 10), nakas+lampu-OFF camera-right, Great Wave tengah. Herman bangun-tidur (Rule 20).
- **START attachments (5):** `E01_kamar_master.png` (layout) + `E01_kamar_bed3q.png` (angle) + `H_herman_front_medium.png` + `R_ratna_front_medium.png` + `sc01_sh02_end.png` (grade). Plat **medium** (Rule 23: plat lebih lebar → frame lebih jauh).
- **START** — mode: **B (FULL MASTER, one-shot — START selalu full prompt, bukan edit; konsistensi doc, Erik 2026-06-29b)** · STATUS: ✅ **ACCEPTED 2026-06-29b (re-roll #3, glow-fix)** → `scene-images/sc01/sc01_sh03_start.png`. Review adversarial: wajah under-light cool-blue dari HP ✓, HP portrait ✓, blocking H-right/R-left ✓, Great Wave + nakas in-frame ✓, clean-shaven ✓, nol halusinasi. Jalan re-roll: `50c9e403`(HP-landscape)✗ → `24f3e4aa`(glow-hilang)✗ → `287017d4` ACCEPTED. Perbaikan dari render `50c9e403` (DITOLAK: HP landscape): **HP portrait-explicit** (4 field) + **grade Deakins-lock** (verbatim SH01/SH02) + **clean-shaven** (Herman regen, buang `grey moustache` stale) + **negasi dibuang** (reference_binding/scene/lighting) + **Kodak 2383** + `time_of_day: night`. Master prompt:
```json
{  
"attachment_manifest": {  
"environment_layout_reference": "E01_kamar_master.png — big-picture room layout, curtained window and wardrobe camera-left, nightstand and table lamp camera-right, framed Great Wave print above headboard, identical materials, identical layout",  
"environment_angle_reference": "E01_kamar_bed3q.png — camera angle and bed framing for this shot, three-quarter view of the bed, match this vantage",  
"identity_reference": [  
"H_herman_front_medium.png — Herman, same man, match face, salt-and-pepper hair, clean-shaven, match proportions",  
"R_ratna_front_medium.png — Ratna, same woman, match face, dark hair, soft full brows, match proportions"  
],  
"grade_reference": "sc01_sh02_end.png — colour grade and tonality reference only, warm room grade"  
},  
"reference_binding": "E01_kamar_master.png = room layout only, window camera-left, nightstand and lamp camera-right; E01_kamar_bed3q.png = camera angle only; sc01_sh02_end.png = warm room colour grade and tonality only",  
"mood": "tender intimate pre-dawn stillness, hushed private waking, quiet domestic register",  
"color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",  
"style": "photorealistic cinematic frame, ARRI Alexa Mini LF, 50mm prime spherical lens, Kodak 2383 film emulation, naturalistic skin rendering",  
"scene": "private bedroom pre-dawn dark, married couple in shared bed, mature man on the camera-right side propped against a slate-grey pillow holding a smartphone aloft at his chest, smartphone held upright in portrait orientation, long axis vertical, screen facing the man, screen a bright uniform cool blue-white luminous slab casting cool blue-white light up onto his newly-awake crumpled face, his hair visibly messy and uncombed from sleep, wife asleep on the camera-left side, hair uncovered loose across the pillow, curtained window on the wife's side camera-left dim deep pre-dawn blue, nightstand with table lamp off on the man's side camera-right, framed Great Wave print centred above the headboard",  
"location": "indoor",  
"time_of_day": "night",  
"atmosphere": "hushed pre-dawn near-darkness, perfectly still",  
"scene_depth": {  
"foreground": "smartphone held upright portrait at the man's chest, long axis vertical, cool blue-white luminous slab, his hand around its lower edge",  
"midground": "the man's face and upper chest, focal centre, lit cool blue-white from the phone below, face visibly kusut and sleep-rumpled, hair berantakan tak tertata",  
"background": "the wife asleep on the pillow camera-left, dark hair loose, face relaxed, dim deep pre-dawn blue curtained window further camera-left, framed Great Wave print above the headboard, lamp off and nightstand camera-right"  
},  
"subjects": [  
{  
"who": "Herman",  
"identity_reference": "H_herman_front_medium.png",  
"wardrobe": "plain dark muted crew-neck cotton sleep t-shirt, plain dark muted pyjama trousers",  
"grooming": "strong just-woke bed-head, salt-and-pepper hair messy, uneven, uncombed, disheveled, flattened in some areas and sticking up in others, natural sleep-messy texture, not styled"  
},  
{  
"who": "Ratna",  
"identity_reference": "R_ratna_front_medium.png",  
"wardrobe": "light muted sleep clothing, dark hair uncovered loose across the pillow",  
"state": "asleep, eyes closed, turned slightly toward him, not the focus"  
}  
],  
"subject_state": "static",  
"action": "the man watching the upright phone held portrait at his chest, his wife still asleep beside him",  
"pose": "man propped against the pillow, head and shoulders raised, leaning back, arm raised holding the phone upright at his chest, wife supine beside him turned slightly toward him, head on the pillow",  
"gesture": "the man's hand gripping the lower portion of the upright portrait phone, fingers along its vertical right side, thumb along its vertical left side, screen facing his face",  
"expression": "man just-woke with wajah kusut, sleep-rumpled and groggy, eyes open but heavy and tired, lower lids slightly puffy, faint under-eye swelling, gaze down on the screen, relaxed sleepy brows, forehead lightly creased, cheeks and mouth slightly slack, lips gently parted, facial muscles still loose from sleep, overall expression newly awakened and not yet fully alert; wife eyes closed, features soft at rest",  
"hair_expression_update": "Herman's hair must clearly read as rambut berantakan tak tertata: messy bed-head, tousled salt-and-pepper strands, uneven silhouette, uncombed texture, slightly flattened where it touched the pillow and lifted in random small clumps, realistic natural morning disorder",  
"framing": "medium two-shot on a 1920x1080 canvas, fixed camera, reclining man's head centred near x1150 head-top near y250 torso toward lower frame, upright portrait phone held near x1010-1110 y400-620 taller than wide, nightstand camera-right spanning x1500-1840 surface near y640-840 fully in frame within his reach, sleeping wife's head camera-left near x320-560 y360-540, tight on the reclining couple",  
"angle": "three-quarter vantage from the man's camera-right side of the bed, matching environment_angle_reference E01_kamar_bed3q.png, camera slightly above eye level, both heads on the pillows in frame",  
"camera": "50mm prime spherical, shallow focus on the man's face, wife softer in the same plane",  
"lighting": "very low-key pre-dawn near-darkness, the man's face lit ONLY by a strong cool blue-white glow from the upright phone screen held below his face, his chin lower cheeks nose-tip and brow clearly under-lit cool blue, cool-blue catchlights in his tired heavy eyes, the sleeping wife and the rest of the room falling to deep dim warm-neutral shadow, dim deep pre-dawn blue at the curtained window camera-left, table lamp off dark base, strong warm-cool contrast, shadows deep soft",  
"aspect_ratio": "16:9",  
"director": "Alfonso Cuarón",  
"directing_style": "intimate naturalistic domestic observation, patient stillness",  
"lighting_director": "Emmanuel Lubezki",  
"lighting_style": "naturalistic available-light, soft directional",  
"production_designer": "Eugenio Caballero",  
"production_design_style": "lived-in middle-class Jakarta domestic authenticity",  
"interior_designer": "Ilse Crawford",  
"interior_design_style": "warm human-centred tactile lived-in",  
"costume_designer": "Deborah Hopper",  
"costume_style": "character-authentic casual sleepwear",  
"makeup_artist": "Eryn Krueger Mekash",  
"makeup_style": "naturalistic matte lived-in skin, real-person feel, subtle sleep-rumpled facial texture, no glamour retouching"  
}
```
> **Catatan grade (validated):** cool-screen + dim-blue-window + warm-room dari grade-ref `sc01_sh02_end.png` + token Rule 21/10. (Look ini di-reverse-engineer jadi prompt one-shot — Rule 25.) Framing kini **MEDIUM** (tighter) karena END tak lagi memuat sit-up.
- **END** — method: **EDIT-IN-PLACE single-pass** pada `sc01_sh03_start.png` (place-phone + relight + lock 2 wajah via `+`) · STATUS: ✅ **ACCEPTED 2026-06-29b** → `scene-images/sc01/sc01_sh03_end.png`. Delta: Herman taruh HP face-down ke nakas camera-right (tetap rebah), glow biru padam → wajah ke ambient dim. Review adversarial: **kedua wajah UTUH** ✓, framing identik START ✓, HP di nakas ✓, nol halusinasi. Jalan: `8f307f68`(Ratna-rusak relight)✗ → `781ae3f3`(repair two-pass)✓ → `63c79ab9`(single-pass, kedua wajah lock-plat) ACCEPTED.
  - **Attachments (2 via `+`):** `H_herman_front_medium.png` + `R_ratna_front_medium.png` (face locks). Canvas = `sc01_sh03_start.png`. Fidelity High. NOL preamble.
  - **⭐ PELAJARAN (validated 2026-06-29b):** relight di edit-in-place **MERUSAK wajah-sekunder di shadow** → lock TIAP wajah dgn **plat via `+`** (token `the sleeping wife unchanged` GAGAL; identity-anchor plat berhasil). END big-relight = jalankan instruksi asli di START bersih + attach SEMUA wajah hadir → **single-pass > place-then-repair**. Edit-instruction final:
```
Edit: the man has set the phone down on the nightstand, screen now dark, he stays reclining.
- phone: the same phone, now lying flat face-down on the nightstand surface at camera-right, screen off dark
- man: his right arm extended to the nightstand at camera-right having set the phone down, hand resting beside it, still reclining back against the pillow, head on the pillow, his face matching attached plate H_herman_front_medium, clear features, clean-shaven
- woman: the sleeping wife at camera-left, eyes closed asleep, calm relaxed, her face matching attached plate R_ratna_front_medium, clear natural features, dark hair loose across the pillow
- lighting: the cool blue-white phone glow extinguished, his face and chest now in dim ambient pre-dawn shadow, soft warm-neutral low ambient, room deep dim
- unchanged: framing unchanged, crop unchanged, camera angle unchanged, Great Wave print unchanged, nightstand and table lamp unchanged camera-right, curtained window unchanged camera-left, color grade unchanged
```

## SEQ1-SC01-SH04 — couple from behind, near-window vantage (rear three-quarter) → Herman sits up  *(method: rear-view + prior-frame pose-anchor, ACCEPTED 2026-06-29)*
- **Intent (03, restructured — SH04 = the sit-up):** start = couple reclining seen from BEHIND / side-back, camera near the curtained window on the room-left, shooting diagonally across the bed toward Herman + the nightstand room-right (matches `sc01_sh03_end`: Herman just set the phone down). end = Herman **sits up** (camera locked). [Lamp-on split to a later SH05 = reach nightstand lamp → lamp ON.]
- **SHOT-CONCEPT (ACCEPTED):** true reverse — "shot dari arah sebaliknya" of the bed3q/SH03 vantage. Camera at the window (room-left), **rear three-quarter / side-back** of both figures (backs + side-backs of heads, NOT frontalized). Room handedness LOCKED from master: window+wardrobe room-left, nightstand+lamp room-right, Great Wave above headboard. Herman room-right reclining (right arm extended to nightstand, phone face-down screen-off), Ratna room-left asleep. Pre-dawn dark, no phone glow, faint cool window blue along camera-left foreground.
- **METHOD — rear-view + prior-frame pose-anchor (Erik, ACCEPTED 2026-06-29; SUPERSEDES the earlier bed4q "clone-SH03 + foot vantage" plan, which kept frontalizing/drifting — `2feb5f55` sitting, `07abf768` mendongak/too-frontal):** what landed = (1) bind the **prior SH04 render** as `current_scene_reference` = pose/action/lighting BEAT anchor only ("do not copy previous frontal camera"); (2) `E01_kamar_master.png` = room layout + **handedness** lock only; (3) **rear identity plates** `H_herman_rear_medium.png` + `R_ratna_rear_medium.png` = back/side-back identity; (4) prior render also = grade/tonality; (5) explicit `camera_position` block + `"this is a real camera move to the window side, not a mirrored or flipped image"`. This is the reference-upload pose-anchor method (Mode C composition/pose anchor), NOT a from-scratch master, NOT the `bed4q` env plate (bed4q unused here). The two prior "front-plate + bed4q" rolls drifted because the bed4q-plate camera is foot-ward/face-visible and fought the rear intent; binding the prior render as pose anchor + rear plates + master-handedness + explicit "real camera move not mirror" is what locked it.
- **START attachments (4 — as generated):** `current_scene_reference` = the immediately-prior SH04 roll (pose/action **and** grade anchor). ⚠ PIN (resolved 2026-06-29): that transient hash roll has since been **deleted from disk** (only canonical `sc01_sh04_*` remain). For any future re-gen, use the accepted **`sc01_sh04_start.png`** itself as the pose/action + grade carrier (it embodies the same beat). + `E01_kamar_master.png` (room layout + handedness lock) + `H_herman_rear_medium.png` (Herman rear identity) + `R_ratna_rear_medium.png` (Ratna rear identity).
- **START** — mode: rear-view + prior-frame pose-anchor (full structured prompt below) · STATUS: ✅ **ACCEPTED 2026-06-29 (Erik: "hasilnya sudah akurat")** → `scene-images/sc01/sc01_sh04_start.png`. Review (Priority-1, render verified): near-window rear three-quarter ✓, Ratna room-left back-view asleep ✓, Herman room-right side-back with right arm to nightstand ✓, phone face-down screen-off ✓, Great Wave + nightstand+lamp room-right in frame ✓, handedness preserved (no mirror) ✓, dim pre-dawn no-glow + cool window blue foreground ✓. Verbatim accepted prompt:
```json
{
"attachment_manifest": {
"current_scene_reference": "latest generated image — pose/action reference only, Herman reclining on the room-right side, right arm extended to nightstand, phone already set down face-down, Ratna asleep beside him, preserve this action beat",
"environment_layout_reference": "E01_kamar_master.png — big-picture room layout and handedness only, curtained window and wardrobe on room-left, nightstand and table lamp on room-right, framed Great Wave print above headboard, identical materials, identical room identity",
"identity_back_reference": [
"H_herman_rear_medium.png — Herman back-view identity only, match back-of-head shape, short salt-and-pepper hair from behind, ears, neck, shoulder width, upper-back silhouette",
"R_ratna_rear_medium.png — Ratna back-view identity only, match rear silhouette, long straight dark hair from behind, shoulder line, back-of-head appearance"
],
"grade_reference": "latest generated image — colour grade and tonality reference only, dim pre-dawn warm-neutral shadow with faint cool window blue"
},
"reference_binding": "latest generated image = pose/action/lighting beat only, do not copy previous frontal camera; E01_kamar_master.png = locked room layout and handedness; H_herman_rear_medium.png and R_ratna_rear_medium.png = rear/side-back identity references only; this is a real camera move to the window side, not a mirrored or flipped image",
"mood": "tender intimate pre-dawn stillness, hushed private waking, quiet domestic register, observed from near the window",
"color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones, faint cool pre-dawn blue from the curtained window, deep dim warm-neutral room shadow",
"style": "photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, naturalistic skin and fabric rendering",
"scene": "private bedroom pre-dawn dark, viewed from near the curtained window on the room-left side, camera shooting diagonally across the bed toward Herman and the nightstand on room-right, married couple seen from rear three-quarter / side-back, Herman reclining on the room-right side with his right arm extended to the nightstand after setting down the phone, phone lying flat face-down on the nightstand surface with screen off dark, Ratna asleep beside him on the room-left side, dark hair loose across the pillow and bedding, table lamp off on the nightstand, framed Great Wave print above the headboard",
"location": "indoor",
"time_of_day": "night",
"atmosphere": "hushed pre-dawn near-darkness, perfectly still, intimate and observational, quiet domestic pause after the phone has been set down",
"camera_position": {
"placement": "near the curtained window on the room-left side, very close to the window curtain, looking diagonally across the bed toward Herman and the nightstand",
"view": "rear three-quarter / side-back view of both figures, mostly backs and side-backs of heads and upper bodies, do not frontalize Herman or Ratna",
"spatial_lock": "real camera move from the previous shot, not a mirror or horizontal flip; preserve room handedness from E01_kamar_master.png"
},
"scene_depth": {
"foreground": "soft out-of-focus cool blue curtain edge along camera-left foreground, dark rumpled duvet rising across the lower frame, bed surface leading toward the couple",
"midground": "Ratna asleep side-back / back view on the room-left side, long dark hair loose across pillow and bedding; Herman reclining side-back on the room-right side, messy salt-and-pepper hair, right arm extended toward the nightstand",
"background": "light-oak headboard, framed Great Wave print above, nightstand and table lamp off on room-right, phone resting face-down on the nightstand, warm-neutral textured wall"
},
"subjects": [
{
"who": "Herman",
"identity_reference": "H_herman_rear_medium.png",
"wardrobe": "plain dark muted crew-neck cotton sleep t-shirt, plain dark muted pyjama trousers",
"grooming": "just-woke bed-head visible from side-back, short salt-and-pepper hair messy, uneven, uncombed, flattened in some areas and lifted in small random clumps",
"state": "awake but tired, reclining, seen mostly from side-back / rear three-quarter, not frontal"
},
{
"who": "Ratna",
"identity_reference": "R_ratna_rear_medium.png",
"wardrobe": "light muted sleep clothing, dark hair uncovered loose across pillow and bedding",
"state": "asleep, eyes not visible or mostly hidden, calm relaxed, seen from back / side-back, not the focus"
}
],
"subject_state": "static",
"action": "Herman has finished setting the phone down on the nightstand; the phone now rests face-down with the screen dark while Herman stays reclining, his right arm still extended toward it; Ratna remains asleep beside him",
"pose": "Herman reclining back against slate-grey pillows on the room-right side, head on pillow, torso angled slightly toward the nightstand, right arm stretched out to camera-right with hand resting beside or lightly near the face-down phone; Ratna lying asleep on the room-left side, turned slightly toward Herman, head on pillow, shoulders and long hair visible from behind",
"gesture": "Herman’s right hand rests naturally beside the phone on the nightstand after placing it down, fingers relaxed; phone is no longer held; Ratna remains motionless asleep",
"expression": "Herman’s face is mostly side-back / partial profile only, still reading as just-woke and tired through posture, head angle, slack neck, messy hair, and slow relaxed hand; Ratna remains asleep with soft resting body language, face mostly hidden by side-back angle and hair",
"phone": {
"state": "same black smartphone, now lying flat face-down on the nightstand surface at room-right, screen off dark, no blue-white glow",
"position": "on the light-oak nightstand within Herman’s reach, close to his resting right hand",
"lighting_effect": "phone glow extinguished completely"
},
"framing": "medium-wide cinematic two-shot on a 1920x1080 canvas, fixed camera near the curtained window, curtain edge visible camera-left foreground, bed and dark duvet filling lower frame, Herman side-back / rear three-quarter on right half of bed, Ratna asleep side-back on left half of bed, nightstand and lamp visible at camera-right, Great Wave print cropped but recognizable above the headboard",
"angle": "near-window side-back angle, camera slightly above mattress level, looking diagonally from room-left/window side across the couple toward the room-right nightstand, maintaining true bedroom layout",
"camera": "50mm prime spherical, shallow-to-moderate focus, focus on Herman’s side-back silhouette and hand near the phone, Ratna softer but readable, foreground curtain softly out of focus",
"lighting": "very low-key pre-dawn near-darkness, no phone glow, Herman’s face and chest now in dim ambient pre-dawn shadow, soft warm-neutral low ambient room light, faint cool blue from the curtained window very near camera-left, table lamp off dark, deep soft shadows across bedding and wall, subdued warm-cool contrast",
"unchanged": "pose/action beat unchanged from latest scene reference, phone already set down, Herman remains reclining, Ratna remains asleep, Great Wave print unchanged and correctly oriented, nightstand and lamp unchanged room-right, curtained window unchanged room-left, bedding and headboard unchanged, color grade unchanged",
"aspect_ratio": "16:9",
"director": "Alfonso Cuarón",
"directing_style": "intimate naturalistic domestic observation, patient stillness, camera quietly observing from the room edge",
"lighting_director": "Emmanuel Lubezki",
"lighting_style": "naturalistic available-light, soft directional pre-dawn ambience, deep honest shadow",
"production_designer": "Eugenio Caballero",
"production_design_style": "lived-in middle-class Jakarta domestic authenticity",
"interior_designer": "Ilse Crawford",
"interior_design_style": "warm human-centred tactile lived-in",
"costume_designer": "Deborah Hopper",
"costume_style": "character-authentic casual sleepwear",
"makeup_artist": "Eryn Krueger Mekash",
"makeup_style": "naturalistic matte lived-in skin, real-person feel, no glamour retouching"
}
```
- **END** — method: **EDIT-IN-PLACE on `sc01_sh04_start.png`** (canvas = accepted START; operation + delta + lock-list, no recompose) · STATUS: ✅ **ACCEPTED 2026-06-29** → `scene-images/sc01/sc01_sh04_end.png` (renamed from hyphen-typo `sc01_sh04-end.png`). Delta: Herman shifts reclining→**sitting up**, right arm to the nightstand, **turns the bedside lamp ON** (warm practical glow now the dominant key camera-right, spilling on wall/arm/shoulder/side-back); Ratna unchanged asleep room-left; phone stays face-down dark; faint cool window blue preserved camera-left (warm-lamp vs cool-window contrast); framing/crop/camera/handedness LOCKED, both still rear/side-back (not frontalized). Review (render verified): sit-up + lamp-on ✓, rear/side-back preserved ✓, contrast ✓. (Lamp-ON here is **per spec** — `03-scene-detail:41` "lampu ON mulai SH04-END"; SH05 = Ratna wakes, no 7→8 restructure.) ⓘ Erik labelled the source "SH03-Start", but the prompt body defines the canvas as "the previous near-window rear / side-back frame" = `sc01_sh04_start.png` (sh03_start is a different bed3q frontal angle) → recorded as edit-in-place on **sh04_start**. Verbatim accepted END edit prompt:
```
Edit on place from previous image.

Change only the action beat: Herman is now sitting up and turning on the bedside lamp; the lamp is now ON.

* source image: previous near-window rear / side-back bedroom frame — same exact framing, same crop, same camera position, same camera angle, same near-window viewpoint, curtain soft in the camera-left foreground, bed and couple viewed from behind / side-back

* action: Herman has shifted from reclining to sitting up more clearly on the camera-right side of the bed, torso raised, back and side-back visible, head turned toward the nightstand, right arm extended toward the lamp, hand touching or holding the lamp switch/base as he turns it on

* lamp: same bedside table lamp on the camera-right nightstand, now switched ON, warm practical glow visible from the lampshade, warm light spilling onto the wall, nightstand surface, Herman’s right arm, shoulder, neck, and side-back profile

* phone: same phone remains on the nightstand, lying flat face-down / screen off dark, not glowing, placed near the lamp and within Herman’s reach

* Herman: same mature man, same rear / side-back identity, same short salt-and-pepper messy bed-head, same dark muted sleep t-shirt, just-woke posture, body still partly under the bedding, viewed mostly from behind and side-back, not frontalized

* Ratna: same sleeping wife on the camera-left side of the bed, unchanged pose, still asleep, eyes closed, calm relaxed, long dark hair loose across the pillow and back, body under dark bedding, viewed from behind / side-back, not frontalized

* lighting change: lamp glow is now the dominant warm practical light on camera-right; preserve faint cool pre-dawn blue from the curtained window at camera-left; maintain warm lamp vs cool window contrast; phone glow remains extinguished

* mood: tender intimate pre-dawn stillness, hushed private waking, quiet domestic register, naturalistic patient observation

* unchanged: framing unchanged, crop unchanged, camera angle unchanged, near-window camera position unchanged, curtain foreground unchanged, bed position unchanged, Herman and Ratna placement unchanged, bedding unchanged, headboard unchanged, Great Wave print unchanged, nightstand unchanged, phone placement unchanged except it remains dark, room layout unchanged, color grade unchanged

* style: photorealistic cinematic frame, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 film emulation, Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, slightly warmer midtones, Emmanuel Lubezki available-light naturalism, deep soft shadows, lived-in middle-class Jakarta bedroom authenticity

Important: this is an edit-on-place continuation of the previous frame. Do not recompose. Do not move the camera. Do not change the angle. Only change Herman’s posture/action and turn the bedside lamp on.
```
