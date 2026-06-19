---
title: Protokol Uji Benchmark — Success Rate Kling 3.0
tags: [explainer-video, pipeline, production, benchmark, kling]
status: draft-v1
created: 2026-06-17
updated: 2026-06-17
aliases: [kling-benchmark, success-rate-test]
---

# Protokol Uji Benchmark — Success Rate Kling 3.0
*Untuk mengunci angka success rate aktual sebelum menetapkan jumlah subscribe di `03-rab-produksi-ai.md`. Menggantikan asumsi lama 50% (generasi Kling lama).*

---

## Tujuan

Mengukur **accept rate** (klip production-ready ÷ total klip digenerate) Kling 3.0 pada scene wajah-manusia dinamis kita, di bawah setelan produksi sebenarnya. Output: satu angka persen yang menggantikan "50% ⚠️" di RAB, plus keputusan jumlah subscribe.

## Setelan uji (samakan persis dengan produksi)

| Parameter | Nilai |
|---|---|
| Model | Kling 3.0 (render final) |
| Resolusi | 1080p |
| Audio bawaan | ON (12 kredit/detik) |
| Durasi segmen | 5 detik (60 kredit/segmen) |
| Anchor | 3–5 gambar referensi per karakter (dari ChatGPT Image v2) untuk reference-locking |
| Teknik | start→end keyframe |
| Sumber prompt | `02-production-brief.md` (motion direction per scene) |

## Sampel

15 segmen total — **5 segmen per karakter dinamis**: K2 (pemuda-laptop), K3 (kurir-motor), K5 (pengusaha-showroom). Tiga karakter ini mewakili tiga tingkat kesulitan gerak (duduk statis → kendaraan bergerak → interaksi layar berdiri).

Biaya uji: 15 × 60 = **900 kredit** (~11% dari satu subscribe Premier 8.000 — aman, masih sisa untuk produksi).

## Rubrik PASS/FAIL (biner per klip — semua harus PASS untuk dihitung lolos)

1. **Konsistensi wajah** — wajah cocok dengan anchor, tidak morphing antar-frame.
2. **Integritas anatomi** — tangan/jari tidak meleleh, objek mekanis (HP/stang/layar) tidak rusak.
3. **Gerak natural** — motion mulus, tidak patah/melayang/warping.
4. **Audio koheren** — ambient/SFX bawaan menyatu dengan adegan (bukan noise acak).
5. **Bebas artefak** — tidak ada flicker, ghosting, atau distorsi tepi mencolok.

Satu kriteria gagal = klip FAIL.

## Pencatatan (tabel log)

| # | Karakter | Kredit | PASS/FAIL | Kriteria gagal (jika ada) | Catatan |
|---|---|---|---|---|---|
| 1 | K2 | 60 | | | |
| … | | | | | |
| 15 | K5 | 60 | | | |

## Hitung & putuskan

- **Accept rate = jumlah PASS ÷ 15.**
- **Kredit per klip diterima = (15 × 60) ÷ jumlah PASS.**

Aturan keputusan jumlah subscribe:

| Accept rate terukur | Keputusan |
|---|---|
| **≥ 65%** | **1× Premier cukup** — kapasitas bersih ~7 mnt jauh di atas kebutuhan ~90 dtk |
| 50–64% | 1× Premier untuk produksi utama; siapkan 1× cadangan revisi (tetap 2×) |
| < 50% | Pertahankan 2× + tinjau ulang anchor/prompt sebelum produksi massal |

## Tindak lanjut

Setelah angka terukur: perbarui baris success-rate + jumlah subscribe di `03-rab-produksi-ai.md`, dan ganti penanda ⚠️ "benchmark generasi lama" dengan angka aktual + tanggal uji.

---

*Lihat juga: `03-rab-produksi-ai.md` · `04-pipeline-ai-production.md` · memory `semesta-kling-pricing-models.md`*
