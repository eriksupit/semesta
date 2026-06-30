---
title: Character Sheet — Recurring Figurans (named, single-scene) · GATE 0
tags: [explainer-video-2, character-sheet, figurans, gate-0]
status: draft
created: 2026-06-21
updated: 2026-06-21
aliases: [ev2-figurans-sheet, F-figurans]
---

# Character Sheet — FIGURANS (named, single-scene) · tag F
> Method, 9-cell template, direction protocol, naming → [[00-README]]. Style tokens + anchors → [[07-style-reference]]. Scene truth → [[03-scene-detail]]. Format authority → [[prompt-rules-image-generation]] (6 lapis) + [[lessons]] (prompt verbatim, nol placeholder).

---

## 0. Notes (read first)
- **Figurans are LIGHTER than main characters** ([[00-README]]:81 — "front + profileA, key shots only"). Zero 9-cell turnaround. Each figuran gets ONLY the plate cells that match the shot-sizes they actually appear in (evidence from [[03-scene-detail]] shot lists). **Profile B + profile full/closeup are never generated** — zero figuran here turns to the far profile or holds a profile shot across the film.
- **Adaptive plate set (locked 2026-06-21, 14 plates for 5 figurans):**
  | Figuran | Scene | Cells to generate | Why (actual shots) |
  |---|---|---|---|
  | Pak Darto | SEQ2-SC01 | `front_full` + `front_medium` + `profileA_medium` | WS gate (24mm, full body) + MS (35mm) |
  | Tika | SEQ3-SC01 | `front_medium` + `profileA_medium` | OTS medium only (50mm) |
  | petugas bank | SEQ3-SC02 | `front_medium` + `front_closeup` + `profileA_medium` | video-call OTS + CU screen (always front webcam) |
  | Rian | SEQ3-SC03 | `front_medium` + `front_closeup` + `profileA_medium` | MCU + OTS + MS (35–50mm) |
  | pembina muda | SEQ4-SC04 | `front_full` + `front_medium` + `profileA_medium` | MWS approach (35mm, ¾ body) + MS |
  - `profileA_medium` is included for every figuran because OTS / ¾ framings appear in their scenes — it helps Kling interpolate the ¾ angle. `front_full` only where a WS/MWS shows the whole body; `front_closeup` only where an MCU/CU lands on the face.
- **Plate = uncovered baseline, faith NOT imposed.** Plates lock the face. Any head covering (hijab/peci) a figuran wears in-scene is added as a GATE B wardrobe layer (same locked rule as Ratna — [[lessons]]:53). For figurans whose religious identity is NOT established in the script, render neutral contemporary modest wear; do not invent a hijab/peci. (Only Ratna's family is established observant.)
- **Render-age:** adults compensate down (model ages up). Adults in §2: Darto 55→50, **Tika re-aged 16→20 (adult, director call 2026-06-21 — unlocks the Lisa adult body-token method, [[lessons]]:54)**, petugas 35→32, Rian 28→25, pembina 25→23.
- **Positive-only tokens, matte plate standard, zero negation, zero keyword-leak** — all the same locked rules as the main sheets ([[prompt-rules-image-generation]] BANNED MASTER LIST; [[lessons]]:88–90).
- **Format compliance (the fix on 2026-06-21):** §3 below holds 14 complete 6-layer JSON prompts, copy-paste ready, zero placeholder — per [[prompt-rules-image-generation]]:44 (STRUKTUR 6 LAPIS mandatory) + [[lessons]]:224 ("prompt harus ada verbatim di file, siap copy-paste, tidak tergantung memory"). The earlier scaffold-and-"paste-the-row" form violated both; replaced.

---

## 1. Reference: shared plate values (already inlined into every §3 cell)
For audit only — every §3 prompt already contains these verbatim. Constant across ALL figuran cells; only `character_identity`, `character_style`, the Lapis-4 state fields, and the view/shot/framing/angle/aspect/camera fields change per cell.
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor", "time_of_day": "studio controlled", "atmosphere": "clinical empty stillness",
  "subject_state": "static",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

**PLATE DEVIATIONS from prompt-rules (declared, justified — same as the main sheets, [[lessons]]:43):** neutral true-to-life `color_grade` (warm grade arrives at GATE B keyframes), clean prime spherical lens (not anamorphic), `scene_depth`/`on_screen_graphic` omitted (plain white isolation), crew scoped to costume/makeup/hair only, portrait aspect per shot. Footwear field present only where feet are in frame (full body); omitted in medium/closeup per positive-only ([[lessons]]:90). All other rules hold.

**Aspect + camera per shot:** full `9:16` / `50mm`, medium `2:3` / `85mm`, closeup `4:5` / `100mm`. Direction protocol ([[00-README]] §3.1): Profile A = subject faces `camera-left`; **zero Profile B** for figurans. Verify each render by visible cheek/ear before approval.

---

## 2. Per-figuran identity + baseline style (reference; inlined into §3)

### F1 — Pak Darto (warung owner, ~55→50) · SEQ2-SC01 · cells: front_full, front_medium, profileA_medium
```json
"character_identity": {
  "role": "Jakarta lower-middle-class neighborhood warung vendor, warm friendly settled presence",
  "ethnicity": "modern Jakartan features, Javanese urban descent",
  "beauty": "ordinary kindly everyday appearance, working-class register, weathered approachable",
  "age": "man 50 years old",
  "facial_features": "mature weathered complexion, soft lined forehead, kind steady eyes, full greying brows, gentle jowl, clean even skin texture",
  "body_features": "stocky settled middle-aged build, slightly rounded, upright relaxed posture"
}
"character_style": {
  "makeup": "groomed natural mature skin, even skin tone, matte setting powder zero shine, fine weathered texture preserved",
  "wardrobe": "short-sleeve collared cotton shirt soft muted olive, plain undershirt visible at collar, relaxed cotton trousers desaturated grey",
  "hair": "short greying side-parted hair, uniformly salt-and-pepper even distribution throughout, dry matte hair, chalky matte finish, neatly combed natural",
  "footwear": "simple rubber sandals, worn casual"
}
```

### F2 — Tika (neighbor helper, 20 — re-aged from 16) · SEQ3-SC01 · cells: front_medium, profileA_medium
```json
"character_identity": {
  "role": "Jakarta neighborhood young woman, part-time helper, bright willing presence",
  "ethnicity": "modern Jakartan features, Javanese urban descent",
  "beauty": "fresh natural young-adult appearance, lower-middle-class register, approachable",
  "age": "woman 20 years old",
  "facial_features": "fresh clear young-adult complexion, smooth skin texture, bright lively eyes, soft natural brows, soft cheeks, clean even jawline",
  "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 160cm frame, upright relaxed posture"
}
"character_style": {
  "makeup": "bare fresh young-adult skin, clean even complexion, natural skin texture, matte finish zero shine",
  "wardrobe": "fitted crew-neck cotton tee soft jersey soft muted dusty-rose, modest contemporary fit",
  "hair": "long uniformly dark hair even tone throughout, simple low tie at nape, soft natural fringe, dry matte hair, chalky matte finish, neatly combed natural"
}
```

### F3 — petugas bank (bank officer, ~35→32) · SEQ3-SC02 · cells: front_medium, front_closeup, profileA_medium
```json
"character_identity": {
  "role": "Jakarta professional bank officer, composed courteous corporate presence",
  "ethnicity": "modern Jakartan features, Javanese urban descent",
  "beauty": "neat professional appearance, middle-class corporate register, polished approachable",
  "age": "man 32 years old",
  "facial_features": "clear even complexion, smooth groomed skin texture, steady attentive eyes, neat defined brows, clean even jawline",
  "body_features": "trim professional adult build, upright composed posture"
}
"character_style": {
  "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, natural texture preserved",
  "wardrobe": "crisp collared dress shirt soft muted slate-blue, neat tidy corporate, plain solid",
  "hair": "short neat side-parted dark hair, uniformly dark even tone throughout, dry matte hair, chalky matte finish, cleanly groomed"
}
```

### F4 — Rian (young office colleague, ~28→25) · SEQ3-SC03 · cells: front_medium, front_closeup, profileA_medium
```json
"character_identity": {
  "role": "Jakarta young office worker, curious eager junior-professional presence",
  "ethnicity": "modern Jakartan features, Javanese urban descent",
  "beauty": "fresh tidy young-adult appearance, middle-class office register, approachable",
  "age": "man 25 years old",
  "facial_features": "distinctive-commoner-features, rounded fuller face shape, soft full cheeks, broad soft jawline, thick full dark brows, deep-set warm almond eyes, light youthful mustache with thin chin stubble, a small mole on the cheek, clear youthful complexion, smooth skin texture",
  "body_features": "stocky compact young-adult build, slightly broad shoulders, upright relaxed posture"
}
"character_style": {
  "makeup": "BB cream sheer coverage, even skin tone, matte setting powder zero shine, youthful texture preserved",
  "wardrobe": "soft collared casual shirt muted charcoal, relaxed office-smart, plain solid",
  "hair": "wavy tousled dark hair medium length, soft natural curl texture, uniformly dark even tone throughout, dry matte hair, chalky matte finish"
}
```

### F5 — pembina muda (young club mentor, ~25→23) · SEQ4-SC04 · cells: front_full, front_medium, profileA_medium
```json
"character_identity": {
  "role": "Jakarta young after-school club mentor, warm encouraging youthful-teacher presence",
  "ethnicity": "modern Jakartan features, Javanese urban descent",
  "beauty": "fresh warm young-adult appearance, middle-class register, friendly approachable",
  "age": "woman 23 years old",
  "facial_features": "distinctive-commoner-features, round full face shape, high soft cheekbones, fuller lips, slightly broad nose, thick full natural brows, warm round expressive eyes, a small beauty mark near the lip, soft dimpled cheeks, fresh clear complexion",
  "body_features": "full curvy young-adult build, natural 36D bustline, full rounded hips, soft rounded waist, 158cm frame, upright relaxed posture"
}
"character_style": {
  "makeup": "light natural foundation even coverage, soft groomed brows, nude soft-matte lip, baked setting powder matte finish zero shine, fresh skin texture preserved",
  "wardrobe": "simple short-sleeve soft blouse muted teal, modest contemporary cut, relaxed casual trousers desaturated grey",
  "hair": "short dark hair, soft natural wave, loose chin-length bob, uniformly dark even tone throughout, dry matte hair, chalky matte finish",
  "footwear": "clean flat canvas shoes, plain"
}
```

### F6 — Ojek (app motorcycle-taxi driver, ~30) · SC03 (eks-SEQ2-SC03) · cells: front_full, front_medium · ✅ prompt LOCKED Fase-2 (generate PENDING, sesi baru)
> Ditambahkan 2026-06-30 (Erik): figuran muncul di shotlist tapi plat belum ada → catat identitas di sini saat Fase-1; prompt plat + generate menyusul di Fase-2. Plat baseline UNCOVERED (wajah dikunci); jaket+helm ojek = lapisan wardrobe GATE B (bukan di plat). Tanpa merek (brand-safe, bukan Gojek/Grab).
```json
"character_identity": {
  "role": "Jakarta app motorcycle-taxi driver, working-class, steady patient service presence",
  "ethnicity": "modern Jakartan features, Javanese Sundanese urban descent",
  "beauty": "plain working-class everyman appearance, weathered friendly",
  "age": "man 30 years old",
  "facial_features": "distinctive-commoner-features, lean angular face shape, short flat nose, light stubble shadow, thick straight brows, calm friendly almond eyes, sun-touched complexion, a small mole on the cheek",
  "body_features": "lean wiry working-class build, 168cm frame, upright ready posture"
}
"character_style": {
  "makeup": "bare healthy male skin, matte finish zero shine, real-person texture preserved",
  "wardrobe": "plate baseline neutral — short-sleeve plain crew-neck tee desaturated grey, relaxed cotton trousers muted charcoal; SCENE wardrobe (GATE B) = generic colored windbreaker jacket plain solid + open-face helmet, no brand, on a motorcycle",
  "hair": "short dark hair, low neat crop, uniformly dark even tone, dry matte hair, chalky matte finish",
  "footwear": "casual low sneakers, plain muted"
}
```
> Plat dibutuhkan (shot-driven SC03-SH05 WIDE Lisa+ojek di gerbang): `F_ojek_front_full` (utama) + `F_ojek_front_medium` (cadangan coverage). Zero Profile B (standar figuran). Generate → `character-images/F_ojek/` (Fase plat).

### F7 — Kurir (last-mile courier, ~28) · SC04 (eks-SEQ2-SC04) · cells: front_full, front_medium · ✅ prompt LOCKED Fase-2 (generate PENDING, sesi baru)
> Ditambahkan 2026-06-30. SC04 = 2 kurir; **1 plat figuran dipakai untuk kurir-1 (foreground); kurir-2 di-stage soft/secondary** (belakang/blur) pakai plat sama atau rear — hindari 2 wajah-kurir ter-lock rapat. Plat baseline UNCOVERED; rompi/seragam kurir = lapisan wardrobe GATE B (tanpa merek, brand-safe).
```json
"character_identity": {
  "role": "Jakarta last-mile delivery courier, working-class, brisk efficient service presence",
  "ethnicity": "modern Jakartan features, Javanese Sundanese urban descent",
  "beauty": "plain working-class everyman appearance, fit practical",
  "age": "man 28 years old",
  "facial_features": "distinctive-commoner-features, square jaw face shape, straight nose, light stubble, thick brows, alert friendly eyes, sun-touched complexion, a small scar on the brow",
  "body_features": "fit sturdy working-class build, broad shoulders, 170cm frame, upright active posture"
}
"character_style": {
  "makeup": "bare healthy male skin, matte finish zero shine, real-person texture preserved",
  "wardrobe": "plate baseline neutral — short-sleeve plain crew-neck tee desaturated steel-blue, relaxed work trousers muted charcoal; SCENE wardrobe (GATE B) = plain solid courier vest/polo + cap, no brand, handling boxes",
  "hair": "short dark hair, low practical crop, uniformly dark even tone, dry matte hair, chalky matte finish",
  "footwear": "sturdy low work shoes, plain muted"
}
```
> Plat dibutuhkan (shot-driven SC04 SH01/SH02/SH05): `F_kurir_front_full` (utama, WIDE memuat+payoff) + `F_kurir_front_medium` (MS memuat kardus). Zero Profile B. Generate → `character-images/F_kurir/` (Fase plat). Kurir-2 = secondary soft pakai plat sama.

### F8 — Peer-mentor (mahasiswi senior, ~22) · SC07 (eks-SEQ2-SC07) · cells: front_full, front_medium · ✅ prompt LOCKED Fase-2 (generate PENDING, sesi baru)
> Ditambahkan 2026-06-30. SC07 = Lisa↔peer-mentor di selasar kampus. Plat baseline UNCOVERED; faith NOT imposed (identitas religi tak ditetapkan → modest contemporary, kerudung TIDAK dipaksakan). Pembeda dari Lisa (mahasiswi 20): mentor sedikit lebih senior/matang, gaya berbeda.
```json
"character_identity": {
  "role": "Jakarta senior university student, peer mentor, warm approachable confident presence",
  "ethnicity": "modern Jakartan features, Javanese urban descent",
  "beauty": "fresh young-adult appearance, friendly mature-student register",
  "age": "woman 22 years old",
  "facial_features": "distinctive-commoner-features, oval face shape, defined cheekbones, warm wide smile, medium-thick natural brows, bright attentive eyes, clear complexion, a small beauty mark near the jaw",
  "body_features": "slim-average young-adult build, natural 34B bustline, 165cm frame, relaxed confident posture"
}
"character_style": {
  "makeup": "light natural foundation even coverage, soft groomed brows, soft rose tinted lip, baked setting powder matte finish zero shine, fresh skin texture preserved",
  "wardrobe": "modest contemporary casual — relaxed soft button cardigan muted mustard over plain crew-neck tee, comfortable straight trousers desaturated navy, campus-casual, head covering not imposed",
  "hair": "medium-length dark hair, soft natural wave, half-tied, uniformly dark even tone, dry matte hair, chalky matte finish",
  "footwear": "clean flat loafers, plain muted"
}
```
> Plat dibutuhkan (shot-driven SC07 SH01/SH04/SH05): `F_mentor_front_full` (WIDE + 2-shot duduk) + `F_mentor_front_medium` (2-shot rapat). Zero Profile B. Generate → `character-images/F_mentor/` (Fase plat).

### F9 — Ibu petugas kebersihan (campus cleaner, perempuan paruh baya ~55) · SC09 (eks-SEQ3-SC09) · cells: front_full, front_medium · ✅ prompt LOCKED Fase-2 (generate PENDING, sesi baru)
> Ditambahkan 2026-06-30. SC09 = Lisa bantu ibu pesan dokter (telemedicine). Plat baseline UNCOVERED; faith NOT imposed (modest paruh-baya; kerudung TIDAK dipaksakan kecuali director menetapkan). Seragam kebersihan kampus = wardrobe GATE B (bukan di plat). Render-age: paruh baya nyata (~55, tak diturunkan; verifikasi guratan usia di plat pertama).
```json
"character_identity": {
  "role": "Jakarta middle-aged campus cleaning staff woman, weathered hardworking gentle presence",
  "ethnicity": "modern Jakartan features, Javanese urban descent",
  "beauty": "humble working-class middle-aged appearance, kind tired warmth",
  "age": "woman 55 years old",
  "facial_features": "distinctive-commoner-features, round softened face shape, fine age lines around eyes and mouth, slightly hollow cheeks, broad gentle nose, thinning natural brows, warm tired eyes, sun-aged complexion, a few age spots",
  "body_features": "stout sturdy middle-aged build, slightly stooped tired posture, 156cm frame"
}
"character_style": {
  "makeup": "bare weathered mature skin, fine wrinkles preserved, matte finish zero shine, real-person texture",
  "wardrobe": "plate baseline neutral — plain modest short-sleeve blouse desaturated grey-green, relaxed dark trousers; SCENE wardrobe (GATE B) = campus cleaning-staff uniform vest/apron, no brand",
  "hair": "greying dark hair, low neat bun, uniformly salt-and-pepper even distribution, dry matte hair, chalky matte finish",
  "footwear": "simple worn flat shoes, plain"
}
```
> Plat dibutuhkan (shot-driven SC09 SH01/SH02/SH04/SH05): `F_ibupetugas_front_full` (MWS + 2-shot) + `F_ibupetugas_front_medium` (2-shot + tangan detail). Zero Profile B. Generate → `character-images/F_ibupetugas/` (Fase plat).

### F10 — Bapak desa lanjut usia (village elder, laki-laki ~62) · SC12 (eks-SEQ5-SC12) · cells: front_full, front_medium · ✅ prompt LOCKED Fase-2 (generate PENDING, sesi baru)
> Ditambahkan 2026-06-30 (Erik: ganti dari "ibu lansia" → variasi demografi + lintas-demografi). SC12 = Lisa bantu bapak desa baca jadwal di terminal. Plat baseline UNCOVERED (wajah dikunci); **peci/kopiah hitam + tongkat = wardrobe/prop GATE B** (bukan di plat). Interaksi Lisa↔bapak NON-MAHRAM → gestur syukur non-sentuh (di scene). Render-age: lansia nyata (~62, tak diturunkan; verifikasi guratan usia di plat pertama).
```json
"character_identity": {
  "role": "Indonesian rural elder man visiting the city, humble devout gentle village presence",
  "ethnicity": "modern Indonesian features, Javanese rural descent",
  "beauty": "weathered humble elderly appearance, kind dignified",
  "age": "man 62 years old",
  "facial_features": "distinctive-commoner-features, lean weathered face shape, deep age lines across forehead and around eyes, sunken cheeks, prominent cheekbones, broad flat nose, thin greying brows, kind tired eyes, dark sun-aged complexion, sparse short grey moustache, a few age spots",
  "body_features": "slight stooped frail elderly build, thin, 162cm frame, leaning posture as if on a cane"
}
"character_style": {
  "makeup": "bare weathered aged male skin, deep wrinkles preserved, matte finish zero shine, real-person texture",
  "wardrobe": "plate baseline neutral — plain modest long-sleeve batik-free button shirt desaturated brown, loose dark trousers; SCENE wardrobe (GATE B) = black peci/kopiah cap + simple shirt + holds a wooden walking cane (tongkat), village-elder modest",
  "hair": "short thinning grey hair, uniformly grey even distribution, dry matte hair, chalky matte finish",
  "footwear": "simple worn sandals, plain"
}
```
> Plat dibutuhkan (shot-driven SC12 SH01/SH02/SH04/SH05): `F_bapakdesa_front_full` (WIDE + 2-shot, bersandar tongkat) + `F_bapakdesa_front_medium` (MS + 2-shot). Zero Profile B. Generate → `character-images/F_bapakdesa/` (Fase plat).

*Scene wardrobe (GATE B), all figurans:* Darto SEQ2-SC01 vendor at stall, baseline, no head covering. Tika SEQ3-SC01 packing helper — religious identity unestablished → neutral modest wear, head covering not imposed (hijab added as GATE B layer only if director establishes her muslimah, broadcast-exposure axis). petugas SEQ3-SC02 video-call from bank desk, neat corporate shirt, front webcam. Rian SEQ3-SC03 office colleague carrying coffee, office-smart casual. pembina SEQ4-SC04 school club mentor, modest contemporary, head covering not imposed (GATE B layer only if established muslimah). Ojek SC03 waiting at gate on a motorcycle, generic colored windbreaker + open-face helmet, no brand, head covering not religious. Kurir SC04 loading boxes, plain courier vest/polo + cap, no brand. Peer-mentor SC07 seated on campus bench, modest campus-casual cardigan, head covering not imposed. Ibu petugas kebersihan SC09 seated on campus bench, campus cleaning-staff uniform vest/apron, head covering not imposed. Bapak desa SC12 at the transit platform, black peci/kopiah cap + simple shirt + wooden cane (tongkat), village-elder modest, non-mahram polite distance from Lisa.

---

## 3. Plate matrix — 24 full t2i prompts (copy-paste ready, zero placeholder)
> F1–F5 = GATE-0 done (accepted renders). **F6–F10 = Fase-2 prompts LOCKED 2026-07-01 (generate PENDING, sesi baru)** — 2 cells each (front_full 9:16/50mm + front_medium 2:3/85mm), uncovered baseline, scene wardrobe (helm/rompi/peci/tongkat) = GATE B.
Authored on the [[prompt-rules-image-generation]] 6-layer pattern + token discipline + banned-list + declared plate deviations (§1). Each block is standalone. Direction protocol ([[00-README]] §3.1): Profile A = `camera-left`; zero Profile B. Label by visible cheek/ear.

---

### F1 — Pak Darto

#### Cell D1 — Front · Full body → `F_darto_front_full.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta lower-middle-class neighborhood warung vendor, warm friendly settled presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary kindly everyday appearance, working-class register, weathered approachable",
    "age": "man 50 years old",
    "facial_features": "mature weathered complexion, soft lined forehead, kind steady eyes, full greying brows, gentle jowl, clean even skin texture",
    "body_features": "stocky settled middle-aged build, slightly rounded, upright relaxed posture"
  },
  "character_style": {
    "makeup": "groomed natural mature skin, even skin tone, matte setting powder zero shine, fine weathered texture preserved",
    "wardrobe": "short-sleeve collared cotton shirt soft muted olive, plain undershirt visible at collar, relaxed cotton trousers desaturated grey",
    "hair": "short greying side-parted hair, uniformly salt-and-pepper even distribution throughout, dry matte hair, chalky matte finish, neatly combed natural",
    "footwear": "simple rubber sandals, worn casual"
  },
  "subject_state": "static",
  "action": "standing still upright for reference, weight even both feet, arms relaxed straight at sides",
  "pose": "neutral standing feet shoulder-width, shoulders squared to camera",
  "gesture": "both arms relaxed straight at sides, hands open natural",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "full body shot, crown to sandal sole visible, floor line visible, generous headroom above crown",
  "angle": "eye-level straight-on, front view, subject squared facing camera, both ears symmetric, nose centered",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell D2 — Front · Medium → `F_darto_front_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta lower-middle-class neighborhood warung vendor, warm friendly settled presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary kindly everyday appearance, working-class register, weathered approachable",
    "age": "man 50 years old",
    "facial_features": "mature weathered complexion, soft lined forehead, kind steady eyes, full greying brows, gentle jowl, clean even skin texture",
    "body_features": "stocky settled middle-aged build, slightly rounded, upright relaxed posture"
  },
  "character_style": {
    "makeup": "groomed natural mature skin, even skin tone, matte setting powder zero shine, fine weathered texture preserved",
    "wardrobe": "short-sleeve collared cotton shirt soft muted olive, plain undershirt visible at collar, relaxed cotton trousers desaturated grey",
    "hair": "short greying side-parted hair, uniformly salt-and-pepper even distribution throughout, dry matte hair, chalky matte finish, neatly combed natural"
  },
  "subject_state": "static",
  "action": "standing still, torso squared to camera, arms relaxed at sides",
  "pose": "upright relaxed, shoulders squared level",
  "gesture": "shoulders relaxed level, arms at sides out of frame",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "MS medium shot, waist up, subject centered",
  "angle": "eye-level straight-on, front view, both ears symmetric, nose centered",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell D3 — Profile A · Medium → `F_darto_profileA_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta lower-middle-class neighborhood warung vendor, warm friendly settled presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary kindly everyday appearance, working-class register, weathered approachable",
    "age": "man 50 years old",
    "facial_features": "mature weathered complexion, soft lined forehead, kind steady eyes, full greying brows, gentle jowl, clean even skin texture",
    "body_features": "stocky settled middle-aged build, slightly rounded, upright relaxed posture"
  },
  "character_style": {
    "makeup": "groomed natural mature skin, even skin tone, matte setting powder zero shine, fine weathered texture preserved",
    "wardrobe": "short-sleeve collared cotton shirt soft muted olive, plain undershirt visible at collar, relaxed cotton trousers desaturated grey",
    "hair": "short greying side-parted hair, uniformly salt-and-pepper even distribution throughout, dry matte hair, chalky matte finish, neatly combed natural"
  },
  "subject_state": "static",
  "action": "standing still in full profile, torso turned ninety degrees, arms relaxed",
  "pose": "upright relaxed, body sideways to camera",
  "gesture": "arms relaxed at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "MS medium shot, waist up, profile",
  "angle": "eye-level, full profile view, subject facing camera-left frame-left audience POV, head rotated ninety degrees sideways, single ear visible, nose in clean silhouette, near cheek toward camera",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

---

### F2 — Tika
*Adult (20, re-aged from 16 — director call 2026-06-21). Lisa adult body-token method applied: `body_features` carries `natural 34C bustline, defined waist and hips` + wardrobe `fitted crew-neck` ([[lessons]]:54). Red-flag words (breasts/busty/large/cup/bra) avoided; catalogue register from scaffold. Escalate 34B if filtered / 34D if under-full; verify silhouette on first plate.*

#### Cell T1 — Front · Medium → `F_tika_front_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta neighborhood young woman, part-time helper, bright willing presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh natural young-adult appearance, lower-middle-class register, approachable",
    "age": "woman 20 years old",
    "facial_features": "fresh clear young-adult complexion, smooth skin texture, bright lively eyes, soft natural brows, soft cheeks, clean even jawline",
    "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 160cm frame, upright relaxed posture"
  },
  "character_style": {
    "makeup": "bare fresh young-adult skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "fitted crew-neck cotton tee soft jersey soft muted dusty-rose, modest contemporary fit",
    "hair": "long uniformly dark hair even tone throughout, simple low tie at nape, soft natural fringe, dry matte hair, chalky matte finish, neatly combed natural"
  },
  "subject_state": "static",
  "action": "standing still, torso squared to camera, arms relaxed at sides",
  "pose": "upright relaxed, shoulders squared level",
  "gesture": "shoulders relaxed level, arms at sides out of frame",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "MS medium shot, waist up, subject centered",
  "angle": "eye-level straight-on, front view, both ears symmetric, nose centered",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell T2 — Profile A · Medium → `F_tika_profileA_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta neighborhood young woman, part-time helper, bright willing presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh natural young-adult appearance, lower-middle-class register, approachable",
    "age": "woman 20 years old",
    "facial_features": "fresh clear young-adult complexion, smooth skin texture, bright lively eyes, soft natural brows, soft cheeks, clean even jawline",
    "body_features": "young womanly build, natural 34C bustline, defined waist and hips, 160cm frame, upright relaxed posture"
  },
  "character_style": {
    "makeup": "bare fresh young-adult skin, clean even complexion, natural skin texture, matte finish zero shine",
    "wardrobe": "fitted crew-neck cotton tee soft jersey soft muted dusty-rose, modest contemporary fit",
    "hair": "long uniformly dark hair even tone throughout, simple low tie at nape, soft natural fringe, dry matte hair, chalky matte finish, neatly combed natural"
  },
  "subject_state": "static",
  "action": "standing still in full profile, torso turned ninety degrees, arms relaxed",
  "pose": "upright relaxed, body sideways to camera",
  "gesture": "arms relaxed at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "MS medium shot, waist up, profile",
  "angle": "eye-level, full profile view, subject facing camera-left frame-left audience POV, head rotated ninety degrees sideways, single ear visible, nose in clean silhouette, near cheek toward camera",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

---

### F3 — petugas bank

#### Cell P1 — Front · Medium → `F_petugasbank_front_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta professional bank officer, composed courteous corporate presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "neat professional appearance, middle-class corporate register, polished approachable",
    "age": "man 32 years old",
    "facial_features": "clear even complexion, smooth groomed skin texture, steady attentive eyes, neat defined brows, clean even jawline",
    "body_features": "trim professional adult build, upright composed posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, natural texture preserved",
    "wardrobe": "crisp collared dress shirt soft muted slate-blue, neat tidy corporate, plain solid",
    "hair": "short neat side-parted dark hair, uniformly dark even tone throughout, dry matte hair, chalky matte finish, cleanly groomed"
  },
  "subject_state": "static",
  "action": "standing still, torso squared to camera, arms relaxed at sides",
  "pose": "upright relaxed, shoulders squared level",
  "gesture": "shoulders relaxed level, arms at sides out of frame",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "MS medium shot, waist up, subject centered",
  "angle": "eye-level straight-on, front view, both ears symmetric, nose centered",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell P2 — Front · Close-up → `F_petugasbank_front_closeup.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta professional bank officer, composed courteous corporate presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "neat professional appearance, middle-class corporate register, polished approachable",
    "age": "man 32 years old",
    "facial_features": "clear even complexion, smooth groomed skin texture, steady attentive eyes, neat defined brows, clean even jawline",
    "body_features": "trim professional adult build, upright composed posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, natural texture preserved",
    "wardrobe": "crisp collared dress shirt soft muted slate-blue collar visible at neckline, plain solid",
    "hair": "short neat side-parted dark hair, uniformly dark even tone throughout, dry matte hair, chalky matte finish, cleanly groomed"
  },
  "subject_state": "static",
  "action": "head and shoulders still, facing lens",
  "pose": "head level, shoulders squared",
  "gesture": "shoulders relaxed level",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens, both eyes open even",
  "framing": "CU close-up, face fills frame, head and top of shoulders",
  "angle": "eye-level straight-on, front view, both eyes visible symmetric, nose centered",
  "camera": "100mm portrait prime spherical, soft background separation",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "4:5",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell P3 — Profile A · Medium → `F_petugasbank_profileA_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta professional bank officer, composed courteous corporate presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "neat professional appearance, middle-class corporate register, polished approachable",
    "age": "man 32 years old",
    "facial_features": "clear even complexion, smooth groomed skin texture, steady attentive eyes, neat defined brows, clean even jawline",
    "body_features": "trim professional adult build, upright composed posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, natural texture preserved",
    "wardrobe": "crisp collared dress shirt soft muted slate-blue, neat tidy corporate, plain solid",
    "hair": "short neat side-parted dark hair, uniformly dark even tone throughout, dry matte hair, chalky matte finish, cleanly groomed"
  },
  "subject_state": "static",
  "action": "standing still in full profile, torso turned ninety degrees, arms relaxed",
  "pose": "upright relaxed, body sideways to camera",
  "gesture": "arms relaxed at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "MS medium shot, waist up, profile",
  "angle": "eye-level, full profile view, subject facing camera-left frame-left audience POV, head rotated ninety degrees sideways, single ear visible, nose in clean silhouette, near cheek toward camera",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

---

### F4 — Rian

#### Cell R1 — Front · Medium → `F_rian_front_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta young office worker, curious eager junior-professional presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh tidy young-adult appearance, middle-class office register, approachable",
    "age": "man 25 years old",
    "facial_features": "distinctive-commoner-features, rounded fuller face shape, soft full cheeks, broad soft jawline, thick full dark brows, deep-set warm almond eyes, light youthful mustache with thin chin stubble, a small mole on the cheek, clear youthful complexion, smooth skin texture",
    "body_features": "stocky compact young-adult build, slightly broad shoulders, upright relaxed posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, even skin tone, matte setting powder zero shine, youthful texture preserved",
    "wardrobe": "soft collared casual shirt muted charcoal, relaxed office-smart, plain solid",
    "hair": "wavy tousled dark hair medium length, soft natural curl texture, uniformly dark even tone throughout, dry matte hair, chalky matte finish"
  },
  "subject_state": "static",
  "action": "standing still, torso squared to camera, arms relaxed at sides",
  "pose": "upright relaxed, shoulders squared level",
  "gesture": "shoulders relaxed level, arms at sides out of frame",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "MS medium shot, waist up, subject centered",
  "angle": "eye-level straight-on, front view, both ears symmetric, nose centered",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell R2 — Front · Close-up → `F_rian_front_closeup.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta young office worker, curious eager junior-professional presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh tidy young-adult appearance, middle-class office register, approachable",
    "age": "man 25 years old",
    "facial_features": "distinctive-commoner-features, rounded fuller face shape, soft full cheeks, broad soft jawline, thick full dark brows, deep-set warm almond eyes, light youthful mustache with thin chin stubble, a small mole on the cheek, clear youthful complexion, smooth skin texture",
    "body_features": "stocky compact young-adult build, slightly broad shoulders, upright relaxed posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, even skin tone, matte setting powder zero shine, youthful texture preserved",
    "wardrobe": "soft collared casual shirt muted charcoal collar visible at neckline, plain solid",
    "hair": "wavy tousled dark hair medium length, soft natural curl texture, uniformly dark even tone throughout, dry matte hair, chalky matte finish"
  },
  "subject_state": "static",
  "action": "head and shoulders still, facing lens",
  "pose": "head level, shoulders squared",
  "gesture": "shoulders relaxed level",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens, both eyes open even",
  "framing": "CU close-up, face fills frame, head and top of shoulders",
  "angle": "eye-level straight-on, front view, both eyes visible symmetric, nose centered",
  "camera": "100mm portrait prime spherical, soft background separation",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "4:5",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell R3 — Profile A · Medium → `F_rian_profileA_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta young office worker, curious eager junior-professional presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh tidy young-adult appearance, middle-class office register, approachable",
    "age": "man 25 years old",
    "facial_features": "distinctive-commoner-features, rounded fuller face shape, soft full cheeks, broad soft jawline, thick full dark brows, deep-set warm almond eyes, light youthful mustache with thin chin stubble, a small mole on the cheek, clear youthful complexion, smooth skin texture",
    "body_features": "stocky compact young-adult build, slightly broad shoulders, upright relaxed posture"
  },
  "character_style": {
    "makeup": "BB cream sheer coverage, even skin tone, matte setting powder zero shine, youthful texture preserved",
    "wardrobe": "soft collared casual shirt muted charcoal, relaxed office-smart, plain solid",
    "hair": "wavy tousled dark hair medium length, soft natural curl texture, uniformly dark even tone throughout, dry matte hair, chalky matte finish"
  },
  "subject_state": "static",
  "action": "standing still in full profile, torso turned ninety degrees, arms relaxed",
  "pose": "upright relaxed, body sideways to camera",
  "gesture": "arms relaxed at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "MS medium shot, waist up, profile",
  "angle": "eye-level, full profile view, subject facing camera-left frame-left audience POV, head rotated ninety degrees sideways, single ear visible, nose in clean silhouette, near cheek toward camera",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

---

### F5 — pembina muda

#### Cell M1 — Front · Full body → `F_pembina_front_full.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta young after-school club mentor, warm encouraging youthful-teacher presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh warm young-adult appearance, middle-class register, friendly approachable",
    "age": "woman 23 years old",
    "facial_features": "distinctive-commoner-features, round full face shape, high soft cheekbones, fuller lips, slightly broad nose, thick full natural brows, warm round expressive eyes, a small beauty mark near the lip, soft dimpled cheeks, fresh clear complexion",
    "body_features": "curvy womanly build, 40D bustline Hemispherical type, full rounded hips, soft rounded waist, 158cm frame, upright relaxed posture",
  "character_style": {
    "makeup": "light natural foundation even coverage, soft groomed brows, nude soft-matte lip, baked setting powder matte finish zero shine, fresh skin texture preserved",
    "wardrobe": "simple short-sleeve soft blouse muted teal, modest contemporary cut, relaxed casual trousers desaturated grey",
    "hair": "short dark hair, soft natural wave, loose chin-length bob, uniformly dark even tone throughout, dry matte hair, chalky matte finish",
    "footwear": "clean flat canvas shoes, plain"
  },
  "subject_state": "static",
  "action": "standing still upright for reference, weight even both feet, arms relaxed straight at sides",
  "pose": "neutral standing feet shoulder-width, shoulders squared to camera",
  "gesture": "both arms relaxed straight at sides, hands open natural",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "full body shot, crown to shoe sole visible, floor line visible, generous headroom above crown",
  "angle": "eye-level straight-on, front view, subject squared facing camera, both ears symmetric, nose centered",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell M2 — Front · Medium → `F_pembina_front_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta young after-school club mentor, warm encouraging youthful-teacher presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh warm young-adult appearance, middle-class register, friendly approachable",
    "age": "woman 23 years old",
    "facial_features": "distinctive-commoner-features, round full face shape, high soft cheekbones, fuller lips, slightly broad nose, thick full natural brows, warm round expressive eyes, a small beauty mark near the lip, soft dimpled cheeks, fresh clear complexion",
    "body_features": "curvy womanly build, 40D bustline Hemispherical type, full rounded hips, soft rounded waist, 158cm frame, upright relaxed posture",
  "character_style": {
    "makeup": "light natural foundation even coverage, soft groomed brows, nude soft-matte lip, baked setting powder matte finish zero shine, fresh skin texture preserved",
    "wardrobe": "simple short-sleeve soft blouse muted teal, modest contemporary cut, relaxed casual trousers desaturated grey",
    "hair": "short dark hair, soft natural wave, loose chin-length bob, uniformly dark even tone throughout, dry matte hair, chalky matte finish"
  },
  "subject_state": "static",
  "action": "standing still, torso squared to camera, arms relaxed at sides",
  "pose": "upright relaxed, shoulders squared level",
  "gesture": "shoulders relaxed level, arms at sides out of frame",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "MS medium shot, waist up, subject centered",
  "angle": "eye-level straight-on, front view, both ears symmetric, nose centered",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell M3 — Profile A · Medium → `F_pembina_profileA_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta young after-school club mentor, warm encouraging youthful-teacher presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh warm young-adult appearance, middle-class register, friendly approachable",
    "age": "woman 23 years old",
    "facial_features": "distinctive-commoner-features, round full face shape, high soft cheekbones, fuller lips, slightly broad nose, thick full natural brows, warm round expressive eyes, a small beauty mark near the lip, soft dimpled cheeks, fresh clear complexion",
    "body_features": "curvy womanly build, 40D bustline Hemispherical type, full rounded hips, soft rounded waist, 158cm frame, upright relaxed posture"
  },
  "character_style": {
    "makeup": "light natural foundation even coverage, soft groomed brows, nude soft-matte lip, baked setting powder matte finish zero shine, fresh skin texture preserved",
    "wardrobe": "simple short-sleeve soft blouse muted teal, modest contemporary cut, relaxed casual trousers desaturated grey",
    "hair": "short dark hair, soft natural wave, loose chin-length bob, uniformly dark even tone throughout, dry matte hair, chalky matte finish"
  },
  "subject_state": "static",
  "action": "standing still in full profile, torso turned ninety degrees, arms relaxed",
  "pose": "upright relaxed, body sideways to camera",
  "gesture": "arms relaxed at sides",
  "expression": "neutral relaxed face, calm gaze forward to horizon, lips closed soft",
  "framing": "MS medium shot, waist up, profile",
  "angle": "eye-level, full profile view, subject facing camera-left frame-left audience POV, head rotated ninety degrees sideways, single ear visible, nose in clean silhouette, near cheek toward camera",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

---

### F6 — Ojek (app motorcycle-taxi driver, man 30) · ✅ prompt LOCKED · generate PENDING (sesi baru)
Plate baseline UNCOVERED. Scene wardrobe (windbreaker jacket + open-face helmet, on a motorcycle) = GATE B. `front_full` (SC03-SH05 WIDE) + `front_medium` (coverage).

#### Cell O1 — Front · Full body → `F_ojek_front_full.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta app motorcycle-taxi driver, working-class, steady patient service presence",
    "ethnicity": "modern Jakartan features, Javanese Sundanese urban descent",
    "beauty": "plain working-class everyman appearance, weathered friendly",
    "age": "man 30 years old",
    "facial_features": "distinctive-commoner-features, lean angular face shape, short flat nose, light stubble shadow, thick straight brows, calm friendly almond eyes, sun-touched complexion, a small mole on the cheek",
    "body_features": "lean wiry working-class build, 168cm frame, upright ready posture"
  },
  "character_style": {
    "makeup": "bare healthy male skin, matte finish zero shine, real-person texture preserved",
    "wardrobe": "short-sleeve plain crew-neck tee desaturated grey, relaxed cotton trousers muted charcoal",
    "hair": "short dark hair, low neat crop, uniformly dark even tone, dry matte hair, chalky matte finish",
    "footwear": "casual low sneakers, plain muted"
  },
  "subject_state": "static",
  "action": "standing still upright for reference, weight even both feet, arms relaxed straight at sides",
  "pose": "neutral standing feet shoulder-width, shoulders squared to camera",
  "gesture": "both arms relaxed straight at sides, hands open natural",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "full body shot, crown to sneaker sole visible, floor line visible, generous headroom above crown",
  "angle": "eye-level straight-on, front view, subject squared facing camera, both ears symmetric, nose centered",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell O2 — Front · Medium → `F_ojek_front_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta app motorcycle-taxi driver, working-class, steady patient service presence",
    "ethnicity": "modern Jakartan features, Javanese Sundanese urban descent",
    "beauty": "plain working-class everyman appearance, weathered friendly",
    "age": "man 30 years old",
    "facial_features": "distinctive-commoner-features, lean angular face shape, short flat nose, light stubble shadow, thick straight brows, calm friendly almond eyes, sun-touched complexion, a small mole on the cheek",
    "body_features": "lean wiry working-class build, 168cm frame, upright ready posture"
  },
  "character_style": {
    "makeup": "bare healthy male skin, matte finish zero shine, real-person texture preserved",
    "wardrobe": "short-sleeve plain crew-neck tee desaturated grey",
    "hair": "short dark hair, low neat crop, uniformly dark even tone, dry matte hair, chalky matte finish"
  },
  "subject_state": "static",
  "action": "standing still, torso squared to camera, arms relaxed at sides",
  "pose": "upright relaxed, shoulders squared level",
  "gesture": "shoulders relaxed level, arms at sides out of frame",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "MS medium shot, waist up, subject centered",
  "angle": "eye-level straight-on, front view, both ears symmetric, nose centered",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

---

### F7 — Kurir (last-mile courier, man 28) · ✅ prompt LOCKED · generate PENDING (sesi baru)
Plate baseline UNCOVERED. Scene wardrobe (courier vest/polo + cap, handling boxes) = GATE B. Kurir-2 = secondary soft on the same plate. `front_full` (SC04 WIDE/payoff) + `front_medium` (MS loading boxes).

#### Cell K1 — Front · Full body → `F_kurir_front_full.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta last-mile delivery courier, working-class, brisk efficient service presence",
    "ethnicity": "modern Jakartan features, Javanese Sundanese urban descent",
    "beauty": "plain working-class everyman appearance, fit practical",
    "age": "man 28 years old",
    "facial_features": "distinctive-commoner-features, square jaw face shape, straight nose, light stubble, thick brows, alert friendly eyes, sun-touched complexion, a small scar on the brow",
    "body_features": "fit sturdy working-class build, broad shoulders, 170cm frame, upright active posture"
  },
  "character_style": {
    "makeup": "bare healthy male skin, matte finish zero shine, real-person texture preserved",
    "wardrobe": "short-sleeve plain crew-neck tee desaturated steel-blue, relaxed work trousers muted charcoal",
    "hair": "short dark hair, low practical crop, uniformly dark even tone, dry matte hair, chalky matte finish",
    "footwear": "sturdy low work shoes, plain muted"
  },
  "subject_state": "static",
  "action": "standing still upright for reference, weight even both feet, arms relaxed straight at sides",
  "pose": "neutral standing feet shoulder-width, shoulders squared to camera",
  "gesture": "both arms relaxed straight at sides, hands open natural",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "full body shot, crown to shoe sole visible, floor line visible, generous headroom above crown",
  "angle": "eye-level straight-on, front view, subject squared facing camera, both ears symmetric, nose centered",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell K2 — Front · Medium → `F_kurir_front_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta last-mile delivery courier, working-class, brisk efficient service presence",
    "ethnicity": "modern Jakartan features, Javanese Sundanese urban descent",
    "beauty": "plain working-class everyman appearance, fit practical",
    "age": "man 28 years old",
    "facial_features": "distinctive-commoner-features, square jaw face shape, straight nose, light stubble, thick brows, alert friendly eyes, sun-touched complexion, a small scar on the brow",
    "body_features": "fit sturdy working-class build, broad shoulders, 170cm frame, upright active posture"
  },
  "character_style": {
    "makeup": "bare healthy male skin, matte finish zero shine, real-person texture preserved",
    "wardrobe": "short-sleeve plain crew-neck tee desaturated steel-blue",
    "hair": "short dark hair, low practical crop, uniformly dark even tone, dry matte hair, chalky matte finish"
  },
  "subject_state": "static",
  "action": "standing still, torso squared to camera, arms relaxed at sides",
  "pose": "upright relaxed, shoulders squared level",
  "gesture": "shoulders relaxed level, arms at sides out of frame",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "MS medium shot, waist up, subject centered",
  "angle": "eye-level straight-on, front view, both ears symmetric, nose centered",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

---

### F8 — Peer-mentor (senior student, woman 22) · ✅ prompt LOCKED · generate PENDING (sesi baru)
Plate baseline UNCOVERED, faith NOT imposed (no head-covering token). `front_full` (SC07 WIDE + seated 2-shot) + `front_medium` (tight 2-shot).

#### Cell N1 — Front · Full body → `F_mentor_front_full.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta senior university student, peer mentor, warm approachable confident presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh young-adult appearance, friendly mature-student register",
    "age": "woman 22 years old",
    "facial_features": "distinctive-commoner-features, oval face shape, defined cheekbones, warm wide smile, medium-thick natural brows, bright attentive eyes, clear complexion, a small beauty mark near the jaw",
    "body_features": "slim-average young-adult build, natural 34B bustline, 165cm frame, relaxed confident posture"
  },
  "character_style": {
    "makeup": "light natural foundation even coverage, soft groomed brows, soft rose tinted lip, baked setting powder matte finish zero shine, fresh skin texture preserved",
    "wardrobe": "modest contemporary campus-casual, relaxed soft button cardigan muted mustard over plain crew-neck tee, comfortable straight trousers desaturated navy",
    "hair": "medium-length dark hair, soft natural wave, half-tied, uniformly dark even tone, dry matte hair, chalky matte finish",
    "footwear": "clean flat loafers, plain muted"
  },
  "subject_state": "static",
  "action": "standing still upright for reference, weight even both feet, arms relaxed straight at sides",
  "pose": "neutral standing feet shoulder-width, shoulders squared to camera",
  "gesture": "both arms relaxed straight at sides, hands open natural",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "full body shot, crown to loafer sole visible, floor line visible, generous headroom above crown",
  "angle": "eye-level straight-on, front view, subject squared facing camera, both ears symmetric, nose centered",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell N2 — Front · Medium → `F_mentor_front_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta senior university student, peer mentor, warm approachable confident presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "fresh young-adult appearance, friendly mature-student register",
    "age": "woman 22 years old",
    "facial_features": "distinctive-commoner-features, oval face shape, defined cheekbones, warm wide smile, medium-thick natural brows, bright attentive eyes, clear complexion, a small beauty mark near the jaw",
    "body_features": "slim-average young-adult build, natural 34B bustline, 165cm frame, relaxed confident posture"
  },
  "character_style": {
    "makeup": "light natural foundation even coverage, soft groomed brows, soft rose tinted lip, baked setting powder matte finish zero shine, fresh skin texture preserved",
    "wardrobe": "modest contemporary campus-casual, relaxed soft button cardigan muted mustard over plain crew-neck tee",
    "hair": "medium-length dark hair, soft natural wave, half-tied, uniformly dark even tone, dry matte hair, chalky matte finish"
  },
  "subject_state": "static",
  "action": "standing still, torso squared to camera, arms relaxed at sides",
  "pose": "upright relaxed, shoulders squared level",
  "gesture": "shoulders relaxed level, arms at sides out of frame",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "MS medium shot, waist up, subject centered",
  "angle": "eye-level straight-on, front view, both ears symmetric, nose centered",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

---

### F9 — Ibu petugas kebersihan (campus cleaner, woman 55) · ✅ prompt LOCKED · generate PENDING (sesi baru)
Plate baseline UNCOVERED, faith NOT imposed. Scene wardrobe (cleaning-staff vest/apron) = GATE B. Render-age: real middle-age ~55 (NOT de-aged — verify age lines on the first plate). `front_full` (SC09 MWS + 2-shot) + `front_medium` (2-shot + hand detail).

#### Cell I1 — Front · Full body → `F_ibupetugas_front_full.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta middle-aged campus cleaning staff woman, weathered hardworking gentle presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "humble working-class middle-aged appearance, kind tired warmth",
    "age": "woman 55 years old",
    "facial_features": "distinctive-commoner-features, round softened face shape, fine age lines around the eyes, fine age lines around the mouth, slightly hollow cheeks, broad gentle nose, thinning natural brows, warm tired eyes, sun-aged complexion, a few age spots",
    "body_features": "stout sturdy middle-aged build, slightly stooped tired posture, 156cm frame"
  },
  "character_style": {
    "makeup": "bare weathered mature skin, fine wrinkles preserved, matte finish zero shine, real-person texture",
    "wardrobe": "plain modest short-sleeve blouse desaturated grey-green, relaxed dark trousers",
    "hair": "greying dark hair, low neat bun, uniformly salt-and-pepper even distribution, dry matte hair, chalky matte finish",
    "footwear": "simple worn flat shoes, plain"
  },
  "subject_state": "static",
  "action": "standing still upright for reference, weight even both feet, arms relaxed straight at sides",
  "pose": "neutral standing feet shoulder-width, shoulders squared to camera",
  "gesture": "both arms relaxed straight at sides, hands open natural",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "full body shot, crown to shoe sole visible, floor line visible, generous headroom above crown",
  "angle": "eye-level straight-on, front view, subject squared facing camera, both ears symmetric, nose centered",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell I2 — Front · Medium → `F_ibupetugas_front_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "Jakarta middle-aged campus cleaning staff woman, weathered hardworking gentle presence",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "humble working-class middle-aged appearance, kind tired warmth",
    "age": "woman 55 years old",
    "facial_features": "distinctive-commoner-features, round softened face shape, fine age lines around the eyes, fine age lines around the mouth, slightly hollow cheeks, broad gentle nose, thinning natural brows, warm tired eyes, sun-aged complexion, a few age spots",
    "body_features": "stout sturdy middle-aged build, slightly stooped tired posture, 156cm frame"
  },
  "character_style": {
    "makeup": "bare weathered mature skin, fine wrinkles preserved, matte finish zero shine, real-person texture",
    "wardrobe": "plain modest short-sleeve blouse desaturated grey-green",
    "hair": "greying dark hair, low neat bun, uniformly salt-and-pepper even distribution, dry matte hair, chalky matte finish"
  },
  "subject_state": "static",
  "action": "standing still, torso squared to camera, arms relaxed at sides",
  "pose": "upright relaxed, shoulders squared level",
  "gesture": "shoulders relaxed level, arms at sides out of frame",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "MS medium shot, waist up, subject centered",
  "angle": "eye-level straight-on, front view, both ears symmetric, nose centered",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

---

### F10 — Bapak desa lanjut usia (village elder, man 62) · ✅ prompt LOCKED · generate PENDING (sesi baru)
Plate baseline UNCOVERED (face locked). Scene wardrobe (black peci/kopiah cap + wooden cane/tongkat) = GATE B. Render-age: real elderly ~62 (NOT de-aged — verify deep age lines on the first plate). `front_full` (SC12 WIDE + 2-shot) + `front_medium` (MS + 2-shot).

#### Cell B1 — Front · Full body → `F_bapakdesa_front_full.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "rural Javanese elder man visiting the city, humble devout gentle village presence",
    "ethnicity": "modern Javanese village features, Javanese rural descent",
    "beauty": "weathered humble elderly appearance, kind dignified",
    "age": "man 62 years old",
    "facial_features": "distinctive-commoner-features, lean weathered face shape, deep age lines across the forehead, deep lines around the eyes, sunken cheeks, prominent cheekbones, broad flat nose, thin greying brows, kind tired eyes, dark sun-aged complexion, sparse short grey moustache, a few age spots",
    "body_features": "slight frail thin elderly build, 162cm frame, gently stooped forward posture"
  },
  "character_style": {
    "makeup": "bare weathered aged male skin, deep wrinkles preserved, matte finish zero shine, real-person texture",
    "wardrobe": "plain modest long-sleeve plain button shirt desaturated brown, loose dark trousers",
    "hair": "short thinning grey hair, uniformly grey even distribution, dry matte hair, chalky matte finish",
    "footwear": "simple worn sandals, plain"
  },
  "subject_state": "static",
  "action": "standing still upright for reference, weight even both feet, arms relaxed straight at sides",
  "pose": "neutral standing feet shoulder-width, shoulders squared to camera",
  "gesture": "both arms relaxed straight at sides, hands open natural",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "full body shot, crown to sandal sole visible, floor line visible, generous headroom above crown",
  "angle": "eye-level straight-on, front view, subject squared facing camera, both ears symmetric, nose centered",
  "camera": "50mm prime spherical, deep focus front to back",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "9:16",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

#### Cell B2 — Front · Medium → `F_bapakdesa_front_medium.png`
```json
{
  "mood": "neutral reference clarity, calm relaxed presence, Peter Hurley studio headshot register",
  "color_grade": "neutral true-to-life color, balanced white-point, accurate natural skin tone, faithful natural color rendering",
  "style": "photorealistic studio reference plate, professional photostock isolated-on-white portrait, commercial stock photography clarity, clean catalogue look, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra natural rendering",
  "scene": "plain solid white background, flat even white fill, subject fully isolated on clean white",
  "location": "indoor",
  "time_of_day": "studio controlled",
  "atmosphere": "clinical empty stillness",
  "character_identity": {
    "role": "rural Javanese elder man visiting the city, humble devout gentle village presence",
    "ethnicity": "modern Javanese village features, Javanese rural descent",
    "beauty": "weathered humble elderly appearance, kind dignified",
    "age": "man 62 years old",
    "facial_features": "distinctive-commoner-features, lean weathered face shape, deep age lines across the forehead, deep lines around the eyes, sunken cheeks, prominent cheekbones, broad flat nose, thin greying brows, kind tired eyes, dark sun-aged complexion, sparse short grey moustache, a few age spots",
    "body_features": "slight frail thin elderly build, 162cm frame, gently stooped forward posture"
  },
  "character_style": {
    "makeup": "bare weathered aged male skin, deep wrinkles preserved, matte finish zero shine, real-person texture",
    "wardrobe": "plain modest long-sleeve plain button shirt desaturated brown",
    "hair": "short thinning grey hair, uniformly grey even distribution, dry matte hair, chalky matte finish"
  },
  "subject_state": "static",
  "action": "standing still, torso squared to camera, arms relaxed at sides",
  "pose": "upright relaxed, shoulders squared level",
  "gesture": "shoulders relaxed level, arms at sides out of frame",
  "expression": "neutral relaxed face, lips closed soft, calm direct gaze to lens",
  "framing": "MS medium shot, waist up, subject centered",
  "angle": "eye-level straight-on, front view, both ears symmetric, nose centered",
  "camera": "85mm prime spherical, medium depth of field",
  "lighting": "flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit",
  "aspect_ratio": "2:3",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic casual wear, fabric worn laundered, class-accurate daily register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "natural photorealistic skin, portrait-level detail, character-appropriate finish, matte zero shine",
  "hair_stylist": "Anissa Salazar", "hair_style": "naturalistic everyday Asian-family hair, real-texture, unstyled lived-in matte finish"
}
```

---

## 4. Generation + naming
Per [[00-README]] §4: `character-images/F_<name>/` per figuran (`F_darto`, `F_tika`, `F_petugasbank`, `F_rian`, `F_pembina`, `F_ojek`, `F_kurir`, `F_mentor`, `F_ibupetugas`, `F_bapakdesa`), each with a `_rejected/` subfolder. Filenames `F_<name>_<view>_<shot>.png` (the §3 cell headers state each target name). Generate ONLY the cells listed per figuran; Profile A via the standard direction protocol; zero Profile B. Verify each render by visible cheek/ear before approval; same rubric as main characters (aspect / view-direction / identity / wardrobe / hair / background-matte).

---

*Figurans sheet v0.4 (10 named single-scene figurans, 24 full 6-layer JSON prompts inlined verbatim per [[prompt-rules-image-generation]]:44 + [[lessons]]:224; adaptive lighter plate set, uncovered baseline, zero Profile B, faith not imposed; Tika re-aged 16→20 adult + Lisa 34C body-token applied [[lessons]]:54; covered-head wear + helm/rompi/peci/tongkat deferred to GATE B; F6–F10 prompts authored Fase-2 2026-07-01, generate PENDING new session, F9 ~55 / F10 ~62 verify-aged-not-deaged on first plate) · Explainer Video 2 · 2026-06-21 / 2026-07-01 · cites [[07-style-reference]] · method [[00-README]]*
