---
title: README — GATE B Keyframes (explainer-video-2)
tags: [explainer-video-2, gate-b, keyframe, readme]
status: active
created: 2026-06-23
updated: 2026-06-26
aliases: [ev2-gateB-readme]
---

# GATE B Keyframes — README

Folder ini menyimpan **prompt keyframe per-scene** untuk produksi gambar (ChatGPT Image v2 = GPT-Image class). Tiap file = satu scene (`SEQ<n>-SC<nn>.md`), berisi prompt tiap shot-nya. User generate eksternal; Claude author + review + assemble-spec. Claude TIDAK pernah generate.

## 📂 Konvensi penyimpanan (WAJIB)
- **Prompt scene disimpan DI SINI:** `explainer-video-2/10-gateB-keyframes/SEQ<n>-SC<nn>.md` — satu file per scene, satu blok prompt per keyframe (START + END).
- **Gambar hasil generate disimpan di:** `explainer-video-2/scene-images/sc<NN>/` — nama final per konvensi `sc<NN>_sh<MM>_{start,end}.png` (lihat `scene-images/README.md`). **Hanya simpan yang sudah ACCEPT.**
- Alur: author prompt di sini → user generate → review (REVIEW-CHECKLIST) → **ACCEPT → rename gambar ke nama final di `scene-images/` + prompt terbukti menggantikan slot kosong di file scene ini**.

## 📐 Metode prompting (BINDING — kanonik, jangan diputuskan ulang)
Aturan penuh di **[[prompt-rules-text-image-to-image]]** (dibangun di atas 6-lapis [[prompt-rules-image-generation]]). Ringkas:
- **Grammar 3-mode** (per keyframe): **A** from-scratch (6-lapis penuh) · **B** identity-anchored (manifest env+identity, L3→`subjects[]`, komposisi penuh di teks/koordinat) · **C** composition-anchored (manifest +`composition_reference`, **delta minimal**, lapis terkunci TAK ditulis ulang). Template JSON literal = Part V.
- **ATTACHMENT MANIFEST wajib** tiap frame ber-reference (env plate + identity plate per orang + composition_reference utk END). Mengoperasikan triad-attachment.
- **Plate-state law:** jangan lampirkan plate berisi objek yang aksi-nya "menciptakan" objek itu (jebakan double-carpet). Objek yang disentuh aksi → disebut + plat-nya di-attach.
- **Subject-count:** ≤1 face-locked (+1 soft); ≥3 runtuh → saf multi-figur **DIBANGUN** (iterative-build Rule 8a: seed ≤1 → +1 per generasi Mode C), bukan sekali-jadi.
- **START/END camera-lock:** framing/angle/camera IDENTIK; hanya Lapis-4 berubah. **END delta-kecil = EDIT-IN-PLACE pada render START** (edit mode "Describe edits", instruksi token-per-token + lock-list `... unchanged`, input-fidelity High) → geometri terkunci by-construction; **Mode C generate-from-attachment = fallback** bila tool tak punya edit mode. Beat gerak-besar → Rule 6a framing-by-union / pecah-shot. Gerak kamera = L6-DELTA eksplisit yang melepas jaminan konsistensi.
- **Framing ladder:** multi-figur default medium/tight; single-subject full-body aman; spec satu tingkat lebih ketat (drift-wider).
- **ADDENDUM A1:** layar device OFF/gelap/dormant di keyframe AI; semua UI/kartu/grafik/super ditempel di After Effects. Lapis 5 dibuang. **(refinement 2026-06-26)** AE yang **menghidupkan layar** (glow + UI = post, bukan generate); kartu iklan/notif = **grafis terbang di ruang 3D**, BUKAN tekstur di permukaan layar → tangan/objek **boleh menutupi layar** di frame AI tanpa merusak reveal iklan; staging natural, jangan dikontorsi demi mengosongkan layar (satu-satunya aturan keras: layar ter-render gelap).
- **Sumber plat:** [[explainer-video-2/ATTACHMENT-PRODUCTION-BACKLOG]] (env master+derivative; karakter full+closeup, **medium dibuang**).

> Catatan scope: aturan di sini = produksi GAMBAR. Tahap downstream (Kling i2v) punya harness/behavior sendiri dan dibahas terpisah — jangan campur ke penalaran prompt gambar.

## 🔁 Siklus per-shot
1. Author prompt (mode A/B/C) di file scene → 2. User generate → 3. Review per [[REVIEW-CHECKLIST]] (8 kriteria + enforcement G0–G6) → 4. ACCEPT → rename gambar final + tulis prompt terbukti di slot → REVISE/REGEN: diagnosa slot gagal, perbaiki, ulang.

## Manifest scene
| Scene | File | Status |
|---|---|---|
| SEQ1-SC01 | `SEQ1-SC01.md` | ⬜ prompts EMPTIED 2026-06-26 — TO RE-AUTHOR (3-mode). 8 render lama di `scene-images/sc01/` (arsip metode lama). |
| SEQ1-SC02 | `SEQ1-SC02.md` | ⬜ prompts EMPTIED 2026-06-26 — TO RE-AUTHOR (3-mode); saf SH03 = uji iterative-build. |
| SEQ1-SC03 … SEQ6 | — | ⬜ belum dibuat (author saat produksi tiba, urut cerita). |
