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
