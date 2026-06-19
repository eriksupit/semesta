---
title: RAB Produksi Video AI — Semesta Digital (working title)
tags: [explainer-video, budget, production, rab]
status: final-v3
created: 2026-06-08
updated: 2026-06-09
aliases: [rab-video, budget-video]
---

# Rencana Anggaran Biaya
## Produksi Video AI — Semesta Digital *(working title)*
*Final v3.0 · 9 Juni 2026 · Ditambahkan: Honor Tenaga Ahli (tim produksi manusia) — model tiga-lane*

---

## Catatan Pembacaan untuk Investor

Satuan waktu dalam dokumen ini adalah **siklus berlangganan bulanan (monthly subscribe)**, bukan durasi produksi. Produksi video AI tidak linear — satu siklus billing bisa mencakup lebih dari satu minggu kerja intensif, atau sebaliknya. Angka "2x monthly subscribe" berarti dua siklus pembayaran bulanan pada platform tersebut, bukan dua bulan waktu kerja.

Semua item dikunci pada satu pilihan. Tidak ada opsional.

---

## Arsitektur Platform

| Layer | Platform | Fungsi |
|---|---|---|
| Text-to-image | Midjourney v8.1 Pro | Generate anchor images semua karakter |
| Image-to-video A | Kling AI Premier | Scene dinamis — karakter 2, 3, 5 |
| Image-to-video B | Runway Gen-4.5 | Scene karakter konsisten — karakter 1, 4, 6, 7 + cold open |
| Backup | Seedance 2.0 via fal.ai | Fallback jika Kling/Runway gagal di scene kritis |
| Scoring | Suno AI Pro | Musik tiga fase sesuai arc visual |
| Prompt Reasoning | Gemma 4 26B via OpenRouter | Prompt engineering anchor images, evaluasi konsistensi visual |
| LLM | Claude Max 20x + ChatGPT Pro | Prompt engineering, brainstorming, iterasi seluruh produksi |

---

## Dasar Kalkulasi

| Parameter | Angka | Sumber |
|---|---|---|
| Success rate Kling (wajah manusia, scene dinamis) | 50% | Review independen April 2026 |
| Success rate Runway Gen-4.5 (dengan reference image) | 70% | Review independen April–Mei 2026 |
| Success rate Seedance 2.0 via fal.ai | 90% | Dokumentasi ByteDance + review independen |
| Buffer iterasi per platform | 20% | Konservatif untuk produksi komersial |
| Biaya kredit Kling — 10 dtk Pro model 1080p image-to-video | 200 kredit/clip | Terverifikasi April 2026 |
| Biaya kredit Runway Gen-4.5 — 10 dtk | 250 kredit/clip | Terverifikasi April 2026 |
| Biaya kredit Runway Gen-4 Turbo — 10 dtk (draft) | 50 kredit/clip | Terverifikasi April 2026 |
| Biaya Seedance via fal.ai | ~$0.10/detik video | fal.ai rate card Mei 2026 |

---

## Rincian Per Platform

---

### 1. Midjourney v8.1 Pro
**Fungsi:** Generate anchor images (still images) seluruh karakter sebagai referensi konsisten untuk Kling dan Runway. Stealth Mode aktif — semua generasi privat, tidak masuk galeri publik Midjourney.

**Kalkulasi kebutuhan:**

| Jenis Generasi | Raw | Success Rate | Total Generate |
|---|---|---|---|
| Anchor per karakter — 4 angle × 7 karakter | 28 | 70% | 40 |
| Variasi ekspresi — 3 ekspresi × 7 karakter | 21 | 70% | 30 |
| Style test & kalibrasi mood visual | 30 | — | 30 |
| Still frames cold open abstrak | 10 | 85% | 12 |
| Iterasi revisi | 25 | — | 25 |
| Buffer 20% | — | — | +27 |
| **Total** | | | **~164 generasi** |

Kapasitas Pro plan: ~1.800 gambar fast/bulan + unlimited Relax mode.
164 generasi vs kapasitas 1.800 fast = **satu subscribe sangat cukup, dua subscribe untuk buffer iterasi bulan kedua.**

| Item | Harga | Subscribe | Total |
|---|---|---|---|
| Midjourney Pro | $60 | × 2 | **$120** |

---

### 2. Kling AI Premier
**Fungsi:** Image-to-video untuk scene dinamis — karakter 2 (pemuda komunitas, laptop), karakter 3 (kurir di motor), karakter 5 (pengusaha menengah, showroom).

**Kalkulasi kebutuhan:**

| Scene | Shot | Kredit/Shot | Subtotal Diterima |
|---|---|---|---|
| K2 — Pemuda (30 dtk) | 3 shot × 10 dtk | 200 | 600 |
| K3 — Kurir (30 dtk) | 3 shot × 10 dtk | 200 | 600 |
| K5 — Pengusaha (30 dtk) | 3 shot × 10 dtk | 200 | 600 |
| **Subtotal clips diterima** | 9 shot | | **1.800 kredit** |

Koreksi success rate 50%:
9 shot ÷ 50% = 18 shot harus digenerate → 18 × 200 = 3.600 kredit
Tambah buffer 20%: 3.600 × 1.2 = **~4.320 kredit dibutuhkan**

Kapasitas Premier: 8.000 kredit/bulan.
Subscribe pertama: produksi utama (sisa ~3.680 kredit untuk iterasi).
Subscribe kedua: revisi scene, shot ulang, penyesuaian pasca-assembly.

| Item | Harga | Subscribe | Total |
|---|---|---|---|
| Kling AI Premier | $65 | × 2 | **$130** |

---

### 3. Runway Gen-4.5
**Fungsi:** Image-to-video untuk scene yang membutuhkan konsistensi wajah tinggi — karakter 1 (ibu rumah tangga, anchor 40 dtk), karakter 4 (profesional perempuan), karakter 6 (tokoh komunitas), karakter 7 (eksekutif korporat), dan cold open abstrak (10 dtk).

**Strategi iterasi:** Draft di Gen-4 Turbo (50 kredit/10 dtk) → locking prompt → render final di Gen-4.5 (250 kredit/10 dtk). Workflow ini memangkas kredit iterasi hingga 80%.

**Kalkulasi kebutuhan:**

| Scene | Shot | Draft Turbo | Final Gen-4.5 | Subtotal |
|---|---|---|---|---|
| K1 — Ibu (40 dtk, anchor) | 4 shot × 10 dtk | 4 × 2x × 50 = 400 | 4 × 250 = 1.000 | 1.400 |
| K4 — Profesional (30 dtk) | 3 shot × 10 dtk | 3 × 2x × 50 = 300 | 3 × 250 = 750 | 1.050 |
| K6 — Tokoh komunitas (30 dtk) | 3 shot × 10 dtk | 3 × 2x × 50 = 300 | 3 × 250 = 750 | 1.050 |
| K7 — Eksekutif (30 dtk) | 3 shot × 10 dtk | 3 × 2x × 50 = 300 | 3 × 250 = 750 | 1.050 |
| S0 — Cold open (10 dtk) | 2 shot × 5 dtk | 4 × 2x × 25 = 200 | 2 × 125 = 250 | 450 |
| **Subtotal** | 15 shot | 1.500 | 3.500 | **5.000 kredit** |

Tambah buffer 20%: 5.000 × 1.2 = **~6.000 kredit dibutuhkan**

Alokasi subscribe:
- Subscribe 1 (Max $76): 9.500 kredit → produksi utama + buffer besar
- Subscribe 2 (Pro $28): 2.250 kredit → revisi dan finalisasi

| Item | Harga | Subscribe | Total |
|---|---|---|---|
| Runway Gen-4.5 Max | $76 | × 1 | $76 |
| Runway Gen-4.5 Pro | $28 | × 1 | $28 |
| **Subtotal Runway** | | | **$104** |

---

### 4. Seedance 2.0 via fal.ai
**Fungsi:** Backup fallback — diaktifkan hanya jika Kling atau Runway gagal menghasilkan clip acceptable setelah 3x iterasi pada scene tertentu. Bukan subscription — pay-as-you-go per detik video.

**Akses:** fal.ai sebagai third-party API wrapper yang mendukung real human faces dan pembayaran internasional. Harness Python sederhana (30–50 baris), setup satu kali.

**Kalkulasi:**

| Skenario | Scene Gagal | Detik Total | @$0.10/dtk | Total |
|---|---|---|---|---|
| Ringan (2 scene) | 2 | 60 dtk | $0.10 | $6 |
| Sedang (4 scene) | 4 | 120 dtk | $0.10 | $12 |
| Berat (7 scene) | 7 | 140 dtk | $0.10 | $14 |

Dengan success rate Seedance 90%, hampir semua generasi langsung diterima — reroll sangat jarang.

**Budget ditetapkan flat sebagai contingency:**

| Item | Jenis | Total |
|---|---|---|
| Seedance 2.0 via fal.ai | Pay-as-you-go contingency | **$20** |

---

### 5. Suno AI Pro
**Fungsi:** Generate tiga stem musik terpisah sesuai arc visual (D-014):
- Stem Fase 1: Drone elektronik disonan — cold open
- Stem Fase 2: Organik hangat membangun — scene karakter
- Stem Fase 3: Full swell → resolve chord hangat — konvergensi + penutup

Stem terpisah per fase memberi editor fleksibilitas mixing penuh.

**Kalkulasi kebutuhan:**

| Kebutuhan | Generasi | Kredit (5/generasi) |
|---|---|---|
| Stem Fase 1 — drone elektronik | 15 | 75 |
| Stem Fase 2 — organik hangat, 3 varian | 25 | 125 |
| Stem Fase 3 — full swell + resolve | 15 | 75 |
| Eksperimen transisi antar fase | 10 | 50 |
| Versi alternatif untuk approval stakeholder | 15 | 75 |
| Buffer 20% | — | +80 |
| **Total** | **~80 generasi** | **~480 kredit** |

Kapasitas Pro: 2.500 kredit/subscribe.
Subscribe pertama: eksperimen dan draft scoring.
Subscribe kedua: revisi pasca-approval stakeholder dan penyesuaian timing terhadap video assembly final.

| Item | Harga | Subscribe | Total |
|---|---|---|---|
| Suno AI Pro | $10 | × 2 | **$20** |

---

### 6. Claude Max 20x
**Fungsi:** Prompt engineering panjang, konsistensi naratif antar scene, analisis anchor images, iterasi script VO, problem-solving teknis sepanjang produksi. Rate limit 20x lebih tinggi dari Pro — tidak terpotong di tengah sesi panjang.

| Item | Harga | Subscribe | Total |
|---|---|---|---|
| Claude Max 20x | $200 | × 2 | **$400** |

---

### 7. ChatGPT Pro
**Fungsi:** Komparasi pendekatan prompt, variasi kreatif via GPT-5.x, akses DALL-E untuk test visual thumbnail cepat, brainstorming paralel dengan Claude untuk validasi silang keputusan kreatif.

| Item | Harga | Subscribe | Total |
|---|---|---|---|
| ChatGPT Pro | $200 | × 2 | **$400** |

---

## Honor Tenaga Ahli (Tim Produksi Manusia)

Bagian ini mencakup honor empat tenaga ahli inti yang menjalankan produksi dari konsep hingga final cut. Angka dalam Rupiah, ditetapkan sebagai **honor proyek** (bukan gaji bulanan) untuk satu siklus produksi penuh (~1–1,5 bulan kerja intensif).

**Model penetapan:** tiga-lane terdiferensiasi. Director sebagai jangkar senior lintas-fase; tiga eksekutor dikalibrasi pada bobot beban kerja masing-masing lane (45–56% dari honor director). Angka diverifikasi terhadap pita pasar kreatif Indonesia 2025–2026 (editor senior Rp 8–15+ jt/bln; motion graphic senior Rp 12–20 jt/bln; engagement proyek freelance flagship duduk di atas pita gaji bulanan).

| Peran | Lane / Tanggung Jawab | Honor |
|---|---|---|
| **Director** | Pimpin seluruh fase: konsep + naskah → deck → generate ide ke gambar → video + music + scoring + dubbing | **Rp 25.000.000** |
| **Editor / Picture-Lock** | Adobe Premiere: rough assembly, gabung AI + live actor, VO dubbing sync, sound mix, kunci timeline (picture lock) | **Rp 14.000.000** |
| **AI Generation Artist** | Midjourney + Runway + Kling + Seedance + harness Gemma 4; anchor consistency, generasi seluruh klip AI | **Rp 13.000.000** |
| **Motion Graphics & Finishing** | S15 konvergensi (7-panel merge), S16 data segment, color grade, integrasi scoring | **Rp 11.000.000** |
| **Subtotal Honor Tenaga Ahli** | | **Rp 63.000.000** |

**Dasar diferensiasi:**
- **Editor / Picture-Lock (Rp 14 jt)** — beban tunggal terberat dan engagement paling panjang; memikul integrasi seluruh timeline (AI + live) sampai terkunci.
- **AI Generation Artist (Rp 13 jt)** — volume iterasi tertinggi (success rate platform 50–70% → reroll besar), paling banyak platform, premium kelangkaan skill.
- **Motion Graphics & Finishing (Rp 11 jt)** — skill spesialis (S15/S16 ditandai keputusan motion-graphics di pipeline), tetapi window kerja lebih pendek dari dua lane di atas.

> **Catatan scope:** Honor ini murni untuk empat tenaga ahli inti. Biaya fisik syuting live (lokasi, sewa kamera/lighting, talent/aktor, wardrobe) dan voice talent + studio dubbing **tidak** termasuk di sini — dianggarkan terpisah di RAB Syuting Live.

---

## Rekapitulasi Total

### A. Biaya Platform / Tools

| # | Platform | Fungsi | Subscribe | Total |
|---|---|---|---|---|
| 1 | Midjourney v8.1 Pro | Anchor images | $60 × 2 | $120 |
| 2 | Kling AI Premier | Video scene dinamis | $65 × 2 | $130 |
| 3a | Runway Gen-4.5 Max | Video scene konsisten (produksi) | $76 × 1 | $76 |
| 3b | Runway Gen-4.5 Pro | Video scene konsisten (revisi) | $28 × 1 | $28 |
| 4 | Seedance 2.0 / fal.ai | Backup contingency | Pay-as-you-go | $20 |
| 5 | Suno AI Pro | Scoring musik | $10 × 2 | $20 |
| 6 | Claude Max 20x | LLM — prompt & produksi | $200 × 2 | $400 |
| 7 | ChatGPT Pro | LLM — brainstorming | $200 × 2 | $400 |
| 8 | Gemma 4 26B / OpenRouter | Prompt reasoning layer | Top-up $20 (one-time) | $20 |
| | **Subtotal Platform** | | | **$1.214** |

### B. Honor Tenaga Ahli

| # | Peran | Honor |
|---|---|---|
| 1 | Director | Rp 25.000.000 |
| 2 | Editor / Picture-Lock | Rp 14.000.000 |
| 3 | AI Generation Artist | Rp 13.000.000 |
| 4 | Motion Graphics & Finishing | Rp 11.000.000 |
| | **Subtotal Honor** | **Rp 63.000.000** |

---

## Konversi & Total Keseluruhan

| Komponen | USD | IDR (kurs Rp 16.300/USD) |
|---|---|---|
| A. Biaya Platform / Tools | $1.214 | ~Rp 19.800.000 |
| B. Honor Tenaga Ahli | — | Rp 63.000.000 |
| **TOTAL KESELURUHAN** | | **~Rp 82.800.000** |

*Kurs estimasi Juni 2026. Honor tenaga ahli mendominasi (~76% dari total) — wajar untuk produksi padat tenaga manusia. Biaya fisik syuting live dianggarkan terpisah di RAB Syuting Live.*

---

## Distribusi Biaya

| Kategori | Biaya | Proporsi |
|---|---|---|
| LLM (Claude + ChatGPT) | $800 | 66% |
| Video generation (Kling + Runway + Seedance) | $254 | 21% |
| Text-to-image (Midjourney) | $120 | 10% |
| Prompt reasoning (Gemma 4 / OpenRouter) | $20 | 2% |
| Scoring (Suno) | $20 | 2% |

---

## Tidak Termasuk dalam RAB Ini

> Catatan: labor editing, post-production, motion graphics, dan sound mixing **sudah termasuk** dalam Honor Tenaga Ahli (Editor/Picture-Lock + Motion Graphics & Finishing). Yang tersisa di luar RAB ini adalah biaya fisik syuting live, voice talent, dan lisensi software.

| Item | Keterangan |
|---|---|
| Syuting live actor (fisik) | Lokasi, sewa kamera, lighting, crew lapangan, wardrobe — di RAB Syuting Live |
| Voice talent dubbing | Honor pengisi suara + sewa studio rekaman (sync dubbing dikerjakan Editor) |
| Lisensi software editing | Adobe Premiere Pro / DaVinci Resolve (langganan, jika belum dimiliki) |
| Setup harness fal.ai | Waktu developer ~2–4 jam, tidak ada biaya platform |

---

### 8. Gemma 4 26B via OpenRouter
**Fungsi:** Prompt reasoning layer di atas Midjourney — menerima brief scene + anchor image yang sudah digenerate, menghasilkan prompt Midjourney yang terstruktur dan presisi, mengevaluasi konsistensi visual antar karakter. Berjalan sebelum setiap sesi generasi Midjourney.

**Model:** Gemma 4 26B A4B (google/gemma-4-26b-a4b-it) via OpenRouter
- Thinking mode aktif untuk chain-of-thought reasoning visual
- Vision input: menerima anchor image sebagai referensi evaluasi
- Context window 256K — cukup untuk membawa seluruh brief produksi dalam satu prompt
- Apache 2.0, tidak ada data retention untuk training

**Mengapa OpenRouter (bukan oMLX lokal):**
Pilihan ini didasarkan pada kebutuhan produksi yang akan menggunakan MacBook M2/M3. oMLX adalah local inference server yang membutuhkan model tersimpan lokal (~14GB) dan minimal 16GB unified memory. OpenRouter menghilangkan constraint hardware — berjalan dari Mac berapapun spec-nya, tanpa storage tambahan, tanpa setup infrastruktur.

**Kalkulasi biaya:**

| Parameter | Angka |
|---|---|
| Biaya per 1M input tokens | $0.06 |
| Biaya per 1M output tokens | $0.33 |
| Estimasi per session (thinking mode + image) | ~$0.001 |
| Total sessions seluruh produksi (~500 sessions) | ~$0.50 |
| Buffer eksperimen & iterasi tak terduga (40×) | ~$20 |

Top-up $20 memberikan buffer 40× di atas estimasi aktual. Kredit OpenRouter tidak expire — sisa kredit tersimpan untuk sesi produksi berikutnya.

> ⚠️ **Catatan platform fee:** OpenRouter mengenakan 5.5% credit card fee dengan minimum $0.80 per top-up. Top-up $20 efektif menjadi $21.10 setelah fee.

| Item | Jenis | Total |
|---|---|---|
| OpenRouter credit top-up | One-time, tidak expire | **$20** |

---

*RAB Final v2.0 · Semesta Digital (working title) · 8 Juni 2026*
*Platform: Kling (scene dinamis) + Runway (scene konsisten) + Seedance/fal.ai (backup)*
*Lihat juga: 00-project-charter.md · 01-concept-document.md · 02-production-brief.md*
