---
title: Prompt Audit Checklist — Pre-Lock Gate (explainer-video-2)
tags: [explainer-video-2, prompt-rules, audit, checklist, active]
status: active
created: 2026-06-24
updated: 2026-06-24
aliases: [ev2-prompt-audit, prompt-audit-checklist]
---

# Prompt Audit Checklist — Pre-Lock Gate

Gate yang dijalankan **sebelum** mengunci / generate prompt apa pun (plat karakter, plat env, keyframe GATE B). Tiap item turunan langsung dari [[prompt-rules-image-generation]] + `lessons.md`; nomor baris = jejak bukti. Dua kelas gate:

- **MEK** = mekanis, ditegakkan via `grep` (deterministik, jalankan dulu).
- **MATA** = penilaian, butuh baca render / prosa `03` (tak bisa di-grep).

Aturan pakai: satu prompt belum "siap" sampai SEMUA MEK lolos `grep` **dan** semua MATA relevan dicentang. Mencatat aturan ≠ menerapkan — audit tiap prompt sendiri, jangan tunggu user menemukan pelanggaran.

---

## A. Token discipline (MEK — grep dulu)

| # | Gate | Grep / cara | Bukti |
|---|---|---|---|
| A1 | Nol negasi | `grep -nE '\b(no|not|without|absent|un-|non-)\b|not in frame|zero ' ` → tiap hit dibuang (kecuali `zero shine`). Elemen tak tampak = **hapus field**, bukan "not in frame". | rules:25,561 · lessons:133 |
| A2 | Nol kata sambung-antar-token/copula/tense di VALUE | `grep -nE '\b(and|but|or|with|for|plus|bearing|is|are|was|be)\b'` di nilai JSON. **EXEMPT (simpan, jangan flag): `of` + preposisi spasial intra-token** `toward/above/below/from/to/into/over/against/on` (load-bearing, bukan lem) | rules:24,567 · rules:641 |
| A3 | Token-per-token di JSON value | tiap value = klaster koma; lem antar-token (`and/but/or/with/for/plus/bearing`) → koma; `of` + preposisi spasial intra-token dipertahankan (prosa markdown di luar value boleh) | rules:24,641 |
| A4 | Keyword-leak scan | tiap token diuji: kalau 1 kata diambil sendiri memunculkan hal tak diinginkan (`light-absorbing`→light, `low-sheen`→sheen, `devout Muslim`→kaligrafi) → ganti akar-bersih | rules:562 · lessons:132 |
| A5 | Uniform, bukan gradien | grep `graying|fade|gradient|gradation|falloff` → ganti `uniform/even/consistent ... throughout` | rules:563 · lessons:131 |
| A6 | Nol redundansi intra/lintas-field | review manual cepat: token yang bilang hal sama 2× | rules:27,28,571 |

---

## B. Spasial — DUA SUMBU JANGKAR (gabungan MEK + MATA)

> Prinsip terkunci: bukan "semua perspektif kamera". Ada **dua sumbu** — keliru memilih sumbu = mode kegagalan yang sudah pernah dibayar.

**Sumbu 1 — Lateral & kedalaman = KAMERA-RELATIF + bahasa depth**
- [ ] B1 (MEK) Penempatan kiri/kanan/atas/bawah pakai `camera-LEFT/RIGHT/BACK`. *(rules:640 — relasi abstrak `opposite/facing` gagal 4×)*
- [ ] B2 (MEK) Grep token melayang `beside | near | behind | next to | one side | side wall | opposite | facing | above | below | beside it` → tiap hit di-anchor ke `camera-DIR` **atau objek bernama** (`camera-right of the desk`, `on top of the KALLAX`); pronoun `beside it` = haram. *(rules:643)*
- [ ] B3 (MATA) Kedalaman pakai `scene_depth{foreground,midground,background}` (bahasa compositing), background eksplisit populated. *(rules:294-312)*

**Sumbu 2 — Cahaya & arah-hadap-wajah = RELATIF-RUANG / ANATOMI (JANGAN kamera)**
- [ ] B4 (MATA) `lighting` relatif-RUANG: `key from the curtained window wall`, BUKAN `from camera-left` (kamera berputar → ruang terbaca beda antar-angle). *(lessons:81)*
- [ ] B5 (MEK) Arah-hadap KARAKTER = anchor anatomi (pipi/telinga tampak) + mirror via reference-image; **NOL token left/right** di plat/keyframe orang. *(lessons:42 · rules:640)*

---

## C. Struktur 6-lapis (MATA)

- [ ] C1 Urutan `mood → color_grade → style` di atas; dunia→peristiwa→subjek→teknis. *(rules:77 · lessons:156)*
- [ ] C2 Nama orang HANYA di Lapis 3 (di Lapis 6 = style-anchor). *(rules:78)*
- [ ] C3 Subjek WAJIB ditulis Lapis 3 — attachment tak bisa menyuntik subjek tak-disebut. *(rules:98)*
- [ ] C4 Lapis 5 (grafis) dibuang utk video (ADDENDUM A1); device muncul, layar bersih comp-aware. *(rules:61 · lessons:57)*
- [ ] C5 Benda mati → `subject_anchor`, `pose`→`composition`, skip gesture/expression. *(rules:177 · lessons:69)*
- [ ] C6 `expression` = fisik murni, nol label emosi/narasi. *(rules:401)*

---

## D. Color grade (MEK + MATA)

- [ ] D1 (MEK) Satu token temperature saja — dua = pelanggaran (warm menang). Grep `warmer`+`cool` co-occur. *(rules:245,598)*
- [ ] D2 (MATA) Video = `slightly warmer midtones`; deck = `cool midtones desaturated, cool-dominant zero amber push`. Jangan tertukar. *(lessons:58,109)*
- [ ] D3 (MEK) Nol token warm bocor field lain: grep `warm|golden|amber|ochre` di `lighting`/`scene_depth`. *(rules:247)*
- [ ] D4 (MATA) Garmen tetap desaturated walau grade hangat. *(lessons:39)*

---

## E. Karakter / identitas (MATA, sebagian MEK)

- [ ] E1 (MEK) Etnis spesifik/`Jakartan`; grep `Indonesian|Betawi` = 0. *(rules:326 · lessons:143)*
- [ ] E2 Usia satu angka + aging-bias (dewasa −; **anak = usia riil**). *(rules:334 · lessons:45)*
- [ ] E3 (MEK) `facial_features` nol token warna: grep `golden|ivory|olive|tan|warm|brown|beige`. *(rules:337)*
- [ ] E4 Makeup 3 lapis (base+features+finish). *(rules:343)*
- [ ] E5 Tiap garmen terlihat (atas+bawah+luar+alas kaki) dispesifikasi afirmatif (anti auto-batik); koreksi bukan dengan negasi. *(rules:357 · rules:548)*
- [ ] E6 `role` nol pemicu-environment & nol keyword-identitas-agama. *(rules:321 · lessons:51)*
- [ ] E7 Karakter MINOR = NOL token ukuran-bra (batas perlindungan anak, non-negotiable). *(lessons:93)*
- [ ] E8 Hijab/mukena = sumbu paparan-non-mahram (termasuk via kamera/siaran), bukan indoor/outdoor. *(lessons:48)*

---

## F. Lapis 6 sinematik (MATA)

- [ ] F1 framing/angle/camera/lighting dari LIBRARY, bukan dikarang. *(rules:459-494 · lessons:67,70)*
- [ ] F2 Off-axis anti-cliché; live-actor beruntun = beda sisi+spot+angle. *(rules:478 · rules:632,635)*
- [ ] F3 Roger Deakins di `color_grade`, BUKAN `lighting_director`. *(rules:500,582)*
- [ ] F4 Crew video: Cuarón / Lubezki / Caballero. *(lessons:59)*

---

## G. Istilah kultural (MATA)

- [ ] G1 Ada English-prior-kuat → pakai English (`prayer mat`/`hijab`/`sarong`); niche tanpa padanan → token tunggal lokal (`mukena`/`peci`), bukan frasa English generik multitafsir. *(rules:80)*

---

## H. Env plate (MATA + MEK)

- [ ] H1 Struktur `subject_anchor` + blok `shot` nested = satu-satunya variabel per-angle. *(lessons:77)*
- [ ] H2 (lihat B1/B2) arah = `camera-LEFT/RIGHT/BACK` atau objek bernama.
- [ ] H3 Furnitur = produk bernama ber-siluet verifiable (KALLAX 2x2 countable), siluet distinct per item. *(rules:640 · lessons:311)*
- [ ] H4 Enumerate tiap aksesori permukaan (keyboard/mouse) atau model improvisasi. *(rules:641 · lessons:311)*
- [ ] H5 Satu artwork public-domain bernama per ruang. *(lessons:83)*
- [ ] H6 (MEK) `environment_reference` token-form eksplisit sebagai field pertama derivatif. *(lessons:84)*
- [ ] H7 Lighting relatif-RUANG (= B4). *(lessons:81)*
- [ ] H8 Master = anchor → tambah objek = regen MASTER dulu, baru derivatif; token derivatif = irisan persis master (verifikasi zoom, bukan ingatan). *(lessons:86 · rules:641)*
- [ ] H9 Nol label identitas-agama di `scene`; lokalisasi via material + kelas + objek konkret. *(lessons:80)*
- [ ] H10 Tiga tinggi kamera env wajib beda nyata (M eye-level · P ~45° high-angle · F low seated-height); "soft high-angle" gampang overshoot ke top-down/low → spec tegas per-tinggi. *(rules:641 · lessons:311)*

---

## I. GATE B keyframe governance (MATA)

- [ ] I1 **Triad attachment tiap frame**: karakter + lingkungan + start/end-ref. Env plate WAJIB walau render sudah tampak ruangnya (objek beraksi → tanpa plat = halusinasi permukaan). *(rules:96)*
- [ ] I2 Attachment-line di TIAP unit; start/end = DUA prompt utuh terpisah (identik kecuali Lapis-4). *(rules:100 · README:18)*
- [ ] I3 END anchor ke render START (`composition_reference` = file render START) + plat wajah, minimal-change. JANGAN generate END dari plat. *(rules:88 · README:45)*
- [ ] I4 START setup-baru di scene ter-lit → lampirkan keyframe accepted sbg `lighting_reference` (token peran "lighting/bedding reference only, not composition source"). *(rules:84 · README:44)*
- [ ] I5 Orientasi hadap hanya dari plat cocok (front/profileA/profileB); NOL "3/4"; shot profil = buang `front_`. *(rules:102 · lessons:61)*
- [ ] I6 Eyeline telentang = cek posisi kamera di RENDER dulu (overhead→ke lensa; diagonal→ke langit-langit). *(rules:90)*
- [ ] I7 Screen-glow = layar ON + HP rear-casing ke kamera (bukan layar off + glow palsu). *(rules:94)*
- [ ] I8 Figur berbaring + env-ref → spec CU/ECU (generator drift melebar; spec satu tingkat lebih ketat). *(rules:92)*
- [ ] I9 Regen HANYA bila target visual berubah (de-negasi/sinonim setara → jangan regen). *(rules:86)*

---

## J. IP / content-filter (MATA)

- [ ] J1 Brand produk = AMAN & wajib (konsistensi). Hanya character/franchise-IP yang trip filter → ganti **kategori subjek** (bukan sekadar de-brand): armored humanoid → Iron Man prior → switch ke subjek public-domain (Schleich T-Rex). *(rules:644-645 · lessons:319)*

---

## K. Sensitivitas (MEK)

- [ ] K1 Grep VO/copy: nol nama organisasi keagamaan, nol `pesantren`, nol `bayangkan`; NU visual-only. *(lessons:16,180,181)*

---

## M. Keselarasan dramatik (MATA — holistik, baca 6 lapis sebagai satu scene)

> Gate **gestalt**, BUKAN per-item. A–L menguji tiap token vs aturan/kehadiran; M menguji apakah SELURUH token **menarik ke arah yang sama** menuju beat dramatik scene. Sebuah prompt bisa lolos A–L (tiap token patuh, tiap elemen hadir) namun ansambelnya mengkhianati drama (mis. `lighting "bright even"` di scene keintiman subuh). *(Provisional 2026-06-24 — penambahan proses, belum render-validated; ditegakkan via /tti-prompt-creator @ authoring + /tti-prompt-audit @ gate)*

- [ ] M1 Tulis SATU kalimat **beat dramatik** shot ini ditafsir dari prosa `03-scene-detail.md` (emosi/momen yang wajib mendarat di frame ini). *(03-scene-detail)*
- [ ] M2 Uji TIAP token sumbu-suasana terhadap beat itu — `framing`, `angle`, `camera`, `lighting`, `color_grade`, `subject_state`/`action`/`pose`, `expression`, `material`, `scene_depth`: menarik ke beat (✓), netral (–), atau melawan/mengencerkan (✗)? *(03-scene-detail)*
- [ ] M3 NOL token ✗ — tiap token yang melawan/mengencerkan beat direvisi ke token yang melayaninya (tetap patuh A–L). Pre-render judgeable: ini soal harmoni internal spec, bukan hasil render. *(03-scene-detail)*

---

## L. Meta-gate (dokumen rule itu sendiri)

- [ ] L1 Tiap baris rule baru punya jejak `(Validated <tgl>, <evidence>)` — provisional ditandai eksplisit. *(rules:642 · lessons:316 · semesta-prompt-rules-sop)*
- [ ] L2 Frontmatter Obsidian lengkap di tiap file. *(lessons:22)*
- [ ] L3 Token negasi di sumber kanonik pun WAJIB ditulis ulang positif sebelum dipakai — sumber kanonik tak otomatis lolos token-discipline. *(lessons:50)*
