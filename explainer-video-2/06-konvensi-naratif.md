---
title: Konvensi Naratif — Sequence / Scene / Shot (Explainer Video 2)
tags: [explainer-video-2, konvensi, sequence, scene, shot, governance]
status: active
created: 2026-06-19
updated: 2026-06-29
aliases: [ev2-06-konvensi, konvensi-naratif, seq-sc-sh, workflow-sop]
---

# Konvensi Naratif — Sequence / Scene / Shot
## Explainer Video 2 · Semesta Digital *(working title)*

> **Sumber kebenaran tunggal** untuk hierarki naratif. `02-storyboard.md`, `03-scene-detail.md`, `05-pipeline-produksi.md`, dan `00-INDEX.md` MENAUTKAN dokumen ini — tidak menyalin isinya. Bila konvensi berubah, ubah di sini saja.

---

## Hierarki (analogi resmi: shot = kata · scene = kalimat · sequence = bab)

| Tingkat | Definisi | Dasar pengelompokan | Padanan pipeline kita |
|---|---|---|---|
| **Sequence (SEQ)** | kumpulan scene yang mengusung **satu tujuan/pesan naratif** | by peristiwa/pesan | 5 babak hari (Subuh / Pagi / Siang / Sore / Malam) — tiap babak satu beat pesan |
| **Scene (SC)** | aksi kontinu dalam **1 lokasi + 1 waktu** | by lokasi + waktu | unit seperti "Herman bangun di kamar", "sholat di ruang keluarga" |
| **Shot (SH)** | **satu setup kamera tunggal** (satu angle/framing/take) | by setup kamera | = **satu keyframe-pair (start→end) = satu segmen 5 dtk Kling** |

### Aturan tegas
- **Scene pecah** begitu lokasi ATAU waktu berganti. Lokasi baru = scene baru; lompatan waktu = scene baru.
- **Shot = satu angle.** Beberapa angle/POV atas aksi yang sama = **coverage** = **beberapa shot dalam satu scene** — bukan satu shot berisi banyak angle.
- **Cross-cut** (memotong bolak-balik antar tokoh di lokasi berbeda yang beraktivitas serempak) = beberapa **scene** terpisah yang di-*intercut* saat edit. Aturan "1 scene = 1 lokasi = 1 waktu" tetap utuh; cross-cut hanya mengatur urutan tayang.
- **1 shot = 1 unit generate** = satu pasangan keyframe (start→end) di ChatGPT Image v2 → satu klip Kling 5 dtk. Sambung antar-shot dalam scene: end-frame SH-N = start-frame SH-(N+1) bila kontinu.
- **Interaksi wajib di scene aktivitas (WAJIB).** Tiap scene aktivitas tokoh harus melibatkan pihak lain — tatap muka ATAU via layar (video-call/live/komentar real-time keduanya sah). DILARANG mono-aktor "berbicara ke ruang kosong". Utamakan interaksi **lintas-kelas / lintas-demografi / lintas-generasi** (sesuai tema pasar lintas-demografis). Pengecualian wajar: beat privat/intim by-design (mis. bangun tidur, momen ibadah).
- **Prosa camera-bound (WAJIB).** Prosa scene hanya mendeskripsikan apa yang tertangkap kamera DI lokasi itu. DILARANG narasi mahatahu yang melompati lokasi atau menyebut orang/ruang di luar pandang kamera (mis. "rumah mulai hidup", "dari kamar seberang Lisa menggeliat" saat scene terkunci di ruang keluarga). Tokoh/ruang lain punya scene-nya sendiri; bila perlu ditampilkan serempak, itu **cross-cut** (scene terpisah), bukan satu kalimat. Tulis seperti kamera, bukan seperti novelis. Garis tematik singkat (mis. "satu gerbang, satu pagi") boleh, asal semua elemennya co-present di lokasi itu.

---

## Penomoran
Format: **`SEQ<n>-SC<nn>-SH<nn>`**.
- Contoh: `SEQ1-SC01-SH02` = Sequence 1 (Subuh), Scene 01, Shot 02.
- Sequence dinomori per babak (SEQ1..SEQ6). **Scene bernomor KONTINU global lintas-sequence** ("bertumbuh": SC01, SC02, …, SC19 — SEQ2 lanjut `SC03` setelah SEQ1 berakhir di `SC02`; **TIDAK reset ke SC01 tiap sequence**). SEQ = label grup. **Shot RESET ke `SH01` di tiap scene.** ID penuh `SEQ<n>-SC<nn>-SH<nn>` (SC kontinu, SH reset). *(Ref legacy reset-style — nama file gateB `SEQ1-SC01.md`, character/env sheet — direkonsiliasi saat disentuh; belum di-rename massal.)*
- Penyimpanan keyframe mengikuti shot: `scene-images/` (lihat konvensi file di `scene-images/README.md`, selaraskan ke `SEQ-SC-SH`).

---

## Workflow Produksi Gambar (SOP) — kanonik · urut · wajib

> Rantai satu-arah dari **cerita** ke **gambar**. Tiap langkah selesai & terkunci sebelum langkah berikut. JANGAN melompati gerbang — membangun keyframe sebelum cerita terkunci adalah sumber churn (terbukti pada riwayat SC01: restruktur 4→7, thrash metode SH04).

**Urutan garap scene = URUT / TERTIB (disiplin Erik):** kerjakan scene KETAT sesuai urutan nomor (SC01→SC02→SC03→…), JANGAN loncat. Daftar scene memang disusun agar cerita tumbuh berurutan; produksi mengikuti urutan itu apa adanya. Satu scene tuntas (locked) sebelum lanjut ke berikutnya.

**Langkah 1 — `03-scene-detail.md` = CERITA (GATE A, clean-slate).**
Tulis & kunci cerita per scene, berurutan. Scene = 1 lokasi + 1 waktu (pindah lokasi/waktu → scene baru). Isi sah: **Pesan misi (ad-provider)** + prosa scene + VO + **blok-narasi per shot** + baris **Grafis UI (AE)** (kapan muncul + copy) + Catatan produksi. **NOL addendum, NOL tag status, NOL catatan metode/revisi bertanggal, NOL prompt** (prompt = GATE B). Status produksi dan metode per-shot TIDAK hidup di sini.

**Langkah 2 — satu doc per scene di `10-gateB-keyframes/SEQ<n>-SC<nn>.md` (GATE B).**
Tiap scene yang sudah terkunci diturunkan jadi SATU dokumen. Di sinilah status produksi, metode per-shot, dan prompt hidup.

**Langkah 3 — tiap shot: BLOK NARASI dulu, baru prompt.**
Sebelum token apa pun, urai shot dalam narasi (template di bawah). Syarat shot: framing + angle **LOCKED** start→end; hanya subjek yang bergerak. Satu shot wajib mampu menggambarkan adegan AWAL (calon image START) dan adegan AKHIR (calon image END).

**Langkah 4 — terjemahkan narasi → prompt.**
START = **full prompt** (master / angle-child; hukum master-parent + edit-in-place: `prompt-rules-text-image-to-image.md`). END = **edit-in-place** pada render START yang sudah accepted.

**Langkah 5 — produksi.**
User generate; Claude menunggu (Claude tidak pernah generate). Render accepted → rename ke `scene-images/` → update status di per-scene doc (Langkah 2) → shot berikutnya.

### Template scene (GATE A · di `03-scene-detail.md`)
```
## SEQ<n>-SC<nn> — <LOKASI> — <WAKTU>
**Pesan misi (ad-provider):** <vertikal app yang ditunjukkan + bukti app layak jadi kanal iklan>
**Prosa scene:** <prosa camera-bound — SHOW bukan TELL (aksi/keadaan tertangkap kamera, bukan label emosi/kesimpulan tema) + RINGKAS (sedikit beat & elemen, satu aksi foreground, ≤2–3 subjek, latar = ambient → wajib bisa jadi SATU gambar yang mudah di-generate)>
**VO (bila ada):** <...>

### Shot — blok narasi
#### SH0N — <judul beat>
- Narasi          : <kalimat deskriptif lengkap, camera-bound>
- Kamera          : <posisi / vantage>
- Angle + Framing : <LOCKED start→end>
- Mood / Cahaya   : <state cahaya>
- Adegan AWAL (→START) : <state awal subjek>
- Adegan AKHIR (→END)  : <delta subjek yang tergambar>

**Grafis UI (AE, non-AI):**
- saat <sub-adegan>, muncul <grafis>, copy: "<teks>"

**— Catatan produksi:** <kategori iklan · grade>
```
> Prompt START (full) / END (edit-in-place) **TIDAK di sini** — diturunkan ke `10-gateB-keyframes` per shot (Langkah 4).
> **Pola prosa scene (dikunci Erik 2026-06-30):** SHOW + RINGKAS. (a) SHOW — perlihatkan lewat aksi/keadaan yang tertangkap kamera, jangan menyebut emosi ("ragu", "sumringah") atau menyimpulkan tema ("ilmu berputar"); biarkan aksi yang bicara. (b) RINGKAS — sedikit elemen, satu aksi foreground jelas, ≤2–3 subjek, sisanya latar ambient, supaya tiap scene mudah jadi satu gambar (prosa kepadatan → susah generate). Acuan: SC09, SC11, SC12 di `03-scene-detail.md`.

---

## Dasar riset (Priority 3)
- Columbia Film Language Glossary — Shot, Scene, and Sequence.
- ScreenWriting Science — Definition of Sequence and Scene.
- Sequence (filmmaking) — Wikipedia.
- BeverlyBoy — Shot vs Scene vs Sequence.

Inti: shot = satu take/setup; scene = aksi kontinu satu lokasi+waktu (berganti lokasi/waktu → scene baru); sequence = kumpulan scene dengan satu tujuan/ide/topik.

---

*Konvensi v1 · 2026-06-19 · kanonik; ditautkan oleh 00-INDEX, 02, 03, 05.*
