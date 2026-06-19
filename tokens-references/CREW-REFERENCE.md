---
title: Crew Reference — Image Generation · Semesta Digital
tags: [tokens-reference, crew-reference, image-generation]
status: active
created: 2026-06-10
updated: 2026-06-10
aliases: [crew-ref, director-ref]
---

# Crew Reference — Image Generation
## Semesta Digital (working title)

*Six crew roles as Lapis 6 parent-child pairs.*
*Related files: [[TOKENS-REFERENCE]] · [[INTERIOR-DESIGN-REFERENCE]] · [[prompt-rules-image-generation]]*

---

## CORE PRINCIPLE — TOKEN DISCIPLINE

**One strong name = gestalt anchor covering many things. Trust the model.**

- Token strings, not sentences
- No conjunctions, no copulas, no to-be verbs, no tenses
- No negations (no X, not X, un-, non-)
- No abstract labels ("warm", "natural", "realistic") — model interprets these freely
- No redundancy across fields — if facial_features has it, makeup_style drops it
- Adjective-dense C2 English: precise, concrete, industry-convention terminology
- Child style = 4–6 tokens maximum, each load-bearing

**WRONG:** `"natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish, zero performance artifice, authentic real-person face"`
→ redundant, abstract labels, negation

**RIGHT:** `"natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish"`
→ 3 concrete tokens, each distinct, no overlap

---

## STRUCTURE — LAPIS 6 (mandatory position)

```json
"framing": "...",
"angle": "...",
"camera": "...",
"lighting": "...",
"aspect_ratio": "16:9",

"director": "[name]",
"directing_style": "[4–6 tokens]",

"lighting_director": "[name]",
"lighting_style": "[4–6 tokens]",

"production_designer": "[film PD name]",
"production_design_style": "[Interior Style Name]: [4–6 material tokens]",

"interior_designer": "[interior designer name]",
"interior_design_style": "[Interior Style Name]: [4–6 spatial tokens]",

"costume_designer": "[name]",
"costume_style": "[4–6 tokens]",

"makeup_artist": "[name]",
"makeup_style": "[4–6 tokens]"
```

**CRITICAL:** Names in Lapis 1 → model generates their face. Names in Lapis 6 → style anchor only.
**NOTE:** `Roger Deakins` always in `color_grade` (Lapis 1) — never in `lighting_director`.

---

## 1. DIRECTOR

Controls: narrative register, camera-subject relationship, pacing feel.

| Name | Child style tokens | Best scenes |
|---|---|---|
| `Annie Leibovitz` | `intimate portrait directness, subject fully present camera, forward energy mid-argument` | S1/S3/S5/S7/S9/S11/S13/S17 live actor |
| `Alfonso Cuarón` | `intimate observational realism, subject embedded environment, unhurried natural rhythm` | S2/S4/S6/S12 community/domestic |
| `Hirokazu Kore-eda` | `quiet domestic authenticity, everyday ritual dignity, unhurried witnessing` | S2/S12 domestic/elder |
| `Bong Joon-ho` | `social realism precise spatial irony, layered class environment, controlled mise-en-scène` | S8/S10/S14 professional/corporate |
| `Apichatpong Weerasethakul` | `tropical semi-outdoor liminal observation, slow organic presence, nature-human boundary dissolving` | S4/S12 outdoor |
| `Gregory Crewdson` | `large-format interior stillness, human absence eerie, fully functional space awaiting` | S0 cold open only |

---

## 2. LIGHTING DIRECTOR (DP / Cinematographer)

Controls: light source quality, shadow character, skin luminosity, color temperature.
`Roger Deakins` = color palette anchor in `color_grade` — not here.

| Name | Child style tokens | Best scenes |
|---|---|---|
| `Emmanuel Lubezki` | `diffused canopy natural daylight, soft directionless key, screen glow secondary fill` | S3/S4/S6/S12 outdoor |
| `Hoyte van Hoytema` | `cool clean interior recessed LED key, precise professional fill, controlled directional` | S1/S5/S7/S8/S9/S11/S13/S14/S17 indoor |
| `Bradford Young` | `warm natural bounce community daylight, ambient fill, intimate soft key` | S2/S12 domestic/community warm |
| `Roger Deakins` | `lifted blacks medium gray, cyan-teal shadows, clean whites, Kodak 2383` | color_grade field only |

---

## 3. PRODUCTION DESIGNER (Film PD)

Controls: set construction, physical environment, spatial authenticity.
Always paired with `interior_designer` for double anchor.
Full style + material library: [[INTERIOR-DESIGN-REFERENCE]]

| Name | Style anchor | Best scenes |
|---|---|---|
| `Eugenio Caballero` | Tropical Modernism, lived-in vernacular, worn patina | S2/S4/S12 |
| `K.K. Barrett` | Sparse near-future domestic, curated minimal surfaces | S1/S5/S7/S8/S9/S11/S13/S17 home office |
| `Hannah Beachler` | Authentic community street, honest functional materials | S3/S6/S10 |
| `Mark Tildesley` | Institutional corporate precision, dark wood veneer, recessed authority | S14 |

**Format:**
```json
"production_designer": "Eugenio Caballero",
"production_design_style": "Tropical Modernism: exposed timber post-and-beam, compacted earth floor, rattan woven fibre accent, worn timber surface patina, tropical foliage integrated"
```

---

## 4. INTERIOR DESIGNER

Controls: spatial philosophy, material language, design style gestalt.
Paired with `production_designer` for double anchor.
Full reference: [[INTERIOR-DESIGN-REFERENCE]]

| Name | Style | Child style tokens | Best scenes |
|---|---|---|---|
| `Geoffrey Bawa` | Tropical Modernism | `indoor-outdoor flow, passive ventilation, local craftsmanship, canopy light diffusion, organic spatial rhythm` | S4/S12 |
| `Axel Vervoordt` | Wabi-Sabi | `beauty imperfection impermanence, weathered surfaces celebrated, tactile natural materials, soulful spatial serenity` | S12/S2 |
| `Ilse Crawford` | Organic Modern | `human-centred organic, sensory warmth, natural material dominant, curved soft form` | S8/S2 |
| `Neri & Hu` | Japandi / Asian Contemporary | `East-West minimalist hybrid, clean restrained line, quality over quantity, urban precision` | S10/S8 |
| `K.K. Barrett` | Modern Professional Workspace | `curated sparse surface, floating desk aesthetic, task-optimised layout, soft material accent` | S1/S5/S7/S8/S9 |
| `John Pawson` | Minimalist | `monastic material purity, deliberate void, single focal point per zone, concealed storage` | S8 workspace minimal |
| `Kengo Kuma` | Asian Zen | `nature-integrated architecture, dissolving inside-outside boundary, bamboo stone horizontal` | S12 contemplative |
| `Hannah Beachler` | Industrial / Community Urban | `authentic functional street, honest urban materials, working-class spatial register` | S3/S6/S10 |
| `Mark Tildesley` | Contemporary Corporate | `precise controlled institutional, corporate weight, architectural authority, no decorative objects` | S14 |

**Format:**
```json
"interior_designer": "Geoffrey Bawa",
"interior_design_style": "Tropical Modernism: indoor-outdoor flow, passive ventilation, local craftsmanship, canopy light diffusion, organic spatial rhythm"
```

---

## 5. COSTUME DESIGNER

Controls: wardrobe register, class calibration, fabric authenticity.

| Name | Child style tokens | Best scenes |
|---|---|---|
| `Michael Wilkinson` | `contemporary urban wardrobe, precise class register, modern professional polish` | S1/S3/S5/S7/S9/S11/S13/S17 live actor, S8/S10/S14 |
| `Deborah Hopper` | `character-authentic casual wear, fabric worn laundered, class-accurate daily register` | S2/S4/S6/S12 |
| `Ann Roth` | `character-driven naturalistic, authentic worn texture, lived-in fabric, no aspirational signal` | S12 elder |
| `Mark Bridges` | `precise contemporary period-adjacent, fabric integrity, professional polish` | S10/S8 |

---

## 6. MAKEUP ARTIST

Controls: skin quality, finish level, character beauty register.
Default: `Judy Chin` for all scenes.

| Name | Child style tokens | Best scenes |
|---|---|---|
| `Judy Chin` | `natural photorealistic skin, portrait-level detail, character-appropriate contemporary finish` | All — primary default |
| `Naomi Donne` | `clean photorealistic skin, precise contemporary beauty, high-definition cinema ready` | S14 executive, S8 corporate |
| `Eryn Krueger Mekash` | `naturalistic everyday beauty, lived-in skin, real-person feel` | S2/S4/S12 domestic/community |

---

## 7. QUICK REFERENCE TABLE — ALL 18 SCENES

| Scene | Director | Lighting Dir | Film PD | Interior Designer | Costume | Makeup |
|---|---|---|---|---|---|---|
| S0 Cold Open | Gregory Crewdson | Hoyte van Hoytema | K.K. Barrett | K.K. Barrett | — | — |
| S1 Live Actor F | Annie Leibovitz | Hoyte van Hoytema | K.K. Barrett | K.K. Barrett | Michael Wilkinson | Judy Chin |
| S2 Ibu RT | Hirokazu Kore-eda | Bradford Young | Eugenio Caballero | Axel Vervoordt | Deborah Hopper | Eryn Krueger Mekash |
| S3 Live Actor M | Annie Leibovitz | Emmanuel Lubezki | Hannah Beachler | Hannah Beachler | Michael Wilkinson | Judy Chin |
| S4 Pemuda | Alfonso Cuarón | Emmanuel Lubezki | Eugenio Caballero | Geoffrey Bawa | Deborah Hopper | Judy Chin |
| S5 Live Actor F | Annie Leibovitz | Hoyte van Hoytema | K.K. Barrett | K.K. Barrett | Michael Wilkinson | Judy Chin |
| S6 Kurir | Alfonso Cuarón | Emmanuel Lubezki | Hannah Beachler | Hannah Beachler | Deborah Hopper | Judy Chin |
| S7 Live Actor M | Annie Leibovitz | Hoyte van Hoytema | K.K. Barrett | K.K. Barrett | Michael Wilkinson | Judy Chin |
| S8 Profesional F | Bong Joon-ho | Hoyte van Hoytema | K.K. Barrett | Ilse Crawford | Michael Wilkinson | Naomi Donne |
| S9 Live Actor F | Annie Leibovitz | Hoyte van Hoytema | K.K. Barrett | K.K. Barrett | Michael Wilkinson | Judy Chin |
| S10 Pengusaha | Bong Joon-ho | Hoyte van Hoytema | Hannah Beachler | Neri & Hu | Michael Wilkinson | Judy Chin |
| S11 Live Actor M | Annie Leibovitz | Hoyte van Hoytema | K.K. Barrett | K.K. Barrett | Michael Wilkinson | Judy Chin |
| S12 Tokoh | Hirokazu Kore-eda | Bradford Young | Eugenio Caballero | Axel Vervoordt | Ann Roth | Eryn Krueger Mekash |
| S13 Live Actor F | Annie Leibovitz | Hoyte van Hoytema | K.K. Barrett | K.K. Barrett | Michael Wilkinson | Judy Chin |
| S14 Eksekutif | Bong Joon-ho | Hoyte van Hoytema | Mark Tildesley | Mark Tildesley | Michael Wilkinson | Naomi Donne |
| S15 Konvergensi | Alfonso Cuarón | Emmanuel Lubezki | Eugenio Caballero | Geoffrey Bawa | — | — |
| S16 Data | — | — | — | — | — | — |
| S17 Live Actor M | Annie Leibovitz | Hoyte van Hoytema | K.K. Barrett | K.K. Barrett | Michael Wilkinson | Judy Chin |

---

## 8. TOKEN DISCIPLINE — FIELD AUDIT CHECKLIST

Before finalising any crew field, verify:
- [ ] Name in Lapis 6 only — never Lapis 1
- [ ] Child style = 4–6 tokens, noun/adjective strings only
- [ ] No copulas (is, are, was), no to-be, no tenses
- [ ] No conjunctions (and, but, with) — use comma separation
- [ ] No negations (no, not, un-, non-, zero)
- [ ] No overlap with other fields (facial_features ≠ makeup_style content)
- [ ] No abstract quality labels ("warm", "natural", "authentic") unless industry-convention term
- [ ] `production_design_style` format: `"[Style Name]: [tokens]"`
- [ ] `interior_design_style` format: `"[Style Name]: [tokens]"`

---

*Crew Reference v2.0 · Semesta Digital · 10 Juni 2026*
*Validated: S4 v2 (Cuarón + Lubezki + Caballero + Geoffrey Bawa + Hopper + Judy Chin) APPROVED*
*Related: [[TOKENS-REFERENCE]] · [[INTERIOR-DESIGN-REFERENCE]] · [[prompt-rules-image-generation]]*
