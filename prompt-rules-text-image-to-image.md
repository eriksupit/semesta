---
title: Prompting Rules — Text + Image-Reference → Image (Multi-Figure Scenes)
tags: [prompt-engineering, text-to-image, image-conditioning, autoregressive, multi-figure, keyframe, research]
status: active
created: 2026-06-25
updated: 2026-06-25
aliases: [text-image-to-image-rules, multi-figure-prompting, plate-state-law, reference-image-dominance, three-mode-grammar]
---

# Prompting Rules — Text + Image-Reference → Image (Multi-Figure Scenes)

A model-behavior reference for generating **multi-figure still images** with an **autoregressive, image-conditioned text-to-image** model (the GPT-Image class: one or more reference images are attached, a text prompt is supplied, a single new image is produced). It answers what the token-level prompting guides do not: **why attaching a reference image introduces drift, how to write the prompt differently depending on what the reference locks, how many figures one frame can carry, and how to keep a scene's start image and end image consistent — purely as images.**

> **Scope is image generation only.** No assumption is made about any downstream tool (animation, video, compositing). A "scene's start image and end image" here means two still images that must stay visually consistent, nothing more. Tools that consume these images have their own, different behavior and are out of scope.

## Scope & method

- **Model class:** autoregressive, image-conditioned generators that accept attached reference images alongside a text prompt and emit one image (GPT-Image-class). Findings are tagged **[general]** (expected to hold for any image-conditioned generator, e.g. Midjourney-class included) or **[class-specific]** (observed on this model class; may differ on diffusion models with separate text/image encoders).
- **Evidence basis:** controlled observation during a production case study (a multi-figure cinematic still-image sequence). Every rule states the **reproducible phenomenon** that produced it, described generically. Project-specific application and per-asset traces are maintained separately and are out of scope here.
- **Terminology:**
  - *plate / reference image* — an image attached to the prompt as a conditioning reference (an environment plate, a character/identity plate, a prior generated frame).
  - *identity anchor* — a plate that pins WHO and WHAT THINGS appear (a face/identity plate, an environment plate). It does **not** pin layout.
  - *composition anchor* — a prior **accepted generated image** that pins WHERE things sit (layout, framing, camera).
  - *face-locked figure* — a character whose identity is pinned by an attached identity plate.
  - *baked object* — an object already present in an attached plate's pixels.
  - *drift-wider* — the tendency of a figure-plus-environment-reference render to come out at a wider framing than the requested shot size.

---

## DIAGNOSIS — why attaching a reference introduces drift

The 6-layer JSON prompt produces consistent images **without** a reference. **With** a reference attached, drift appears: new objects, framing shift, misplaced subjects/objects, restructured content — so a scene's start and end images stop matching. The cause is **not** what it first looks like.

**Falsified hypothesis — token overflow.** A natural guess: the reference image is converted to text, merged with the prompt, the total exceeds the model's effective budget, and the model silently trims what it "deems" unnecessary. This is **wrong** on two counts. (1) Reference images are encoded as **image tokens**, not converted to text and merged into the prompt. (2) The decisive counter-evidence: **trimming the text prompt did not remove the drift.** If overflow were the cause, shortening the text would have measurably helped; it did not. Token pressure is real (image inputs are token-heavy) but it is not the failure mechanism.

**Actual causes — three, layered:**
1. **Generate = resample, not edit. [class-specific]** When a reference is attached and the model generates a NEW image, the reference is a **soft influence** and the composition is **re-sampled from scratch** — it is not locked. This is why two images from the same plates but different prompts come out with different layouts. The model class exposes distinct "generate" vs "edit" behaviors; only edit/anchor behavior preserves geometry. A neutral environment/identity plate does **not** make the model "edit" — it still resamples.
2. **Layout-imprecision. [general]** The model class's own published guidance acknowledges difficulty *placing elements precisely in structured or layout-sensitive compositions*. Misplacement is a documented model weakness, independent of token count.
3. **Reference-dominance + constraint-dilution. [general]** An attached image is a strong prior that competes with text; and the more simultaneous constraints a single frame carries (figures, objects, instructions), the lower the fidelity to each one.

These three causes — not overflow — are what the rules below are built to manage.

---

## PART I — REFERENCE-IMAGE BEHAVIOR (model laws)

### 1. PLATE-STATE LAW — an attached reference image is the floor of truth  [general]  🔒
Text can **add** subjects and poses, and **re-light**, within an attached plate. Text **cannot delete or override an object baked into the plate.**

- **Corollary (the dominant authoring trap):** never attach a plate that already contains an object whose **creation** is the prompt's action. If the action is "create / unroll / build / place object X," the plate must show **bare ground** (X absent); if the plate already shows X in place, the action must be dropped or reduced to a touch. Never both — doing both yields a **duplicate object**.
- **For state-change beats** (rolled→laid, off→on, closed→open): the plate must show the **post-action** state, OR you attach a **pre-action** plate (object absent) and let the text create it. The cut between two shots absorbs the state change; one frame never shows the transformation.
- **Reproducible phenomenon:** with an object baked laid-out in the plate, a prompt instructing "bare ground" did not remove it, and an action instructing the model to lay that object out produced a **second** copy on top. Inversely, an object given an action but **absent** from any attached plate was **hallucinated** onto an invented surface. Text alone neither reliably deletes nor reliably creates; the plate wins.
- **Status:** ✅ validated (both directions: duplicate-on-baked, hallucination-on-absent).

### 2. SUBJECT-COUNT CEILING — 1 face-locked, +1 only if softened  [general]
Per generated frame: **1 face-locked subject renders reliably one-shot.** A second figure is admissible **only as a soft / partial / near-background** presence — not a co-equal balanced two-shot. **Three or more text-summoned face-locked figures collapse** (positions swap, identities merge, floor objects drop).

- The apparent "two-character" success in practice resolves as **1 resolved + 1 softened**, so "2 co-equal face-locked" is **unproven** and must be treated as unsafe until demonstrated.
- **Reproducible phenomenon:** zero-subject and single-subject reference-conditioned renders converged one-shot; renders asked to carry 3–4 text-summoned face-locked figures repeatedly swapped figure positions and dropped floor objects across successive attempts. The reliable band measured is 0–1; the cliff sits between 1 and 3, with N=2-co-equal an untested gap.
- **Status:** ✅ validated (0–1 reliable, ≥3 collapse); ⚠️ N=2 co-equal is an untested gap.

### 3. COORDINATES PLACE, THEY DO NOT RAISE THE CEILING  [class-specific]
A canvas-pixel placement grammar — declare a reference canvas (e.g. 1920-wide), give each object a `center-x` within a central band with an edge margin, and a `center-y` as depth (nearer camera = larger y / lower in frame) — reliably **positions** objects.

- But coordinates were validated **placing inanimate objects on a zero-subject plate**, where the addressable units were objects, not rendered people. When face-locked **figures** were later added by text to the same scene, blocking still collapsed.
- **Therefore:** coordinates reliably place baked/prop anchors and position the ≤1–2 figures the model has **already agreed to draw**; they do **not** raise the subject-count ceiling of Rule 2. Coordinates are a placement instrument layered on top of the ceiling, never a substitute for it.
- **Status:** ✅ validated (placement on objects); the non-extension to figure-count is the corrective finding.

### 4. DRIFT-WIDER — figure + environment-reference renders wider than requested  [class-specific]
A figure rendered against an attached environment reference comes out at a **wider** framing than the requested shot size. Compensate by **specifying one stop tighter** than the visual target (ask for CU to land MCU; ask for MCU to land MS).
- **Status:** ✅ validated.

---

## PART II — THE THREE-MODE PROMPT GRAMMAR

The single most useful distinction for a reference-conditioned prompt is **what kind of anchor is attached**:

- An **identity anchor** (a face plate, an environment plate) locks **WHO** and **WHAT THINGS** — *not* WHERE. A neutral plate never locks layout (this is the root of start-image drift: a plate is mistaken for a composition lock).
- A **composition anchor** (a prior **accepted generated image**) locks **WHERE** — layout, framing, camera.

A frame may carry neither, identity-only, or both. That gives three prompting modes, and the prompt's shape differs in each.

### Governing principle — LOCKED or CHANGED, never re-described
In any reference-conditioned frame, every one of the 6 layers is either:
- **LOCKED** — already pinned by an anchor → **reference it, do NOT re-describe it.** Re-describing a locked layer in full prose invites the model to re-sample that layer and drift.
- **CHANGED** — genuinely different this frame → **describe only the delta.**

Never write a layer that is "locked but re-described in full." That single habit is the largest avoidable source of drift.

### The three modes

- **Mode A — From-scratch (no reference attached).** Full 6-layer prompt; composition comes entirely from text. This is the stable baseline the canonical 6-layer rules already cover.
- **Mode B — Identity-anchored (plates attached, NO composition anchor).** Plates lock faces/things; **layout is NOT locked**, so composition must still be fully specified in text (Lapis-2 world/space + Lapis-6 framing + coordinates). Lapis-3 verbose identity prose is trimmed (the plate locks the face) down to a minimal subject token + `identity_reference`. **This is the hardest mode and the main source of start-image drift** — because authors wrongly assume the plate locks layout.
- **Mode C — Composition-anchored (a prior accepted generated image is attached).** The anchor locks layout → **delta-only**: all locked layers are referenced ("match attached image exactly, change only:") and only the changed layer (normally Lapis-4, the event) is described. The END image of a scene is generated this way against the START image, which is what keeps the pair consistent.

### Per-layer map (what each mode does to each layer)

| Layer | Mode A (from-scratch) | Mode B (identity-anchored) | Mode C (composition-anchored) |
|---|---|---|---|
| L1 mood / color_grade / style | FULL | FULL | REFERENCE ("match attached image") |
| L2 scene / space / scene_depth | FULL | **FULL** (layout lives here — must be specified) | REFERENCE |
| L3 subject (identity) | FULL | TRIMMED → minimal token + `identity_reference` | REFERENCE → minimal token + `identity_reference` |
| L4 event / state | FULL | FULL | **DELTA** (the only full-detail layer) |
| L6 technical (framing/camera/lighting) | FULL | FULL (framing/camera from text) | REFERENCE (unless a technical value deliberately changes → DELTA) |

**Un-trimmable floor (all anchored modes, B and C):** the attachment reference lines (repeated per generate unit), the explicit attachment-pointer tokens, the per-figure subject tokens, the affirmative wardrobe spec, and **any object the Lapis-4 action touches must be named explicitly AND have its plate attached** (an anchor image alone does not let the model reliably handle an object given an action).

- **Status:** ✅ Mode A validated (stable baseline); ✅ Mode C validated for the END-anchors-START case; ⚠️ Mode B's "specify-layout-in-text-because-plate-does-not-lock-it" is the diagnosed fix, render-validation of the full per-layer map is PENDING.

### START / END pair — camera lock (the consistency guarantee)  🔒
A scene's START and END images form a pair where **only the subject changes, not the camera**.
- **Rule:** START and END must share **identical framing, angle, and camera position**. Between them, ONLY Lapis-4 (the subject's state / action / pose / expression) changes — so the viewer reads the subject as moving while the camera stays still. Generate the END in **Mode C** anchored on the accepted START image, with L6 (framing/camera) marked LOCKED → referenced, never re-described.
- **Camera move = explicit exception.** Any intended camera move (push-in, pan, tilt) makes L6 a **DELTA**, not a reference — which **forfeits the start/end consistency guarantee** and reintroduces drift risk. It must be a deliberate per-shot decision, never an accident of re-describing L6. If a move is wanted, treat the END as a near-fresh composition and expect to iterate.
- **Status:** ✅ validated (Mode C END-anchors-START); this is the headline statement of that mechanic.

### EDIT-IN-PLACE — the deterministic framing lock for small-delta pairs  🔒  ✅ validated 2026-06-26
When the generator exposes an **edit mode** that operates on a loaded image (a "describe edits" box that edits THIS image in place, optionally a single localizing point/comment + an input-fidelity control), produce the END by **editing the accepted START render in place** — NOT by generating a new image from the START as an attached reference. Edit-in-place rewrites only the targeted pixels, so framing / angle / camera / crop / lighting are preserved **by construction** (the *generate = resample* vs *edit = preserves geometry* split in the Diagnosis). This is the deterministic camera-lock; **generate-from-attachment (Mode C) is the fallback** when no edit mode exists.
- **Scope — small-delta only:** the END differs from the START by a contained subject change within the SAME framing (eyes closed→open, screen off→on, light shift, small expression/pose change). For **large-movement** beats (sit→stand, traverse) a small-region edit cannot hold the change → fall back to Rule 6a framing-by-union or decompose (Rule 8).
- **Instruction discipline:** the edit text is **token-per-token** (comma-separated discrete descriptors, no `and/with/but` glue — same SOP as the JSON prompt), stating ONLY the delta + an explicit lock list (`framing unchanged, crop unchanged, head position unchanged, lighting unchanged, skin unchanged, hair unchanged`). Set input-fidelity to its highest setting if offered. Keep the delta minimal — an over-long edit instruction reintroduces drift.
- **Reproducible phenomenon:** an END made by generate-from-attachment drifted framing across attempts (luck-dependent); the same END made by edit-in-place on the START render held framing pixel-faithfully first try, while a token-per-token groggy-eyes delta landed without narrowing the eyes (sleep-crust/redness tokens rendered weakly — acceptable).
- **Status:** ✅ validated first-use (SH01 pair, 2026-06-26); principled mechanism (edit preserves geometry), adopt as preferred for small-delta pairs.

---

## PART III — SHOT-DESIGN DISCIPLINE (decide before writing the prompt)

The highest-leverage move is upstream: design the shot list, figure count, and framing **first**, so each generated frame is intrinsically low-variance and need not be re-rendered. The looping failure mode is *author a high-variance frame, then patch tokens turn-by-turn*; these rules prevent it.

### 5. CROWD COVERAGE — shot-ladder + backs-of-figures
Cover a group (congregation, family, crowd) **across a shot ladder** — e.g. a lead figure's action in MS, the group from behind in a row, an over-shoulder — never in one frame carrying all faces + action + floor object at once.
- **Backs-of-figures are cheap on IDENTITY only.** A back-turned figure needs **no face-identity plate**. It still requires a subject token in the prompt, the environment plate, and an affirmative spec of its back-visible clothing (unspecified garments fill with a stereotyped default). "Free" means free of the *face plate*, nothing more.
- **Status:** ✅ validated (identity half — a row facing away from camera carries many figures safely).

### 6. FRAMING LADDER — multi-figure tightens; single-subject full-body is safe
- For **multi-figure** frames: default to **medium or tighter** (MS / CU / ECU). A full-body wide of multiple figures is the **gated** case.
- **Single-subject full-body is NOT gated** — it is routine and safe. The failure surface scales with figure **count**, not with full-body framing per se.
- A multi-figure full-body wide is permitted only when **all** of: (a) ≤1 face-locked figure (Rule 2) **or** the establishing exception (Rule 7); (b) the plate already carries the blocking; (c) the wide is **scene-developing** (builds spatial geometry no tighter shot can), not merely "show everyone."
- Always apply drift-wider compensation (Rule 4).
- **Status:** ✅ validated (single-subject full-body safe; multi-figure full-body = max failure surface).

### 6a. FRAMING-BY-UNION — a still camera must contain every subject state in the span  🔒
Decide framing at the **concept stage**, from the **union of all subject positions across START→END**, never from a single state. The camera is fixed; only the subject moves.
- **Procedure:** concept first → test whether ONE still framing can hold every state the subject passes through (start pose AND end pose). If yes, lock that framing for both frames.
- **If the beat moves the subject through space** (sit→stand, near→far): **widen the still frame** until it contains both extremes at once — e.g. a figure seated on the bed edge in START and standing in END must BOTH sit inside the same fixed frame. Never tilt / pan / track to follow the subject; a camera that follows is a camera move that forfeits the consistency guarantee (Part II start/end camera-lock).
- **If no single still frame can hold the union** (or holding it destroys the needed tightness): **split the beat into two shots** at a cut (Rule 8 decompose), each its own still-camera span.
- **Corollary:** framing is chosen by the **widest moment, not the first moment**. An ECU that fits START but crops out the END action is the wrong size — the union dictates the framing.
- **Status:** ✅ design rule (user-mandated 2026-06-26; corollary of the Part II start/end camera-lock).

### 7. STATIC MULTI-FIGURE ESTABLISHING EXCEPTION  ⚠️ PENDING
Some beats genuinely require 3–4 **named, face-locked** people in one frame and cannot be backs-only (a family convergence, a payoff group shot). Forbidding them outright would gut such scenes. Such a frame is permitted when **all four** hold:
- (a) it is the scene's **sole** beat requiring simultaneous face recognition;
- (b) figures are **STATIC** — seated/standing, no complex action (a static multi-figure frame carries far less generation variance than an action-laden one);
- (c) **each** figure carries its own identity plate + a **distinct** affirmative garment + a **position/colour anchor** (Rule 3 coordinates);
- (d) it is authored as **one** image (built, not generated in a single pass — see Rule 8).
- **Status:** ⚠️ PENDING — a designed hypothesis, not yet render-validated. Validate on first use; if 3–4 static face-locked still collapses, fall back to Rule 5 decomposition and record the result.

### 8. DECOMPOSE vs BUILD — minimize the consistency burden
Two ways to render a multi-figure scene carry very different consistency costs (image-only — no downstream tool assumed):
- **Decompose** into more separate shots → more *final* images that must each stay mutually consistent (same identities, palette, space across every image) → the continuity burden compounds with every added final image.
- **Build** one frame iteratively → many cheap authoring generations collapse to ONE final image; the intermediates are discarded, so nothing extra must be held consistent.
- **Rule:** prefer BUILD for a single establishing / convergence image; DECOMPOSE only at a genuine cut boundary, where visual continuity across the cut is not expected. Never decompose inside a continuity span (where one image must visually continue into the next) — that maximizes the number of images you must hold consistent at once.
- **Status:** ✅ design rule (image-continuity burden, not generation cost).

### 8a. ITERATIVE-BUILD method (how to build a multi-figure frame)  ⚠️ PENDING
To obtain a multi-figure frame without ever authoring a multi-figure frame in one pass:
- **Seed:** generate the establishing frame with **≤1 subject** (Mode B), composition stable per Rule 2, and accept it. This accepted image becomes the **composition anchor**.
- **Add:** add **one** figure per subsequent generation in **Mode C delta-only**, anchored on the freshly accepted image ("match attached image exactly, ADD one figure at `center-x/center-y`, change nothing else"). Per Rule 1, the already-present figures are baked into the anchor → they persist; the text only adds.
- **Result:** the final multi-figure image is **built**, not generated in one shot. This is the budget-free path to Rule 7's establishing exception (build adds cheap authoring generations, not extra final images — Rule 8).
- **Residual risk:** the model may slightly re-pose an earlier figure when adding a new one (a partial re-sample); minimized by Mode C minimal-change + the composition anchor. **Status:** ⚠️ PENDING — validate on first use.

---

## PART IV — TEXT DISCIPLINE

### 9. TEXT-ECONOMY = de-duplication hygiene, NOT a cause-fix  [general]
Trimming prose that merely restates an attached plate is **mechanical hygiene**, not a fix for multi-figure collapse. Do **not** over-credit it: text length is a *secondary* lever; the causes are reference-dominance (Rule 1) and subject-count (Rule 2). Over-trimming has a documented regression (a required object was dropped).
- **Un-trimmable floor (never cut):** the attachment reference lines (repeated per generate unit), the explicit attachment-pointer tokens, the per-figure subject tokens, and the affirmative wardrobe spec. Economy removes only cross-field/in-field **duplication** and filler.
- **Relationship to Mode C:** in a composition-anchored frame, trimming is not about budget — it is about **not re-describing a locked layer** (Part II governing principle). The reason to cut is anti-resample, not anti-overflow.
- **Status:** ✅ validated (correction of an earlier "efficiency" overclaim).

### 10. NO CLOCK-TIME — carry time-of-day through lighting, not a number  [general]
A clock time (`04.40`, `7am`) is **inert** to the model — it cannot render a numeral as a lighting condition. Stating it wastes tokens and conveys nothing. Carry time-of-day through the **lighting** layer (plus a coarse phase token in `time_of_day` such as `pre-dawn` / `dusk`) describing the actual light: direction, warmth/coolness, intensity, which source is or is not lit.
- **Reproducible precedent:** analog clock faces / clock-time were dropped from a room's plates because numerals and clock-hands render unreliably; the time-of-day (pre-dawn subuh) is read instead from a very-low-key cool-blue ambient with no warm sun risen and no lit practical lamp.
- **Pairs with the grade/lighting split:** the warm look stays in `color_grade`; the cool, dim pre-dawn condition lives in `lighting`.
- **Status:** ✅ validated (user-mandated 2026-06-26; clock-removal precedent).

### 11. TOKEN-PER-TOKEN IS MANDATORY ON EVERY PROMPT SURFACE — binding, not advisory  [general]  🔒
Every prompt the model authors MUST be **token-per-token**: comma-separated discrete descriptors, zero connective glue (`and / but / or / with / for / plus / bearing` → comma), keep only load-bearing prepositions (`of` + spatial `on/onto/from/to/into/over/against/above/below/toward`). This applies to **EVERY surface** — the 6-layer JSON **AND** the edit-mode "describe edits" instruction. The edit box being natural-language-friendly does **NOT** license prose; glued clauses risk under-weighting / dropping descriptors.
- **Redundant-pronoun ban:** drop any possessive/pronoun whose referent is already fixed — `male` already implies `his`, a single subject makes `his/her/its` informationless. State the attribute directly (`skin tone matched`, never `match his skin tone`).
- **Pre-emit self-check (mandatory):** before sending any prompt/edit text, scan for (a) a finite or infinitive verb chain inside a clause (`reaching in to grasp it`), (b) a pronoun (`his/her/its`), (c) a banned glue word. Any hit = prose → re-tokenize before emit.
- **Why this is a rule, not a tip:** it recurred twice in one session because it was treated as a stylistic suggestion; it is a HARD GATE. Elevated from advisory to binding.
- **Status:** ✅ mandated 2026-06-26 (user correction, recurred twice).

### 12. NO MOTION VERBS on a still frame  [general]  🔒
A still image freezes one instant; a motion verb (`entering`, `reaching`, `rising`, `lifting`, `walking`, `grabbing`) tells the model to depict movement → blur or an ambiguous half-position. Describe the **frozen state**: where the element IS + its static pose. State-participles (`curled`, `pressed`, `seated`, `settled`) are fine; motion-participles (`entering`, `reaching`) are not.
- **Reproducible phenomenon:** `hand entering from the bottom edge` rendered a hand splayed mid-motion, not a clean grip; `mature male hand, lower frame, fingertips curled over the left long side` describes the end-state directly.
- **Status:** ✅ validated 2026-06-26 (SH02-END).

### 13. GEOMETRY-EXPLICIT placement — map each contact to a named side, not a vague "part"  [general]  🔒
For any contact/placement, first lock the object's **orientation + axis** (`phone upright portrait, long axis vertical`), then map **each** contact to a SPECIFIC side/edge/region (`thumb on the right long side, four fingertips over the left long side`). A loose "part" token (`grip the edges`, `the long edges`) leaves the model to guess the geometry → it fails (a hand splays flat instead of gripping). Think in plane-space like a photo editor: position, side, dimension.
- **Reproducible phenomenon:** `fingers curling around the phone long edges` (vague, both sides, one hand) rendered a flat splay; `thumb on the right long side, fingertips over the left long side` pins a real cross-grip.
- **Status:** ✅ validated 2026-06-26 (SH02-END).

### 14. EDIT-IN-PLACE — lock baked elements with "<element> unchanged", never re-describe  [general]  🔒
In an edit-in-place operation the base image already contains its elements; re-describing one (`phone flat in place on the nightstand`) is redundant and competes with the edit (the model may re-draw / re-place it). State only the **delta** (the added element) + lock every baked element with `<element> unchanged` (`phone unchanged, nightstand unchanged, lamp unchanged, framing unchanged`). A lock token is stronger and less ambiguous than a fresh description.
- **Status:** ✅ validated 2026-06-26 (SH02-END).

---

## PART V — PROMPT STRUCTURE (templates)  ⚠️ LIVE / PROVISIONAL

> **Status: LIVE document — NOT locked.** This is the current best template, not yet hardened across many generation cases; it will evolve as real renders expose gaps. Treat every field choice as provisional. **Revision trigger:** any render where a correctly-authored prompt still drifts → diagnose which structural slot failed, amend the template here with a dated trace.

Built on the canonical 6-layer JSON (`../prompt-rules-image-generation.md`). Adds a mandatory ATTACHMENT MANIFEST header and renders the body differently per mode (Part II).

### ATTACHMENT MANIFEST — mandatory header for every reference-conditioned frame (Mode B & C)
Explicit list of each attached file + role + bind-token (operationalizes the triad-attachment + attachment-line rules). One `identity_reference` entry per face-locked person in frame; `composition_reference` only in Mode C.
```json
"attachment_manifest": {
  "environment_reference": "<E0X_room_orientation>.png — same room, identical materials, identical furniture, identical layout, new camera only",
  "identity_reference": [
    "<CHAR_view_shot>.png — same person, match face, match proportions"
  ],
  "composition_reference": "<sc0X_shY_start>.png — match exactly, identical framing, angle, camera, lighting, layout"
}
```

### Mode A — from-scratch (no attachment; full 6-layer)
No manifest; composition entirely from text. For an inanimate-environment plate, replace `character_identity`/`character_style` with `subject_anchor { primary_subject, subject_material, supporting_objects, human_absence_signal }`.
```json
{
  "mood": "<directorial tone token>",
  "color_grade": "<grade tokens, ONE temperature, zero colour-name>",
  "style": "<medium + lens + film-stock tokens>",
  "scene": "<interior/exterior style name — material tokens>",
  "location": "<indoor | outdoor | semi-outdoor>",
  "time_of_day": "<morning | afternoon | evening | night>",
  "atmosphere": "<spatial-energy token>",
  "scene_depth": { "foreground": "<0–2m from lens>", "midground": "<subject + immediate env>", "background": "<population + depth>" },
  "character_identity": { "role": "...", "ethnicity": "...", "beauty": "...", "age": "<single integer>", "facial_features": "<texture only, zero colour>", "body_features": "..." },
  "character_style": { "makeup": "<base + features + finish>", "wardrobe": "<fabric + construction + fit + colorway, EVERY visible garment>", "hair": "<barbering term + matte finish>", "footwear": "..." },
  "subject_state": "<static | dynamic | speaking>",
  "action": "<mid-process verb>",
  "pose": "<body description (+ canvas coordinates if needed)>",
  "gesture": "<physical only>",
  "expression": "<physical tokens, Duchenne if positive>",
  "framing": "<EWS…ECU — spec ONE stop tighter than target>",
  "angle": "<eye-level | low | high | dutch + composition>",
  "camera": "<NNmm prime spherical, DOF>",
  "lighting": "<source + quality, zero colour-name, zero negation>",
  "aspect_ratio": "<e.g. 16:9>",
  "director": "<name>", "directing_style": "...",
  "lighting_director": "<name>", "lighting_style": "...",
  "production_designer": "<name>", "production_design_style": "...",
  "interior_designer": "<name>", "interior_design_style": "...",
  "costume_designer": "<name>", "costume_style": "...",
  "makeup_artist": "<name>", "makeup_style": "..."
}
```

### Mode B — identity-anchored (plates attached, NO composition anchor)
MANIFEST (env + identity, no composition) + full 6-layer body with ONE change: **L3 collapses to a `subjects[]` array** (who + identity pointer + this-scene wardrobe — the plate locks the face, so no facial/body re-description). **Composition lives fully in `scene_depth` + framing/angle/camera + `pose` coordinates** because the plate does NOT lock layout.
```json
{
  "attachment_manifest": { "environment_reference": "...", "identity_reference": ["..."] },
  "mood": "...", "color_grade": "...", "style": "...",
  "scene": "...", "location": "...", "time_of_day": "...", "atmosphere": "...",
  "scene_depth": { "foreground": "...", "midground": "...", "background": "..." },
  "subjects": [
    { "who": "<name>", "identity_reference": "<file>.png", "wardrobe": "<this-scene garments, affirmative, every visible piece>" }
  ],
  "subject_state": "...", "action": "...", "pose": "<body + center-x/center-y coordinates>", "gesture": "...", "expression": "...",
  "framing": "<one stop tighter than target>", "angle": "...", "camera": "...", "lighting": "...", "aspect_ratio": "...",
  "director": "<name>", "directing_style": "...", "lighting_director": "<name>", "lighting_style": "...",
  "production_designer": "<name>", "production_design_style": "...", "interior_designer": "<name>", "interior_design_style": "...",
  "costume_designer": "<name>", "costume_style": "...", "makeup_artist": "<name>", "makeup_style": "..."
}
```

### Mode C — composition-anchored (a prior accepted render attached; minimal delta)
MANIFEST (env + identity + composition) + a SHORT delta block ONLY — locked layers (L1/L2/L6) are NOT re-written, because re-describing a locked layer invites resample (Part II governing principle).
```json
{
  "attachment_manifest": {
    "environment_reference": "...",
    "identity_reference": ["..."],
    "composition_reference": "<sc0X_shY_start>.png — match exactly, identical framing, angle, camera, lighting, layout"
  },
  "match_reference": "match composition_reference exactly — identical framing, angle, camera, lighting, layout; change ONLY the event below",
  "subjects": [ { "who": "<name>", "identity_reference": "<file>.png" } ],
  "change_only": { "subject_state": "...", "action": "...", "pose": "...", "gesture": "...", "expression": "..." },
  "touched_objects": [ { "object": "<name>", "reference": "<plate>.png", "change": "<what the action does to it>" } ]
}
```
Provisional encoding = minimal JSON (chosen over a prose sentence for skill-consistency + auditability). The `subjects[]` array form (vs suffixed `character_identity_husband/_wife`) is the multi-figure generalization — a live design choice.

- **Status:** ⚠️ PROVISIONAL — the three templates are the diagnosed-correct shapes; render-validation across cases pending, revision expected.

---

## ENFORCEMENT — a pre-emit gate (recording a rule ≠ applying it)

Documented rules fail when they are recorded but not checked before each generation. Run a **blocking pre-emit gate** for every frame, with the plate-state item firing **first**:

- **G0 — PLATE-STATE CHECK (blocking):** Does any action verb transform / create / place an object the attached plate already shows in its final state? If YES → STOP. Swap to a pre-action plate, or drop the verb. (Rule 1.)
- **G1 — Mode declared:** which mode is this frame (A / B / C)? Every layer is then marked LOCKED or CHANGED; no locked layer is re-described in full (Part II).
- **G2 — Reference completeness:** every figure/object/environment named in the prompt has a corresponding attached plate (face plate only where the figure shows a face — Rule 5); any object the action touches is named + plated.
- **G3 — Subject-count:** ≤1 face-locked figure (Rule 2), or the establishing exception (Rule 7) is explicitly invoked (built per Rule 8a).
- **G4 — Framing:** multi-figure defaults to medium-or-tighter (Rule 6) with drift-wider compensation (Rule 4).
- **G5 — Consistency burden:** prefer building one frame over decomposing into multiple final images that must stay mutually consistent (Rule 8).
- **G6 — Camera lock (start/end):** the END shares the START's framing/angle/camera (L6 LOCKED, referenced not re-described); any camera move is a declared L6-DELTA that forfeits the consistency guarantee (Part II).

A frame is **not ready** until G0–G6 pass. Run this before declaring readiness; do not wait for a reviewer to catch it.

---

## Validation ledger

| Rule | Status | Reproducible evidence |
|---|---|---|
| Diagnosis: drift = resample + layout-imprecision + dominance (not overflow) | ✅ validated | text-trim did not fix drift; published layout-imprecision note |
| 1 Plate-state law | ✅ validated | duplicate-on-baked + hallucination-on-absent |
| 2 Subject-count (0–1 reliable, ≥3 collapse) | ✅ validated | zero/single converge; 3–4 swap + drop |
| 2 (N=2 co-equal) | ⚠️ untested gap | observed only as 1 resolved + 1 softened |
| 3 Coordinates ≠ count ceiling | ✅ validated | placed objects on zero-subject plate; figures still collapsed |
| 4 Drift-wider | ✅ validated | figure + env-reference renders wider |
| Part II — 3-mode grammar (A/B/C, LOCKED-or-CHANGED) | ✅ A & C / ⚠️ B map | A stable; C = END-anchors-START; B full map PENDING |
| Part II — start/end camera lock | ✅ validated | Mode C END-anchors-START; camera move = L6-DELTA exception |
| Part II — edit-in-place END (small-delta pairs) | ✅ validated (first-use) | edit-on-START holds framing by construction; generate-from-attachment = fallback |
| 5 Backs-of-figures (identity-free) | ✅ validated | away-facing rows carry many figures |
| 6 Single-subject full-body safe / multi-figure gated | ✅ validated | single full-body accepted; multi full-body collapsed |
| 6a Framing-by-union (still camera holds all states) | ✅ design rule | user-mandated; corollary of camera-lock — widen or split, never follow |
| 7 Static establishing exception | ⚠️ PENDING | validate on first multi-figure establishing use |
| 8 Decompose vs build (consistency burden) | ✅ design rule | image-continuity burden |
| 8a Iterative-build (single-figure addition) | ⚠️ PENDING | validate on first build |
| 9 Text-economy = hygiene | ✅ validated | over-trim dropped a required object |
| 10 No clock-time (lighting carries time-of-day) | ✅ validated | clock numerals inert/unreliable; lighting + phase token carry it |
| 11 Token-per-token mandatory on every surface | ✅ mandated | binding (not advisory); applies to edit-box too; redundant-pronoun ban; pre-emit self-check |
| 12 No motion verbs on a still frame | ✅ validated | "entering" → splay mid-motion; describe frozen state |
| 13 Geometry-explicit placement (named sides) | ✅ validated | vague "long edges" → splay; map thumb/fingertips to specific sides |
| 14 Edit-in-place: lock baked elements, don't re-describe | ✅ validated | "phone flat in place" redundant/ambiguous → "phone unchanged" |
| Part V — prompt-structure templates (manifest + Mode A/B/C) | ⚠️ live / provisional | diagnosed shape; render-validation pending, evolves with cases |

## Changelog
- **2026-06-25** — Document created as a clean-slate, project-agnostic research reference (image generation only; no downstream/animation behavior assumed). Findings derived from a multi-figure cinematic still-image case study; project-specific traces maintained separately. Method decided via multi-agent brainstorm + three adversarial verification passes against direct render evidence.
- **2026-06-25** — Encoded the diagnosis (drift = resample-not-edit + layout-imprecision + reference-dominance; token-overflow falsified), the three-mode prompt grammar (identity-anchor vs composition-anchor; Mode A/B/C; LOCKED-or-CHANGED principle; per-layer map), and the decompose-vs-build + iterative-build method (Rule 8 / 8a).
- **2026-06-25** — Added the explicit START/END camera-lock rule (Part II): identical framing/angle/camera, only Lapis-4 changes; camera move = explicit L6-DELTA that forfeits the consistency guarantee. Added enforcement gate G6.
- **2026-06-25** — Added PART V — PROMPT STRUCTURE (templates), flagged **LIVE / PROVISIONAL**: ATTACHMENT MANIFEST header + Mode A (full 6-layer) / Mode B (full minus trimmed L3, composition in text) / Mode C (minimal delta JSON, locked layers not re-written). Explicitly a live document that evolves with generation cases; revision trigger defined.
- **2026-06-26** — Added Rule 6a FRAMING-BY-UNION (Part III): framing is decided at the concept stage from the union of all subject positions across START→END so one still camera contains every state; widen the frame rather than follow the subject, and split the beat into two shots if the union cannot fit. Camera never tracks/pans/tilts to follow — subject moves, camera still. User-mandated design principle, corollary of the Part II start/end camera-lock.
- **2026-06-26** — Added Rule 10 NO CLOCK-TIME (Part IV): a clock time is inert to the model; carry time-of-day through the lighting layer (plus a coarse phase token), never a numeral. Pairs with the warm-grade / cool-dim-lighting split. User-mandated; clock-removal precedent.
- **2026-06-26** — Adopted EDIT-IN-PLACE as the preferred deterministic camera-lock for small-delta start/end pairs (Part II): produce the END by editing the accepted START render in place (edit-mode "describe edits" + token-per-token delta + explicit `... unchanged` lock list + high input-fidelity), NOT by generate-from-attachment (now the fallback). Validated first-use on the SH01 pair; large-movement beats still follow Rule 6a framing-by-union / decompose.
- **2026-06-26** — Added Rule 11 TOKEN-PER-TOKEN MANDATORY ON EVERY SURFACE (Part IV), elevated from advisory to **binding** after the model twice reverted to prose (glue words + redundant `his` after `male`) in the edit-box instruction. Adds the redundant-pronoun ban + a mandatory pre-emit self-check (scan for verb-clauses / pronouns / glue before sending). Applies to the edit-mode "describe edits" text, not just the JSON.
- **2026-06-26** — Added Rules 12 (no motion verbs on a still — `entering/reaching/lifting` → frozen-state description), 13 (geometry-explicit placement — lock orientation+axis then map each contact to a named side, not a vague "part"; "Photoshop logic"), 14 (edit-in-place — lock baked elements with `<element> unchanged`, never re-describe). All three from the SH02-END hand-grip authoring corrections; general Rules 12–13 mirrored into the 6-layer canon `prompt-rules-image-generation.md`.
