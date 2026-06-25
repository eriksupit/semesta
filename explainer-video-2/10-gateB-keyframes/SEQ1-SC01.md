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

## SEQ1-SC01-SH01 — ECU/CU mata Herman · overhead · 50mm
- **Intent (03):** start = mata terpejam, lelap. end = mata terbuka, mengerjap, fokus ke langit-langit. Bookend ke coda SEQ6-SC03.
- **SHOT-CONCEPT (FIX — Rule 6a framing-by-union, identik dua frame):** overhead vantage, kamera tepat di atas wajah supine menatap lurus ke bawah; pita mata–alis dominan; 50mm; 16:9. Kamera diam; HANYA mata yang berubah START→END. **Ratna TIDAK di frame** (mustahil terbaca di ECU; ia hadir di SH04).
- **Attachments:** identity `H_herman_front_closeup.png` SAJA. Env TIDAK dilampirkan (ECU tak menampilkan ruang; lampiran env memicu drift-wider Rule 4).
- **START** — mode: **B** · STATUS: ✅ **ACCEPTED 2026-06-26** → `scene-images/sc01/sc01_sh01_start.png`. Review: G0–G6 lolos; identitas Herman held (verifikasi penuh bentuk-mata tertunda ke END karena mata terpejam); render mendarat **CU** (bukan ECU ekstrem — drift-wider Rule 4, eyes tetap dominan, diterima); grade very-low-key subuh sedikit dingin (dalam toleransi). Proven prompt:
```json
{
  "attachment_manifest": {
    "identity_reference": ["H_herman_front_closeup.png — same man, match face shape, grey moustache, salt-and-pepper hair, mature skin texture, calm eyes, match proportions"]
  },
  "mood": "intimate pre-dawn stillness, the first breath before waking, hushed sacred quiet",
  "color_grade": "warm Deakins-style grade, midtones slightly warm, gentle filmic contrast, one warm temperature",
  "style": "photorealistic cinematic still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering, fine film grain",
  "scene": "private bedroom in pre-dawn dark, a mature man lying supine on his back, head resting on a matte slate-grey cotton pillow",
  "location": "indoor",
  "time_of_day": "pre-dawn",
  "atmosphere": "dark hushed pre-dawn dimness, barely-there ambient",
  "scene_depth": {
    "foreground": "the man's eyes and brow filling the frame, the focal centre",
    "midground": "bridge of the nose and the matte slate-grey pillow beneath the head",
    "background": "soft dark out-of-focus bedding falling away"
  },
  "subjects": [
    { "who": "Herman", "identity_reference": "H_herman_front_closeup.png", "wardrobe": "cropped out of this extreme close-up of the eyes" }
  ],
  "subject_state": "static",
  "action": "lying still on his back asleep, both eyes gently closed in the dimness",
  "pose": "supine, face turned up toward the ceiling, head centred on the pillow",
  "gesture": "facial muscles fully relaxed in sleep",
  "expression": "both eyes softly closed, eyelids smooth and still, lips lightly closed, deeply at rest",
  "framing": "ECU extreme close-up, only the eyes-brow-nose-bridge band fills the frame, eyes the dominant subject",
  "angle": "overhead vantage, camera directly above the face looking straight down, face square to the overhead lens",
  "camera": "50mm prime spherical, shallow focus on the eyes, soft fall-off",
  "lighting": "very-low-key pre-dawn darkness, faint cool bluish pre-sunrise glow barely seeping through the curtains, no warm sun risen yet, no practical lamp lit, deep soft shadows across the face, a soft cool wrap grazing the brow, dim near-black ambient",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalist realism",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light, soft directional",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic lived-in skin, real-person feel"
}
```
- **END** — method: **EDIT-IN-PLACE** pada `sc01_sh01_start.png` (BUKAN generate-from-attachment) · STATUS: ✅ **ACCEPTED 2026-06-26** → `scene-images/sc01/sc01_sh01_end.png`. Review: framing **identik START by construction** (edit-in-place — geometri di luar mata = piksel asli; camera-lock deterministik, bukan kebetulan); ekspresi grogi (mata berat/sayu, TIDAK sipit) lebih kuat dari versi generate-from-attachment. Catatan jujur: token `sleep crust`/merah ter-render lemah (akseptabel). **Cara reproduksi:** muat render START di edit-view → set input-fidelity High → (opsional) drop satu comment-point di area mata → di "Describe edits" tempel instruksi token-per-token:
```
open both eyes, just awake, eyes open at natural relaxed rounded width, full natural aperture, gaze straight up toward the camera, faintly bloodshot, slightly red, tired, lightly puffy lower lids, small fleck of sleep crust in each inner eye corner, eyes comfortably rounded, framing unchanged, crop unchanged, head position unchanged, lighting unchanged, skin unchanged, hair unchanged
```
> Metode baku start/end **delta-kecil = edit-in-place** (kanonik: `prompt-rules-text-image-to-image` Part II EDIT-IN-PLACE). Generate-from-attachment (Mode C) = fallback bila tool tak punya edit mode.

## SEQ1-SC01-SH02 — CU ponsel di nakas · top-down insert · 50mm macro
- **Intent (03):** start = layar menyala (`Waktu Subuh 04.42` + kartu iklan sarung — **rendered OFF, UI in After Effects**). end = ibu jari menyentuh "matikan". Insert top-down, screen OFF (A1).
- **SHOT-CONCEPT (FIX — Rule 6a, identik dua frame):** top-down CU/macro insert HP di nakas; kamera di atas permukaan menatap ke bawah; HP dominan; 50mm macro; 16:9. Kamera diam; END hanya menambah ibu jari.
- **Konsistensi antar-shot (BUKAN attach render shot-lain):** token-block `mood/color_grade/style/inti-lighting` disamakan **verbatim ke SH01** + env plate bersama + grade post. Attach render SH01 dilarang (reference-dominance impor komposisi wajah).
- **Attachments:** env `E01_kamar_nightstand.png` SAJA.
- **START** — mode: **B** · STATUS: ✅ **ACCEPTED 2026-06-26** → `scene-images/sc01/sc01_sh02_start.png`. Review: layar gelap/OFF (A1) ✓; ruang (kayu light-oak / base lampu / tepi bantal) cocok plat, nol halusinasi ✓; grade subuh konsisten SH01 ✓; top-down insert mendarat (sedikit high-angle, akseptabel). Proven prompt:
```json
{
  "attachment_manifest": {
    "environment_reference": "E01_kamar_nightstand.png — same nightstand, same phone, same lamp, identical light-oak wood, identical materials, identical layout, new camera only"
  },
  "mood": "intimate pre-dawn stillness, the first breath before waking, hushed sacred quiet",
  "color_grade": "warm Deakins-style grade, midtones slightly warm, gentle filmic contrast, one warm temperature",
  "style": "photorealistic cinematic still, ARRI Alexa Mini LF, 50mm macro prime spherical lens, Kodak Portra rendering, fine film grain",
  "scene": "top-down insert of a smartphone lying flat face-up on the light-oak MALM nightstand surface, dark dormant black glass screen, beside the switched-off table lamp base, headboard edge nearby",
  "location": "indoor",
  "time_of_day": "pre-dawn",
  "atmosphere": "dark hushed pre-dawn dimness",
  "scene_depth": {
    "foreground": "the smartphone lying flat face-up, dark dormant black glass screen, dominant in frame",
    "midground": "matte light-oak nightstand surface around the phone",
    "background": "soft dark, switched-off lamp base at the frame edge"
  },
  "subject_anchor": {
    "primary_subject": "smartphone lying flat face-up on the nightstand, dark dormant matte black glass screen",
    "supporting_objects": { "nightstand": "matte light-oak MALM nightstand surface", "lamp": "table lamp base at frame edge, switched off" },
    "human_absence_signal": "the phone resting alone untouched, the surface around it clear"
  },
  "subject_state": "static",
  "action": "the phone resting still on the nightstand, screen dark and dormant",
  "framing": "ECU macro insert, the phone filling most of the frame, tight on the device",
  "angle": "top-down, camera directly above the nightstand surface looking straight down, phone square to the overhead lens",
  "camera": "50mm macro prime spherical, shallow focus on the phone face",
  "lighting": "very-low-key pre-dawn darkness, faint cool bluish pre-sunrise glow barely seeping through the curtains, no warm sun risen yet, no practical lamp lit, deep soft shadows on the nightstand surface",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "intimate naturalist realism",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in"
}
```
- **END** — method: **EDIT-IN-PLACE** on `sc01_sh02_start.png` (delta: tangan mengambil HP) · STATUS: ✅ **ACCEPTED 2026-06-26** → `scene-images/sc01/sc01_sh02_end.png`. Review: framing **identik START by construction** (edit-in-place) ✓; skin Herman + lighting subuh konsisten ✓; layar OFF (A1) ✓. **Kompromi diterima (logged):** gestur terbaca **telapak menelungkup di atas HP**, BUKAN genggaman-tepi penuh. Re-roll geometri-grip (`1a82e744`) sempat memperbaiki genggaman TAPI **framing-nya geser** → melanggar camera-lock; karena framing = constraint keras, user memilih versi ini (framing utuh > gestur sempurna). Bridge ke SH03 (memegang) masih terbaca. Proven edit-instruction:
```
mature male hand, entering from bottom frame edge, fingers settling onto the smartphone, palm grasping the phone, pre-lift grip, natural relaxed grip, skin tone matched, skin texture matched, skin source attached portrait sc01_sh01_end.png, dim lighting matched, phone flat in place on nightstand, screen dark dormant black glass, nightstand unchanged, lamp unchanged, framing unchanged, crop unchanged, lighting unchanged, color unchanged
```
> **Observasi metode (PENDING, N=1):** instruksi edit yang lebih agresif/panjang (geometri-grip Rules 12–14) JUSTRU drift framing, sedangkan instruksi ini (lebih ringan) menahan framing. Hipotesis: makin besar/agresif delta tangan → makin tinggi risiko resample framing di edit-in-place; edit-in-place menjamin framing kuat pada delta-KECIL (mata), tak sekuat itu pada delta tangan-besar. Konfirmasi di shot lain sebelum jadi aturan.

## SEQ1-SC01-SH03 — MCU Herman + ponsel · 50mm
- **Intent (03):** start = layar bertransisi. end = grafik saham tampil (screen OFF in frame, glow via `lighting`), wajah tersorot cahaya layar hangat, Herman mengangguk.
- **Attachments (TBD):** env `E01_kamar_bed3q.png`; identity Herman (full+closeup per new standard).
- **START** — mode: ___ · STATUS: ⬜ TO AUTHOR
- **END** — mode: C · STATUS: ⬜ TO AUTHOR

## SEQ1-SC01-SH04 — MS samping ranjang · 35mm
- **Intent (03):** start = Herman menelungkupkan ponsel, bangkit duduk. end = berdiri mengenakan sarung (`solid plain-weave sarong, dark muted colorway`). Payoff diegetik dimulai.
- **Attachments (TBD):** env `E01_kamar_bed3q.png` (+ `E01_kamar_master.png` regen); identity Herman full (+ profileA if side-of-bed).
- **START** — mode: ___ · STATUS: ⬜ TO AUTHOR
- **END** — mode: C · STATUS: ⬜ TO AUTHOR
