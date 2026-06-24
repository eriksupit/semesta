---
title: GATE B Keyframes — SEQ1-SC02 (INT. RUANG KELUARGA, 04.43 · sholat subuh)
tags: [explainer-video-2, gate-b, keyframe, seq1-sc02]
status: active
created: 2026-06-24
updated: 2026-06-24
aliases: [ev2-gateB-seq1-sc02]
---

# GATE B Keyframes — SEQ1-SC02

> Scene truth → [[03-scene-detail]] (SEQ1-SC02). Identity lock → [[08-character-sheet/R-ratna]] · [[08-character-sheet/H-herman]] · [[08-character-sheet/L-lisa]] · [[08-character-sheet/A-andi]]. Room lock → [[09-environment-sheet/E02-ruangkeluarga]]. Standar 6-lapis + grade hangat + ADDENDUM A1 → [[00-WORKLOG]] · [[prompt-rules-image-generation]]. Format template → [[10-gateB-keyframes/SEQ1-SC01]].

> **🔒 TRIAD ATTACHMENT MANDATORY (Erik mandate 2026-06-23):** SETIAP frame (START & END) WAJIB melampirkan + menyebut di prompt KETIGA kategori: **(1) KARAKTER** (plat wajah/figur tiap orang dalam frame), **(2) LINGKUNGAN** (plat env E02), **(3) START/END-REFERENCE** (render anchor). Render anchor saja TIDAK cukup untuk objek yang diberi aksi (sajadah, saklar, monitor) → tanpa plat lingkungan model halusinasi permukaan/objek. Tak ada pengecualian.

> **STRUKTUR 3-SHOT (revisi 2026-06-24, Erik):** SH03 (takbir→ruku) disederhanakan jadi **berdiri bersedekap (qiyam) ditahan, START→END beda angle saja** — gerak pose multi-karakter sinkron (ruku/sujud 4 orang) risiko-tinggi i2v warp. **SH04 (sujud) DIHAPUS.** END SH03 = push-in di sumbu reverse yang sama (high-angle `prayer_high` dibatalkan). **Reblock 2026-06-24:** seluruh sholat (SH02+SH03) pindah ke plate `E02_ruangkeluarga_reverse_prayer.png`, sholat menghadap jendela/kamera (qibla=jendela), plate karakter `front`. SC02 = **3 shot / 6 keyframe**. Konsekuensi hilir: `03-scene-detail.md` hapus SH04 + shot-count film 57→56 (sync terpisah).

## Aturan keras yang dibawa
1. **Grade hangat LOCKED:** `Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones`. Hangat HANYA dari `color_grade`; garmen desaturated; negasi 0; tanpa nama organisasi.
2. **Cahaya scene:** subuh 04.43, jendela GELAP (pra-fajar). SH01-START ruang gelap (hanya rona biru tipis dari jendela). SH01-END dan seterusnya **lampu plafon ON → praktis interior HANGAT** mengisi ruang. Subuh-biru hanya di luar jendela; interior warm-practical.
3. **ADDENDUM A1 — NOL grafis di frame AI.** SH01 = satu-satunya beat layar: monitor "bangun" dirender sebagai **panel netral menyala blank** (browser pesanan + kartu iklan kemasan ditempel di After Effects). **SH02 → SH03 = Bersih Saat Sakral: NOL grafis, layar mati/redup di latar.**
4. **Tiap keyframe = SATU prompt utuh-mandiri** membawa SENDIRI `environment_reference` + `identity_reference` per orang. START & END identik kecuali Lapis-4. END anchor ke render START (`composition_reference`), minimal-change.
5. **Orientasi = plat yang cocok SAJA.** Tak ada plat 3/4; figur menoleh/profil → lampirkan plat profil SAJA (front mendominasi). Arah hadap cocok sisi qibla; tangan/objek camera-LEFT/RIGHT; nol token kabur (`near`/`beside`).
6. **Blocking sholat (semua shot SH02+):** **qibla = dinding camera-LEFT** (dinding sofa + Red Fuji). Herman imam berdiri sendiri di depan (camera-LEFT), menghadap camera-LEFT. Tiga makmum satu saf bahu-membahu di belakangnya (camera-RIGHT dari imam): urut Andi · Ratna · Lisa, semua menghadap camera-LEFT. Kamera menembak dari depan-ruang off-axis → keluarga terbaca PROFIL menghadap camera-left, kedalaman saf imam-depan/makmum-belakang jelas. Desk + monitor di dinding belakang = latar dalam.

## Reference-lock per shot
| Shot | Env plate | Character plate(s) |
|---|---|---|
| SH01 WS desktop | `E02_ruangkeluarga_screen.png` + `E02_ruangkeluarga_master.png` | Ratna `R_ratna_profileA_medium.png` (**UNCOVERED** + **PROFIL hadap camera-left ke dinding saklar**, tidak ke lensa — WS observasional; pra-sholat mahram-only per R-ratna §0; home wear via wardrobe) |
| SH02 MS sajadah→saf | `E02_ruangkeluarga_reverse_prayer.png` | **START (berkumpul mengobrol):** Herman `H_herman_front_full.png` (imam, hadap kamera); Ratna `R_ratna_hijab_profileA_medium.png` (hadap camera-LEFT, di camera-right); Lisa `L_lisa_profileB_full.png` (hadap camera-RIGHT, di camera-left); Andi `A_andi_profileB_full.png` (hadap camera-RIGHT ke Ratna). **END (saf terbentuk):** keempat plat `front` (Herman/Lisa/Andi `front_full`, Ratna `hijab_front_medium`), menghadap kamera |
| SH03 WS qiyam bersedekap | START & END `E02_ruangkeluarga_reverse_prayer.png` (END push-in lebih rapat, sumbu sama) | keempat: Herman `H_herman_front_full.png`; Ratna `R_ratna_hijab_front_medium.png`; Lisa `L_lisa_front_full.png`; Andi `A_andi_front_full.png` (menghadap kamera) |

> **Catatan plat profil:** semua figur menghadap camera-LEFT → lampirkan plat **profileA** (konvensi A = hadap camera-left), buang front untuk figur profil. Ratna pakai plat **hijab** (kepala tertutup; mukena dirender oleh token wardrobe). Lisa & Andi tak punya plat tertutup → wajah dari plat profileA, penutup (mukena Lisa / peci Andi) dirender oleh token wardrobe (prinsip sama Ratna: token garmen penutup hadir → look tertutup dari wardrobe, bukan role).

## Wardrobe lock (SEQ1-SC02 — dari [[08-character-sheet]] §4)
- **Herman (imam):** `long-sleeve plain koko shirt stand-collar muted off-white, solid plain-weave sarong dark muted colorway wrapped waist, black velvet peci cap`, barefoot. *(payoff: sarung yang diiklankan SC01 kini dipakai imam)*
- **Ratna — SH01 (pra-sholat, UNCOVERED):** `comfortable home tunic relaxed modest muted, modest trousers charcoal`, hair `low bun, hairline visible`, flat house slippers. *(mahram-only, tak ada siaran → terbuka per R-ratna §0; mukena baru dipakai dari SH02 = "sakral SH02+")*
- **Ratna — SH02–SH03 (makmum, sholat):** `two-piece white mukena prayer set, opaque cotton, full head-and-body cover, plain matte weave`, barefoot. *(ganti baju terjadi di CUT SH01→SH02)*
- **Lisa (makmum):** `two-piece white mukena prayer set, opaque cotton, full head-and-body cover, plain matte weave`, barefoot.
- **Andi (makmum, anak):** `long-sleeve plain child koko shirt stand-collar muted off-white, child solid plain-weave sarong dark muted wrapped waist, small black velvet peci cap`, barefoot.

---

## SEQ1-SC02-SH01 — WS Ratna di desktop (beat iklan) · segmen 5 dtk
**Attach tiap frame:** `E02_ruangkeluarga_screen.png` + `E02_ruangkeluarga_master.png` (LINGKUNGAN ruang+desk+monitor) + `R_ratna_profileA_medium.png` (KARAKTER — **UNCOVERED**, PROFIL hadap camera-left ke dinding saklar, tidak ke lensa). START = ruang gelap, Ratna di saklar dinding. END = anchor ke render START + lampu ON + **monitor tetap MATI/gelap**, Ratna kepala menoleh ke monitor, ekspresi tenang (TANPA senyum — sendirian, tak ada pesanan terlihat di render). **A1: monitor MATI di render AI; browser pesanan + kartu iklan kemasan di-composite penuh di After Effects ke layar gelap (screen-replacement tak butuh layar nyala — layar nyala = anomali). Beat-iklan SH01 utuh, sepenuhnya di post.**

### SH01-START (prompt utuh — ruang gelap, Ratna meraih saklar)
```json
{
  "mood": "quiet pre-dawn domestic stillness, the household waking before fajr, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "shared living room of an urban middle-class family, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, open ceramic-tiled floor kept clear, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn darkness before sunrise",
  "atmosphere": "quiet lived-in domestic calm, dim near-dark stillness before fajr",
  "environment_reference": "attached reference plates E02_ruangkeluarga_screen.png and E02_ruangkeluarga_master.png, same living room, the MICKE desk, generic unbranded all-in-one desktop on the far back wall beside the curtained window, the light switch plate beside the open doorway, identical furniture, identical layout, single Hokusai Red Fuji print on the camera-left wall, faithful room match",
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_profileA_medium.png, same identical face, same identity, hair visible uncovered, faithful profile match, Ratna seen in profile with her face toward camera-left toward the switch wall",
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, fine natural texture preserved, matte finish zero shine",
    "wardrobe": "comfortable home tunic relaxed modest muted, modest trousers charcoal",
    "hair": "dark hair worn in a low bun, hairline visible uncovered, dry matte hair, chalky matte finish",
    "footwear": "flat house slippers"
  },
  "subject_state": "dynamic",
  "action": "Ratna standing at the camera-left wall by the open doorway, her camera-left hand raised to the light switch plate, fingertips on the switch about to press it, the room still dark around her",
  "pose": "standing in profile facing camera-left toward the switch wall, turned away from the lens, head lowered with chin tucked down, looking down at a small light switch plate on the camera-left wall, her camera-left hand pressing the switch, fingertips on the switch plate, the dark desk, the sleeping desktop on the far back wall toward camera-right, the open prayer floor toward camera-right",
  "expression": "eyes lowered to the light switch under her fingertips, calm awake settled, mouth relaxed, early-morning quiet",
  "framing": "WS of the living room in near-darkness, Ratna small at the switch wall, the light switch plate visible under her hand on the camera-left wall, the desk, the dark monitor legible on the far back wall, the open floor, the furniture in shadow",
  "angle": "eye-level slight wide, off-axis composition, anti-cliché",
  "camera": "35mm prime spherical, deep focus front to back, large room safe from melt",
  "lighting": "very low-key pre-dawn darkness, the sky outside still night-dark before fajr, the curtained far-wall window a deep dark blue at very low luminance, only a faint cold blue cast into the room, a soft warm practical spill from the open doorway, a light left on in the next room, that warm spill modelling Ratna from the doorway side, the rest of the room sinking into deep shadow, every screen dark and off, underexposed moody nocturnal rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic modest prayer wear, fabric worn laundered, class-accurate register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel"
}
```

### SH01-END (ANCHOR ke render START — lampu ON, monitor bangun blank, Ratna melirik senyum)
**Attach:** `sc02_sh01_start.png` (START-ref komposisi) + `E02_ruangkeluarga_screen.png` + `E02_ruangkeluarga_master.png` (LINGKUNGAN desk/monitor) + `R_ratna_profileA_medium.png` (KARAKTER — **UNCOVERED**, PROFIL hadap camera-left). Minimal-change: komposisi/posisi IDENTIK START, yang berubah = lampu ON (interior hangat), monitor menyala panel blank, Ratna melirik ke monitor dengan senyum tipis.
```json
{
  "composition_reference": "attached frame sc02_sh01_start.png, the SH01-START render, identical room composition, same Ratna position, same WS framing and crop, her body and back-to-lens profile orientation held identical to the start render, only the ceiling lamp turning on and her head turning to glance toward the desk on the far back wall by the window",
  "environment_reference": "attached reference plates E02_ruangkeluarga_screen.png and E02_ruangkeluarga_master.png, same living room, the MICKE desk, generic unbranded all-in-one desktop on the far back wall, identical layout, identical materials, single Hokusai Red Fuji print, faithful room match",
  "mood": "quiet pre-dawn domestic stillness, the household waking before fajr, a small warm beat of the day's work waiting, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "shared living room of an urban middle-class family, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, open ceramic-tiled floor kept clear, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn before sunrise, interior lamp now on",
  "atmosphere": "quiet lived-in domestic calm, warm lamplit stillness before fajr",
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_profileA_medium.png, same identical face, same identity, hair visible uncovered, faithful profile match, Ratna seen in profile with her face toward camera-left toward the switch wall",
    "role": "Jakarta middle-class home-culinary UMKM entrepreneur, modest mature Muslim woman, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "beauty": "ordinary dignified mature woman, warm approachable, lived-in, middle-class register",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, fine mature lines at eye corners, full soft even-tone brows, calm warm steady eyes, gentle full cheeks",
    "body_features": "soft maternal build, gentle midsection softness, 158cm frame, relaxed shoulders, natural mature posture"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, fine natural texture preserved, matte finish zero shine",
    "wardrobe": "comfortable home tunic relaxed modest muted, modest trousers charcoal",
    "hair": "dark hair worn in a low bun, hairline visible uncovered, dry matte hair, chalky matte finish",
    "footwear": "flat house slippers"
  },
  "subject_state": "dynamic",
  "action": "the ceiling lamp now switched on filling the room with warm light, the all-in-one desktop on the far back wall by the window standing dark and switched off, Ratna having pressed the switch now turning her head to glance toward the desk on the far back wall by the window, her body still turned to the switch wall",
  "pose": "standing in profile facing camera-left toward the switch wall, turned away from the lens, body and shoulders kept to the start-frame profile, only her head turned to glance toward the desk on the far back wall by the window, her camera-left hand lowering from the light switch on the camera-left wall",
  "expression": "calm settled attention, eyes resting toward the desk on the far back wall, mouth relaxed and neutral, quiet composed, early-morning quiet",
  "framing": "WS of the living room now warmly lamplit, Ratna at the switch wall glancing toward the desk, the lit monitor a small bright neutral panel on the far back wall, identical crop to the start frame",
  "angle": "eye-level slight wide, off-axis composition, anti-cliché",
  "camera": "35mm prime spherical, deep focus front to back, large room safe from melt",
  "lighting": "warm interior ceiling lamp now on as the key, soft warm practical fill across the room, the curtained far-wall window still dark blue pre-dawn outside, the all-in-one monitor dark and switched off, even matte rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic modest prayer wear, fabric worn laundered, class-accurate register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel"
}
```

**Audit SH01:** beat iklan tunggal; monitor = panel netral menyala blank (browser+kartu iklan ke AE, A1); START gelap subuh-biru → END lampu warm-practical; Ratna mukena (kepala tertutup, plat hijab); negasi 0; warmth dari `color_grade` + lampu praktis; tiap frame bawa baris attachment sendiri.

---

## SEQ1-SC02-SH02 — MS Herman gelar sajadah → saf terbentuk · segmen 5 dtk
**Attach START:** `sc02_sh01_end.png` (acuan cahaya warm-lamplit + kontinuitas grade SAJA, kamera baru) + `E02_ruangkeluarga_reverse_prayer.png` (LINGKUNGAN plate-sholat reverse + **4 mat warna ter-bake 1-1-2**: sage-green depan=Herman · dusty-blue tengah=Andi · terracotta belakang-kiri=Lisa · warm-taupe belakang-kanan=Ratna; sofa camera-right, TV camera-left, pintu+KALLAX latar, karpet PERSISK tengah) + `H_herman_front_full.png` (Herman, imam, di mat sage-green depan, menghadap kamera) + `R_ratna_hijab_profileA_medium.png` (Ratna mukena, **PROFIL hadap camera-LEFT**, di mat warm-taupe) + `L_lisa_profileB_full.png` (Lisa mukena, **PROFIL hadap camera-RIGHT**, di mat terracotta) + `A_andi_profileB_full.png` (Andi koko+peci, **PROFIL hadap camera-RIGHT ke Ratna**, di mat dusty-blue tengah) — momen persiapan: tiap orang **di mat warnanya**, ketiga makmum **berkumpul saling berhadapan, mengobrol santai, lengan tidak bersedekap**; mat dari plat (token mat dibuang dari teks). **END:** anchor `sc02_sh02_start.png` + `E02_ruangkeluarga_reverse_prayer.png` + keempat plat front (Herman `front_full`, Ratna `hijab_front_medium`, Lisa `front_full`, Andi `front_full`), saf terbentuk menghadap kamera (i2v START→END = badan berputar ke depan menata saf). **Bersih Saat Sakral: NOL grafis; layar mati di latar.**

### SH02-START (prompt utuh — pola baru: 4 mat dari plat, tiap orang di mat warnanya, makmum mengobrol)
> **Pola terbaru (2026-06-24):** sajadah TIDAK dibuat oleh teks — ikut dari plat `E02_ruangkeluarga_reverse_prayer.png` (4 mat polos warna-beda, 1-1-2 saf). Tiap orang dipaku ke **mat warnanya** + koordinat kanvas x/y. Compaction (dedup) + colour-anchor + canvas-pixel grammar. Mat-creation token DIBUANG.
```json
{
  "mood": "quiet pre-dawn devotion gathering, the family turning toward prayer, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "shared living room, urban middle-class family, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, open ceramic-tiled floor, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn before sunrise, interior lamp on",
  "atmosphere": "quiet lived-in domestic calm, warm lamplit devotion before fajr",
  "lighting_reference": "attached frame sc02_sh01_end.png, lighting and continuity reference only, same warm interior lamplit key, same dark blue pre-dawn window",
  "environment_reference": "attached plate E02_ruangkeluarga_reverse_prayer.png, the prayer-master reverse view, the PERSISK rug with four coloured prayer mats already laid in a one-one-two formation, sage-green front, dusty-blue middle, terracotta back-left, warm-taupe back-right, EKTORP sofa, framed Red Fuji, on the camera-right wall, BESTÅ TV bench on the camera-left wall, open doorway, KALLAX shelf, on the far wall ahead, window-desk wall behind the camera, faithful room match",
  "character_identity_husband": {
    "identity_reference": "attached plate H_herman_front_full.png, same identical face, same identity, faithful frontal match, Herman the imam kneeling on the sage-green front mat nearest the camera, facing the camera toward the window-qibla",
    "role": "Jakarta middle-class export-import office supervisor, modest mature man, dignified",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build, 168cm frame, natural mature posture"
  },
  "character_style_husband": {
    "makeup": "bare mature skin, matte finish zero shine",
    "wardrobe": "long-sleeve plain koko shirt stand-collar muted off-white, solid plain-weave sarong dark muted colorway wrapped waist, black velvet peci cap",
    "hair": "hair concealed under the black velvet peci cap, uniformly salt-and-pepper at the sides",
    "footwear": "barefoot"
  },
  "character_identity_wife": {
    "identity_reference": "attached plate R_ratna_hijab_profileA_medium.png, same identical face, same identity, head covered, faithful profile match, Ratna in profile facing camera-left, standing on the warm-taupe back-right mat turned toward the children",
    "role": "modest mature Muslim woman, makmum, dignified maternal warmth",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, soft natural skin texture, gentle full cheeks",
    "body_features": "soft maternal build, 158cm frame, full adult standing height, natural upright head-to-body proportions, tall composed stature"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, matte finish zero shine",
    "wardrobe": "two-piece white mukena prayer set, opaque cotton, full head-and-body cover, plain matte weave",
    "hair": "hair fully concealed under the white mukena head-cover",
    "footwear": "barefoot"
  },
  "character_identity_daughter": {
    "identity_reference": "attached plate L_lisa_profileB_full.png, same identical face, same identity, faithful profile match, Lisa in profile facing camera-right, standing on the terracotta back-left mat turned toward her mother Ratna",
    "role": "young woman university student, daughter, makmum",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "young woman 19 years old",
    "facial_features": "youthful smooth complexion, soft natural skin texture, calm eyes",
    "body_features": "young slender build, natural 34C bustline, 162cm frame, full adult standing height, natural upright head-to-body proportions, tall composed stature"
  },
  "character_style_daughter": {
    "makeup": "natural youthful skin, soft matte finish zero shine",
    "wardrobe": "two-piece white mukena prayer set, opaque cotton, full head-and-body cover, plain matte weave",
    "hair": "hair fully concealed under the white mukena head-cover",
    "footwear": "barefoot"
  },
  "character_identity_son": {
    "identity_reference": "attached plate A_andi_profileB_full.png, same identical face, same identity, faithful profile match, Andi the young son in profile facing camera-right toward his mother Ratna, standing on the dusty-blue middle mat",
    "role": "young boy, son, makmum",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "boy 10 years old",
    "facial_features": "clear healthy child complexion, soft child skin texture, bright calm eyes",
    "body_features": "plain child build, 138cm frame"
  },
  "character_style_son": {
    "makeup": "bare healthy child skin, matte finish zero shine",
    "wardrobe": "long-sleeve plain child koko shirt stand-collar muted off-white, child solid plain-weave sarong dark muted wrapped waist, small black velvet peci cap",
    "hair": "child hair concealed under the small black velvet peci cap",
    "footwear": "barefoot"
  },
  "subject_state": "dynamic",
  "action": "Herman kneeling on the sage-green front mat, smoothing it, facing the camera toward the window-qibla; behind him the mother and two children gathered each on their own coloured prayer mat before prayer, chatting softly, smiling, arms hanging loose and open at their sides, turned inward toward one another in warm conversation",
  "pose": "Herman foreground on the sage-green front mat at x 960 y 920, kneeling, facing the camera; Andi standing on the dusty-blue middle mat at x 960 y 780 facing camera-right toward his mother; Lisa standing on the terracotta mat at x 800 y 640 facing camera-right toward Ratna; Ratna standing on the warm-taupe mat at x 1120 y 640 facing camera-left toward the children; the three makmum turned inward in a relaxed chat, the one-one-two formation reading in depth toward the lens, the EKTORP sofa beyond x 1500 at camera-right and the BESTÅ TV bench before x 420 at camera-left kept outside the figures band, 16:9 canvas at 1920x1080 reference",
  "expression": "Herman calm focused on the mat, mother and two children warm with light happy smiles mid soft chat, an easy joyful family moment before prayer",
  "framing": "MS to WS across the prayer rug, Herman on the sage-green front mat in the foreground, the three on their coloured mats behind in one-one-two depth, the open doorway on the far wall behind the family",
  "angle": "eye-level, Herman facing the camera in the foreground, the makmum on their mats behind turned toward one another, slightly off-axis, anti-cliché",
  "camera": "35mm prime spherical, focus on Herman at the front mat, soft background falloff",
  "lighting": "warm interior ceiling lamp key, soft warm practical fill, faint dark blue pre-dawn spill from the window-wall behind the camera, the flat-screen television at camera-left dark and switched off, zero graphics, even matte rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic modest prayer wear, fabric worn laundered, class-accurate register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel"
}
```

### SH02-END (ANCHOR ke render START — keluarga berkumpul membentuk saf di belakang imam)
**Attach:** `sc02_sh02_start.png` (komposisi/cahaya) + `E02_ruangkeluarga_reverse_prayer.png` (LINGKUNGAN plate-sholat reverse) + `H_herman_front_full.png` + `R_ratna_hijab_front_medium.png` + `L_lisa_front_full.png` + `A_andi_front_full.png` (KARAKTER keempat, menghadap kamera). Beda dari START = saf terbentuk: Herman imam berdiri di depan (terdekat kamera) menghadap kamera, tiga makmum (Andi · Ratna · Lisa) satu baris bahu-membahu di belakangnya (lebih dalam di ruang), semua menghadap kamera. **Lisa mukena, Andi koko+sarung+peci anak.**
```json
{
  "composition_reference": "attached frame sc02_sh02_start.png, the SH02-START render, same living room reverse view, same warm lamplit pre-dawn lighting and grade, same prayer mat on the rug; CHANGE: the family now standing in a prayer line facing the camera, Herman risen as imam at the front nearest the camera, the three makmum in one row behind him facing the camera",
  "environment_reference": "attached reference plate E02_ruangkeluarga_reverse_prayer.png, the prayer-master reverse view, the PERSISK oriental rug laid flat as the central prayer surface with four prayer mats laid in a column on it, EKTORP sofa, framed Red Fuji print, on the camera-right wall, BESTÅ TV bench on the camera-left wall, the two floor cushions set beside the TV bench at camera-left, the open doorway, the KALLAX shelf, on the far wall ahead, the window-desk wall behind the camera, faithful room match",
  "mood": "quiet pre-dawn congregational devotion, the family standing for fajr behind the imam, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "shared living room of an urban middle-class family, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, open ceramic-tiled floor for prayer, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn before sunrise, interior lamp on",
  "atmosphere": "quiet lived-in domestic calm, warm lamplit congregational devotion",
  "character_identity_husband": {
    "identity_reference": "attached reference plate H_herman_front_full.png, same identical face, same identity, faithful frontal match, Herman the imam at the front nearest the camera, facing the camera toward the window-qibla",
    "role": "Jakarta middle-class export-import office supervisor, modest mature man, the imam leading the prayer",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build, 168cm frame, natural mature posture"
  },
  "character_style_husband": {
    "makeup": "bare mature skin, matte finish zero shine",
    "wardrobe": "long-sleeve plain koko shirt stand-collar muted off-white, solid plain-weave sarong dark muted colorway wrapped waist, black velvet peci cap",
    "hair": "hair concealed under the black velvet peci cap",
    "footwear": "barefoot"
  },
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_hijab_front_medium.png, same identical face, same identity, head covered, faithful frontal match, Ratna a makmum in the row behind the imam, facing the camera",
    "role": "modest mature Muslim woman, makmum",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, gentle full cheeks",
    "body_features": "soft maternal build, 158cm frame, full adult standing height, natural upright head-to-body proportions, tall composed stature"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, matte finish zero shine",
    "wardrobe": "two-piece white mukena prayer set, opaque cotton, full head-and-body cover, plain matte weave",
    "hair": "hair fully concealed under the white mukena head-cover",
    "footwear": "barefoot"
  },
  "character_identity_daughter": {
    "identity_reference": "attached reference plate L_lisa_front_full.png, same identical face, same identity, faithful frontal match, Lisa the daughter, a makmum in the row behind the imam, facing the camera",
    "role": "young woman university student, daughter, makmum",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "young woman 19 years old",
    "facial_features": "youthful smooth complexion, soft natural skin texture, calm eyes",
    "body_features": "young slender build, natural 34C bustline, 162cm frame, full adult standing height, natural upright head-to-body proportions, tall composed stature"
  },
  "character_style_daughter": {
    "makeup": "natural youthful skin, soft matte finish zero shine",
    "wardrobe": "two-piece white mukena prayer set, opaque cotton, full head-and-body cover, plain matte weave",
    "hair": "hair fully concealed under the white mukena head-cover",
    "footwear": "barefoot"
  },
  "character_identity_son": {
    "identity_reference": "attached reference plate A_andi_front_full.png, same identical face, same identity, faithful frontal match, Andi the young son, a makmum in the row behind the imam, facing the camera",
    "role": "young boy, son, makmum",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "boy 10 years old",
    "facial_features": "clear healthy child complexion, soft child skin texture, bright calm eyes",
    "body_features": "plain child build, 138cm frame"
  },
  "character_style_son": {
    "makeup": "bare healthy child skin, matte finish zero shine",
    "wardrobe": "long-sleeve plain child koko shirt stand-collar muted off-white, child solid plain-weave sarong dark muted wrapped waist, small black velvet peci cap",
    "hair": "child hair concealed under the small black velvet peci cap",
    "footwear": "barefoot"
  },
  "subject_state": "static",
  "action": "the family standing in congregational formation facing the camera, Herman the imam standing alone at the front on his prayer mat nearest the camera facing the camera toward the window-qibla, the boy Andi standing on his own prayer mat well forward one row directly behind the imam, a clear step ahead of the women, Ratna and Lisa standing side by side on their own prayer mats a full row further back behind Andi, distinctly behind him, all facing the camera, hands at their sides settling before takbir",
  "pose": "Herman at the front nearest the camera on his mat facing the camera; one row behind him the boy Andi on his own mat; a full row further back behind Andi, distinctly behind him the two women Ratna and Lisa side by side on their own mats; the saf reading imam, then the boy, then the women, in depth toward the lens",
  "expression": "all calm, eyes lowered, devotional stillness, settled",
  "framing": "WS of the prayer formation facing the camera, the imam at the front nearest the camera, Andi one row behind, Ratna and Lisa in the back row held within the central band of the 16:9 frame from x 680 to x 1240 of 1920, a clear margin of at least 430px to each side edge, four prayer mats in a column, the whole saf legible, the EKTORP sofa camera-right, the BESTÅ TV bench camera-left, the open doorway on the far wall behind the family",
  "angle": "eye-level, the saf facing the camera, imam-front and makmum-row in depth, slightly off-axis, anti-cliché",
  "camera": "35mm prime spherical, deep focus front to back, large-room WS safe from melt",
  "lighting": "warm interior ceiling lamp key, soft warm practical fill across the saf, faint dark blue pre-dawn spill from the window-wall behind the camera, the flat-screen television on the camera-left wall dark and switched off, zero graphics, even matte rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic modest prayer wear, fabric worn laundered, class-accurate register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel"
}
```

**Audit SH02:** payoff sarung pada imam Herman; Bersih Saat Sakral mulai (nol grafis, monitor redup/mati latar); empat figur di Lapis-3 (subjek wajib di prompt, bukan diharap dari attachment); blocking saf qibla=camera-left, imam-depan/makmum-baris-belakang; Lisa+Andi penutup dari wardrobe (mukena/peci); negasi 0; warmth dari `color_grade`+lampu; tiap frame bawa baris attachment sendiri.

---

## SEQ1-SC02-SH03 — WS qiyam bersedekap (ditahan, START→END beda angle) · segmen 5 dtk
**Penyederhanaan (Erik 2026-06-24):** pose **berdiri bersedekap (qiyam, tangan kanan di atas kiri di dada/perut) DITAHAN identik** dari START ke END; yang berubah **HANYA kamera** — START eye-level menghadap kamera, END **push-in sedikit lebih rapat di sumbu reverse yang sama** (high-angle dibatalkan: plate `prayer_high` = sumbu lama, tak cocok reverse). Tidak ada gerak pose multi-karakter (ruku/sujud dibuang). Gerak i2v = push-in halus atas subjek statis, risiko warp minimal.

**Attach START:** `sc02_sh02_end.png` (acuan komposisi saf + cahaya) + `E02_ruangkeluarga_reverse_prayer.png` (LINGKUNGAN plate-sholat reverse) + keempat plat (Herman `front_full`, Ratna `hijab_front_medium`, Lisa `front_full`, Andi `front_full`). **Attach END:** `sc02_sh03_start.png` (anchor identitas+pose, pose ditahan) + `E02_ruangkeluarga_reverse_prayer.png` (LINGKUNGAN, sumbu sama, framing sedikit lebih rapat) + keempat plat.

### SH03-START (prompt utuh — qiyam bersedekap, eye-level frontal-off-axis)
```json
{
  "mood": "quiet pre-dawn congregational prayer, the family standing in qiyam for fajr, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "shared living room of an urban middle-class family, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, open ceramic-tiled floor for prayer, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn before sunrise, interior lamp on",
  "atmosphere": "quiet lived-in domestic calm, warm lamplit congregational devotion",
  "composition_reference": "attached frame sc02_sh02_end.png, the SH02-END render, continuity anchor — same imam Herman at the front nearest the camera, same boy Andi well forward one row directly behind the imam, a clear step ahead of the women, same Ratna and Lisa in the back row, all facing the camera, same warm lamplit pre-dawn lighting and grade; the family now standing in qiyam with arms folded",
  "environment_reference": "attached reference plate E02_ruangkeluarga_reverse_prayer.png, the prayer-master reverse view, the PERSISK rug as the prayer surface with four prayer mats laid in a column on it, EKTORP sofa, framed Red Fuji print, on the camera-right wall, BESTÅ TV bench on the camera-left wall, the open doorway on the far wall ahead, the window-desk wall behind the camera, faithful room match",
  "character_identity_husband": {
    "identity_reference": "attached reference plate H_herman_front_full.png, same identical face, same identity, faithful frontal match, Herman the imam at the front nearest the camera, facing the camera toward the window-qibla",
    "role": "modest mature man, the imam leading the prayer",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build, 168cm frame, natural mature posture"
  },
  "character_style_husband": {
    "makeup": "bare mature skin, matte finish zero shine",
    "wardrobe": "long-sleeve plain koko shirt stand-collar muted off-white, solid plain-weave sarong dark muted colorway wrapped waist, black velvet peci cap",
    "hair": "hair concealed under the black velvet peci cap",
    "footwear": "barefoot"
  },
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_hijab_front_medium.png, same identical face, same identity, head covered, faithful facial and head match, Ratna a makmum in the row",
    "role": "modest mature Muslim woman, makmum",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, gentle full cheeks",
    "body_features": "soft maternal build, 158cm frame, full adult standing height, natural upright head-to-body proportions, tall composed stature"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, matte finish zero shine",
    "wardrobe": "two-piece white mukena prayer set, opaque cotton, full head-and-body cover, plain matte weave",
    "hair": "hair fully concealed under the white mukena head-cover",
    "footwear": "barefoot"
  },
  "character_identity_daughter": {
    "identity_reference": "attached reference plate L_lisa_front_full.png, same identical face, same identity, faithful frontal match, Lisa a makmum in the row behind the imam, facing the camera",
    "role": "young woman student, daughter, makmum",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "young woman 19 years old",
    "facial_features": "youthful smooth complexion, calm eyes",
    "body_features": "young slender build, natural 34C bustline, 162cm frame, full adult standing height, natural upright head-to-body proportions, tall composed stature"
  },
  "character_style_daughter": {
    "makeup": "natural youthful skin, soft matte finish zero shine",
    "wardrobe": "two-piece white mukena prayer set, opaque cotton, full head-and-body cover, plain matte weave",
    "hair": "hair fully concealed under the white mukena head-cover",
    "footwear": "barefoot"
  },
  "character_identity_son": {
    "identity_reference": "attached reference plate A_andi_front_full.png, same identical face, same identity, faithful frontal match, Andi a makmum in the row behind the imam, facing the camera",
    "role": "young boy, son, makmum",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "boy 10 years old",
    "facial_features": "clear healthy child complexion, bright calm eyes",
    "body_features": "plain child build, 138cm frame"
  },
  "character_style_son": {
    "makeup": "bare healthy child skin, matte finish zero shine",
    "wardrobe": "long-sleeve plain child koko shirt stand-collar muted off-white, child solid plain-weave sarong dark muted wrapped waist, small black velvet peci cap",
    "hair": "child hair concealed under the small black velvet peci cap",
    "footwear": "barefoot"
  },
  "subject_state": "static",
  "action": "the whole family standing still in qiyam, arms folded in prayer, the right hand resting over the left across the front of the body, Herman the imam at the front on his prayer mat nearest the camera facing the camera, the boy Andi well forward one row directly behind the imam, a clear step ahead of the women on his own mat, Ratna and Lisa side by side a full row further back behind Andi, distinctly behind him on their own mats, all standing in the same folded-arm posture facing the camera, held motionless",
  "pose": "Herman at the front nearest the camera one step ahead on his mat facing the camera, arms folded; one row behind him the boy Andi on his own mat, arms folded; a full row further back behind Andi, distinctly behind him the two women Ratna and Lisa side by side on their own mats, arms folded; the saf reading imam, then the boy, then the women, in depth toward the lens, every figure held still",
  "expression": "all calm, eyes lowered to the floor ahead, devotional stillness",
  "framing": "WS of the standing prayer facing the camera, the imam at the front nearest the camera, Andi one row behind, Ratna and Lisa in the back row held within the central band of the 16:9 frame from x 680 to x 1240 of 1920, a clear margin of at least 430px to each side edge, four prayer mats in a column, full saf legible, the EKTORP sofa camera-right, the BESTÅ TV bench camera-left, the open doorway on the far wall behind the family",
  "angle": "eye-level, the saf facing the camera, reading in depth, slightly off-axis, anti-cliché",
  "camera": "35mm prime spherical, deep focus front to back, large-room WS safe from melt",
  "lighting": "warm interior ceiling lamp key, soft warm practical fill across the saf, faint dark blue pre-dawn spill from the window-wall behind the camera, the flat-screen television on the camera-left wall dark and switched off, zero graphics, even matte rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic modest prayer wear, fabric worn laundered, class-accurate register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel"
}
```

### SH03-END (ANCHOR ke render START — pose qiyam DITAHAN identik, kamera ke soft high-angle ~45°)
**Attach:** `sc02_sh03_start.png` (anchor identitas+pose — pose bersedekap ditahan, JANGAN ubah) + `E02_ruangkeluarga_reverse_prayer.png` (LINGKUNGAN, sumbu sama) + keempat plat front. Beda dari START = **HANYA kamera**: push-in sedikit lebih rapat di sumbu reverse yang sama. Pose, wardrobe, identitas, susunan saf identik.
```json
{
  "composition_reference": "attached frame sc02_sh03_start.png, the SH03-START render, the SAME family in the SAME folded-arm qiyam posture, same imam at the front, same boy Andi one row behind, same Ratna and Lisa in the back row, all facing the camera, same wardrobe, same warm lamplit pre-dawn lighting and grade; the ONLY change is the camera pushing in slightly closer on the same reverse axis, the prayer posture itself held completely identical and unchanged",
  "environment_reference": "attached reference plate E02_ruangkeluarga_reverse_prayer.png, the prayer-master reverse view, same axis as the start frame, slightly tighter framing pushed in on the saf, the PERSISK rug and the four prayer mats prominent, EKTORP sofa camera-right, BESTÅ TV bench camera-left, the open doorway on the far wall ahead, faithful room match",
  "mood": "quiet pre-dawn congregational prayer held in a calm settled frame, Roma-style observational tenderness",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, clean prime spherical lens, Kodak 2383 print stock emulation",
  "scene": "shared living room of an urban middle-class family, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, open ceramic-tiled floor for prayer, lived-in working-family",
  "location": "indoor",
  "time_of_day": "pre-dawn before sunrise, interior lamp on",
  "atmosphere": "quiet lived-in domestic calm, warm lamplit congregational devotion",
  "character_identity_husband": {
    "identity_reference": "attached reference plate H_herman_front_full.png, same identical face, same identity, faithful frontal match, Herman the imam at the front nearest the camera, facing the camera toward the window-qibla",
    "role": "modest mature man, the imam leading the prayer",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "man 46 years old",
    "facial_features": "luminous healthy complexion, full uniformly grey moustache trimmed even tone, calm steady eyes",
    "body_features": "average build, 168cm frame, natural mature posture"
  },
  "character_style_husband": {
    "makeup": "bare mature skin, matte finish zero shine",
    "wardrobe": "long-sleeve plain koko shirt stand-collar muted off-white, solid plain-weave sarong dark muted colorway wrapped waist, black velvet peci cap",
    "hair": "hair concealed under the black velvet peci cap",
    "footwear": "barefoot"
  },
  "character_identity_wife": {
    "identity_reference": "attached reference plate R_ratna_hijab_front_medium.png, same identical face, same identity, head covered, faithful facial and head match, Ratna a makmum in the row",
    "role": "modest mature Muslim woman, makmum",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "woman 41 years old",
    "facial_features": "luminous healthy complexion, gentle full cheeks",
    "body_features": "soft maternal build, 158cm frame, full adult standing height, natural upright head-to-body proportions, tall composed stature"
  },
  "character_style_wife": {
    "makeup": "bare mature skin, matte finish zero shine",
    "wardrobe": "two-piece white mukena prayer set, opaque cotton, full head-and-body cover, plain matte weave",
    "hair": "hair fully concealed under the white mukena head-cover",
    "footwear": "barefoot"
  },
  "character_identity_daughter": {
    "identity_reference": "attached reference plate L_lisa_front_full.png, same identical face, same identity, faithful frontal match, Lisa a makmum in the row behind the imam, facing the camera",
    "role": "young woman student, daughter, makmum",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "young woman 19 years old",
    "facial_features": "youthful smooth complexion, calm eyes",
    "body_features": "young slender build, natural 34C bustline, 162cm frame, full adult standing height, natural upright head-to-body proportions, tall composed stature"
  },
  "character_style_daughter": {
    "makeup": "natural youthful skin, soft matte finish zero shine",
    "wardrobe": "two-piece white mukena prayer set, opaque cotton, full head-and-body cover, plain matte weave",
    "hair": "hair fully concealed under the white mukena head-cover",
    "footwear": "barefoot"
  },
  "character_identity_son": {
    "identity_reference": "attached reference plate A_andi_front_full.png, same identical face, same identity, faithful frontal match, Andi a makmum in the row behind the imam, facing the camera",
    "role": "young boy, son, makmum",
    "ethnicity": "modern Jakartan features, Javanese urban descent",
    "age": "boy 10 years old",
    "facial_features": "clear healthy child complexion, bright calm eyes",
    "body_features": "plain child build, 138cm frame"
  },
  "character_style_son": {
    "makeup": "bare healthy child skin, matte finish zero shine",
    "wardrobe": "long-sleeve plain child koko shirt stand-collar muted off-white, child solid plain-weave sarong dark muted wrapped waist, small black velvet peci cap",
    "hair": "child hair concealed under the small black velvet peci cap",
    "footwear": "barefoot"
  },
  "subject_state": "static",
  "action": "the whole family still standing in the identical folded-arm qiyam, arms folded right over left, held completely motionless, the camera pushed in slightly closer on the same reverse axis, the imam at the front nearest the camera, the boy Andi one row behind, Ratna and Lisa in the back row, all facing the camera unchanged in posture",
  "pose": "identical to the start frame, Herman at the front nearest the camera one step ahead facing the camera, one row behind him the boy Andi, a full row further back behind Andi, distinctly behind him the two women Ratna and Lisa side by side, every figure on their own prayer mat with arms folded, the saf reading imam, then the boy, then the women, in depth toward the lens",
  "expression": "all calm, eyes lowered, devotional stillness, a settled held frame",
  "framing": "WS pushed in slightly tighter on the saf facing the camera, the four prayer mats in a column and the saf centred on the rug clear of the side walls prominent, the open floor around them, a calm composed frame clean of any interface or graphics",
  "angle": "eye-level, the saf facing the camera, pushed in slightly closer, reading in depth, slightly off-axis, anti-cliché",
  "camera": "35mm prime spherical, deep focus front to back, pushed in slightly closer at standing eye-level",
  "lighting": "warm interior ceiling lamp key, soft warm practical fill across the saf, faint dark blue pre-dawn spill from the window-wall behind the camera, the flat-screen television on the camera-left wall dark and switched off, zero graphics, even matte rendering",
  "aspect_ratio": "16:9",
  "director": "Alfonso Cuarón", "directing_style": "observational domestic naturalism, unhurried intimate register",
  "lighting_director": "Emmanuel Lubezki", "lighting_style": "naturalistic available-light feel, soft motivated sources, gentle falloff",
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality",
  "costume_designer": "Deborah Hopper", "costume_style": "character-authentic modest prayer wear, fabric worn laundered, class-accurate register",
  "makeup_artist": "Eryn Krueger Mekash", "makeup_style": "naturalistic everyday beauty, lived-in skin, real-person feel"
}
```

**Audit SH03:** pose qiyam bersedekap DITAHAN identik START→END (zero gerak pose multi-karakter — anti i2v-warp); gerak hanya kamera eye-level→push-in di sumbu reverse (plate `reverse`, high-angle dibatalkan); zona sakral nol grafis; blocking saf konsisten SH02 (qibla=jendela/kamera, imam-depan-terdekat-kamera/makmum-baris-belakang, menghadap kamera); empat figur di Lapis-3; Lisa+Andi penutup dari wardrobe; negasi 0; warmth dari `color_grade`+lampu; tiap frame bawa attachment sendiri.

---

## Manifest
| Shot | Frame | File target | Status |
|---|---|---|---|
| SH01 WS desktop (beat iklan) | START | `scene-images/sc02/sc02_sh01_start.png` | ✅ ACCEPTED (2026-06-24) |
| | END | `scene-images/sc02/sc02_sh01_end.png` | ✅ ACCEPTED (2026-06-24, refleks menengok ruang baru-menyala; verifikasi adversarial digeser ke shot berikutnya per Erik) |
| SH02 MS sajadah→saf | START | `scene-images/sc02/sc02_sh02_start.png` | ✅ ACCEPTED (2026-06-24, POLA BARU: mat-dari-plat + colour-anchor + canvas x/y + compaction; one-shot, Erik "jenius") |
| | END | `scene-images/sc02/sc02_sh02_end.png` | ⏳ |
| SH03 WS qiyam (ditahan, beda angle) | START | `scene-images/sc02/sc02_sh03_start.png` | ⏳ |
| | END | `scene-images/sc02/sc02_sh03_end.png` | ⏳ |

Storage: `scene-images/sc02/`. Generate urut SH01-START → SH01-END → SH02-START → SH02-END → SH03-START → SH03-END; review tiap render (wajah/ruang/saf vs plat) sebelum lanjut; rename yang accepted → `sc02_sh<NN>_<start|end>.png`; nol `Content*.png` leftover.

*SEQ1-SC02 keyframe sheet v1.0 · Explainer Video 2 · 2026-06-24 · 3 shot / 6 keyframe (SH04 sujud dihapus, SH03 disederhanakan ke qiyam-ditahan beda-angle, Erik 2026-06-24) · format [[10-gateB-keyframes/SEQ1-SC01]] · env [[09-environment-sheet/E02-ruangkeluarga]]*
