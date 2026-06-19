---
title: Character Images — Konvensi Penyimpanan Plat Referensi (GATE 0)
tags: [explainer-video-2, character-images, reference-plate, gate-0, convention]
status: active
created: 2026-06-19
updated: 2026-06-19
---

# Character Images — Plat Referensi Karakter (GATE 0)

Folder ini menampung **plat referensi white-bg multi-angle** hasil ChatGPT Image v2, **satu subfolder per karakter** (paralel dengan konvensi `scene-images/`). Plat dipakai sebagai jangkar konsistensi prompt GATE B **dan** set reference-locking Kling 3.0 (3–5 gambar). Naskah promptnya ada di `08-character-sheet/<file karakter>.md`.

## Struktur folder
```
character-images/
  H_herman/    R_ratna/    L_lisa/    A_andi/    F_figurans/
```
Subfolder per tokoh diberi nama `<TAG>_<char>` (TAG: H/R/L/A/F).

## Konvensi penamaan file
9 plat per tokoh utama = 3 view × 3 shot:
```
<TAG>_<char>_<view>_<shot>.png
```
- **view** ∈ `front` · `profileA` · `profileB` — **JANGAN pakai `left`/`right`** (model t2i tidak andal soal arah; lihat `08-character-sheet/00-README.md` §3.1).
- **shot** ∈ `full` · `medium` · `closeup`.

Contoh `H_herman/`:
```
H_herman_front_full.png      H_herman_front_medium.png      H_herman_front_closeup.png
H_herman_profileA_full.png   H_herman_profileA_medium.png   H_herman_profileA_closeup.png
H_herman_profileB_full.png   H_herman_profileB_medium.png   H_herman_profileB_closeup.png
```
Figuran (`F_figurans/`) lebih ringkas: `front` + `profileA`, shot kunci saja.

## Aturan
- Hanya simpan plat **lolos GATE 0** (akurat + konsisten identitas). Kandidat gagal → subfolder `_rejected/` per tokoh.
- **Urutan generate:** `front` dulu (jangkar) → `profileA` → `profileB` digenerate sebagai **mirror profileA via reference-image upload**, bukan token "kiri/kanan". Verifikasi tiap render dari pipi/telinga yang tampak sebelum simpan.
- Plat = baseline outfit netral (bukan wardrobe per-scene). Wardrobe per-scene dipakai nanti di keyframe GATE B, bukan di plat.
