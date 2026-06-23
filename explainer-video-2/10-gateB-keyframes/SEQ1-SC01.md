---
title: GATE B Keyframes — SEQ1-SC01 (INT. KAMAR HERMAN, 04.40) · PILOT
tags: [explainer-video-2, gate-b, keyframe, seq1-sc01, pilot]
status: active
created: 2026-06-23
updated: 2026-06-23
aliases: [ev2-gateB-seq1-sc01]
---

# GATE B Keyframes — SEQ1-SC01 · PILOT

> Scene truth → [[03-scene-detail]] (SEQ1-SC01). Identity lock → [[08-character-sheet/H-herman]]. Room lock → [[09-environment-sheet/E01-kamar]]. Standar 6-lapis + grade hangat → [[00-WORKLOG]] GATE B (2026-06-21, baris 167) + [[prompt-rules-image-generation]]. ADDENDUM A1 (layar OFF, grafis di After Effects).

> **🔒 ATURAN ATTACHMENT MANDATORY (Erik mandate 2026-06-23):** SETIAP shot (START & END) WAJIB melampirkan + menyebut di prompt KETIGA kategori: **(1) KARAKTER** (plat wajah/figur tiap orang dalam frame), **(2) LINGKUNGAN** (plat env, mis. `E01_kamar_*`), **(3) START/END-REFERENCE** (plat arah / render anchor). MESKI render START/END sudah menampilkan lingkungan, plat lingkungan TETAP wajib diattach + disebut — render anchor saja TIDAK cukup untuk objek yang diberi aksi (kalau tidak → model halusinasi). Tak ada pengecualian.

## Aturan keras yang dibawa
1. **Grade hangat LOCKED** (terverifikasi keyframe SH03): `Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones`. Hangat HANYA dari `color_grade`; garmen desaturated; negasi 0; tanpa nama organisasi.
2. **ADDENDUM A1:** layar device OFF/gelap di keyframe AI; UI/kartu/grafik (`Waktu Subuh · 04.42`, kartu sarung Cap Gajah, widget grafik saham) ditempel di After Effects. Lapis 5 dibuang.
3. **Dual reference-lock tiap segmen:** plat env E01 + plat wajah H_herman (tabel per shot).
4. **Tiap keyframe = SATU prompt utuh-mandiri.** Tiap unit generate (START dan END terpisah) membawa SENDIRI baris `environment_reference` + `character_identity.identity_reference` — zero "combine with fixed-spec" (SOP plat, [[09-environment-sheet/E01-kamar]]:61). START & END identik kecuali Lapis-4 (`subject_state`/`action`/`pose`/`expression`). Chain end-N = start-(N+1).
5. **Arah kamera:** HP yang dipegang/ditatap → punggung HP ke kamera, layar ke subjek, angle off-axis anti-cliché. HP tergeletak (insert top-down) → layar OFF, ruang layar bersih untuk AE.
6. **State kontekstual:** Herman baru bangun → kucel (kelopak berat, pipi sleep-creased, rambut gepeng sebelah) di Lapis-4 + hair/makeup state; identitas wajah tetap dari `identity_reference`.

## Reference-lock per shot
| Shot | Env plate | Face plate |
|---|---|---|
| SH01 ECU mata | `E01_kamar_bed3q.png` | `H_herman_front_closeup.png` |
| SH02 CU ponsel | `E01_kamar_nightstand.png` | `H_herman_front_medium.png` |
| SH03 MCU Herman+ponsel | `E01_kamar_bed3q.png` | `H_herman_front_medium.png` + `H_herman_front_closeup.png` |
| SH04 MS samping ranjang | `E01_kamar_bed3q.png` (+ `E01_kamar_master.png`) | `H_herman_front_full.png` + `H_herman_profileA_full.png` |

---

## SEQ1-SC01-SH01 — CU wajah Herman (Ratna soft di belakang) · segmen 5 dtk
Attach tiap frame: `H_herman_front_closeup.png` + `R_ratna_front_full.png` (istri tidur di sisi camera-left, uncovered — kamar privat hanya mahram, per R-ratna §0) + `E01_kamar_bed3q.png`.

### SH01-START (prompt utuh — mata terpejam, lelap)
```json
{
  "mood": "intimate pre-dawn domestic stillness, quiet awakening, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "private bedroom of an urban middle-class married couple, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn darkness before sunrise",
  "atmosphere": "quiet lived-in domestic calm, dim near-dark stillness",
  "environment_reference": "attached reference plate E01_kamar_bed3q.png, same bedroom, identical furniture, identical layout, identical materials, single Hokusai Great Wave print, faithful room match, new camera per shot block only",
  "character_identity_husband": {
    "identity_reference": "attached reference plate H_herman_front_medium.png, same identical face, same identity, faithful facial and head-and-torso match",
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style_husband": {
    "makeup": "bare mature skin, fine natural texture preserved, faint sleep-creased cheek, matte finish zero shine",
    "wardrobe": "plain cotton crew-neck sleep tee muted slate-grey",
    "hair": "uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, chalky matte finish, noticeably tousled bed-head sticking up unevenly, mussed and flattened on one side, clearly disordered from sleep"
  },
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_front_full.png, same identical face, same identity, faithful facial match, his wife Ratna asleep beside him",
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, fine natural texture preserved, matte finish zero shine",
    "wardrobe": "plain cotton long-sleeve sleep top muted slate-blue",
    "hair": "long uniformly dark hair worn loose, tousled and mussed from sleep, spread unevenly across the pillow, dry matte hair, chalky matte finish"
  },
  "subject_state": "static",
  "action": "lying on back on the bed, head settled into the pillow, eyelids closed in sleep",
  "pose": "supine on the camera-right side of the bed nearest his nightstand, head resting on pillow, bedding creased around him, his wife Ratna asleep on the camera-left side of the bed, lying on her back, head on the pillow, hair loose across the pillow, bedding drawn over her, both occupying the shared bed, face upward to the ceiling",
  "expression": "eyes closed soft, eyelids still, brows relaxed smooth, mouth slack in sleep, overall face slack and open, fully at rest",
  "framing": "CU close-up on Herman's face filling the frame, tight intimate crop, his sleeping wife soft and partial in the near background camera-left",
  "angle": "over-bed three-quarter high angle looking down onto the resting face, off-axis composition, anti-cliché",
  "camera": "50mm prime spherical, shallow focus on the eyes, soft background falloff",
  "lighting": "very low-key pre-dawn darkness, most of the room sinking into deep shadow, only a faint cool blue glow from the left-wall window before sunrise, face gently modelled by that faint blue light, cool blue-grey shadows, slightly warm skin midtones, underexposed moody rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, sleep-disturbed grooming"
}
```

### SH01-END (prompt utuh — ANCHOR ke render START, hanya mata terbuka menatap ke langit-langit)
**Attach (MANDATORY: karakter + lingkungan + start/end-ref SELALU ada):** `sc01_sh01_start.png` (START-ref komposisi) + `E01_kamar_master.png` (LINGKUNGAN) + `H_herman_front_closeup.png` + `R_ratna_front_full.png` (KARAKTER). Prompt = minimal-change: komposisi/posisi/framing/lighting IDENTIK START, hanya Lapis-4 (mata) berubah. (Catatan: pair SH01 sudah ter-render sebelum aturan ini; plate lingkungan ditambahkan ke spec untuk konsistensi, tanpa regen.)
```json
{
  "composition_reference": "attached frame sc01_sh01_start.png, the SH01-START render, identical composition, same head and pillow position, same room crop, same MCU framing, same lighting and grade, only the eyes change",
  "environment_reference": "attached reference plate E01_kamar_master.png, same bedroom, identical layout and materials, single Hokusai Great Wave print, faithful room match",
  "mood": "intimate pre-dawn domestic stillness, quiet awakening, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "private bedroom of an urban middle-class married couple, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn darkness before sunrise",
  "atmosphere": "quiet lived-in domestic calm, dim near-dark stillness",
  "character_identity_husband": {
    "identity_reference": "attached reference plate H_herman_front_medium.png, same identical face, same identity, faithful facial and head-and-torso match",
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style_husband": {
    "makeup": "bare mature skin, fine natural texture preserved, faint sleep-creased cheek, matte finish zero shine",
    "wardrobe": "plain cotton crew-neck sleep tee muted slate-grey",
    "hair": "uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, chalky matte finish, noticeably tousled bed-head sticking up unevenly, mussed and flattened on one side, clearly disordered from sleep"
  },
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_front_full.png, same identical face, same identity, faithful facial match, his wife Ratna asleep beside him",
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, fine natural texture preserved, matte finish zero shine",
    "wardrobe": "plain cotton long-sleeve sleep top muted slate-blue",
    "hair": "long uniformly dark hair worn loose, tousled and mussed from sleep, spread unevenly across the pillow, dry matte hair, chalky matte finish"
  },
  "subject_state": "dynamic",
  "action": "eyelids lifting open slowly, one slow blink, pupils settling into focus up toward the ceiling above him",
  "pose": "supine on the camera-right side of the bed nearest his nightstand, head resting on pillow, bedding creased around him, his wife Ratna asleep on the camera-left side of the bed, lying on her back, head on the pillow, hair loose across the pillow, bedding drawn over her, both occupying the shared bed, face turned up toward the ceiling, head and pillow position held identical to the start frame",
  "expression": "eyes open heavy-lidded, gaze drifting up to the ceiling above, eyes directed upward over the camera, brows faintly raised, under-eyes puffy with sleep, mouth still slack, groggy just-woken micro-tension",
  "framing": "CU close-up on Herman's face filling the frame, tight intimate crop, his sleeping wife soft and partial in the near background camera-left, identical crop to the start frame",
  "angle": "over-bed three-quarter high angle looking down onto the resting face, off-axis composition, anti-cliché",
  "camera": "50mm prime spherical, shallow focus on the eyes, soft background falloff",
  "lighting": "very low-key pre-dawn darkness, most of the room sinking into deep shadow, only a faint cool blue glow from the left-wall window before sunrise, face gently modelled by that faint blue light, cool blue-grey shadows, slightly warm skin midtones, underexposed moody rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, sleep-disturbed grooming"
}
```

> **Aturan pasangan (berlaku semua END):** frame END di-anchor ke render START (`composition_reference`) + **plat lingkungan WAJIB** + plat wajah (karakter), prompt minimal-change. Jadi SH02-END anchor ke render SH02-START, dst. Jangan generate END dari plat saja — TAPI plat lingkungan TETAP wajib diattach (render anchor saja tak cukup untuk objek yang diberi aksi → halusinasi). Triad MANDATORY tiap frame: karakter + lingkungan + start/end-ref.

**Audit SH01:** kamera over-bed 3/4 off-axis; kucel state di Lapis-4 + hair/makeup; warmth hanya `color_grade`; lighting dim jujur ke 04.40; negasi 0; tak ada device di frame; tiap frame bawa baris attachment sendiri.

---

## SEQ1-SC01-SH02 — CU ponsel di nakas · segmen 5 dtk
**Attach per frame:** START = `E01_kamar_nightstand.png` (subjek/props) + `H_herman_front_medium.png` + `R_ratna_front_full.png` (Herman menjangkau + istri tidur, Lapis-3) + `sc01_sh01_end.png` (acuan cahaya subuh gelap). END = `sc01_sh02_start.png` (komposisi) + `H_herman_front_medium.png` + `R_ratna_front_full.png`. Layar OFF total (A1 — `Waktu Subuh`+kartu sarung ke After Effects). Catatan kunci: manusia ada di PROMPT (Lapis-3), bukan diharap dari attachment.

### SH02-START (prompt utuh — Herman menjangkau ponsel, istri tidur, layar OFF)
```json
{
  "mood": "intimate pre-dawn domestic stillness, quiet awakening, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "private bedroom of an urban middle-class married couple, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn darkness before sunrise",
  "atmosphere": "quiet lived-in domestic calm, dim near-dark stillness",
  "environment_reference": "attached reference plate E01_kamar_nightstand.png, same nightstand, identical props, identical materials, faithful match",
  "lighting_reference": "attached frame sc01_sh01_end.png used only as the lighting and bedding reference, same very low-key cool blue pre-dawn darkness, same deep-shadow matte bedding tone, lighting and bedding role only",
  "subject_anchor": {
    "primary_subject": "IKEA MALM 2-drawer chest white stained oak veneer as nightstand camera-right of the bed, a smartphone lying screen-up near the front edge closest to camera, screen fully dark and switched off, the phone the dominant foreground element",
    "subject_material": "oak veneer particleboard, matte glass phone screen dark and switched off, brushed aluminium phone body",
    "supporting_objects": {
      "lamp": "table lamp with fabric shade switched off",
      "headboard": "headboard edge behind, otherwise uncluttered surface"
    }
  },
  "character_identity_husband": {
    "identity_reference": "attached reference plate H_herman_front_medium.png, same identical face, same identity, faithful facial match",
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, full uniformly grey moustache trimmed even tone",
    "body_features": "average build, 168cm frame, mature male hand and forearm"
  },
  "character_style_husband": {
    "makeup": "bare mature skin, faint sleep-creased cheek, matte finish zero shine",
    "wardrobe": "plain cotton crew-neck sleep tee muted slate-grey",
    "hair": "uniformly salt-and-pepper hair, noticeably tousled bed-head, mussed and flattened one side, disordered from sleep"
  },
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_front_full.png, same identical face, same identity, faithful facial match, his wife Ratna asleep",
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, gentle full cheeks",
    "body_features": "soft maternal build, 158cm frame"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, matte finish zero shine",
    "wardrobe": "plain cotton long-sleeve sleep top muted slate-blue",
    "hair": "long dark hair worn loose, tousled and mussed from sleep, spread across the pillow"
  },
  "subject_state": "dynamic",
  "action": "Herman lying on the camera-right side of the bed, head on the pillow just woken, extending his near hand toward the phone on the nightstand, fingers approaching but not yet touching; his wife Ratna asleep on the camera-left side",
  "pose": "Herman supine turning slightly toward the nightstand, near arm reaching out; Ratna asleep on her side camera-left, head on pillow",
  "expression": "Herman eyes open heavy-lidded groggy just-woken; Ratna face relaxed asleep",
  "framing": "CU favouring the nightstand, phone dominant in the lower-front of frame, Herman's head on the pillow and reaching arm entering the upper-right, Ratna asleep soft in the deeper background camera-left",
  "angle": "eye-level slight high angle across the nightstand toward the bed, off-axis composition, anti-cliché",
  "camera": "35mm prime spherical, phone in sharp foreground focus, figures in soft falloff",
  "lighting": "very low-key pre-dawn darkness, nightstand and phone in deep shadow, only a faint cool blue glow from the left-wall window before sunrise, cool blue-grey shadows, underexposed moody rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```

### SH02-END (ANCHOR ke render SH02-START — Herman setengah bangkit + ambil ponsel)
**Attach:** `scene-images/sc01/sc01_sh02_start.png` (render SH02-START = jangkar ruang/identitas/cahaya) + `H_herman_front_medium.png` + `R_ratna_front_full.png`. Beda dari START = GERAK: Herman setengah bangkit (menumpu siku) + mengangkat ponsel → menyambung SH03 (bersandar pegang HP). Ruang/identitas tetap dari render START. **Layar ON menghadap wajah Herman, TAPI HP dipegang punggung-ke-kamera** → glow biru layar memancar ke wajah, konten layar tak terlihat lensa (A1 aman: muka layar tak menghadap kamera; UI tetap ke AE bila perlu).
```json
{
  "composition_reference": "attached frame sc01_sh02_start.png, the SH02-START render — same room, same nightstand, same Ratna asleep camera-left, same identities, same low-key cool-blue lighting and grade; CHANGE: Herman now half-risen propping on his near elbow, torso lifted off the bed, the phone lifted into his hand",
  "environment_reference": "attached reference plate E01_kamar_nightstand.png, same nightstand and bedside geometry, identical props and materials, faithful match",
  "mood": "intimate pre-dawn domestic stillness, quiet awakening, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "private bedroom of an urban middle-class married couple, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn darkness before sunrise",
  "atmosphere": "quiet lived-in domestic calm, dim near-dark stillness",
  "character_identity_husband": {
    "identity_reference": "attached reference plate H_herman_front_medium.png, same identical face, same identity, faithful facial match",
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, full uniformly grey moustache trimmed even tone",
    "body_features": "average build, 168cm frame, mature male hand and forearm"
  },
  "character_style_husband": {
    "makeup": "bare mature skin, faint sleep-creased cheek, matte finish zero shine",
    "wardrobe": "plain cotton crew-neck sleep tee muted slate-grey",
    "hair": "uniformly salt-and-pepper hair, noticeably tousled bed-head, mussed and flattened one side, disordered from sleep"
  },
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_front_full.png, same identical face, same identity, faithful facial match, his wife Ratna asleep",
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, gentle full cheeks",
    "body_features": "soft maternal build, 158cm frame"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, matte finish zero shine",
    "wardrobe": "plain cotton long-sleeve sleep top muted slate-blue",
    "hair": "long dark hair worn loose, tousled and mussed from sleep, spread across the pillow"
  },
  "subject_state": "dynamic",
  "action": "Herman lifting his head off the pillow and propping up onto his near elbow, beginning to rise, his hand lifting the phone off the nightstand and turning it so its rear casing faces the camera and the lit screen faces his own face; his wife Ratna still asleep camera-left, calm and motionless",
  "pose": "Herman half-risen propped on one elbow, torso lifted off the bed, phone held in his hand rear casing toward the camera, lit screen toward his face; Ratna asleep on her side camera-left",
  "expression": "Herman eyes open more awake, groggy lifting register; Ratna face relaxed asleep; phone screen remaining fully dark",
  "framing": "MCU of Herman half-rising on his elbow with the phone in his hand, nightstand and lamp camera-right, Ratna asleep soft in the background camera-left",
  "angle": "eye-level three-quarter onto Herman half-risen, off-axis composition, anti-cliché",
  "camera": "35mm prime spherical, focus on Herman's face and the held phone, soft background falloff",
  "lighting": "cool-blue glow from the phone's lit screen spilling onto Herman's face and hand, the phone held rear casing toward the camera so the screen content stays hidden from the lens, the rest very low-key pre-dawn darkness with a faint cool blue window glow, cool blue-grey shadows, underexposed moody rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```

**Audit SH02:** layar OFF total (A1); insert top-down off-axis; `clean uncluttered screen space` buat compositing; HP screen-up dark (deviasi sadar dari plat face-down); lighting dim jujur; negasi 0; warmth cuma `color_grade`; tiap frame bawa baris attachment sendiri.

---

## SEQ1-SC01-SH03 — Herman duduk di tepi ranjang menatap ponsel (Ratna tidur di belakang) · segmen 5 dtk
Attach SH03-START: `sc01_sh02_end.png` (START-ref kontinuitas/cahaya) + `E01_kamar_bed3q.png` (LINGKUNGAN ruang/headboard) + `E01_kamar_nightstand.png` (LINGKUNGAN nakas, foreground camera-right) + `H_herman_profileB_medium.png` SAJA (KARAKTER Herman — PROFIL hadap camera-right; front_medium DIBUANG karena frontal mendominasi) + `R_ratna_front_medium.png` (KARAKTER Ratna berbaring di belakang camera-left, head-and-torso). **Layar ON menghadap mata Herman, HP edge-ke-kamera** → glow biru ke wajah, konten (grafik saham) tak terlihat lensa, ke AE.

**🎥 SUDUT KAMERA SH03 (akar fix — orientasi = plat yang cocok):** Herman duduk **PROFIL menghadap camera-RIGHT ke arah nakas** (plat `profileB` = hadap camera-right; **lampirkan profileB SAJA, BUANG front_medium** — frontal mendominasi & tak ada plat 3/4). **Nakas + lampu + ponsel di FOREGROUND camera-right** tepat di hadapan profilnya. Aksi taruh-ponsel: **tangan camera-right** turun ke nakas camera-right; **tangan camera-left** diam di paha camera-left; Ratna tidur camera-left. NOL token kabur (`near`/`beside`) — semua camera-LEFT/RIGHT. (Pelajaran: shot frontal tak bisa render aksi menjangkau objek samping; "3/4" tak punya plat → balik frontal; pakai PROFIL + plat profileB tunggal. Profile A SALAH: hadap camera-left = membelakangi nakas.) Arc pose: SH02 siku → **SH03 duduk tepi profil-kanan + taruh ponsel ke nakas** → SH04 berdiri.

### SH03-START (prompt utuh — Herman duduk di tepi ranjang, menatap ponsel)
```json
{
  "mood": "intimate pre-dawn domestic stillness, quiet awakening, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "private bedroom of an urban middle-class married couple, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn darkness before sunrise",
  "atmosphere": "quiet lived-in domestic calm, dim near-dark stillness",
  "composition_reference": "attached frame sc01_sh02_end.png, the SH02-END render, continuity anchor — same Herman, same wife Ratna asleep toward camera-left, same cool-blue pre-dawn lighting and grade; Herman now risen further to sit on the edge of the bed in three-quarter view",
  "environment_reference": "attached reference plates E01_kamar_bed3q.png and E01_kamar_nightstand.png, same bedroom, the IKEA MALM nightstand with its lamp standing at camera-right, identical furniture, single Hokusai Great Wave print, faithful room and headboard match",
  "character_identity_husband": {
    "identity_reference": "attached reference plate H_herman_profileB_medium.png, same identical face, same identity, faithful profile and head-and-torso match, Herman seen in profile with his face pointing toward camera-right",
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style_husband": {
    "makeup": "bare mature skin, fine natural texture preserved, faint sleep-creased cheek, matte finish zero shine",
    "wardrobe": "plain cotton crew-neck sleep tee muted slate-grey",
    "hair": "uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, chalky matte finish, noticeably tousled bed-head sticking up unevenly, mussed and flattened on one side, clearly disordered from sleep"
  },
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_front_medium.png, his wife Ratna asleep reclining on the bed behind him toward camera-left, head and upper torso, faithful identity and facial match, soft background",
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, gentle full cheeks",
    "body_features": "soft maternal build, 158cm frame"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, fine natural texture preserved, matte finish zero shine",
    "wardrobe": "plain cotton long-sleeve sleep top muted slate-blue",
    "hair": "long uniformly dark hair worn loose, tousled and mussed from sleep, spread unevenly across the pillow, dry matte hair, chalky matte finish"
  },
  "subject_state": "static",
  "action": "sitting on the edge of the bed seen in profile, his body and face turned in profile toward camera-right toward the nightstand, reading the phone held up in his camera-right hand at his profile, the lit screen facing his own eyes and the phone edge toward the lens; his camera-left hand resting on his camera-left thigh; the nightstand with its lamp standing in the camera-right foreground in front of him",
  "pose": "Herman seated on the edge of the bed in profile, feet down on the rug, his body and face turned in profile toward camera-right facing the nightstand, his camera-right hand holding the phone up at his profile screen toward his eyes, his camera-left hand flat on his camera-left thigh, the camera-right foreground occupied by the nightstand and lamp he faces; his wife Ratna asleep on the bed behind him toward camera-left, lying down head on the pillow hair loose",
  "expression": "eyes open sleep-heavy settling into focus on the screen, brows faintly drawn in early attention, mouth still relaxed, groggy just-woken register",
  "framing": "MCU of Herman seated in profile on the edge of the bed facing camera-right, head and torso in frame so the seated profile reads, the nightstand and lamp in the camera-right foreground he faces, his profile catching the cool-blue phone glow, the held phone in the lower frame, his sleeping wife soft in the deeper background toward camera-left, phone screen hidden from camera",
  "angle": "eye-level, Herman seated in profile facing camera-right toward the nightstand, off-axis composition, anti-cliché, the nightstand and phone in the camera-right foreground",
  "camera": "50mm prime spherical, Herman in profile facing camera-right, shallow focus on the face, the camera-right foreground nightstand softly held, soft background falloff",
  "lighting": "cool-blue screen-glow from the phone's lit screen lighting Herman's profile from the side as the key light, phone held with its edge toward the lens and the screen angled toward his own face so the screen content stays hidden from the lens, the rest of the room in very low-key pre-dawn darkness, faint cool blue window glow, cool blue-grey shadows, deep shadow falloff, matte skin rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, sleep-disturbed grooming"
}
```

### SH03-END (ANCHOR ke render SH03-START — letakkan ponsel ke nakas)
**Attach (MANDATORY: karakter + lingkungan + start/end-ref SELALU ada):** `sc01_sh03_start.png` (START-ref = komposisi 3/4 duduk-tepi) + `E01_kamar_nightstand.png` (LINGKUNGAN = geometri nakas camera-right, permukaan target taruh HP) + `E01_kamar_bed3q.png` (LINGKUNGAN ruang) + `H_herman_profileB_medium.png` SAJA (KARAKTER Herman PROFIL hadap camera-right; front_medium DIBUANG) + `R_ratna_front_medium.png` (KARAKTER Ratna berbaring belakang camera-left). Beda dari START = GERAK terukur: **tangan camera-right Herman SUDAH menaruh ponsel face-down di permukaan nakas camera-right**, jari lepas di atas permukaan nakas (BUKAN di lutut), tangan camera-left tetap di paha camera-left, angguk kecil selesai, glow biru padam. Herman tetap **profil hadap camera-right ke arah nakas** (sudut sama dari START). Jembatan ke SH04 (ponsel sudah di nakas).
```json
{
  "composition_reference": "attached frame sc01_sh03_start.png, the SH03-START render, same Herman seated on the edge of the bed in profile facing camera-right toward the nightstand, same crop and framing, same nightstand in the camera-right foreground; CHANGE: Herman's camera-right hand has carried the phone down and set it face-down on the camera-right nightstand surface, his fingertips lifting off it on the nightstand, the screen-glow already gone from his face",
  "environment_reference": "attached reference plates E01_kamar_nightstand.png and E01_kamar_bed3q.png, the IKEA MALM nightstand camera-right with its lamp in the camera-right foreground, the exact surface where Herman sets the phone down, the smartphone now resting face-down flat on that nightstand surface dark screen down clearly visible in the camera-right foreground, identical nightstand geometry and materials, faithful match",
  "mood": "intimate pre-dawn domestic stillness, quiet awakening, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "private bedroom of an urban middle-class married couple, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn darkness before sunrise",
  "atmosphere": "quiet lived-in domestic calm, dim near-dark stillness",
  "character_identity_husband": {
    "identity_reference": "attached reference plate H_herman_profileB_medium.png, same identical face, same identity, faithful profile and head-and-torso match, Herman seen in profile with his face pointing toward camera-right",
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style_husband": {
    "makeup": "bare mature skin, fine natural texture preserved, faint sleep-creased cheek, matte finish zero shine",
    "wardrobe": "plain cotton crew-neck sleep tee muted slate-grey",
    "hair": "uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, chalky matte finish, noticeably tousled bed-head sticking up unevenly, mussed and flattened on one side, clearly disordered from sleep"
  },
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_front_medium.png, his wife Ratna asleep reclining on the bed behind him toward camera-left, head and upper torso, faithful identity and facial match, soft background",
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, fine natural texture preserved, matte finish zero shine",
    "wardrobe": "plain cotton long-sleeve sleep top muted slate-blue",
    "hair": "long uniformly dark hair worn loose, tousled and mussed from sleep, spread unevenly across the pillow, dry matte hair, chalky matte finish"
  },
  "subject_state": "dynamic",
  "action": "the smartphone now resting face-down flat on the camera-right nightstand surface, Herman's camera-right hand on the nightstand fingertips just lifting off the phone he has set down, his camera-left hand resting on his camera-left thigh, a small settled nod completed",
  "pose": "Herman seated on the edge of the bed in profile facing camera-right toward the nightstand, his camera-right arm extended down and forward to the camera-right nightstand where the phone now lies face-down, camera-right fingertips just above it on the nightstand surface, his camera-left hand flat on his camera-left thigh; his wife Ratna asleep on the bed behind him toward camera-left, head on the pillow hair loose",
  "expression": "eyes lowered off the dark phone, calm settled acknowledgement, brows level, mouth softly closed, a small nod",
  "framing": "MCU of Herman seated in profile on the edge of the bed facing camera-right, the camera-right foreground nightstand bearing the face-down phone clearly visible with his camera-right hand on the nightstand surface, his sleeping wife soft in the deeper background toward camera-left, identical crop to the start frame",
  "angle": "eye-level, Herman seated in profile facing camera-right toward the nightstand, off-axis composition, anti-cliché, the nightstand and face-down phone in the camera-right foreground",
  "camera": "50mm prime spherical, Herman in profile facing camera-right, the camera-right foreground nightstand and phone in focus, soft background falloff",
  "lighting": "the cool-blue screen-glow already gone from Herman's face now the phone rests dark and face-down on the camera-right nightstand, the room settled into very low-key pre-dawn darkness, faint cool blue window glow, cool blue-grey shadows, deep shadow falloff, matte skin rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, sleep-disturbed grooming"
}
```

**Audit SH03 (revisi PROFIL + plat profileB-tunggal — akar fix):** Herman **PROFIL hadap camera-RIGHT ke arah nakas** (plat `profileB`; konvensi A=left/B=right); **lampirkan profileB SAJA, front_medium DIBUANG** (frontal mendominasi, tak ada plat 3/4). **Nakas + lampu + ponsel di FOREGROUND camera-right** tepat di hadapan profilnya (objek di-enumerasi). Aksi taruh-ponsel terukur: **tangan camera-right** menaruh ponsel face-down di nakas camera-right; **tangan camera-left** di paha camera-left; Ratna tidur camera-left. NOL token kabur (`near`/`beside` dibuang). HP edge-ke-kamera, layar ON ke mata (glow biru nyata; grafik saham AE; A1 aman). Negasi 0; warmth cuma `color_grade`. START & END berbagi sudut sama (pasangan i2v). Attach: START = `sc01_sh02_end` + `bed3q` + `nightstand` + `H_herman_profileB_medium` + `R_ratna_front_medium` (5 file); END = `sc01_sh03_start` + `nightstand` + `bed3q` + `H_herman_profileB_medium` + `R_ratna_front_medium` (5 file). **Pelajaran terkunci: (1) orientasi HANYA dari plat yang cocok — tak ada plat 3/4, jangan minta 3/4; (2) frontal mendominasi → untuk profil lampirkan plat profil SAJA, buang front; (3) arah hadap cocok sisi objek (objek camera-right → profileB); (4) "HP punggung-square-ke-kamera + baca" memaksa frontal — pakai HP edge-ke-kamera; (5) tiap tangan camera-LEFT/RIGHT, nol token kabur.**

---

## SEQ1-SC01-SH04 — MS samping ranjang · segmen 5 dtk
Attach: START = `sc01_sh03_end.png` (ACUAN CAHAYA + KONTINUITAS — subuh gelap cool-blue, tone tekstil, posisi Herman/Ratna lanjut dari SH03-END) + `H_herman_profileA_full.png` SAJA (Herman PROFIL hadap camera-left; front_full DIBUANG — frontal mendominasi) + `R_ratna_front_full.png` (istri berbaring camera-left) + `E01_kamar_bed3q.png` + `E01_kamar_master.png`; END = `sc01_sh04_start.png` + `R_ratna_front_medium.png` (istri duduk, fokus tajam) + `H_herman_profileA_full.png` (Herman soft foreground profil) + `E01_kamar_bed3q.png` + `E01_kamar_master.png`. **🎥 ORIENTASI SH04 (pelajaran SH03):** Herman berdiri **PROFIL hadap camera-LEFT** (menghadap ruang + ke arah Ratna camera-left → memotivasi rack-focus END); punggung ke nakas camera-right yang sudah selesai. profileA-tunggal, NOL campur front. **Wardrobe KONSISTEN kedua frame: sleep tee + celana panjang kolor (long drawstring lounge pants)** — Herman bangun sudah berpakaian, TIDAK ganti baju di scene ini. Payoff sarung (produk iklan) dipindah ke scene SHOLAT (cut langsung ke sarung + baju sholat) — biar scene kamar tak ruwet/bertele-tele.

### SH04-START (prompt utuh — telungkupkan ponsel, bangkit berdiri dari tepi ranjang)
```json
{
  "mood": "intimate pre-dawn domestic stillness, quiet awakening, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "private bedroom of an urban middle-class married couple, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn darkness before sunrise",
  "atmosphere": "quiet lived-in domestic calm, dim near-dark stillness",
  "environment_reference": "attached reference plates E01_kamar_bed3q.png and E01_kamar_master.png, same bedroom, identical furniture, identical layout, identical materials, single Hokusai Great Wave print, faithful room match, new camera per shot block only",
  "lighting_reference": "attached frame sc01_sh03_end.png used only as the lighting and continuity reference, not a composition source, same very low-key cool-blue pre-dawn darkness, same deep-shadow matte bedding tone, same Herman just risen from the camera-right edge and same Ratna asleep camera-left, continuity carried forward to this wider MS framing",
  "character_identity_husband": {
    "identity_reference": "attached reference plate H_herman_profileA_full.png, same identical face, same identity, same build, faithful profile match, Herman seen in profile with his body and face turned toward camera-left",
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style_husband": {
    "makeup": "bare mature skin, fine natural texture preserved, faint sleep-creased cheek, matte finish zero shine",
    "wardrobe": "plain cotton crew-neck sleep tee muted slate-grey, plain cotton long drawstring lounge pants muted slate",
    "hair": "uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, chalky matte finish, noticeably tousled bed-head sticking up unevenly, mussed and flattened on one side, clearly disordered from sleep",
    "footwear": "barefoot"
  },
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_front_full.png, same identical face, same identity, faithful facial match, his wife Ratna asleep on the bed toward camera-left",
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, fine natural texture preserved, matte finish zero shine",
    "wardrobe": "plain cotton long-sleeve sleep top muted slate-blue",
    "hair": "long uniformly dark hair worn loose, tousled and mussed from sleep, spread unevenly across the pillow, dry matte hair, chalky matte finish"
  },
  "subject_state": "dynamic",
  "action": "having just laid the phone face-down on the nightstand camera-right, turning his body to face camera-left and pushing up from the bed edge to stand, weight rising onto his feet on the rug, his camera-right hand pressing off the mattress",
  "pose": "Herman rising from the camera-right edge of the bed in profile facing camera-left, torso lifting upright mid-motion to standing, feet on the rug, his back to the camera-right nightstand he has finished with; his wife Ratna asleep on the camera-left side of the bed behind him, lying down head on the pillow hair loose",
  "expression": "eyes open awake but still soft, calm settled, mouth relaxed, mild morning heaviness",
  "framing": "MS to medium-full, head to mid-thigh, Herman in profile facing camera-left rising at the camera-right edge of the bed, nightstand camera-right behind him, headboard and Hokusai print behind, Ratna asleep camera-left",
  "angle": "eye-level three-quarter from the foot-left of the bed, off-axis composition, anti-cliché",
  "camera": "35mm prime spherical, deep focus front to back",
  "lighting": "very low-key pre-dawn darkness, most of the room sinking into deep shadow, only a faint cool blue glow from the left-wall window before sunrise, figures gently modelled by that faint blue light, cool blue-grey shadows, underexposed moody rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, sleep-disturbed grooming"
}
```

### SH04-END (ANCHOR ke render SH04-START — fokus pindah ke Ratna bangun duduk, lalu cut)
**Attach (MANDATORY: karakter + lingkungan + start/end-ref SELALU ada):** `sc01_sh04_start.png` (START-ref = komposisi layout) + `E01_kamar_bed3q.png` + `E01_kamar_master.png` (LINGKUNGAN = ruang/ranjang tempat Ratna duduk) + `R_ratna_front_medium.png` (KARAKTER fokus tajam, Ratna duduk) + `H_herman_profileA_full.png` (KARAKTER foreground soft, profil hadap camera-left). Beda dari START = **rack focus**: Herman tetap berdiri profil hadap camera-left tapi jatuh ke soft-focus; fokus pindah ke background — Ratna sudah bangun, duduk di ranjang camera-left, jadi subjek tajam. Lalu cut ke scene berikutnya. **KOREKSI komposisi (user 2026-06-23):** kamera digeser lebih ke camera-LEFT + Herman didorong lebih MAJU (massa soft-foreground lebih besar) agar seimbang dengan `sc01_sh04_start.png`.
```json
{
  "composition_reference": "attached frame sc01_sh04_start.png, the SH04-START render — same bedroom, same Herman standing in profile facing camera-left, same Ratna on the bed camera-left, same very low-key cool-blue pre-dawn lighting and grade; CHANGE: the camera moves well to the camera-left, low and close; Herman has stepped much closer to the camera and toward his wife, looming very large as a soft out-of-focus mass filling the camera-right third of the frame, while the focus racks to his wife Ratna who has woken and is sitting up on the bed camera-left, now more centred in the frame as the sharp subject; Herman turns his head to her and the two meet each other's eyes and share a soft warm just-woken smile",
  "environment_reference": "attached reference plates E01_kamar_bed3q.png and E01_kamar_master.png, same bedroom, identical furniture, identical layout, identical materials, single Hokusai Great Wave print, faithful room match",
  "mood": "intimate pre-dawn domestic stillness, quiet awakening, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "private bedroom of an urban middle-class married couple, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn darkness before sunrise",
  "atmosphere": "quiet lived-in domestic calm, dim near-dark stillness",
  "character_identity_husband": {
    "identity_reference": "attached reference plate H_herman_profileA_full.png, same identical face, same identity, same build, faithful profile match, Herman in profile facing camera-left, looming very large as a soft out-of-focus mass filling the camera-right third of frame, stepped much closer toward his wife",
    "role": "Jakarta middle-class export-import office supervisor, modest mature man",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature male, unremarkable approachable, lived-in",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines forehead and eye corners, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build slight midsection softness, 168cm frame, rounded shoulders, natural mature posture"
  },
  "character_style_husband": {
    "makeup": "bare mature skin, fine natural texture preserved, faint sleep-creased cheek, matte finish zero shine",
    "wardrobe": "plain cotton crew-neck sleep tee muted slate-grey, plain cotton long drawstring lounge pants muted slate",
    "hair": "uniformly salt-and-pepper hair, even grey distribution throughout, dry matte hair, chalky matte finish, noticeably tousled bed-head sticking up unevenly, mussed and flattened on one side, clearly disordered from sleep",
    "footwear": "barefoot"
  },
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_front_medium.png, same identical face, same identity, faithful head-and-torso and facial match, his wife Ratna now awake and sitting up on the bed camera-left, the sharp focal subject",
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, fine natural texture preserved, matte finish zero shine",
    "wardrobe": "plain cotton long-sleeve sleep top muted slate-blue",
    "hair": "long uniformly dark hair worn loose, tousled and mussed from sleep, spread unevenly across the pillow, dry matte hair, chalky matte finish"
  },
  "subject_state": "dynamic",
  "action": "the focus racks to his wife Ratna who has just woken and is sitting up on the bed camera-left, lifting her face toward Herman; Herman, having stepped much closer toward her, looms large in the soft-focus foreground filling the camera-right third of the frame and turns his head to her — the two meet each other's eyes and share a soft warm just-woken smile",
  "pose": "Herman standing in profile facing camera-left, stepped much closer to the camera and toward his wife, looming very large as a soft out-of-focus mass filling the camera-right third of the frame, his head turned toward her meeting her gaze; his wife Ratna sitting up on the bed camera-left in sharp focus, more centred in the frame, torso raised off the pillow, one hand on the mattress, hair loose and tousled, her face lifted toward him meeting his eyes",
  "expression": "Ratna and Herman lock eyes, meeting each other's gaze, a soft warm just-woken smile passing between them; Ratna (sharp) looking up toward him with a gentle smile, eyes warm; Herman (soft foreground) head turned toward her, answering with a faint tender smile",
  "framing": "MS, camera well to the camera-left and low, Herman looming as a large soft foreground mass filling the camera-right third of frame, Ratna sitting up more centred camera-left as the sharp focal point, headboard and Hokusai print behind",
  "angle": "eye-level, camera moved well to the camera-left and closer in, low across the foot of the bed, off-axis composition, anti-cliché",
  "camera": "35mm prime spherical, rack focus pulling from the foreground Herman to the background Ratna, shallow depth of field, Ratna sharp and Herman soft",
  "lighting": "very low-key pre-dawn darkness, most of the room sinking into deep shadow, only a faint cool blue glow from the left-wall window before sunrise, figures gently modelled by that faint blue light, cool blue-grey shadows, underexposed moody rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel",
  "hair_stylist": "Tim Muir", "hair_style": "naturalistic mature register, uniformly grey even distribution, sleep-disturbed grooming"
}
```

**Audit SH04 (orientasi diperbaiki — pelajaran SH03):** Herman berdiri **PROFIL hadap camera-LEFT** (plat `profileA_full` TUNGGAL, front_full DIBUANG — frontal mendominasi); menghadap ruang + ke arah Ratna camera-left → memotivasi rack-focus END; punggung ke nakas camera-right yang sudah selesai; tangan camera-right menumpu kasur saat bangkit. Arc: START telungkupkan ponsel + **bangkit BERDIRI profil** (`sc01_sh03_end` acuan cahaya+kontinuitas + profileA_full + R_ratna_front_full + bed3q+master), END **rack focus ke Ratna bangun duduk** camera-left background (Herman soft-foreground profil), lalu CUT; END anchor `sc01_sh04_start` + `R_ratna_front_medium` (Ratna duduk, tajam) + `H_herman_profileA_full` (soft). **Wardrobe KONSISTEN tee + celana panjang kolor** (NOL ganti-baju — sarung ke scene sholat); off-axis 3/4 foot-left; barefoot; warmth cuma `color_grade`; negasi 0; orientasi = plat tunggal cocok, nol campur front+profile; tiap tangan/objek camera-LEFT/RIGHT.

---

## Status manifest
| Shot | Pair authored | Generated | Reviewed |
|---|---|---|---|
| SH01 CU wajah (dark subuh, Ratna soft-bg) | ✅ (START+END utuh) | START ✅ · END ✅ | **PAIR COMPLETE** — `sc01_sh01_start.png` + `sc01_sh01_end.png`; CU rapat, gelap-subuh biru, Ratna camera-left soft, bed-head, mata END terbuka ke langit-langit (bukan lensa), identitas H+R konsisten; siap Kling i2v |
| SH02 CU ponsel (Herman menjangkau + Ratna tidur) | ✅ (START+END utuh) | START ✅ · END ✅ | **PAIR COMPLETE** — `sc01_sh02_start.png` + `sc01_sh02_end.png`; manusia di Lapis-3, START Herman menjangkau (HP di nakas), END Herman setengah bangkit + HP punggung-ke-kamera layar-ON glow biru ke wajah, Ratna tidur kiri, subuh gelap; siap Kling i2v |
| SH03 MCU profil camera-right + ponsel | ✅ (profil + profileB-tunggal) | START ✅ · END ✅ | **PAIR COMPLETE** — `sc01_sh03_start.png` + `sc01_sh03_end.png`; Herman PROFIL hadap camera-right (fix berhasil: profileB-tunggal, front_medium dibuang), START baca HP glow biru, END HP sudah di nakas camera-right + tangan camera-right lepas di permukaan + glow padam, Ratna tidur camera-left, subuh gelap; siap Kling i2v |
| SH04 MS samping (profil) | ✅ (profileA-tunggal + lighting-ref) | START ✅ · END ✅ | **PAIR COMPLETE** — `sc01_sh04_start.png` + `sc01_sh04_end.png`; START Herman bangkit PROFIL hadap camera-left (profileA-tunggal), END kamera geser camera-left + Herman besar foreground kanan + **keduanya beradu pandang + senyum hangat**, rack-focus ke Ratna duduk tajam; kontinuitas dari `sc01_sh03_end`; siap Kling i2v |

**GATE B SEQ1-SC01 SELESAI 8/8 — SEMUA KEYFRAME ACCEPTED (2026-06-23).** 8 render di `scene-images/sc01/`: `sc01_sh0{1,2,3,4}_{start,end}.png`, nol `Content` leftover. Identity-lock H+R tahan, subuh cool-blue konsisten, arc pose rebah→bangun→siku→duduk-profil→taruh-HP→berdiri→adu-pandang+senyum. NEXT: **GATE C** — Kling 3.0 i2v (5dtk, 1080p audio-on, dual reference-lock env+wajah per shot) → VO TTS terpisah → grafis A1 di After Effects → assemble → PILOT REPORT (apakah dual reference-lock bertahan di i2v).
