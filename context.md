---
title: Context — Semesta Digital
tags: [meta, context, active-session]
status: active
created: 2026-06-08
updated: 2026-06-10
---

# Context — Sesi Aktif

## State AKHIR Sesi (2026-06-23 · ENV PAUSED → PILOT SEQ1-SC01 AKTIF) — TERBARU
**Keputusan Erik (2026-06-23):** ⏸ **GATE 0-ENV DI-PAUSE setelah E03**. Aktif sekarang = **PILOT SEQ1-SC01** (INT. KAMAR HERMAN, 04.40, contoh kanonik 4-beat) — jalankan SATU scene end-to-end (GATE B keyframe 6-lapis → GATE C Kling 3.0 i2v 5-dtk 1080p audio-on → VO TTS terpisah → grafis A1 di After Effects → assemble) untuk membuktikan workflow sebelum produksi massal. Sukses = pipeline terbukti + PILOT REPORT (apakah dual reference-lock env+wajah bertahan di Kling i2v). Aset hulu siap: **E01 kamar ✅ + Herman ✅**, SH03 sudah punya standar 6-lapis tervalidasi. Reference per-shot menamai file konkret `environment-images/E01_kamar/*` + `character-images/H_herman/*` (Herman satu-satunya tokoh on-screen; sisi Ratna kosong per prosa). Paket: `handoff/HANDOFF-2026-06-23-PILOT-SEQ1-SC01.md` + `INITIAL-PROMPT-2026-06-23-PILOT-SEQ1-SC01.txt`. **E04 Dapur di-HOLD** (handoff sudah dibuat, dieksekusi setelah pilot). Lanjutan env (E04→E06 → luar-rumah + E08) menanti hasil pilot.

## State AKHIR Sesi (2026-06-23 · GATE 0-ENV E03 COMPLETE 4/4)
**E03 Ruang Belajar (Andi, SEQ2-SC03) LENGKAP 4/4** (`environment-images/E03_ruangbelajar/`): master · desk (MS) · tablet (CS insert) · doorway (MWS). Semua dari satu master, token-per-token, arah ber-anchor kamera, A1 screens-off. Doc `09-environment-sheet/E03-ruangbelajar.md` v1.0 COMPLETE. Inherit §3 house anchor; artwork ketiga = Hokusai **Kajikazawa in Kai Province** (distinct dari E01 Great Wave / E02 Red Fuji).
**Kebakuan baru sesi ini (tervalidasi, masuk `prompt-rules` + memory `semesta-env-prompt-craft` — jangan putuskan ulang):**
1. **Ornamen kamar anak = produk bernama prior-kuat** (LEGO build, Rubik's Cube, desk globe, world map), bukan `toy` generik. Rubik's ter-summarize di shot lebar, muncul di insert ketat (T).
2. **DUA guardrail generator:** (a) filter token-teks, (b) filter image-similarity di output/reference. Membersihkan (a) TIDAK membersihkan (b). Iron Man: token diblokir → de-brand `red-gold robot` lolos token TAPI model tetap menggambar likeness Iron-Man → master itu lalu menendang derivatif D di guardrail (b). **Fix: ganti KATEGORI SUBJEK** (humanoid-armor → hewan nyata) = `Schleich Tyrannosaurus rex toy figure` (real animal = inheren public-domain + Schleich = merek produk aman). Tervalidasi end-to-end (master + 4 plate lolos).
3. **Merek PRODUK aman & WAJIB** untuk konsistensi (IKEA/LEGO/Rubik's/Schleich/Hokusai lolos); hanya **karakter/franchise ber-IP** yang kena filter → swap REAKTIF per-token, jangan de-brand menyeluruh.
4. **Grep-audit token arah pra-lock** wajib: `beside|behind|side wall|one side|next to|opposite|facing|above|below|beside it` — tiap hit harus ber-anchor camera-LEFT/RIGHT/BACK atau objek bernama (Erik menangkap `beside curtained window` + kontradiksi `beside`↔`behind` di draf E03).
**NEXT:** E04 Dapur Ratna (SEQ3-SC01, live-selling UMKM) — lanjut home-room block; lalu E05/E06 → luar-rumah + E08 → balik GATE B keyframe SEQ1. Handoff: `handoff/HANDOFF-2026-06-23-ENV-E04-dapur.md`.

## State Sesi (2026-06-21 · GATE B dibuka + GATE 0-ENV berjalan)
**GATE B:** standar shot 6-lapis tervalidasi di SEQ1-SC01-SH03 (6 iterasi): HP punggung-ke-kamera + kartu/grafis di-handle terpisah, angle off-axis anti-cliché, `expression` jadi sub-objek (overall/eyes/brows/mouth/muscles) untuk wajah bangun-tidur, spasial subjek-di-atas-kasur. **Token grade-hangat DIKUNCI** (terverifikasi): `Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones` (hangat hanya dari color_grade; garmen desaturated). Crew video Cuarón/Lubezki/Caballero. Field baru `character_identity.identity_reference` ikat plate↔attachment.
**ADDENDUM A1 (kanonik `00-WORKLOG`):** semua grafis (UI/kartu iklan/grafik/super) DIBATALKAN dari generate AI → digarap After Effects oleh animator; **Lapis 5 dibuang** dari prompt keyframe. Disebar ke `prompt-rules`/`05`/`03`/`lessons`/memory `semesta-no-ai-graphics-addendum.md`.
**GATE 0-ENV:** inventaris **14 environment unik** (E01–E14; 6 ruang rumah berbagi 1 anchor arsitektur + 8 luar-rumah) + metode `09-environment-sheet/00-README-ENV.md` (empty-room, grade netral, scoped-angle bukan 360, **3 anchor wajib**: kelas pemilik + brand INTERNASIONAL register + desainer INTERNASIONAL Caballero/Ilse Crawford + **named public-domain artwork** default Hokusai untuk konsistensi). Folder `environment-images/` + `E01_kamar/` dibuat. **E01 master v3.1 jadi** (compliant: subject_anchor, token library, positive-only, camera-relative + geografi relasional, dua Hokusai).
**Koreksi keras user (terekam, benar):** (1) prompt env awal saya **langgar `prompt-rules`** (negasi `no/NOT`, token non-library framing/angle/camera/lighting, tanpa `subject_anchor`) → diperbaiki, formula contek plate karakter approved (H-herman Cell 1); (2) saya sempat **defeatist** (coret multi-angle env, goal minimal) → SALAH, terbantah 53 plate karakter konsisten; metode benar = **reference-image upload + spec sudut tegas** (cara karakter), bukan text-only (ter-cermin) / bukan "match plate" (klon).
**NEXT:** `bed3q` E01 via reference-image upload master + spec sudut tegas → `wallart`/`nightstand` → kunci E01 + tulis `E01-kamar.md` → rollout E02–E14 → kembali ke GATE B keyframe SEQ1. Tertunda: runtime ≈312s vs 300s; sinkron O4 hilir.

## State AKHIR Sesi (2026-06-21 · GATE 0 CLOSED — figuran 14/14, seluruh GATE 0 LENGKAP)
**Fokus:** Menutup GATE 0 — kelompok figuran. **Figuran SELESAI 14/14** di `character-images/F_<name>/`: Darto 3 (front_full/medium + profileA_medium) · Tika 2 · petugas bank 3 (+front_closeup) · Rian 3 (+front_closeup) · pembina 3. Adaptive plate set (front + profileA saja, **nol Profile B**), uncovered baseline, faith-not-imposed. `F-figurans.md` v0.3 = 14 prompt 6-lapis penuh verbatim (sebelumnya scaffold-placeholder → diperbaiki ke format baku). `00-README` baris figuran = COMPLETE; `00-WORKLOG` entri penutup GATE 0 ditulis.

**SELURUH GATE 0 LENGKAP:** Herman 9 · Ratna 12 · Lisa 9 · Andi 9 · figuran 14.

**Kebakuan baru sesi ini (sudah masuk `lessons.md` + memory `semesta-gate0-character-pipeline.md` — baca, jangan putuskan ulang):**
1. **Karakter terkunci sebagai minor TIDAK boleh diberi token ukuran-bra/bust** (batas perlindungan anak). Tika dikunci 16 → render age-appropriate benar. Untuk siluet dewasa, **re-age karakter ke dewasa dulu** (Tika 16→20, director call) → baru metode body-token Lisa sah (`young womanly build, 34C`).
2. **Render figuran cenderung jatuh ke "wajah generik" yang sama** (saling mirip + mirip main char) bila `facial_features` hanya token positif umum. Fix: token `distinctive-commoner-features` + ciri konkret (bentuk wajah, tekstur rambut, kumis/cambang, tahi lalat, build). Rian & pembina di-regenerate karena mirip tokoh lain.
3. **Body-shape antar perempuan dibedakan via ukuran bra konkret + tinggi + build** (Tika 34C/160 · Lisa 34C/162 · pembina 36D/158 curvy).
4. **Aksesori kacamata DIBUANG** — frame tidak stabil lintas angle di reference-lock; pembeda harus intrinsik (wajah/tubuh/rambut), bukan aksesori dipakai.
5. **Panjang lengan WAJIB eksplisit** di `wardrobe` (`short-sleeve`/`long-sleeve`) — tanpa itu regenerate tidak konsisten.
6. **Peran figuran ikut prosa `03`, bukan dikarang** — Darto = pedagang warung (BUKAN satpam); perannya menyetir beat iklan SEQ2-SC01.
7. **Tiap sel plate = prompt 6-lapis penuh verbatim** (nol scaffold/placeholder), `prompt-rules`:44 + `lessons`:224.

**NEXT: GATE B** — prompt keyframe 6-lapis per shot (grade HANGAT video), plate jadi reference-lock Kling + jangkar prompt. **Paket handoff GATE B SUDAH dibuat:** `handoff/HANDOFF-2026-06-21-GATEB.md` + `INITIAL-PROMPT-2026-06-21-GATEB.txt` (buka sesi baru dengan diskusi DECIDE-FIRST: token grade-hangat + urutan kerja + model pasangan keyframe). **`Herman Model.png` ke-10 SUDAH dihapus user (2026-06-21) — `H_herman/` kini tepat 9 plate.** Carryover tersisa: runtime ~312s vs 300s (putus pangkas-1-shot vs terima 312); sinkron O4 hilir (`04-ad-inventory-map`/deck `11`/tabel `05` masih "15-scene/5-babak"). Total plate GATE 0 = 53.

## State Sesi (2026-06-21 · GATE 0 Andi LENGKAP 9/9)
**Fokus:** Author + validasi character sheet Andi (karakter 4/4 GATE 0, anak laki 10). **Andi SELESAI: 9/9 plat tergenerate, divalidasi, di-rename, di-approve** di `character-images/A_andi/` (Front/ProfileA/ProfileB × full/medium/closeup, uncovered, crop pendek natural). `A-andi.md` v0.1; manifest `00-README` Andi COMPLETE. **Render-age 10 DIKUNCI** (terverifikasi pada plat pertama). 9 plat uncovered saja — SEQ6-SC02 ngaji tanpa peci (per prosa `03` baris 268/276). Nol body-feminization token (anak laki). Makeup `bare child skin` ditulis ulang positif (sumber `07 §3.3` `no makeup` = negasi → `bare healthy child skin … matte finish zero shine`).

**Keputusan dikunci sesi ini (sudah masuk `lessons.md` + memory `semesta-gate0-character-pipeline.md`):**
- **Render-age di bawah usia riil hanya untuk DEWASA; anak = usia riil, nol kompensasi menua (terverifikasi Andi 10).** Herman 50→46, Ratna 45→41, Lisa 20→19 (dewasa, model menuakan). Untuk anak, bias menua tidak muncul — `boy 10 years old` menghasilkan anak ~10 tahun tanpa drift remaja. Kunci di usia riil untuk karakter anak.

**NEXT (sesi figuran):** GATE 0 tinggal `F-figurans.md` (figuran berulang) → entri WORKLOG penutup GATE 0 → GATE B prompt authoring per shot (grade HANGAT video). Diskusi pemilihan figuran mana yang digenerate = agenda berikutnya. Tertunda lama: runtime ~312s vs 300s; file `Herman Model.png` ke-10.

## State Sesi (2026-06-21 · GATE 0 Lisa LENGKAP 9/9)
**Fokus:** Author + validasi character sheet Lisa (karakter 3/4 GATE 0). **Lisa SELESAI: 9/9 plat tergenerate, divalidasi, di-rename, di-approve** di `character-images/L_lisa/` (Front/ProfileA/ProfileB × full/medium/closeup, uncovered, rambut tergerai, body `34C` konsisten). `L-lisa.md` v0.2; manifest `00-README` Lisa COMPLETE; `00-WORKLOG` entri 2026-06-21. **Render-age 19 DIKUNCI** (terverifikasi). 3 frontal awal (body `slim`) di-regenerate ulang dgn `34C` agar satu-tubuh; frontal lama dihapus-ganti.

**Keputusan dikunci sesi ini (sudah masuk `lessons.md` + memory `semesta-gate0-character-pipeline.md`):**
- **Siluet dada feminin di t2i = ukuran bra konkret register fashion, bukan adjektiva abstrak.** `slim/womanly/hourglass/curves/feminine` GAGAL membentuk dada di profil (3× gagal — torso rata/maskulin). BERHASIL: `body_features: "...natural 34C bustline, defined waist and hips..."` + `wardrobe: "fitted crew-neck..."`. Lolos filter karena plat ber-register `commercial stock photography/catalogue`. Hindari kata-merah `breasts/busty/large/cup-lepas/bra`. Eskalasi: ter-filter→34B, kurang→34D. (Detail penuh di lessons.)
- **KONSEKUENSI (SELESAI):** 3 frontal awal (body `slim`) sudah di-regenerate ulang dengan `34C` + `fitted` dan dihapus-ganti → 9 plat kini satu-tubuh konsisten. Tidak ada plat tertunda lagi untuk Lisa.

**NEXT (sesi Andi):** tulis `08-character-sheet/A-andi.md` (anak 10, bare healthy skin, anchor Anissa Salazar hair / Deborah Hopper costume; 4 scene SEQ2-SC03, SEQ4-SC04, SEQ6-SC01/02) + folder `character-images/A_andi/`. Lalu figuran → entri WORKLOG penutup GATE 0 → GATE B prompt authoring per shot (grade HANGAT video). Tertunda lama: runtime ~312s vs 300s; file `Herman Model.png` ke-10.

## State Sesi (2026-06-20 · GATE 0 Ratna LENGKAP 12/12)
**Fokus:** Menulis + memvalidasi character sheet Ratna (karakter 2/4 GATE 0). **Ratna SELESAI penuh: 12/12 plat tergenerate, divalidasi, di-rename, di-approve** di `character-images/R_ratna/` — 9 plat uncovered turnaround (Front/ProfileA/ProfileB × full/medium/closeup, rambut tergerai) + 3 plat hijab reference (front-medium/front-closeup/profileA-medium, voile dusty-teal). Sheet `08-character-sheet/R-ratna.md` v0.3. `00-README` manifest menandai Ratna COMPLETE; `00-WORKLOG` entri 2026-06-20.

**Keputusan dikunci sesi ini (semua sudah masuk `lessons.md` + memory `semesta-gate0-character-pipeline.md` — baca di sesi Lisa, JANGAN diputuskan ulang):**
1. **Sumbu modesty hijabi = PAPARAN-NON-MAHRAM, bukan indoor/outdoor.** Hijab lepas hanya bila yang hadir semua mahram (suami/anak) atau perempuan. Ada mata non-mahram (fisik MAUPUN lewat kamera/siaran) → hijab wajib. Konsekuensi tajam: 2 scene Ratna di RUMAH tetap berhijab (SEQ3-SC01 live-sell tersiar publik; SEQ3-SC02 video-call bank). 3 keadaan: uncovered (SEQ2-SC03, SEQ6-SC01/02) · hijab (SEQ3-SC01/02, SEQ4-SC03, SEQ5-SC02) · mukena (SEQ1-SC02).
2. **Kata "hijabi"/penutup-kepala di `character_identity.role` = keyword-leak** yang memaksa kerudung walau wardrobe kosong (dibaca model paling awal). Plat uncovered pakai `role: modest mature Muslim woman` (nol pemicu); hijab muncul hanya bila token garmen hijab eksplisit ada.
3. **Plat referensi = rambut TERGERAI/terurai, bukan diikat** (kunci identitas rambut penuh). Penataan/pengikatan diserahkan ke keyframe scene GATE B. Berlaku semua karakter berambut tampak. (Koreksi user atas plat Ratna terkuncir.)
4. **Karakter bertutup-kepala = baseline plat uncovered + beberapa plat tertutup REPRESENTATIF** (bukan turnaround penuh). Ratna 9 uncovered + 3 hijab = 12. Lisa tidak berhijab → 9 plat saja.
5. Token negasi di sumber kanonik (`07 §3.2` `no visible strands`) tetap wajib ditulis ulang positif (`hairline fully concealed`) sebelum dipakai.

**Render-age:** Herman 50→46, Ratna 45→41. Lisa (20) = OPEN, rekomendasi ~19, verifikasi pada plat pertama.

**CATATAN GIT:** vault BUKAN git repository — `commit` belum bisa; `git init` = keputusan user yang belum diotorisasi.

**NEXT (sesi Lisa — terpisah):** tulis `08-character-sheet/L-lisa.md` (identitas + 9 prompt plat uncovered + wardrobe 6-scene) + folder `character-images/L_lisa/`. Lisa = mahasiswi+kreator 20, anchor Michael Wilkinson/Judy Chin/Camille Friend, makeup on-camera ready, 6 scene (SEQ2-SC01/04, SEQ3-SC04, SEQ4-SC02, SEQ5-SC01, SEQ6-SC01). Lalu Andi → figuran → GATE B. Lanjut via `handoff/HANDOFF-2026-06-20-LISA.md` + `INITIAL-PROMPT-2026-06-20-LISA.txt`.

## State Sesi (2026-06-19 · GATE B Prep — GATE 0 Herman LENGKAP 9/9)
**Fokus:** O4 sinkron + GATE 0 character sheet. **Herman SELESAI penuh: 9/9 plat tergenerate, divalidasi, di-rename, di-approve** di `character-images/H_herman/` (front/profileA/profileB × full/medium/closeup). Folder `08-character-sheet/` (00-README + H-herman.md). `07-style-reference.md` jadi.

**Aturan token DIKUNCI sesi ini (semua sudah masuk `prompt-rules` + `lessons.md` + memory `semesta-gate0-character-pipeline.md` + `08-character-sheet/00-README` — baca di sesi Ratna, JANGAN diputuskan ulang):**
1. **Multi-angle = 9 gambar terpisah** (3 view × 3 shot), bukan 3-in-frame.
2. **Rasio per-shot:** full body `9:16`, medium `2:3`, close-up `4:5` (GPT Image 2 dukung semua native).
3. **Camera-relative direction** (= screen/frame, audience POV, BUKAN subjek): Profile A = hadap `camera-left`, Profile B = `camera-right`. Profile B digenerate sebagai **mirror Profile A via reference-image upload**. Bandingkan plat **full-res berdampingan** sebelum menilai arah (thumbnail menipu — saya sempat salah-baca).
4. **Positive-only (nol negasi):** jangan `no X`/`not in frame`/`without`; tulis positif atau HAPUS field bila elemen tak tampak (sepatu di close-up → hapus field `footwear`).
5. **Keyword-leak:** hindari kata-dominan yang menyeret konsep tak diinginkan (`light-absorbing`→bocor `light`; `non-reflective`→`reflective`; `low-sheen`→`sheen`). GPT Image 2 autoregressif, tak bisa mundur koreksi.
6. **Uniform, bukan gradien** (di set plat): `salt-and-pepper graying temples` → `uniformly salt-and-pepper hair, even grey distribution throughout`. Larangan ditulis positif, bukan `no gradient`.
7. **MATTE PLATE STANDARD (anti-sheen):** hair `dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural`; lighting `flat even soft diffused three-point studio key … matte skin and hair rendering` (BUANG `high-key` — pemicu specular).
8. **Plat baseline:** scene `plain solid white background, subject isolated` (BUKAN "cyclorama studio" yang memicu ruang); style + token photostock; grade netral true-to-life (warm grade menyusul di keyframe GATE B); render-age 46→50.
9. **Deviasi plat (sah, dideklarasikan):** prime lens (bukan anamorphic), tanpa scene_depth/graphic, crew di-scope ke costume/makeup/hair, rasio potret.

**Alur validasi per plat (disepakati):** user generate → simpan ke `character-images/<TAG>_<char>/` → saya baca + jajarkan full-res + nilai rubrik (rasio/view-arah/identitas/wardrobe/latar/sheen) → user "setuju" → saya rename ke `<TAG>_<char>_<view>_<shot>.png`. Error <5% diterima (mis. sheen close-up Herman). Gagal → `_rejected/`.

**Catatan:** ada file ke-10 `Herman Model.png` di `H_herman/` (di luar 9 kanonik) — belum diklarifikasi user, TIDAK disentuh.

**NEXT (sesi Ratna — terpisah, sesi ini terlalu padat):** tulis `08-character-sheet/R-ratna.md` (identitas + 9 prompt plat penuh + wardrobe per-scene) + buat folder `character-images/R_ratna/`. Ratna = hijabi 45, paling kompleks (uji katalog hijab/modest `07` + hair tertutup Camille Friend + 8 scene). Lalu Lisa/Andi/figuran → entri WORKLOG penutup GATE 0 → GATE B prompt authoring per shot (grade HANGAT). Tertunda: runtime ~312s vs 300s (diajukan saat GATE B).

## State Sesi (2026-06-18 · Rebuild Konsep Cerita Video — sebelumnya)

**Fokus:** Brainstorming rebuild naratif explainer video → konsep "Satu Keluarga, Satu Hari Penuh" untuk audiens ads provider, di folder BARU `explainer-video-2/`.

**Filing baru (dieksekusi):** Folder `explainer-video-2/` dibuat. Isi: `00-INDEX.md` (hub + peta pewarisan), `00-WORKLOG.md` (log proses & keputusan — sumber proses, sinkron memory+session-anchors+scope), `01-storyline.md` (hasil akhir clean-slate, masih kerangka), `02-storyboard.md`/`03-scene-detail.md`/`04-ad-inventory-map.md` (stub). RAB `03`/`03-a`, pipeline `04`/`04-a`, dan aset deck (`08`+19 PNG, `09`, `11`) TIDAK disalin — diwariskan via tautan INDEX (satu sumber kebenaran). `explainer-video/` lama = arsip + rumah aset deck. Pemisahan proses vs hasil: `00-WORKLOG.md` = proses, `01-storyline.md` = hasil clean.

**Keputusan dikunci (2026-06-18, detail di `explainer-video-2/00-WORKLOG.md` Decision Log):**
- Tema: 1 keluarga kelas menengah Jakarta (Herman 50/Ratna 45/Lisa 20/Andi 10), seharian penuh subuh→malam, persinggungan tetangga lintas kelas.
- Usaha Ratna = kuliner rumahan/frozen food (B2C+B2B, resep dari masterclass in-app).
- Struktur: garis-waktu-hari cross-cut; cold-open dibuang; live-actor host dibuang; 5 babak / 15 scene / ~300s.
- Grammar 4-beat: Peristiwa→App UI→Potensi Iklan→Payoff diegetik. Aturan "Bersih Saat Sakral" (frame komersial nol saat ibadah). Contoh kanonik #1 = subuh sarung "Cap Gajah" + grafik saham overnight.
- VO laki-laki tunggal: eksplisit pada MAKNA/tema, implisit pada MEKANIK fitur; larangan "bayangkan" + nama organisasi tetap.
- Peta potensi iklan 15-scene (menanjak: FMCG harian → high-intent → launch-partner); 2 scene sengaja bebas iklan (subuh & ibadah) = bukti brand-safe.

**Pemisahan proses/hasil (dikunci):** file live di-rename → `00-WORKLOG.md` = log proses & keputusan (sumber, sinkron memory+anchors+scope); `01-storyline.md` baru = HASIL akhir clean-slate. Alur: keputusan dicatat di WORKLOG → matang → dituang bersih ke STORYLINE → diterjemah ke 02/03/04/05.

**Pipeline produksi (dikunci → `explainer-video-2/05-pipeline-produksi.md`):** stack keyframe=ChatGPT Image v2, video+audio-adegan=Kling 3.0 i2v start→end. 4 KOREKSI: (1) **narator=trek terpisah** (TTS/VO + mix edit), BUKAN Kling; (2) keyframe per **SEGMEN 5-dtk** berantai (end-N=start-N+1), bukan 2/scene; (3) **grade VIDEO hangat** override cool deck-standard `prompt-rules` b.208; (4) keyframe=**pasangan identity-konsisten** (1 spec tetap Lapis1–3&6 + 2 varian Lapis4 start/end). Siklus 3-gerbang (Detail→Prompt→Keyframe→Storyboard) + tabel status per-scene. Acuan prompt: `prompt-rules-image-generation.md` + `explainer-video/08`.

**Storage gambar:** `explainer-video-2/scene-images/` + subfolder `sc01`–`sc15` + `README.md` (konvensi `sc<NN>_seg<M>_start/end.png`; hanya simpan yang lolos GATE C).

**Struktur folder final `explainer-video-2/`:** `00-INDEX`, `00-WORKLOG`, `01-storyline`, `02-storyboard`, `03-scene-detail`, `04-ad-inventory-map`, `05-pipeline-produksi`, `scene-images/`.

**OPEN:** O1 kebijakan nama brand (rekomendasi: mock realistis; "Cap Gajah" contoh kerja internal saja); O4 dampak hilir ke RAB/pipeline/deck bila scene/durasi final bergeser; token grade hangat video belum ditetapkan (akan dikunci saat scene pertama disusun).

**NEXT:** isi detail Babak 1 (Sc1–Sc2) → catat di `00-WORKLOG.md`, rancang segmentasi 5-dtk, tetapkan token grade hangat video, lalu tuang bersih ke `01-storyline.md`.

**UPDATE SESI 2026-06-19 (GATE B Prep — O4 sinkron + GATE 0 dimulai):** (1) **O4 SELESAI** — `05-pipeline §5` tabel status dibangun ulang ke 19-scene/6-babak; `04-ad-inventory-map` stub diperbaiki (sumber `03`, tiga zona bebas-iklan). **Premis handoff dikoreksi:** deck `explainer-video/11` TIDAK stale — "19 scenes" di situ = deck ilustrasi 19-PNG lama (S0–S17b), bukan 19 scene video; tak perlu diubah. (2) **GATE 0 dimulai** — scope character sheet DIPERLUAS ke 5 dimensi (identitas+makeup+hair+wardrobe+footwear, per `prompt-rules` Lapis-3). File baru: **`07-style-reference.md`** (mewarisi `tokens-references` via link + delta hijab/anak/usia-matang/warm-grade + **anchor hair baru** Anissa Salazar/Camille Friend/Tim Muir + pasangan Lapis-6 `hair_stylist`+`hair_style`). **`08-character-sheet/`** jadi FOLDER per-tokoh (debat: 9 prompt × N tokoh terlalu panjang untuk satu doc): `00-README.md` (metode) + `H-herman.md` SELESAI (identitas FIXED + **9 prompt plat t2i penuh** + wardrobe per-scene). (3) **Koreksi multi-angle (user):** = 9 gambar terpisah/tokoh (3 view × 3 shot), bukan 3-in-frame. **PROTOKOL ARAH t2i** dikunci (model tak andal left/right — bukti arxiv+OpenAI): front/profileA/profileB anatomi + profileB=mirror via reference-image, nol token left/right. (4) Aset plat: `character-images/<TAG>_<char>/` (subfolder per tokoh + `_rejected/` + README), `character-images/H_herman/` dibuat. Semua kebakuan → memory `semesta-gate0-character-pipeline.md` + `lessons.md`. **NEXT:** `R-ratna.md` (uji katalog hijab) → Lisa/Andi/figuran → entri WORKLOG penutup GATE 0 → GATE B prompt authoring per shot. Runtime ~312s vs 300s masih tertunda (diajukan saat GATE B).

**UPDATE AKHIR SESI 2026-06-19 (successor — GATE A LENGKAP):** `03-scene-detail.md` selesai penuh **SEQ1–SEQ6 / 6 babak / 19 scene / 57 shot / ≈312s** (verified grep). Keputusan sesi ini: (1) SEQ3-SC02 diubah B2B→**bank-as-tenant** (Ratna ajukan modal via cabang virtual bank). (2) SEQ4 "Dunia Melebar" — 4 scene **nol jual-beli** (government-as-tenant / masterclass / koperasi-inklusi / edutainment anak). (3) SEQ5 SENJA/PRA-PULANG ditambah (struktur jadi 6 babak; ibadah geser ke SEQ6) — Lisa terminal TransJakarta + Ratna bayar-tagihan PPOB; Andi di rumah, Herman dikecualikan dari transit. (4) SEQ6 MALAM — makan+opt-in syariah → **SC02 ngaji ba'da Maghrib** (Ratna ajari Andi; kitab hardcopy + monitor kitab digital; "Bersih Saat Sakral" = **nol komersial BUKAN nol layar**; sholat Maghrib berjamaah dilepas, Subuh tetap jangkar) → **coda kamar SEQ6-SC03 bookend ke pembuka** (Herman matikan HP grafik saham, pejamkan mata; VO penutup di sini). (5) ADDENDUM PIPELINE: **STEP 0/GATE 0 Character & Wardrobe Sheet** (white-bg multi-angle, plat identitas + katalog wardrobe per-scene; untuk prompt keyframe + reference-locking Kling) → ditulis ke `05`/`02`/`03`/`00-INDEX`; pipeline jadi 4-gerbang. 3 zona bebas-iklan (Subuh sholat, ba'da-Maghrib ngaji [nol komersial, layar hanya kitab digital], coda layar-padam) bingkai film. **OPEN O4 (carryover):** `04-ad-inventory-map`, deck `11`, tabel status `05` masih "15-scene/5-babak" → wajib sinkron ke 19-scene/6-babak sebelum GATE B; runtime ~312s bisa dipangkas 1 shot bila ingin kunci 300s. NEXT: GATE 0 character sheet → GATE B prompt authoring. Lanjut via `handoff/HANDOFF-2026-06-19-GATEA-COMPLETE.md`.

**UPDATE AKHIR SESI 2026-06-19:** Penulisan scene berjalan jauh. Hierarki dikunci jadi Sequence→Scene→Shot (`06-konvensi-naratif.md` kanonik; +aturan camera-bound, interaksi-wajib, penomoran RESET per induk). OPERATING CONTRACT Erik ditanam di `CLAUDE.md` (+memory `semesta-operating-contract.md`). Status `03-scene-detail.md`: **SEQ1 (Subuh) + SEQ2 (Pagi) SELESAI; SEQ3 (Siang) SC01/SC03/SC04 tervalidasi, SC02 PENDING** (usul ubah ke "ruang bank digital" Ratna — kurangi kesan marketplace, munculkan diferensiator bank-as-tenant). SEQ4 (Sore) + SEQ5 (Malam) belum ditulis. Lanjutkan via `handoff/HANDOFF-2026-06-19-SCENES.md` + `INITIAL-PROMPT-2026-06-19-SCENES.txt`.

---

## State Akhir Sesi (2026-06-17 · Riset Kling AI Model & Kredit)

**Fokus:** Riset terverifikasi (web, Priority 3) untuk pipeline video AI — paket Kling mana, model mana, dan kapasitas durasi per subscribe.

**Temuan dikunci (detail di `lessons.md` §Insight Kling AI + memory `semesta-kling-pricing-models.md`):**
- Paket Premier ($64.99/8.000 kredit) = kantong kredit, BUKAN pengunci model. Bisa jalankan 2.6 maupun 3.0.
- Kling 3.0 (GA 5 Feb 2026) = pilihan render final scene karakter; **reference-locking 3–5 gambar = fitur konsistensi karakter yang 2.6 TIDAK punya**. 2.6 = draft murah. Menyerang akar success-rate 50% wajah manusia.
- Tarif 3.0 i2v: 1080p tanpa audio 8 kredit/dtk; **1080p audio-on 12 kredit/dtk** (audio WAJIB per user); 720p tanpa audio 6.
- Kapasitas 1 subscribe Premier audio-on: kotor 666 dtk (~11 mnt); bersih ~433 dtk (~7 mnt) @65%. Kebutuhan riil ~90 dtk → 1 subscribe ~3,7× berlebih; "2× subscribe" = cadangan revisi.
- **Segmen 5 detik = standar produksi** (per-kredit sama dengan 10 dtk, tapi waste per generate-gagal separuh + kontrol keyframe lebih ketat).
- Anchors dibuat eksternal di ChatGPT Image v2; video di Kling via start→end keyframe.

**CAVEAT belum tuntas:** success-rate 50%/65% = benchmark generasi lama → wajib re-benchmark 10–15 generate uji Kling 3.0 sebelum dikunci ke `03-rab-produksi-ai.md`.

**SELESAI dieksekusi (user-approved 2026-06-17):** `03-rab-produksi-ai.md` + `04-pipeline-ai-production.md` SUDAH diperbarui — (a) model strategy 2.6-draft→3.0-final reference-locking, (b) tabel kapasitas audio-on, (c) kalkulasi ulang berbasis detik + segmen-5-detik standar, (d) penanda ⚠️ re-benchmark success rate di 3.0, (e) frontmatter updated 2026-06-17. Total dolar TETAP $130 (Premier ×2) — sengaja tidak diubah tanpa hasil re-benchmark.

**Temuan tambahan (terverifikasi 2026-06-17, sudah di memory + lessons):**
- **Model selector Premier:** 2.5 Turbo / 2.6 / 3.0 semua bisa dipilih, kredit beda per model (per 5s 1080p: ~35 / ~55 / 60 kredit). **Audio bawaan HANYA di 3.0** → video+audio production-ready wajib 3.0.
- **Plafon production-ready/subscribe:** 666 dtk (~11 mnt) teoretis; patokan **~7 menit @65% accept**. Kebutuhan riil ~90 dtk → satu subscribe 4–7× cukup.
- **Keputusan Kling vs Luma Labs: TETAP Kling 3.0.** Luma unggul HDR/grading/spasial/char-reference & lebih murah, tapi kalah di dua kebutuhan inti (tidak ada audio bawaan terintegrasi + render wajah manusia lebih lemah). Luma dicatat sebagai kandidat FALLBACK pengganti Seedance, tidak diadopsi.

**Belum dieksekusi:** re-benchmark success rate Kling 3.0 (10–15 generate uji) sebelum mengunci jumlah subscribe (2× berpotensi turun ke 1×) — tugas sisi user/produksi. **Protokol uji sudah disiapkan: `explainer-video/04-a-kling3-benchmark-protocol.md`** (15 segmen, 5 per karakter K2/K3/K5, rubrik PASS/FAIL 5-kriteria, biaya uji 900 kredit, aturan keputusan ≥65%→1× / 50–64%→2× / <50%→tinjau ulang). User tinggal menjalankan uji + isi tabel log.

---

## State Akhir Sesi (2026-06-10 · S11 Image Generation)

**Fokus:** Generate ilustrasi investor deck satu-per-satu ke `08`, review terhadap `prompt-rules`, approve, simpan PNG.

**Selesai sesi ini (Sesi 11):** S3, S4, S5, S6, S7, S8, S9 approved → **total 10/16** (S0–S9). PNG di `rough-presentation-image/` dengan naming convention.

**Keputusan/standar dikunci sesi ini:**
- STANDAR TONE DECK tunggal: semua color_grade = `cool midtones desaturated, cool-dominant zero amber push` (acuan S2). `slightly warmer`/`neutral cool midtones` DEPRECATED. Token warm di lighting/scene_depth juga dinetralkan. S5–S14+S17 sudah di-rollout.
- Anti dead-center: live actor full body → off-axis third + low-angle; MCU intim → off-center tipis.
- Non-presenter scene → WAJIB interaksi >1 orang (co-present atau remote via layar video-call).
- Presenter scene → environment populated + dinamis + variatif (kontinuitas via wardrobe/face, bukan ruangan).
- Ekspresi fisik murni, no label naratif, no `brows lifted`/`eyes wide` lone (worry) → Duchenne/relaxed.
- Super graphic UNIK per scene.
- Kelemahan mekanis recurring: HP rear-casing screen hidden + grafis di atas HP + stang `simple clean minimal detail`; tangan jauhkan dari objek kecil.

**Status gambar:** APPROVED 14/17 (S0–S12 + S12b). REMAINING 3: S13, S14, S17. SKIP: S15, S16. Deck jadi 17 scene (S12b ADDED). Rule batik dikunci (garmen tak-dispesifikasi + token etnis → auto-batik; spesifikasi afirmatif menekan, koreksi bukan dengan negasi). S12b `S12b-tokoh-komunitas-ibadah.png` = scene tambahan (elder jeda ibadah, fitur sharia opt-in) — DUA grafis satu frame tervalidasi (banner diegetik ID + kartu investor EN); makna abstrak jangan 100% teks (beri isyarat non-teks). Naskah S12b ada di `06-storyline.md` Beat 2b. S13 `S13-live-actor-transisi-6.png` APPROVED (15/17) — turn-back portrait + pose aktif + flip subjek-kanan/grafis-kiri memutus monoton presenter (off-center tipis saja tidak cukup). S14 `S14-eksekutif-korporat.png` + S14b `S14b-ibu-belajar-kuliner.png` APPROVED (17/18). S14b = scene tambahan kedua (ibu berjilbab belajar kuliner-untuk-usaha, mengisi gap representasi hijabi; rule baru: layar memunggungi kamera → kartu screen-preview floating). Deck jadi 18 scene (ADDED: S12b + S14b). **KEPUTUSAN (user-approved 2026-06-10): S15 & S16 DILEPAS dari aset deck — keduanya beat VIDEO saja (post-prod composite + tipografi), bukan ilustrasi. Hanya `08` + scope/context diubah; SEMUA dokumen video (storyboard/brief/pipeline/RAB/charter/storyline) UTUH. Convergence opsional = montase dari 7 PNG karakter, nol generate.** S17 `S17-live-actor-penutup.png` APPROVED → **18/18 ilustrasi inti deck tuntas** (lesson: anti-monoton presenter terkonfirmasi full-body — flip sisi + geser spot + angle dinamis jalan mid-stride). S17b `S17b-live-actor-penutup-perempuan.png` APPROVED → **DECK ILUSTRASI 19/19 SELESAI** (S0–S14 + S12b + S14b + S17 + S17b; S15/S16 video-only). S17b = cermin S17 (bookend M/F); pelajaran: super companion wajib MENGUATKAN bukan duplikat (S17 struktur → S17b payoff manusiawi). Naskah S17b di `06-storyline.md` Beat 5b. **HANDOFF CLAUDE DESIGN SELESAI (2026-06-10):** `handoff/HANDOFF-CLAUDE-DESIGN-2026-06-10.md` (self-contained, upload-via "Upload a doc") + `handoff/INITIAL-PROMPT-CLAUDE-DESIGN-2026-06-10.txt` (paste di chat input). Disesuaikan dengan UI Claude Design (`claude-design-ui.png`): Claude Design TIDAK baca filesystem → manifes 19 gambar kunci-ganda (nama file + deskripsi konten), nol referensi filepath, handoff self-contained (Section 1/2/4 + matrix + one-liner di-embed). **RESCOPED (user-approved 2026-06-10): deck Claude Design ini KHUSUS proposal VISUAL scene-per-scene (lampiran).** Narasi investor + proposal tekstual + finansial = deck TERPISAH yang dibangun nanti, lalu digabung manual user dengan deck visual ini sebagai lampiran. Handoff sekarang = galeri 19 scene urut S0→S17b, satu scene/slide, caption tipis (ID+judul+one-liner), grade cool dipertahankan, satu task: S6 composite kartu Rp 340.000. DIBUANG dari deck ini: peta-nomor-slide, narasi investor, angka/Section 3, ecosystem montage (pindah ke deck naratif). **Proyek ilustrasi: TUNTAS 19/19 + handoff visual Claude Design siap.**

**Deck NARATIF investor (terpisah dari deck visual) — kerangka v1 dibuat 2026-06-10:** `explainer-video/09-narrative-deck-framework.md`. 17 slide grounded ke `Executive Brief` + `Proyeksi NU` (Priority 1, angka real: margin 8–12% vs 15–30%; GMV Y1 0,5–1T→Y4 20–30T; capital USD 88–150jt; NU ~60jt anggota + 30jt diaspora, 28.000 pesantren, struktur 6-tingkat ke dusun; revenue 4-kaki 35-45/20-30/15-25/10-20%; legal 4-lapis RPM + Koperasi Platform; top-3 risk). Deck visual 19-scene = LAMPIRAN deck ini (digabung manual). 3 PLACEHOLDER tersisa (domain user): slide 14 team, slide 15 the ask/nominal, detail finansial unit-economics. CATATAN: di deck INVESTOR, nama NU/Muhammadiyah/bank/pesantren BOLEH disebut (beda dgn VO video publik yang melarangnya). `09` di-upgrade jadi SPEAKER-COPY penuh (14 slide ditulis lengkap dari sumber; slide 14 team / 15 the-ask / unit-econ = `[FILL]`, user SKIP ketiganya). Handoff naratif placeholder-aware dibuat: `handoff/HANDOFF-CLAUDE-DESIGN-NARRATIVE-2026-06-10.md` + `INITIAL-PROMPT-CLAUDE-DESIGN-NARRATIVE-2026-06-10.txt`. Metode: upload `09` + `Executive Brief` + `Proyeksi NU` via "Upload a doc", paste initial-prompt; gambar TIDAK perlu (opsional 3–4 hero). Instruksi tegas: jangan karang angka, slide 14/15 disisakan sebagai placeholder. **REVISI deck visual (2026-06-10):** Claude Design sudah meng-export PDF deck visual (title + 19 scene + caption + S6 card composited, bagus). User minta tiap scene diikuti HALAMAN DETAIL (naskah/storyline). Dibuat: `explainer-video/10-scene-detail-naskah.md` (19 entri: Adegan/Pesan&Super/Naskah-VO[LOCKED|draft]/Poin strategis) untuk DIUPLOAD + `handoff/INITIAL-PROMPT-CLAUDE-DESIGN-VISUAL-REVISE-2026-06-10.txt` (prompt KOREKSI: sisipkan 1 halaman detail setelah tiap scene, jangan rebuild, jangan ubah halaman gambar). Akar masalah: handoff visual lama saya scope "thin caption only" → detail keluar by design. **STATUS: deck visual (19/19 + revisi detail siap) + deck naratif (copy v1 + handoff). Tersisa di sisi user: upload `10`+prompt-revise ke Claude Design; validasi baris VO [draft] di `10`.**

**KOREKSI AUDIENS (2026-06-10):** user mengoreksi — deck presentasi ini untuk **PROVIDER IKLAN**, bukan investor (bukti Priority 1: `01-concept §2` audiens utama = provider iklan, rantai nilai video→provider iklan→brand→biayai pre-dev). Deck investor `09` mis-aimed untuk konteks ini → DIBIARKAN sebagai artefak investor terpisah (jangan dipakai untuk provider iklan). DIBUAT BARU khusus provider iklan: `explainer-video/11-adprovider-deck-framework.md` (15 slide: scale/reach/brand-safe/belonging/high-intent/first-party/why-now/what-we-offer[FILL]) + `handoff/HANDOFF-CLAUDE-DESIGN-ADPROVIDER-2026-06-10.md` + `INITIAL-PROMPT-CLAUDE-DESIGN-ADPROVIDER-2026-06-10.txt`. Register: traffic/inventory/reach BOLEH di deck ini (override larangan `08`); tetap larang bayangkan/revolusi; nada brand-safe/belonging. 1 PLACEHOLDER user: slide 12 commercial offer (CPM/format/pricing — jangan dikarang). Skala dikutip dari Executive Brief + Proyeksi NU. **KOREKSI PERAN (2026-06-10): saya sempat menyerahkan kerja KONTEN (tarik angka dari brief, susun chart) ke Claude Design (agen DESAIN). Salah peran.** Diperbaiki: dibuat SATU dokumen konten FINAL `explainer-video/11-adprovider-deck-content.md` (15 slide, headline+body+visual-spec+speaker, semua angka eksplisit verbatim, slide 12 placeholder commercial). Draf framework lama `11-adprovider-deck-framework.md` DIHAPUS (digantikan). Handoff+initial-prompt ad-provider ditulis ulang jadi **DESIGN-ONLY**: upload HANYA doc konten, jangan upload brief mentah, jangan menulis/menghitung. **2 PELAJARAN dikunci di lessons: (a) cek audiens ke `01-concept §2` dulu; (b) saya=penulis konten, Claude Design=pelayout saja.** Tersisa user: slide 12 commercial offer (CPM/format/terms). (Sesi 12, 2026-06-10. S10 `S10-pengusaha-menengah.png` — lesson: layar besar + jari-di-layar aman dari melt; Teknik 3 dashboard embedded + Teknik 2 floating card terbaca bersamaan; interaksi dua-orang-baca-layar-sama valid B2B. S11 `S11-live-actor-transisi-5.png` — presenter di open operations floor berpopulasi tervalidasi, rebuild solo→populated pattern; ekspresi `brows lifted`+label naratif → fisik non-artificial. S12 di-patch pre-emptif: dead-center→off-axis low-angle OTS, tablet face-grid disoftkan untuk hindari melt.)

**Open items — RESOLVED (user-approved 2026-06-10):** (1) S6 → pertahankan foto bersih, kartu "Rp 340.000" di-composite di tahap Claude Design (overlay datar), jangan regenerate. (2) S17 → cool untuk deck; "warm arrival" disimpan sebagai catatan grading VIDEO di `06-storyline.md`, tidak diterapkan ke deck still.

**Next session:** lanjut generate S10 → S11 → S12 → S13 → S14 → S17. Setelah 16/16 → handoff Claude Design (16 PNG + Section 1–4 `08`).
Handoff sesi ini: `handoff/HANDOFF-2026-06-10-S11.md` + `handoff/INITIAL-PROMPT-2026-06-10-S11.txt`.

---

## State Akhir Sesi (2026-06-09 · Konversi DOCX Format Awam)

**Fokus sesi ini:** Konversi 9 dokumen explainer-video (01, 02, 03, 03-a, 04, 05, 06, 07, 08) ke `.docx` format awam.

**Keputusan user (dikunci):** Pendekatan **Hybrid** — Level 2 (glosarium + framing awam) untuk dokumen eksternal 01/02/03/03-a/08; Level 1 (konversi format bersih) untuk dokumen internal 04/05/06/07. Output ke `explainer-video/docx-export/`.

**Selesai sesi ini:**
- 9/9 `.docx` dihasilkan di `explainer-video/docx-export/`. Verifikasi: nol kebocoran frontmatter; tabel ter-render sebagai tabel Word asli (03: 22 tabel, 03-a: 10, 05: 19).
- Tool: pandoc 3.9.0.2 (`~/.local/bin/pandoc`).
- **Metode Level 2 (penting):** body asli disalin VERBATIM (tabel/angka/struktur tak diubah — patuh scope "jangan ubah substansi"); humanisasi hanya berupa bagian "Panduan Membaca & Glosarium Istilah" yang disisipkan di depan. Bahasa mengikuti dokumen: ID untuk 01/02/03/03-a, EN untuk 08.
- **Catatan 08:** Section 5 (S0–S17, ~960 baris prompt JSON) diperlakukan sebagai lampiran teknis berlabel — humanisasi prompt token-string tidak masuk akal; glosarium menjelaskan Section 1–4 (yang dibaca investor) + cara baca lampiran.

**Tidak ada pekerjaan konversi tertunda.** Semua 9 dokumen tuntas.

---

## State Sesi Sebelumnya (2026-06-09 · RAB Tenaga Ahli + Syuting Live)

**Fokus sesi ini:** Menyusun RAB honor tenaga ahli + RAB syuting live (di luar RAB tools `03` yang sudah ada).

**Selesai sesi ini:**
- **`03-rab-produksi-ai.md` → v3.0** — ditambah Bagian B "Honor Tenaga Ahli" model tiga-lane: Director Rp 25 jt (dikunci user) / Editor-Picture-lock Rp 14 jt / AI Generation Artist Rp 13 jt / Motion Graphics & Finishing Rp 11 jt = **Rp 63 jt**. Rekap dipecah A (tools) + B (honor). Tabel "Tidak Termasuk" diperbarui agar konsisten.
- **`03-a-rab-syuting-live.md` → v2.0** (FILE BARU) — RAB syuting live tier profesional komersial **~Rp 65,5 jt**. Keputusan: set tetap berdandan, BUKAN greenscreen. 1 hari, Jakarta, 2 aktor (P+L), crew komersial ramping, voice/dubbing terpisah ke post.
- **Total produksi keseluruhan: ~Rp 148,3 jt** (tools 19,8 + honor 63 + syuting 65,5).

**Keputusan validated dikunci:**
- Honor model tiga-lane terdiferensiasi (bukan rata).
- Live actor = set tetap, greenscreen ditolak (3 alasan: brief minta set nyata+rack focus; live actor jangkar manusiawi vs dunia AI; compositing manusia ke AI video = VFX berisiko tinggi).
- Tier RAB harus konsisten flagship lintas komponen (koreksi user "terlalu murah" pada draft Rp 34 jt → revisi Rp 65,5 jt).

**Next session (DIMINTA USER):** Konversi 9 dokumen explainer-video (01, 02, 03, 03-a, 04, 05, 06, 07, 08) menjadi `.docx` dengan format penulisan mudah dibaca & dipahami awam. Detail di handoff.

---

## State Sesi Sebelumnya (2026-06-10 · S11 Image Generation)

**Fokus:** Generate ulang seluruh 18 ilustrasi S0–S17 untuk investor deck — reset penuh dari S0.

**Selesai sesi ini:**
- S0 APPROVED — cold open, empty workspace, 4 monitors, human absence signals. File: S0-cold-open.png.png (double extension — perlu rename manual)
- S1 APPROVED — Jakarta co-working, populated background 8+ workers, feminine hip displacement + wrist tilt validated, cool palette. File: S1-live-actor-pembuka.png
- S2 APPROVED — ibu rumah tangga, off-axis angle, countertop foreground, Duchenne expression validated, background figure adult woman. File: S2-karakter-1-ibu-rumah-tangga.png

**Lessons dikunci sesi ini:**
- Scene material pull palette: warm material → amber drift, fix: cool-dominant zero amber push
- Atmosphere token controls pose energy: calm professional focus → statis, electric forward momentum → dinamis
- Redundansi dalam satu field = token lemah
- Gender tokens validated: feminine hip displacement + feminine wrist tilt
- Label narasi di field BANNED
- Live actor → populated environment, bukan home office
- `brows lifted` → model render worry/shock, bukan positive surprise. Wajib anchor Duchenne
- Jangan paksa wajah menoleh ke background figure — reaksi pertama ke device screen
- Off-axis angle pattern validated S2: camera left-of-subject looking right across foreground object
- Domestic warm material + Bradford Young → amber drift, wajib cool-dominant zero amber push

**Status gambar:**
- APPROVED: 5/16 (S0, S1, S2, S3, S4)
- DRAFT: 11/16 (S5–S14, S17)
- SKIP: S15 (post-prod composite), S16 (tipografi)
- STANDAR TONE DECK dikunci: semua color_grade = `cool midtones desaturated, cool-dominant zero amber push`. S5–S14 + S17 sudah di-rollout. S17 warm-closer di-cool-kan (flag override ke user).

**Lessons baru Sesi 11:**
- Angle klise tengah BANNED live actor full body → off-axis right-third + low-angle, lingkungan jadi diagonal leading lines (validated S3)
- DUA token midtones-temperature dalam satu color_grade BANNED → warm menang. Pilih SATU; konsistensi malam/indoor = cool midtones desaturated + cool-dominant zero amber push (acuan S2)
- Konsistensi tone dinilai dengan membandingkan langsung ke PNG scene approved sebelumnya
- Marker APPROVED di `08` wajib diverifikasi terhadap PNG fisik di folder

**File PNG di vault:**
- S0: rough-presentation-image/S0-cold-open.png
- S1: rough-presentation-image/S1-live-actor-pembuka.png
- S2: rough-presentation-image/S2-karakter-1-ibu-rumah-tangga.png
- S3: rough-presentation-image/S3-live-actor-transisi-1.png
- S4: rough-presentation-image/S4-pemuda-komunitas.png

## Next Session
Lanjut generate dari S5. Semua prompt sudah final di `08`. Generate satu per satu, review, approve, simpan PNG.
Urutan: S5 → S6 → S7 → S8 → S9 → S10 → S11 → S12 → S13 → S14 → S17
Setelah 16/16 approved → handoff untuk sesi Claude Design (bangun presentasi deck investor).

Handoff + initial prompt sesi ini:
- `handoff/HANDOFF-2026-06-10-S10.md`
- `handoff/INITIAL-PROMPT-2026-06-10-S10.txt`

## State AKHIR Sesi (2026-06-23 · GATE 0-ENV E02 COMPLETE 4/4) — TERBARU
**E02 Ruang Keluarga LENGKAP 4/4** (`environment-images/E02_ruangkeluarga/`): master · prayer_high (~45° high-angle) · floorseat (tight-MS) · screen (CS, keyboard+mouse verified). Semua v2 dari satu anchor, token-ified. Doc `09-environment-sheet/E02-ruangkeluarga.md` v1.1 manifest 4/4 ✅.
**Kebakuan baru (masuk `prompt-rules` + memory `semesta-env-prompt-craft.md` + `INTERIOR-DESIGN-REFERENCE §6` — jangan putuskan ulang):** (1) named-product VERIFIABILITY > name-presence (KALLAX 2x2 cube countable, BESTÅ flat-door, vs LACK ambiguous); (2) camera-LEFT/RIGHT/BACK untuk env kamera-tetap (abstract opposite/facing gagal 4×); (3) artwork public-domain beda per ruang (E01 Great Wave vs E02 Red Fuji); (4) enumerate setiap aksesori permukaan (keyboard/mouse) atau render inkonsisten; (5) master=anchor → tambah objek = regen master DULU lalu re-derive semua turunan; (6) token-per-token, nol and/for/with di nilai token (b.119); (7) tiga tinggi kamera beda (M eye-level · P ~45° · F low).
**Proses:** 4 attempt master ditolak sebelum v2; E06 tetap pegang meja makan (bukan E02); `_rejected/` dihapus per Erik.
**NEXT:** E03 ruang belajar (Andi, SEQ2-SC03), lanjut home-room block (E03→E06), warisi §3 house anchor; lalu luar-rumah + E08; kembali GATE B keyframe SEQ1. Tertunda: runtime ≈312s vs 300s; sinkron O4 hilir.

## State Sesi (2026-06-23 · PILOT SEQ1-SC01 — GATE B authoring) — TERBARU
GATE 0-ENV PAUSED; jalan PILOT SEQ1-SC01 end-to-end. Doc baru `explainer-video-2/10-gateB-keyframes/SEQ1-SC01.md` + `README.md`. Grade hangat DIKUNCI versi `00-WORKLOG`/`05` (`...Kodak 2383 emulation, slightly warmer midtones`) — versi header `03` (golden-hour+amber, dua token temperatur) DROP, perlu disinkron nanti. SH01 (ECU mata, kucel) + SH02 (CU ponsel, layar OFF/A1) authored sebagai **prompt utuh START/END terpisah**.
**Kebakuan baru (kanonik di `prompt-rules` §Struktur 6 Lapis + README 10-gateB + memory `semesta-image-prompt-craft`):** tiap keyframe = SATU prompt utuh-mandiri yang membawa SENDIRI `environment_reference` + `identity_reference`; start/end = dua prompt utuh terpisah, masing-masing ulang baris attachment; JANGAN pecah fixed-spec+varian. Plus checklist authoring: arah kamera (HP punggung-ke-kamera utk held, top-down layar-OFF utk insert), state kontekstual bangun-tidur (kucel di Lapis-4, identitas tetap dari plate), cahaya layar via lighting bukan layar nyala.
**NEXT:** author SH03 (MCU) + SH04 (MS) pola utuh → user generate keyframe → review face/room → Kling i2v → VO+AE → assemble → PILOT REPORT.

## State Sesi (2026-06-23 · PILOT SEQ1-SC01 — review SH01 + kebakuan keyframe-pair) — TERBARU
8 prompt SEQ1-SC01 authored; SH01-START digenerate 2× (regen) → **ACCEPT** (`Content 1672x941 (1).png`); identity-lock wajah Herman BERTAHAN di keyframe. Dibuat `REVIEW-CHECKLIST.md` (8 kriteria). 
**Kebakuan keyframe baru tervalidasi (kanonik di `prompt-rules` §Struktur 6 Lapis + README 10-gateB + CLAUDE.md §PROMPT-CRAFT SOP + memory `semesta-image-prompt-craft`):** (1) tiap keyframe = prompt utuh-mandiri bawa attachment-line sendiri; (2) **END anchor ke render START** (`composition_reference`=file render START + plat wajah, prompt minimal-change) — jangan generate END dari plat saja (i2v warp); (3) figur-berbaring + env-ref melebar ke MCU (setel token MCU); (4) eyeline over-bed "ke langit-langit" = "ke lensa overhead". SH01-END prompt sudah diubah ke metode anchor. Keputusan desain: SEQ1-SC01 tetap 4 shot (tolak sisip shot langit-langit — pacing + bookend mata-ke-penonton).
**NEXT:** user generate SH01-END (anchor ke render START) → SH02–SH04 → review → Kling i2v → VO+AE → assemble → PILOT REPORT.

## State Sesi (2026-06-23 · PILOT SEQ1-SC01 — SH01+SH02 PAIR COMPLETE) — TERBARU
**Keyframe accepted:** SH01 pair (`sc01_sh01_start/end.png`) + SH02 pair (`sc01_sh02_start/end.png`) — semua subuh-gelap cool-blue, Herman+Ratna di kasur (Lapis-3), identity-lock tahan. **Plat E01 diregen clock-free:** master/bed3q/nightstand ✅ LOCKED; wallart ⏸ deferred (hygiene, tak dipakai). 
**Teknik prompting tervalidasi sesi ini (kanonik di `prompt-rules` + CLAUDE.md §PROMPT-CRAFT SOP + memory):** subjek wajib di Lapis-3 (attachment layer-2 saja); screen-glow = layar ON + HP rear-to-camera; rapat figur-berbaring pakai CU/ECU bukan MCU; eyeline over-bed cek kamera (diagonal→langit-langit); istilah kultural English-prior vs token-lokal-niche; improvisasi=celah prompt→enumerasi tertutup+match jumlah objek kanon; subuh=very-low-key cool-blue di lighting; END anchor ke render START; regen hanya bila target visual berubah; two-char key simetris husband/wife.
**🔒 TRIAD ATTACHMENT MANDATORY (Erik 2026-06-23):** tiap frame WAJIB attach+sebut karakter + lingkungan + start/end-ref — plat lingkungan tetap wajib walau render anchor sudah menampilkan ruang (anchor saja → halusinasi objek-beraksi; bukti SH03-END nakas). Kanonik: `prompt-rules` + CLAUDE.md + memory + banner SEQ1-SC01.
**Arc kamar SEQ1-SC01 (direvisi dinamis 2026-06-23):** SH01 rebah→mata bangun · SH02 siku+HP · SH03 duduk-tepi nonton HP→END letakkan HP ke nakas · SH04 bangkit berdiri→END rack-focus ke Ratna bangun duduk→cut. Sarung DIBUANG dari kamar (wardrobe konsisten tee+celana panjang kolor); payoff sarung pindah ke scene sholat. Accepted: SH01✅✅ SH02✅✅ SH03-START✅.
**NEXT:** generate SH03-END → SH04 START/END → Kling i2v → VO+AE → assemble → PILOT REPORT.

## Sisipan lintas-sesi (2026-06-24 · TOOLING prompt-audit — TIDAK mengubah scope/mandat PILOT)
*Catatan untuk agent sesi lain (mis. yang sedang menggarap GATE 0-ENV/PILOT): infrastruktur baru, bukan pergeseran scope. Pakai otomatis saat ter-trigger.*
- **Gate proses baru — audit pre-lock WAJIB sebelum kunci/generate prompt t2i** (plat GATE 0 / keyframe GATE B). Sumber aturan: `explainer-video-2/PROMPT-AUDIT-CHECKLIST.md` (52 item A–L, MEK=grep vs MATA=cek render, tiap baris ber-jejak baris-bukti). Kanonik di `CLAUDE.md` §PROMPT-CRAFT SOP (butir PRE-LOCK AUDIT GATE).
- **Dua skill proyek aktif** di `.claude/skills/` — menyala otomatis saat ter-trigger pasca-restart (project skills auto-discovered tiap sesi): **`/tti-prompt-audit`** (`<path>`|paste-JSON → 9 grep MEK + walk MATA + verdict COMPLIANT/BELUM); **`/tti-prompt-creator`** (tulis prompt 6-lapis untuk satu shot → LOOP dengan audit sampai COMPLIANT; research-before-dispatch@entry · brave/loop@engine · anti-sycophancy@honesty-gate; MATA render-dependent = PENDING post-render).
- **Aturan token baru (kanonik di `prompt-rules`):** kata-hubung antar-token (`and/but/or/with/for/plus/bearing`) → koma; pertahankan `of` + preposisi spasial intra-token (`toward/above/below/from/to/into/over/against/on`).
- **Sharing tim:** skill aktif di `.claude/` TAK ter-share git (`.gitignore:9`); mirror reference ter-track di `skills-reference/` (5 skill + README, header provenance, re-sync manual, source-of-truth = file asal).
