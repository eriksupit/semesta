---
title: Handoff — Konversi Dokumen Explainer-Video ke DOCX (Format Awam)
tags: [handoff, session-transition, docx, explainer-video]
status: active
created: 2026-06-09
updated: 2026-06-09
aliases: [handoff-rab-docx]
---

# HANDOFF — Sesi Konversi DOCX

```goal
GOAL: Convert 9 explainer-video markdown documents into .docx files written in a
      layman-friendly, easy-to-read format (formal Indonesian, accessible to a
      non-expert reader — investors, partners, crew without production background).
COMPLETION CONDITION: All 9 .docx files produced, saved to vault, each (a) readable
      by a non-expert, (b) jargon expanded on first use, (c) clean professional
      formatting (headings, tables, spacing), (d) frontmatter YAML stripped from body.
OUT OF SCOPE: Changing the substance of any decision/number; regenerating images;
      building the investor deck; renaming the product.
```

## Konteks Sesi Sebelumnya (9 Juni 2026 — RAB)

Sesi RAB selesai. Yang dihasilkan/dikunci:
- `03-rab-produksi-ai.md` v3.0 — ditambah Honor Tenaga Ahli model tiga-lane (Director 25 / Editor 14 / AI Gen 13 / Motion 11 = Rp 63 jt).
- `03-a-rab-syuting-live.md` v2.0 (baru) — RAB syuting live tier profesional ~Rp 65,5 jt, set tetap (bukan greenscreen).
- Total produksi keseluruhan ~Rp 148,3 jt.

Tidak ada pekerjaan RAB yang tertunda. Sesi berikutnya adalah task baru: konversi DOCX.

## Task Sesi Berikutnya

Konversi 9 dokumen ini ke `.docx` dalam format penulisan yang mudah dibaca & dipahami awam:

1. `/Users/eriksupit/Desktop/superapps/explainer-video/01-concept-document.md`
2. `/Users/eriksupit/Desktop/superapps/explainer-video/02-production-brief.md`
3. `/Users/eriksupit/Desktop/superapps/explainer-video/03-rab-produksi-ai.md`
4. `/Users/eriksupit/Desktop/superapps/explainer-video/03-a-rab-syuting-live.md`
5. `/Users/eriksupit/Desktop/superapps/explainer-video/04-pipeline-ai-production.md`
6. `/Users/eriksupit/Desktop/superapps/explainer-video/05-storyboard-rough.md`
7. `/Users/eriksupit/Desktop/superapps/explainer-video/06-storyline.md`
8. `/Users/eriksupit/Desktop/superapps/explainer-video/07-live-production-brief.md`
9. `/Users/eriksupit/Desktop/superapps/explainer-video/08-investor-deck-brief.md`

## Keputusan yang HARUS diklarifikasi ke user di awal sesi

"Format penulisan mudah dipahami awam" punya dua kemungkinan kedalaman — tanyakan satu hal ini sebelum mulai (lampirkan rekomendasi):
- **Level 1 — Konversi format saja:** markdown → docx dengan formatting bersih, frontmatter dibuang, tabel rapi. Konten tidak diubah.
- **Level 2 — Adaptasi awam:** selain konversi, prosa ditulis ulang agar non-ahli paham — istilah teknis (DOP, rack focus, image-to-video, credit, buyout, anchor image) dijelaskan saat pertama muncul, struktur dibuat ramah pembaca.

Rekomendasi: **Level 2** untuk dokumen menghadap eksternal (01, 02, 03, 03-a, 08) karena pembacanya investor/awam; **Level 1** untuk dokumen operasional internal (04, 05, 06, 07) karena pembacanya tim produksi. Konfirmasi dulu — jangan asumsikan.

## Catatan Teknis untuk Eksekusi

- **Tool:** cek ketersediaan `pandoc` (`which pandoc`). Pandoc adalah jalur md→docx paling bersih. Jika tidak ada, alternatif `python-docx` (butuh parsing markdown manual) — pandoc sangat dianjurkan.
- **Frontmatter YAML:** pandoc bisa memproses atau membuangnya; pastikan blok `---...---` tidak bocor ke body docx.
- **Untuk Level 2:** alur = baca .md → tulis ulang versi awam ke .md sementara (atau langsung) → pandoc ke .docx. Pertimbangkan skill `explain-humanize` untuk disiplin bahasa awam (formal Indonesia, ekspansi akronim, tanpa metafora baru).
- **Output:** simpan .docx di mana? Tanyakan — usul: subfolder baru `explainer-video/docx-export/` agar tidak mencampur dengan .md.
- **Tabel kompleks** (RAB, timing reference) harus tetap terbaca sebagai tabel di docx — verifikasi pandoc me-render tabel markdown dengan benar.

## Pipeline & Aturan Sesi (wajib)

- Bootstrap dulu (`/session-anchors` Protocol A): baca CLAUDE.md, MEMORY.md, scope.md, context.md, lessons.md, handoff ini.
- Lessons relevan: user menolak menu/opsi tanpa rekomendasi tunggal; "approve/kunci/go/oke" = persetujuan penuh, langsung eksekusi; setiap output disimpan ke vault dengan frontmatter Obsidian lengkap; riset sebelum klaim; jangan eksekusi tanpa otorisasi eksplisit (Prohibition 1).
- Skills co-aktif: `/anti-sycophancy` `/confidence` `/research-before-dispatch` `/brave`.
- Tutup sesi dengan pipeline penutup + handoff baru.

## Status Vault Saat Ini

- RAB lengkap: `03` (v3.0) + `03-a` (v2.0). Total produksi ~Rp 148,3 jt.
- Image generation (jalur paralel terpisah): 5/16 approved (S0–S4), lanjut S5 — lihat `HANDOFF-2026-06-10-S8.md` jika kembali ke jalur itu.
- `Superapp — Home.md` sudah diupdate dengan `03-a` + handoff ini.

---

*Handoff disusun 9 Juni 2026 pada penutupan sesi RAB.*
