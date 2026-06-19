---
title: Superapp — Home
aliases:
  - Home
  - Peta Induk
  - MOC
type: index
status: active
created: 2026-05-13
updated: 2026-06-09
tags:
  - superapp
  - moc
---

# Semesta Digital — Peta Induk Vault
*(working title -- nama final dikunci setelah investor & stakeholder approve)*

> [!abstract] Tentang vault ini
> Basis pengetahuan untuk konsep **Semesta Digital** -- superapp *integrated-marketplace* dengan **fairness engine** sebagai prinsip operasional. Dokumen mentah `.docx` diarsipkan di `raw-kb/`; catatan Markdown di bawah adalah versi yang dapat dibaca, dicari, dan ditautkan di Obsidian.

---

## Navigasi Utama

### ⚙️ Meta -- Project Management
File-file ini dibaca Claude di setiap sesi sebelum bekerja.

- [[context]] -- konteks aktif sesi yang sedang berjalan
- [[scope]] -- batas scope sesi aktif
- [[lessons]] -- preferensi user yang tervalidasi + insight antar sesi
- [[prompt-rules-image-generation]] -- **WAJIB DIBACA** sebelum menulis prompt image generation apapun. Struktur granular = standar wajib semua scene. `on_screen_graphic` + `graphic_proximity` (CSS positioning logic) untuk Teknik 2 floating UI. Berlaku untuk GPT Image 2, Midjourney, Kling, Runway, Seedance. Diupdate setiap ada lessons baru.
- [[tokens-references/TOKENS-REFERENCE]] -- **REFERENSI TOKEN** lengkap: shot size, camera angle, composition, pose, gesture, expression, makeup, wardrobe, hair, footwear, atmosphere. Gunakan untuk variasi visual antar scene.
- [[tokens-references/CREW-REFERENCE]] -- **REFERENSI CREW** lengkap: director, lighting director, production designer, costume designer, makeup artist — parent-child pairs untuk Lapis 6. Quick reference table semua 18 scene.
- [[tokens-references/INTERIOR-DESIGN-REFERENCE]] -- **REFERENSI INTERIOR DESIGN** lengkap: 31 style dengan material tokens, designer anchor per style, scene-to-style mapping semua 18 scene, material token library.
- [[handoff/00-project-instructions-source]] -- source teks project instructions Claude Project

### 🛠 Skills
- `.claude/skills/session-anchors/SKILL.md` -- membaca dan menulis semua anchor files (context/scope/lessons/handoff).

### 📚 Knowledge Base

- [[knowledge-base/Executive Brief]]
- [[knowledge-base/Ikhtisar Naratif]]
- [[knowledge-base/Proyeksi NU sebagai Co-Founder]]

### 🎬 Explainer Video

- [[explainer-video/00-project-charter]]
- [[explainer-video/01-concept-document]]
- [[explainer-video/02-production-brief]]
- [[explainer-video/03-rab-produksi-ai]] -- RAB tools + **Honor Tenaga Ahli v3.0** (model tiga-lane Rp 63 jt)
- [[explainer-video/03-a-rab-syuting-live]] -- **RAB Syuting Live v2.0** (set tetap, tier profesional ~Rp 65,5 jt). Total produksi keseluruhan ~Rp 148,3 jt
- [[explainer-video/04-pipeline-ai-production]]
- [[explainer-video/05-storyboard-rough]]
- [[explainer-video/06-storyline]]
- [[explainer-video/07-live-production-brief]]
- [[explainer-video/08-investor-deck-brief]] -- ✅ master brief deck VISUAL, **19/19 ilustrasi APPROVED** (S0–S17b, +3 added: S12b/S14b/S17b); S15/S16 dilepas (video-only)
- [[explainer-video/09-narrative-deck-framework]] -- deck NARATIF **INVESTOR** v1 (17 slide, capital raise) — audiens investor, artefak terpisah
- [[explainer-video/10-scene-detail-naskah]] -- 🆕 detail+naskah per-scene (19 entri) untuk halaman detail deck visual (upload ke Claude Design)
- [[explainer-video/11-adprovider-deck-content]] -- 🆕 **deck PROVIDER IKLAN — KONTEN FINAL design-ready** (15 slide, angka eksplisit, slide 12 placeholder); Claude Design tinggal melayout
- `handoff/HANDOFF-CLAUDE-DESIGN-2026-06-10.md` + `INITIAL-PROMPT-…txt` -- ✅ handoff deck visual (upload-ready, manifes 19 gambar)
- `explainer-video/docx-export/` -- ✅ **9 dokumen versi .docx format awam** (Hybrid: Level 2 glosarium untuk 01/02/03/03-a/08, Level 1 untuk 04/05/06/07)

### 🖼️ Rough Presentation Images

- `explainer-video/rough-presentation-image/S0-cold-open.png` -- ✅ approved
- `explainer-video/rough-presentation-image/S1-live-actor-pembuka.png` -- ✅ approved
- `explainer-video/rough-presentation-image/S2-ibu-rumah-tangga.png` -- ✅ approved
- `explainer-video/rough-presentation-image/S3-live-actor-transisi-1.png` -- ✅ approved (S3-M anchor dikunci)
- `explainer-video/rough-presentation-image/S4-pemuda-komunitas-v2.png` -- ✅ approved (Tropical Modernism Geoffrey Bawa validated)
- S5–S17 -- 🔄 pending generate

### 📦 Handoff

- `handoff/HANDOFF-2026-06-09-DOCX.md` -- **handoff terbaru** (konversi 9 dokumen → .docx SELESAI)
- `handoff/INITIAL-PROMPT-2026-06-09-DOCX.txt`
- `handoff/HANDOFF-2026-06-09-RAB.md` -- handoff sesi RAB (konversi DOCX, kini selesai)
- `handoff/INITIAL-PROMPT-2026-06-09-RAB.txt`
- `handoff/HANDOFF-2026-06-10-S8.md` -- handoff image generation (lanjutan generate S5–S17)
- `handoff/INITIAL-PROMPT-2026-06-10-S8.txt`

### 🗄️ Arsip Sumber
- `raw-kb/` -- dokumen `.docx` asli

---

## Status Proyek

| Area | Status | Catatan |
|---|---|---|
| Konsep & dokumen inti | ✅ Selesai | knowledge-base/ |
| Explainer video 01–08 | ✅ Selesai | explainer-video/ |
| Prompt rules image generation | ✅ Selesai | prompt-rules-image-generation.md — struktur granular + on_screen_graphic/graphic_proximity CSS positioning |
| Arsitektur prompt granular | ✅ Tervalidasi | S0 (subject_anchor) + S1 (character_anchor) + S2 (on_screen_graphic Teknik 2) approved sebagai patokan |
| Illustration images S0–S2 | ✅ Approved | rough-presentation-image/ (3/18) |
| Illustration images S3–S17 | 🔄 In Progress | 15 tersisa (S3 approved), prompt full granular siap generate |
| Tokens Reference | ✅ Selesai | tokens-references/TOKENS-REFERENCE.md — shot size, angle, composition, pose, gesture, expression, makeup, wardrobe, hair, footwear, atmosphere |
| Claude Design deck | ⏳ Pending | setelah 18 gambar approved |
| Nama produk final | ⏳ Pending | Masih "Semesta Digital" (working title) |

---

## Tindak Lanjut

- [x] S3 APPROVED — anchor S3-M dikunci (MA-1 bomber + night bazaar expansive plaza)
- [ ] Generate S4–S17 dengan struktur granular standar + tokens dari TOKENS-REFERENCE.md, simpan di `explainer-video/rough-presentation-image/`
- [ ] Anchor F (S1-F) → copy verbatim ke S5/S9/S13; anchor M (S3-M) → copy verbatim ke S7/S11/S17
- [ ] Buat handoff + initial-prompt ke Claude Design setelah semua 18 gambar approved
- [ ] Verifikasi angka Slide 17 (Segmen Data) dengan data aktual
- [ ] Lengkapi Slide 18 (The Ask) dan Slide 20 (Team) dari founding team
- [ ] Tetapkan nama produk final

---

*Catatan: S1-with-graphics (lima vertikal) DI-DROP — S1 plain final.*
