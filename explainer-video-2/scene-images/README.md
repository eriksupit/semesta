---
title: Scene Images — Konvensi Penyimpanan Keyframe
tags: [explainer-video-2, scene-images, keyframe, convention]
status: active
created: 2026-06-18
updated: 2026-06-18
---

# Scene Images — Tempat Seluruh Keyframe

Folder ini menampung semua gambar keyframe hasil ChatGPT Image v2, **satu subfolder per scene** (`sc01`–`sc15`, sesuai 15 scene di `01-storyline.md` / `05-pipeline-produksi.md`).

## Konvensi penamaan file (per pipeline §1 koreksi 2 & 4)
Keyframe disimpan **per segmen 5 detik**, berpasangan start→end. Aturan sambung: end-frame segmen-N = start-frame segmen-(N+1).

```
sc<NN>_seg<M>_start.png
sc<NN>_seg<M>_end.png
```
Contoh `sc02` (subuh, 2 segmen):
```
scene-images/sc02/sc02_seg1_start.png
scene-images/sc02/sc02_seg1_end.png      # = start seg2 (boleh di-symlink/duplikat sebagai sc02_seg2_start.png)
scene-images/sc02/sc02_seg2_start.png
scene-images/sc02/sc02_seg2_end.png
```

## Aturan
- Hanya simpan keyframe **terpilih & lolos GATE C** (akurat + konsisten identitas). Kandidat yang ditolak jangan ditaruh di sini (pakai subfolder `_rejected/` per scene bila perlu arsip).
- Jumlah segmen per scene ditetapkan saat detail adegan disusun (GATE A) — lihat tabel status di `05-pipeline-produksi.md`.
- Status keyframe per scene dilacak di kolom **Keyframe (C)** tabel `05-pipeline-produksi.md`.
