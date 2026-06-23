---
title: Review Checklist — GATE B Keyframes (explainer-video-2)
tags: [explainer-video-2, gate-b, keyframe, review, pilot]
status: active
created: 2026-06-23
updated: 2026-06-23
aliases: [ev2-gateB-review-checklist]
---

# Review Checklist — GATE B Keyframes

Rubrik lolos/tolak per keyframe yang digenerate. Reviewer (Claude) membandingkan PNG hasil LANGSUNG ke plat acuan (bukan dari ingatan). Tiap kriteria = PASS / FAIL / N/A + catatan bukti. Ini juga tulang punggung PILOT REPORT.

> Konteks aturan → [[README]] + [[SEQ1-SC01]]. Plat wajah → `character-images/`. Plat ruang → `environment-images/`.

## Cara pakai
1. Simpan PNG ke `scene-images/sc<NN>/` (konvensi nama lihat `scene-images/README.md`).
2. Reviewer baca PNG + plat wajah + plat ruang yang di-attach shot itu.
3. Isi 8 kriteria. **Tolak bila ada 1+ FAIL pada kriteria KERAS (K).** Kriteria lunak (L) yang gagal = catat, boleh accept bila tak merusak naratif.
4. Verdict: ACCEPT / REVISE (sebut token mana diubah) / REGEN.

## 8 kriteria

| # | Kriteria | Tipe | PASS bila | FAIL bila |
|---|---|---|---|---|
| 1 | **Identity-lock wajah** | K | Fitur tokoh cocok plat wajah: bentuk wajah, etnis, kumis/rambut salt-and-pepper, usia matang, tahi-lalat/ciri khas | Wajah drift (orang lain), umur meleset, kumis/rambut beda, ciri khas hilang |
| 2 | **Konsistensi ruang** | K | Furnitur + layout + artwork (Hokusai) + material cocok plat ruang; objek tidak berhalusinasi/melt | Furnitur beda, artwork salah, objek tak-ada-di-plat muncul, layout flip |
| 3 | **State / ekspresi (Lapis-4)** | K | Sesuai blok shot: bangun-tidur=kucel (kelopak berat, sleep-creased, bed-head), aksi & pose benar | Ekspresi salah (mis. wajah plat rapi-netral saat harusnya kucel), aksi tak sesuai |
| 4 | **Layar OFF (ADDENDUM A1)** | K | Semua layar device gelap/OFF; ruang layar bersih untuk AE | Ada UI/teks/kartu/grafik ter-render di layar (harusnya di AE) |
| 5 | **Arah kamera** | K | HP dipegang=punggung-ke-kamera/layar-ke-subjek; HP tergeletak=top-down layar-OFF; angle off-axis | Layar HP diputar ke kamera; angle klise center/eye-level frontal |
| 6 | **Grade hangat tanpa drift** | L | Redup hangat sesuai jam; midtone slightly warm; latar gelap natural | Drift kuning berlebih; garmen ikut menguning; over-bright tak sesuai jam |
| 7 | **Garmen afirmatif (anti auto-batik)** | L | Garmen polos desaturated sesuai wardrobe shot | Muncul motif batik/pattern tak diminta |
| 8 | **Rasio + framing** | L | 16:9; framing sesuai token shot | Rasio salah; framing meleset jauh dari maksud shot |

## Catatan pilot khusus
- **Cahaya layar di wajah (SH03)** = harus dari `lighting` (screen-glow underlight), BUKAN layar nyala. PASS bila wajah tersorot hangat tapi layar tetap OFF.
- **Continuity HP**: SH03 HP dipegang → SH04 HP telungkup di nakas (cek arah & posisi konsisten antar-shot).
- **Wardrobe transition SH04**: START sleep-tee → END sleep-tee + sarung lilit pinggang (cek sarung polos desaturated, bukan batik).
- **Bookend**: SH01 motif mata (CU wajah, mata focal point) — END mata terbuka harus jelas terbaca untuk gerak buka-mata di Kling i2v.

## Log review (diisi saat tiap keyframe masuk)
| Keyframe | File | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | Verdict |
|---|---|---|---|---|---|---|---|---|---|---|
| SH01-START | `scene-images/sc01/sc01_sh01_start.png` (regen) | PASS | PASS (parsial, MCU — uji penuh di SH04) | PASS | N/A | PASS | PASS | PASS | PASS (render melebar ke MCU, token diselaraskan) | **ACCEPT** |
| SH01-END | `scene-images/sc01/sc01_sh01_end.png` | PASS | PASS (match START) | PASS (mata terbuka ke lensa) | N/A | PASS | PASS | PASS | PASS (MCU, kontinuitas ketat vs START) | **ACCEPT** — metode END-anchor-ke-render-START TERVALIDASI |
| SH02-START | — | | | | | | | | | ⏳ |
| SH02-END | — | | | | | | | | | ⏳ |
| SH03-START | — | | | | | | | | | ⏳ |
| SH03-END | — | | | | | | | | | ⏳ |
| SH04-START | — | | | | | | | | | ⏳ |
| SH04-END | — | | | | | | | | | ⏳ |
