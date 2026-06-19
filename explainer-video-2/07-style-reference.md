---
title: Style Reference — Explainer Video 2 (Wardrobe · Hair · Makeup + Artist Anchors)
tags: [explainer-video-2, style-reference, wardrobe, hair, makeup, image-generation, gate-0]
status: active
created: 2026-06-19
updated: 2026-06-19
aliases: [ev2-07-style-reference, ev2-style-ref, wardrobe-hair-makeup-reference]
---

# Style Reference — Explainer Video 2
## Konsep "Satu Keluarga, Satu Hari Penuh" · Semesta Digital *(working title)*

> **Role:** the styling foundation for GATE 0. Catalogs wardrobe / hair / makeup / footwear **styles + artist/expert anchors** for this video's cast, then maps each anchor to each character. Cited by `08-character-sheet.md` (per-character locks) and by every GATE B prompt (Lapis 3 + Lapis 6).
> **Inheritance, not duplication:** the generic token libraries already exist and are **inherited by link, never copied** —
> - Wardrobe/hair/makeup/footwear token libraries → [[tokens-references/TOKENS-REFERENCE]] §7 makeup · §8 wardrobe · §9 hair · §10 footwear
> - Costume + makeup crew anchors → [[tokens-references/CREW-REFERENCE]] §5 costume · §6 makeup
> - Field method, 6-layer order, banned-list → [[prompt-rules-image-generation]]
> This document adds only the **DELTAS** this cast needs (modest/hijab, child, mature-age, warm-grade) + the **new hair anchor** that the old references lack + the per-character mapping.
> **Grade note:** video uses a WARM grade (override of cool deck-standard, `prompt-rules` b.208). Warmth comes from `color_grade` ONLY — **garment colorway stays desaturated** to avoid the amber-drift failure (validated S4/S11). Never push warmth through fabric color.

---

## 1. Cast (style targets)
| Tag | Character | Age | Vertical context | Styling register |
|---|---|---|---|---|
| H | Herman | 50 | supervisor ekspor-impor + trader | mature male, modest middle-class, neat-worn |
| R | Ratna | 45 | UMKM kuliner (hijabi) | mature hijabi entrepreneur, practical modest |
| L | Lisa | 20 | mahasiswi + content creator | young urban woman, contemporary styled |
| A | Andi | 10 | SD daring | child boy, simple healthy everyday |
| F* | recurring figurans | — | Tika, Bu Sari, Rian, kolega, kurir, tetangga | light locks at recurrence points |

---

## 2. ARTIST / EXPERT ANCHOR ROSTER

### 2.1 Wardrobe — costume anchors (inherited [[tokens-references/CREW-REFERENCE]] §5)
| Anchor | Child-style tokens | Applies to |
|---|---|---|
| `Deborah Hopper` | `character-authentic casual wear, fabric worn laundered, class-accurate daily register` | H daily, R domestic/UMKM, F neighbours |
| `Michael Wilkinson` | `contemporary urban wardrobe, precise class register, modern professional polish` | L creator/campus, professional contexts |
| `Ann Roth` | `character-driven naturalistic, authentic worn texture, lived-in fabric, no aspirational signal` | mature register reinforcement (H/R) |

**DELTA — modest/hijab wardrobe (no film-designer anchor; expert source anchor):** source `modest-fashion construction convention` — tokens in §3.1 below. Method: specify garment construction affirmatively; ethnic/print labels BANNED (auto-batik rule, `prompt-rules` b.331).

### 2.2 Makeup — makeup-artist anchors (inherited [[tokens-references/CREW-REFERENCE]] §6)
| Anchor | Child-style tokens | Applies to |
|---|---|---|
| `Eryn Krueger Mekash` | `naturalistic everyday beauty, lived-in skin, real-person feel` | H, R, F community |
| `Judy Chin` | `natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish` | L (default) |
| `Naomi Donne` | `clean photorealistic skin, precise contemporary beauty, high-definition cinema ready` | only if a polished/formal beat arises |

### 2.3 Hair — NEW anchors (absent in old references; researched 2026-06-19)
*Old references had no hair-department anchor — hair was token-only (Paul Mitchell as token source). These film hair anchors give hair true anchor parity with costume/makeup.*

| Anchor | Child-style tokens | Applies to | Source |
|---|---|---|---|
| `Anissa Salazar` | `naturalistic everyday Asian-family hair, real-texture straight black, unstyled lived-in finish` | PRIMARY — whole family baseline | *Everything Everywhere All At Once* |
| `Camille Friend` | `culturally authentic hairline framing, textured natural body, dignified grooming` | R hijab-framed hairline, L styled young-woman | *Black Panther* hair dept head |
| `Tim Muir` | `naturalistic mature register, graying authentic, neat working-class grooming` | H (50, graying) | *Yellowstone* hair dept head |

---

## 3. STYLE DELTA CATALOGS (cast-specific; generic base inherited from TOKENS-REFERENCE)

### 3.1 Wardrobe — modest / mature / child deltas
*(Base fabric/construction/fit/colorway tokens → [[tokens-references/TOKENS-REFERENCE]] §8. Below = additions only.)*

**Hijab / modest-wear construction tokens (R + female figurans):**
| Token | Use |
|---|---|
| `square voile hijab neatly pinned, opaque matte weave, draped over shoulders` | R standard everyday |
| `instant-jersey hijab snug fit, soft matte knit, no visible hairline` | R cooking/active beats |
| `long-sleeve tunic blouse, relaxed modest cut, mid-thigh length, plain weave` | R top layer |
| `wide-leg modest trousers, cotton twill, full-length, solid uniform colorway` | R bottom |
| `loose cardigan over tunic, soft knit, hip-length` | R outer / community |

**Mature-male tokens (H, 50):**
| Token | Use |
|---|---|
| `short-sleeve cotton-poplin shirt, soft collar, relaxed fit, muted solid` | H home/office casual |
| `batik-free plain safari-cut shirt, structured cotton, two chest pockets` | H office (explicitly plain, anti-auto-batik) |
| `pressed cotton-twill trousers, mid-rise straight, charcoal solid` | H bottom |

**Child tokens (A, 10):**
| Token | Use |
|---|---|
| `child crew-neck cotton tee, soft jersey, relaxed fit, muted solid` | A everyday |
| `child elastic-waist shorts, cotton twill, knee-length` | A home |
| `child school polo, soft pique knit, plain solid` | A study beat |

**Colorway:** desaturated only (§8 list). Warmth via grade, NOT garment. BANNED: batik, paisley, ikat, floral, ethnic print, terracotta, ochre, amber, golden.

### 3.2 Hair — modest / mature / child / young-creator deltas
*(Base cuts/barbering → [[tokens-references/TOKENS-REFERENCE]] §9. Below = additions only.)*

| Token | Character |
|---|---|
| `hair fully covered by hijab, no visible strands, smooth covered crown` | R standard |
| `minimal front hairline visible under loose hijab, neat parted, matte` | R relaxed-home variant |
| `short side-part, salt-and-pepper graying temples, natural matte finish, neatly combed` | H (50) |
| `child short natural crop, side parting, soft matte finish` | A (10) |
| `long straight black hair, middle part, glossy healthy finish, half-up clip` | L campus |
| `long straight black hair, low ponytail, face-framing wisps, glossy finish` | L creator-on-camera |

**BANNED:** `natural black hair shoulder length` (generic, `prompt-rules`); covered-hair must read as deliberate hijab, never bald.

### 3.3 Makeup — warm-grade / mature / child / hijabi deltas
*(Base layers base+feature+finish → [[tokens-references/TOKENS-REFERENCE]] §7. Three-layer rule still mandatory. Below = additions only.)*

| Token set | Character |
|---|---|
| `light tinted moisturizer natural coverage, softly defined brows clear lip balm minimal blush flush, translucent loose powder set matte finish zero shine` | R (hijabi natural, mature) |
| `BB cream sheer coverage, groomed brows even skin tone, matte setting powder zero shine, fine mature texture preserved` | H (50, male, lived-in) |
| `bare healthy skin, no makeup, clear even child complexion, zero shine` | A (10) |
| `medium-coverage satin foundation poreless, defined brows lash mascara nude glossy lip soft bronzer, baked setting powder matte finish zero shine` | L (young, on-camera ready) |

**Warm-grade note:** finish stays matte zero-shine; warmth comes from `color_grade`, not from amber makeup tones. BANNED: `HD makeup`, `HD setting powder`, makeup without finish layer.

### 3.4 Footwear deltas
*(Base → [[tokens-references/TOKENS-REFERENCE]] §10.)*
| Token | Character |
|---|---|
| `flat slip-on mules, matte leather, minimal` | R home/UMKM |
| `plain leather loafers, soft sole, muted` | H office |
| `child velcro canvas sneakers, rubber sole, plain` | A |
| `clean white low-top canvas sneakers, rubber sole` | L |

---

## 4. NEW SCHEMA ELEMENT — Lapis 6 hair pair (sub-decision approved 2026-06-19)
Add a hair anchor pair alongside `costume_designer` / `makeup_artist`, parity in Lapis 6:
```json
"hair_stylist": "[name from §2.3]",
"hair_style": "[4–6 tokens from §2.3 / §3.2]"
```
- Names in Lapis 6 = style anchor ONLY (never Lapis 1 — `prompt-rules` b.77).
- To be reflected in `prompt-rules` field list + [[tokens-references/CREW-REFERENCE]] §6.5 when GATE B authoring begins.

---

## 5. ANCHOR → CHARACTER MAP (quick reference for GATE B)
| Character | Costume | Makeup | Hair |
|---|---|---|---|
| Herman (50) | Deborah Hopper / Ann Roth | Eryn Krueger Mekash | Tim Muir |
| Ratna (45, hijabi) | Deborah Hopper | Eryn Krueger Mekash | Camille Friend |
| Lisa (20, creator) | Michael Wilkinson | Judy Chin | Camille Friend |
| Andi (10) | Deborah Hopper | (bare healthy skin) | Anissa Salazar |
| Family baseline | — | — | Anissa Salazar |
| Figurans (F*) | Deborah Hopper | Eryn Krueger Mekash | Anissa Salazar |

---

## 6. USAGE CONTRACT
1. `08-character-sheet.md` locks each character's identity + per-scene wardrobe/hair/makeup/footwear by **citing token sets from §3 + anchors from §5**.
2. Every GATE B prompt injects: Lapis 3 `character_style { makeup, wardrobe, hair, footwear }` from the per-scene lock + Lapis 6 `costume_designer`/`makeup_artist`/`hair_stylist` pairs from §5.
3. Garment colorway desaturated; warmth via `color_grade` only.
4. Every visible garment specified affirmatively (anti-auto-batik); negation BANNED.

---

*Style Reference v1.0 · Explainer Video 2 · 2026-06-19 · inherits [[tokens-references/TOKENS-REFERENCE]] + [[tokens-references/CREW-REFERENCE]] · process log `00-WORKLOG.md`*
