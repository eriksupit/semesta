---
title: GATE 0-ENV — Environment Reference Model (Method + Registry)
tags: [explainer-video-2, gate-0-env, environment, reference-model, image-generation]
status: active
created: 2026-06-21
updated: 2026-06-21
aliases: [ev2-09-env-readme, gate0-env-method, environment-reference]
---

> **Role:** the GATE 0-ENV counterpart of `08-character-sheet/00-README`. Defines how we build **empty-room environment reference plates** per location, so every keyframe in that location is spatially consistent and Kling 3.0 can reference-lock the space (not just the faces).
> **Why this exists:** text prompts cannot reliably lock room geometry / furniture position across shots (proven failure: subject rendered *beside* the bed instead of *on* it). Environment plates are to SPACE what GATE 0 character plates are to FACES.
> **Reads:** scene truth `03-scene-detail.md` · style backbone `07-style-reference.md` · prompt rules `prompt-rules-image-generation.md` · governance `00-WORKLOG.md` (incl. ADDENDUM A1).

---

## 1. Principles (locked)

1. **Empty room, no characters.** Plates capture space + set dressing only. Characters are composited later via their own GATE 0 plates at the keyframe.
2. **Neutral grade, not the warm video grade.** Plates render true-to-life neutral so the WARM `color_grade` + per-scene practical lighting are applied at GATE B keyframes, NOT baked into the plate. (Same discipline as character plates, `lessons` GATE 0.)
3. **ADDENDUM A1 applies.** Zero graphics. Device screens (TV, monitor, phone) render **off/neutral** — any UI is added in After Effects.
4. **Scoped-angle, NOT literal 360.** Generate only the angles the location's shots in `03` actually use (adaptive-set logic, same as figurans). A 360 spin is wasteful and t2i-unreliable.
5. **House architectural anchor (shared).** The 6 home rooms (E1–E6) inherit ONE architecture/material style anchor for cross-room continuity — like the family hair anchor. Defined in §3.
6. **Direction protocol** mirrors character plates: anchor angles to visible architecture (which wall / window / doorway), generate the master first then derive coverage; reverse angle via reference-image of the master where the 180° line matters. Positive-only tokens, zero negation.

## 2. Scoped-angle rubric (per environment)

Default plate set per location — keep only what its shot-list needs:
- **MASTER / establishing wide** — full room geography, the anchor plate (ALWAYS).
- **REVERSE (≈180°)** — opposite wall, only if shots cross the line / show the far side.
- **KEY ANGLE(s)** — the specific camera setups the location's shots use (read from `03` shot-list: shot size + lens).
- **DETAIL / insert corner** — only if a prop area is featured (e.g. nightstand, shop counter, big screen wall).

> Each environment's exact angle list is finalized **when that env's plates are authored**, read against its `03` shot-list (lazy-on-demand). The rubric above is the default; reused locations (E8 office, E1 bedroom) get the fullest sets.

## 2.5 Three MANDATORY anchors per env (baku, locked 2026-06-21 — validated on E01 Kamar Herman)

Every environment prompt MUST carry all three:
1. **Owner social class** — explicit token in `scene` (e.g. `lower-middle-class urban Jakarta household`). Calibrates furnishing tier, exactly as a character `role` social class calibrates grooming (`lessons` b.120).
2. **Interior brand/merk — INTERNATIONAL, as register not logo.** Name international brands by quality-tier; the Jakarta/Javanese tokens localize them. Do NOT restrict to Indonesian brands — local brands render poorly and the model localizes nuance anyway (user-validated). Write as `<brand>-style register` + construction tokens; never demand a literal logo (anti-logo-melt, same principle as cup-size-as-fashion-register).
3. **Interior designer — INTERNATIONAL pair (Lapis 6), chosen by REGISTER not luxury.** `production_designer` (film realism) + `interior_designer`/`interior_design_style`. The model localizes nationality; it does NOT localize CLASS → pick naturalistic/lived-in anchors that compose with the owner's class, never ultra-luxury for a modest home.
4. **Wall art / decorative artwork = NAMED public-domain works by a famous artist** — never generic AI art (which renders differently every angle → consistency break across plates + keyframes). A named, heavily-reproduced work gives the model a strong prior → it renders the SAME recognizable image across all angles. Rules: (a) **public domain** (commercial sales tool — no copyright); (b) **strong model prior** (pick ubiquitous works, not obscure-but-locally-accurate ones — Raden Saleh is culturally apt but weak prior → inconsistent); (c) **class/culture-plausible as a framed print** (woodblock/print register, not a pretentious oil); (d) localized by the Jakarta tokens. **Default home pair:** Katsushika Hokusai — *"The Great Wave off Kanagawa"* (c.1831) + *"Fine Wind, Clear Morning (Red Fuji)"* (c.1831), from *Thirty-Six Views of Mount Fuji*, matching dark wood frames. Name the work titles + artist verbatim in `scene`.

**Tier table:**
| Owner class | Brand register (international) | Designer pair |
|---|---|---|
| Lower-middle (E1–E6 home, E14 warung) | `IKEA` + `flat-pack particleboard, laminate, ready-to-assemble` | Eugenio Caballero (Roma realism) + Ilse Crawford / Studioilse (warm human-centred, unpretentious) |
| Upper (E7 affluent neighbour element, premium spaces) | `Minotti` / `Roche Bobois` register | luxury anchor (e.g. Vincent Van Duysen / Kelly Hoppen) |
| Civic / commercial (E8 office, E11 balai, E12 school, E13 terminal, E9 kafe) | contract/institutional or hospitality register | Caballero realism + context-appropriate designer |

## 2.6 Prompt structure standard (locked 2026-06-22 — validated on E01 Kamar master)

Env plate prompts use this structure (refines the 6-layer base for empty-room consistency + to suppress model "creative" drift across derivative angles):

1. **`shot` block (nested) = the ONLY per-angle variable.** Group `composition, framing, angle, camera_position, camera_direction, camera, lighting, aspect_ratio` under one `shot` object. Derivatives (other angles) copy `mood/color_grade/style/scene/subject_anchor/crew` **verbatim** and rewrite ONLY `shot`. World + contents stay locked; only the camera moves. Add explicit `camera_position` + `camera_direction` so the angle is defined, not improvised.
2. **`supporting_objects` = nested sub-slots, not one fat list.** Each object/zone gets its own short keyed slot (`nightstand`, `chair`, `wardrobe`, `window_dressing`, `rug`, `openings`, `floor`, …), ≤~10 tokens each. Reason: t2i models ignore/summarize token-overloaded single fields (`prompt-rules` b.27/544, `lessons` expression-sub-object precedent). Discrete slots get full attention weight → objects cannot be summarized away.
3. **No `plate_id`, no character names.** Names of occupants are inert to a t2i model in an empty room and add tokens. The big context belongs in `scene` (e.g. `private bedroom of an urban middle-class married couple`). Traceability lives in the filename + per-env file, not the prompt.
4. **No religious / strong-identity label in `scene`.** A label like `devout Muslim household` is a keyword-leak (`lessons` b.51): it competes with `wall_art` and pulls in unrequested decor (validated — it forced calligraphy to reappear over the Hokusai instruction). Rely on **social class** + **concrete objects** (sarong, peci, mukena, prayer mat carry devotion as set-dressing; class carries furnishing tier) — never an identity label.
5. **Lighting phrased room-relative, not camera-relative.** `key from the curtained window wall` (fixed source) not `from camera-left` (rotates with the camera → room reads different per angle).
6. **Furniture = named branded lock-anchors.** Use exact manufacturer product + finish per `tokens-references/INTERIOR-DESIGN-REFERENCE.md §6` so the same piece reproduces the same form/tone across angles.
7. **Wall art = a SINGLE named public-domain work** (not a pair). One frame = one anchor; two frames multiply placement variables across angles. Home default: Hokusai *"The Great Wave off Kanagawa"* (strongest reproduction prior). Overrides the two-work pair in §2.5(d).

8. **Derivatives MUST carry an explicit `environment_reference` field (token form), not rely on the harness "see the attachment".** Analog to the character `identity_reference` (`lessons` b.62). Place it as the FIRST field of each derivative cell; value = token strings (NOT a sentence — `prompt-rules` b.119) naming the master file + match-tokens, e.g. `attached reference plate E01_kamar_master.png, same room, identical furniture, identical layout, identical materials, named artwork, faithful room match, new camera per shot block only`. The master plate itself has no `environment_reference` (first plate, no attachment).

**E01 Kamar master = LOCKED** (`environment-images/E01_kamar/E01_kamar_master.png`, 2026-06-22): single Hokusai Great Wave + branded furniture (MALM bed + MALM nightstand + INGOLF chair + PAX wardrobe + LILL curtains + PERSISK rug), neutral grade, lived-in family, A1-clean. Derivatives bed3q / wallart_reverse / nightstand to follow via the `shot`-only-rewrite method (upload master as reference + new `shot`).

## 3. House architectural anchor (E1–E6, shared)

`production_designer: Eugenio Caballero` · `production_design_style: Roma-style middle-class domestic realism, lived-in working-family interior, class-accurate dressing` **+** `interior_designer: Ilse Crawford` · `interior_design_style: warm human-centred tactile lived-in, unpretentious frugal materiality`. Material/palette gestalt: matte painted plaster walls, IKEA-style flat-pack laminate/particleboard furniture, plain woven textiles desaturated, modest fixtures, real lived-in surfaces — localized by Jakarta/Javanese tokens. Each room varies dressing/function but keeps this gestalt so the home reads as ONE house across SEQ1→SEQ6.

## 4. Environment registry (14 unique — locked 2026-06-21)

TAG = `E<NN>_<slug>`. Storage: `environment-images/E<NN>_<slug>/` (+ `_rejected/`), names `E<NN>_<slug>_<angle>.png` (e.g. `E01_kamar_master.png`).

| TAG | Environment | Used by shots | Reuse | Notes |
|---|---|---|---|---|
| E01_kamar | Kamar Herman | SEQ1-SC01 + SEQ6-SC03 | 2× | **Bookend — coda must match opener exactly** |
| E02_ruangkeluarga | Ruang keluarga | SEQ1-SC02 + SEQ6-SC02 | 2× | sholat + ngaji |
| E03_ruangbelajar | Ruang belajar (Andi) | SEQ2-SC03 | 1× | **✅ DONE 4/4** (2026-06-23) home room; Kajikazawa + Schleich T-Rex hero |
| E04_dapur | Dapur Ratna | SEQ3-SC01 | 1× | live-selling UMKM |
| E05_sudutkerja | Sudut kerja Ratna | SEQ3-SC02 | 1× | home work corner |
| E06_ruangmakan | Ruang makan | SEQ6-SC01 | 1× | family convergence |
| E07_gerbangwarung | Gerbang kompleks + warung Darto (EXT) | SEQ2-SC01 | 1× | exterior; pos satpam, paving, mango tree |
| E08_kantor | Kantor ekspor-impor | SEQ2-SC02 + SEQ3-SC03 + SEQ4-SC01 | **3×** | highest-ROI; fullest angle set |
| E09_kafe | Kafe | SEQ2-SC04 | 1× | Lisa |
| E10_ruangkreator | Ruang kreator dekat kampus | SEQ3-SC04 + SEQ4-SC02 | 2× | merged (coworking + masterclass); dressing variation |
| E11_balaiwarga | Balai warga | SEQ4-SC03 | 1× | koperasi/inklusi |
| E12_ekskul | Ruang ekskul sekolah | SEQ4-SC04 | 1× | edutainment anak |
| E13_terminal | Terminal TransJakarta | SEQ5-SC01 | 1× | large public space, densest inventory |
| E14_warung | Warung kelontong gang | SEQ5-SC02 | 1× | evening; distinct from E07 |

## 5. Workflow per environment

1. Read the location's `03` shot-list → list the camera setups → pick the scoped-angle plates (§2).
2. **Create the per-env file `E<NN>-<slug>.md`** (analog to `08-character-sheet/H-herman.md`): §1 room identity lock (the FIXED `mood/color_grade/style/scene/subject_anchor/crew` block) + §2 method + §3 plate matrix (full prompt per angle, zero placeholder) + §4 status manifest. This is the reusable home of every angle prompt — author prompts here, not only in chat. Master plate authored first (no reference-image); derivatives = §1 verbatim + rewrite ONLY the `shot` block (§2.6) + upload the master as reference-image. Preseden: `E01-kamar.md`.
3. User generates → review (geometry, dressing, continuity, neutral grade) → approve → rename to `E<NN>_<slug>_<angle>.png` → update the per-env file's §4 manifest.
4. Plates become Kling reference-lock + the `scene`/`scene_depth` anchor cited by GATE B keyframe prompts of that location.

## 6. Usage contract

- GATE 0-ENV **precedes keyframe rollout** for a location (build the room once, reuse across all its shots).
- A keyframe prompt for a location cites its approved env plate(s) as reference + keeps `scene`/`scene_depth` consistent with them.
- Does NOT alter GATE 0 character plates; warmth + practicals + any graphic stay at keyframe / post.

---

*GATE 0-ENV method v1.0 · Explainer Video 2 · 2026-06-21 · governance `00-WORKLOG.md` (ADDENDUM A1) · companion `08-character-sheet/00-README.md`*
