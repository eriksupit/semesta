---
title: Prompt Rules — GPT Image 2 · Semesta Digital
tags: [prompt-rules, gpt-image, illustration, active]
status: active
created: 2026-06-09
updated: 2026-06-09
---

# GPT Image 2 Prompt Rules
## Semesta Digital — Illustration Prompts
*Validated through live generation sessions · Updated continuously*

---

## Aturan Format

### 1. Gunakan JSON dengan field eksplisit
Setiap field adalah instruksi mandiri — model mengalokasikan attention per key-value secara terpisah, bukan membaca sebagai narasi holistik. Prose panjang membiarkan model menginterpretasi bebas berdasarkan training data.

Fields wajib per prompt:
- `scene` — setting, environment, apa yang ada di ruang ini
- `action` — apa yang *terjadi* secara fisik dan konkret di dalam frame
- `camera` — angle, distance, framing spesifik
- `lighting` — sumber cahaya, arah, kualitas, suhu warna
- `style` — satu referensi dominan yang konkret
- `palette` — warna spesifik dengan hex code bila perlu
- `aspect_ratio` — wajib dicantumkan setiap prompt

### 2. Tulis `action` sebagai kejadian fisik konkret
Bukan deskripsi suasana, bukan mood. Model hanya bisa merender sesuatu yang *terjadi secara fisik*.

❌ "The scene feels impersonal and cold"
✅ "A cursor drifts across the screen and clicks a button with nothing behind it"

### 3. Satu style keyword dominan
Dua style keyword yang berkontradiksi (misal "flat illustration" + "dramatic cinematic") menyebabkan model memilih satu secara acak.

❌ "flat editorial illustration, cinematic, dramatic"
✅ "Cinematic digital painting. Key art register for a live-action thriller."

### 4. Constraint ditulis sebagai pernyataan positif
Prompt negatif ("no humans", "no text", "no cartoon") tidak stabil di GPT Image 2 — model kadang justru memunculkan elemen yang ingin dihindari.

❌ "no humans, no hands, no cartoon style"
✅ "The room is empty. The only subject is the monitor." (tulis apa yang *ada*)

### 5. Camera language spesifik
GPT Image 2 default ke "neutral 35mm + natural light" bila tidak ada camera instruction. Ini menghilangkan dramatic feel.

Gunakan: "low-angle wide shot", "medium close-up from slightly below eye level", "overhead shot", bukan "cinematic angle" (terlalu loose).

### 6. Physical specifics mengalahkan adjective stacks
"Overhead fluorescent light pooling on wet concrete, light fog at ankle height" > "dramatic, moody, atmospheric"

Model merender hal fisik, bukan kata sifat.

---

## Aturan Style

### Style yang benar untuk Semesta Digital deck
**Cinematic digital painting** — dramatic, high contrast, painterly but grounded.
Referensi: key art film live-action thriller, Black Mirror promotional art.

Bukan:
- Editorial flat illustration (menghasilkan matte 2D magazine aesthetic)
- Photorealism (terlalu stock photo)
- Kartun / animasi (kehilangan dramatic weight)
- Sci-fi concept art (terlalu tech-hero)
- 3D render (impersonal, floating in void)

### Mengapa "editorial illustration" gagal
Kata "editorial illustration" di training data GPT Image 2 paling sering diasosiasikan dengan flat magazine illustration. Model akan default ke sana, mengabaikan deskripsi adegan yang dramatic.

---

## Aturan Adegan

### Setiap prompt harus punya "kehidupan"
Gambar yang baik punya tension — ada sesuatu yang *terjadi*. Frame yang hanya mendeskripsikan suasana tanpa aksi akan menghasilkan stock photo wannabe.

Setiap prompt wajib punya minimal satu aksi fisik konkret yang bisa dirender.

### Konsistensi live actor (S1, S3, S5, S7, S9, S11, S13, S17)
Semua 8 segmen live actor harus menghasilkan kesan satu orang yang sama. Gunakan field `character_anchor` yang identik di semua 8 prompt.

---

## Revision Protocol

- Generate S0 dulu sebagai format test sebelum mengkonversi semua 18 prompt
- Revisi satu prompt pada satu waktu — jangan reopen seluruh dokumen
- Log setiap revisi di revision log `08-investor-deck-brief.md` dengan tanggal + alasan
- Prompt tetap berlabel DRAFT sampai user eksplisit menyetujui

---

## Update Log

| Tanggal | Perubahan | Alasan |
|---|---|---|
| 2026-06-09 | File dibuat | Konsolidasi semua prompt rules dari sesi iterasi S0 |
| 2026-06-09 | Style: cinematic digital painting (bukan editorial illustration) | "Editorial illustration" di GPT Image 2 default ke flat magazine style |
| 2026-06-09 | Constraint positif — larang prompt negatif | Prompt negatif tidak stabil di GPT Image 2, kadang justru memunculkan elemen yang dihindari |
| 2026-06-09 | Action sebagai physical concrete event | Suasana/mood tidak dirender — hanya aksi fisik yang konkret |
| 2026-06-09 | Satu style keyword dominan | Dua style yang berkontradiksi menyebabkan model memilih acak |
