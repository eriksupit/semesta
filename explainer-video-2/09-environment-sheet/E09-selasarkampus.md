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
  "scene": "covered campus walkway, shaded colonnade, public bench, painted concrete columns, terrazzo floor, leafy green courtyard, semi-institutional Indonesian campus, calm public space",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "quiet shaded campus calm",
  "subject_anchor": {
    "primary_subject": "covered campus walkway, roofed colonnade, row of painted concrete columns camera-LEFT, terrazzo floor receding, public bench along the inner wall camera-RIGHT, leafy green courtyard beyond the columns",
    "subject_material": "painted concrete columns, terrazzo floor, painted plaster campus wall, weathered timber-slat bench, real lived-in campus surfaces",
    "supporting_objects": {
      "bench": "public bench, weathered timber slats, painted steel frame, against the inner wall camera-RIGHT",
      "columns": "row of painted concrete columns, camera-LEFT, open colonnade side, roof beams above",
      "notice_board": "campus notice board, inner wall camera-RIGHT, behind the bench, plain pinned notices",
      "wall": "painted plaster campus wall, camera-RIGHT, muted tone",
      "courtyard": "leafy green campus courtyard, garden, faint lecture building, beyond the columns camera-LEFT background",
      "plants": "potted leafy plants, along the colonnade base, camera-LEFT",
      "bin": "plain campus rubbish bin, camera-RIGHT, beside the bench",
      "lamp": "plain walkway ceiling lamp, switched off",
      "floor": "clean terrazzo floor, receding down the walkway"
    },
    "human_absence_signal": "unoccupied, still, bench empty, walkway clear, courtyard quiet, empty"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian public campus exterior realism, semi-institutional, class-accurate, lived-in"
}
```
**Canonical layout (defined by master, directions FROM THE MASTER CAMERA's POV, camera along the walkway):** a roofed colonnade — a row of painted concrete columns on the camera-LEFT (open side, a leafy courtyard + faint lecture building visible beyond the columns), the painted plaster campus inner wall on the camera-RIGHT carrying a notice board, a weathered timber-slat public bench against the inner wall camera-RIGHT, potted plants along the colonnade base camera-LEFT, a rubbish bin beside the bench, terrazzo floor receding down the walkway. **The bench is the seating focus (SC07 + SC09); perimeter = columns camera-left + inner wall camera-right; the walkway runs into the background.**

**ADDENDUM A1:** NO device in the empty plate — Lisa's phone arrives with her at GATE B. When it appears, the screen renders OFF/neutral and all UI (SC07 community peer-mentor profile card, SC09 doctor-schedule flow) is composited in After Effects. Any campus signage / notice-board text renders as plain blank notes (text = AE). No figures in the plate.

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

### Cell M — MASTER · establishing WIDE → `E09_selasarkampus_master.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Full walkway geography — the anchor plate. Establishes the colonnade camera-LEFT, the bench against the inner wall camera-RIGHT, the courtyard beyond, the walkway receding.
```json
{
  "mood": "neutral reference clarity, calm empty walkway stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "covered campus walkway, shaded colonnade, public bench, painted concrete columns, terrazzo floor, leafy green courtyard, semi-institutional Indonesian campus, calm public space",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "quiet shaded campus calm",
  "subject_anchor": {
    "primary_subject": "covered campus walkway, roofed colonnade, row of painted concrete columns camera-LEFT, terrazzo floor receding, public bench along the inner wall camera-RIGHT, leafy green courtyard beyond the columns",
    "subject_material": "painted concrete columns, terrazzo floor, painted plaster campus wall, weathered timber-slat bench, real lived-in campus surfaces",
    "supporting_objects": {
      "bench": "public bench, weathered timber slats, painted steel frame, against the inner wall camera-RIGHT",
      "columns": "row of painted concrete columns, camera-LEFT, open colonnade side, roof beams above",
      "notice_board": "campus notice board, inner wall camera-RIGHT, behind the bench, plain pinned notices",
      "wall": "painted plaster campus wall, camera-RIGHT, muted tone",
      "courtyard": "leafy green campus courtyard, garden, faint lecture building, beyond the columns camera-LEFT background",
      "plants": "potted leafy plants, along the colonnade base, camera-LEFT",
      "bin": "plain campus rubbish bin, camera-RIGHT, beside the bench",
      "lamp": "plain walkway ceiling lamp, switched off",
      "floor": "clean terrazzo floor, receding down the walkway"
    },
    "human_absence_signal": "unoccupied, still, bench empty, walkway clear, courtyard quiet, empty"
  },
  "shot": {
    "composition": "full covered-walkway geography, one frame, roofed colonnade, row of concrete columns camera-LEFT, terrazzo floor receding, public bench along the inner wall camera-RIGHT, notice board behind the bench, leafy courtyard beyond the columns camera-LEFT, legible",
    "framing": "WS establishing, walkway receding to background, roof beams visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "at one end of the covered walkway, looking down the colonnade, open courtyard side camera-left, inner wall side camera-right",
    "camera_direction": "down the walkway, columns camera-left, bench against the inner wall camera-right, courtyard beyond",
    "camera": "28mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, shaded diffused key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian public campus exterior realism, semi-institutional, class-accurate, lived-in"
}
```

### Cell BGK — BENCH MS → `E09_selasarkampus_bangku.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Serves SEQ2-SC07-SH03/04/05 (Lisa + mentor at the bench, 50mm/35mm). The bench at seated height, the inner wall + notice board behind, the focal mid-ground.
```json
{
  "environment_reference": "attached reference plate E09_selasarkampus_master.png, same covered campus walkway, identical colonnade, identical bench, identical layout, identical materials, faithful walkway match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty walkway stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "covered campus walkway, shaded colonnade, public bench, painted concrete columns, terrazzo floor, leafy green courtyard, semi-institutional Indonesian campus, calm public space",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "quiet shaded campus calm",
  "subject_anchor": {
    "primary_subject": "public bench, weathered timber slats, painted steel frame, against the inner wall camera-RIGHT, campus notice board behind the bench, a concrete column camera-LEFT edge",
    "subject_material": "painted concrete columns, terrazzo floor, painted plaster campus wall, weathered timber-slat bench, real lived-in campus surfaces",
    "supporting_objects": {
      "notice_board": "campus notice board, inner wall behind the bench, plain pinned notices",
      "wall": "painted plaster campus wall, behind the bench, muted tone",
      "column": "a painted concrete column, camera-LEFT edge, roof beam above",
      "courtyard": "leafy green campus courtyard, faint, beyond the column camera-LEFT background",
      "bin": "plain campus rubbish bin, beside the bench",
      "floor": "clean terrazzo floor"
    },
    "human_absence_signal": "unoccupied, still, bench empty, walkway clear, quiet"
  },
  "shot": {
    "composition": "medium framing on the public bench, weathered timber-slat bench, against the inner wall camera-RIGHT, notice board behind, dominant centre, a concrete column camera-LEFT edge, compressed walkway",
    "framing": "MS, bench fills frame, seated height, walkway compressed behind",
    "angle": "eye-level, seated height",
    "camera_position": "across the walkway from the open colonnade side, facing the bench against the inner wall, pushed in from establishing wide",
    "camera_direction": "toward the bench, the inner wall, notice board behind, column camera-left edge",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, shaded diffused key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian public campus exterior realism, semi-institutional, class-accurate, lived-in"
}
```

### Cell BGK2 — DISTINCT BENCH VANTAGE → `E09_selasarkampus_bangku2.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Serves SEQ3-SC09-SH01/02/04 (midday; ibu + Lisa at the bench, 35mm/50mm). A deliberately WIDER, more colonnade-depth vantage with the bench at the camera-RIGHT, the columns + courtyard along camera-LEFT — clearly distinct from the BGK tight bench MS so SC09 is not a twin of SC07. Midday grade = GATE B.
```json
{
  "environment_reference": "attached reference plate E09_selasarkampus_master.png, same covered campus walkway, identical colonnade, identical bench, identical layout, identical materials, faithful walkway match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty walkway stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic exterior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "covered campus walkway, shaded colonnade, public bench, painted concrete columns, terrazzo floor, leafy green courtyard, semi-institutional Indonesian campus, calm public space",
  "location": "outdoor",
  "time_of_day": "day",
  "atmosphere": "quiet shaded campus calm",
  "subject_anchor": {
    "primary_subject": "covered campus walkway vantage, public bench at the camera-RIGHT against the inner wall, row of painted concrete columns camera-LEFT, leafy green courtyard beyond the columns camera-LEFT, terrazzo floor leading down the walkway",
    "subject_material": "painted concrete columns, terrazzo floor, painted plaster campus wall, weathered timber-slat bench, real lived-in campus surfaces",
    "supporting_objects": {
      "bench": "public bench, weathered timber slats, painted steel frame, camera-RIGHT against the inner wall",
      "columns": "row of painted concrete columns, camera-LEFT, open colonnade side, roof beams above",
      "notice_board": "campus notice board, inner wall camera-RIGHT, plain pinned notices",
      "courtyard": "leafy green campus courtyard, garden, faint lecture building, beyond the columns camera-LEFT background",
      "plants": "potted leafy plants, along the colonnade base, camera-LEFT",
      "floor": "clean terrazzo floor, leading down the walkway"
    },
    "human_absence_signal": "unoccupied, still, bench empty, walkway clear, courtyard quiet, empty"
  },
  "shot": {
    "composition": "medium-wide framing further down the walkway, the public bench at the camera-RIGHT against the inner wall, more colonnade depth, concrete columns camera-LEFT, leafy courtyard beyond the columns camera-LEFT, terrazzo floor leading in, wider vantage distinct from the tight bench plate",
    "framing": "MWS, bench camera-RIGHT, walkway depth visible, courtyard camera-LEFT, eye-level",
    "angle": "eye-level",
    "camera_position": "further down the walkway from the establishing wide, the bench at the camera-RIGHT against the inner wall, the open colonnade along camera-LEFT, distinct wider vantage from the BGK plate",
    "camera_direction": "along the walkway, bench camera-right, columns camera-left, courtyard beyond",
    "camera": "35mm prime spherical, deep focus front to back",
    "lighting": "soft even neutral daylight, shaded diffused key, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Indonesian public campus exterior realism, semi-institutional, class-accurate, lived-in"
}
```

---

## 4. Status manifest
| Cell | Angle | File | Serves | Status |
|---|---|---|---|---|
| M | establishing WIDE | `E09_selasarkampus_master.png` | SC07-SH01 | ✅ prompt LOCKED · generate PENDING (sesi baru) |
| BGK | bench MS | `E09_selasarkampus_bangku.png` | SC07-SH03/04/05 | ✅ prompt LOCKED · generate PENDING (sesi baru) |
| BGK2 | distinct bench vantage | `E09_selasarkampus_bangku2.png` | SC09-SH01/02/04 | ✅ prompt LOCKED · generate PENDING (sesi baru) |

Storage: `environment-images/E09_selasarkampus/` (+ `_rejected/`). Naming: `E09_selasarkampus_<angle>.png`.
Generate M first (no reference-image). Then BGK / BGK2 via the `shot`-only-rewrite method: upload `E09_selasarkampus_master.png` as reference + paste §1 verbatim + the cell's `shot` block. BGK2 is intentionally a wider, distinct vantage from BGK (avoid twin shots). Empty-EXT (no figures, no device in plate); figures + UI + warm/midday grade = GATE B / After Effects.

---

*E09 Selasar Kampus environment sheet — Fase-2 prompts LOCKED (generate PENDING, sesi baru) · Explainer Video 2 · 2026-07-01 · EXTERIOR (declared anchor deviation; repurposed slot E09 from the cut kafe) · used 2× (SC07 + SC09, bangku2 distinct vantage) · token-per-token · camera-relative direction.*
