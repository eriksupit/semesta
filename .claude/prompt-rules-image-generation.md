---
title: Prompt Rules — Image Generation · Semesta Digital
tags: [prompt-rules, image-generation, illustration, active]
status: active
created: 2026-06-09
updated: 2026-06-09
---

# Image Generation Prompt Rules
## Semesta Digital — Semua Model Image Generation
*Berlaku untuk: GPT Image 2, Midjourney, Kling, Runway, Seedance, dan model apapun yang dipakai di pipeline ini.*
*Validated through live generation sessions · Updated continuously*

---

## Prinsip Dasar

Prinsip-prinsip ini adalah **prinsip universal prompt image generation** — bukan spesifik satu model. Setiap model punya syntax berbeda, tapi kelemahan yang sama: model menginterpretasi berdasarkan training data jika instruksi tidak cukup spesifik dan terstruktur.

---

## Aturan Format

### 1. Gunakan struktur field eksplisit
Setiap field adalah instruksi mandiri — model mengalokasikan attention per key-value secara terpisah, bukan membaca sebagai narasi holistik. Prose panjang membiarkan model menginterpretasi bebas berdasarkan training data.

**Untuk GPT Image 2 / ChatGPT:** gunakan JSON literal `{ }` dengan field berlabel.
**Untuk Midjourney:** gunakan comma-separated tags dengan label eksplisit (`--ar`, `--style`, dll.).
**Untuk Kling / Runway:** adaptasi field yang sama ke format prose terstruktur per baris — model video lebih responsif terhadap action description per baris daripada JSON.

Fields wajib di semua model:
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
Dua style keyword yang berkontradiksi menyebabkan model memilih satu secara acak — berlaku di semua model.

❌ "flat illustration, cinematic, dramatic"
✅ "Cinematic digital painting. Key art register for a live-action thriller."

### 4. Constraint ditulis sebagai pernyataan positif
Prompt negatif ("no humans", "no text", "no cartoon") tidak stabil — model kadang justru memunculkan elemen yang ingin dihindari. Tulis apa yang *ada*, bukan apa yang tidak ada.

❌ "no humans, no hands, no cartoon style"
✅ "The room is empty. The only subject is the monitor."

*Catatan Midjourney: `--no` parameter tersedia dan lebih stabil dari prompt negatif di model lain, tapi tetap ditulis setelah semua positive description selesai.*

### 5. Camera language spesifik
Semua model default ke framing netral bila tidak ada camera instruction — ini menghilangkan dramatic feel.

Gunakan: "low-angle wide shot", "medium close-up from slightly below eye level", "overhead shot" — bukan "cinematic angle" (terlalu loose, model interpretasi bebas).

### 6. Physical specifics mengalahkan adjective stacks
"Overhead fluorescent light pooling on wet concrete, light fog at ankle height" > "dramatic, moody, atmospheric"

Model merender hal fisik, bukan kata sifat — berlaku universal.

---

## Aturan Style

### Style yang benar untuk Semesta Digital deck (illustration)
**Cinematic digital painting** — dramatic, high contrast, painterly but grounded.
Referensi konkret: key art film live-action thriller, Black Mirror promotional art, "Fifteen Million Merits" visual register.

Bukan:
- Editorial flat illustration — menghasilkan matte 2D magazine aesthetic di semua model
- Photorealism — terlalu stock photo
- Kartun / animasi — kehilangan dramatic weight
- Sci-fi concept art — terlalu tech-hero, floating in void
- 3D render isolated object — impersonal, clipart feeling

### Style yang benar untuk production video (Kling / Runway)
**Lihat `04-pipeline-ai-production.md` §2.2** — cinematic prompts untuk video berbeda dari illustration prompts untuk deck. Jangan campur.

### Mengapa "editorial illustration" selalu gagal
Kata "editorial illustration" di training data semua model paling sering diasosiasikan dengan flat magazine illustration. Model default ke sana, mengabaikan deskripsi adegan yang dramatic. Jangan gunakan frasa ini.

---

## Aturan Adegan

### Setiap prompt harus punya "kehidupan"
Gambar yang baik punya tension — ada sesuatu yang *terjadi*. Frame yang hanya mendeskripsikan suasana tanpa aksi menghasilkan stock photo / clipart.

Setiap prompt wajib punya minimal satu aksi fisik konkret yang bisa dirender.

### Berpikir sebagai director, bukan sebagai deskriptor
Tugas prompt writer adalah membuat keputusan artistik — bukan mendeskripsikan objek dan menyerahkan interpretasi ke model. Tanya: *apa yang dirasakan penonton saat melihat frame ini?* Jawaban itu yang masuk ke `action` dan `scene`, bukan deskripsi teknis objeknya.

### Konsistensi live actor (S1, S3, S5, S7, S9, S11, S13, S17)
Semua 8 segmen live actor harus menghasilkan kesan satu orang yang sama. Gunakan field `character_anchor` yang identik di semua 8 prompt — deskripsi fisik, pakaian, background identik kata per kata.

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
| 2026-06-09 | File dibuat sebagai GPT-specific | Konsolidasi prompt rules dari sesi iterasi S0 |
| 2026-06-09 | Renamed + reframed ke prinsip universal | Rules ini berlaku untuk semua model (Midjourney, Kling, Runway, GPT Image, dll.) — bukan GPT-only |
| 2026-06-09 | Style: cinematic digital painting | "Editorial illustration" default ke flat magazine style di semua model |
| 2026-06-09 | Constraint positif | Prompt negatif tidak stabil, tulis apa yang ada |
| 2026-06-09 | Action sebagai physical concrete event | Suasana/mood tidak dirender |
| 2026-06-09 | Tambah: berpikir sebagai director | Root cause clipart: deskripsi objek, bukan keputusan artistik |
