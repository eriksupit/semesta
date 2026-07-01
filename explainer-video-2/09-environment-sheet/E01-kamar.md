---
title: Environment Sheet — E01 Kamar Herman · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e01-kamar, gate-0-env, image-generation]
status: active
created: 2026-06-22
updated: 2026-06-22
aliases: [ev2-e01-kamar, E01-kamar, kamar-herman-env]
---

# Environment Sheet — E01 KAMAR HERMAN · tag E01
> Method, scoped-angle rubric, 3 anchors, prompt-structure standard → [[00-README-ENV]] (§2.6 = prompt structure). Scene truth → [[03-scene-detail]] (SEQ1-SC01 + SEQ6-SC03). Furniture lock-anchors → [[tokens-references/INTERIOR-DESIGN-REFERENCE]] §6.
> **Room:** the parents' private bedroom (Herman + Ratna). Bookend — opens (SEQ1-SC01) and closes (SEQ6-SC03) the film; the coda must match the opener exactly. Empty-room reference plates, neutral grade; warm grade + practical light + characters added at GATE B keyframes.

---

## 1. Room identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E01 angle)
This block stays identical across ALL E01 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E01_kamar_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "private bedroom of an urban middle-class married couple, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "morning",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "IKEA MALM double bed frame with high headboard, white stained oak veneer, neatly made against rear wall, one side creased one side smooth",
    "subject_material": "oak veneer particleboard, matte cotton bedding muted slate-grey, ceramic-tiled floor",
    "wall_art": "a single dark-wood-framed woodblock print centered on the wall above the headboard reproducing Katsushika Hokusai 'The Great Wave off Kanagawa', Thirty-Six Views of Mount Fuji, surrounding walls plain matte plaster kept clean bare empty, this single framed Hokusai print the only wall-mounted item in the entire room",
    "supporting_objects": {
      "nightstand": "IKEA MALM 2-drawer chest white stained oak veneer as nightstand camera-right, face-down phone dark screen, lamp switched off",
      "chair": "IKEA INGOLF chair solid wood antique stain slatted backrest by the bed, folded dark plain-weave sarong and black brimless velvet cap on it",
      "wife_devotion": "folded white mukena and rolled prayer mat on a low shelf, folded plain headscarf on the same low shelf",
      "storage": "IKEA PAX wardrobe oak-effect doors along the left wall",
      "window_dressing": "IKEA LILL white sheer net curtains on the left-wall window",
      "rug": "IKEA PERSISK HAMADAN handmade oriental wool rug low pile",
      "openings": "closed white door on the right wall",
      "floor": "pair of slippers placed parallel on the rug"
    },
    "human_absence_signal": "unoccupied, still, one side of the bed smooth and undisturbed"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious materiality"
}
```
**Canonical layout (defined by master, reused by all angles):** bed against rear wall · single Hokusai centered above headboard · nightstand + lamp camera-right · PAX wardrobe + LILL-curtained window camera-left · closed door right wall · PERSISK rug + slippers foreground.

---

## 2. Method (per [[00-README-ENV]] §2.6)
> **⭐ OVERRIDE 2026-06-29 (validated bed4q experiment):** angle derivatives are NOT standalone full-prompt cells re-uploading the master in a fresh window (that resamples → inconsistent — proven across ~6 bed4q renders). **Canonical:** `E01_kamar_master.png` = parent (full prompt, Cell M); every other angle (bed3q, bed4q, nightstand, …) = **EDIT-IN-PLACE child in the SAME context window as the master**, master annotated (1) *recent camera view* + (2) *next/goal camera view* (terse goal-delta). The full-JSON cells below (B / B4 / N) are kept as the **fallback / spec record only**. Within a shot, framing+angle locked. Full law: `prompt-rules-text-image-to-image.md` changelog 2026-06-29.
- **Master generated first, no reference-image.** (Fallback path) Each derivative uploads `E01_kamar_master.png` as reference + rewrites ONLY the `shot` block → same room, new camera (not text-only mirror, not clone). Validated bed3q 2026-06-22; **demoted 2026-06-29.**
- **Branded furniture lock-anchors** keep furniture identical across angles ([[tokens-references/INTERIOR-DESIGN-REFERENCE]] §6).
- **Single named artwork** (Hokusai Great Wave) = strong cross-angle prior.
- **No religious-identity label** in `scene` (keyword-leak — pulled calligraphy over Hokusai); devotion carried by concrete objects + social class only.
- ADDENDUM A1: zero graphics, screens off. Neutral grade (warm at GATE B).

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` shot-list)
Each cell below is a COMPLETE copy-paste-ready prompt (full 6-layer + `subject_anchor` + `shot`), per SOP — zero scaffold, zero "combine with §1". §1 remains the canonical identity-lock reference; the cells are what you paste into the generator. Scoped to E01's shots: SEQ1-SC01 (ECU eyes, CU phone-on-nightstand, MCU Herman+phone, MS side-of-bed) + SEQ6-SC03 (MCU + ECU, bookend). Derivatives upload `E01_kamar_master.png` as reference-image.

### Cell M — MASTER · establishing wide (GRADED, lamp-ON) → `E01_kamar_master.png` · ✅ ACCEPTED 2026-07-02
> **RESET method (2026-07-01d):** master = full-prompt from-scratch, **grade BAKED** (subuh warm-lamp + cool-blue window), **attachment: NONE**. This is the accepted prompt (Erik-edited, 4th roll). Key fixes baked in: left-wall depth-order clause + anti-mirror; phone landscape/melintang canvas-% placement; `layout_continuity` lock-block. See `lessons.md` 2026-07-02.
```json
{
  "mood": "pre-dawn subuh domestic calm, quiet intimate stillness, gentle warmth of a single lit bedside lamp against cool blue dawn",
  "color_grade": "warm amber midtones from the practical lamp, cool blue shadow tones from pre-dawn window light, filmic warm-cool contrast, slightly-warmer Deakins midtones, gentle low-key",
  "style": "photorealistic cinematic interior, architectural clarity, ARRI Alexa Mini LF, prime spherical lens, Kodak Portra rendering, Roger Deakins naturalistic lighting",
  "scene": "private bedroom of a modern urban middle-class married couple, clean well-maintained contemporary IKEA flat-pack laminate furniture, matte painted plaster walls, tidy plain textiles, warm domestic",
  "location": "indoor",
  "time_of_day": "pre-dawn subuh around 04.40",
  "atmosphere": "quiet intimate domestic calm, lamp-lit against blue dawn",
  "subject_anchor": {
    "primary_subject": "IKEA MALM double bed, high headboard, white stained oak veneer, neatly made, against rear wall, one side slightly creased, one side smooth",
    "subject_material": "oak veneer particleboard, matte cotton bedding muted slate-grey, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, centered above headboard, Katsushika Hokusai 'The Great Wave off Kanagawa', only wall-mounted item",
    "supporting_objects": {
      "rear_wall": "headboard rear wall a single continuous matte plaster surface, unbroken solid plaster from corner to corner, carrying only the centered Hokusai print",
      "nightstand": "IKEA MALM 2-drawer chest, white stained oak, camera-right, table lamp switched on with warm glow. On the nightstand top, place exactly one slim black smartphone to the LEFT of the lamp base, clearly visible as a small horizontal rectangle. The phone lies flat with its black back casing facing upward, screen not visible. Its long edge must run perfectly left-to-right, parallel to the bottom edge of the image frame, forming a landscape / melintang horizontal silhouette. Do not place the phone vertically, diagonally, upright, or with its long edge running front-to-back. The nightstand is otherwise uncluttered",
      "phone_position": "final phone placement: exactly one slim black smartphone on the camera-right nightstand, positioned to the LEFT of the lamp base around the visual area x 66.5%, y 60.5% of the frame. It must appear as a clearly horizontal left-to-right rectangle, parallel to the bottom image edge, with black back casing visible and screen not visible",
      "chair": "IKEA INGOLF chair, antique-stain wood, slatted back, camera-right, folded dark plain-weave sarong, black velvet peci on seat",
      "wife_devotion": "low shelf, camera-right, folded white mukena, rolled prayer mat, folded plain headscarf",
      "storage": "IKEA PAX wardrobe, oak-effect doors, camera-left side wall, placed toward the near-camera foreground end, outside of the window position",
      "window_dressing": "single window set into the camera-left side wall, IKEA LILL sheer net curtains, cool blue pre-dawn light beyond; placed closer to the bed/headboard area than the wardrobe",
      "left_wall_layout": "on the camera-left side wall, from the deeper interior near the headboard area toward the outer near-camera foreground edge, the correct order is: window first, then PAX wardrobe; both remain on the same camera-left wall zone and the whole room must not be mirrored or flipped",
      "rug": "IKEA PERSISK HAMADAN oriental wool rug, low pile",
      "openings": "closed white door, camera-right wall",
      "floor": "slippers, parallel, on rug"
    },
    "human_absence_signal": "unoccupied, still, one side smooth"
  },
  "shot": {
    "composition": "full room, bed centered on rear wall, framed print centered above headboard, headboard wall a plain continuous plaster surface, camera-left wall carrying the window closer to the bed/headboard area and the PAX wardrobe farther outward toward the near-camera foreground edge, camera-right nightstand holding the warm lit lamp and exactly one clearly horizontal face-down black smartphone to the left of the lamp base, floor across foreground",
    "framing": "wide establishing, floor bottom 15%, ceiling line top",
    "angle": "eye-level, slight low angle, straight-on, centered",
    "camera_position": "room center axis, wall opposite the bed, equidistant from both side walls",
    "camera_direction": "facing headboard wall, square-on, symmetric, print on central vertical axis",
    "camera": "24mm prime spherical, deep focus",
    "lighting": "warm practical key from the bedside table lamp camera-right, cool blue pre-dawn ambient through the sheer-curtained camera-left side window, soft matte falloff, warm-cool contrast, low-key gentle",
    "aspect_ratio": "16:9"
  },
  "layout_continuity": {
    "left_side_order_correction": "from inside/deeper room near the bed-headboard area outward toward the near-camera edge, window first, then wardrobe",
    "phone_correction": "phone is final not transitional: flat on the camera-right nightstand to the left of the lamp base, long edge left-to-right parallel to the bottom image edge, landscape/melintang",
    "do_not_change": "do not alter bed position, rear wall, Hokusai print position or orientation, nightstand, lamp, chair, sarong, peci, low shelf, mukena, prayer mat, headscarf, closed white door, rug, slippers, ceramic floor, warm-cool pre-dawn grade, or straight-on centered framing",
    "do_not_mirror": "do not mirror or flip the room; preserve the established room handedness, keep only the corrected window-wardrobe ordering and the horizontal phone placement"
  },
  "negative_prompt": {
    "phone_errors": "no vertical phone, no portrait-orientation phone, no diagonal phone, no upright phone, no phone standing on edge, no phone with long edge running front-to-back, no second phone, no phone to the right of the lamp base",
    "layout_errors": "do not swap the room handedness, do not mirror the room, do not move the door, do not add extra wall art, do not add people"
  },
  "production_designer": "Eugenio Caballero, modern middle-class domestic realism, clean well-maintained dressing",
  "interior_designer": "Ilse Crawford, warm human-centred tactile, unpretentious contemporary materiality"
}
```
> Canonical layout correction (E01): camera-left wall = **window near headboard (deeper), PAX wardrobe toward foreground (outer)**; nightstand+warm lamp+face-down horizontal phone camera-right; rear headboard wall solid plaster + single Hokusai.

### Cell B — BED 3/4 (SH03, cool) → `E01_kamar_bed3q.png` · ✅ ACCEPTED 2026-07-02
Serves SEQ1-SC01-SH03 (right-diagonal medium, Herman lying). **Method (CANONICAL) = EDIT-IN-PLACE FROM the master render, in a master-anchored ChatGPT session** (canvas = master render; old disk plates are legacy, NOT the edit canvas). Re-angle to the right-side 3/4 + cool-grade both hold in-session. ⚠ CORRECTION 2026-07-02: an earlier note here claimed "regrade the old bed3q plate / re-angle drifts by reference-dominance" — that drift was MY separate reference-UPLOAD-in-fresh-window experiments, NOT Erik's in-session master-edit (which re-angles cleanly, proven on B4). The text below is the descriptive target spec (the exact in-session prompt Erik typed was not captured):
```text
Target: right-side three-quarter view of the bed — headboard + Hokusai 'The Great Wave' print, camera-right nightstand + chair, camera-left window + wardrobe, rug + slippers, foot toward camera.
Grade: pre-dawn subuh, bedside lamp OFF (dark shade, no glow), room lit solely by cool blue pre-dawn ambient through the sheer-curtained camera-left window — very low-key, dim, cool blue tonality, clean exposure, lifted shadow detail, no black crush, no warm cast. Preserve room identity + handedness, do not mirror. 16:9.
```

### Cell M-off — MASTER lamp-OFF (GRADED, cool) → `E01_kamar_master_lampoff.png` · ✅ ACCEPTED 2026-07-02
Parent for the COOL derivatives (SH02 nightstand, SH03 bed3q). **Edit-in-place on the accepted `E01_kamar_master.png` render** (canvas = that render, no re-upload). Accepted prompt verbatim:
```text
Edit (fidelity High, canvas = E01_kamar_master render):
Switch the bedside table lamp OFF — bulb and shade go dark, remove the warm glow entirely, no warm cast on the nightstand, headboard, or walls. Relight the whole room with only the cool blue pre-dawn ambient through the sheer-curtained camera-left window: very low-key, dim, cool blue tonality throughout, gentle clean exposure with lifted shadow detail, low noise, no black crush.
Everything else unchanged: bed and bedding, headboard, the Hokusai 'The Great Wave' print position and orientation, the rear headboard wall solid plaster, the camera-right nightstand holding exactly one face-down horizontal black phone (screen off) to the left of the now-dark lamp, the chair with folded sarong and peci, the low shelf, the camera-left wall layout (window nearer the headboard, PAX wardrobe toward the foreground), the rug, the slippers, the closed white door, the ceramic floor, and the exact straight-on centered framing. Do not move, add, or mirror anything — only change the lighting from warm-lamp-on to cool-blue lamp-off.
```

### Cell N — NIGHTSTAND insert (SH02, cool) → `E01_kamar_nightstand.png` · ✅ ACCEPTED 2026-07-02
SEQ1-SC01-SH02. **Edit-in-place on `E01_kamar_master_lampoff.png`** (canvas) **+ attached angle reference**. Erik-edited accepted prompt, verbatim (adds explicit camera-height delta + frame layout + prop-lock, per lessons 2026-07-02):
```text
Reframe tighter into a close insert of the camera-right nightstand, using the attached angle reference: camera height lowered from the previous high top-down view, with only a very slight downward angle / subtle tilt-up feeling, closer to a natural bedside insert rather than an overhead shot.
Fill the 16:9 frame with the nightstand top in the lower-right foreground, the switched-off table lamp on the right side of the nightstand, and the single face-down black smartphone to the LEFT of the lamp base. The phone must lie flat in horizontal / landscape orientation, its long edge running left-to-right across the nightstand, screen off, black casing visible, not diagonal, not vertical, not upright. The nightstand surface remains otherwise uncluttered.
Include the adjacent bed edge and pale wood headboard on the left side of frame, with grey bedding and pillow partially visible. Behind, show the matte plaster wall and the lower corner / lower portion of the dark-wood-framed Hokusai "The Great Wave off Kanagawa" print near the upper-left of frame, cropped naturally by the tighter composition.
Lighting remains lamp-off only: very low-key cool-blue pre-dawn ambient from the camera-left window, dim but clean exposure, lifted shadow detail, no black crush, no warm lamp glow, no warm cast on the wall, headboard, nightstand, lamp shade, or phone.
Everything else unchanged from the bedroom continuity: same camera-right MALM nightstand, same lamp switched off, same single face-down horizontal black phone left of the lamp base, same headboard, same bedding, same Hokusai print position and orientation, same cool-blue pre-dawn grade. Do not add objects, do not move the phone to the right of the lamp, do not rotate the phone vertically or diagonally, do not turn the lamp on, do not mirror the room. Keep 16:9.
```

### Cell B4 — BED 3/4 left-side / window-side (SH04, cool) → `E01_kamar_bed4q.png` · ✅ ACCEPTED 2026-07-02
SEQ1-SC01-SH04 (wide 2-subject, Herman camera-right / Ratna camera-left). **Method = EDIT-IN-PLACE FROM the master render, in a master-anchored ChatGPT session** (canvas = master lamp-off render; NOT an upload of any old disk plate — those are legacy). Re-angle described relative to room furniture ("near the wardrobe / window curtain, same height, slight rightward tilt") + cool-grade lock; identity + handedness held cleanly (in-session master-edit re-angles without drift). Erik-edited accepted prompt, verbatim:
```text
Edit-in-place (canvas = render master lamp-off):
Change the camera angle to a left-side three-quarter bedroom view from very close to the camera-left window curtains. Move the camera forward from the wardrobe area until it is almost pressed against / just beside the outer edge of the sheer curtain, with the curtain occupying the far-left foreground edge of the frame. Keep the camera at approximately the same height as the previous room view, then apply a slight tilt / pan to the RIGHT so the view looks diagonally across the bed toward the headboard and camera-right wall.
The bed should dominate the frame in a calm three-quarter view: foot of the bed closer to camera, headboard farther back, both pillows visible, grey bedding dimly lit with soft cool-blue folds. Show the pale MALM headboard and the correctly oriented Hokusai "The Great Wave off Kanagawa" print centered above it on the rear plaster wall.
Preserve the same room identity and true handedness: window and sheer curtain remain on the actual camera-left wall, with the PAX wardrobe also on the camera-left side but mostly out of view / only implied near the far-left edge; the MALM nightstand, switched-off table lamp, single face-down horizontal black phone, wooden chair with folded sarong and black peci, low shelf, and closed white door remain on the actual camera-right side. Do not mirror or flip the room.
Keep the cool blue lamp-off pre-dawn grade exactly: bedside lamp switched OFF, shade dark, no glow, no warm cast anywhere. The room is lit only by very low-key cool-blue pre-dawn ambient coming through the sheer-curtained camera-left window. Dim but clean exposure, lifted shadow detail, no black crush, quiet subuh stillness.
Keep all furniture, objects, materials, wall art, rug, slippers, bedding, ceramic floor, and room continuity unchanged. Do not add people or objects. Do not move the furniture. Only change the camera position to the near-curtain left-side vantage with a slight rightward tilt. Keep 16:9.
```
**SH04-END warm variant → `E01_kamar_bed4q_warm.png` · ✅ ACCEPTED 2026-07-02** — edit-in-place ON the accepted `E01_kamar_bed4q.png` COOL render (canvas = that render), delta = lamp ON; vantage held, warm-cool contrast. Accepted prompt verbatim:
```text
Edit-in-place (canvas = render E01_kamar_bed4q cool):
Switch the camera-right bedside table lamp ON, with a warm amber glow keying the nightstand, the headboard, and the bed from the camera-right side. Keep the cool blue pre-dawn ambient coming through the sheer-curtained camera-left window, so the room reads as a filmic warm-cool contrast — warm amber midtones near the lamp, cool blue shadow tones toward the window. Low-key and gentle, clean exposure, lifted shadow detail, no black crush.
Everything else unchanged: same left-side three-quarter vantage, same bed, bedding, headboard, Hokusai print, nightstand, chair, window, wardrobe, door, rug, slippers, room identity and handedness. Do not move the camera, do not re-angle, do not add or move objects, do not mirror the room. Only change the lighting from lamp-off to warm lamp-on. Keep 16:9.
```

### Cell R — eye-level medium head-end (SH05 Ratna, warm) → `E01_kamar_ratna_med.png` · ✅ ACCEPTED 2026-07-02
SEQ1-SC01-SH05 (medium on Ratna sitting up, camera-left side, warm grade ← SH04-END). Background env-plate. **Edit-in-place (reframe tighter to eye level) ON the accepted `E01_kamar_bed4q_warm.png` render.** Accepted prompt verbatim:
```text
Edit-in-place (canvas = render E01_kamar_bed4q_warm):
Reframe tighter and bring the camera down to eye level, into a medium shot of the near-left side of the bed — the side by the window where the wife lies. Frame the head end of that left side and the wall behind: the pale MALM headboard and the Hokusai 'The Great Wave' print above it, with the warm-lit nightstand and switched-on lamp visible in the camera-right background.
Keep the same warm lamp-on grade exactly — warm amber key from the camera-right lamp, cool blue pre-dawn ambient from the camera-left window behind, filmic warm-cool contrast, low-key, clean exposure, no black crush. Everything else unchanged: same room, furniture, materials, wall art, handedness. Only tighten to the eye-level medium framing. Do not re-angle beyond eye level, do not mirror, do not add people or objects. 16:9.
```

---

## 4. Status manifest
| Cell | Angle | File | Status |
|---|---|---|---|
| M | establishing wide (GRADED lamp-ON) | `E01_kamar_master.png` | ✅ ACCEPTED 2026-07-02 · **RESET graded** (subuh warm-lamp + cool-blue window, attachment NONE) · left-wall order jendela(dalam)→lemari(luar) · rear wall solid plaster · HP melintang face-down kiri-lampu · supersede master netral lama |
| M-off | establishing wide (GRADED lamp-OFF) | `E01_kamar_master_lampoff.png` | ✅ ACCEPTED 2026-07-02 · **edit-in-place DI ATAS `E01_kamar_master.png`** (matikan lampu → very-low-key cool-blue pra-subuh, geometri identik) · parent utk derivatif COOL (SH02 nakas-CU, SH03 bed3q). Validasi: darken+cool = arah edit-in-place aman |
| B | bed 3/4 (SH03, cool) | `E01_kamar_bed3q.png` | ✅ ACCEPTED 2026-07-02 · **edit-in-place DARI render master** (sesi ter-anchor-master; re-angle right-side 3/4 + cool lamp-off) · timpa legacy · (koreksi: "regrade plat-lama/reference-dominance drift" = artefak teknik reference-upload saya, bukan metode in-session) |
| N | nightstand insert (SH02, cool) | `E01_kamar_nightstand.png` | ✅ ACCEPTED 2026-07-02 · **RESET: edit-in-place dari `E01_kamar_master_lampoff.png`** (reframe-tight nakas camera-right + turunkan tinggi kamera dari top-down ke bedside-insert; lampu OFF, HP face-down melintang kiri-lampu, cool-blue lamp-off, 16:9) · supersede plat netral lama |
| B4 | bed 3/4 left/window-side (SH04-START, cool) | `E01_kamar_bed4q.png` | ✅ ACCEPTED 2026-07-02 · **edit-in-place DARI render master lamp-off** (sesi ter-anchor-master; re-angle "dekat tirai/lemari, tinggi sama, tilt kanan"); identitas+handedness utuh, grade cool lamp-off · timpa legacy |
| B4-warm | bed 3/4 left/window-side (SH04-END, warm) | `E01_kamar_bed4q_warm.png` | ✅ ACCEPTED 2026-07-02 · **edit-in-place lamp-ON DI ATAS `E01_kamar_bed4q` cool** (vantage sama, warm-cool contrast) · file baru (bed4q cool tetap START) |
| R | eye-level medium head-end (SH05 Ratna, warm) | `E01_kamar_ratna_med.png` | ✅ ACCEPTED 2026-07-02 · **reframe eye-level DI ATAS `E01_kamar_bed4q_warm`** (rapatkan ke head-end sisi-kiri Ratna, warm) · background-plate keyframe SH05 |
| W | wall-art reverse | `E01_kamar_wallart_reverse.png` | ⏸ DEFERRED — tidak dipakai SEQ1-SC01 (hygiene). Plat lama masih ber-jam + spec sudah dikoreksi (1 nakas, kiri kosong); regen head-on saat ada scene yang memakainya. Jangan dipakai apa adanya. |

> **Clock removal (2026-06-23):** jam weker analog dibuang dari seluruh spec E01 (jarum analog tak andal di t2i, 2 render gagal; waktu subuh tetap via kartu AE `Waktu Subuh · 04.42` di layar HP). Keempat plat lama mengandung jam → regen **master dulu** (clock-free), lalu derivatif attach master baru. SH01 `sc01_sh01_*` yang sudah ACCEPT aman (jam di luar crop CU).

Storage: `environment-images/E01_kamar/` (+ `_rejected/`). Naming: `E01_kamar_<angle>.png`.
Generate W and N via the `shot`-only-rewrite method: upload `E01_kamar_master.png` as reference + paste §1 verbatim + the cell's `shot` block.

---

*E01 Kamar environment sheet v1.0 · Explainer Video 2 · 2026-06-22 · method [[00-README-ENV]] · companion [[08-character-sheet/H-herman]]*
