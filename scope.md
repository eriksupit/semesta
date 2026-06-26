---
title: Scope — Semesta Digital
tags: [meta, scope, active-session]
status: active
created: 2026-06-08
updated: 2026-06-18
---

# Scope — AKTIF (2026-06-26c · CHARACTER-PLATE REGEN — Herman 12 plat DONE · SC01 di-restruktur 7-shot)

## STATUS TERBARU (2026-06-26c · pivot regen karakter + DAG 12-cell)
- **PIVOT:** keluarga di-regen lebih muda + metode plat baru. Herman → **clean-shaven, token 41 (~46)**; Ratna → token 37 (~42); usia anak dipertahankan. Semua sheet pakai **DAG 12-cell** (closeup→medium→fullbody × front/profileA/profileB/rear; `reference_image` berantai di body+header+tabel; `front_closeup`=master; **anak CU Front = blend wajah ortu** attach H+R front_closeup; FB-profile attach medium-profile). Kanonik: `08-character-sheet/*.md` §3 + `lessons.md` + memory.
- **SELESAI:** **Herman 12/12 plat** generated+ACCEPTED (`character-images/H_herman/`) — identitas konsisten lintas sudut, clean-shaven, usia ~mid-40s, rear wajah-tersembunyi ✓ (catatan non-blok: footwear full = sepatu-tali bukan loafer).
- **SC01 di-restruktur 4→7 shot** (`10-gateB-keyframes/SEQ1-SC01-RESTRUCTURE-2026-06-26.md`): waking sequence (SH03 taruh HP → SH04 lampu nyala/rear → SH05 Ratna bangun duduk → SH06 Herman berdiri menengok → SH07 Ratna senyum), sholat digeser sesudahnya. Env baru `bed4q` (kiri-diagonal, mirror bed3q) = dependensi SH04–SH05. SH03-START regen medium accepted (akan di-supersede saat scene diregen dgn Herman baru).
- **ATURAN BARU sesi ini (lessons + memory):** +5-aging→token=target−5 (dewasa); identity-propagation DAG; report lokasi+attachment tiap prompt; attach WAJIB di body JSON tiap cell; edit reference_image PER-CELL + audit set-match+JSON (regex blok serakah pernah korup Cell 6/7).
- **KOREKSI PERILAKU (Erik):** Confidence = konviksi, jangan diulang mekanis / jangan re-gate yang sudah di-pre-authorize / jangan sebut "ceremony".
- **NEXT:** generate **Ratna 12 plat** (setengah-jalan: closeups+front_medium+rear_closeup ada; sisa medium-profiles+fullbody+rear) → **Andi 12** (CU Front attach wajah ortu; Andi=pilot risiko-tua) → **Lisa 12** → lalu regen scene SC01 dari SH01 dengan Herman/Ratna baru.
- **OUT OF SCOPE:** generate gambar (user); Kling/i2v; commit/push tanpa "ya".

---

# Scope — Riwayat: (2026-06-25 · METODE text+image→image DEFINITIF → FASE PRODUKSI ATTACHMENT)

## STATUS TERBARU (2026-06-25 · sesi metode + backlog produksi)
- **SELESAI sesi ini:** (1) doc riset CLEAN-SLATE `prompt-rules-text-image-to-image.md` (vault root) — project-agnostic, IMAGE-ONLY (Kling DIPISAH): Part I hukum + Part II grammar 3-mode + camera-lock + Part III shot-design + Part IV text + **Part V struktur + 4 template JSON literal (LIVE/PROVISIONAL)** + enforcement G0–G6 + ledger. (2) `explainer-video-2/ATTACHMENT-PRODUCTION-BACKLOG.md` — generate-list shot-driven: **env 27 to-gen / 41 final**, **karakter ~14 inti** (full+closeup, buang medium).
- **METODE INTI (definitif):** image-reference DOMINASI teks (plate-state law); diagnosis drift = resample-bukan-edit + layout-imprecision + reference-dominance (BUKAN token-overflow — terfalsifikasi); subject-count ≤1 face-locked (+1 softened), ≥3 runtuh; grammar 3-mode (A from-scratch / B identity-anchored / C composition-anchored delta-only); LOCKED-atau-CHANGED per lapis; master=Mode A + derivative=anchored; angle SHOT-DRIVEN (bukan 360); start/end camera-LOCK (hanya L4 berubah). PENDING render-validation: Rule 7 establishing-exception, Rule 8a iterative-build, Mode B map, Part V templates.
- **KEPUTUSAN PRODUKSI:** produksi SEMUA shot dari awal; lengkapi attachment DULU; sholat subuh SEQ1-SC02 = **WAJAH MENGHADAP KAMERA** (kunci plat peci/mukena + jadikan saf qiyam SH03 uji utama iterative-build); karakter full+closeup buang medium; E01 master regen (miring→lurus).
- **NEXT:** validasi Rule 8a iterative-build LEBIH AWAL di saf SEQ1-SC02; lalu generate env master→derivative + plat covered-prayer per backlog; baru keyframe scene. User generate, Claude author+review.
- **OUT OF SCOPE:** generate gambar (tugas user); Kling/i2v (urusan terpisah, dibahas kelak); commit hanya bila user minta; jangan buka ulang trilemma permukaan / premis scope-360.

---

# Scope — Riwayat: (2026-06-25 · reboot metode — SUPERSEDED oleh metode definitif di atas)

## STATUS (sesi reboot metode)
- **AKTIF:** brainstorm METODE prompting+produksi text+image→image, lalu tulis `prompt-rules-text-image-to-image.md`. Paket: `handoff/HANDOFF-2026-06-25-EV2-PROMPTING-METHOD-BRAINSTORM.md` + `.txt`.
- **DOKTRIN "POLA BARU build-asset-first" (2026-06-24) DIRETRAKSI** — DOUBLE CARPET (`26629cfc-…png`, `Content 1672x941 (2).png`); image-reference MENDOMINASI teks.
- **TERKUNCI:** trilemma permukaan-sholat SOLVED di level PLATE (`E02_…_reverse_prayer.png` + `_subuh`). SH01 pair accepted+committed.

---

# Scope — Riwayat: AKTIF (2026-06-24 · GATE B keyframe SEQ1-SC02 — POLA PROMPT BARU [DIRETRAKSI 2026-06-25], SH02-START accepted)

## STATUS TERBARU (2026-06-24 · sesi pola-baru)
- **AKTIF:** GATE B keyframe SEQ1-SC02. **3/6 terkunci** (SH01 pair + SH02-START). **NEXT = SH02-END + SH03 dengan POLA BARU**, lalu review render user. YA NEVER generate.
- **POLA PROMPT BARU = WAJIB** (semua di `prompt-rules` changelog 2026-06-24): (1) build-asset-first — objek/situasi khusus di-bake ke set-plate turunan master, bukan teks; (2) colour-tagging objek = anchor posisi+kepemilikan; (3) canvas-pixel grammar DUA sumbu (x + y-depth, 1920×1080); (4) long-axis membujur/melintang eksplisit + dimensi cm; (5) compaction-by-dedup (satu fakta satu field, front-load subjek, tail crew; TANPA simbol pemrograman).
- **Dikunci:** SC02 3-shot; plate sholat `E02_ruangkeluarga_reverse_prayer.png` (4 mat warna ter-bake, 1-1-2 saf: sage-green=Herman/dusty-blue=Andi/terracotta=Lisa/warm-taupe=Ratna); mat DARI PLAT bukan teks; `E02_ruangkeluarga_reverse.png` = base no-mats (dipulihkan dari `115609e`).
- **OUT OF SCOPE:** generate gambar (tugas user); GATE C Kling sampai semua keyframe ADDENDUM A2 lengkap; commit hanya bila user minta.
- Handoff terbaru: `handoff/HANDOFF-2026-06-24-GATEB-SEQ1-SC02-SH02END.md` + `INITIAL-PROMPT-2026-06-24-GATEB-SEQ1-SC02-SH02END.txt`.

---

# Scope — Riwayat: AKTIF (2026-06-18 · Rebuild Konsep Cerita Video → folder explainer-video-2/)

## STATUS PIJAKAN
- Riset produksi Kling (2026-06-17) DITUTUP & tersimpan: `03`, `04`, `04-a` final/approved; total $130 dibekukan sampai re-benchmark. Jangan dibuka ulang kecuali user minta.
- Handoff: `handoff/HANDOFF-2026-06-18-STORY-CONCEPT.md` + `INITIAL-PROMPT-2026-06-18-STORY-CONCEPT.txt`.

## MANDAT
Rebuild naratif penuh explainer video → konsep "Satu Keluarga, Satu Hari Penuh" di folder BARU `explainer-video-2/`. Output: storyline → storyboard, cakupan 5 menit (≈300s), audiens ads provider.

## DOKUMEN AKTIF (explainer-video-2/)
- `00-WORKLOG.md` = log proses & keputusan (sumber proses; sinkron dgn memory + session-anchors + scope).
- `01-storyline.md` = hasil akhir storyline (clean-slate, diisi setelah matang).
- `02-storyboard.md` / `03-scene-detail.md` / `04-ad-inventory-map.md` = stub.
- `05-pipeline-produksi.md` = pipeline produksi terkoreksi (stack + siklus 3-gerbang + tabel status).
- `00-INDEX.md` = hub + peta pewarisan (RAB/pipeline/deck v1 diwariskan via tautan, tidak disalin).

## KEPUTUSAN DIKUNCI (2026-06-18)
- Struktur garis-waktu-hari cross-cut; cold-open dibuang; live-actor host dibuang.
- 5 babak / 15 scene / ~300s. Usaha Ratna = kuliner rumahan/frozen food.
- Grammar 4-beat: Peristiwa→App UI→Potensi Iklan→Payoff diegetik; aturan "Bersih Saat Sakral".
- VO laki-laki tunggal: eksplisit makna, implisit mekanik; larangan "bayangkan"/nama-organisasi tetap.
- Peta potensi iklan 15-scene; 2 scene bebas iklan (subuh & ibadah).

## STATUS (per sesi 2026-06-19 GATE B Prep — O4 SELESAI, GATE 0 berjalan)
- **O4 SELESAI:** `05-pipeline §5` + `04-ad-inventory-map` sinkron ke 19-scene/6-babak. Deck `11` TIDAK perlu diubah (premis handoff dikoreksi — "19 scenes" di `11` = deck PNG lama).
- **GATE 0 berjalan:** scope diperluas → 5 dimensi (identitas+makeup+hair+wardrobe+footwear). File baru `07-style-reference.md` (warisi `tokens-references` + delta + hair anchor baru). `08-character-sheet/` = FOLDER per-tokoh; `00-README.md` + `H-herman.md` (9 prompt plat penuh) SELESAI. Aset `character-images/<TAG>_<char>/`. Kebakuan → memory `semesta-gate0-character-pipeline.md` + `lessons.md`.
- **Koreksi kunci:** multi-angle = 9 gambar/tokoh (3 view × 3 shot); PROTOKOL ARAH t2i (front/profileA/profileB anatomi + mirror, nol left/right).

## STATUS LANJUT (akhir sesi 2026-06-19 GATE B Prep — GATE 0 Herman 9/9 LENGKAP)
- **Herman SELESAI:** 9 plat di `character-images/H_herman/` divalidasi+approve. `08-character-sheet/` (00-README + H-herman.md) + `07-style-reference.md` jadi.
- **9 aturan token DIKUNCI** (multi-angle 9-gambar, rasio per-shot 9:16/2:3/4:5, camera-relative + mirror-via-reference, positive-only, keyword-leak, uniform-bukan-gradien, matte-plate-standard anti-sheen, plain-white scene, deviasi plat). Semua di `prompt-rules`/`lessons`/memory/`00-README` — baca, jangan putuskan ulang.
- **Sesi Ratna dipisah** (sesi ini terlalu padat). Handoff dibuat.

## STATUS LANJUT (akhir sesi 2026-06-20 — GATE 0 Ratna 12/12 LENGKAP)
- **Ratna SELESAI:** 12 plat di `character-images/R_ratna/` (9 uncovered turnaround rambut tergerai + 3 hijab ref) divalidasi+approve. `R-ratna.md` v0.3; `00-README` manifest COMPLETE; `00-WORKLOG` entri 2026-06-20.
- **Kebakuan baru DIKUNCI** (semua di `lessons.md`+memory — baca, jangan putuskan ulang): sumbu modesty=paparan-non-mahram (bukan indoor/outdoor); "hijabi" di `role`=keyword-leak (dibuang dari plat uncovered); plat referensi rambut TERGERAI (styling ke GATE B); karakter bertutup = baseline uncovered + plat tertutup representatif.
- **CATATAN GIT:** vault bukan repo; `commit` belum bisa; `git init` = keputusan user.

## STATUS LANJUT (akhir sesi 2026-06-21 — GATE 0 Lisa 9/9 LENGKAP)
- **Lisa SELESAI:** 9 plat di `character-images/L_lisa/` (Front/ProfileA/ProfileB × full/medium/closeup, uncovered, rambut tergerai, body `34C` konsisten) divalidasi+approve. `L-lisa.md` v0.2; `00-README` manifest COMPLETE; `00-WORKLOG` entri 2026-06-21.
- **Kebakuan baru DIKUNCI** (lessons+memory — baca, jangan putuskan ulang): siluet dada feminin di t2i = **ukuran bra konkret register fashion** (`body_features: ...natural 34C bustline, defined waist and hips...` + `wardrobe: fitted crew-neck...`), BUKAN adjektiva abstrak (`slim/womanly/hourglass/curves/feminine` gagal 3× — torso rata di profil). Lolos filter via register `commercial stock photography/catalogue`; hindari kata-merah `breasts/busty/large/cup-lepas/bra`; eskalasi 34B/34D. 3 frontal awal (slim) di-regenerate `34C` agar satu-tubuh.
- **Render-age 19 dikunci** (terverifikasi pada plat).

## STATUS LANJUT (akhir sesi 2026-06-21 — GATE 0 Andi 9/9 LENGKAP)
- **Andi SELESAI:** 9 plat di `character-images/A_andi/` (Front/ProfileA/ProfileB × full/medium/closeup, uncovered, crop pendek) divalidasi+approve. `A-andi.md` v0.1; `00-README` manifest COMPLETE. 9 plat uncovered saja (SEQ6-SC02 ngaji tanpa peci per prosa). Nol body-feminization token.
- **Render-age 10 DIKUNCI** (terverifikasi plat pertama). **Kebakuan baru DIKUNCI** (lessons+memory): render-age di bawah usia riil HANYA untuk dewasa; anak = usia riil, nol kompensasi menua.
- **GATE 0 tinggal figuran:** `F-figurans.md` (figuran berulang) → entri WORKLOG penutup GATE 0 → GATE B. Diskusi pilih figuran mana = agenda berikutnya.

## STATUS LANJUT (sesi 2026-06-21 — GATE B dibuka + GATE 0-ENV berjalan)
- **GATE B:** standar shot 6-lapis + token grade-hangat (`Roger Deakins … slightly warmer midtones`) + crew video (Cuarón/Lubezki/Caballero) DIKUNCI di `00-WORKLOG`. Field `identity_reference` ikat plate↔attachment.
- **ADDENDUM A1 (kanonik `00-WORKLOG`):** seluruh grafis nol dari generate AI → digarap After Effects; **Lapis 5 dibuang**. Disebar ke `prompt-rules`/`05`/`03`/`lessons`/memory.
- **GATE 0-ENV:** 14 environment (E01–E14), metode `09-environment-sheet/00-README-ENV.md` (empty-room, grade netral, scoped-angle, 3 anchor wajib: kelas pemilik + brand internasional + desainer internasional Caballero/Ilse Crawford + named artwork Hokusai). `environment-images/` dibuat; **E01 master v3.1 jadi** (compliant).
- **Kebakuan/koreksi baru** (lessons + memory — baca, jangan ulang): env=scene benda-mati → `subject_anchor`; prompt env wajib token-library + positive-only (contek plate karakter approved); geo-label `scene` BANNED → lokalisasi via material+register; **multi-angle env via metode reference-image karakter** (bukan text-only/klon); jangan defeatist — multi-angle konsisten terbukti pada 53 plate karakter.
- **NEXT:** selesaikan angle E01 (reference-image upload + spec sudut tegas) → E02–E14 → kembali ke GATE B keyframe SEQ1. Tertunda lama: runtime ≈312s vs 300s; sinkron O4 hilir.

## STATUS LANJUT (akhir sesi 2026-06-21 — GATE 0 CLOSED, figuran 14/14)
- **GATE 0 DITUTUP penuh:** figuran SELESAI 14/14 (`F_darto` 3 · `F_tika` 2 · `F_petugasbank` 3 · `F_rian` 3 · `F_pembina` 3). `F-figurans.md` v0.3 (14 prompt 6-lapis verbatim). `00-README` figuran=COMPLETE; `00-WORKLOG` entri penutup GATE 0. Karakter GATE 0 final: Herman 9 · Ratna 12 · Lisa 9 · Andi 9 · figuran 14.
- **Kebakuan baru DIKUNCI** (semua di `lessons.md`+memory — baca, jangan putuskan ulang): minor tak boleh token-bra (re-age dulu ke dewasa, Tika 16→20); pembeda wajah figuran via `distinctive-commoner-features`+ciri konkret (render figuran cenderung jatuh ke wajah generik sama); body-shape via cup konkret+tinggi+build (Tika 34C/Lisa 34C/pembina 36D); kacamata dibuang (frame tak stabil lintas angle); panjang lengan wajib eksplisit di wardrobe; peran figuran ikut prosa `03` (Darto pedagang, bukan satpam); tiap sel = prompt 6-lapis penuh verbatim.
- **NEXT: GATE B** prompt keyframe per shot (grade hangat). **Handoff GATE B SUDAH dibuat:** `handoff/HANDOFF-2026-06-21-GATEB.md` + `INITIAL-PROMPT-2026-06-21-GATEB.txt` (sesi baru dibuka dgn diskusi DECIDE-FIRST: token grade-hangat + urutan kerja + pairing keyframe). **`Herman Model.png` SUDAH dihapus user → `H_herman/` tepat 9 plate.** Carryover: runtime ~312s vs 300s; sinkron O4 hilir (`04-ad-inventory-map`/deck `11`/tabel `05`). Total plate GATE 0 = 53.

## NEXT (sesi figuran — historis: sesi Andi)
- **GATE 0 lanjut:** `08-character-sheet/A-andi.md` (anak 10 — bare healthy skin, anchor hair Anissa Salazar / costume Deborah Hopper; 4 scene SEQ2-SC03, SEQ4-SC04, SEQ6-SC01/02) + folder `character-images/A_andi/` → `F-figurans.md` → entri WORKLOG penutup GATE 0. **[Andi SELESAI 2026-06-21 — lihat STATUS LANJUT di atas.]**
- **Render-age Andi OPEN:** anak 10, verifikasi pada plat pertama (pola Lisa). **[DIKUNCI 10 — terverifikasi.]**
- **Lalu GATE B:** prompt 6-lapis t2i per shot (grade HANGAT video), pakai character sheet + `07` sebagai jangkar.
- **Tertunda:** runtime ~312s vs 300s (opsi pangkas 1 shot); file `Herman Model.png` (ke-10, perlu klarifikasi user).
- **Handoff:** `handoff/HANDOFF-2026-06-20-LISA.md` + `INITIAL-PROMPT-2026-06-20-LISA.txt`.

## BELUM DITENTUKAN
- O1 kebijakan nama brand (mock vs asli); O4 verifikasi dampak hilir ke RAB/pipeline/deck bila scene/durasi bergeser.

## OUT OF SCOPE
- Menyentuh kembali pekerjaan Kling kecuali user merge-kan ke mandat ini.
- Mengubah angka/keputusan dokumen sumber tanpa approval eksplisit.
- Mengunci nama produk final.

## GUARDRAIL
- VO publik dilarang sebut NU/Muhammadiyah/bank/pesantren; tone deck cool; live actor jangkar manusia di dunia AI.
- **OPERATING CONTRACT (kanonik di `CLAUDE.md`):** mutasi butuh "ya" per-aksi; stay in scope; `Confidence: NN%` tiap respons substantif; <95% → riset+loop sampai >95%, satu rekomendasi tanpa menu; conviction bukan dereferen, jangan tag ritual "approve/override/amend" di giliran diskusi. Lihat CLAUDE.md untuk teks penuh — jangan disalin.

---

# Scope — Riwayat: Sesi S12 SELESAI (deck pipeline tuntas)

## STATUS: ilustrasi 19/19 APPROVED + 3 doc konten deck + handoff Claude Design SIAP
- APPROVED 19/19: S0–S17b (termasuk tambahan S12b, S14b, S17b). PNG verified di `rough-presentation-image/`. S15/S16 dilepas dari deck (video-only; dokumen video utuh).
- Doc konten deck (audiens BEDA): `09` INVESTOR (3 [FILL]) · `11-adprovider-deck-content` PROVIDER IKLAN (FINAL, [FILL] slide 12) · `10-scene-detail-naskah` pelengkap visual (14 VO [draft]).
- Handoff Claude Design (`handoff/`): visual + revisi-detail + ad-provider(design-only) + investor.
- Handoff sesi: `handoff/HANDOFF-2026-06-10-S12.md` + `handoff/INITIAL-PROMPT-2026-06-10-S12.txt`.

## TERSISA DI SISI USER (next session)
- Isi placeholder: `09` team/the-ask/unit-econ; `11` slide 12 commercial. Validasi 14 VO [draft] di `10`. Jalankan Claude Design. (Opsional) tinjau label "investor" `08`; tulis Section 3 prose.

## ATURAN PERAN (kunci sesi ini)
SAYA penulis konten; Claude Design HANYA pelayout. Cek audiens ke `01-concept §2` sebelum tulis copy.

---

# Scope — Riwayat: Continue Image Generation S10–S17
- APPROVED: S0–S9 (PNG-verified). REMAINING 6: S10–S14, S17. SKIP/REMOVED: S15, S16. ADDED: S12b, S14b, S17b.
- Handoff: `handoff/HANDOFF-2026-06-10-S11.md` + `INITIAL-PROMPT-2026-06-10-S11.txt`.

## IN SCOPE (sesi baru)
- Generate + approve 6 scene tersisa (S10→S11→S12→S13→S14→S17) ke `explainer-video/08-investor-deck-brief.md`.
- Terapkan LOCKED STANDARDS di handoff: tone deck tunggal (cool), anti dead-center, interaksi >1 orang non-presenter, ekspresi non-artificial, super unik, fix mekanis+tangan, token discipline.
- Per approval: rename PNG, update `08` status + count, update lessons/MEMORY/internal memory.
- Setelah 16/16: buat handoff + initial prompt untuk sesi Claude Design (16 PNG + Section 1–4 dari `08`).

## OPEN ITEMS (konfirmasi user di sesi baru)
- S6: kartu grafis "Rp 340.000" tidak jelas terlihat — terima atau regenerate?
- S17: warm-arrival closer sudah di-cool-kan — keep cool (default) atau restore controlled warm?

## STOP CONDITION
16/16 APPROVED → handoff Claude Design siap → sesi ditutup.

## OUT OF SCOPE (berlaku umum)
- Mengubah substansi keputusan/angka di dokumen sumber.
- Mengunci nama produk final (pending approval investor/stakeholder).

---

# Scope — Sesi Sebelumnya (Image Generation Reset S0–S17)

## IN SCOPE
- Generate ulang seluruh 18 ilustrasi (S0–S17) untuk `explainer-video/08-investor-deck-brief.md`.
- Semua prompt sudah final di `08` — tidak perlu revisi prompt kecuali ada masalah nyata saat generate.
- Review hasil generate terhadap `prompt-rules-image-generation.md` v2.
- Update status approved di `08` per scene + filepath PNG.
- Simpan PNG ke `explainer-video/rough-presentation-image/` dengan naming convention.
- Setelah 18/18 approved: buat handoff + initial prompt untuk sesi Claude Design.

## OUT OF SCOPE
- Mengubah struktur 6-layer prompt yang sudah dikunci.
- Mengubah graphic matrix investor register yang sudah dikunci.
- Mengubah komposisi matrix live actor yang sudah dikunci.
- Membangun presentasi deck (sesi Claude Design terpisah berikutnya).
- Mengubah struktur deck (Section 2) / copy investor (Section 3) — sudah final.
- Mengunci nama produk final (pending approval investor/stakeholder).
- Mengisi angka Slide 17/18/20 (placeholder, domain founding team).

## Urutan Generate
S0 → S1 → S2 → S3 → S4 → S5 → S6 → S7 → S8 → S9 → S10 → S11 → S12 → S13 → S14 → S17 → S15 → S16

## Stop Condition
18/18 APPROVED → handoff Claude Design siap → sesi ditutup.

## Riwayat Scope
| Tanggal | Perubahan |
|---|---|
| 2026-06-08 | Initial: generate S5–S17 |
| 2026-06-09 | Expanded: graphic wajib semua scene, scene_depth wajib semua scene |
| 2026-06-09 | Reset: generate ulang dari S0, semua prompt sudah final |
| 2026-06-10 | Sesi 11: S3–S9 approved (10/16). Tone deck distandarkan cool, anti-dead-center, interaksi non-presenter, fix mekanis+tangan. Lanjut S10–S17 di sesi baru (HANDOFF-S11). |

## UPDATE 2026-06-23 — GATE 0-ENV E03 COMPLETE → **ENV PAUSED, PILOT AKTIF**
- **⏸ GATE 0-ENV DI-PAUSE (keputusan Erik 2026-06-23).** Aktif sekarang = **PILOT SEQ1-SC01 end-to-end** (GATE B keyframe → GATE C Kling i2v → VO + grafis AE → assemble) untuk membuktikan workflow sebelum scaling. Paket: `handoff/HANDOFF-2026-06-23-PILOT-SEQ1-SC01.md` + `INITIAL-PROMPT-2026-06-23-PILOT-SEQ1-SC01.txt`. Reference-lock: `E01_kamar/*` + `H_herman/*` (Herman satu-satunya tokoh on-screen).
- **E04 Dapur di-HOLD** — handoff `HANDOFF-2026-06-23-ENV-E04-dapur.md` sudah jadi, dieksekusi SETELAH pilot (atau setelah pipeline-gap dari pilot diperbaiki).
- **E01 ✅ · E02 ✅ · E03 Ruang Belajar ✅ (4/4)** locked (master/desk/tablet/doorway). GATE 0-ENV rollout berjalan (paused di E03).
- **NEXT env = E04 Dapur Ratna (SEQ3-SC01, live-selling UMKM)** — lanjut home-room block (E04→E06 berbagi §3 house anchor), lalu luar-rumah (E07, E09–E14) + E08 kantor (3×).
- **Kebakuan baru E03 (terkunci, lihat `context.md` TERBARU + `prompt-rules` + memory):** ornamen anak = produk bernama; DUA guardrail (token + image-similarity) → kalau prior runtuh ke karakter-IP ganti KATEGORI subjek (Schleich T-Rex), bukan de-brand kata; merek produk aman & wajib, hanya karakter-IP kena filter (swap reaktif); grep-audit token arah pra-lock.
- Standar env terkunci di `09-README-ENV §2.6` + `E02`/`E03` (token-per-token, verifiable named products, camera-relative, master-as-anchor). Out of scope: GATE B keyframes sampai home-room block env selesai.
