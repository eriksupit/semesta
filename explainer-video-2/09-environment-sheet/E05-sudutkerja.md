---
title: Environment Sheet — E05 Sudut Kerja Ratna · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e05-sudutkerja, gate-0-env, interior]
status: fase2-prompt-locked
created: 2026-06-30
updated: 2026-07-01
aliases: [ev2-e05-sudutkerja, E05-sudutkerja, sudut-kerja-ratna-env]
---

# Environment Sheet — E05 SUDUT KERJA RATNA · tag E05
> Method, scoped-angle rubric, 3 anchors, prompt-structure standard → [[00-README-ENV]] (§2.6 = prompt structure). Scene truth → [[03-scene-detail]] (SEQ3-SC08). Shotlist → `10-gateB-keyframes/SEQ3-SC08.md`. Furniture lock-anchors → [[tokens-references/INTERIOR-DESIGN-REFERENCE]] §6.
> **Room:** Ratna's home work corner (UMKM online-business nook) — a small home-office where she opens a bank's virtual branch on an all-in-one desktop and video-calls a bank officer (SEQ3-SC08-SH01 MW establishing, SH02/SH04 CU screen insert, SH03/SH05 M Ratna at the all-in-one). 1× use. **Same house as E01/E02/E03** — inherits the §3 architecture anchor + material gestalt (matte plaster, IKEA flat-pack laminate, plain desaturated textiles, ceramic floor). Distinct from E02 (ruang-keluarga desktop) + E04 (dapur) + E15 (depan-rumah). Empty-room reference plates, neutral grade; warm grade + practical light + Ratna (berhijab) added at GATE B keyframes.

> **Token discipline (locked):** every JSON token value below is a comma-delimited token cluster, NOT a sentence — conjunctions (`and / for / with / bearing`) and prose connectors are banned inside token values (`prompt-rules` b.119). Surrounding markdown is documentation, not pasted into the generator. **Fase-2 status:** prompts LOCKED, **generate PENDING (sesi baru)** — generate is a separate session per the author-all-then-generate workflow.

---

## 1. Room identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E05 angle)
This block stays identical across ALL E05 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E05_sudutkerja_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "home work corner, urban middle-class family home, small online-business nook, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, low open shelving, lived-in working-family",
  "location": "indoor",
  "time_of_day": "midday",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "home work station, IKEA LINNMON white-stained oak effect tabletop on IKEA ALEX drawer unit, far back wall, centered, all-in-one desktop computer, wide single-piece display, thin bezel, slim central stand, screen off dark neutral, centred on the desk, swivel work chair tucked at it",
    "subject_material": "matte painted plaster walls muted off-white, white-stained oak effect laminate furniture, raw pine open shelving, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Ejiri in Suruga Province', Thirty-Six Views of Mount Fuji, centered above the desk, far back wall",
    "supporting_objects": {
      "desk": "IKEA LINNMON tabletop on IKEA ALEX drawer unit, white-stained oak effect, far back wall, centered, all-in-one desktop computer screen off dark neutral, slim wireless keyboard, mouse, before the display, short order notebook, plain ceramic mug, small desk lamp switched off, otherwise uncluttered",
      "chair": "IKEA-style swivel work chair, plain dark mesh back, plain pale seat, tucked at the desk",
      "shelf": "IKEA IVAR raw pine open shelving unit, camera-RIGHT wall, plain unbranded brown cardboard parcel boxes stacked, clear packing tape roll, kraft bubble-wrap roll, flat folded flyer stack, otherwise tidy",
      "rug": "small plain flat-weave grey low-pile rug, on the open ceramic floor, before the desk",
      "window_dressing": "IKEA LILL white sheer net curtains, far back wall, camera-right of the desk",
      "plant": "small potted leafy green plant, plain terracotta pot, camera-LEFT corner, on the floor",
      "openings": "open doorway, camera-LEFT wall, light switch plate beside the doorway",
      "lighting_fixture": "plain ceiling lamp switched off, small desk lamp on the desk, switched off",
      "wall_hook": "modest wall hook, camera-LEFT wall, beside the doorway, plain cloth tote bag"
    },
    "human_absence_signal": "unoccupied, still, chair tucked in, screen dark, room empty, quiet"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```
**Canonical layout (defined by master, reused by all angles — directions are FROM THE MASTER CAMERA's point of view):** LINNMON-on-ALEX work desk centered on the far BACK wall + all-in-one desktop (screen OFF) + swivel chair + small desk lamp, the LILL-curtained window on the far BACK wall to the desk's camera-RIGHT, framed Hokusai *Ejiri in Suruga Province* print centered above the desk · IVAR raw-pine open shelf on the camera-RIGHT wall holding plain unbranded brown cardboard parcel boxes + packing tape + bubble-wrap roll + folded flyer stack (the UMKM packing signal that ties to dapur E04) · open doorway + light switch + wall hook (plain cloth tote) on the camera-LEFT wall (Ratna's entry path) · a small potted plant in the camera-LEFT floor corner · a small flat-weave rug on the open floor before the desk. **Furniture lines the perimeter; the centre floor stays clear** so the room reads as a normal home work nook and leaves a clean approach to the desk.

**ADDENDUM A1:** ONE device appears, OFF — the all-in-one desktop on the work desk (the SEQ3-SC08 bank-virtual-branch / video-call screen). In every plate the screen renders OFF / dark / neutral. All UI (digital waiting-room + "Bicara dengan petugas" button, bank officer video feed via `F3 petugasbank`, pulled transaction history, "Pembiayaan UMKM" card, "Diproses" status) is composited in After Effects.

**Modesty / wardrobe note:** Ratna's apron + hijab are GATE B wardrobe layers, NOT baked into this empty-room plate. The wall hook carries a plain cloth tote (neutral), never the apron.

---

## 2. Method (per [[00-README-ENV]] §2.6)
- **Master generated first, no reference-image.** The MEJA derivative uploads `E05_sudutkerja_master.png` as reference + rewrites ONLY the `shot` block → same room, new camera. (Generate happens in a separate session per the author-all-then-generate workflow; at authoring time the derivative only carries the `environment_reference` token.)
- **Same house as E01/E02/E03:** inherits the §3 architecture/material anchor (matte plaster, IKEA flat-pack laminate, plain desaturated textiles, ceramic-tiled floor). UMKM home-office dressing (LINNMON+ALEX work desk + IVAR pine packing shelf + parcel boxes + all-in-one) differentiates function without breaking the house gestalt.
- **Branded furniture lock-anchors** keep furniture identical across angles — LINNMON+ALEX desk (distinct silhouette from E02's MICKE adult desk + E03's PÅHL child desk) + IVAR raw-pine open shelf (distinct from E03's white KALLAX) + LILL curtains = house-register IKEA pieces named for strong prior.
- **All-in-one desktop, screen OFF** — a wide single-piece display on a slim stand (strong distinctive silhouette, melt-safe per the keterangan); UI in AE. One device only.
- **Fourth distinct named artwork** — Hokusai *Ejiri in Suruga Province* (E01 = Great Wave, E02 = Red Fuji, E03 = Kajikazawa); same *Thirty-Six Views* register, a compositionally distinct image (travellers, wind) so the four rooms stay individually recognizable (§2.6(7) single-work rule). Swappable at Session-B revision if Erik prefers another.
- **No religious / strong-identity label** in `scene` — devotion-free room; class + concrete UMKM objects carry the read (`lessons` b.51 keyword-leak).
- **Token-per-token values** — no conjunctions inside JSON token values (b.119); comma-delimited clusters only. Negation ban absolute.
- ADDENDUM A1: zero graphics, screen off. Neutral grade (warm at GATE B).

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` SEQ3-SC08 shot-list)
Each cell is a COMPLETE copy-paste-ready prompt, zero scaffold. §1 is the canonical identity-lock; the cells are what you paste. Scoped to E05's two plates: MASTER (establishing MW, serves SH01) · MEJA (desk-station MS, serves SH02/SH03/SH04/SH05 — both the 50mm mediums and the 85mm screen inserts crop into it). The MEJA derivative uploads `E05_sudutkerja_master.png` as reference-image at generate time.

### Cell M — MASTER · establishing MW → `E05_sudutkerja_master.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Full room geography — the anchor plate. Establishes desk-on-back-wall + all-in-one, packing shelf camera-RIGHT, doorway camera-LEFT.
```json
{
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "home work corner, urban middle-class family home, small online-business nook, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, low open shelving, lived-in working-family",
  "location": "indoor",
  "time_of_day": "midday",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "home work station, IKEA LINNMON white-stained oak effect tabletop on IKEA ALEX drawer unit, far back wall, centered, all-in-one desktop computer, wide single-piece display, thin bezel, slim central stand, screen off dark neutral, centred on the desk, swivel work chair tucked at it",
    "subject_material": "matte painted plaster walls muted off-white, white-stained oak effect laminate furniture, raw pine open shelving, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Ejiri in Suruga Province', Thirty-Six Views of Mount Fuji, centered above the desk, far back wall",
    "supporting_objects": {
      "desk": "IKEA LINNMON tabletop on IKEA ALEX drawer unit, white-stained oak effect, far back wall, centered, all-in-one desktop computer screen off dark neutral, slim wireless keyboard, mouse, before the display, short order notebook, plain ceramic mug, small desk lamp switched off, otherwise uncluttered",
      "chair": "IKEA-style swivel work chair, plain dark mesh back, plain pale seat, tucked at the desk",
      "shelf": "IKEA IVAR raw pine open shelving unit, camera-RIGHT wall, plain unbranded brown cardboard parcel boxes stacked, clear packing tape roll, kraft bubble-wrap roll, flat folded flyer stack, otherwise tidy",
      "rug": "small plain flat-weave grey low-pile rug, on the open ceramic floor, before the desk",
      "window_dressing": "IKEA LILL white sheer net curtains, far back wall, camera-right of the desk",
      "plant": "small potted leafy green plant, plain terracotta pot, camera-LEFT corner, on the floor",
      "openings": "open doorway, camera-LEFT wall, light switch plate beside the doorway",
      "lighting_fixture": "plain ceiling lamp switched off, small desk lamp on the desk, switched off",
      "wall_hook": "modest wall hook, camera-LEFT wall, beside the doorway, plain cloth tote bag"
    },
    "human_absence_signal": "unoccupied, still, chair tucked in, screen dark, room empty, quiet"
  },
  "shot": {
    "composition": "full room geography, one frame, LINNMON-on-ALEX work desk, all-in-one screen off, framed Hokusai Ejiri above the desk, far back wall, curtained window camera-right of the desk, IVAR pine packing shelf, camera-RIGHT wall, parcel boxes, open doorway, light switch, camera-LEFT wall, potted plant camera-left floor corner, small rug, open floor centre, legible",
    "framing": "MWS establishing, floor visible bottom 20%, ceiling line visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "front of room, looking toward far back window wall, packing-shelf wall camera-right, doorway wall camera-left",
    "camera_direction": "straight down the room, desk, Hokusai Ejiri, window, far back wall, packing shelf camera-right, doorway camera-left, open floor centre",
    "camera": "28mm prime spherical, deep focus front to back",
    "lighting": "soft diffused midday daylight key from the curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```

### Cell MEJA — DESK / work-station MS → `E05_sudutkerja_meja.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Serves SEQ3-SC08-SH03/SH05 (M Ratna at the all-in-one, 50mm) + provides the background for the SH02/SH04 CU screen inserts (85mm crop into the same all-in-one). The desk station at a seated adult's height, all-in-one the focal mid-ground, screen OFF (UI in AE).
```json
{
  "environment_reference": "attached reference plate E05_sudutkerja_master.png, same home work corner, identical furniture, identical layout, identical materials, single Hokusai Ejiri print, faithful room match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "home work corner, urban middle-class family home, small online-business nook, IKEA-style flat-pack laminate furniture, matte painted plaster walls, plain desaturated textiles, low open shelving, lived-in working-family",
  "location": "indoor",
  "time_of_day": "midday",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "home work station, IKEA LINNMON white-stained oak effect tabletop on IKEA ALEX drawer unit, far back wall, centered, all-in-one desktop computer, wide single-piece display, thin bezel, slim central stand, screen off dark neutral, centred on the desk, swivel work chair tucked at it",
    "subject_material": "matte painted plaster walls muted off-white, white-stained oak effect laminate furniture, raw pine open shelving, plain desaturated woven textiles, ceramic-tiled floor",
    "wall_art": "single dark-wood-framed woodblock print, Katsushika Hokusai 'Ejiri in Suruga Province', Thirty-Six Views of Mount Fuji, centered above the desk, far back wall",
    "supporting_objects": {
      "desk": "IKEA LINNMON tabletop on IKEA ALEX drawer unit, white-stained oak effect, far back wall, centered, all-in-one desktop computer screen off dark neutral, slim wireless keyboard, mouse, before the display, short order notebook, plain ceramic mug, small desk lamp switched off, otherwise uncluttered",
      "chair": "IKEA-style swivel work chair, plain dark mesh back, plain pale seat, tucked at the desk",
      "shelf": "IKEA IVAR raw pine open shelving unit, camera-RIGHT wall, plain unbranded brown cardboard parcel boxes stacked, clear packing tape roll, kraft bubble-wrap roll, flat folded flyer stack, otherwise tidy",
      "rug": "small plain flat-weave grey low-pile rug, on the open ceramic floor, before the desk",
      "window_dressing": "IKEA LILL white sheer net curtains, far back wall, camera-right of the desk",
      "plant": "small potted leafy green plant, plain terracotta pot, camera-LEFT corner, on the floor",
      "openings": "open doorway, camera-LEFT wall, light switch plate beside the doorway",
      "lighting_fixture": "small desk lamp on the desk, switched off",
      "wall_hook": "modest wall hook, camera-LEFT wall, beside the doorway, plain cloth tote bag"
    },
    "human_absence_signal": "unoccupied, still, chair tucked in, screen dark, room empty, quiet"
  },
  "shot": {
    "composition": "medium framing on the work desk station, LINNMON-on-ALEX desk, all-in-one screen off dark neutral, dominant centre, swivel chair tucked at the desk, framed Hokusai Ejiri above the desk, curtained window camera-right behind, sliver of IVAR packing shelf, camera-RIGHT edge, compressed back wall",
    "framing": "MS, desk station fills frame, seated adult height, room compressed behind",
    "angle": "eye-level, seated adult height",
    "camera_position": "in front of the desk, pushed in from establishing wide, seated adult height",
    "camera_direction": "toward the desk, all-in-one screen, framed Hokusai Ejiri, curtained window, far back wall",
    "camera": "50mm prime spherical, deep focus front to back",
    "lighting": "soft diffused midday daylight key from the curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```

---

## 4. Status manifest
| Cell | Angle | File | Serves | Status |
|---|---|---|---|---|
| M | establishing MW | `E05_sudutkerja_master.png` | SC08-SH01 | ✅ prompt LOCKED · generate PENDING (sesi baru) |
| MEJA | desk-station MS (+ screen-insert bg) | `E05_sudutkerja_meja.png` | SC08-SH02/03/04/05 | ✅ prompt LOCKED · generate PENDING (sesi baru) |

Storage: `environment-images/E05_sudutkerja/` (+ `_rejected/`). Naming: `E05_sudutkerja_<angle>.png`.
Generate M first (no reference-image). Then MEJA via the `shot`-only-rewrite method: upload `E05_sudutkerja_master.png` as reference + paste §1 verbatim + the cell's `shot` block. Verify each prop against the master image before locking. All-in-one screen renders OFF/polos (A1); UI in After Effects.

---

*E05 Sudut Kerja Ratna environment sheet — Fase-2 prompts LOCKED (generate PENDING, sesi baru) · Explainer Video 2 · 2026-07-01 · INT same house E01–E03 (UMKM home-office nook, distinct from E02/E04/E15) · fourth distinct Hokusai (Ejiri) · all-in-one screen-OFF (A1) · token-per-token · camera-relative direction.*
