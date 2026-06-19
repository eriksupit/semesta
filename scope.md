---
title: Scope — Semesta Digital
tags: [meta, scope, active-session]
status: active
created: 2026-06-08
updated: 2026-06-18
---

# Scope — AKTIF (2026-06-18 · Rebuild Konsep Cerita Video → folder explainer-video-2/)

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

## NEXT (sesi Lisa)
- **GATE 0 lanjut:** `08-character-sheet/L-lisa.md` (mahasiswi+kreator 20 — **9 plat saja, tidak berhijab**, rambut tergerai; anchor Michael Wilkinson/Judy Chin/Camille Friend; makeup on-camera ready; 6 scene SEQ2-SC01/04, SEQ3-SC04, SEQ4-SC02, SEQ5-SC01, SEQ6-SC01) + folder `L_lisa/` → `A-andi.md` → `F-figurans.md` → entri WORKLOG penutup GATE 0.
- **Render-age Lisa OPEN:** rekomendasi ~19, verifikasi pada plat pertama.
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
