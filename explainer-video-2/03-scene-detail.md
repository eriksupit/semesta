---
title: Scene Detail — Explainer Video 2 (Satu Keluarga, Satu Hari Penuh)
tags: [explainer-video-2, scene-detail, naskah, vo, adegan-prosa]
status: draft
created: 2026-06-18
updated: 2026-06-19
aliases: [ev2-03-scene-detail]
---

# Scene Detail — Explainer Video 2

> Hierarki **Sequence → Scene → Shot** mengikuti `06-konvensi-naratif.md` (kanonik). Tiap scene = 1 lokasi + 1 waktu, ditulis prosa, grammar 4-beat (**Peristiwa → App UI → Potensi Iklan → Payoff**) + VO bila checkpoint makna (D5 `00-WORKLOG.md`). Aturan "Bersih Saat Sakral" berlaku. 1 shot = 1 setup kamera = 1 keyframe-pair. Ini GATE A; prompt 6-lapis penuh di GATE B. Tiap **shot** = satu target prompt t2i (keyframe-pair); sebelum GATE B, dibuat **character sheet (GATE 0)** — plat identitas white-background multi-angle + katalog wardrobe per-scene — sebagai pemandu konsistensi wajah/wardrobe (lihat `05-pipeline-produksi.md`).

## GRADE HANGAT VIDEO (dikunci di sini — standar untuk semua frame video)
Override cool deck-standard `prompt-rules` b.208. String `color_grade` standar video:
`Roger Deakins palette, lifted blacks medium gray, warm golden-hour midtones, gentle amber dawn highlights, clean whites, Kodak 2383 emulation`
> Hangat di sini DISENGAJA (mood domestik/keluarga). Larangan token lain tetap: tanpa negasi, tanpa label emosi, tiap garmen dispesifikasi afirmatif (anti auto-batik), tanpa nama organisasi.

---

# SEQ1 — SUBUH (≈40 detik · 2 scene / 8 shot)
**Pesan sequence:** hari dimulai sama untuk semua orang; sistem yang adil tahu kapan menawarkan dan kapan diam. *(Konvensi SEQ/SC/SH: `06-konvensi-naratif.md`.)*

> Tiap **scene** = 1 lokasi + 1 waktu, ditulis sebagai **skenario prosa** (waktu, lokasi, aksi, dinamika, isi ruang). Di bawahnya **daftar shot** (1 shot = 1 setup kamera = 1 keyframe-pair/segmen 5dtk) + **Catatan produksi**.

---

> **ADDENDUM A1 (2026-06-21, `00-WORKLOG`):** semua elemen grafis di shot-list & prosa di seluruh dokumen ini — UI app, kartu iklan/notifikasi (`Waktu Subuh`, kartu sarung), grafik saham, super text — **TIDAK digenerate AI**. AI hanya render scene murni (device tampil, layar netral/mati, framing comp-aware); grafis digarap di After Effects oleh animator. Beat "App UI/Potensi Iklan" diwujudkan di POST.

## SEQ1-SC01 — INT. KAMAR HERMAN — 04.40 WIB *(waking sequence · 7-shot multi-angle CUT grammar)*
1. Sepasang mata terbuka. Kelopak mata Herman mengerjap di keremangan; pandangnya menemukan langit-langit.
2. Di nakas, layar ponselnya menyala sendiri: pengingat **`Waktu Subuh · 04.42`**, dan tepat di bawahnya sebuah kartu tipis menggeser masuk — iklan sarung tenun ("Cap Gajah"), bersahaja, seperti pas dengan momennya. Ibu jarinya menyentuh layar.
3. Herman meraih ponsel, lalu meletakkannya kembali di nakas — masih berbaring, tenang.
4. Dilihat dari belakang ranjang, tangannya menjangkau saklar lampu nakas; cahaya hangat menyala, mengisi kamar yang tadinya gelap.
5. Di sisinya Ratna terjaga oleh cahaya, perlahan bangun dan duduk, menoleh ke arah Herman.
6. Herman bangkit berdiri di tepi ranjang, menengok kembali ke Ratna.
7. Ratna membalas dengan senyum tenang — awal hari yang sama, untuk mereka berdua.

**VO (laki-laki, tenang):** *"Satu hari dimulai. Hari yang sama — untuk semua orang."*

**Shot list** *(within-shot: angle+framing LOCKED, hanya subjek berubah START→END; between-shot: CUT shot-reverse-shot di poros ranjang, right-diag `bed3q` ↔ left-diag `bed4q`; lampu ON mulai SH04-END → SH05–SH07 lebih hangat)*
> **STATUS PRODUKSI (per 2026-06-29 · update penanda ini tiap shot selesai):** SH01 ✅ DONE (start+end). SH02 ✅ DONE (start+end). SH03 ✅ DONE (start+end). SH04 ✅ DONE (start+end, 2026-06-29). SH05–SH07 ⬜ BELUM. Penanda lama "(DONE — accepted)" = sisa sesi 2026-06-26 yang file-nya tak ada di disk → dikoreksi & diregenerasi ulang.

- **SEQ1-SC01-SH01** — *overhead · ECU/CU mata · 85mm.* start: mata terpejam di keremangan. end: mata terbuka, fokus ke langit-langit. *(✅ DONE — start+end accepted 2026-06-29 · `sc01_sh01_{start,end}.png` · master-parent + edit-in-place)*
- **SEQ1-SC01-SH02** — *top-down · CU macro ponsel di nakas.* start: layar menyala, `Waktu Subuh 04.42` + kartu iklan sarung di bawahnya (layar OFF di render, UI di AE — A1). end: tangan meraih & menggenggam HP (pre-lift, bridge ke SH03). *(✅ DONE — start+end accepted 2026-06-29 · `sc01_sh02_{start,end}.png`)*
- **SEQ1-SC01-SH03** — *right-diag `bed3q` · medium.* start: Herman berbaring memegang ponsel. end: ia meletakkan ponsel kembali di nakas — **tetap berbaring** (bangkit-duduk di-elide di cut). *(✅ DONE — start+end accepted 2026-06-29b · `sc01_sh03_{start,end}.png`)*
- **SEQ1-SC01-SH04** — *near-window vantage · H+R REAR-VIEW / side-back.* start: pasangan dilihat dari belakang, kamar gelap, Herman baru menaruh ponsel di nakas (rebah). end: Herman **bangkit duduk** & **lampu nakas menyala**, cahaya hangat mengisi kamar. *(✅ DONE — start+end accepted 2026-06-29 · `sc01_sh04_{start,end}.png` · METODE: rear-view + prior-frame pose-anchor [render sebelumnya = `current_scene_reference` beat] + rear plate H/R + master untuk handedness + "real camera move, not mirror" — **`E01_kamar_bed4q.png` TIDAK dipakai** (plate foot-vantage menampilkan wajah, melawan intent rear; lihat [[10-gateB-keyframes/SEQ1-SC01]] SH04). END = sit-up + lamp-on (per baris 41) via EDIT-IN-PLACE pada `sc01_sh04_start.png`; prompt START + END verbatim tercatat di [[10-gateB-keyframes/SEQ1-SC01]].)*
- **SEQ1-SC01-SH05** — *left-diag `bed4q` · long · H+R rear-view fullbody.* start: Ratna masih berbaring, Herman duduk membelakangi. end: Ratna bangun, **duduk**, menoleh ke Herman. *(⬜ BELUM · grade ← SH04-END)*
- **SEQ1-SC01-SH06** — *right-diag `bed3q` · long · wajah H+R terlihat.* start: Herman duduk di tepi ranjang, Ratna duduk di belakang. end: Herman **berdiri**, menengok kembali ke Ratna. *(⬜ BELUM · grade ← SH05-END · angle berubah → fresh master, bukan edit-in-place)*
- **SEQ1-SC01-SH07** — *right-diag `bed3q` · close · Herman blur FG / Ratna fokus BG.* start: Ratna menatap Herman, ekspresi netral. end: Ratna **tersenyum** tenang. *(⬜ BELUM · grade ← SH06-END)*

**— Catatan produksi:** *Potensi iklan* — Surface: kartu apparel + pengingat subuh di layar ponsel (SH02). Momen intent: persiapan ibadah (apparel). Kategori: apparel muslim/sarung. Sarung/berdiri-kenakan-sarung + sholat-prep **DIDEFERENSI** ke scene hilir (bukan lagi di SC01). Grade pre-dawn gelap SH01–SH04-START → hangat lampu-nyala SH04-END–SH07; identitas Herman+Ratna dikunci (plat DAG baru). `E01_kamar_bed4q.png` (mirror `bed3q`) = dependensi keras SH04–SH05.

---

## SEQ1-SC02 — INT. RUANG KELUARGA — 04.43 WIB
Di luar jendela masih gelap pekat — subuh Indonesia, matahari baru terbit nyaris dua jam lagi. Ratna menekan saklar; lampu ruang menyala, dan **berbarengan dengan itu layar desktop all-in-one di meja samping ikut bangun dari sleep** — menampilkan browser lapak online-nya: daftar pesanan yang masuk semalam menumpuk, dan di pojok sebuah kartu iklan kecil pemasok kemasan. Ratna meliriknya, senyum tipis — rezeki sudah mengetuk sebelum pagi — lalu memunggunginya untuk bersiap. Herman muncul di ambang pintu, sarung dan peci terpasang, menggelar sajadah; layar desktop kini terabaikan, meredup di latar. Keluarga berkumpul membentuk saf; Herman maju sebagai imam. Sejenak hening. Takbir pertama diangkat. Sejak titik ini tak ada satu pun layar, notifikasi, atau iklan dalam frame: ruang sepenuhnya milik keluarga yang khusyuk sholat berjamaah. Sistem yang tadi menawarkan sarung, angka pasar, dan pesanan dagang kini tahu diri untuk diam.

**Shot list**
- **SEQ1-SC02-SH01** — WS ruang keluarga, jendela gelap. start: ruang gelap, Ratna meraih saklar. end: lampu menyala + layar desktop all-in-one (generik, tak-bermerek) bangun dari sleep menampilkan browser lapak Ratna (pesanan semalam + kartu iklan kemasan); Ratna melirik, senyum tipis. *(35mm · layar besar, aman dari melt)*
- **SEQ1-SC02-SH02** — MS. start: Ratna memunggungi layar, Herman menggelar sajadah (desktop meredup di latar). end: keluarga berkumpul membentuk saf di belakangnya. *(payoff: sarung yang diiklankan dipakai imam)*
- **SEQ1-SC02-SH03** — WS. **Berdiri bersedekap (qiyam) ditahan**, empat orang satu saf-imam. start: qiyam, kamera eye-level frontal-off-axis. end: qiyam (pose identik), kamera soft high-angle ~45°. *(zona sakral — nol grafis · beda angle saja)*

> **Catatan revisi 2026-06-24 (Erik):** SH04 (sujud) DIHAPUS; SH03 disederhanakan dari "takbir→ruku" ke "qiyam bersedekap ditahan, START→END beda angle saja". SEQ1-SC02 jadi **3 shot**. Alasan: i2v sulit menerjemahkan gerak rukuk/sujud serempak 4 orang. Keyframe → [[10-gateB-keyframes/SEQ1-SC02]].

**— Catatan produksi:** *Potensi iklan* (SH01 saja, pra-sakral) — Surface: browser lapak Ratna di layar desktop + kartu iklan pemasok kemasan/bahan. Momen intent: pelaku UMKM cek pesanan semalam. Kategori: marketplace/UMKM · kemasan · e-wallet. *(Teaser vertikal Ratna; kerja penuh B2C/B2B di SEQ3.)* **Bersih Saat Sakral** sejak SH02 (sajadah) → NOL grafis. VO senyap. Lampu interior, jendela gelap (subuh); identitas + wardrobe keluarga dikunci. *(Lisa & Andi di saf = perkenalan tipis; sosok penuh di SEQ2-SC03/SC04.)*

---

# SEQ2 — PAGI / BERANGKAT (≈55 detik · 4 scene / 11 shot)
**Pesan sequence:** satu kompleks, banyak kelas dan profesi, semua bergerak di aplikasi yang sama dengan aturan yang sama. *(Konvensi: `06-konvensi-naratif.md`.)*

---

## SEQ2-SC01 — EXT. GERBANG KOMPLEKS — 06.45 WIB
Matahari sudah naik. Gerbang kompleks perumahan menengah-bawah: pos satpam kecil, paving retak, pohon mangga di tepi. **Lisa, 20 tahun**, ransel di punggung, keluar menuju kampus. Di depan pos, Pak Darto pemilik warung menata dagangan; ponselnya berbunyi — pesanan masuk lewat aplikasi, ia tersenyum mengecek layar. Lisa menyapanya, lalu membuka aplikasi di ponselnya sendiri dan memesan transport; konfirmasi tukang ojek muncul di layar. Sebuah SUV mengkilap pelan melintas keluar; di belakang kemudi, seorang tetangga kelas atas menutup panggilan kerja di layar mobil — aplikasi yang sama, antarmuka yang sama. Lisa dan Pak Darto bertukar senyum; SUV membunyikan klakson tipis, ramah. Tiga kelas, satu gerbang, satu pagi.

**VO (laki-laki):** *"Di gerbang yang sama, jalan masing-masing berbeda — tapi aturannya satu."*

**Shot list**
- **SEQ2-SC01-SH01** — WS gerbang. start: Lisa keluar dari gang, ransel di punggung, gerbang & pos satpam terbingkai. end: ia melangkah ke arah pos, kompleks hidup di latar (tetangga menyapu, anak sekolah lewat). *(24mm)*
- **SEQ2-SC01-SH02** — MS Lisa & Pak Darto. start: Pak Darto menata dagangan, ponselnya menampilkan notifikasi pesanan dari aplikasi. end: Lisa menyapa, layar ponselnya sendiri menampilkan konfirmasi pesan-transport. *(35mm)*
- **SEQ2-SC01-SH03** — MS SUV melintas. start: SUV pelan keluar, kaca turun. end: tetangga kelas atas menutup panggilan di layar dalam mobil (UI aplikasi sama), bertukar angguk dengan Lisa & Pak Darto. *(35mm)*

**— Catatan produksi:** *Potensi iklan* — Surface: notifikasi pesanan di ponsel Pak Darto + pesan-transport di ponsel Lisa + antarmuka aplikasi di layar mobil. Momen intent: transaksi & mobilitas pagi, konteks lintas-kelas. Kategori: transport / e-wallet / telco / kampanye publik. *Payoff:* aplikasi yang sama dipakai tiga kelas berbeda dalam satu gerbang — bukti "aturan satu". Anchor = Lisa (bukan Herman). Grade hangat; kompleks pertama kali tampil di sini.

---

## SEQ2-SC02 — INT. KANTOR EKSPOR-IMPOR — 08.30 WIB
Ruang kerja kantor ekspor-impor, sibuk tenang: meja-meja, monitor, peta rute pengiriman di dinding. Herman duduk di mejanya, membuka **ruang kerja virtual** di aplikasi — dokumen, jadwal kontainer, dan kanal koordinasi tim muncul rapi dalam satu papan. Seorang rekan menghampiri, menunjuk satu baris di layar; Herman mengangguk, menggeser kartu tugas. Kerja yang biasanya berserak di banyak alat, kini di satu tempat.

**Shot list**
- **SEQ2-SC02-SH01** — MS Herman di meja. start: ia membuka laptop. end: layar menampilkan papan ruang-kerja virtual (dokumen + jadwal kontainer + kanal tim). *(50mm)*
- **SEQ2-SC02-SH02** — OTS rekan kerja. start: rekan menunjuk satu baris di layar. end: Herman menggeser kartu tugas, keduanya membaca papan yang sama. *(50mm)*

**— Catatan produksi:** *Potensi iklan* — Surface: placement di papan ruang kerja (mis. layanan bank/B2B, logistik). Momen intent: keputusan kerja/korporat. Kategori: bank / layanan B2B / logistik. Layar besar (aman dari melt); Teknik 3 embedded UI di layar (`prompt-rules`). Grade hangat.

---

## SEQ2-SC03 — INT. RUANG BELAJAR RUMAH — 08.30 WIB *(cross-cut dengan SEQ2-SC02)*
Sudut belajar di rumah: meja kecil, dinding tempel poster, cahaya pagi dari jendela. Andi, 10 tahun, seragam SD rapi, duduk di depan tablet — **kelas daring** sedang berlangsung, wajah guru dan teman-temannya dalam kotak-kotak kecil, papan pelajaran di layar. Andi mengangkat tangan, menjawab; di layar muncul tanda apresiasi — bintang kecil "Jawaban Tepat". Ratna masuk membawa nampan, menaruh segelas susu di samping anaknya, mengusap kepalanya sekilas; Andi nyengir tanpa lepas dari layar. Belajar dari rumah, sungguh-sungguh — dan ditemani.

**Shot list**
- **SEQ2-SC03-SH01** — MS Andi + tablet. start: Andi menyimak, kotak kelas daring di layar. end: ia mengangkat tangan, menjawab. *(50mm)*
- **SEQ2-SC03-SH02** — CU layar tablet (kartu floating bila layar membelakangi). start: papan pelajaran. end: tanda apresiasi "Jawaban Tepat" + bintang muncul (sponsor modul). *(Teknik 2/2b `prompt-rules`)*
- **SEQ2-SC03-SH03** — MWS. start: Ratna masuk membawa nampan, menaruh susu di samping Andi. end: ia mengusap kepala Andi, anak itu nyengir; keduanya satu frame hangat. *(50mm)*

**— Catatan produksi:** *Potensi iklan* — Surface: sponsor modul belajar + tanda apresiasi + kartu di sisi kelas daring + segelas susu (placement nutrisi). Momen intent: keluarga + edukasi. Kategori: edtech / nutrisi anak / ATK. Cross-cut SEQ2-SC02↔SC03 (ayah kerja / anak belajar, jam sama, lokasi beda). Andi diperkuat (3 shot, + momen hangat dgn Ratna). Grade hangat; layar tablet besar aman.

---

## SEQ2-SC04 — INT. KAFE — 10.00 WIB
Kafe kecil dekat kampus, ramai-santai: kopi, kabel laptop, obrolan rendah. Lisa, 20 tahun, di meja sudut dekat jendela, menyimak **kuliah daring** di laptop sambil menulis catatan. Kelas berakhir — ia menutup jendela kuliah, lalu membuka **modul "belajar bisnis"** di aplikasi yang sama, membaca sebentar dengan tertarik. Baru setelah itu, dalam jeda, ia mengangkat ponsel dan **merekam klip pendek** merangkum yang baru ia pelajari untuk audiensnya — ia content creator. Kuliah, ilmu, dan karya, berurutan dari satu meja kafe.

**Shot list**
- **SEQ2-SC04-SH01** — MWS Lisa di meja jendela. start: ia menyimak kuliah daring di laptop. end: ia menulis catatan, layar kuliah masih berlangsung. *(35mm)*
- **SEQ2-SC04-SH02** — OTS ke layar laptop. start: jendela kuliah ditutup (kelas selesai). end: ia membuka modul "belajar bisnis" di aplikasi yang sama, membaca. *(50mm)*
- **SEQ2-SC04-SH03** — MCU Lisa merekam klip. start: kelas sudah usai, ia mengangkat ponsel mulai bicara ke kamera. end: senyum tipis, menekan stop, melihat hasil. *(50mm)*

**— Catatan produksi:** *Potensi iklan* — Surface: sponsored content di kanal Lisa + venue kafe + modul belajar. Momen intent: gaya hidup, niat beli, skill→penghasilan. Kategori: lifestyle / gadget / F&B / edu-fintech. Grade hangat; background kafe hidup.

---

# SEQ3 — SIANG / PUNCAK AKTIVITAS (≈70 detik · 4 scene / 14 shot)
**Pesan sequence:** aktivitas ekonomi keluarga memuncak — jual-beli, kerja, investasi, belajar — semua tertampung satu aplikasi dengan aturan main yang sama. *(Konvensi: `06-konvensi-naratif.md`.)* Ratna jadi bintang sequence ini (vertikal marketplace penuhnya).

---

## SEQ3-SC01 — INT. DAPUR RUMAH RATNA — 11.00 WIB *(marketplace B2C · live-selling)*
Dapur rumah, terang oleh siang. Ratna, celemek terpasang, menghadap ponsel yang terpasang di tripod kecil — ia sedang **siaran jualan langsung** frozen food-nya. Ia mengangkat sepiring risoles ke kamera, bicara ramah; di layar, **komentar dan pesanan pembeli** dari berbagai daerah mengalir masuk real-time, ikon "pesan" bermunculan. Di sisinya, **Tika — tetangga dewasa muda** yang ia bayar paruh waktu — sigap mengemas pesanan yang masuk ke box berlabel, sesekali menyebut jumlah ke Ratna. Saat satu pesanan ditutup, notifikasi **pembayaran dompet digital** masuk. Dapur kecil, pasar seluas layar.

**Shot list**
- **SEQ3-SC01-SH01** — MS Ratna live. start: ia mengangkat piring risoles ke ponsel di tripod, bicara ke kamera. end: komentar/pesanan pembeli mengalir di layar. *(50mm · interaksi: audiens live lintas-daerah)*
- **SEQ3-SC01-SH02** — OTS Ratna & Tika. start: Tika membaca pesanan masuk di layar. end: ia mengemas ke box, menyebut jumlah ke Ratna (interaksi lintas-generasi). *(50mm)*
- **SEQ3-SC01-SH03** — CU layar ponsel. start: aliran komentar + slot pesanan. end: kartu iklan pemasok kemasan lewat tipis di pojok. *(Teknik 2/2b)*
- **SEQ3-SC01-SH04** — CU tangan/layar. start: pembayaran dompet digital masuk. end: saldo bertambah, Ratna & Tika bertukar senyum. *(payoff B2C)*

**— Catatan produksi:** *Potensi iklan* — Surface: live-shopping (slot produk, pin pesanan) + kartu pemasok kemasan + dompet digital. Momen intent: detik beli saat live. Kategori: FMCG bahan/kemasan · e-wallet · live-commerce. Interaksi: audiens live (lintas-daerah/demografi) + Tika dewasa muda (lintas-generasi: Ratna 45 / Tika 20). 4-beat: live → pesanan masuk → iklan kemasan → bayar. Grade hangat siang.

---

## SEQ3-SC02 — INT. SUDUT KERJA RUMAH RATNA — 13.00 WIB *(virtual office · bank-as-tenant)*
Sudut kerja di rumah Ratna, siang terang. Siaran jualan sudah usai; box pesanan tertumpuk rapi di belakang. Ratna duduk menghadap layar all-in-one, mengusap dahi — pesanan membludak, ia perlu modal menaikkan kapasitas produksi. Ia membuka **cabang virtual sebuah bank di dalam aplikasi** — kantor bank yang hadir sebagai tenant di ruang yang sama dengan lapaknya tadi, lengkap dengan ruang tunggu digital dan tombol "bicara dengan petugas". Ia menekan, dan **panggilan video dengan petugas bank** tersambung: di layar, seorang petugas berpakaian rapi menyapa ramah dari mejanya di cabang. Ratna menjelaskan usahanya, menunjukkan riwayat transaksi yang otomatis tertarik dari lapaknya; petugas menatap data yang sama di sisinya, menjelaskan opsi modal usaha. Di pojok layar, kartu produk pembiayaan UMKM tergeser masuk halus. Ratna mengangguk, menekan "ajukan"; status berubah jadi "diproses". Tanpa antre, tanpa keluar rumah — bank datang ke ruang kerjanya.

**Shot list**
- **SEQ3-SC02-SH01** — MS Ratna di meja kerja. start: ia mengusap dahi di samping tumpukan box, membuka aplikasi. end: layar menampilkan pintu cabang virtual bank (tenant) + tombol "bicara dengan petugas". *(50mm · layar besar aman dari melt)*
- **SEQ3-SC02-SH02** — OTS Ratna ke layar. start: panggilan video tersambung, petugas bank menyapa dari mejanya. end: Ratna menjelaskan usaha, riwayat transaksi lapak tertarik otomatis di layar (interaksi lintas-kelas via video). *(50mm)*
- **SEQ3-SC02-SH03** — CU layar. start: petugas memaparkan opsi modal, kartu produk pembiayaan UMKM tergeser masuk di pojok. end: Ratna menekan "ajukan", status berubah "diproses". *(payoff: akses modal dari rumah · Teknik 3 embedded UI)*
- **SEQ3-SC02-SH04** — MS Ratna. start: panggilan ditutup, ia bersandar lega menatap layar. end: ia berbalik ke tumpukan box, siap produksi lebih besar. *(35mm · payoff diegetik: modal → kapasitas naik)*

**— Catatan produksi:** *Potensi iklan* — Surface: ruang cabang virtual bank (tenant) + kartu produk pembiayaan UMKM + riwayat transaksi sebagai data underwriting. Momen intent: butuh modal usaha, keputusan finansial. Kategori: bank / fintech-lending / layanan keuangan UMKM. **Diferensiator bank-as-tenant / virtual office** ditampilkan konkret pertama kali di sini (mengimbangi berat-marketplace SEQ3). Interaksi: Ratna (UMKM) ↔ petugas bank (profesional) via video — lintas-kelas. Nama bank generik/mock. 4-beat: butuh modal → buka cabang virtual di app → kartu produk pembiayaan → pengajuan diproses. Layar besar aman. Grade hangat siang.

---

## SEQ3-SC03 — INT. KANTOR EKSPOR-IMPOR — 12.30 WIB *(financial trading, sela kerja)*
Jam istirahat di kantor. Herman membuka **modul trading di aplikasi** — grafik saham bergerak pelan, posisi miliknya tampil rapi. **Rian, kolega muda**, lewat membawa kopi, melongok penasaran ke layar dan bertanya pelan. Herman menunjuk grafik, menjelaskan singkat caranya menahan diri — bukan mengejar, hanya keputusan terukur; ia menekan satu order kecil, konfirmasi muncul. Rian mengangguk, mencatat di benaknya. Herman menutup modul, keduanya kembali bekerja. Ilmu yang ditularkan di sela tugas.

**Shot list**
- **SEQ3-SC03-SH01** — MCU Herman + layar. start: ia membuka modul trading, grafik + posisinya tampil. end: Rian melongok dari sisi, bertanya. *(50mm · interaksi lintas-generasi)*
- **SEQ3-SC03-SH02** — OTS Rian ke layar. start: Herman menunjuk grafik, menjelaskan disiplin (anti-judi). end: ia menekan satu order, konfirmasi + kartu iklan sekuritas/fintech muncul. *(payoff: keputusan investasi terukur)*
- **SEQ3-SC03-SH03** — MS dua orang. start: Rian mengangguk paham. end: keduanya kembali ke pekerjaan masing-masing. *(35mm)*

**— Catatan produksi:** *Potensi iklan* — Surface: placement di modul trading. Momen intent: keputusan investasi. Kategori: sekuritas / fintech. Nada: terkelola & tenang (anti-judi). Interaksi: Herman menularkan ke kolega muda Rian (lintas-generasi). Layar besar aman. Grade hangat.

---

## SEQ3-SC04 — INT. RUANG KERJA BERSAMA (COWORKING) — 14.00 WIB *(Lisa MENGAJAR jadi kreator)*
Ruang kerja bersama dekat kampus, terang dan rapi. Lisa berdiri di depan layar besar, **memandu workshop kecil: "Jadi Kreator & Jualan Lewat Konten"**. Di hadapannya peserta campur — **dua ibu-ibu pelaku UMKM berjilbab dan beberapa anak muda** — menyimak sambil membuka aplikasi di gawai masing-masing. Lisa mendemonstrasikan di layar: cara membuat etalase, merekam konten singkat, dan menautkannya ke marketplace. Salah satu ibu mengangkat tangan bertanya; Lisa menghampiri, menunjukkan langsung di ponsel ibu itu hingga etalase pertamanya tayang. Yang muda mengajari yang lebih senior; ilmu berputar.

**Shot list**
- **SEQ3-SC04-SH01** — WS ruang. start: Lisa memandu di depan layar besar, peserta campur menyimak. end: layar menampilkan langkah membuat etalase + konten. *(35mm · interaksi: kelas lintas-usia/kelas)*
- **SEQ3-SC04-SH02** — MS Lisa & peserta. start: seorang ibu UMKM mengangkat tangan bertanya. end: Lisa menghampiri, menunjuk langsung di ponsel ibu itu. *(50mm)*
- **SEQ3-SC04-SH03** — OTS ke ponsel ibu. start: etalase/konten ibu itu disusun bersama Lisa. end: etalase pertamanya tayang + tertaut marketplace; ibu itu sumringah. *(payoff: ilmu Lisa jadi usaha orang lain)*

**— Catatan produksi:** *Potensi iklan* — Surface: sponsor workshop/masterclass + alat kreator + etalase marketplace. Momen intent: skill→usaha (milik peserta). Kategori: edu-fintech · marketplace · gadget/alat kreator. Interaksi: Lisa (muda) mengajar ibu-ibu UMKM + anak muda (lintas-usia, lintas-kelas). Lisa naik dari murid → guru. Grade hangat; coworking hidup di latar.

---

# SEQ4 — SORE / DUNIA MELEBAR (≈65 detik · 4 scene / 12 shot)
**Pesan sequence:** hari melandai dan aktivitas bergeser dari dagang ke **layanan publik, ilmu, dan komunitas** — superapp menampung jauh lebih dari jual-beli, dan aturannya tetap satu untuk semua. *(Konvensi: `06-konvensi-naratif.md`.)* SEQ4 sengaja **nol transaksi dagang** (marketplace sudah penuh di SEQ3); tiap scene mengangkat satu vertikal non-dagang di lingkaran sosial masing-masing tokoh.

---

## SEQ4-SC01 — INT. KANTOR EKSPOR-IMPOR — 16.00 WIB *(virtual office · government-as-tenant)*
Sore di kantor, cahaya jingga miring lewat jendela. Herman di mejanya membuka **loket virtual sebuah kantor layanan publik yang hadir sebagai tenant di aplikasi** — bukan menjual apa pun, melainkan mengurus dokumen izin ekspor yang biasanya menuntut antre berjam-jam. Ia menekan "ajukan dokumen", dan **panggilan video dengan petugas instansi** tersambung: petugas berseragam rapi memeriksa berkas yang sudah tertarik otomatis di layarnya, mengangguk, membubuhkan verifikasi. Di samping Herman, rekan kerjanya mencondong, menunjuk satu baris status di papan yang sama; keduanya membaca layar yang identik. Status berubah jadi "terverifikasi". Urusan negara, selesai dari meja sendiri.

**VO (laki-laki, tenang):** *"Sore menjelang. Yang dulu menuntut antre dan perantara — kini cukup dari satu meja, dengan aturan yang sama untuk siapa pun."*

**Shot list**
- **SEQ4-SC01-SH01** — MS Herman di meja. start: cahaya sore, ia membuka aplikasi. end: layar menampilkan loket virtual instansi layanan publik (tenant) + tombol "ajukan dokumen". *(50mm · layar besar aman dari melt)*
- **SEQ4-SC01-SH02** — OTS Herman ke layar. start: panggilan video tersambung, petugas instansi menyapa, berkas tertarik otomatis. end: petugas membubuhkan verifikasi, status bergerak. *(50mm · interaksi lintas-kelas: warga ↔ aparat via layar)*
- **SEQ4-SC01-SH03** — MS Herman + rekan. start: rekan mencondong menunjuk baris status di papan yang sama. end: status "terverifikasi", keduanya mengangguk. *(35mm · payoff: layanan publik tanpa antre)*

**— Catatan produksi:** *Potensi iklan* — Surface: ruang loket instansi (tenant) + kartu layanan/kampanye publik di papan. Momen intent: urusan administrasi/legal. Kategori: kampanye layanan publik · B2B legal/compliance · logistik ekspor. **Diferensiator lembaga-pemerintah-as-tenant** ditampilkan pertama kali di sini. Interaksi: Herman ↔ petugas (via layar) + rekan (tatap muka). Nama instansi generik/mock. Grade hangat sore (jingga miring).

---

## SEQ4-SC02 — INT. RUANG KOMUNITAS KREATOR — 16.30 WIB *(edukasi · masterclass, Lisa kembali jadi murid)*
Ruang komunitas kreator dekat kampus, terang sore. Lisa duduk di antara sederet anak muda menghadap layar besar — **kelas masterclass langsung** sedang berjalan, seorang mentor memandu dari layar, memaparkan teknik bercerita untuk konten. Lisa menyimak serius, sesekali mencoba langkah di gawainya mengikuti instruksi; di SEQ3 ia yang mengajar, di sini ia kembali jadi murid pada tingkat lebih tinggi. Seorang peserta di sebelahnya bertanya, Lisa menoleh, mereka berdiskusi pelan membandingkan catatan. Ilmu tidak berhenti — ia berputar naik.

**Shot list**
- **SEQ4-SC02-SH01** — WS ruang komunitas. start: mentor memandu di layar besar, peserta kreator menyimak. end: kamera menemukan Lisa di antara mereka, menyimak serius. *(35mm · interaksi: kelas + mentor via layar)*
- **SEQ4-SC02-SH02** — MS Lisa + peserta sebelah. start: peserta bertanya, Lisa menoleh. end: keduanya berdiskusi membandingkan catatan (lintas-peer). *(50mm)*
- **SEQ4-SC02-SH03** — OTS ke gawai Lisa. start: ia mencoba langkah mengikuti modul masterclass. end: tanda progres modul muncul + sponsor modul tipis di sisi. *(50mm · payoff: murid→guru→murid lagi, ilmu berputar)*

**— Catatan produksi:** *Potensi iklan* — Surface: sponsor modul masterclass + alat kreator + venue komunitas. Momen intent: pengembangan skill. Kategori: edtech/masterclass · gawai-kreator · lifestyle. Bukan jual-beli — konsumsi ilmu. Interaksi lintas-peer + mentor via layar. Lisa = simpul "ilmu berputar". Grade hangat sore.

---

## SEQ4-SC03 — INT. BALAI WARGA — 16.45 WIB *(komunitas · koperasi & inklusi finansial)*
Balai warga sederhana, kursi plastik melingkar, sore teduh. Ratna duduk bersama ibu-ibu tetangga — **pertemuan komunitas/koperasi warga**. Bukan menjual: mereka mengelola **iuran dan tabungan bersama lewat fitur komunitas di aplikasi**, dasbor transparan menampilkan saldo kelompok yang bisa dilihat semua anggota. Ratna menunjukkan layarnya ke seorang ibu yang lebih senior, menjelaskan cara menyetor; ibu itu manggut-manggut, mencoba sendiri di gawainya. Modal usaha Ratna sudah cair siang tadi — kini ia mendorong tetangga ikut tumbuh. Kebersamaan yang tercatat rapi, terbuka untuk semua.

**Shot list**
- **SEQ4-SC03-SH01** — WS balai warga. start: ibu-ibu melingkar, gawai di tangan masing-masing. end: Ratna di tengah membuka dasbor komunitas di layarnya. *(35mm · interaksi lintas-generasi/kelas)*
- **SEQ4-SC03-SH02** — MS Ratna & ibu senior. start: Ratna menunjukkan cara menyetor iuran. end: ibu senior mencoba sendiri, berhasil, tersenyum. *(50mm)*
- **SEQ4-SC03-SH03** — CU layar. start: dasbor koperasi — saldo kelompok + indikator transparansi terbuka. end: kartu layanan keuangan inklusif tergeser tipis di sisi. *(payoff: komunitas tumbuh bersama, transparan)*

**— Catatan produksi:** *Potensi iklan* — Surface: dasbor koperasi/komunitas + kartu layanan keuangan inklusif + venue balai warga. Momen intent: keuangan kolektif, inklusi. Kategori: layanan keuangan inklusif · kampanye sosial · kesehatan komunitas. Menampilkan **fairness/transparansi** (dasbor terbuka) — bukan transaksi dagang. Menutup benang SEQ3-SC02 (modal Ratna cair → ia dorong tetangga). Interaksi lintas-generasi. Grade hangat sore.

---

## SEQ4-SC04 — INT. RUANG EKSKUL SEKOLAH — 16.00 WIB *(edutainment · literasi anak, cross-cut dengan SC01)*
Ruang ekstrakurikuler sekolah seusai jam pelajaran, ceria dan rapi. Andi bersama beberapa teman mengelilingi satu tablet — **klub belajar interaktif**: modul edukasi yang dikemas seperti permainan, plus sudut **literasi keuangan anak** (celengan digital yang diawasi orang tua). Mereka bergiliran menjawab tantangan di layar; tiap jawaban tepat memunculkan tanda apresiasi. Seorang pembina muda mendekat, memberi petunjuk, ikut bertepuk saat satu tim menyelesaikan tantangan. Belajar yang terasa seperti bermain — dan dilakukan bersama.

**Shot list**
- **SEQ4-SC04-SH01** — MS Andi + teman. start: mereka mengelilingi tablet, modul edukasi-permainan di layar. end: Andi menjawab tantangan, teman-temannya menyimak (lintas-peer). *(50mm)*
- **SEQ4-SC04-SH02** — CU layar tablet. start: tantangan kuis + sudut celengan digital anak. end: tanda apresiasi muncul + sponsor edukasi anak tipis di sisi. *(Teknik 2/2b `prompt-rules`)*
- **SEQ4-SC04-SH03** — MWS. start: pembina muda mendekat memberi petunjuk. end: satu tim menyelesaikan tantangan, semua bertepuk semringah. *(35mm · payoff: belajar = bermain, bersama)*

**— Catatan produksi:** *Potensi iklan* — Surface: sponsor modul edukasi anak + tanda apresiasi + sudut literasi keuangan anak. Momen intent: keluarga + edukasi anak. Kategori: edtech anak · nutrisi · konten ramah-anak (brand-safe premium). Cross-cut dengan SC01 (ayah urus layanan publik / anak belajar, sore sama, lokasi beda). Bukan jual-beli. Interaksi lintas-peer + pembina. Grade hangat sore.

---

# SEQ5 — SENJA / PRA-PULANG (≈38 detik · 2 scene / 6 shot)
**Pesan sequence:** hari mereda dan kota bergerak pulang; perjalanan dan urusan rutin senja pun tertampung satu aplikasi — mudah dan setara untuk siapa saja. *(Konvensi: `06-konvensi-naratif.md`.)* Herman dikecualikan dari babak ini (penghindaran over-exposure bapak); Andi sudah di rumah, muncul di SEQ6.

---

## SEQ5-SC01 — INT. TERMINAL TRANSJAKARTA — 17.30 WIB *(mobilitas · transit hub)*
Senja turun, lampu terminal bus rapid-transit mulai menyala dan arus komuter memadat. Lisa berada di antara antrean, ransel di punggung; ia membuka aplikasi, memesan dan membayar tiket perjalanan, lalu menempelkan gawainya di gerbang tap — palang terbuka, ia melangkah ke peron. Di dinding peron, layar luar-ruang digital besar menyalakan iklan bergerak silih berganti di atas kepala para penumpang. Seorang ibu lanjut usia di sebelahnya tampak ragu membaca papan jadwal; Lisa menoleh, menunjukkan jadwal kedatangan di layar gawainya, ibu itu mengangguk berterima kasih. Pulang pun punya jalannya — sama mudahnya untuk siapa saja.

**VO (laki-laki, tenang):** *"Senja turun di kota. Pulang pun punya jalannya — semudah itu, dan sama untuk siapa saja."*

**Shot list**
- **SEQ5-SC01-SH01** — WS terminal senja. start: arus komuter padat, layar OOH digital menyala di latar, Lisa masuk antrean membuka aplikasi. end: ia memilih tiket perjalanan di gawai. *(24mm · keramaian transit hidup)*
- **SEQ5-SC01-SH02** — CU gawai + gerbang tap. start: tiket terbayar di layar, ia menempelkan gawai di gerbang. end: palang terbuka + kartu sponsor transport lewat tipis di layar. *(50mm macro · Teknik 2/2b)*
- **SEQ5-SC01-SH03** — MS peron. start: Lisa menunggu, layar OOH digital besar menyala iklan di atasnya. end: ia menunjukkan jadwal di gawainya ke ibu lanjut usia di sebelah (interaksi lintas-generasi). *(35mm · payoff: transit setara & mudah)*

**— Catatan produksi:** *Potensi iklan* — Surface: layar OOH digital peron + kartu sponsor transport di app + tiket/tap-gerbang + kios di latar. Momen intent: mobilitas pulang, captive audience di transit. Kategori: transport · telco · e-wallet · F&B/ritel · kampanye publik. **Hub transit = inventaris terpadat di seluruh film** (banyak permukaan sekaligus). Interaksi lintas-generasi (Lisa ↔ ibu lanjut usia). Bookend dengan ojek-pagi SEQ2-SC01 (berangkat/pulang) — mode massal + setting terminal sengaja beda. Grade hangat senja (lampu terminal mulai menyala).

---

## SEQ5-SC02 — INT. WARUNG KELONTONG TETANGGA — 17.30 WIB *(utilitas finansial · bayar-tagihan, cross-cut dengan SC01)*
Warung kelontong kecil di gang dekat rumah, lampu kuning hangat menyala saat langit meredup. Ratna mampir dalam perjalanan pulang dari balai warga; ia berdiri di depan etalase, membuka aplikasi pada menu pembayaran. Bukan berbelanja barang — ia **melunasi aneka tagihan rumah sekaligus**: listrik, iuran jaminan kesehatan, pulsa, lalu mengisi ulang celengan digital Andi. Pemilik warung, seorang bapak paruh baya, menyapanya sambil menata rokok di rak; mereka mengobrol ringan soal harga-harga. Satu per satu tagihan berubah "lunas" di layar. Urusan rumah yang dulu berserak di banyak loket, kini beres dari depan warung.

**Shot list**
- **SEQ5-SC02-SH01** — MS warung senja. start: Ratna di depan etalase, lampu warung kuning, pemilik warung menyapa. end: ia membuka menu pembayaran tagihan di gawai. *(35mm · interaksi lintas-tetangga)*
- **SEQ5-SC02-SH02** — CU gawai. start: daftar tagihan (listrik / jaminan kesehatan / pulsa) + isi ulang celengan digital Andi. end: status berubah "lunas" satu per satu + kartu iklan utilitas/telco tipis di sisi. *(50mm · Teknik 2/2b)*
- **SEQ5-SC02-SH03** — MS Ratna & pemilik warung. start: keduanya mengobrol ringan. end: Ratna pamit, melangkah pulang, warung hangat di latar. *(35mm · payoff: semua urusan rumah beres dari satu tempat)*

**— Catatan produksi:** *Potensi iklan* — Surface: menu bayar-tagihan/PPOB + kartu utilitas/telco + isi-ulang celengan anak + rak warung di latar. Momen intent: rutinitas finansial rumah tangga senja. Kategori: utilitas (listrik) · asuransi/jaminan kesehatan · telco · e-wallet. **Bukan jual-beli barang** — fitur utilitas finansial, kategori iklan baru. Interaksi lintas-tetangga (Ratna ↔ pemilik warung). Cross-cut dengan SC01 (Lisa transit / Ratna urus tagihan, senja sama, lokasi beda). Grade hangat senja (lampu warung kuning).

---

# SEQ6 — MALAM / PULANG & SAKRAL (≈43 detik · 3 scene / 6 shot)
**Pesan sequence:** hari yang penuh menutup di tempat ia dimulai — rumah; sistem yang adil tahu kapan menemani dan kapan diam, dan manusia yang memegang kendali. *(Konvensi: `06-konvensi-naratif.md`.)* Penutup film: app-beat komersial terakhir (opt-in syariah) → **"Bersih Saat Sakral"** (ngaji ba'da Maghrib, nol komersial, melengkapi Subuh) → coda kamar (bookend ke pembuka).

---

## SEQ6-SC01 — INT. RUANG MAKAN — 18.30 WIB *(konvergensi keluarga · app-beat komersial terakhir)*
Malam turun, ruang makan benderang oleh lampu hangat. Keluarga lengkap akhirnya berkumpul: Herman sudah pulang, tasnya tersampir di kursi; Ratna menata lauk — sebagian hidangan malam ini adalah frozen food buatannya sendiri yang tadi siang ia siarkan (payoff diegetik menutup hari); Lisa baru tiba, meletakkan ransel; Andi sudah lebih dulu duduk menunggu. Mereka makan bersama, mengobrolkan hari masing-masing. Menjelang azan Maghrib, Herman meraih ponselnya dan di aplikasi **mengaktifkan opt-in mode syariah** — sebuah pilihan, bukan paksaan; tampilan menyesuaikan tenang. Ia menelungkupkan ponsel di meja. Sejak itu, layar berhenti menawarkan apa pun.

**Shot list**
- **SEQ6-SC01-SH01** — WS ruang makan. start: keluarga lengkap duduk satu meja, lampu hangat, hidangan (termasuk frozen food Ratna) tersaji. end: mereka makan bersama, mengobrol (interaksi lintas-generasi penuh — empat tokoh satu frame). *(35mm · payoff: produk Ratna jadi hidangan keluarga)*
- **SEQ6-SC01-SH02** — CU ponsel di tangan Herman. start: ia mengaktifkan toggle opt-in mode syariah, tampilan app menyesuaikan tenang. end: ia menelungkupkan ponsel di meja — app-beat komersial terakhir film. *(50mm · transisi menuju zona sakral)*

**— Catatan produksi:** *Potensi iklan* (SH02 saja, pra-sakral) — Surface: pilihan mode syariah di app (opt-in pengguna). Momen intent: penyelarasan nilai/keyakinan. Kategori: layanan/konten syariah (halal, keuangan syariah) — opt-in, bukan default. **Ini permukaan komersial terakhir**; sejak SC02 nol grafis. Opt-in syariah ditampilkan sebagai pilihan, tanpa nama organisasi keagamaan. Interaksi keluarga penuh. Grade hangat malam (lampu interior).

---

## SEQ6-SC02 — INT. RUANG KELUARGA — 18.50 WIB *(ngaji ba'da Maghrib · kitab digital sebagai wasilah)*
Ba'da Maghrib, ruang keluarga teduh oleh lampu hangat. Ratna duduk berdampingan dengan Andi di lantai beralas. Di hadapan Andi terbuka sebuah **kitab hardcopy** — halaman bertajwid, dibaca pelan. Di samping mereka, **satu monitor menampilkan versi digital kitab yang sama**: baris yang sedang dibaca tersorot lembut, penanda tajwid mengikut. Ratna menuntun sambil menengok layar itu, ujung jarinya menunjuk pulang-balik antara kitab fisik Andi dan panduan di monitor; Andi melafalkan, sesekali Ratna membetulkan dengan sabar. Tak ada satu pun iklan atau kartu komersial dalam frame — layar di sini hanya melayani yang sakral. Tradisi tidak digantikan; ia ditemani.

*(Zona sakral — VO senyap. VO penutup dipindah ke coda SEQ6-SC03.)*

**Shot list**
- **SEQ6-SC02-SH01** — MS Ratna & Andi. start: Andi menghadap kitab hardcopy terbuka, Ratna di sampingnya. end: Ratna menengok monitor kitab digital, jarinya menuntun baris (interaksi lintas-generasi). *(50mm · zona sakral — layar hanya konten ibadah, nol iklan)*
- **SEQ6-SC02-SH02** — CU bergantian kitab ↔ monitor. start: baris yang dilafalkan Andi di kitab hardcopy. end: baris sama tersorot di monitor (penanda tajwid), tanpa kartu iklan apa pun. *(50mm macro · bukti brand-safe: wasilah sakral, nol komersial)*

**— Catatan produksi:** **Bersih Saat Sakral = NOL KOMERSIAL (bukan nol layar):** monitor hadir tetapi hanya menampilkan kitab digital, NOL kartu iklan/grafis komersial. Scene bebas-iklan kedua (melengkapi SEQ1-SC02 Subuh). Tema: **teknologi sebagai wasilah** untuk ibadah — payoff diegetik opt-in syariah (SC01). Hardcopy + digital berdampingan = tradisi ditemani, bukan digantikan; ngaji ba'da Maghrib (praktik keluarga Muslim Indonesia). Sholat Maghrib berjamaah dilepas (sholat Subuh SEQ1-SC02 tetap jangkar ibadah; bookend utama film = coda SC03). Interaksi Ratna↔Andi lintas-generasi. VO senyap. Identitas + wardrobe dikunci. Grade hangat malam.

---

## SEQ6-SC03 — INT. KAMAR HERMAN — 20.30 WIB *(coda · bookend pembuka SEQ1-SC01)*
Malam larut, kamar yang sama tempat hari ini bermula. Herman berbaring di ranjang, lampu nyaris padam. Ia melirik ponsel di tangannya sekilas — **grafik pergerakan saham**, kini garis penutupan hari ini, gema persis dari sorotan dini hari tadi; tak ada kartu iklan, ia tak mengejar apa pun, hanya menengok lalu melepas. Ibu jarinya menyentuh tombol; layar **padam**. Ia meletakkan ponsel telungkup di nakas, menarik selimut, dan **memejamkan mata**. Hari yang penuh menutup persis di tempat ia dibuka — mata yang tadi terbuka, kini terpejam.

**VO (laki-laki, tenang, penutup):** *"Satu hari penuh. Teknologi yang adil tahu kapan menemani — dan kapan diam. Manusia yang memegang kendali; teknologi sekadar jalannya."*

**Shot list**
- **SEQ6-SC03-SH01** — MCU Herman + ponsel di ranjang (cermin SEQ1-SC01-SH03). start: ia melirik grafik saham penutupan hari, wajah tersorot cahaya layar redup. end: ibu jari menekan, layar padam; cahaya hilang dari wajahnya. *(50mm · echo pembuka — tanpa kartu iklan, layar dipadamkan = "tahu kapan diam")*
- **SEQ6-SC03-SH02** — ECU mata Herman (cermin terbalik SEQ1-SC01-SH01). start: ia meletakkan ponsel telungkup, mata masih terbuka di keremangan. end: kelopak mata menutup perlahan; frame meredup ke penutup. *(50mm · bookend: hari buka dengan mata terbuka, tutup dengan mata terpejam)*

**— Catatan produksi:** **Coda bebas-iklan** — layar muncul hanya untuk dipadamkan (grafik saham penutupan, NOL kartu iklan), memperkuat tema VO "tahu kapan diam". Bukan pelanggaran Bersih Saat Sakral: ini wind-down privat **setelah** ibadah selesai (preseden Subuh: ibadah dikurung, hidup berlanjut). Bookend ketat ke SEQ1-SC01: ranjang yang sama, motif HP+grafik-saham, ECU mata dibalik (buka→tutup). VO penutup mendarat di sini agar kata + gambar-akhir berpadu. Identitas Herman + kamar dikunci (konsisten SEQ1-SC01). Grade hangat malam, nyaris gelap.

---

## STATUS GATE A — LENGKAP
`03-scene-detail.md` kini memuat **SEQ1–SEQ6 penuh** (6 babak / 19 scene / 56 shot · runtime ≈307s) *(SEQ1-SC02-SH04 sujud dihapus 2026-06-24, 57→56 shot, −5s)*. Struktur hari: Subuh → Pagi → Siang → Sore → Senja/Pra-Pulang → Malam, ditutup coda kamar (bookend ke pembuka). Dua scene bebas-iklan (Subuh sholat & ba'da-Maghrib ngaji — yang kedua "nol komersial bukan nol layar": kitab digital sebagai wasilah) + coda layar-dipadamkan membingkai hari. Runtime ~312s sedikit di atas target ≈300s — bila perlu dikunci 300s, pangkas satu shot saat sinkron. Siap lanjut ke GATE B (prompt 6-lapis) setelah closure sesi + sinkron dampak hilir O4 (`04-ad-inventory-map`, deck `11`) yang masih menyebut kerangka "15-scene/5-babak".
