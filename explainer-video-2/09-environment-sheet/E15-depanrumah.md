---
title: Environment Sheet — E15 Depan Rumah Ratna (EXT) · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e15-depanrumah, gate-0-env, exterior]
status: fase2-prompt-locked
created: 2026-06-30
updated: 2026-07-01
aliases: [ev2-e15-depanrumah, E15-depanrumah, depan-rumah-ratna-env]
---

# Environment Sheet — E15 DEPAN RUMAH RATNA (EXT) · tag E15
> Method/anchor → [[00-README-ENV]] (§2.6). Scene truth → [[03-scene-detail]] SEQ2-SC04. Shotlist → `10-gateB-keyframes/SEQ2-SC04.md`.
> **Room (EXT):** the front yard + porch of a middle-class Indonesian house in the morning, with an **open front door** revealing a glimpse of the kitchen inside (the stacked frozen-food boxes of Ratna's business). The UMKM logistics pickup point (SC04). 1× use. **Same house as E01/E02/E03** — this is the exterior front of the same family home, so it inherits the architecture + material gestalt (matte plaster, simple desaturated materials). Empty-EXT reference plates, neutral grade; figures (Ratna hijab, 2 couriers) + the box van + warm grade = GATE B.

> **EXTERIOR — declared anchor deviation:** no IKEA home furniture, no Hokusai home wall-art. Register = realism of a middle-class Indonesian house. Anchor = `production_designer` **Eugenio Caballero** (Roma realism). Discipline that holds: **empty-EXT** (zero figures + zero vehicles in the plate), **neutral grade**, **scoped-angle**, token-per-token, positive-only.
> **Box-van decision (Fase-2):** the courier box van is NOT baked into the plate — it is a figure-action element staged with the couriers at GATE B (keeps the plate clean + reusable, like E07's empty forecourt). The master shows a CLEAR paved parking space where the van parks.

> **Token discipline (locked):** comma-delimited clusters, no conjunction glue, zero negation, camera-relative direction. **Fase-2 status:** prompts LOCKED, **generate PENDING (sesi baru)**.

---

## 1. Scene identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E15 angle)
This block stays identical across ALL E15 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E15_depanrumah_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm empty yard stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "middle-class house front yard, Indonesian residential home exterior, morning, matte plaster facade, open wooden front door, clay-tile roof, paved yard, low boundary fence, lived-in working-family",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in yard calm",
  "subject_anchor": {
    "primary_subject": "middle-class house front facade, matte plaster wall, simple barred window, open wooden front door, clay-tile roof, camera centre, paved front yard, clear open parking space, low boundary fence",
    "subject_material": "matte plaster facade muted off-white, clay-tile roof, weathered wood door, grey paving, real lived-in house surfaces",
    "supporting_objects": {
      "door": "open wooden front door, centre facade, a glimpse of the kitchen interior beyond, metal storage rack, stacked plain-labelled cardboard frozen-food boxes, shadier interior",
      "facade": "matte plaster house facade, simple barred window, small porch step, plain house-number plate beside the door",
      "fence": "low boundary fence, small gate, camera-RIGHT, potted plants along the base",
      "yard": "paved front yard, grey paving, clear open parking space, foreground",
      "doormat": "plain doormat, plain sandals, at the door step",
      "plants": "potted leafy plants, on the porch, beside the door",
      "pole": "plain utility pole, power cabling, camera-LEFT edge",
      "floor": "grey paving yard, thin grass strip along the edges"
    },
    "human_absence_signal": "unoccupied, still, door open, yard clear, parking space empty, quiet"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class house exterior realism, same family home, class-accurate, lived-in"
}
```
**Canonical layout (defined by master, directions FROM THE MASTER CAMERA's POV, camera from the street facing the house):** the middle-class house facade at centre-back (matte plaster wall, barred window, OPEN wooden front door — through it a glimpse of the kitchen interior: a metal storage rack + stacked plain-labelled cardboard frozen-food boxes, shadier than outside) · a paved front yard with a CLEAR open parking space in the foreground (the box van parks here at GATE B) · a low boundary fence + small gate camera-RIGHT with potted plants, a utility pole camera-LEFT, a doormat + sandals + potted plants on the porch step. **Perimeter framed by the facade + fence; the front yard stays open for the van + courier crew at GATE B.**

**ADDENDUM A1:** NO device in the empty plate — Ratna's tablet arrives with her at GATE B; its screen renders OFF/neutral, the order-list UI ("Dijemput" / "Pembayaran diterima") = After Effects. No vehicles in the plate (the box van = GATE B). Any house signage / box labels render plain (text = AE).

---

## 2. Method (per [[00-README-ENV]] §2.6 + EXT deviation)
- **Master generated first, no reference-image.** PTU derivative uploads `E15_depanrumah_master.png` as reference + rewrites ONLY the `shot` block → same house front, new camera. (Generate = separate session; at authoring time the derivative only carries the `environment_reference` token.)
- **Same house as E01/E02/E03** (exterior) — matte plaster facade, simple desaturated materials, class-accurate. The open-door kitchen glimpse ties to Ratna's UMKM (full kitchen = E04, not needed here; SC04 only needs the background glimpse via the door).
- **EXT anchor deviation declared:** no IKEA, no Hokusai. Caballero realism + concrete enumerated house/yard elements.
- **Empty-EXT, neutral grade, no vehicles:** figures + box van + warm-morning grade = GATE B.
- **No readable brands** (van = plain unbranded at GATE B; box labels = AE).
- **Token-per-token values** — no conjunctions inside JSON token values (b.119); comma-delimited clusters only. Negation ban absolute.

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` SEQ2-SC04 shot-list)
Each cell is a COMPLETE copy-paste-ready prompt, zero scaffold. §1 is the canonical identity-lock. Scoped to E15's two plates: MASTER (establishing WIDE, serves SH01/SH02/SH05) · PTU (doorway MS with kitchen glimpse, serves SH04). PTU uploads `E15_depanrumah_master.png` as reference-image at generate time.

### Cell M — MASTER · establishing WIDE → `E15_depanrumah_master.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Full front-of-house geography — the anchor plate. Establishes the facade + open door centre, fence camera-RIGHT, utility pole camera-LEFT, clear parking space foreground.
```json
{
  "mood": "neutral reference clarity, calm empty yard stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "middle-class house front yard, Indonesian residential home exterior, morning, matte plaster facade, open wooden front door, clay-tile roof, paved yard, low boundary fence, lived-in working-family",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in yard calm",
  "subject_anchor": {
    "primary_subject": "middle-class house front facade, matte plaster wall, simple barred window, open wooden front door, clay-tile roof, camera centre, paved front yard, clear open parking space, low boundary fence",
    "subject_material": "matte plaster facade muted off-white, clay-tile roof, weathered wood door, grey paving, real lived-in house surfaces",
    "supporting_objects": {
      "door": "open wooden front door, centre facade, a glimpse of the kitchen interior beyond, metal storage rack, stacked plain-labelled cardboard frozen-food boxes, shadier interior",
      "facade": "matte plaster house facade, simple barred window, small porch step, plain house-number plate beside the door",
      "fence": "low boundary fence, small gate, camera-RIGHT, potted plants along the base",
      "yard": "paved front yard, grey paving, clear open parking space, foreground",
      "doormat": "plain doormat, plain sandals, at the door step",
      "plants": "potted leafy plants, on the porch, beside the door",
      "pole": "plain utility pole, power cabling, camera-LEFT edge",
      "floor": "grey paving yard, thin grass strip along the edges"
    },
    "human_absence_signal": "unoccupied, still, door open, yard clear, parking space empty, quiet"
  },
  "shot": {
    "composition": "full front-of-house geography, one frame, middle-class house facade, open front door centre, kitchen glimpse beyond the door, paved front yard, clear parking space foreground, low boundary fence camera-RIGHT, potted plants, utility pole camera-LEFT, clay-tile roof, legible",
    "framing": "WS establishing, yard foreground, roofline visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "from the street side, facing the house front, fence side camera-right, utility-pole side camera-left",
    "camera_direction": "toward the house facade, open front door, kitchen glimpse beyond, paved yard foreground",
    "camera": "28mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, flat diffused key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class house exterior realism, same family home, class-accurate, lived-in"
}
```

### Cell PTU — DOORWAY MS (kitchen glimpse) → `E15_depanrumah_pintu.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Serves SEQ2-SC04-SH04 (Ratna at the threshold, the kitchen glimpse behind, 50mm). The open doorway at standing height, the kitchen glimpse (stacked frozen-food boxes) the shaded mid-ground.
```json
{
  "environment_reference": "attached reference plate E15_depanrumah_master.png, same house front, identical facade, identical open door, identical layout, identical materials, faithful house match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty yard stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "middle-class house front yard, Indonesian residential home exterior, morning, matte plaster facade, open wooden front door, clay-tile roof, paved yard, low boundary fence, lived-in working-family",
  "location": "outdoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in yard calm",
  "subject_anchor": {
    "primary_subject": "open wooden front door, doorway threshold, centre facade, a glimpse of the kitchen interior beyond, metal storage rack, stacked plain-labelled cardboard frozen-food boxes, shadier interior",
    "subject_material": "matte plaster facade muted off-white, weathered wood door, grey paving, real lived-in house surfaces",
    "supporting_objects": {
      "facade": "matte plaster house facade around the door, simple barred window camera-RIGHT, plain house-number plate beside the door",
      "kitchen_glimpse": "kitchen interior beyond the doorway, metal storage rack, stacked plain-labelled cardboard frozen-food boxes, a work table, shadier interior",
      "doormat": "plain doormat, plain sandals, at the door step",
      "plants": "potted leafy plants, on the porch, beside the door",
      "floor": "grey paving porch step, threshold"
    },
    "human_absence_signal": "unoccupied, still, door open, threshold clear, quiet"
  },
  "shot": {
    "composition": "medium framing on the open front doorway, weathered wood door, doorway threshold, dominant centre, a glimpse of the kitchen interior beyond, metal storage rack, stacked plain-labelled cardboard frozen-food boxes, shadier interior, plaster facade around the door",
    "framing": "MS, doorway fills frame, standing eye-level, interior glimpse behind",
    "angle": "eye-level, standing height",
    "camera_position": "in front of the open doorway, pushed in from establishing wide, standing eye-level",
    "camera_direction": "toward the open doorway, the kitchen glimpse beyond, stacked frozen-food boxes, shadier interior",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight outside, slightly shaded interior beyond the door, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian middle-class house exterior realism, same family home, class-accurate, lived-in"
}
```

---

## 4. Status manifest
| Cell | Angle | File | Serves | Status |
|---|---|---|---|---|
| M | establishing WIDE | `E15_depanrumah_master.png` | SC04-SH01/SH02/SH05 | ✅ prompt LOCKED · generate PENDING (sesi baru) |
| PTU | doorway MS (kitchen glimpse) | `E15_depanrumah_pintu.png` | SC04-SH04 | ✅ prompt LOCKED · generate PENDING (sesi baru) |

Storage: `environment-images/E15_depanrumah/` (+ `_rejected/`). Naming: `E15_depanrumah_<angle>.png`.
Generate M first (no reference-image). Then PTU via the `shot`-only-rewrite method: upload `E15_depanrumah_master.png` as reference + paste §1 verbatim + the cell's `shot` block. Empty-EXT (no figures, no van, no device in plate); figures + box van + tablet UI + warm-morning grade = GATE B / After Effects.

---

*E15 Depan Rumah Ratna environment sheet — Fase-2 prompts LOCKED (generate PENDING, sesi baru) · Explainer Video 2 · 2026-07-01 · EXTERIOR (declared anchor deviation; same family home as E01–E03; outside the original 14-inventory, new scene) · open-door kitchen glimpse · box van = GATE B (not baked) · token-per-token · camera-relative direction.*
