---
title: GATE A2 Narasi — SEQ1-SC01 (INT. KAMAR HERMAN — 04.40)
tags: [explainer-video-2, gate-a2, shot-narrative, SEQ1-SC01]
status: narrative-locked
created: 2026-06-30
updated: 2026-06-30
aliases: [ev2-seq1-sc01-narrative]
---

# GATE A2 Narasi — SEQ1-SC01
## INT. KAMAR HERMAN — 04.40 WIB

> **Konvensi dua-doc (`06` Langkah 2):** dokumen ini = **NARASI saja** (blok-narasi per shot + baris Teknis shot-spec + Grafis UI + Catatan produksi). Skeleton prompt 6-lapis penuh + status produksi hidup di **`Prompt-SEQ1-SC01.md`** (terpisah, diisi saat fase prompt setelah semua shotlist kelar). Sumber cerita: `03-scene-detail.md` SEQ1-SC01.
>
> **Reset 2026-06-30:** doc ini sebelumnya menumpuk prompt+status+lesson (335 baris). Direset ke narasi-saja. Prompt lama tetap di git history; render lama (`scene-images/sc01/sc01_sh0{1..4}_*`) di-supersede karena breakdown berubah 4→5 shot.

**Pesan misi (ad-provider):** Permukaan iklan pertama film, di momen paling privat — subuh. App menampilkan pengingat sholat + satu kartu apparel kontekstual, lalu diam saat keluarga bersiap ibadah. Bukti: inventaris hadir di touchpoint intim secara kontekstual + brand-safe + tahu-kapan-berhenti.

**Prosa scene (dari `03`):** Keremangan subuh, kamar masih gelap. Kelopak mata Herman mengerjap, pandangnya menemukan langit-langit. Di nakas, layar ponselnya menyala sendiri — pengingat waktu subuh muncul bersama UI iklan sarung tenun. Herman meraih ponsel, menimangnya sejenak, melihat grafik isu pasar saham semalam, lalu meletakkannya kembali ke nakas — masih berbaring, tenang. Tangannya menjangkau saklar lampu nakas; cahaya hangat menyala, mengisi kamar yang tadinya gelap. Di sisinya Ratna terjaga oleh cahaya, perlahan bangun dan duduk, menoleh tersenyum ke arah suaminya.

**VO (laki-laki, tenang):** *"Satu hari dimulai. Hari yang sama — untuk semua orang."*

**Scene constants:** Herman + Ratna, mahram-only (Ratna **uncovered**, rambut tampak — `R-ratna §0`). Ranjang: Herman camera-right (sisi nakas+lampu), Ratna camera-left. Layout kamar: jendela camera-left (subuh biru-pekat), nakas+lampu camera-right, artwork *Great Wave* di dinding tengah. Grade: pra-subuh cool-blue → menghangat saat SH04 lampu nyala. Beat privat by-design → SH01–SH04 boleh mono-aktor (Herman); Ratna co-present di SH04–SH05.

---

## Shot — blok narasi

### SH01 — Herman terbangun
- Narasi          : Wajah Herman di keremangan; kelopak mengerjap, pandang ke atas — bagi Herman itu langit-langit kamar, bagi kamera itu tatapan masuk ke lensa.
- Kamera          : overhead, tepat di atas wajah supine (vantase langit-langit)
- Angle + Framing : **top-down murni** CU wajah · LOCKED start→end
- Mood / Cahaya   : pra-subuh very-low-key cool-blue, nyaris siluet; nuansa kebiruan tipis
- Adegan AWAL (→START) : mata terpejam, wajah tenang menghadap atas
- Adegan AKHIR (→END)  : mata terbuka, tatapan masuk ke lensa (bagi Herman: ke langit-langit)
- Teknis (shot-spec)  : attach `H_herman_front_closeup` (identity wajah); env tak dilampir (CU tak tampak ruang) · 85mm · 16:9 · camera-move = none (kamera diam, hanya mata gerak) · key: tanpa key kuat, cool-blue pre-dawn ambient tipis · **exposure bersih low-ISO, shadow detail diangkat secukupnya (anti black-crush/noise)**

### SH02 — Ponsel di nakas menyala
- Narasi          : Insert nakas; layar ponsel menghadap kamera, menyala sendiri — slab cahaya dingin menerpa permukaan nakas; tangan Herman masuk dari ranjang meraih.
- Kamera          : dekat nakas, sisi camera-right ranjang, sedikit tilt down
- Angle + Framing : CU insert objek (nakas + HP) · LOCKED start→end
- Mood / Cahaya   : gelap → cool blue-white glow dari layar HP jadi key
- Adegan AWAL (→START) : layar ponsel gelap, nakas remang
- Adegan AKHIR (→END)  : layar menyala (slab dingin), tangan Herman masuk meraih HP
- Teknis (shot-spec)  : attach `E01_kamar_nightstand` (insert) + `E01_kamar_master` (layout/handedness) · 100mm macro · 16:9 · camera-move = none · key: slab cool blue-white dari layar HP (**render slab polos tanpa UI; konten UI = After Effects, A1**) · **exposure bersih low-ISO anti-noise**

### SH03 — Menimang ponsel
- Narasi          : Herman berbaring menggenggam HP di atas dada, wajah disinari cahaya layar dingin; menatapnya sejenak lalu mengulurkan tangan menaruh HP kembali ke nakas.
- Kamera          : sisi ranjang camera-right, setinggi kasur (eye-level berbaring), angle kanan-diagonal `bed3q`
- Angle + Framing : MEDIUM (kepala+dada+lengan) · LOCKED start→end
- Mood / Cahaya   : wajah di-key cahaya HP cool-blue, ruang jatuh ke shadow tipis
- Adegan AWAL (→START) : HP tergenggam di atas dada, mata menatap layar
- Adegan AKHIR (→END)  : lengan terulur, HP menyentuh permukaan nakas; masih berbaring
- Teknis (shot-spec)  : attach `E01_kamar_master` + `E01_kamar_bed3q` (angle) + `H_herman_front_medium` + `R_ratna_front_medium` · 50mm · 16:9 · camera-move = none · 2-subjek (Herman camera-right, Ratna tidur camera-left uncovered) · key: cool blue-white dari HP ke wajah Herman, ruang shadow · **exposure bersih low-ISO anti-crush**

### SH04 — Lampu nakas menyala
- Narasi          : Tangan Herman menjangkau saklar lampu nakas; cahaya hangat menyala mengisi kamar; di sisinya Ratna mulai terusik cahaya.
- Kamera          : wide dari sudut kaki ranjang (`bed4q`), menangkap dua figur berbaring
- Angle + Framing : WIDE 2-subjek (ranjang penuh) · LOCKED start→end
- Mood / Cahaya   : kamar gelap cool-blue → warm lamp glow mengisi (ambient jendela tetap biru)
- Adegan AWAL (→START) : kamar gelap, tangan Herman menjangkau saklar, Ratna diam tidur
- Adegan AKHIR (→END)  : lampu hangat menyala, kamar terisi cahaya, Ratna mulai menggeliat
- Teknis (shot-spec)  : attach `E01_kamar_master` + `E01_kamar_bed4q` (angle) + `H_herman_front_full` + `R_ratna_front_full` · 35mm · 16:9 · camera-move = none · 2-subjek (Herman camera-right sisi nakas, Ratna camera-left) · key: transisi gelap→warm lamp camera-right, jendela cool-blue tetap (kontras warm-cool)

### SH05 — Ratna bangun
- Narasi          : Ratna, rambut tergerai, terjaga oleh cahaya; perlahan bangkit duduk dan menoleh tersenyum ke arah suaminya.
- Kamera          : sisi camera-left ranjang (sisi Ratna), eye-level
- Angle + Framing : MEDIUM pada Ratna · LOCKED start→end
- Mood / Cahaya   : warm lamp glow (grade ← SH04-END)
- Adegan AWAL (→START) : Ratna berbaring, mata baru terbuka di bawah cahaya hangat
- Adegan AKHIR (→END)  : Ratna duduk, menoleh, senyum ke arah Herman (camera-right)
- Teknis (shot-spec)  : attach `E01_kamar_master` + `R_ratna_front_medium` + grade-ref `sc01_sh04_end` (warm, setelah SH04 jadi) · 50mm · 16:9 · camera-move = none · 1-subjek (Ratna uncovered) · key: warm lamp glow dari camera-right (off-frame, dari arah lampu+Herman)

---

**Grafis UI (AE, non-AI):**
- SH02 — saat layar HP menyala: pengingat subuh + kartu apparel · copy: `Waktu Subuh · 04.42` + sarung tenun "Cap Gajah"
- SH03 — saat Herman menatap HP: grafik pasar saham semalam (aktivitas ponsel; konten app, bukan iklan)

**— Catatan produksi:** apparel muslim/sarung · grade pra-subuh cool-blue → menghangat saat SH04 lampu nyala · Herman+Ratna mahram-only (Ratna uncovered, rambut tampak) · beat privat by-design (mono-aktor SH01–SH04 sah; Ratna co-present SH04–SH05). Skeleton 6-lapis penuh + status → `Prompt-SEQ1-SC01.md` (fase prompt).
