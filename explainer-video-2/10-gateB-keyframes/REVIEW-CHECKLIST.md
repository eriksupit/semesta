---
title: Review Checklist — GATE B Keyframes (explainer-video-2)
tags: [explainer-video-2, gate-b, keyframe, review]
status: active
created: 2026-06-23
updated: 2026-06-26
aliases: [ev2-gateB-review-checklist]
---

# Review Checklist — GATE B Keyframes

Rubrik lolos/tolak per keyframe yang digenerate. Reviewer (Claude) membandingkan PNG hasil **LANGSUNG** ke plat acuan yang di-attach (bukan dari ingatan). Aligned ke metode **[[prompt-rules-text-image-to-image]]** (enforcement G0–G6) + [[prompt-rules-image-generation]] (token discipline).

> Plat wajah → `character-images/`. Plat ruang → `environment-images/`. Konvensi nama gambar → `scene-images/README.md`.

## Cara pakai
1. User simpan PNG ke `scene-images/sc<NN>/`.
2. Reviewer baca PNG + tiap plat (env + identity) + (utk END) render START yang di-anchor.
3. Jalankan **PRE-EMIT GATE** (sebelum verdict) lalu **8 kriteria**.
4. Verdict: **ACCEPT** (→ rename gambar ke `sc<NN>_sh<MM>_{start,end}.png` + tulis prompt terbukti ke slot file scene) / **REVISE** (sebut slot/token mana diubah) / **REGEN**.
5. Tolak bila ada 1+ FAIL pada kriteria KERAS (K). Kriteria lunak (L) gagal = catat, boleh accept bila tak merusak naratif.

## PRE-EMIT GATE (G0–G6 — metode) — cek SEBELUM menilai render
- **G0 Plate-state:** tak ada verba aksi yang menciptakan/menaruh objek yang plat-nya sudah menampilkannya final (anti double-object).
- **G1 Mode declared:** frame dideklarasi A/B/C; tiap lapis LOCKED (dirujuk) atau CHANGED (delta) — lapis terkunci TAK ditulis ulang (Mode C).
- **G2 Reference completeness:** tiap orang/objek/ruang yang disebut prompt punya plat ter-attach (plat WAJAH hanya bila wajah tampak).
- **G3 Subject-count:** ≤1 face-locked (+1 soft) — atau saf multi-figur memakai iterative-build (Rule 8a), bukan sekali-jadi.
- **G4 Framing:** multi-figur medium/tighter + kompensasi drift-wider (spec satu tingkat lebih ketat).
- **G5 Consistency burden:** establishing dibangun (bukan didekomposisi jadi banyak gambar final).
- **G6 Camera-lock:** END berbagi framing/angle/camera START (L6 LOCKED). Delta-kecil → **END = edit-in-place pada render START** (geometri terkunci by-construction); generate-from-attachment = fallback. Gerak kamera = L6-DELTA deklaratif yang melepas jaminan konsistensi.

## 8 kriteria (nilai render)
| # | Kriteria | Tipe | PASS bila | FAIL bila |
|---|---|---|---|---|
| 1 | **Identity-lock wajah** | K | Fitur tokoh cocok plat wajah (bentuk wajah, etnis, usia, ciri khas) | Wajah drift (orang lain), umur meleset, ciri khas hilang |
| 2 | **Konsistensi ruang** | K | Furnitur + layout + artwork + material cocok plat ruang; nol objek halusinasi/melt | Furnitur/artwork beda, objek tak-ada-di-plat muncul, layout flip |
| 3 | **Plate-state (no duplikat)** | K | Objek yang aksi-nya menciptakan TIDAK ganda; objek ter-bake tidak terhapus paksa | Double-object (mis. karpet di atas karpet); objek aksi hilang |
| 4 | **State/ekspresi (Lapis-4)** | K | Sesuai blok shot (kucel saat bangun, aksi & pose benar) | Ekspresi/aksi salah (mis. wajah plat rapi-netral saat harusnya kucel) |
| 5 | **Layar OFF (ADDENDUM A1)** | K | Semua layar device gelap/OFF/dormant (glow + UI = AE; kartu iklan = grafis terbang, occlusion layar oleh tangan/objek OK — staging natural) | Ada UI/teks/kartu/glow ter-render di layar oleh AI |
| 6 | **Arah kamera + camera-lock** | K | HP punggung-ke-kamera/insert-top-down; angle off-axis; START/END framing-angle IDENTIK (kecuali L6-DELTA dideklarasi) | Layar diputar ke kamera; angle klise; START/END geser framing tak-sengaja |
| 7 | **Subject-count terjaga** | K | Jumlah figur face-locked sesuai (≤1+soft per generasi build); posisi tidak tertukar | Figur tertukar posisi, identitas merge, figur rontok |
| 8 | **Grade + garmen + rasio** | L | Hangat sesuai jam, midtone slightly warm; garmen polos desaturated (anti-batik); 16:9; framing sesuai | Drift kuning; motif batik tak diminta; rasio/framing meleset |

## Log review (diisi saat tiap keyframe masuk)
*(reset 2026-06-26 — produksi di-reboot ke metode 3-mode; render lama SC01 = arsip metode lama, tidak di-log di sini)*

| Keyframe | File | G0–G6 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | Verdict |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| — | — | | | | | | | | | | ⏳ |
