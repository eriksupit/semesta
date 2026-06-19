---
title: Interior Design Reference — Image Generation · Semesta Digital
tags: [tokens-reference, interior-design, image-generation]
status: active
created: 2026-06-10
updated: 2026-06-10
aliases: [interior-ref, design-style-ref]
---

# Interior Design Reference — Image Generation
## Semesta Digital (working title)
*Interior design style + designer as parent-child pair in `production_design_style` child token.*
*Use style name as gestalt anchor, then specify material tokens. Model trained on millions of design articles.*

---

## Structure in prompt

```json
"production_designer": "[film production designer]",
"production_design_style": "[interior_design_style]: [material tokens specific to scene]"
```

Example S4:
```json
"production_designer": "Eugenio Caballero",
"production_design_style": "Tropical Modernism: lived-in community architecture, organic timber post-and-beam, worn timber surface patina, human-scale space, tropical vegetation integrated into structure"
```

Example S14:
```json
"production_designer": "Mark Tildesley",
"production_design_style": "Contemporary Minimalist Corporate: precise controlled institutional interior, matte-painted light grey drywall, dark wood veneer table, recessed LED ceiling authority, no decorative objects"
```

---

## 1. INTERIOR DESIGN STYLES — MASTER LIST

Organised by cluster. Each entry: style name + core visual tokens + best use for Semesta Digital scenes.

---

### CLUSTER 1 — CALM & CONSIDERED

**Minimalist**
- Core tokens: `clean surfaces, deliberate negative space, single focal point per zone, muted monochromatic palette, concealed storage`
- Material: `matte white drywall, engineered timber floor, floating shelf minimal objects`
- Designer anchor: `John Pawson` — monastic minimalism, material purity
- Best for: S8 home workspace, S5/S7/S9/S11/S13 home office

**Japandi**
- Core tokens: `Scandinavian functionality merged Japanese restraint, low-profile furniture, intentional empty space, quality over quantity, muted neutral palette`
- Material: `pale ash timber, washi paper panel, matte ceramic, linen textile, brushed brass minimal fixture`
- Designer anchor: `Neri & Hu` (Shanghai) — East-West contemporary minimalism
- Best for: S8 workspace, S1 home office modern variant

**Wabi-Sabi**
- Core tokens: `beauty in imperfection and impermanence, weathered surfaces celebrated, organic irregular forms, tactile natural materials, nothing polished to perfection`
- Material: `unglazed ceramic, rough-hewn timber, textured plaster wall showing maker's mark, aged brass, worn linen`
- Designer anchor: `Axel Vervoordt` — wabi-sabi master, soulful spaces connected to nature
- Best for: S12 community elder, S2 domestic authentic

**Asian Zen**
- Core tokens: `meditative stillness, horizontal low lines, ryokan register, bamboo and stone, controlled natural light shafts`
- Material: `tatami mat or equivalent, sliding shoji-style panel, smooth river stone, dark-stained timber, minimal altar object`
- Designer anchor: `Kengo Kuma` — Japanese materiality, nature-integrated architecture
- Best for: S12 elder contemplative scene

---

### CLUSTER 2 — NATURAL & GROUNDED

**Tropical Modernism**
- Core tokens: `Geoffrey Bawa register, indoor-outdoor flow, passive ventilation implied, local material and craftsmanship, canopy light diffusion`
- Material: `exposed timber post-and-beam, compacted earth or polished concrete floor, rattan or woven fibre, stone or laterite wall, dense tropical foliage framing`
- Designer anchor: `Geoffrey Bawa` — father of Tropical Modernism, Sri Lankan/Southeast Asian
- Best for: S4 pavilion, S12 elder outdoor, S6 street adjacent

**Biophilic**
- Core tokens: `maximum nature connectivity, living walls or dense planting, natural light dominant, organic forms, material honesty`
- Material: `exposed concrete or raw plaster, moss wall or hanging plants, timber grain visible, natural stone surface, floor-to-ceiling glazing to greenery`
- Designer anchor: `Vo Trong Nghia` (Vietnam) — bamboo and biophilic tropical architecture
- Best for: S4 pavilion enhanced, S12 outdoor community

**Organic Modern**
- Core tokens: `curves over right angles, warm neutral palette, natural texture layering, sculptural forms, soft ambient light`
- Material: `curved plaster wall, bouclé or textured linen upholstery, travertine surface, oak timber, hand-thrown ceramic`
- Designer anchor: `Ilse Crawford` — human-centred organic design, sensory warmth
- Best for: S8 professional home workspace, S2 upgraded domestic

**Rustic / Vernacular**
- Core tokens: `authentic craft and local material, aged surfaces honoured, imperfect handmade objects, functional beauty`
- Material: `rough-sawn timber, unplaned beam, terracotta tile floor, handwoven textile, iron hardware`
- Designer anchor: `Joanna Gaines` — modern rustic farmhouse register
- Best for: S2 kitchen authentic, S4 pavilion raw variant

---

### CLUSTER 3 — URBAN & INDUSTRIAL

**Industrial**
- Core tokens: `factory-to-loft conversion, exposed structure celebrated, Edison bulb or track lighting, raw material palette`
- Material: `exposed brick or concrete block wall, steel beam or column, polished concrete floor, metal shelving, pendant industrial lamp`
- Designer anchor: `Philippe Starck` — industrial with wit and elegance
- Best for: S10 warehouse/showroom, S6 urban street adjacent

**Neo-Industrial / Soft Industrial**
- Core tokens: `industrial structure softened with warm material, functional yet livable, precision without coldness`
- Material: `brushed steel, concrete floor polished, timber accent warm, recessed LED strip, open plan`
- Designer anchor: `Neri & Hu` — contemporary Asian urban industrial
- Best for: S10 entrepreneur warehouse, co-working S3 background

**Brutalist**
- Core tokens: `raw concrete mass celebrated, bold geometric form, monumental scale, material honesty paramount`
- Material: `board-formed concrete wall, exposed aggregate, minimal fenestration, concrete floor, steel fixture`
- Designer anchor: `Le Corbusier` legacy — structural concrete exposed
- Best for: S3 night market adjacent architecture background

---

### CLUSTER 4 — CONTEMPORARY PROFESSIONAL

**Contemporary Minimalist Corporate**
- Core tokens: `precision controlled environment, institutional weight, clear hierarchy of space, quality material restrained`
- Material: `matte-painted light grey drywall, dark wood veneer surface, recessed LED ceiling downlight, upholstered conference chair, wall display screen`
- Designer anchor: `Mark Tildesley` (film PD) / `Gensler` (corporate interiors firm)
- Best for: S14 executive meeting room, S10 high-end showroom

**Modern Professional Workspace**
- Core tokens: `curated sparse surface, floating desk aesthetic, task-optimised layout, soft material accent`
- Material: `wall-mounted floating shelf, matte white drywall, fixed casement window, engineered oak floor, ceramic mug minimal desk`
- Designer anchor: `K.K. Barrett` (film PD) — Her aesthetic, near-future sparse
- Best for: S8 professional woman desk, S1/S5/S9 home office

**Scandinavian**
- Core tokens: `hygge warmth, functional beauty, natural material dominant, light maximised, clutter eliminated`
- Material: `pale birch or ash timber, white-washed wall, linen textile, ceramic pendant light, potted plant single`
- Designer anchor: `Norm Architects` (Copenhagen) — refined Nordic domesticity
- Best for: S8 workspace clean variant, S1 home office light

---

### CLUSTER 5 — COMMUNITY & VERNACULAR URBAN

**Jakarta Lower-Middle Urban Domestic**
- Core tokens: `compact urban kitchen register, cement-plaster wall unpainted, jalousie window, laminate or worn tile surface, ambient clutter of daily life`
- Material: `cement-plaster wall, ceramic floor tile 30x30 off-white, laminate countertop worn edge, open wooden shelf, jalousie window`
- Designer anchor: `Eugenio Caballero` (film PD) — lived-in authentic space
- Best for: S2 Ibu RT kitchen — VALIDATED

**Jakarta Working-Class Urban Street**
- Core tokens: `low-rise shophouse facade, asphalt road, functional public space, motorbike and street furniture`
- Material: `painted concrete shophouse facade, asphalt surface, steel or timber street furniture, overcast diffused urban daylight`
- Designer anchor: `Hannah Beachler` (film PD) — authentic community street
- Best for: S6 courier street

**Community Pavilion Tropical**
- Core tokens: `semi-outdoor social gathering space, organic timber structure, tropical canopy overhead, compacted earth or concrete floor, human-scale intimate`
- Material: `exposed timber post-and-beam, corrugated fibre-cement or palm leaf soffit, compacted earth floor, low wooden bench`
- Designer anchor: `Geoffrey Bawa` / `Eugenio Caballero` hybrid
- Best for: S4 pemuda pavilion — VALIDATED, S12 elder outdoor

---

## 2. INTERIOR DESIGNER REFERENCE — PARENT ANCHOR

These names go in `production_designer` field (Lapis 6) or as anchor in `production_design_style`.
**Rule: name in `production_designer` field, style detail in `production_design_style` child.**

| Designer | Nationality | Style | Best For Semesta |
|---|---|---|---|
| `Axel Vervoordt` | Belgium | Wabi-sabi, timeless minimalism, soulful spaces, natural texture | S12 elder, S2 authentic domestic |
| `Ilse Crawford` | UK | Human-centred organic, sensory warmth, natural material | S8 workspace, S2 domestic |
| `Neri & Hu` | China/Shanghai | Contemporary Asian minimalism, East-West hybrid, urban precision | S10 entrepreneur, S8 corporate-adjacent |
| `Geoffrey Bawa` | Sri Lanka | Tropical Modernism, indoor-outdoor flow, local craft | S4 pavilion, S12 outdoor |
| `Vo Trong Nghia` | Vietnam | Biophilic tropical, bamboo and concrete, sustainable vernacular | S4 pavilion variant |
| `John Pawson` | UK | Monastic minimalism, material purity, deliberate void | S8 home workspace minimal |
| `Kengo Kuma` | Japan | Nature-integrated architecture, dissolving boundary inside-outside | S12 contemplative |
| `Kelly Wearstler` | USA | Bold maximalist, layered texture, glamorous material | Not recommended Semesta (too luxury) |
| `Norm Architects` | Denmark | Refined Nordic domesticity, hygge warmth, pale timber | S1/S5 home office clean |
| `K.K. Barrett` | USA (film PD) | Curated sparse near-future domestic | S8/S1/S5 home workspace |
| `Eugenio Caballero` | Mexico (film PD) | Lived-in naturalistic community, worn surface patina | S2/S4/S12 |
| `Hannah Beachler` | USA (film PD) | Authentic community street, functional materials | S6/S10 |
| `Mark Tildesley` | UK (film PD) | Institutional corporate precision | S14/S10 |

---

## 3. SCENE-TO-STYLE MAPPING — ALL 18 SCENES

| Scene | Interior Design Style | Designer Anchor | Key Material Tokens |
|---|---|---|---|
| S0 Cold Open | Neo-Industrial Corporate | K.K. Barrett | oak veneer desk, steel legs, four monitors, curtain wall glazing, acoustic ceiling |
| S1 Live Actor F | Modern Professional Workspace | K.K. Barrett | exposed concrete wall, open bookshelf, fixed-pane window, oak floor |
| S2 Ibu RT | Jakarta Lower-Middle Urban Domestic | Eugenio Caballero | cement-plaster wall, ceramic tile floor, laminate countertop, jalousie window |
| S3 Live Actor M | Neo-Industrial Urban Night | Hannah Beachler | expansive polished concrete plaza, modular steel-timber vendor booth, LED strip overhead |
| S4 Pemuda | Tropical Modernism / Community Pavilion | Eugenio Caballero | timber post-and-beam, fibre-cement soffit, compacted earth floor, tropical canopy |
| S5 Live Actor F | Modern Professional Workspace | K.K. Barrett | exposed concrete wall, open bookshelf, fixed-pane window, oak floor |
| S6 Kurir | Jakarta Working-Class Urban Street | Hannah Beachler | asphalt road, shophouse facade, motorbike foreground, overcast urban daylight |
| S7 Live Actor M | Modern Professional Workspace | K.K. Barrett | exposed concrete wall, open bookshelf, fixed-pane window, oak floor |
| S8 Profesional F | Organic Modern / Japandi | Ilse Crawford | matte-painted drywall off-white, fixed casement window, wall-mounted floating desk, ceramic mug |
| S9 Live Actor F | Modern Professional Workspace | K.K. Barrett | exposed concrete wall, open bookshelf, fixed-pane window, oak floor |
| S10 Pengusaha | Soft Industrial / Warehouse Showroom | Hannah Beachler | concrete block wall, polished concrete floor, industrial pendant lamp, steel shelving, product boxes |
| S11 Live Actor M | Modern Professional Workspace | K.K. Barrett | exposed concrete wall, open bookshelf, fixed-pane window, oak floor |
| S12 Tokoh | Tropical Modernism / Wabi-Sabi | Eugenio Caballero | timber post-and-beam, compacted earth, rattan chair, tropical canopy soft light |
| S13 Live Actor F | Modern Professional Workspace | K.K. Barrett | exposed concrete wall, open bookshelf, fixed-pane window, oak floor |
| S14 Eksekutif | Contemporary Minimalist Corporate | Mark Tildesley | matte light grey drywall, dark wood veneer table, recessed LED downlight, wall display |
| S15 Konvergensi | Composite all zones | All | each zone carries its own style — unified by shared central radiance |
| S16 Data | Typographic / Black field | — | near-black background, pure white typography, no spatial elements |
| S17 Live Actor M | Modern Professional Workspace | K.K. Barrett | exposed concrete wall, open bookshelf, fixed-pane window, oak floor |

---

## 4. MATERIAL TOKEN LIBRARY

### Wall finishes
| Token | Style | Scene |
|---|---|---|
| `exposed concrete feature wall unpainted` | Industrial / Modern | S1/S3/S5/S7 home office |
| `cement-plaster wall unpainted rough texture` | Vernacular domestic | S2 kitchen |
| `matte-painted drywall off-white` | Contemporary professional | S8/S14 |
| `matte-painted light grey drywall` | Corporate minimalist | S14 |
| `exposed brick wall rough mortar` | Industrial | S10 |
| `board-formed concrete wall` | Brutalist / S0 |
| `textured plaster wall showing maker's mark` | Wabi-sabi | S12 |
| `timber post-and-beam structure visible` | Tropical vernacular | S4/S12 |

### Floor finishes
| Token | Style | Scene |
|---|---|---|
| `engineered oak flooring warm grain` | Modern domestic | S1/S5/S7/S9 |
| `ceramic floor tile 30x30 off-white` | Vernacular domestic | S2 |
| `compacted earth floor` | Tropical vernacular | S4/S12 |
| `polished concrete floor` | Industrial/urban | S3/S10 |
| `brushed concrete floor` | Corporate | S14 |

### Furniture + fixtures
| Token | Style | Scene |
|---|---|---|
| `built-in open bookshelf unit books potted plants` | Contemporary home | S1/S5/S7/S9 |
| `wall-mounted floating desk shelf` | Minimalist workspace | S8 |
| `low wooden bench table surface` | Tropical vernacular | S4 |
| `rattan low chair` | Tropical vernacular | S12 |
| `dark wood veneer conference table edge` | Corporate | S14 |
| `industrial steel shelving units` | Warehouse | S10 |
| `pendant industrial lamp fixture overhead` | Industrial | S10 |
| `recessed LED ceiling downlights` | Corporate minimalist | S14 |
| `jalousie window` | Jakarta domestic | S2 |
| `fixed-pane window large` | Modern home | S1/S5/S7/S8 |
| `floor-to-ceiling glazed curtain wall` | Corporate/S0 | S0/S14 |

---

## 5. RULES

- **Interior design style name = gestalt anchor** — model trained on millions of design magazine articles, recognises style name before material tokens
- **Style name goes in `production_design_style` child** — not as standalone field
- **Material tokens follow style name** — format: `[Style Name]: [material token 1], [material token 2], ...`
- **BANNED for Semesta Digital:** maximalist (too luxury), Hollywood Regency (wrong register), Art Deco (wrong era), Moroccan/Bohemian (wrong geography)
- **BANNED material tokens in `scene` field:** geographic labels (`Jakarta kitchen`, `traditional Indonesian`), ethnic labels (`Javanese decor`), motif labels (`batik pattern wall`)
- **Always pair** interior design style with film production designer — double anchor

---

*Interior Design Reference v1.0 · Semesta Digital · 10 Juni 2026*
*Sources: SampleBoard, House Beautiful, Design Pataki, Authentic Interior, Bocado Lobo*
*Validated: S2 (Jakarta Lower-Middle Domestic), S3 (Neo-Industrial Night), S4 (Tropical Modernism)*
