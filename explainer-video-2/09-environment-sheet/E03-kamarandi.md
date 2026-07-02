---
title: Environment Sheet — E03 Kamar Andi · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e03-kamarandi, gate-0-env, image-generation]
status: active
created: 2026-06-23
updated: 2026-07-02
aliases: [ev2-e03-kamarandi, E03-kamarandi, kamar-andi-env, ev2-e03-ruangbelajar]
---

# Environment Sheet — E03 KAMAR ANDI · tag E03
> Method → [[00-README-ENV]] + [[semesta-env-method-kling]] (RESET graded master + edit-in-place derivatives). Scene truth → [[10-gateB-keyframes/SEQ2-SC06]] (INT. RUANG BELAJAR — 08.30, cross-cut SC05). Master render → `environment-images/E03_kamarandi/E03_kamarandi_master.png`.
> **Room:** Andi's own bedroom with a study corner (child ~10). The SEQ2-SC06 online-class beat plays at the study desk inside Andi's bedroom. 1× use.

> **★ CONCEPT RESET 2026-07-02 (Erik approve).** E03 was a standalone "ruang belajar" that read too much like the E02 living room (same house-register + same desk-on-back-wall / cube-shelf-side-wall / framed-print pattern → near-twin). MERGED into **Andi's bedroom + study corner** (one room, saves space; a middle-class Indonesian kid's study is normally in his bedroom). The **single child bed** is now the room-defining object → differentiates hard from the living room at the room-TYPE level (not just dressing). Same house register held (IKEA/plaster/Hokusai). Slug `ruangbelajar` → `kamarandi`; old scene label SC03 → real scene **SEQ2-SC06**.

> **★ GRADE (RESET graded master, 2026-07-02).** Scene = morning 08.30. Grade BAKED into the master per [[semesta-env-method-kling]] (Kling i2v takes look from the env image). **Cinematic day-interior warm-cool separation:** cool soft neutral-blue morning daylight from the window = the ambient anchor (the "blue" that keeps E03 in the same cinematic family as E02's subuh), warm amber clip desk-lamp practical ON = the warm pool. Single grade state (no toggle). Correction that drove this: my first E03 master was warm-dominant / flat = un-cinematic vs E02's warm-cool separation (Erik flagged "belum sinematik, tak ada biru").

> **A1 (screens OFF, UI=AE) + token-dignity (modern/clean, no weathered/class-coded)** hold. Third distinct Hokusai = *Kajikazawa in Kai Province* (E01 Great Wave, E02 Red Fuji). Zero character-IP (Schleich real-animal T-Rex; earlier Marvel/de-branded-robot tokens tripped an Iron-Man likeness guardrail — see `_rejected` history, now deleted).

---

## 1. Room identity lock (canonical layout)
**Canonical layout (from the master RENDER = Rank-1 truth, camera POV = front of room looking at the far back window-desk wall):** single child bed along the **camera-LEFT** wall (headboard back-left) = dominant object · study corner on the far **BACK** wall = PÅHL desk + tablet-on-stand (OFF) + child chair + clip lamp (ON), the LILL-curtained window on the **camera-LEFT** of the desk (toward the bed side), framed Kajikazawa print above the desk · KALLAX 2×2 cube shelf (storybooks + LEGO + globe) with the Schleich T-Rex hero on top + cork pinboard (world map) above it on the **camera-RIGHT** wall · open doorway + light switch + wall hook (cloth tote) on the **camera-RIGHT** wall toward the front · small child rug on the open ceramic floor centre. **No sofa, no TV** — this is a bedroom, not the living room.
> **⚠ HANDEDNESS — render overrode spec (corrected 2026-07-02c):** the Cell M master PROMPT text says "window camera-RIGHT of the desk", but the ACCEPTED master render placed the **window camera-LEFT of the desk** (near the bed). Rank-1 truth = the render → **window camera-LEFT**. Confirmed on the `desk` derivative (window camera-left, shelf/T-Rex camera-right). All derivatives + downstream keyframes follow the RENDER handedness, NOT the master prompt's "camera-right" wording. Master JSON below kept VERBATIM as submitted (historical record); do not re-read its "camera-right" as truth.

**ADDENDUM A1:** ONE device, OFF — the tablet on its folding stand (the SEQ2-SC06 online-class tablet). Screen renders OFF/dark; all UI (online-class board, "Jawaban Tepat ⭐" sponsor mark, side ad card) composited in After Effects.

---

## 2. Method
- **Master = full-prompt from-scratch, grade BAKED** (morning warm-cool separation), attachment NONE. Accepted first-roll (Erik-generated). Prompt verbatim in Cell M below.
- **Derivatives = edit-in-place on the accepted master render** (canvas = `E03_kamarandi_master.png`; NOT reference-upload, NOT old disk plates — legacy deleted) + the angle/reframe delta. One derivative per distinct shot-angle SEQ2-SC06 needs.
- SEQ2-SC06 angle-need (from the scene doc): SH01 doorway/MWS establishing · SH02 desk MEDIUM (Andi+tablet) · SH03 tablet CLOSE insert · SH04 desk MEDIUM 2-shot (Andi+Ratna, same desk angle as SH02) · SH05 = character CU (no env plate). → env derivatives: **doorway** (SH01) + **desk** (SH02/SH04) + **tablet** (SH03). ✅ ALL ACCEPTED (edit-in-place from the master render). E03 COMPLETE 4/4.

---

## 3. Plate matrix

### Cell M — MASTER · establishing wide (GRADED, day warm-cool) → `E03_kamarandi_master.png` · ✅ ACCEPTED 2026-07-02
Bedroom+study establishing. Bed dominant camera-left, study corner back wall by window, shelf+doorway camera-right. Grade = cool daylight anchor + warm desk-lamp practical ON. Accepted prompt VERBATIM (Erik-generated, first roll):
```json
{
  "mood": "bright cinematic morning domestic stillness, a child's bedroom with a study corner where cool soft daylight falls from the window against a warm practical desk lamp, cinematic warm-cool separation, restrained naturalism, unoccupied and still",
  "color_grade": "cinematic restrained day-interior grade, cool soft neutral-blue morning daylight from the window as the ambient anchor, warm amber desk-lamp practical pooling on the pine desk and nearby wall, gentle warm-cool separation, neutral off-white plaster preserved, natural white-stained pine tones, shaped cinematic contrast, lifted but shaped blacks, soft matte falloff, clean exposure, slightly cool Deakins daylight midtones, Lubezki-style observational naturalism, no flat even brightness, no global warm wash, no yellow wall cast, no orange cast, no sepia, no teal-orange look",
  "style": "photorealistic cinematic interior, architectural clarity, ARRI Alexa Mini LF, 24mm prime spherical lens, deep focus front to back, Kodak Portra natural rendering, Roger Deakins-inspired restrained practical-light naturalism, Emmanuel Lubezki-style observational domestic realism",
  "scene": "child's bedroom with a study corner in a modern urban middle-class family home, clean well-maintained contemporary IKEA flat-pack laminate furniture, a single child bed as the main furniture, matte painted plaster walls, tidy plain textiles, low tidy shelving, soft small child floor rug, warm domestic realism",
  "location": "indoor",
  "time_of_day": "morning around 08.30",
  "atmosphere": "quiet cinematic domestic calm, cool morning daylight through the sheer-curtained window meeting a warm desk-lamp pool, a child's tidy bedroom, still and unoccupied",
  "subject_anchor": {
    "primary_subject": "single child bed, IKEA SLÄKT white frame, plain, neatly made, plain pale duvet with a small simple pattern, one pillow, long side against the camera-left wall, headboard at the far back-left corner, the room-defining object",
    "subject_material": "neutral muted off-white matte painted plaster walls, white-stained pine effect laminate furniture, white bed frame, plain desaturated woven textiles, clean ceramic-tiled floor with soft warm and cool reflections",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Kajikazawa in Kai Province', Thirty-Six Views of Mount Fuji, centered above the study desk, far back wall, correct orientation",
    "supporting_objects": {
      "bed": "single child bed, IKEA SLÄKT white frame, low plain headboard, neatly made pale duvet with a small simple pattern, one pillow, long side along the camera-left wall, headboard at the far back-left corner",
      "desk": "study corner, IKEA PÅHL desk white-stained pine effect, against the far back wall beside the window, generic unbranded tablet on a folding stand facing the chair, screen off dark neutral, slim closed exercise book, short pencil cup, Rubik's Cube 3x3 colour cube, otherwise uncluttered",
      "chair": "small child desk chair, plain white frame, plain pale seat, tucked at the desk",
      "shelf": "IKEA KALLAX shelving unit, 2x2 open square cube grid, white-stained oak effect, on the camera-right wall, closed hardcover storybooks, LEGO Classic small colourful brick build, LEGO brick storage box, small educational desk globe, in the cubes, otherwise tidy",
      "display_figure": "Schleich Tyrannosaurus rex toy figure, museum-realistic sculpt, posed standing, on top of the KALLAX unit, prominent, single hero display piece",
      "rug": "small soft pale grey low-pile child rug, on the open ceramic floor, centre",
      "window_dressing": "one normal-proportioned rectangular window set into the far back wall beside the desk, fully visible, not cropped, fitted with IKEA LILL sheer net curtains, cool soft morning daylight beyond",
      "pinboard": "small cork pinboard, on the camera-right wall above the KALLAX shelf, educational world map poster pinned, otherwise plain",
      "openings": "open doorway on the camera-right wall toward the front, light switch plate beside the doorway",
      "lighting_fixture": "plain ceiling lamp switched off, small clip reading lamp clamped at the desk edge switched ON, a warm amber practical glow at the desk",
      "wall_hook": "modest wall hook on the camera-right wall beside the doorway, plain cloth tote bag hanging from it"
    },
    "human_absence_signal": "unoccupied, still, bed neatly made, chair tucked in, tablet screen dark, room empty, quiet"
  },
  "shot": {
    "composition": "full room geography in one frame: single child bed along the camera-left wall as the dominant foreground object, study corner on the far back wall with the PÅHL desk and tablet on its stand beside the sheer-curtained window and the framed Kajikazawa print above the desk, KALLAX cube shelf with the Schleich Tyrannosaurus rex on top and the cork pinboard above it on the camera-right wall, open doorway and light switch on the camera-right wall toward the front, small child rug on the open floor centre, all legible",
    "framing": "WS establishing, floor visible bottom 20%, ceiling line visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "front of room, looking toward the far back window-desk wall",
    "camera_direction": "straight down the room toward the far back wall, bed along camera-left, study desk and Kajikazawa and window on the far back wall, KALLAX shelf and doorway camera-right, open floor centre",
    "camera": "24mm prime spherical, deep focus front to back",
    "lighting": "cool soft neutral-blue morning daylight from the sheer-curtained back-wall window as the ambient key, a warm amber desk-lamp practical pooling on the PÅHL desk and the wall beside it, gentle localized falloff rather than a global wash; sunlit and lamp-lit zones read warm, the shadow side, doorway wall, under-shelf, and corners hold cool blue-gray ambient; shaped cinematic contrast, lifted blacks, no black crush, not flat, not evenly lit, restrained saturation",
    "aspect_ratio": "16:9"
  },
  "layout_continuity": {
    "do_not_change": "do not alter the single child bed on the camera-left wall, PÅHL desk and window on the far back wall, Kajikazawa print position or orientation, KALLAX shelf, Schleich T-Rex, cork pinboard, doorway, child rug, ceramic floor, or straight-down-the-room framing; keep the bed as the dominant camera-left object and the study corner on the far back wall beside the window",
    "do_not_mirror": "do not mirror or flip the room, preserve room handedness: single bed on the camera-left wall, study desk and window on the far back wall, KALLAX shelf and cork pinboard and doorway on the camera-right wall"
  },
  "negative_prompt": {
    "screen_errors": "no glowing screens, no lit tablet, all screens off dark neutral",
    "grade_errors": "no flat even catalog brightness, no evenly lit showroom, no single-temperature wash, no global warm wash, no yellow wall cast, no caramel ceiling, no orange cast, no sepia, no overly saturated amber, no exaggerated teal-orange grading, no crushed blacks, no night, no dark room",
    "layout_errors": "do not mirror the room, do not turn this into a living room, no sofa, no television, do not move the bed off the camera-left wall, do not move the desk away from the window, do not crop or block the window, do not make the window a narrow slit, do not add extra wall art, do not add people"
  },
  "production_designer": "Eugenio Caballero, modern middle-class domestic realism, clean well-maintained dressing",
  "interior_designer": "Ilse Crawford, warm human-centred tactile, unpretentious contemporary materiality"
}
```
> Render review PASS: bed dominant camera-left (reads clearly as child bedroom, NOT living room) · study corner back wall by window · clip lamp ON warm pool ⟷ cool window daylight (cinematic warm-cool separation, not flat) · T-Rex on KALLAX · Kajikazawa above desk · cork pinboard + world map camera-right · doorway + tote camera-right · screens OFF · handedness correct. ⚠ minor non-blocking: KALLAX reads ~2 cubes not full 2×2 (background, accepted).

### Cell D — DESK / study-station MEDIUM → `E03_kamarandi_desk.png` · ✅ ACCEPTED 2026-07-02
Serves SEQ2-SC06 SH02 (Andi+tablet MEDIUM, 50mm) + SH04 (2-shot Andi+Ratna, same angle). **Method = edit-in-place on the accepted `E03_kamarandi_master.png` render.** Render PASS: desk + tablet(OFF) + tucked chair + Kajikazawa fill frame · window camera-LEFT (cool daylight) ⟷ clip-lamp warm pool = warm-cool separation held · KALLAX+T-Rex camera-RIGHT · handedness consistent with master render · bed fell out of frame. ⚠ minor: desk reads with a front panel (PÅHL is open-leg) — background detail, accepted. Accepted prompt VERBATIM:
```text
Edit-in-place (canvas = render E03_kamarandi_master):
Reframe into a medium shot of the study corner on the far back wall. Push in from the establishing wide toward the PÅHL desk so the desk, the tablet on its folding stand (screen OFF dark neutral), the tucked child chair, and the framed Kajikazawa print above fill the frame, with the sheer-curtained window and its cool daylight just behind on the camera-right of the desk. Camera at seated-child height, eye-level, 50mm feel. Let the single child bed fall to the far camera-left frame edge or just out of frame.
Keep the same day grade exactly: cool soft neutral-blue morning daylight from the window as the ambient anchor, a warm amber clip desk-lamp practical pooling on the desk, gentle warm-cool separation, neutral off-white plaster, lifted blacks, shaped cinematic contrast, not flat, not evenly lit. Everything else unchanged — same desk, same tablet and folding stand, same child chair, same Kajikazawa print position and orientation, same window, same ceramic floor, same room identity and handedness (bed camera-left, desk and window on the back wall, KALLAX shelf and doorway camera-right). Do not turn the tablet screen on, do not add UI, do not add people, do not mirror the room. Keep 16:9.
```
> Note: the prompt text says "window ... camera-right of the desk" but the render (following the master) placed it camera-LEFT — consistent with the master render, accepted. Downstream: window camera-LEFT is truth.

### Cell T — TABLET insert CLOSE → `E03_kamarandi_tablet.png` · ✅ ACCEPTED 2026-07-02
Serves SEQ2-SC06 SH03 (CU tablet screen, 85mm). **Method = edit-in-place on the accepted `E03_kamarandi_master.png` render.** Render PASS: tablet on folding stand fills frame, screen OFF dark neutral slab (ideal for AE online-class UI + "Jawaban Tepat ⭐") · pencil cup + Rubik's Cube camera-right · sheer window camera-LEFT with cool daylight · warm lamp pool ⟷ cool window = warm-cool separation held · handedness consistent. Accepted prompt VERBATIM:
```text
Edit-in-place (canvas = render E03_kamarandi_master):
Reframe into a close insert of the tablet on the PÅHL desk. Fill the frame with the tablet on its folding stand, its screen OFF as a dark neutral slab — no UI, no icons, no glow. Show the white-pine desk surface with the short pencil cup and the small Rubik's Cube 3x3 beside the stand, and behind them a soft out-of-focus sliver of the far back wall and the sheer-curtained window on the camera-left with its cool daylight. Camera close in front of the desk at seated-child height, slight eye-level angle onto the screen, 85mm feel, shallow-ish depth.
Keep the same day grade exactly: cool soft neutral-blue morning daylight from the camera-left window, a warm amber clip desk-lamp practical pooling on the desk, gentle warm-cool separation, neutral off-white plaster, lifted blacks, shaped cinematic contrast, not flat. Everything else unchanged — same tablet and folding stand, same desk surface and props, same window on camera-left, same room identity and handedness. Do not turn the tablet screen on, do not add UI, do not add people, do not mirror the room. Keep 16:9.
```

### Cell W — DOORWAY 3/4 diagonal establishing → `E03_kamarandi_doorway.png` · ✅ ACCEPTED 2026-07-02
Serves SEQ2-SC06 SH01 (establishing, 35mm). **Method = edit-in-place RE-ANGLE on the master render (furniture-anchored, NOT "keep same vantage").** ⚠ First attempt hedged "keep the same front-of-room camera position" → render came back near-identical to master (Erik flagged "angle sama terus?"). REJECT + redo: drop the hedge, anchor the camera to the doorway/shelf side + name the diagonal → landed a real 3/4 diagonal establishing (bed camera-left foreground, desk+window mid/back, KALLAX+T-Rex+tote+doorway camera-right foreground). Distinct angle from master, identity + grade + handedness held. Accepted prompt (redo) VERBATIM:
```text
Edit-in-place (canvas = render E03_kamarandi_master):
Change the camera angle to a three-quarter establishing view taken from the camera-right doorway corner. Move the camera to the camera-right side near the open doorway and angle it diagonally across the room toward the far back wall, so the view looks over the child rug toward the PÅHL study desk and the sheer-curtained window, with the single child bed running along the camera-left wall in the mid-ground. Keep eye-level standing height, 35mm feel. This is a real diagonal re-angle, not the flat front-on master view.
Keep the room and handedness exactly: single bed on the camera-left wall, study desk with the tablet on its stand and the framed Kajikazawa above on the far back wall, the window on the camera-left of the desk, the KALLAX shelf with the Schleich T-Rex on top and the cork map above it now in the camera-right foreground beside the open doorway, the cloth tote on the wall hook.
Keep the same day grade exactly: cool soft neutral-blue morning daylight from the window as the ambient anchor, a warm amber clip desk-lamp practical pooling on the desk, gentle warm-cool separation, neutral off-white plaster, lifted blacks, shaped cinematic contrast, not flat, not evenly lit. Do not turn the tablet screen on, do not add UI, do not add people, do not mirror the room. Keep 16:9.
```
> **Lesson:** edit-in-place CAN re-angle (moderate 3/4) if you anchor the camera to named furniture + drop any "keep same vantage" phrasing. A hedge to "keep vantage" collapses the derivative back onto the master (edit-in-place under-shoots + the hedge kills the delta). Frontal near-master first attempt DELETED.

---

## 4. Status manifest
| Cell | Angle | File | Status |
|---|---|---|---|
| M | establishing wide (GRADED day warm-cool) | `E03_kamarandi_master.png` | ✅ ACCEPTED 2026-07-02 · RESET concept (Kamar Andi bedroom+study) + graded (cool-daylight anchor + warm desk-lamp ON), attachment NONE · bed dominant camera-left · screens OFF · handedness OK · legacy `ruangbelajar` plates + folder + rejected DELETED (Erik) |
| D | desk / study-station MEDIUM (SH02/SH04) | `E03_kamarandi_desk.png` | ✅ ACCEPTED 2026-07-02 — edit-in-place from master render; desk+tablet(OFF)+chair+Kajikazawa fill frame, warm-cool grade held, handedness consistent (window camera-LEFT), bed out of frame |
| T | tablet insert CLOSE (SH03) | `E03_kamarandi_tablet.png` | ✅ ACCEPTED 2026-07-02 — edit-in-place from master render; tablet fills frame screen-OFF slab (UI=AE), pencil cup + Rubik's, window camera-LEFT cool, warm-cool grade held |
| W | doorway 3/4 diagonal establishing (SH01) | `E03_kamarandi_doorway.png` | ✅ ACCEPTED 2026-07-02 — edit-in-place RE-ANGLE (furniture-anchored) from master render; real diagonal (not flat-frontal), identity+grade+handedness held; frontal near-master 1st attempt REJECTED+deleted |

Storage: `environment-images/E03_kamarandi/` (+ `_rejected/`). Naming: `E03_kamarandi_<angle>.png`.
**Workflow:** master accepted (graded, attachment NONE) → each derivative = edit-in-place on the accepted master render + angle/reframe delta.

---

*E03 Kamar Andi environment sheet v2.0 (concept RESET 2026-07-02) · Explainer Video 2 · COMPLETE 4/4 graded (master/desk/tablet/doorway) ACCEPTED · same house as [[E01-kamar]] / [[E02-ruangkeluarga]] · third distinct Hokusai (Kajikazawa) · Schleich T-Rex hero · scene [[10-gateB-keyframes/SEQ2-SC06]]*
