---
title: Prompt Rules — Image Generation · Semesta Digital
tags: [prompt-rules, image-generation, active]
status: active
created: 2026-06-09
updated: 2026-06-10
---

# Image Generation Prompt Rules
## Semesta Digital — Semua Model Image Generation
*Berlaku untuk: GPT Image 2, Midjourney, Kling, Runway, Seedance, dan model apapun di pipeline ini.*
*Validated through live generation sessions · Updated continuously*
*Related files: [[tokens-references/CREW-REFERENCE]] · [[tokens-references/TOKENS-REFERENCE]] · [[tokens-references/INTERIOR-DESIGN-REFERENCE]]*

---

## PRINSIP UTAMA — TOKEN DISCIPLINE

**Satu token kuat melingkupi banyak hal. Percayakan ke model.**

- Token strings, bukan kalimat
- Tanpa kata sambung (and, but, with)
- Tanpa copula (is, are, was, be)
- Tanpa to-be, tanpa tenses
- **Tanpa negasi — MUTLAK. `no X`, `not X`, `not in frame`, `without X`, `un-`, `non-`. Negasi dibaca model sebagai izin berinisiatif → non-compliant. Tulis POSITIF (apa yang ADA), atau HAPUS field bila elemennya tak tampak. `tidak berkepala`→`headless`.**
- Tanpa label abstrak (warm, natural, realistic, authentic) kecuali industry-convention term
- Tanpa redundansi lintas field — jika facial_features sudah ada, makeup_style tidak ulang
- Tanpa redundansi dalam satu field — satu token kuat, tidak perlu diperkuat token lain yang bilang hal sama
- Adjective-dense C2 English: precise, concrete, industry-convention terminology
- Child style = 4–6 tokens maximum, masing-masing load-bearing

**WRONG:** `"natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish, zero performance artifice, authentic real-person face"`
→ redundant, abstract labels, negation

**RIGHT:** `"natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish"`

**WRONG (redundansi dalam field):** `"slight forward lean, body 30 degrees camera, settled mid-delivery"`
→ tiga token bilang hal sama

**RIGHT:** `"body 30 degrees camera, weight front leg"`

---

## STRUKTUR 6 LAPIS (mandatory)

```
Lapis 1 — GLOBAL ANCHO  mood, color_grade, style

Lapis 2 — WORLD & SPACE
  scene, location, time_of_day, atmosphere, scene_depth

Lapis 3 — SUBJECT (FIXED)
  character_identity { role, ethnicity, beauty, age, facial_features, body_features }
  character_style    { makeup, wardrobe, hair, footwear }
  — ATAU —
  subject_anchor { primary_subject, subject_material, supporting_objects, human_absence_signal }

Lapis 4 — EVENT & STATE (VARIABLE)
  subject_state, action, pose, gesture, expression

Lapis 5 — GRAPHIC LAYER  ❌ DIBATALKAN untuk video (ADDENDUM A1, 2026-06-21)
  on_screen_graphic / graphic_proximity / ui_overlay = DIBUANG dari semua prompt keyframe video.
  Semua grafis (UI/kartu iklan/grafik/super/motion) digarap di After Effects oleh animator manusia,
  composite di post. Device tetap muncul, framing comp-aware (ruang layar bersih), layar netral/mati.
  Kanonik: 00-WORKLOG ADDENDUM A1. (Berlaku video; deck still S0–S17b tetap pakai field grafis lama.)

Lapis 6 — CINEMATIC TECHNICAL
  framing, angle, camera, lighting, aspect_ratio
  director, directing_style
  lighting_director, lighting_style
  production_designer, production_design_style
  interior_designer, interior_design_style
  costume_designer, costume_style
  makeup_artist, makeup_style
```

**Logika urutan:** dunia terbentuk → peristiwa terjadi → subjek hadir → teknis mengontrol
**CRITICAL:** Nama orang di Lapis 1 → model generate wajah mereka. Nama orang di Lapis 6 → style anchor only.

**ISTILAH KULTURAL: PAKAI PADANAN BER-PRIOR-KUAT (English), HINDARI NICHE/TRANSLITERASI (Validated 2026-06-23, E01 mukena/peci).** Model t2i terlatih dominan data Barat/non-Islam → istilah Islam-Nusantara niche tanpa padanan Inggris kuat di-render reka-reka. Aturan: token = istilah yang model PAHAM. `mukena` (tanpa English umum; Arab pun tak ber-prior-kuat — garmen Nusantara) → deskriptif kuat `folded white prayer shawl` (atau turun `folded white cloth`). `peci`/songkok (niche) → `black brimless velvet cap` (deskripsi bentuk). JANGAN ganti istilah yang SUDAH ber-prior-kuat menjadi transliterasi: `prayer mat/prayer rug` (objek Islam dikenali kuat di data Barat) JANGAN jadi `sholat mat`; `hijab`/`headscarf` + `sarong` aman dipertahankan. Prinsip: prior kuat > "akurasi nama" lokal; akurasi kultural dijaga di kombinasi objek ber-prior-kuat, bukan nama niche. **KOREKSI render (E01, 2026-06-23):** untuk garmen yang BENAR-BENAR tak punya padanan English ber-prior (mukena), frasa English generik multi-kata (`folded white prayer shawl`) malah MULTITAFSIR → model memunculkan objek tambahan di zona itu. Token tunggal lokal (`mukena`) ternyata LEBIH aman: di-render sebagai satu kain terlipat netral, tak memicu objek ganda. Jadi urutan pilihan: (1) ada English-prior-kuat → pakai English; (2) tak ada → token tunggal lokal > frasa English generik multi-kata; (3) kalau token tunggal pun gagal → turun ke satu objek strong-prior konkret (`folded white linens`).

**IMPROVISASI = CELAH PROMPT; TUTUP DENGAN ENUMERASI TERTUTUP, JANGAN MAKLUMI (Validated 2026-06-23, E01 master regen).** Kalau model menambah objek tak diminta (mis. bingkai dinding + ornamen di dinding kosong), itu tanda prompt kurang mendikte zona itu — BUKAN untuk dimaklumi. Perbaiki di prompt: zona kosong (dinding, permukaan) dikunci enumerasi tertutup afirmatif — sebut "the only N items total: A, B" + "kept clean bare empty" (tanpa negasi `no other`). Contoh dinding E01: `wall_art` = Hokusai + "surrounding walls plain matte plaster kept clean bare empty, this single framed Hokusai print the only wall-mounted item in the entire room". CATATAN PENTING: jangkar zona itu pilih SATU objek bermerek/ber-prior-kuat saja (Hokusai) — jangan tambah objek lembut tak-bermerek (mis. headscarf-on-hook) sebagai "pengisi", karena justru jadi sumber inkonsistensi baru lintas-angle; benda lembut taruh di permukaan (rak), bukan dipajang di dinding. Pola sama dengan `otherwise uncluttered surface` (E01 nakas) + enumerate-every-accessory (E02).

**PLAT ENV NETRAL-GRADE → START SETUP-BARU LAMPIRKAN KEYFRAME ACCEPTED SBG ACUAN CAHAYA (Validated 2026-06-23, GATE B SEQ1-SC01-SH02).** Plat environment dibuat grade NETRAL (geometri/props, bukan look scene) — look hangat/redup hanya lahir di keyframe GATE B yang sudah digenerate. Maka START dari setup-kamera-baru di scene yang SUDAH ter-lit harus melampirkan satu keyframe accepted scene itu sebagai `lighting_reference` (acuan pencahayaan + tone tekstil), DI SAMPING plat subjek — beri token peran eksplisit ("used only as the lighting and bedding reference, not a composition source") agar generator tak menyeret subjek/komposisi dari acuan cahaya itu. Tanpa ini, START render terang/netral dan putus kontinuitas dari shot sebelumnya.

**REGEN-ON-PROMPT-CHANGE HANYA BILA TARGET VISUAL BERUBAH (Validated 2026-06-23, GATE B SEQ1-SC01).** Prompt yang berubah TIDAK selalu menuntut generate ulang. Bila perubahan mengubah target visual (mis. framing ECU→MCU, pose, wardrobe), render lama menyimpang → regen + validasi token baru. Bila perubahan hanya pembersihan token-discipline yang MEMPERTAHANKAN target visual (de-negasi, sinonim setara — mis. `unguarded`→`open, fully at rest`), render accepted tetap instance setia → JANGAN regen (regen = buang frame valid + bisa merusak pasangan start/end yang sudah match). Diskriminator: apakah gambar yang seharusnya dihasilkan berubah?

**KEYFRAME-PAIR: END ANCHOR KE RENDER START (Validated 2026-06-23, GATE B SEQ1-SC01).** Untuk pasangan start/end satu shot (masuk Kling i2v), frame END digenerate dengan meng-attach GAMBAR START yang sudah jadi sebagai jangkar komposisi (field `composition_reference` menyebut file render START) + plat wajah untuk identitas; prompt direduksi jadi minimal-change — komposisi/posisi kepala/framing/lighting IDENTIK START, hanya Lapis-4 (peristiwa) berubah. JANGAN generate END hanya dari plat (wajah/kamar) — plat netral menghasilkan komposisi BARU yang tak match START → i2v men-warp antara dua frame tak-sejajar. Berlaku juga untuk start yang chain dari end shot sebelumnya (anchor ke render end itu). Catatan: ini melengkapi aturan attachment-line — START lahir dari plat, END lahir dari render START.

**EYELINE SUBJEK TELENTANG = TERGANTUNG POSISI KAMERA (Validated 2026-06-23, GATE B SEQ1-SC01-SH01-END, dikoreksi dari render).** Hanya bila kamera BENAR-BENAR overhead (tepat di atas wajah) gaze "ke atas" = ke lensa. Bila kamera **diagonal-atas-samping** (kasus nyata SH01: render keluar 3/4 dari sisi-atas, bukan tepat overhead), gaze-ke-lensa terbaca seperti menatap-menyamping ke penonton = canggung. Maka untuk angle diagonal, tulis eyeline = `gaze up toward the ceiling above, eyes directed upward over the camera` (mata ke atas vertikal, otomatis menjauh dari lensa = natural orang bangun). Pelajaran: cek posisi kamera di RENDER dulu sebelum mengunci arah eyeline; jangan asumsikan overhead.

**FRAMING FIGUR-BERBARING + `environment_reference` SELALU MELEBAR — UNTUK SHOT RAPAT PAKAI CU/ECU, JANGAN MCU (Validated 2026-06-23, GATE B SEQ1-SC01-SH01, 3 render).** Subjek berbaring/duduk di ranjang + plat ruang di-attach selalu di-render LEBIH LEBAR dari token; token `MCU` mendarat di MS/wide two-shot (apalagi bila ada 2 figur). Maka: kalau mau shot RAPAT pada wajah, tulis **`CU close-up ... face filling the frame, tight crop`** (atau ECU) — selalu spec satu tingkat lebih ketat dari target karena generator drift melebar. `MCU` hanya kalau memang mau MS-ish. Figur kedua (mis. istri tidur) ditaruh "soft/partial near-background", bukan two-shot seimbang, supaya subjek utama tetap dominan.

**SCREEN-GLOW KE WAJAH = LAYAR ON + HP PUNGGUNG-KE-KAMERA (Validated 2026-06-23, GATE B SEQ1-SC01-SH02-END).** Kalau butuh cahaya layar HP memancar ke wajah subjek, JANGAN tulis "layar off + glow disimulasikan" (kontradiktif: off tak memancar). Teknik benar: **layar ON (menyala) menghadap subjek, tapi HP dipegang rear-casing-toward-camera** → glow ke wajah NYATA + konten layar tak terlihat lensa (tak ada UI yang meleleh; UI tetap di AE/kartu floating bila perlu). A1 tetap terpenuhi karena muka layar tak menghadap kamera. Token: `cool/warm glow from the phone's lit screen onto the face, phone held rear casing toward camera so screen content stays hidden from the lens`.

**🔒 TRIAD ATTACHMENT MANDATORY TIAP FRAME — KARAKTER + LINGKUNGAN + START/END-REF (Erik mandate 2026-06-23, GATE B SEQ1-SC01-SH03).** SETIAP unit generate (START & END) WAJIB melampirkan + menyebut di prompt KETIGA kategori: (1) **KARAKTER** — plat wajah/figur tiap orang dalam frame; (2) **LINGKUNGAN** — plat env (`E01_kamar_*` dst); (3) **START/END-REFERENCE** — plat arah (START) / render anchor (END, `composition_reference`). **MESKI render START/END sudah menampilkan lingkungan, plat lingkungan TETAP WAJIB diattach + disebut** — render anchor saja TIDAK cukup, terutama untuk objek yang DIBERI AKSI (Herman meletakkan HP ke nakas → tanpa plat nakas, model halusinasi permukaan). Bukti: SH03-END "set phone on nightstand" tanpa `E01_kamar_nightstand.png` → permukaan dihalusinasi. Tak ada pengecualian, termasuk END yang di-anchor ke render. Generalisasi dari aturan subjek-wajib di bawah. **ENFORCEMENT WAJIB (pre-emit cross-check):** sebelum frame dinyatakan siap, audit tiap nama di prompt (`identity_reference` per orang, `environment_reference` per objek/ruang) HARUS punya plat ter-attach yang bersesuaian; orang berbaring = plat full/medium (bukan closeup). Nama-tanpa-plat = belum siap. Mencatat aturan ini ≠ menerapkannya — jalankan audit sendiri tiap frame, jangan tunggu user menemukan pelanggaran.

**SUBJEK WAJIB DI PROMPT (LAPIS-3), ATTACHMENT HANYA LAYER-2 (Validated 2026-06-23, GATE B SEQ1-SC01-SH02).** Prompt teks = layer pertama yang dipatuhi model; attachment (reference image) cuma penguat layer-2 — ia TAK BISA menyuntikkan subjek yang tak disebut di prompt. Bukti: SH02-START sempat tanpa token manusia (cuma `subject_anchor` nakas) sambil mengandalkan `lighting_reference` = render pasangan tidur → render keluar KOSONG tanpa orang. Maka: setiap manusia/objek yang harus tampil WAJIB ditulis eksplisit di Lapis-3 (`character_identity...`), apa pun isi attachment. Jangan pernah pakai attachment sebagai pengganti subjek; ia hanya menjaga konsistensi identitas/cahaya untuk subjek yang SUDAH disebut prompt.

**ATTACHMENT-LINE WAJIB DI TIAP UNIT GENERATE (Validated 2026-06-23, GATE B SEQ1-SC01 pilot).** Tiap keyframe yang di-generate harus SATU prompt utuh-mandiri yang membawa SENDIRI baris referensi attachment-nya: `environment_reference` (plat ruangan) + `character_identity.identity_reference` (plat wajah), menyebut nama file plat yang di-attach. Pasangan start/end = DUA prompt utuh terpisah (identik kecuali Lapis-4), masing-masing mengulang baris attachment — JANGAN dipecah jadi "fixed-spec + varian" lalu mengandalkan penggabungan mental; model membaca tiap unit sendiri-sendiri dan tak tahu attachment mana yang diikat bila barisnya hanya ada di blok fixed yang terpisah. SOP plat utuh: `09-environment-sheet/E01-kamar.md` ("COMPLETE copy-paste-ready prompt, zero scaffold, zero combine").

**🔒 ORIENTASI SUBJEK DI KEYFRAME = HANYA DARI PLAT YANG COCOK; FRONTAL MENDOMINASI (Validated 2026-06-23, GATE B SEQ1-SC01-SH03, ≥4 render frontal berulang).** Untuk mengarahkan hadap subjek di keyframe scene, konsekuensi keras PROTOKOL ARAH: (1) **Tak ada plat 3/4** — plat cuma front (0°), profileA (hadap camera-left), profileB (hadap camera-right). Token "three-quarter / 3/4 view" = orientasi tanpa referensi → model jatuh ke frontal. JANGAN tulis "3/4"; pilih front ATAU profil. (2) **Frontal mendominasi** — bila `front_*` ikut di-attach bersama plat profil, output cenderung frontal. Untuk shot PROFIL, **lampirkan plat profil (profileA/B) SAJA, BUANG front**. (3) **Arah hadap cocok sisi objek aksi** — objek di camera-right (mis. nakas) → subjek **profileB** (hadap camera-right); profileA = membelakangi objek camera-right → aksi menjangkau tak ter-render. (4) **Shot frontal tak bisa render aksi menjangkau objek samping** (wajah frontal vs lengan ke samping = konflik → aksi dibuang); pakai profil. (5) **"HP punggung-square-ke-kamera + baca layar" memaksa wajah frontal** — bentrok dengan pose menoleh; untuk subjek profil-membaca pakai **HP edge-ke-lensa, layar miring ke wajah** (konten tak terbaca lensa → A1 aman). (6) Tiap tangan ditetapkan **camera-LEFT/RIGHT**, objek+arah perspektif kamera terukur; NOL token kabur (`near`/`beside`/"3/4"). Bukti: SH03 di-prompt "3/4 toward camera-right" + attach `front_medium`+`profileB` → render frontal terus; fix = profil + `profileB` tunggal.

---

## TEMPLATE LENGKAP — SCENE KARAKTER

```json
{
  "mood": "[direktorial emotional register, photographer anchor]",
  "color_grade": "Roger Deakins palette, lifted blacks medium gray, cyan-teal shadows, clean whites, Kodak 2383 emulation, [midtones token]",
  "style": "photorealistic cinema still, ARRI Alexa Mini LF, Panavision Ultra Primo anamorphic, Kodak 2383 print stock emulation",

  "scene": "[Interior Style Name] — [material token 1], [material token 2], [material token 3], [spatial quality token]",
  "location": "[indoor / outdoor / semi-outdoor]",
  "time_of_day": "[morning / afternoon / evening / night]",
  "atmosphere": "[spatial energy token]",
  "scene_depth": {
    "foreground": "[physical elements 0–2m from lens — props, surfaces, partial objects]",
    "midground": "[primary subject + immediate environment — 2–5m]",
    "background": "[depth, population, atmosphere — 5m+, always describe as populated/alive unless emptiness is intentional]"
  },

  "character_identity": {
    "role": "[kota] [kelas sosial opsional] [deskripsi peran]",
    "ethnicity": "[modern Javanese features / modern Jakartan features]",
    "beauty": "[jelita / cantik / tampan / gagah]",
    "age": "[man/woman N years old]",
    "facial_features": "[kualitas tekstur saja — zero nama warna]",
    "body_features": "[build, posture, bearing]"
  },
  "character_style": {
    "makeup": "[base layer], [feature layer], [finish layer], [1–2 industry technique tokens]",
    "wardrobe": "[fabric], [construction/silhouette designation], [fit], [colorway desaturated]",
    "hair": "[cut + barbering term], [styling technique], [finish]",
    "footwear": "[silhouette], [material], [sole], [branding level]"
  },

  "subject_state": "[static / dynamic / speaking]",
  "action": "[konkret fisik mid-process, present participle chains — tanpa redundansi]",
  "pose": "[industry pose term + gender token jika perlu]",
  "gesture": "[konkret hand/arm position + gender token jika perlu]",
  "expression": "[deskripsi fisik — zero label emosi]",

  // Lapis 5 (on_screen_graphic / graphic_proximity / ui_overlay) DIBATALKAN untuk video — ADDENDUM A1 (00-WORKLOG). Grafis = After Effects, post. Field grafis di bawah dipertahankan HANYA untuk deck still lama.
  // "on_screen_graphic": "[deck-only — Teknik 2 air-composited frosted glass card, teal-cyan accent, pill badge]",
  // "graphic_proximity": "[deck-only — CSS positioning: center-x aligned [device], top edge [N]px above [device screen], width [N]px height [N]px, z-index above [layer] below [layer]]",

  "framing": "[shot size + body anchor tokens]",
  "angle": "[camera position token]",
  "camera": "[lens mm] Panavision Ultra Primo anamorphic, [DOF token]",
  "lighting": "[source 1 primary key], [source 2 secondary fill]",
  "aspect_ratio": "16:9",

  "director": "[name]",
  "directing_style": "[4–6 tokens]",

  "lighting_director": "[name]",
  "lighting_style": "[4–6 tokens]",

  "production_designer": "[film PD name]",
  "production_design_style": "[Interior Style Name]: [4–6 material tokens]",

  "interior_designer": "[interior designer name]",
  "interior_design_style": "[Interior Style Name]: [4–6 spatial tokens]",

  "costume_designer": "[name]",
  "costume_style": "[4–6 tokens]",

  "makeup_artist": "[name]",
  "makeup_style": "[4–6 tokens]"
}
```

---

## TEMPLATE LENGKAP — SCENE BENDA MATI / SUBJECT ANCHOR

```json
{
  "mood": "...",
  "color_grade": "...",
  "style": "...",

  "scene": "...",
  "location": "...",
  "time_of_day": "...",
  "atmosphere": "...",

  "subject_anchor": {
    "primary_subject": "...",
    "subject_material": "...",
    "supporting_objects": "...",
    "human_absence_signal": "..."
  },

  "subject_state": "static",
  "action": "...",

  "framing": "...",
  "composition": "...",
  "angle": "...",
  "camera": "...",
  "lighting": "...",
  "aspect_ratio": "16:9",

  "director": "[name]",
  "directing_style": "[tokens]",
  "lighting_director": "[name]",
  "lighting_style": "[tokens]",
  "production_designer": "[name]",
  "production_design_style": "[Style]: [tokens]",
  "interior_designer": "[name]",
  "interior_design_style": "[Style]: [tokens]"
}
```

---

## LAPIS 1 — GLOBAL ANCHOR

### `mood`
Direktorial emotional register. Industry photography/cinema anchor name wajib.
- `warm directness, forward energy, mid-argument conviction, Annie Leibovitz intimate portrait`
- `intimate observational realism, unhurried natural rhythm, Alfonso Cuarón`
- `clinical stillness, eeriness human absence, fully functional space awaiting, Gregory Crewdson`
- `focused solitary determination, quiet self-direction`
- `professional calm analytical ease, work done well`
- `dignified authority earned presence, unhurried stillness`
- `electric urban energy, person fully alive their city`

### `color_grade`

**STANDAR TONE DECK (MUTLAK, semua 16 scene) — `cool midtones desaturated, cool-dominant zero amber push`.**
Seluruh deck investor memakai SATU grade identik ini. Alasan: scene dievaluasi berdampingan dalam satu deck — variasi midtones antar-scene = inkonsistensi yang langsung terlihat. Acuan visual terkunci: S2 (`S2-karakter-1-ibu-rumah-tangga.png`). String color_grade WAJIB sama persis di setiap scene:
`Roger Deakins palette, lifted blacks medium gray, cyan-teal shadows, clean whites, Kodak 2383 emulation, cool midtones desaturated, cool-dominant zero amber push`

`slightly warmer midtones` dan `neutral cool midtones` **DEPRECATED untuk deck ini** — keduanya menghasilkan drift kuning saat ketemu material/praktis hangat (terbukti S3 malam, S4 siang timber). Jangan dipakai lagi.

Roger Deakins palette wajib. Midtones token satu pilihan saja (referensi historis, deck pakai standar di atas):
- `cool midtones desaturated` — indoor co-working, professional
- `neutral cool midtones` — corporate, professional indoor
- `cool-dominant zero amber push` — push modifier, pasangkan dengan midtones cool/neutral (JANGAN dengan warm)

**BANNED:** `golden`, `amber`, `ochre`, `warm` sebagai standalone descriptor; `slightly warmer midtones` di scene manapun; DUA token temperature dalam satu color_grade.

**WARM token di field LAIN juga drift palette** — `warm ambient bounce`, `warm pool`, `warm diffused canopy light`, `golden pool`, `maximum warm daylight` di `lighting`/`scene_depth` menarik ke kuning meski color_grade sudah cool. Ganti dengan `cool-neutral ambient bounce`, `neutral pool`, `clean cool light pool`, `bright cool daylight`. (Pengecualian aman: `warm directness`/`warm domestic register` di `mood` dan `warm expressive` di `facial_features` — register emosi/ekspresi, bukan warna; terbukti S1/S2 approved tetap cool.)

### `style`
Selalu: `photorealistic cinema still, ARRI Alexa Mini LF, Panavision Ultra Primo anamorphic, Kodak 2383 print stock emulation`

---

## LAPIS 2 — WORLD & SPACE

### `scene`
Format: `[Interior Style Name] — [material token 1], [material token 2], [material token 3]`
Interior Style Name sebagai gestalt anchor, diikuti material tokens konkret.

**BANNED:** label geografis (`Jakarta kitchen`), label etnis (`Javanese interior`), label motif (`batik decor`), nama warna di material

**CRITICAL — scene material pull palette:**
- `exposed brick` + `pendant industrial lamps` → amber/yellow drift wajib override dengan `cool-dominant zero amber push`
- `timber` + `pendant lamps` → warm pull, perlu dikontrol di `color_grade`
- `matte painted concrete` + `recessed LED cool-white` → palette netral, aman untuk semua midtones token

Token library lengkap: [[INTERIOR-DESIGN-REFERENCE]]

### `location`
`indoor` | `outdoor` | `semi-outdoor`

### `time_of_day`
`morning` | `afternoon` | `evening` | `night`

### `atmosphere`
Spatial energy token — suasana ruang, bukan cuaca:
- `lively bustling crowd energy`
- `intimate quiet domestic`
- `dramatic urban pulse`
- `calm professional focus`
- `communal gathering warmth`
- `clinical empty stillness`
- `industrial purposeful hum`
- `corporate controlled precision`
- `focused solitary determination`
- `dignified unhurried presence`
- `electric forward momentum`

**CRITICAL — atmosphere pull on pose:**
- `calm professional focus` → model default ke pose statis
- `electric forward momentum` → model default ke pose dinamis mid-motion
- Pilih atmosphere sesuai energy yang diinginkan, bukan suasana ruang saja

### `scene_depth`
Three depth planes as explicit sub-fields. Mandatory for all scenes with environment, crowd, or background activity.

```json
"scene_depth": {
  "foreground": "[physical elements 0–2m from lens — props, surfaces, partial objects]",
  "midground": "[primary subject + immediate environment — 2–5m]",
  "background": "[depth, population, atmosphere — 5m+]"
}
```

**Rules:**
- `foreground`: physical objects near lens — handlebar, countertop, desk surface, street furniture. Token strings only.
- `midground`: subject + immediate surroundings. Mirror of character_identity context.
- `background`: population density + architectural depth + sky/horizon. Must be explicit — model default is empty/sparse. Always describe as populated/alive unless scene intentionally empty (S0).
- BANNED: negation tokens in any sub-field — describe what IS present, not what is absent.
- BANNED for S0 and S16 — these scenes use subject_anchor, no depth layers needed.

**Validated S6:** `background: dense Jakarta urban street fully populated — 10+ motorcycles and cars mid-traffic, pedestrians on sidewalk, warung signage, low-rise shophouse facades both sides` → eliminated empty-world problem.

---

## LAPIS 3 — SUBJECT (FIXED)

### `character_identity`

**`role`** — format: `[kota] [kelas sosial opsional] [deskripsi peran]`
Environment-agnostic. BANNED: role yang trigger environment (TV presenter, doctor, news anchor).

**`ethnicity`**
- `modern Javanese features` — etnis spesifik
- `modern Jakartan features` — urban city identity
BANNED: `Indonesian features`, `Betawi features`

**`beauty`**
- `jelita` — female middle-class ke atas
- `cantik` — female lower-middle/domestic
- `tampan` — male polished
- `gagah` — male authoritative

**`age`** — satu angka eksplisit, +5 tahun aging bias
Target 35 → tulis `woman 20 years old`

**`facial_features`** — ZERO TOKEN WARNA
Hanya kualitas/tekstur: `luminous complexion`, `healthy glow`, `radiant complexion`, `clear healthy skin`
BANNED: golden, ivory, olive, tan, warm, brown, beige

### `character_style`

**`makeup`** — 3 layer wajib: base + features + finish. Tambah 1–2 industry technique tokens.
- Base: `full-coverage foundation pore-blurring primer seamless blended base`
- Features: `soft contour cheekbones defined arched brows nude satin lipstick peach cream blush`
- Finish: `baked setting powder long-wearing matte finish oil-controlled complexion zero shine`
- Technique: `strobing highlight bridge nose brow bone`, `colour-corrected under-eye`, `baking technique`
BANNED: HD makeup, HD setting powder, makeup tanpa finish layer

**`wardrobe`** — fabric + construction designation + fit + colorway desaturated
- Fabric: `linen-cotton blend`, `oxford cloth`, `matte nylon shell`, `cotton jersey`, `cotton twill`
- Designation: `MA-1 bomber silhouette`, `notched lapel two-button front`, `French tuck`, `OCBD`
- Fit: `slim fit`, `relaxed fit`, `oversized`
- Colorway: `muted slate-grey`, `charcoal grey`, `off-white`, `dark navy`, `faded sage-grey`
BANNED: batik, paisley, ikat, floral, ethnic print, terracotta, ochre, amber, golden

**CRITICAL — garmen tak-dispesifikasi = auto-batik (validated S12 A/B).** Akar masalahnya BUKAN token etnis memaksa batik — melainkan **GAP**: garmen yang terlihat tapi tidak dispesifikasi di `wardrobe` diisi model dengan default kultural (sarung/batik bermotif), dipicu token `Javanese`/`Jakartan`/etnis lain. Bukti: S12 elder, garmen atas dispesifikasi (off-white polos → patuh), garmen bawah KOSONG (→ batik sarung). Setelah garmen bawah dispesifikasi `dark charcoal cotton drawstring trousers, flat plain weave, solid uniform colorway` → motif HILANG total, scene identik selebihnya. **Aturan: SETIAP garmen yang terlihat (atas, bawah, luar, alas kaki) WAJIB dispesifikasi eksplisit dengan token konstruksi afirmatif (fabric + construction + fit + colorway). Token etnis TIDAK override garmen yang sudah eksplisit — spesifikasi afirmatif menekan default kultural.** Jangan koreksi dengan negasi (`no batik`/`no motif` = BANNED); koreksi dengan menspesifikasi garmennya.

**`hair`** — cut + barbering/salon term + finish
- `short textured crop low fade sides, natural parting, matte pomade finish`
- `voluminous bouncy blowout deep side part, shoulder-length, glossy finish`
- `short natural crop low-fade sides, matte finish`

**`footwear`** — silhouette + material + sole + branding level
- `low-profile clean leather sneakers, white rubber cupsole, minimal branding`
- `canvas low-top sneakers rubber toe cap slightly worn, off-white`
- `derby shoes polished leather cap-toe, leather sole`

---

## LAPIS 4 — EVENT & STATE (VARIABLE)

### `subject_state`
`static` | `dynamic` | `speaking`

### `action`
Token konkret fisik, present participle chains. Mid-process wajib — bukan pose statis.
**Tanpa redundansi** — satu chain of micro-physical verbs, tidak perlu diperkuat ulang.
BANNED: abstract state labels, tenses, label narasi di akhir (`making a point, controlled`)

### `pose`
Industry convention terms + gender token jika relevan:
- `contrapposto` — weight one leg, natural S-curve
- `contrapposto weight front leg, feminine hip displacement` — female grounded mid-delivery
- `three-quarter stance body 45 degrees`
- `neutral standing feet shoulder-width`
- `seated upright slight forward lean`
- `both palms flat desk arms locked weight forward`
- `mid-stride contrapposto, back heel lifting` — dynamic walking

**Gender tokens validated:**
- `feminine hip displacement` — natural weight shift female contrapposto
- `feminine wrist tilt` — gesture modifier female

### `gesture`
Concrete hand/arm position tokens + gender token jika relevan.
BANNED: `hands relaxed` tanpa posisi konkret, label narasi di akhir.
- `one hand raised chest height, fingers loosely spread, elbow bent, feminine wrist tilt mid-point` ✅ validated S1

### `expression`
Physical description only. BANNED: `happy`, `confident`, `warm smile`, emotion labels, label narasi.
- `Duchenne smile eyes crinkled outer corners cheeks lifted`
- `closed-mouth soft smile jaw relaxed cheeks slightly lifted`
- `mouth open mid-speech lifted brows animated direct gaze`
- `mouth open mid-vowel, brows slightly lifted, direct gaze camera`
- `focused gaze at screen jaw relaxed slight concentration furrow between brows`

---

## LAPIS 5 — GRAPHIC LAYER (opsional)

### Teknik 1 — Ambient glow
Cahaya layar pada wajah. Tanpa field tambahan.

### Teknik 2 — Floating graphic (on_screen_graphic + graphic_proximity)
Dua field selalu berpasangan.

**WAJIB — teks super UNIK per scene.** `element 1` + `element 2` tidak boleh kembar antar scene. Tiap scene punya pesan investor sendiri (lihat graphic matrix di `08`). Validated S5: awalnya duplikat S1 (`One Account. Every Activity.`), ditolak user → diganti `All-Day Engagement` / `One Integrated Session`. Sebelum lock: cek semua super scene approved, pastikan tidak ada yang sama.

**`on_screen_graphic`:**
```
air-composited superimpose over scene — frosted glass card panel rounded corners semi-transparent white fill subtle inner glow edge soft gaussian blur backdrop — element 1: [konten] clean sans-serif large weight teal-cyan accent color centered — element 2: [badge] pill-shaped badge teal-cyan solid fill white text medium weight centered below element 1 — card panel soft drop shadow layered depth over scene
```

**`graphic_proximity`** — CSS positioning logic wajib:
```
center-x aligned with [anchor device], top edge of card [N]px above top edge of [device screen], card width approximately [N]px, card height approximately [N]px, z-index above [layer below], z-index below [layer above]
```

Pattern tervalidasi S2:
```
center-x aligned with smartphone device, top edge of card 20px above top edge of smartphone screen, card width approximately 280px, card height approximately 100px, z-index above subject hands, z-index below subject face
```

BANNED: `ui_overlay`, `floating_ui`, `screen_ui`, `phone screen facing camera`, pixel offset >80px, arah manusia tanpa anchor+pixel

### Teknik 2b — DUA grafis dalam satu frame (diegetic banner + investor card) — validated S12b
Untuk scene yang butuh memperkuat makna in-world, sah memuat DUA elemen grafis dalam satu `on_screen_graphic` (struktur tidak berubah — tetap satu field `on_screen_graphic` + satu `graphic_proximity`, isinya mendeskripsikan dua objek):
- **Element A — banner notifikasi diegetik** (UI app yang benar-benar dilihat user): gaya push-notification OS, **boleh Bahasa Indonesia** (UI app autentik, bukan super investor), muncul dari tepi atas HP. Contoh tervalidasi S12b: `'Waktu Sholat Tiba' + clock glyph + '12:03'`.
- **Element B — kartu investor frosted** (register Inggris, seperti scene lain): `'Built Around Your Beliefs' / 'Sharia Mode · Opt-In'`.
Kunci agar tidak garble/crowding: **bedakan TIPE visualnya** (banner OS vs frosted card) + **pisahkan posisi** di `graphic_proximity` (banner anchored ke HP, card ke sudut frame). Dua frosted card kembar BANNED (membingungkan + garble). Preseden split bahasa: diegetic ID + investor EN sah berdampingan (S10 dashboard ID + kartu EN, S12b banner ID + kartu EN).

**Layar yang MEMUNGGUNGI kamera → JANGAN embed UI di layar; pakai kartu "screen-preview" floating (validated S14b).** Bila device (tablet/laptop) menghadap subjek sehingga punggungnya ke kamera, memaksa UI di layar fisik (Teknik 3) membuat model memutar device menghadap kamera = posisi tidak natural/terbalik. FIX: tablet/laptop `rear casing toward camera screen facing the [subject]`, lalu isi layar ditampilkan sebagai **kartu floating screen-preview** (rounded-rect menyerupai layar app: thumbnail + progress bar + label) melayang di atas device, dengan asumsi "itulah layar yang kita lihat". Tetap bedakan tipe dari kartu investor agar tidak garble. Validated S14b: tablet membelakangi kamera + kartu `Kelas Kuliner · Modul 3` floating + kartu investor `Skills Become Income` — keduanya bersih.

### Teknik 3 — UI embedded device
Field `ui_overlay` pada device screen. Sah untuk S6/S10/S12/S14.

### Kelemahan recurring — rendering objek mekanis + tangan (WAJIB diantisipasi)
Validated S6 (kurir + sepeda motor):
1. **Stang/spion motor pecah saat dipaksa render layar HP yang menempel di kemudi.** Memaksa `smartphone screen visible/UI visible` di phone-mount stang membuat model menegosiasikan layar + geometri kemudi sekaligus → stang/spion berantakan. FIX: HP `rear casing toward camera screen hidden`; angka/data tampil lewat **kartu grafis di atas HP**, bukan di layar HP. Tambah `simple clean minimal detail` pada stang.
2. **Tangan meleleh di titik kontak dengan objek kecil.** `hand resting near phone mount` / tangan menyentuh HP/objek kecil = model gabung dua geometri rumit → jari ambigu. FIX: jauhkan tangan dari objek kecil — `hand resting relaxed on thigh away from [object]`. Tangan netral (paha/pangkuan) jauh lebih aman daripada tangan yang menyentuh device/grip/spion.
Prinsip umum: kurangi jumlah titik di mana tangan + objek-kecil + permukaan-mekanis bertemu dalam satu frame.
3. **Layar BESAR aman dari melt (validated S10, S11).** Kebalikan dari HP kecil: monitor/wall-display/tablet permukaan luas datar → jari menyentuh layar (`finger touching monitor screen index finger on rising column`) ter-render bersih, tidak ambigu. Untuk scene yang butuh interaksi tangan-layar, pilih layar besar, bukan HP. Bonus: di layar besar, Teknik 3 (dashboard/chart embedded di layar) DAN Teknik 2 (kartu frosted melayang di atas layar) terbaca bersamaan dalam satu frame.

---

## LAPIS 6 — CINEMATIC TECHNICAL

### `framing`
Shot size + body anchor tokens. Full library: [[TOKENS-REFERENCE]]
- `EWS` — extreme wide, subject tiny
- `WS` — full body generous space
- `FS` — full body subject fills
- `MWS` — knees up
- `CS` — mid-thigh up
- `MS` — waist up
- `MCU` — chest/shoulders up
- `CU` — face fills
- `ECU` — single feature

Fullbody: `full body shot, crown to sneaker sole visible, floor visible 15% bottom frame, generous headroom above crown`
Live actor speaking: `medium long shot, full frame knees to head, floor visible bottom edge`
BANNED: `head to toe` (ambigu)

### `angle`
`eye-level` | `eye-level slight low angle` | `low angle worm's eye` | `high angle` | `dutch angle`

**CRITICAL — angle klise tengah BANNED untuk live actor full body.** `subject centered frame` + `eye-level` → komposisi "presenter jalan ke kamera" paling standar, lingkungan terbuang. Wajib off-axis: dorong subjek ke `right-third`/`left-third`, posisikan kamera ke salah satu sisi rendah, biarkan lingkungan (plaza, koridor, garis lampu) menyusut diagonal jadi **leading lines**.
Pattern tervalidasi S3 (full body wide night): `angle: "low angle worm's eye, camera positioned low-left looking up and across plaza, subject right-third, plaza converging diagonal left"` + `framing: "...subject right-third frame, left two-thirds plaza receding to vanishing point, vendor booths and overhead LED strips strong diagonal leading lines"`. Prinsipnya = off-axis S2 diskalakan ke wide shot.

### `camera`
`[lens mm] Panavision Ultra Primo anamorphic, [DOF]`
- 24mm — wide, expansive environment
- 35mm — live actor speaking
- 50mm — character scene standard
- 85mm — tight portrait

### `lighting`
Source + quality tokens. Zero nama warna. Zero negasi.
Outdoor: `diffused canopy daylight from above soft directionless key`
Indoor day: `large fixed-pane window [position] bright diffused daylight primary key`
Indoor corporate: `recessed LED ceiling downlights primary key`
Indoor co-working: `city-facing glass wall diffused daylight primary key, recessed LED ceiling downlights cool-white secondary fill`
Night: `recessed LED strip overhead cool-white primary key, smartphone screen cool secondary uplight`

### Crew pairs (nama + child style) — LAPIS 6 ONLY
Full crew reference: [[CREW-REFERENCE]]

**`director` + `directing_style`**
**`lighting_director` + `lighting_style`** — NOTE: Roger Deakins di color_grade, bukan di sini
**`production_designer` + `production_design_style`** — format: `"[Style Name]: [tokens]"`
**`interior_designer` + `interior_design_style`** — format: `"[Style Name]: [tokens]"`
**`costume_designer` + `costume_style`**
**`makeup_artist` + `makeup_style`**

---

## TEKNIK UI — REFERENSI PER SCENE

| Scene | Teknik | Field |
|---|---|---|
| S2 Ibu RT | Teknik 2 | `on_screen_graphic` + `graphic_proximity` — smartphone |
| S4 Pemuda | Teknik 2 | `on_screen_graphic` + `graphic_proximity` — laptop |
| S6 Kurir | Teknik 3 | `ui_overlay` — phone mount |
| S8 Profesional | Teknik 1 | ambient glow only |
| S10 Pengusaha | Teknik 3 | `ui_overlay` — monitor |
| S12 Tokoh | Teknik 3 | `ui_overlay` — tablet |
| S14 Eksekutif | Teknik 3 | `ui_overlay` — wall display |

---

## FOTOGRAFER & SINEMATOGRAFER ANCHOR (mood + style field)

- `Gregory Crewdson` — S0, scene kosong, interior stillness
- `Annie Leibovitz` — live actor portrait, character shots
- `Steve McCurry` — documentary portrait lokal
- `Roger Deakins` — color grade SEMUA scene (color_grade field)
- `Emmanuel Lubezki` — outdoor/community
- `Bradford Young` — karakter informal, domestic
- `Hoyte van Hoytema` — indoor professional, corporate

---

## BANNED MASTER LIST

**Karakter:**
- `Indonesian` di field apapun
- `TV presenter`, `news anchor`, `doctor` — trigger environment
- `Betawi features`, `Indonesian features`
- Token warna di `facial_features` — golden, ivory, olive, tan, warm, brown, beige
- Rentang usia — pakai satu angka + aging bias
- `cantik jelita` bersamaan

**Wardrobe:**
- Motif labels: batik, paisley, ikat, floral, ethnic print
- Warna saturated: terracotta, ochre, amber, golden
- Wardrobe tanpa fabric + construction detail
- **Garmen terlihat dibiarkan KOSONG/tak-dispesifikasi saat ada token etnis** (Javanese/Jakartan/dll) → model auto-isi batik/sarung bermotif. WAJIB spesifikasi tiap garmen (atas+bawah+luar) dengan token konstruksi afirmatif. Validated S12 A/B.
- Koreksi auto-batik dengan negasi (`no batik`, `no motif`, `without pattern`) — negasi BANNED; koreksi dengan menspesifikasi garmen secara afirmatif.

**Scene:**
- Label geografis: `traditional Indonesian`, `Javanese interior`, `Jakarta kitchen`
- Label etnis: `batik decor`
- `exposed brick` + `pendant industrial lamps` tanpa `cool-dominant zero amber push` di color_grade

**Makeup:**
- `HD makeup`, `HD setting powder`
- Makeup tanpa finish layer

**Token discipline:**
- **NEGASI MUTLAK DILARANG — `no X`, `not X`, `not in frame`, `without X`, `absent X`, `un-`, `non-`, `zero X` (kecuali token finish tervalidasi `zero shine`).** Model membaca negasi sebagai "JANGAN itu, lakukan ini" → mengambil inisiatif sendiri → tidak compliant. **WAJIB tulis POSITIF: deskripsikan apa yang ADA, bukan apa yang absen.** Pola: `tidak berkepala` → `headless`; `no stylized push` → `faithful natural rendering`; `no batik` → spesifikasi garmen afirmatif. **Untuk elemen yang tidak tampak karena framing (mis. sepatu di close-up): HAPUS field-nya, jangan tulis `"not in frame"`** — hanya tulis yang hadir di frame. (Pelajaran 2026-06-19: `"footwear": "not in frame"` di plat Herman = pelanggaran; diperbaiki dengan menghapus field.)
- **KEYWORD-LEAK — bukan hanya `no`/`non`; HINDARI kata apa pun yang kata-dominannya menyeret konsep tak diinginkan.** GPT Image 2 autoregressif: generate progresif token demi token, **tak bisa mundur mengoreksi** — konsep salient terbentuk duluan. Token `light-absorbing` memuat `light` → model berisiko me-render CAHAYA pada objek, lawan dari maksud. Token `low-sheen` memuat `sheen`; `non-reflective` memuat `reflective`. **Pakai token yang akar-katanya sudah benar:** untuk matte gelap → `dry matte hair, velvety matte strands, chalky matte finish` (nol `light`/`sheen`/`reflect`/`non`). Uji tiap token: apakah ada kata yang, bila diambil sendiri, memunculkan hal yang tak diinginkan? Bila ya, ganti. (Koreksi user 2026-06-19.) **Leak juga bersembunyi di FIELD IDENTITAS / semantik-kuat, bukan cuma field gaya:** label seperti `devout Muslim household` di `scene`/`role` menyeret dekor tak diminta (mis. kaligrafi) yang MENIMPA instruksi eksplisit (mis. `wall_art` Hokusai). Lokalisasi lewat material + kelas sosial + objek konkret bernama, JANGAN label identitas/agama. (Validated 2026-06-22, E01-ENV: token `devout Muslim` memunculkan kaligrafi 2× sampai dibuang.)
- **KONSISTENSI — token UNIFORM, bukan gradien (untuk set multi-plat/reference).** Deskripsi gradien/gradasi (`graying temples`, `fade`, `sheen falloff`, `gradient`, peralihan warna/tekstur) di-render BEDA tiap generate → titik inkonsistensi di set yang menuntut wajah/wardrobe konsisten. **Tulis state UNIFORM tunggal & POSITIF:** `uniform <X> throughout`, `even <X> distribution`, `consistent flat <finish>`, `single solid <tone>`. Contoh: `salt-and-pepper graying temples` → `uniformly salt-and-pepper hair, even grey distribution throughout, flat matte finish`. **JANGAN tulis sebagai `no gradient`/`no gradation`** (itu negasi terlarang) — pakai token uniform positif. Kunci terkuat: salin atribut via **reference-image**, bukan dideskripsi ulang. (Pelajaran 2026-06-19: sheen rambut close-up Herman beda dari plat lain karena token gradien.)
- **REFERENCE-IMAGE DERIVATIVE DISCIPLINE — gambar MASTER = sumber kebenaran DETAIL.** Saat membuat turunan dari plate master (sudut lain ruang yang sama; mirror Profile-B karakter): copy blok tetap (Lapis 1–3 & 6) VERBATIM, ubah HANYA variabel sudut (kelompokkan jadi blok `shot`: composition/framing/angle/camera_position/camera_direction/camera/lighting/aspect_ratio), dan upload master sebagai reference-image. **Token turunan WAJIB = irisan persis dengan yang BENAR-BENAR tampil di master — tak kurang, tak lebih.** Lebih = improvisasi (objek tak ada di master muncul); kurang = inkonsistensi (objek master hilang). **Verifikasi tiap objek ke gambar master (zoom/bandingkan) sebelum kunci — jangan dari ingatan/asumsi.** (Validated 2026-06-22, E01-ENV nightstand gagal 3× karena edit token dari asumsi: tambah buku → buang jam → buang ponsel, konvergen saat = persis master.)
- **EXPLICIT ATTACHMENT-POINTER TOKEN — jangan andalkan harness "lihat attachment".** Saat plate dibuat dengan reference-image, sertakan field token bernama yang MENYEBUT file attachment + match-token: `identity_reference` (karakter) / `environment_reference` (ruang), nilai = token strings (BUKAN kalimat), mis. `attached reference plate <file>.png, same room, identical furniture, named artwork, faithful match, new camera only`. Taruh sebagai field awal. Kewajiban harness untuk membaca attachment lemah/tak terjamin tanpa pointer eksplisit ini.
- **ANTI-IMPROVISASI tanpa negasi — enumerasi TERTUTUP.** Untuk mencegah model menambah objek pada permukaan/area, pakai daftar tertutup positif: `bearing only X, Y, and Z` + `otherwise uncluttered surface`/`otherwise empty`. Ini menggantikan `no extra items`/`no books` yang terlarang (negasi). (Validated 2026-06-22, E01-ENV.)
- Kata sambung tanpa fungsi token
- Label emosi di `expression`
- Label narasi di field manapun (`making a point, controlled`, `person mid-sentence making a case`)
- Abstrak tanpa konkret
- Redundansi dalam satu field — token yang bilang hal sama dua kali
- Redundansi lintas field — jika sudah ada di field lain, tidak perlu diulang
- `ui_overlay`, `floating_ui`, `screen_ui` untuk Teknik 2 floating
- `phone screen facing camera` — device screen always faces subject, not camera. Subject faces camera.
- `on_screen_graphic` tanpa `graphic_proximity`
- Pixel offset >80px di graphic_proximity
- `head to toe` (ambigu)
- `hands relaxed` tanpa posisi konkret

**Crew:**
- Nama orang di Lapis 1
- `Roger Deakins` di `lighting_director` (dia di `color_grade`)
- Child style tanpa nama parent
- Token negasi di child style

---

## COLOR GRADE TOKEN LIBRARY

Midtones (pilih SATU midtones-temperature token per scene):
- `slightly warmer midtones` — live actor, warm interior
- `cool midtones desaturated` — indoor co-working, professional, glass wall lighting
- `neutral cool midtones` — corporate, professional indoor

Push modifier (boleh dipasangkan dengan SATU midtones token cool/neutral di atas, JANGAN dengan `slightly warmer midtones`):
- `cool-dominant zero amber push` — outdoor night, string lights present; indoor warm material (brick, timber pendant)

**BANNED — dua token temperature bertabrakan dalam satu `color_grade`.** `slightly warmer midtones` + `cool-dominant zero amber push` bersamaan = warm menang, frame golden (terbukti S3 iterasi-1). Untuk scene malam / material hangat / praktis lampu hangat: pakai `cool midtones desaturated, cool-dominant zero amber push` (acuan konsistensi S2 + S3 approved).

---

## UPDATE LOG

| Tanggal | Perubahan |
|---|---|
| 2026-06-09 | File dibuat — konsolidasi sesi S0–S2 |
| 2026-06-09 | Struktur granular, on_screen_graphic, graphic_proximity CSS positioning |
| 2026-06-09 | facial_features zero warna, wardrobe garment construction, scene design interior tokens |
| 2026-06-09 | Urutan field mood→color_grade→style di atas character_identity |
| 2026-06-10 | 6-layer structure: Lapis 1–6, scene naik ke Lapis 2, footwear field baru |
| 2026-06-10 | location, time_of_day, atmosphere fields baru di Lapis 2 |
| 2026-06-10 | Industry terminology wajib per field: wardrobe designation, barbering terms, makeup techniques |
| 2026-06-10 | Crew pairs di Lapis 6: director, lighting_director, production_designer, costume_designer, makeup_artist |
| 2026-06-10 | interior_designer + interior_design_style field baru di Lapis 6 |
| 2026-06-10 | Token discipline: no conjunctions, no copulas, no negations, adjective-dense C2 English |
| 2026-06-10 | production_design_style + interior_design_style format: `[Style Name]: [tokens]` |
| 2026-06-10 | Validated S4 v2: Geoffrey Bawa + Eugenio Caballero double anchor → significant improvement |
| 2026-06-09 | scene_depth added to Lapis 2 — three sub-fields mandatory all scenes with environment |
| 2026-06-09 | Device screen always faces subject, not camera |
| 2026-06-09 | S6 APPROVED — File: rough-presentation-image/S6-karakter-3-kurir.png |
| 2026-06-10 | S1 iteration lessons: (1) scene material pull palette — exposed brick + pendant lamps → amber drift, fix: matte concrete + recessed LED cool-white + cool-dominant zero amber push. (2) atmosphere token controls pose energy — calm professional focus → statis, electric forward momentum → dinamis. (3) Redundansi dalam satu field = token lemah — satu token kuat tanpa penguat. (4) Gender tokens validated: feminine hip displacement di pose, feminine wrist tilt di gesture. (5) Label narasi di akhir field BANNED — expression dan gesture harus deskripsi fisik murni tanpa label interpretif. (6) Untuk live actor populated environment: scene = komunal/co-working, bukan home office. |
| 2026-06-10 | S2 iteration lessons: (1) `brows lifted` dibaca model sebagai worry/shock — untuk positive surprise wajib anchor Duchenne: `cheeks lifted Duchenne pull, mouth open mid-exhale of delight, eyes crinkling outer corners`. (2) Jangan paksa wajah menoleh ke background figure — reaksi pertama selalu ke device screen. (3) Off-axis angle pattern validated: camera left-of-subject looking right across foreground object + subject right-third frame. (4) Domestic scene warm material + Bradford Young → amber drift wajib dikontrol dengan `cool midtones desaturated, cool-dominant zero amber push`. |
| 2026-06-10 | S3 APPROVED — File: rough-presentation-image/S3-live-actor-transisi-1.png. Iteration lessons: (1) **Angle klise tengah BANNED untuk live actor full body** — `subject centered frame` + eye-level = komposisi presenter standar. Fix off-axis: subject right-third + low-angle camera low-left + lingkungan diagonal leading lines (lihat seksi angle). (2) **DUA token midtones dalam satu `color_grade` BANNED — warm menang.** S3 sempat punya `slightly warmer midtones` + `cool-dominant zero amber push` bersamaan; meski ada cool-dominant, token warm + praktis lampu booth hangat menarik seluruh frame ke golden. Aturan "pilih SATU midtones" itu mutlak. Untuk konsistensi deck antar scene malam/indoor: samakan persis ke `cool midtones desaturated, cool-dominant zero amber push` (acuan S2). (3) **Konsistensi tone lintas-scene di-cek dengan membandingkan langsung ke PNG scene approved sebelumnya**, bukan dinilai per-scene terpisah. |
| 2026-06-10 | **STANDAR TONE DECK ditetapkan + di-rollout ke semua scene belum-tergenerate.** Setelah S4 kembali drift kuning (siang, timber + earth + warm bounce), seluruh color_grade S5–S14 + S17 disamakan ke `cool midtones desaturated, cool-dominant zero amber push`; `slightly warmer midtones` + `neutral cool midtones` di-deprecate untuk deck ini. Token warm di field lain juga dinetralkan (`warm ambient bounce`→`cool-neutral`, `warm pool`/`golden pool`→`neutral/clean cool pool`, S17 `maximum warm`→`maximum bright cool`). Lihat seksi `color_grade` untuk standar mutlak. S17 (penutup) yang tadinya sengaja terhangat ikut di-cool-kan — flag ke user untuk override bila warm arrival beat tetap diinginkan. |
| 2026-06-10 | S4 APPROVED — File: rough-presentation-image/S4-pemuda-komunitas.png (5/16). VALIDATED standar tone deck: cool grade menetralkan timber+earth daytime tanpa golden-drift. Off-axis OTS dua-subjek + ekspresi Duchenne natural (tanpa label naratif) terbukti. Pattern interaksi: kamera over-the-shoulder subjek kedua (foreground soft), subjek utama tajam left-third, low-angle setinggi meja → diagonal non-klise. |
| 2026-06-10 | S5 APPROVED — File: rough-presentation-image/S5-live-actor-transisi-2.png (6/16). Lessons: (1) teks super graphic WAJIB unik per scene — S5 duplikat S1 ditolak, diganti `All-Day Engagement`/`One Integrated Session`. (2) live actor scene wajib populated + dinamis + variatif (open team floor + glass partition 6+ kolega + `electric forward momentum`), bukan workspace solo `calm professional focus`; kontinuitas presenter via wardrobe/face, bukan ruangan. (3) pose natural satu tangan gesturing + feminine tokens, bukan `both palms flat arms locked`. |
| 2026-06-10 | S6 APPROVED — File: rough-presentation-image/S6-karakter-3-kurir.png (7/16). Non-presenter scene direbuild jadi interaksi (kurir serah-terima paket ke pemilik warung, dua orang, off-axis low-angle). Dua kelemahan mekanis recurring divalidasi + masuk seksi "Kelemahan recurring": (1) stang/spion motor pecah saat dipaksa render layar HP → HP rear-casing screen hidden + data via grafis di atas HP + stang `simple clean minimal detail`. (2) tangan meleleh saat menyentuh objek kecil (HP) → jauhkan tangan ke paha (`left hand resting relaxed on left thigh`). |
| 2026-06-10 | S7 APPROVED — File: rough-presentation-image/S7-live-actor-transisi-3.png (8/16). Validasi pola presenter scene: recurring "Modern Professional Workspace" solo divariasikan jadi open breakout floor + glass meeting room 4+ kolega + atmosphere `electric forward momentum`; ekspresi natural (`lips parted post-word, relaxed assured gaze, cheeks lightly lifted`) menggantikan `brows lifted ... — narrative label`. Karakter (MA-1 bomber M) dikunci, hanya environment yang divariasikan. |
| 2026-06-10 | S8 APPROVED — File: rough-presentation-image/S8-karakter-4-profesional-perempuan.png (9/16). Interaksi >1 orang TIDAK harus co-present: wajah kedua di video-call layar laptop sah untuk scene remote/Virtual Office. Angle `eye-level off-axis camera left-of-subject across desk` menggantikan `subject centered frame` klise. Ekspresi & action & midground dibersihkan dari label naratif. |
| 2026-06-10 | S9 APPROVED — File: rough-presentation-image/S9-live-actor-transisi-4.png (10/16). Beat intim MCU tetap boleh off-center tipis (`subject just off-center left` + `eye-level slight three-quarter soft off-axis`) — anti dead-center tanpa kehilangan intimasi. `eyes wide`/`brows slightly lifted` diganti `direct warm gaze, cheeks lightly lifted, relaxed open` (wide-eyes = kaget/artificial). Graphic di MCU pakai acuan frame-relative (`right-third of frame, chest level`), bukan `subject waistline` yang ter-crop. |
| 2026-06-10 | S17b APPROVED (ADDED scene) — File: rough-presentation-image/S17b-live-actor-penutup-perempuan.png (19/19 deck COMPLETE). Closer perempuan = **cermin S17** (subjek kanan + grafis kiri, jendela kanan; S17 sebaliknya) → pasangan bookend M/F seimbang, jalan mid-stride feminin (hip displacement + rapikan rambut) beda dari semua talking-head F sebelumnya. **Pelajaran super (slip saya, dikoreksi): scene companion TIDAK boleh menduplikat super scene pasangannya — wajib MENGUATKAN.** Saya sempat menyalin super S17 verbatim; salah, melanggar aturan unik-per-scene yang saya sendiri kunci. Fix: S17 = pernyataan struktur (`One Ecosystem./One Set of Rules for Everyone`), S17b = payoff manusiawi (`A Place for Everyone./Belonging by Design`) — dua paруh satu penutup. "Sesuaikan untuk konsistensi" = konsisten REGISTER, bukan teks identik. Full-body F: garmen bawah dispesifikasi (trousers match blazer) per rule batik. |
| 2026-06-10 | S17 APPROVED — File: rough-presentation-image/S17-live-actor-penutup.png (18/18 core). Pelajaran S13 (anti-monoton presenter) terkonfirmasi di **full-body**: iter-1 berdiri statis front + subjek-kanan/grafis-kiri = masih kembar pola sebelumnya; fix dengan ubah TIGA serentak — (1) **flip sisi** subjek left-third + grafis right-third, (2) **geser spot** di kantor sama (sudut rak buku → area jendela lantai-ke-langit, lantai oak jadi diagonal leading line), (3) **angle dinamis** jalan mid-stride ke kamera + kamera dari sisi (bukan eye-level front). Hasil closer terasa "arrival" hidup, bukan presenter pajangan. Aturan umum dikunci: tiap live-actor beruntun WAJIB beda sisi + beda spot + beda angle/pose, bukan sekadar geser dari tengah. **S15 & S16 dilepas dari deck** (video-only beats) — deck inti tuntas 18/18. |
| 2026-06-10 | S14b APPROVED (ADDED scene) — File: rough-presentation-image/S14b-ibu-belajar-kuliner.png (17/18). **Mengisi gap representasi** — grep `hijab/jilbab` di seluruh `08` = nol; semua perempuan sebelumnya muda-profesional/tanpa jilbab. S14b = ibu setengah baya berjilbab menengah-bawah belajar masterclass kuliner in-app bersama tetangga untuk mulai usaha (vertikal pendidikan → marketplace). **Anti-klise domestik:** angkat jadi mikro-wirausaha (produk berlabel + dua perempuan belajar aktif), bukan "ibu di dapur". **Jilbab dispesifikasi afirmatif** (`plain jersey hijab neatly pinned muted dusty-blue`) — patuh rule garmen anti-batik; usia ditulis 40 → render setengah-baya pas. **Pelajaran teknis kunci: layar yang MEMUNGGUNGI kamera jangan di-embed UI — pakai kartu screen-preview floating** (iter-1 mencoba UI di layar tablet → tablet kebalik menghadap kamera; iter-2 tablet membelakangi + kartu `Kelas Kuliner · Modul 3` floating + kartu investor `Skills Become Income` = dua grafis beda-tipe, nol garble). |
| 2026-06-10 | S14 APPROVED — File: rough-presentation-image/S14-eksekutif-korporat.png (16/17). Interaksi korporat dua-orang di wall display tervalidasi: eksekutif + kolega membaca peta Indonesia glowing + dashboard angka di layar besar; jari menunjuk layar besar bersih (konsisten S10). Patch pra-generate yang terbukti perlu: buang label naratif (`connection not conquest, satisfaction of a system working as intended`, `expression caught in the moment`, `both witnessing...in real time`, `sharing the frame`) → fisik murni; buang negasi (`no windows`, `no tie`) → afirmatif (`controlled institutional light`, `open collar top button undone`); spesifikasi garmen bawah (`slim-fit charcoal wool suit trousers flat front`) per rule batik; angle default `eye-level slight low angle` → tambah `three-quarter off-axis, camera low-left across conference table` agar meja jadi leading line. |
| 2026-06-10 | S13 APPROVED — File: rough-presentation-image/S13-live-actor-transisi-6.png (15/17). **Off-center saja TIDAK cukup memutus monoton presenter** — iterasi-1 (front-on MCU, eye-level slight-low, tangan terkatup, subjek kiri + grafis kanan) masih terbaca identik dengan S1/S5/S9 (user: "angle & gesture-pose monoton, termasuk letak"). Fix tervalidasi: ubah TIGA hal sekaligus — (1) angle jadi **turn-back portrait** (kamera di sisi subjek, badan three-quarter membelakang ke jendela, kepala menoleh balik ke lensa) bukan front-on lagi; (2) pose **aktif** (contrapposto + tangan fingertips ke lapel + feminine wrist tilt) bukan tangan terkatup statis; (3) **flip komposisi** subjek right-third + grafis left-third (kebalikan default). Longgarkan framing ke MS waist-up agar pose tangan terbaca. Pelajaran: untuk presenter beruntun, variasikan angle+pose+sisi sekaligus, bukan cuma geser subjek sedikit dari tengah. |
| 2026-06-10 | S12b APPROVED (ADDED scene) — File: rough-presentation-image/S12b-tokoh-komunitas-ibadah.png (14/17). **DUA grafis dalam satu frame tervalidasi** — banner notifikasi diegetik ID (`Waktu Sholat Tiba · 12:03`, gaya push-notification dari HP) + kartu investor EN (`Built Around Your Beliefs / Sharia Mode · Opt-In`) keduanya terbaca bersih tanpa garble. Kunci: bedakan TIPE visual (banner OS vs frosted card) + pisahkan posisi (banner→HP, card→sudut frame); dua frosted card kembar dilarang. **Makna devosional/abstrak jangan ditanggung 100% oleh teks** — beri isyarat visual non-teks (tangan elder ke dada + pemuda latar ikut menjeda) supaya frame tidak terbaca "orang cek HP". Sensitivitas: kata `sharia`/`Waktu Sholat` = nama fitur/UI app, BUKAN nama organisasi → tidak melanggar larangan NU/pesantren verbal (larangan spesifik ke nama organisasi keagamaan + 'pesantren', bukan istilah ibadah generik). Scene tambahan = companion beat (S12b setelah S12), divariasikan komposisinya (berdiri/medium vs duduk/OTS) agar tidak monoton. |
| 2026-06-10 | S12 APPROVED — File: rough-presentation-image/S12-tokoh-komunitas.png (13/16). **Eksperimen A/B garmen tak-dispesifikasi → auto-batik (tervalidasi).** Versi-1 (garmen bawah elder kosong di `wardrobe`) → render sarung batik bermotif; versi-2 (garmen bawah dispesifikasi `dark charcoal cotton drawstring trousers, flat plain weave, solid uniform colorway`) → celana polos, motif hilang total, scene identik selebihnya. Akar: GAP garmen + token `Javanese` → model isi default kultural; token etnis TIDAK override garmen yang sudah eksplisit. Aturan dikunci: tiap garmen terlihat WAJIB dispesifikasi afirmatif; jangan koreksi dengan negasi. Juga tervalidasi: off-axis OTS untuk scene interaksi duduk (`camera near young man shoulder looking up`) + tablet face-grid disoftkan (`faces indistinct soft-focus bokeh tiles`) terbaca tanpa melt. |
| 2026-06-10 | S11 APPROVED — File: rough-presentation-image/S11-live-actor-transisi-5.png (12/16). **Presenter full-body di OPEN OPERATIONS FLOOR berpopulasi tervalidasi** — prompt asli S11 masih solo home-office + `focused solitary determination` (langgar standar presenter populated + mandate "lingkungan dinamis"); di-rebuild jadi `Open Analytics Operations Floor` (kolom beton, workbench dual-monitor, glass partition, mezzanine) + `electric forward momentum` + 6+ kolega di workstation + 2 orang baca dashboard di glass wall. Hasil: floor benar-benar hidup, subjek left-third mid-stride off-axis, kartu `Fairness Engine` jernih, kontinuitas karakter M terjaga. Pattern "rebuild solo workspace → populated professional floor" (S5/S7) terbukti lagi; tiap presenter scene WAJIB ruang berbeda + berpopulasi. Ekspresi di-patch pre-emptif: `brows slightly lifted` + label naratif (`arrested motion, held breath before delivery`) → `lips parted mid-word, cheeks lightly lifted, relaxed assured`. |
| 2026-06-10 | S10 APPROVED — File: rough-presentation-image/S10-pengusaha-menengah.png (11/16). **Layar BESAR + jari menyentuh layar AMAN dari melt** — kebalikan kelemahan HP kecil (S6): monitor/wall-display permukaan luas, model render kontak tangan-layar bersih. Teknik 3 (dashboard chart embedded di monitor: bar chart + judul `Pembeli Baru dari Luar Kota` + angka) DAN Teknik 2 (kartu frosted `Rp 4.2M` melayang di atas monitor) terbaca bersamaan dalam satu frame — kombinasi embedded-UI + floating-card valid di layar besar. **Interaksi "dua orang membaca layar sama"** tervalidasi untuk scene B2B/profesional (pengusaha menunjuk data + staf condong dari balik bahu kiri membaca layar yang sama) — beda stakes, satu fokus. Warehouse `industrial purposeful hum` + 2 pekerja background bergerak antar rak = lingkungan kerja hidup, bukan showroom mati. |
| 2026-06-23 | E02 Ruang Keluarga master APPROVED — File: environment-images/E02_ruangkeluarga/E02_ruangkeluarga_master.png. **Universal rule — named-product VERIFIABILITY beats name-presence.** A branded furniture token only locks consistency if its silhouette has a strong, confirmable prior. Weak-silhouette names let t2i improvise the form: `IKEA LACK TV bench` rendered as ambiguous cubes (→ swapped to `IKEA BESTÅ`, low flat-door media cabinet) and a generic `low open shelf` rendered as a plain cabinet (→ pinned to `IKEA KALLAX, 2x2 open square cube grid`). Pick products whose silhouette is **iconic + countable** (KALLAX cubes = count per angle) or **unmistakable** (BESTÅ flat-door), and keep **distinct silhouettes per piece** in one room so two units never blur. **Camera-relative direction for fixed-camera env plates:** abstract spatial relations (`directly opposite`, `facing`) failed 4 renders — sofa/TV kept landing on perpendicular walls; fixed by `camera-LEFT wall` / `camera-RIGHT wall` anchoring (legit for env plates; the left/right ban is character-anatomy only). Also reaffirmed: distinct named public-domain artwork per room (E01 Hokusai Great Wave vs E02 Hokusai Red Fuji) keeps rooms distinct while same house register holds. Token library → `tokens-references/INTERIOR-DESIGN-REFERENCE §6`. |
| 2026-06-23 | E02 audit — TWO universal rules locked. **(1) Enumerate every surface accessory or the model improvises inconsistently.** A featured surface (desk, counter, shelf) left as "object + otherwise uncluttered" gets random fill: the MICKE desk rendered a mouse in one E02 plate, nothing in another, because keyboard/mouse were never named. Fix: spell out every small object on a legible surface as explicit tokens (`slim wireless keyboard, mouse, before the monitor`). Same root as the garment auto-batik gap — any visible unspecified object is filled by the model. **(2) Master = the reference anchor; if the spec gains an object, regenerate the MASTER first, then re-derive dependents.** Derivatives upload the master as reference-image, so a master missing the new object contradicts the updated prompt and reopens improvisation. Add object → regenerate master → re-derive the dependent angles (Erik correction; "regenerate the insert only" was wrong — it ignored the reference chain). Reaffirmed token-per-token (b.119): no `and / for / with / bearing` inside JSON token VALUES — comma-delimited clusters only; surrounding markdown docs may stay prose. |
| 2026-06-23 | **PROVISIONAL (pending render-validation — NOT yet validated)** — E03 Ruang Belajar (Andi, child SD). **Child-room ornaments must be NAMED strong-prior products, not a generic `toy`.** Same verifiability rule as branded furniture (named-product > name-presence): a generic `plain wooden toy` has no stable silhouette → t2i improvises a different object per angle, breaking cross-plate consistency. Use globally iconic, countable toys whose form the model already knows: `LEGO Classic small colourful brick build` + `LEGO brick storage box`, `Rubik's Cube 3x3 colour cube`, `small educational desk globe`, `educational world map poster pinned` (cork pinboard). Wall_art stays the single public-domain framed work (§2.6(7), here Hokusai Kajikazawa); toys live in `supporting_objects`. **Status: applied to E03 spec, awaiting Cell M render — if any named toy renders inaccurate/melts, correct the choice then (Erik: "nanti kalau nggak akurat baru dikoreksi"). Promote to a `(Validated <date>, <evidence>)` rule only after a clean render.** |
| 2026-06-23 | **MANDATORY pre-lock grep audit for placement tokens (enforcement of the camera-relative rule).** The camera-relative direction rule was locked on E02, yet ambiguous placement tokens still leaked into the E03 draft (`beside curtained window`, `pinboard/wall_hook side wall`, `child rug one side`, pronoun `beside it`) — proving the rule needs a mechanical enforcement step, not just a written rule. **Before locking ANY environment doc, grep every placement word — `beside | behind | side wall | one side | next to | opposite | facing | above | below | beside it` — and confirm each hit is anchored to `camera-LEFT/RIGHT/BACK` or a NAMED object (`camera-right of the desk`, `on top of the KALLAX unit`, `centered above the desk`); rewrite any bare/abstract one.** Also catches INTERNAL CONTRADICTIONS across slots (E03: desk slot said window `beside` the desk while window_dressing said `behind the desk` — two slots disagreeing forces improvisation). A pronoun like `beside it` is ambiguous to a t2i model (no referent resolution) — always name the referent. (Validated 2026-06-23, E03 audit — Erik caught `beside`-without-camera; reinforces the E02 camera-relative kebakuan.) |
| 2026-06-23 | **Product-brand names are SAFE and REQUIRED for consistency; only copyrighted CHARACTER / franchise IP trips the content filter → swap REACTIVELY per-token, never de-brand wholesale.** Evidence (E03 master): the first master with IKEA PÅHL/KALLAX + LEGO + Rubik's Cube + Hokusai generated cleanly; generation only FAILED after a named Marvel character token (`Iron Man Mark III`) was added; replacing JUST that token with a generic strong-prior `articulated humanoid robot, red-gold armor` passed. Lesson: do NOT generalise an IP block into "de-brand everything" — that destroys the verifiability the brand names provide (E02: generic `LACK` → random cubes; `KALLAX 2x2` → stable form). Policy: keep all product-brand tokens (IKEA / LEGO / Rubik's / named public-domain art); if a SPECIFIC token is blocked, swap only that one, preferring a named character → generic-but-strong-prior descriptor. The narrow blocked category seen so far = named fictional characters / franchises (Marvel etc.). (Validated 2026-06-23, E03 — Erik corrected my over-broad de-brand framing.) |
| 2026-06-23 | **CORRECTION to the row above — text-level de-brand is NOT sufficient when the model's prior collapses a generic token back onto a copyrighted character; you must change the SUBJECT CATEGORY, not just drop the name.** Evidence (E03): after the `Iron Man` text token was blocked, the de-branded `articulated humanoid robot, red-gold armor` token DID generate a master — but the model still drew an unmistakable Iron-Man-like figure. When that master was uploaded as the reference-image for derivative D, a SECOND, different guardrail fired — image-level `similarity to third-party content` — blocking every derivative (screenshot evidence). So there are TWO guardrails: (1) text-token filter, (2) output/reference image-similarity filter; clearing (1) does not clear (2). Root fix when a silhouette has an overwhelming character prior (armored humanoid → Iron Man): **switch to a subject with NO character ownership — a real animal, a real vehicle, a public-domain object — then it is safe to name a product brand for sculpt-consistency.** E03 resolution: hero figure → `Schleich Tyrannosaurus rex toy figure` (real animal = inherently public-domain subject + Schleich = proven-safe product brand for a specific, consistent sculpt). (VALIDATED 2026-06-23, E03: Schleich T-Rex master generated cleanly AND derivative D generated from it with NO image-similarity block — the exact failure the Iron-Man master caused; subject-category swap confirmed end-to-end. Supersedes the "de-branded robot passed" claim above — that master was rejected to `_rejected/`.) |
