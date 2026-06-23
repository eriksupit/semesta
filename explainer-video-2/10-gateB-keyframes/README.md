---
title: README — GATE B Keyframes (explainer-video-2)
tags: [explainer-video-2, gate-b, keyframe, readme]
status: active
created: 2026-06-23
updated: 2026-06-23
aliases: [ev2-gateB-readme]
---

# GATE B Keyframes — README

Folder ini berisi prompt keyframe 6-lapis per-scene untuk GATE B (ChatGPT Image v2). Tiap file = satu scene (`SEQ<n>-SC<nn>.md`), berisi prompt untuk tiap shot-nya. User generate eksternal; Claude author + review + assemble-spec.

> Standar 6-lapis + grade hangat → `00-WORKLOG` GATE B (2026-06-21, baris 167) + [[prompt-rules-image-generation]]. Scene truth → [[03-scene-detail]]. Identitas tokoh → [[08-character-sheet]]. Ruangan → [[09-environment-sheet]]. ADDENDUM A1 (layar OFF, grafis di After Effects).

## ATURAN WAJIB (jangan diputuskan ulang)

### 1. Tiap keyframe = SATU prompt utuh-mandiri (attachment-line wajib)
Tiap unit yang digenerate harus prompt utuh berdiri sendiri yang membawa SENDIRI baris referensi attachment-nya:
- `environment_reference` — menyebut nama file plat ruangan yang di-attach (mis. `E01_kamar_bed3q.png`).
- `character_identity.identity_reference` — menyebut nama file plat wajah yang di-attach (mis. `H_herman_front_closeup.png`).

**Pasangan start/end = DUA prompt utuh terpisah**, identik kecuali Lapis-4 (`subject_state`/`action`/`pose`/`expression`); masing-masing MENGULANG baris attachment. **JANGAN** pecah jadi "fixed-spec + varian Lapis-4" lalu mengandalkan penggabungan mental — model membaca tiap unit sendiri-sendiri dan tak tahu attachment mana yang diikat bila barisnya hanya ada di blok fixed terpisah. SOP sumber: `09-environment-sheet/E01-kamar.md:61` ("COMPLETE copy-paste-ready prompt, zero scaffold, zero combine"). *(Dikoreksi Erik 2026-06-23; kanonik di `prompt-rules` §Struktur 6 Lapis.)*

### 2. Grade hangat LOCKED (satu-satunya sumber kehangatan)
`Roger Deakins palette, lifted blacks medium gray, neutral shadows, clean whites, Kodak 2383 emulation, slightly warmer midtones`. Hangat HANYA dari `color_grade`; garmen desaturated + dispesifikasi afirmatif (anti auto-batik); negasi 0; tanpa nama organisasi.

### 3. ADDENDUM A1 — layar OFF, grafis di After Effects
Semua layar device render OFF/gelap di keyframe AI; semua UI/kartu/grafik/super ditempel di After Effects. Lapis 5 dibuang. Device tetap muncul, framing comp-aware (ruang layar bersih).

### 4. Dual reference-lock tiap segmen
Tiap keyframe attach plat env (E01…) + plat wajah (H_herman…). Ini yang diuji pilot: apakah dual reference-lock bertahan lewat Kling i2v.

### 5. Checklist authoring per-shot (audit, jangan generate buta)
- **Arah kamera = penentu keberhasilan.** HP dipegang/ditatap → punggung HP ke kamera, layar ke subjek (`rear casing toward camera screen facing the subject`), angle off-axis anti-cliché. HP tergeletak (insert) → top-down, layar OFF, ruang layar bersih untuk AE.
- **State kontekstual = matter.** Bangun tidur → kucel (kelopak berat, pipi sleep-creased, rambut gepeng sebelah) di Lapis-4 + hair/makeup state; identitas wajah TETAP dari `identity_reference`.
- **Cahaya layar via `lighting`**, bukan layar nyala di frame (A1).
- **Audit ke prosa `03` + plat** sebelum menulis token.

## Konvensi pasangan & chaining
- 1 shot = 1 segmen 5 dtk = 1 pasang keyframe (START + END).
- Chain: end-N = start-(N+1) bila shot mengalir kontinu.
- Lapis 1–3 & 6 identik antar start/end; hanya Lapis-4 berubah.
- **START SETUP-BARU DI SCENE TER-LIT LAMPIRKAN KEYFRAME ACCEPTED SBG ACUAN CAHAYA.** Plat env netral-grade (geometri/props saja); look hangat-redup hanya ada di keyframe accepted. Jadi START kamera-baru = plat subjek + satu keyframe accepted scene itu sebagai `lighting_reference` (token peran: "lighting and bedding reference only, not a composition source"). Contoh: SH02-START = plat nakas + `sc01_sh01_end.png`. *(Validated 2026-06-23.)*
- **END FRAME ANCHOR KE RENDER START (bukan ke plat).** Frame END digenerate dengan meng-attach **gambar START yang sudah jadi** sebagai jangkar komposisi (`composition_reference`) + plat wajah (identitas); prompt jadi minimal-change (komposisi/posisi/framing/lighting IDENTIK START, hanya Lapis-4 berubah). Jangan generate END dari plat saja — plat netral menghasilkan komposisi BARU yang tak match START → Kling i2v warp. Sama untuk start yang chain dari end shot sebelumnya (anchor ke render end itu). *(Validated 2026-06-23, SEQ1-SC01.)*

## Manifest scene
| Scene | File | Status |
|---|---|---|
| SEQ1-SC01 (PILOT) | `SEQ1-SC01.md` | authoring LENGKAP 4/4 — SH01 ✅ · SH02 ✅ · SH03 ✅ · SH04 ✅ (8 prompt utuh start/end) |
