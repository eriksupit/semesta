---
title: Pipeline Produksi — Explainer Video 2 (Satu Keluarga, Satu Hari Penuh)
tags: [explainer-video-2, pipeline, produksi, kling, image-generation, output]
status: active
created: 2026-06-18
updated: 2026-06-18
aliases: [ev2-05-pipeline, pipeline-produksi-2]
---

# Pipeline Produksi — Explainer Video 2
## Konsep "Satu Keluarga, Satu Hari Penuh" · Semesta Digital *(working title)*

> **Peran dokumen:** acuan teknis produksi konsep video baru. Menautkan, bukan menyalin: aturan prompt di `prompt-rules-image-generation.md`, contoh implementasi di `explainer-video/08-investor-deck-brief.md`, dan pewarisan biaya/kapasitas di `explainer-video/04-pipeline-ai-production.md` + `04-a-kling3-benchmark-protocol.md`.
> **Status proses:** keputusan dicatat di `00-WORKLOG.md`; hasil naratif di `01-storyline.md`.

---

## 1. Stack Produksi (dikunci 2026-06-18)
- **Keyframe (gambar):** ChatGPT Image v2 (GPT Image 2), text-to-image, eksternal.
- **Video adegan:** Kling 3.0, image-to-video via **start-frame → end-frame keyframe**.
- **Audio adegan (ambience/SFX/foley):** Kling 3.0 audio-on (sinkron per klip).
- **Audio narator (VO laki-laki):** **TREK TERPISAH** — TTS berkualitas atau pengisi suara, di-mix di tahap edit. **BUKAN** output Kling.
- **Pra-produksi — Character & Wardrobe Reference Sheet:** ChatGPT Image v2, **white background**, **multi-angle**. Plat identitas tetap (wajah + perawakan) per tokoh = jangkar konsistensi; plus **katalog wardrobe per-scene** per tokoh (wardrobe berbeda tiap scene, dikunci di `03-scene-detail.md`). Melayani dua hal sekaligus: jangkar visual saat menulis prompt keyframe (Lapis 1–3) **dan** gambar referensi untuk **reference-locking Kling 3.0** (3–5 gambar). Disimpan di `character-images/`.

### Koreksi arsitektur yang dikunci (4)
1. **Narator ≠ Kling.** Audio-on Kling = audio adegan, bukan pembacaan naskah presisi. Narator adalah satu trek menerus melintasi semua scene & cut → aset lapisan-edit, bukan output per-klip. Generate terpisah, mix di edit.
2. **Keyframe per SHOT (= setup kamera = segmen 5 detik), bukan per scene.** Hierarki SEQ/SC/SH di `06-konvensi-naratif.md`: 1 shot = 1 keyframe-pair. Scene 20 dtk = beberapa shot → set keyframe berantai. Aturan sambung bila kontinu: **end-frame SH-N = start-frame SH-(N+1)**.
3. **Grade VIDEO hangat, bukan cool deck-standard.** `prompt-rules` baris 208 mengunci grade COOL khusus 19 still deck. Video konsep keluarga = hangat. Token hangat DIKUNCI (terverifikasi keyframe SEQ1-SC01-SH03, lihat `00-WORKLOG` GATE B): `Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones`. Hangat hanya dari `color_grade`; garmen desaturated.
5. **Nol grafis dari AI (ADDENDUM A1, `00-WORKLOG`).** Semua grafis (UI/kartu iklan/grafik/super/motion) digarap di After Effects oleh animator manusia. Prompt keyframe **membuang Lapis 5**; device tetap muncul, framing comp-aware (ruang layar bersih), layar netral/mati. Beat "App UI/Potensi Iklan" diwujudkan di POST.
4. **Keyframe = PASANGAN identity-konsisten, bukan still tunggal.** `08` = still diam. Untuk start→end: **1 blok spec tetap** (Lapis 1–3 & 6: identitas, wardrobe, scene, kamera dikunci sama persis) **+ 2 varian Lapis 4** (subject_state/action/pose/gesture/expression) — satu untuk start, satu untuk end. Dua gambar = dua momen dari aksi yang sama.

---

## 2. Siklus Per-Scene (terkoreksi)
```
[STEP 0] CHARACTER & WARDROBE SHEET (ChatGPT Image v2, white bg, multi-angle)
  │  plat identitas tetap per tokoh + katalog wardrobe per-scene
  └─> [GATE 0] approve plat identitas + katalog wardrobe
        │  (jangkar konsistensi: disuntik ke tiap prompt GATE B Lapis 1–3 + reference-locking Kling)
        ▼
STORYLINE (clean di 01) 
  └─> DETAIL ADEGAN (03-scene-detail) + rancang segmentasi 5-dtk per scene
        └─> [GATE A] approve / revisi detail adegan
              └─> TULIS PROMPT t2i (per segmen):
                     1 spec tetap (Lapis 1–3 & 6) + 2 state Lapis-4 (start, end),
                     grade VIDEO hangat, compliant prompt-rules
                    └─> [GATE B] approve / revisi prompt
                          └─> GENERATE pasangan keyframe ke ChatGPT Image v2
                                └─> [GATE C] pilih keyframe akurat + konsisten identitas
                                      └─> MASUK STORYBOARD (02-storyboard)
                                            └─> SCENE / SEGMEN BERIKUTNYA → ulangi
```
Trek **narator + audio-adegan** ditangani di jalur edit, paralel & terpisah dari generate keyframe.

> **Tiap shot = satu target prompt t2i.** Ke-**56 shot** (SEQ1–SEQ6) masing-masing = satu keyframe-pair (start→end) → himpunan target lengkap **~112 keyframe** *(SEQ1-SC02-SH04 sujud dihapus 2026-06-24)*. `02-storyboard.md` = **kompendium gambar utuh** dari semua shot ini.

### Empat gerbang validasi
- **GATE 0 — Character sheet:** plat identitas tetap (wajah/perawakan, multi-angle, **white background**) + katalog wardrobe per-scene disetujui; jadi pemandu konsistensi yang disuntikkan ke **setiap** prompt GATE B (Lapis 1–3) + reference-locking Kling 3.0. **Mendahului GATE B** (sekali di awal, dipakai ulang seluruh produksi).
- **GATE A — Detail adegan:** Peristiwa→App UI→Potensi Iklan→Payoff jelas; segmentasi 5-dtk masuk akal; "Bersih Saat Sakral" dipatuhi.
- **GATE B — Prompt:** compliant 6-lapis `prompt-rules`; grade hangat (token dikunci, `00-WORKLOG` GATE B); spec tetap identik antar start/end; hanya Lapis 4 berbeda; **Lapis 5 grafis DIBUANG (ADDENDUM A1 — grafis di After Effects)**; tiap prompt mengikat plate GATE 0 via `character_identity.identity_reference`; crew video Cuarón/Lubezki/Caballero + costume/makeup/hair per `07 §5`.
- **GATE C — Keyframe:** akurasi visual + konsistensi identitas/wardrobe/scene antar pasangan & antar segmen; end-N = start-(N+1) tersambung.

---

## 3. Acuan Prompt (wajib dibaca sebelum menulis prompt)
- Struktur 6-lapis, token discipline, banned-list → `prompt-rules-image-generation.md`.
- Contoh implementasi prompt nyata (still) → `explainer-video/08-investor-deck-brief.md` Section 5.
- **Catatan override:** untuk video, ganti `color_grade` cool deck-standard → grade hangat video (token hangat final ditetapkan di WORKLOG saat scene pertama disusun). Larangan token lain (negasi, label emosi, garmen tak-dispesifikasi=auto-batik) TETAP berlaku.

---

## 4. Pewarisan Biaya & Kapasitas (tidak disalin — otoritatif di lokasi asli)
- `explainer-video/03-rab-produksi-ai.md` — RAB tools + honor.
- `explainer-video/04-pipeline-ai-production.md` — pipeline produksi AI (strategi model 2.6-draft→3.0-final).
- `explainer-video/04-a-kling3-benchmark-protocol.md` — protokol uji success-rate Kling 3.0.
- **Dampak hilir (O4):** bila jumlah scene/segmen/durasi final bergeser dari asumsi, RAB & kapasitas subscribe wajib di-review.

---

## 5. Tabel Pelacakan Status Per-Scene (live)
**Struktur GATE A LENGKAP: 6 babak / 19 scene / 56 shot / ≈307s** (sumber kanonik: `03-scene-detail.md`, SEQ1–SEQ6). Detail (A) = ✅ untuk seluruh scene.
Status: `—` belum · `🟡` proses · `✅` lolos gate. Keyframe terpilih disimpan di `scene-images/` per scene (konvensi: `scene-images/README.md`); plat identitas + wardrobe di `character-images/` (GATE 0).

| Scene | Detail (A) | Prompt (B) | Keyframe (C) | Storyboard | Catatan |
|---|---|---|---|---|---|
| SEQ1-SC01 | ✅ | — | — | — | Subuh · kamar Herman · 4-beat kanonik (apparel + saham) |
| SEQ1-SC02 | ✅ | — | — | — | Subuh · sholat berjamaah · **sakral SH02+ = nol grafis** (teaser UMKM SH01) |
| SEQ2-SC01 | ✅ | — | — | — | Pagi · gerbang kompleks · lintas-kelas |
| SEQ2-SC02 | ✅ | — | — | — | Pagi · kantor ekspor-impor |
| SEQ2-SC03 | ✅ | — | — | — | Pagi · ruang belajar rumah (cross-cut SC02) |
| SEQ2-SC04 | ✅ | — | — | — | Pagi · kafe |
| SEQ3-SC01 | ✅ | — | — | — | Siang · dapur Ratna · marketplace B2C live-selling |
| SEQ3-SC02 | ✅ | — | — | — | Siang · virtual office · bank-as-tenant |
| SEQ3-SC03 | ✅ | — | — | — | Siang · financial trading (sela kerja) |
| SEQ3-SC04 | ✅ | — | — | — | Siang · coworking · Lisa mengajar |
| SEQ4-SC01 | ✅ | — | — | — | Sore · government-as-tenant (izin) · nol jual-beli |
| SEQ4-SC02 | ✅ | — | — | — | Sore · masterclass (Lisa kembali murid) · nol jual-beli |
| SEQ4-SC03 | ✅ | — | — | — | Sore · koperasi & inklusi finansial · nol jual-beli |
| SEQ4-SC04 | ✅ | — | — | — | Sore · edutainment literasi anak (cross-cut SC01) · nol jual-beli |
| SEQ5-SC01 | ✅ | — | — | — | Senja · terminal TransJakarta · inventaris terpadat |
| SEQ5-SC02 | ✅ | — | — | — | Senja · warung · PPOB bayar-tagihan (cross-cut SC01) |
| SEQ6-SC01 | ✅ | — | — | — | Malam · ruang makan · opt-in syariah · app-beat komersial terakhir |
| SEQ6-SC02 | ✅ | — | — | — | Malam · ngaji ba'da Maghrib · **bebas-iklan: nol komersial** (kitab digital) |
| SEQ6-SC03 | ✅ | — | — | — | Malam · coda kamar · **bebas-iklan: layar-padam, bookend SEQ1-SC01** |

---

*Pipeline Produksi v1 · 2026-06-18 · proses di `00-WORKLOG.md` · acuan: `prompt-rules-image-generation.md`, `explainer-video/08`, `explainer-video/04`/`04-a`*
