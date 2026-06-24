---
title: INDEX — Explainer Video 2 (Konsep "Satu Keluarga, Satu Hari Penuh")
tags: [explainer-video-2, index, hub, navigation]
status: active
created: 2026-06-18
updated: 2026-06-18
aliases: [ev2-index, explainer-video-2-home]
---

# INDEX — Explainer Video 2
## Konsep "Satu Keluarga, Satu Hari Penuh" · Semesta Digital *(working title)*

Folder `explainer-video-2/` adalah rumah **reboot naratif** explainer video: satu keluarga kelas menengah Jakarta, seharian penuh, untuk audiens **ads provider**. Menggantikan konsep "galeri 7 arketipe" di `explainer-video/`. Durasi target 5 menit (≈300 detik).

---

## Dokumen di folder ini (konsep baru)
| File | Isi | Status |
|---|---|---|
| `00-INDEX.md` | Hub + peta pewarisan (dokumen ini) | active |
| `00-WORKLOG.md` | **Log proses & seluruh keputusan/tindakan**; tersambung ke memory + `/session-anchors` + `scope.md`. Bukan hasil akhir. | live |
| `01-storyline.md` | **Hasil akhir storyline (clean-slate)** — cerita final, tanpa catatan proses | draft-clean |
| `02-storyboard.md` | Storyboard rough per-scene (shot, framing, durasi) | stub |
| `03-scene-detail.md` | Detail per-scene (prosa skenario + shot list + catatan produksi). **GATE A LENGKAP: SEQ1–SEQ6 / 6 babak / 19 scene / 57 shot / ≈312s** | active |
| `04-ad-inventory-map.md` | Lapisan potensi iklan per-scene (untuk dibaca provider); sumber turunan `03`; tiga zona bebas-iklan | stub |
| `05-pipeline-produksi.md` | Pipeline produksi terkoreksi: stack Kling/ChatGPT Image v2, siklus 3-gerbang per-scene, tabel status | active |
| `06-konvensi-naratif.md` | **Konvensi Sequence/Scene/Shot** (kanonik) — ditautkan oleh 02/03/05, tidak disalin | active |
| `07-style-reference.md` | **Referensi gaya GATE 0**: katalog wardrobe/hair/makeup/footwear + anchor artis/expert (costume/makeup warisan `tokens-references`, **hair anchor baru**) + delta cast (hijab/anak/usia-matang/warm-grade) + tabel anchor→tokoh. Mewarisi `tokens-references` via link; dikutip `08` + tiap prompt GATE B | active |
| `08-character-sheet/` | **Character & Wardrobe Sheet (GATE 0)** — subfolder, satu dokumen per tokoh + `00-README.md` (metode + template plat 9-sel view×shot + protokol token-arah). Tiap file: identitas FIXED + matriks plat 9-sel + wardrobe per-scene. Herman selesai (pola); Ratna/Lisa/Andi/figuran berikutnya. Mengutip `07` | draft |
| `scene-images/` | Tempat seluruh keyframe; subfolder per scene + `README.md` konvensi penamaan | active |
| `character-images/` | **Aset plat referensi GATE 0**: PNG white-bg multi-angle per tokoh (di-generate dari prompt di `08`), jangkar konsistensi + reference-locking Kling 3.0. Spesifikasi naskahnya ada di `08-character-sheet/` (per tokoh) + `07-style-reference.md`. Penamaan plat: `<TAG>_<char>_<view>_<shot>.png` (view: front/profileA/profileB) | active |
| `PROMPT-AUDIT-CHECKLIST.md` | **Pre-lock gate audit prompt** — 52 item (A–L) turunan `prompt-rules-image-generation` + `lessons`, ditandai MEK (grep) vs MATA (cek render), tiap baris ber-jejak baris-bukti. Dijalankan sebelum mengunci/generate prompt apa pun (plat/keyframe). Otomasi: skill `/tti-prompt-audit` (`.claude/skills/tti-prompt-audit/`) — jalankan 9 grep MEK + walk MATA + verdict | active |
| `../skills-reference/` | **Mirror reference ter-track** (di luar `.claude/` yang ke-ignore git) untuk sharing ke tim: 5 skill toolkit prompt — `tti-prompt-creator`, `tti-prompt-audit` (project) + `research-before-dispatch`/`brave`/`anti-sycophancy` (global), tiap file ber-header provenance + disiplin re-sync manual | active |

> **Alur kerja:** keputusan disepakati & dicatat di `00-WORKLOG.md` (proses) → setelah matang, dituangkan bersih ke `01-storyline.md` (hasil) → diterjemahkan ke `02`/`03`/`04`.

---

## Pewarisan dari `explainer-video/` (v1) — JANGAN disalin, tetap otoritatif di lokasi aslinya

**Produksi (tidak bergantung cerita, masih sah penuh):**
- `explainer-video/03-rab-produksi-ai.md` — RAB tools + honor tenaga ahli
- `explainer-video/03-a-rab-syuting-live.md` — RAB syuting live
- `explainer-video/04-pipeline-ai-production.md` — pipeline produksi AI
- `explainer-video/04-a-kling3-benchmark-protocol.md` — protokol uji Kling 3.0

> Catatan: bila konsep baru mengubah jumlah scene/durasi final, RAB & pipeline perlu di-review (dampak hilir O4 di `01-storyline.md`). Sampai itu terjadi, dokumen di atas tetap otoritatif.

**Aset deck (milik deliverable LAIN — deck investor/ad-provider, BUKAN video ini):**
- `explainer-video/08-investor-deck-brief.md` + `rough-presentation-image/` (19 PNG) — menggambarkan konsep 7-arketipe LAMA; tetap dipakai untuk DECK, usang untuk VIDEO konsep baru.
- `explainer-video/09-narrative-deck-framework.md` — deck naratif investor
- `explainer-video/11-adprovider-deck-content.md` — konten deck ad-provider (acuan janji ke provider: brand-safe, belonging, high-intent)
- `Semesta Digital — Ad Partnership Deck.pdf`, `Semesta Digital — Visual Scene Proposal.pdf`

**Konteks dasar (tetap otoritatif):**
- `explainer-video/00-project-charter.md`, `01-concept-document.md`, `02-production-brief.md`
- vault root: `Executive Brief.md`, `Proyeksi NU sebagai Co-Founder.md`

**Digantikan oleh folder ini (v1 naratif — arsip, jangan dipakai untuk konsep baru):**
- `explainer-video/05-storyboard-rough.md` → digantikan `02-storyboard.md`
- `explainer-video/06-storyline.md` → digantikan `01-storyline.md`
- `explainer-video/07-live-production-brief.md` → ditinjau ulang (live actor dibuang)
- `explainer-video/10-scene-detail-naskah.md` → digantikan `03-scene-detail.md`

---

*INDEX v1 · 2026-06-18 · Semesta Digital (working title)*
