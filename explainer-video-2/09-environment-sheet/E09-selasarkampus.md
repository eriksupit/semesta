---
title: Environment Sheet — E09 Selasar Kampus (EXT) · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e09-selasarkampus, gate-0-env, exterior]
status: fase2-prompt-locked
created: 2026-06-30
updated: 2026-07-01
aliases: [ev2-e09-selasarkampus, E09-selasarkampus, selasar-kampus-env]
---

# Environment Sheet — E09 SELASAR KAMPUS (EXT) · tag E09
> Method/anchor → [[00-README-ENV]] (§2.6). Scene truth → [[03-scene-detail]] SEQ2-SC07 (10.00) **+ SEQ3-SC09** (13.00). Shotlists → `10-gateB-keyframes/SEQ2-SC07.md` + `SEQ3-SC09.md`.
> **Room (EXT):** a shaded covered campus walkway (selasar) with a public bench — where the app brings real connection (SC07 peer-mentor) + service access (SC09 telemedicine). **Used 2×** (SC07 morning, SC09 midday); the `bangku2` cell is a deliberately distinct vantage so SC09 does not read as a twin of SC07. Empty-EXT reference plates, neutral grade; figures (Lisa/mentor/ibu) + warm grade added at GATE B.

> **EXTERIOR — declared anchor deviation:** no IKEA home furniture, no Hokusai home wall-art. Register = a public / semi-institutional Indonesian campus. Anchor = `production_designer` **Eugenio Caballero** (realism). Discipline that holds: **empty-EXT** (zero figures), **neutral grade**, **scoped-angle**, token-per-token, positive-only, A1 (device screens OFF; the community-profile / doctor-schedule UI = After Effects).

> **Token discipline (locked):** comma-delimited clusters, no conjunction glue, zero negation, camera-relative direction. **Fase-2 status:** prompts LOCKED, **generate PENDING (sesi baru)**.

---

## 1. Scene identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E09 angle)
This block stays identical across ALL E09 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E09_selasarkampus_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm empty walkway stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "modern university covered walkway, contemporary campus colonnade, clean white columns, large-format stone floor, landscaped green courtyard, glass academic building, vertical garden green wall, planters, bright well-maintained Indonesian university, calm public space",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "quiet bright modern campus calm",
  "subject_anchor": {
    "primary_subject": "modern covered campus walkway, contemporary roofed colonnade, row of clean white square columns camera-LEFT, large-format polished stone floor receding, two contemporary benches along the inner wall camera-RIGHT, landscaped green courtyard, glass academic building beyond the columns",
    "subject_material": "clean white rendered columns, large-format grey stone floor, smooth painted wall light clean tone, powder-coated steel and timber benches, glass curtain-wall building, well-maintained modern campus surfaces",
    "supporting_objects": {
      "bench_one": "contemporary bench, slatted timber seat, sleek powder-coated steel frame, against the inner wall camera-RIGHT, foreground",
      "bench_two": "second contemporary bench, slatted timber seat, powder-coated steel frame, against the inner wall camera-RIGHT, further down the walkway, a slim side planter beside it",
      "columns": "row of clean white square rendered columns, camera-LEFT, open colonnade side, flat roof soffit above",
      "info_display": "modern wall-mounted digital information display, inner wall camera-RIGHT, behind the first bench, screen off dark neutral, slim bezel",
      "wayfinding_totem": "modern freestanding wayfinding totem, slim vertical directional sign pillar, blank faces, brushed metal, camera-RIGHT edge near the walkway",
      "green_wall": "vertical garden green wall panel, lush foliage, on a wall section camera-RIGHT background",
      "wall": "smooth painted campus wall, camera-RIGHT, light clean tone",
      "courtyard": "landscaped green campus courtyard, manicured garden, modern glass academic building, beyond the columns camera-LEFT background",
      "planter_boxes": "row of large modern planter boxes with leafy ornamental trees, along the colonnade base camera-LEFT",
      "bollard_lamps": "row of sleek modern bollard garden lamps, low, along the colonnade edge camera-LEFT, switched off",
      "recycling_station": "modern paired recycling and waste bins station, slim, camera-RIGHT beside the first bench",
      "ceiling": "clean flat walkway soffit, recessed downlights switched off",
      "floor": "large-format polished grey stone floor, clean, receding down the walkway"
    },
    "human_absence_signal": "unoccupied, still, benches empty, walkway clear, courtyard quiet, empty"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian public campus exterior realism, semi-institutional, class-accurate, lived-in"
}
```
**Canonical layout (defined by master, directions FROM THE MASTER CAMERA's POV, camera along the walkway):** a modern roofed colonnade — a row of clean white square columns on the camera-LEFT (open side, a landscaped courtyard + a modern glass academic building beyond the columns), planter boxes with ornamental trees + low bollard lamps along the colonnade base camera-LEFT · the smooth painted inner wall on the camera-RIGHT carrying a wall-mounted digital display (OFF) + a vertical-garden green wall, TWO contemporary timber-and-steel benches against the inner wall camera-RIGHT (first bench foreground + a recycling station beside it, second bench further down with a side planter), a slim brushed-metal wayfinding totem near the camera-RIGHT edge, large-format polished stone floor receding down the walkway. **The benches are the seating focus (SC07 + SC09); perimeter = white columns + planters camera-left, inner wall + green wall + display camera-right; the walkway runs clear into the background.**

**ADDENDUM A1:** NO device in the empty plate — Lisa's phone arrives with her at GATE B. When it appears, the screen renders OFF/neutral and all UI (SC07 community peer-mentor profile card, SC09 doctor-schedule flow) is composited in After Effects. The wall-mounted digital display + the wayfinding totem render OFF / blank in the plate (all content = AE). No figures in the plate.

---

## 2. Method (per [[00-README-ENV]] §2.6 + EXT deviation)
- **Master generated first, no reference-image.** BGK + BGK2 derivatives upload `E09_selasarkampus_master.png` as reference + rewrite ONLY the `shot` block → same walkway, new camera. (Generate = separate session; at authoring time the derivative only carries the `environment_reference` token.)
- **EXT anchor deviation declared:** no IKEA, no Hokusai. Caballero realism + concrete enumerated campus elements (colonnade columns, timber-slat bench, notice board, terrazzo floor, courtyard) — each a strong real-world type, named for consistency across angles.
- **`bangku2` is a deliberately distinct vantage** (wider, more colonnade depth + courtyard, bench at frame edge) so SC09 does NOT read as a twin of SC07's tight bench MS — the same bench + layout, a clearly different composition.
- **Empty-EXT, neutral grade:** figures + warm/midday grade = GATE B.
- **No readable institution brands/logos** (brand-safe; generic campus identity).
- **Token-per-token values** — no conjunctions inside JSON token values (b.119); comma-delimited clusters only. Negation ban absolute.

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` SEQ2-SC07 + SEQ3-SC09 shot-lists)
Each cell is a COMPLETE copy-paste-ready prompt, zero scaffold. §1 is the canonical identity-lock. Scoped to E09's three plates: MASTER (establishing WIDE, serves SC07-SH01) · BGK (bench MS, serves SC07-SH03/04/05) · BGK2 (distinct wider bench vantage, serves SC09-SH01/02/04). BGK/BGK2 upload `E09_selasarkampus_master.png` as reference-image at generate time.

### Cell M — MASTER · establishing WIDE → `E09_selasarkampus_master.png` · ✅ GENERATED + ACCEPTED (2026-07-01, modern-enriched v3)
Full modern walkway geography — the anchor plate. Establishes the white colonnade + planter boxes/ornamental trees + bollard lamps camera-LEFT, two contemporary benches + digital display (OFF) + green wall + wayfinding totem + recycling station camera-RIGHT, glass academic building in the landscaped courtyard, walkway receding. **v1 (`9acaa285…`, dated) + v2 (`d3f12037…`, modern-but-sparse) both rejected → v3 modern + object-enriched per Erik-validated set (bollard lamps · planter boxes+trees · green wall · wayfinding totem · 2nd bench+side planter · recycling station). Token-dignity applied (see lessons 2026-07-01). Full-prompt regen.**
```json
{
  "mood": "neutral reference clarity, calm empty walkway stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "modern university covered walkway, contemporary campus colonnade, clean white columns, large-format stone floor, landscaped green courtyard, glass academic building, vertical garden green wall, planters, bright well-maintained Indonesian university, calm public space",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "quiet bright modern campus calm",
  "subject_anchor": {
    "primary_subject": "modern covered campus walkway, contemporary roofed colonnade, row of clean white square columns camera-LEFT, large-format polished stone floor receding, two contemporary benches along the inner wall camera-RIGHT, landscaped green courtyard, glass academic building beyond the columns",
    "subject_material": "clean white rendered columns, large-format grey stone floor, smooth painted wall light clean tone, powder-coated steel and timber benches, glass curtain-wall building, well-maintained modern campus surfaces",
    "supporting_objects": {
      "bench_one": "contemporary bench, slatted timber seat, sleek powder-coated steel frame, against the inner wall camera-RIGHT, foreground",
      "bench_two": "second contemporary bench, slatted timber seat, powder-coated steel frame, against the inner wall camera-RIGHT, further down the walkway, a slim side planter beside it",
      "columns": "row of clean white square rendered columns, camera-LEFT, open colonnade side, flat roof soffit above",
      "info_display": "modern wall-mounted digital information display, inner wall camera-RIGHT, behind the first bench, screen off dark neutral, slim bezel",
      "wayfinding_totem": "modern freestanding wayfinding totem, slim vertical directional sign pillar, blank faces, brushed metal, camera-RIGHT edge near the walkway",
      "green_wall": "vertical garden green wall panel, lush foliage, on a wall section camera-RIGHT background",
      "wall": "smooth painted campus wall, camera-RIGHT, light clean tone",
      "courtyard": "landscaped green campus courtyard, manicured garden, modern glass academic building, beyond the columns camera-LEFT background",
      "planter_boxes": "row of large modern planter boxes with leafy ornamental trees, along the colonnade base camera-LEFT",
      "bollard_lamps": "row of sleek modern bollard garden lamps, low, along the colonnade edge camera-LEFT, switched off",
      "recycling_station": "modern paired recycling and waste bins station, slim, camera-RIGHT beside the first bench",
      "ceiling": "clean flat walkway soffit, recessed downlights switched off",
      "floor": "large-format polished grey stone floor, clean, receding down the walkway"
    },
    "human_absence_signal": "unoccupied, still, benches empty, walkway clear, courtyard quiet, empty"
  },
  "shot": {
    "composition": "full modern covered-walkway geography, one frame, contemporary roofed colonnade, row of clean white columns camera-LEFT, planter boxes with ornamental trees and bollard lamps along the colonnade base camera-LEFT, large-format stone floor receding, two contemporary benches along the inner wall camera-RIGHT, digital information display screen off and wayfinding totem and green wall camera-RIGHT, recycling station beside the first bench, landscaped courtyard with a glass academic building beyond the columns camera-LEFT, legible",
    "framing": "WS establishing, walkway receding to background, roof soffit visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "at one end of the covered walkway, looking down the colonnade, open courtyard side camera-left, inner wall side camera-right",
    "camera_direction": "down the walkway, columns and planters camera-left, benches against the inner wall camera-right, courtyard beyond",
    "camera": "28mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, bright diffused key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian public campus exterior realism, semi-institutional, class-accurate, lived-in"
}
```

### Cell BGK — BENCH MS → `E09_selasarkampus_bangku.png` · ✅ prompt LOCKED · generate PENDING (modern-enriched v3)
Serves SEQ2-SC07-SH03/04/05 (Lisa + mentor at the bench, 50mm/35mm). The first contemporary bench at seated height, the inner wall + green wall + digital display (OFF) behind, the focal mid-ground.
```json
{
  "environment_reference": "attached reference plate E09_selasarkampus_master.png, same modern covered campus walkway, identical white colonnade, identical contemporary bench, identical green wall, identical digital display, identical layout, identical materials, faithful walkway match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty walkway stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "modern university covered walkway, contemporary campus colonnade, clean white columns, large-format stone floor, landscaped green courtyard, glass academic building, vertical garden green wall, planters, bright well-maintained Indonesian university, calm public space",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "quiet bright modern campus calm",
  "subject_anchor": {
    "primary_subject": "contemporary bench, slatted timber seat, powder-coated steel frame, against the inner wall camera-RIGHT, wall-mounted digital display screen off behind, vertical garden green wall behind, a clean white column camera-LEFT edge",
    "subject_material": "clean white rendered columns, large-format grey stone floor, smooth painted wall light clean tone, powder-coated steel and timber bench, well-maintained modern campus surfaces",
    "supporting_objects": {
      "info_display": "modern wall-mounted digital information display, inner wall behind the bench, screen off dark neutral, slim bezel",
      "green_wall": "vertical garden green wall panel, lush foliage, inner wall behind the bench",
      "wall": "smooth painted campus wall, behind the bench, light clean tone",
      "column": "a clean white square column, camera-LEFT edge, flat roof soffit above",
      "courtyard": "landscaped green campus courtyard, faint, beyond the column camera-LEFT background",
      "recycling_station": "modern paired recycling and waste bins station, slim, beside the bench",
      "floor": "large-format polished grey stone floor, clean"
    },
    "human_absence_signal": "unoccupied, still, bench empty, walkway clear, quiet"
  },
  "shot": {
    "composition": "medium framing on the contemporary bench, slatted timber-and-steel bench, against the inner wall camera-RIGHT, digital display screen off and green wall behind, dominant centre, a clean white column camera-LEFT edge, compressed walkway",
    "framing": "MS, bench fills frame, seated height, walkway compressed behind",
    "angle": "eye-level, seated height",
    "camera_position": "across the walkway from the open colonnade side, facing the bench against the inner wall, pushed in from establishing wide",
    "camera_direction": "toward the bench, the inner wall, digital display and green wall behind, white column camera-left edge",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, bright diffused key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian public campus exterior realism, semi-institutional, class-accurate, lived-in"
}
```

### Cell BGK2 — DISTINCT BENCH VANTAGE → ⛔ **DROPPED (2026-07-01)** · SC09 uses master + bangku as env-refs
**DROPPED (reference-dominance, same-axis re-vantage).** BGK2 tried to differentiate via a nudge on the SAME axis (28mm→35mm, "further down the walkway"); the render (`4fd98284…`, in `_rejected/`) came back ≈ the master, only marginally tighter. Same failure mode as **E07 GTE** and **E06 MEJA** — a distinct plate needs a genuinely different ANGLE, not a same-axis zoom/shift. **SC09 (ibu + Lisa telemedicine) therefore attaches `E09_selasarkampus_master.png` (wides) + `E09_selasarkampus_bangku.png` (bench mediums); its distinctness from SC07 is created at the GATE-B keyframe — different subjects, midday grade vs morning, different framing — not chased as a separate plate.** Prompt below retained for reference only (do NOT generate).
```json
{
  "environment_reference": "attached reference plate E09_selasarkampus_master.png, same modern covered campus walkway, identical white colonnade, identical contemporary benches, identical green wall, identical layout, identical materials, faithful walkway match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty walkway stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "modern university covered walkway, contemporary campus colonnade, clean white columns, large-format stone floor, landscaped green courtyard, glass academic building, vertical garden green wall, planters, bright well-maintained Indonesian university, calm public space",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "quiet bright modern campus calm",
  "subject_anchor": {
    "primary_subject": "modern covered campus walkway vantage, contemporary benches at the camera-RIGHT against the inner wall, row of clean white square columns camera-LEFT, planter boxes with ornamental trees along the colonnade base camera-LEFT, landscaped green courtyard beyond the columns camera-LEFT, large-format stone floor leading down the walkway",
    "subject_material": "clean white rendered columns, large-format grey stone floor, smooth painted wall light clean tone, powder-coated steel and timber benches, glass curtain-wall building, well-maintained modern campus surfaces",
    "supporting_objects": {
      "benches": "two contemporary benches, slatted timber seats, powder-coated steel frames, camera-RIGHT against the inner wall",
      "columns": "row of clean white square columns, camera-LEFT, open colonnade side, flat roof soffit above",
      "info_display": "modern wall-mounted digital information display, inner wall camera-RIGHT, screen off dark neutral",
      "green_wall": "vertical garden green wall panel, lush foliage, inner wall camera-RIGHT background",
      "courtyard": "landscaped green campus courtyard, manicured garden, modern glass academic building, beyond the columns camera-LEFT background",
      "planter_boxes": "row of large modern planter boxes with leafy ornamental trees, along the colonnade base camera-LEFT",
      "bollard_lamps": "row of sleek modern bollard garden lamps, low, along the colonnade edge camera-LEFT, switched off",
      "floor": "large-format polished grey stone floor, clean, leading down the walkway"
    },
    "human_absence_signal": "unoccupied, still, benches empty, walkway clear, courtyard quiet, empty"
  },
  "shot": {
    "composition": "medium-wide framing further down the walkway, the contemporary benches at the camera-RIGHT against the inner wall, digital display and green wall behind, more colonnade depth, clean white columns and planter boxes camera-LEFT, landscaped courtyard beyond the columns camera-LEFT, large-format stone floor leading in, wider vantage distinct from the tight bench plate",
    "framing": "MWS, benches camera-RIGHT, walkway depth visible, courtyard camera-LEFT, eye-level",
    "angle": "eye-level",
    "camera_position": "further down the walkway from the establishing wide, the benches at the camera-RIGHT against the inner wall, the open colonnade along camera-LEFT, distinct wider vantage from the BGK plate",
    "camera_direction": "along the walkway, benches camera-right, columns and planters camera-left, courtyard beyond",
    "camera": "35mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, bright diffused key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian public campus exterior realism, semi-institutional, class-accurate, lived-in"
}
```

---

## 4. Status manifest
| Cell | Angle | File | Serves | Status |
|---|---|---|---|---|
| M | establishing WIDE | `E09_selasarkampus_master.png` | SC07-SH01 | ✅ **GENERATED + ACCEPTED (2026-07-01, modern-enriched v3)** |
| BGK | bench MS | `E09_selasarkampus_bangku.png` | SC07-SH03/04/05 | ✅ **GENERATED + ACCEPTED (2026-07-01, modern-enriched v3)** |
| BGK2 | distinct bench vantage | ~~`E09_selasarkampus_bangku2.png`~~ | SC09-SH01/02/04 | ⛔ **DROPPED** — SC09 uses master + bangku (reference-dominance, same-axis re-vantage; cf. GTE, E06 MEJA) |

**E09 COMPLETE (2 plates: M + BGK).** BGK2 dropped — SC09 attaches `E09_selasarkampus_master.png` + `E09_selasarkampus_bangku.png`; distinctness at keyframe.

Storage: `environment-images/E09_selasarkampus/` (+ `_rejected/`). Naming: `E09_selasarkampus_<angle>.png`.
Generate M first (no reference-image). Then BGK / BGK2 via the `shot`-only-rewrite method: upload `E09_selasarkampus_master.png` as reference + paste §1 verbatim + the cell's `shot` block. BGK2 is intentionally a wider, distinct vantage from BGK (avoid twin shots). Empty-EXT (no figures, no device in plate); figures + UI + warm/midday grade = GATE B / After Effects.

---

*E09 Selasar Kampus environment sheet — Fase-2 prompts LOCKED (generate PENDING, sesi baru) · Explainer Video 2 · 2026-07-01 · EXTERIOR (declared anchor deviation; repurposed slot E09 from the cut kafe) · used 2× (SC07 + SC09, bangku2 distinct vantage) · token-per-token · camera-relative direction.*
