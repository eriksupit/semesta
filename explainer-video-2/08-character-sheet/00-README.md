---
title: Character & Wardrobe Sheet — Index & Method (GATE 0)
tags: [explainer-video-2, character-sheet, gate-0, readme, reference-locking]
status: active
created: 2026-06-19
updated: 2026-06-19
aliases: [ev2-08-readme, character-sheet-index]
---

# Character & Wardrobe Sheet — Index & Method (GATE 0)
## Konsep "Satu Keluarga, Satu Hari Penuh" · Semesta Digital *(working title)*

> **Folder role:** GATE 0 deliverable, split one file per character (9 plate prompts × N characters is too long for a single doc). This README holds the **shared method** (defined ONCE here); each character file holds only its identity lock + plate matrix + per-scene wardrobe.
> **Cites:** style tokens + artist anchors → [[07-style-reference]]. Field method + 6-layer order + banned-list → [[prompt-rules-image-generation]]. Scene truth → [[03-scene-detail]]. Process log → [[00-WORKLOG]].

---

## 1. File manifest
| File | Character | Scenes present | Status |
|---|---|---|---|
| `H-herman.md` | Herman (50) | SEQ1-SC01/02, SEQ2-SC02, SEQ3-SC03, SEQ4-SC01, SEQ6-SC01/03 | drafting |
| `R-ratna.md` | Ratna (45, hijabi) | SEQ1-SC02, SEQ2-SC03, SEQ3-SC01/02, SEQ4-SC03, SEQ5-SC02, SEQ6-SC01/02 | **COMPLETE — 12/12 plates approved** (9 uncovered turnaround + 3 hijab ref) |
| `L-lisa.md` | Lisa (20, creator) | SEQ2-SC01/04, SEQ3-SC04, SEQ4-SC02, SEQ5-SC01, SEQ6-SC01 | **COMPLETE — 9/9 plates approved** (uncovered turnaround, hair loose, body `34C` consistent) |
| `A-andi.md` | Andi (10) | SEQ2-SC03, SEQ4-SC04, SEQ6-SC01/02 | **COMPLETE — 9/9 plates approved** (uncovered turnaround, short crop, render-age 10) |
| `F-figurans.md` | 5 named single-scene figurans (Pak Darto, Tika, petugas bank, Rian, pembina muda) | SEQ2-SC01, SEQ3-SC01/02/03, SEQ4-SC04 | **COMPLETE — 14/14 plates approved** (Darto 3 · Tika 2 · petugas bank 3 · Rian 3 · pembina 3; adaptive set, front+profileA only, zero Profile B) |

Generated plates land in `../character-images/` (see naming §4).

---

## 2. What each character file contains
1. **Identity lock (FIXED)** — `character_identity` block (role, ethnicity, beauty, render-age, facial_features texture-only, body_features). Pasted verbatim into Lapis 3 of every prompt for that character. Render-age note: model ages subjects up — write below real age (real 50 → `46 years old`).
2. **Plate matrix (9 cells)** — baseline-outfit reference plates for Kling 3.0 reference-locking. See §3 template.
3. **Per-scene wardrobe table** — for each scene the character appears in: wardrobe + footwear (+ peci/hijab variant) tokens from [[07-style-reference]]; hair + makeup anchors stay fixed per character.

---

## 3. PLATE MATRIX TEMPLATE — 9 cells per character (3 view × 3 shot)
Each cell = **one separate image generation** (ChatGPT Image v2). All 9 share: the FIXED identity block + baseline neutral outfit + plain solid white background + flat even studio light + neutral relaxed face. Only **view tokens** + **shot/framing tokens** + **aspect_ratio** change.

> **POSITIVE-ONLY TOKENS (firm rule, `prompt-rules` negation ban).** Never write negation/absence — no `not in frame`, `no X`, `without X`. Model reads negation as licence to improvise → non-compliant. Describe only what IS in frame; for an element cropped out (e.g. footwear in a close-up) **omit the field entirely** rather than writing `"not in frame"`. Rewrite any negative as positive (`headless`, `faithful natural rendering`).
> **KEYWORD-LEAK (firm).** Beyond `no`/`non`: avoid any token whose dominant word drags an unwanted concept — `light-absorbing` leaks `light`, `low-sheen` leaks `sheen`, `non-reflective` leaks `reflective`. Use root-clean tokens.
> **MATTE PLATE STANDARD (locked, anti-sheen — applies to every character's hair field + plate lighting).** Hair finish: `dry matte hair, velvety matte strands, chalky matte finish, loosely combed natural`. Plate lighting: `flat even soft diffused three-point studio key, soft shadowless fill, matte skin and hair rendering, white seamless evenly lit` — **no `high-key`** (it drives specular gloss on dark hair). Colour stays a uniform state (`uniformly <colour> … even distribution throughout`), never a gradient.

**Aspect ratio per shot type (MANDATORY — GPT Image 2 supports all natively; each shot a distinct ratio so the subject is revealed optimally):**
- **Full body → `9:16`** (tallest; whole figure + headroom + floor visible)
- **Medium → `2:3`**
- **Close-up → `4:5`** (face fills frame; headshot ratio)

| # | View | Shot | aspect_ratio | View tokens | Shot/framing tokens |
|---|---|---|---|---|---|
| 1 | Frontal | Full body | `9:16` | `front view, facing camera straight-on, both ears visible symmetric, nose centered` | `full body shot, crown to sole visible, floor visible, generous headroom` |
| 2 | Frontal | Medium | `2:3` | (same front tokens) | `MS medium shot, waist up` |
| 3 | Frontal | Close-up | `4:5` | (same front tokens) | `CU close-up, face fills frame` |
| 4 | Profile A | Full body | `9:16` | `full profile view, head and torso rotated ninety degrees, single ear visible, nose in silhouette against background, near cheek toward camera` | `full body shot, crown to sole visible, floor visible` |
| 5 | Profile A | Medium | `2:3` | (same profile-A tokens) | `MS medium shot, waist up` |
| 6 | Profile A | Close-up | `4:5` | (same profile-A tokens) | `CU close-up, profile face fills frame` |
| 7 | Profile B | Full body | `9:16` | **generate by mirroring cell 4** (see §3.1) — `same character, opposite full profile, other cheek toward camera, nose silhouette pointing opposite direction` | `full body shot, crown to sole visible, floor visible` |
| 8 | Profile B | Medium | `2:3` | (same profile-B tokens) | `MS medium shot, waist up` |
| 9 | Profile B | Close-up | `4:5` | (same profile-B tokens) | `CU close-up, profile face fills frame` |

### 3.1 Direction-reliability protocol (WHY no "left/right")
Text-to-image models — including autoregressive ChatGPT Image v2 — are unreliable at parsing abstract "left/right" (documented spatial bias; OpenAI's own community reports left-right failures). So:
- **Never** anchor a view to screen "left/right". Anchor to **visible anatomy** (which cheek/ear shows) and to **silhouette direction**.
- **Profile B is generated as a MIRROR of Profile A using the Profile-A image as a reference upload**, not from a text "other side" instruction. Image-conditioning bypasses text-direction ambiguity.
- **Generation order:** Frontal first (anchor) → Profile A → Profile B (mirror via reference) → verify each render by which cheek/ear is visible; discard mislabeled.
- **Labelling:** files use `profileA` / `profileB`, never `left` / `right`.
- **CAMERA-RELATIVE convention (absolute — settles "whose perspective", film-industry standard).** Direction is always **camera-relative = screen/frame-relative = audience POV**, NEVER subject-relative. `camera-left`/`camera-right` mean the left/right side of the *frame* as the viewer sees it ([StudioBinder screen direction](https://www.studiobinder.com/blog/what-is-screen-direction-in-film/)). This removes the "my left vs your left vs subject's left" ambiguity that caused a mislabel on 2026-06-19. Convention:
  - **Profile A = subject faces `camera-left`** (locked for Herman by `H_herman_profileA_full.png`).
  - **Profile B = subject faces `camera-right`** (mirror).
  - All 3 shots of a profile face the SAME camera side. Write it in the prompt (`subject facing camera-left, full profile`) AND verify by which frame edge the nose points.
  - Caveat: t2i models don't reliably OBEY direction tokens even camera-relative → camera-relative is the unambiguous SPEC + verification anchor; **generation reliability for Profile B still comes from mirror-via-reference** (§ above).
  - When comparing two plates, align them side-by-side at FULL resolution before judging — downscaled thumbnails can deceive (lesson 2026-06-19).

---

## 4. Plate storage + naming (`../character-images/`)
**One subfolder per character** (parallel to `scene-images/`): `character-images/<TAG>_<char>/` (e.g. `H_herman/`), with a `_rejected/` subfolder per character for GATE-0 failures. Full convention → [[character-images/README]].
Filenames: `<TAG>_<character>_<view>_<shot>.png` — view ∈ {front, profileA, profileB}; shot ∈ {full, medium, closeup}.
Example: `character-images/H_herman/H_herman_front_full.png`, `…/H_herman_profileB_medium.png`.
9 plates per main character (Herman/Ratna/Lisa/Andi) = 36 plates; figurans lighter (front+profileA, key shots only). Keep only GATE-0-approved plates.

---

## 5. Usage contract (feeds GATE B)
1. Plates approved here (GATE 0) become the Kling 3.0 reference-lock set + the visual anchor when writing keyframe prompts.
2. Every GATE B prompt injects: Lapis 3 `character_style { makeup, wardrobe, hair, footwear }` from the per-scene wardrobe table + Lapis 6 `costume_designer`/`makeup_artist`/`hair_stylist` pairs from [[07-style-reference]] §5.
3. Garment colorway desaturated; warmth via `color_grade` only. Every visible garment specified affirmatively (anti-auto-batik).

---

*Character Sheet folder · Explainer Video 2 · 2026-06-19 · method defined once here, characters in sibling files*
