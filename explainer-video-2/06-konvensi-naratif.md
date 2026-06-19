---
title: Konvensi Naratif — Sequence / Scene / Shot (Explainer Video 2)
tags: [explainer-video-2, konvensi, sequence, scene, shot, governance]
status: active
created: 2026-06-19
updated: 2026-06-19
aliases: [ev2-06-konvensi, konvensi-naratif, seq-sc-sh]
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
- Sequence dinomori per babak (SEQ1..SEQ5). **Scene RESET ke `SC01` di tiap sequence** (SEQ2 mulai dari `SEQ2-SC01`, bukan melanjutkan nomor SEQ1). **Shot RESET ke `SH01` di tiap scene.** Tiap shot ditulis dengan ID penuh `SEQ<n>-SC<nn>-SH<nn>`. JANGAN menomori global/berlanjut antar induk.
- Penyimpanan keyframe mengikuti shot: `scene-images/` (lihat konvensi file di `scene-images/README.md`, selaraskan ke `SEQ-SC-SH`).

---

## Dasar riset (Priority 3)
- Columbia Film Language Glossary — Shot, Scene, and Sequence.
- ScreenWriting Science — Definition of Sequence and Scene.
- Sequence (filmmaking) — Wikipedia.
- BeverlyBoy — Shot vs Scene vs Sequence.

Inti: shot = satu take/setup; scene = aksi kontinu satu lokasi+waktu (berganti lokasi/waktu → scene baru); sequence = kumpulan scene dengan satu tujuan/ide/topik.

---

*Konvensi v1 · 2026-06-19 · kanonik; ditautkan oleh 00-INDEX, 02, 03, 05.*
