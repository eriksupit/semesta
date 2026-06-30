---
title: Environment Sheet — E05 Sudut Kerja Ratna (frozen-food kitchen-adjacent) · GATE 0-ENV
tags: [explainer-video-2, environment-sheet, e05-sudutkerja, gate-0-env, interior, frozen-food]
status: fase2-prompt-locked
created: 2026-06-30
updated: 2026-07-01
aliases: [ev2-e05-sudutkerja, E05-sudutkerja, sudut-kerja-ratna-env, dapur-frozen-food-ratna]
---

# Environment Sheet — E05 SUDUT KERJA RATNA · tag E05
> Method, scoped-angle rubric, 3 anchors, prompt-structure standard → [[00-README-ENV]] (§2.6 = prompt structure). Scene truth → [[03-scene-detail]] (SEQ3-SC08). Shotlist → `10-gateB-keyframes/SEQ3-SC08.md`. Furniture lock-anchors → [[tokens-references/INTERIOR-DESIGN-REFERENCE]] §6.
> **Room:** Ratna's home **frozen-food micro-business work corner** — a kitchen-adjacent production + admin nook where she runs her frozen-food UMKM and (SEQ3-SC08) opens a bank's virtual branch on a **tablet on a stand** + video-calls a bank officer (SC08-SH01 MW establishing, SH02/SH04 CU tablet-screen insert, SH03/SH05 M Ratna at the prep worktable). 1× use. **Same house as E01/E02/E03** — inherits the §3 architecture anchor + material gestalt (matte plaster, IKEA flat-pack laminate, plain desaturated textiles, ceramic floor), here pushed toward a working home-kitchen-production register (stainless prep surfaces, chest freezers). Distinct from E02 (ruang-keluarga **desktop** — Ratna's fixed computer lives there) + E15 (depan-rumah EXT, box-van courier pickup). Empty-room reference plates, neutral grade; warm grade + practical light + Ratna (berhijab, bercelemek) added at GATE B keyframes.

> **Token discipline (locked):** every JSON token value below is a comma-delimited token cluster, NOT a sentence — conjunctions (`and / for / with / bearing`) and prose connectors are banned inside token values (`prompt-rules` b.119). Surrounding markdown is documentation, not pasted into the generator. **Fase-2 status:** prompts LOCKED, **generate PENDING (sesi baru)**.
> **Frozen-food equipment grounded in research (2026-07-01, browsed not guessed):** medium-scale Indonesian frozen-food UMKM (Rp15–50jt) inventory — chest freezer(s) ~500L (often >1 = scale signal), stainless prep table, vacuum sealer + hand sealer + food-grade pouches, digital scale, stove/stockpot/steamer, stainless storage rack, sink, food-grade tubs. Sources: fimela, ukmindonesia, posy.co.id, jayaagungmesin, pusatmesinpacking, mufdana, cmcsolution, wix.

---

## 1. Room identity lock (FIXED — paste verbatim into the `shot`-only-rewrite of every E05 angle)
This block stays identical across ALL E05 angles. Derivatives rewrite ONLY the `shot` block (§3) and upload `E05_sudutkerja_master.png` as the reference-image.
```json
{
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "home frozen-food micro-business work corner, urban middle-class family home, kitchen-adjacent production nook, IKEA-style flat-pack laminate furniture, stainless steel prep surfaces, chest freezers, matte painted plaster walls, ceramic wall splashback, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "midday",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "home frozen-food work corner, stainless steel prep worktable, far back wall, centered, slim tablet on a small angled tablet stand, screen off dark neutral, on the worktable, one white lid-top chest freezer, camera-RIGHT, plain stool tucked at the worktable",
    "subject_material": "matte painted plaster walls muted off-white, white ceramic splashback tiles, brushed stainless steel surfaces, white chest-freezer enamel, raw pine open shelving, food-grade translucent plastic, ceramic-tiled floor, plain desaturated woven textiles",
    "supporting_objects": {
      "prep_table": "stainless steel prep worktable, far back wall, centered, slim tablet on a small angled stand, screen off dark neutral, tabletop vacuum sealer machine, hand impulse sealer, roll of clear food-grade vacuum pouches, small digital kitchen scale, stainless mixing bowl, short order notebook, working frozen-food prep station",
      "freezers": "one white lid-top chest freezer, camera-RIGHT wall, lid closed, plain enamel, frozen-food storage",
      "cook_counter": "short tiled cook counter, camera-LEFT wall, two-burner gas stove, large stainless stockpot, stacked steamer pot, otherwise tidy",
      "wall_rack": "brushed stainless steel wall rack, above the prep worktable, far back wall, food-grade translucent plastic tubs stacked, lidded containers, sealed labeled vacuum pouches, neat",
      "fulfillment_shelf": "IKEA IVAR raw pine open shelving unit, camera-RIGHT wall, plain unbranded brown cardboard parcel boxes, several stacked, several sealed labeled ready-to-ship, packing tape dispenser, bundled flyers, small pile of sealed labeled parcels on the floor below the unit camera-RIGHT, working fulfillment stock",
      "sink": "small stainless steel sink, camera-LEFT wall, plain mixer tap, ceramic splashback tiles over it",
      "rug": "small plain flat-weave grey low-pile rug, on the open ceramic floor, before the prep worktable",
      "window_dressing": "IKEA LILL white sheer net curtains, far back wall, camera-right of the prep worktable",
      "openings": "open doorway, camera-LEFT wall, light switch plate beside the doorway",
      "lighting_fixture": "plain ceiling lamp switched off, slim under-shelf strip light switched off",
      "wall_hook": "modest wall hook, camera-LEFT wall, beside the doorway, plain cloth tote bag"
    },
    "human_absence_signal": "unoccupied, still, stool tucked in, tablet screen dark, freezer lid closed, room empty, quiet"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```
**Canonical layout (defined by master, reused by all angles — directions are FROM THE MASTER CAMERA's point of view):** the **stainless prep worktable** centered on the far BACK wall (the SC08 work surface) carrying the **tablet-on-stand** (screen OFF, the bank-virtual-branch / video-call device) + vacuum sealer + hand sealer + pouch roll + digital scale + mixing bowl, a **brushed-stainless wall rack** above it holding stacked food-grade tubs + sealed pouches, the LILL-curtained window on the far BACK wall to the worktable's camera-RIGHT · **camera-RIGHT wall** = the storage/dispatch side — **a white lid-top chest freezer** + the IVAR raw-pine fulfillment shelf with sealed labeled ready-to-ship parcels + packing materials + a small parcel pile on the floor below it · **camera-LEFT wall** = the wet/prep + entry side — a short tiled cook counter (two-burner stove + stockpot + steamer), a small stainless sink, the open doorway + light switch + wall hook (plain cloth tote, Ratna's entry path) · ceramic-tiled floor, a small rug before the prep worktable, centre floor clear. **NO framed wall art** — the back wall is a plain ceramic-tiled kitchen splashback (Erik 2026-07-01: drop the print so E05 reads distinctly from E01/E02/E03/E06). The equipment lines the perimeter; the centre floor stays clear so the room reads as a *working home frozen-food production + admin corner*, not a styled showroom/living-room.

**ADDENDUM A1:** ONE active device appears, OFF — the **tablet on its stand** on the prep worktable (the SEQ3-SC08 bank-virtual-branch / video-call screen). In every plate the tablet screen renders OFF / dark / neutral, propped on the stand (a stable surface for the SH02/SH04 CU screen-inserts). All UI (digital waiting-room + "Bicara dengan petugas" button, bank officer video feed via `F3 petugasbank`, pulled transaction history, "Pembiayaan UMKM" card, "Diproses" status) is composited in After Effects. Chest-freezer / appliance forms are generic, no brand logo (anti-melt).

**Modesty / wardrobe note:** Ratna's apron + hijab are GATE B wardrobe layers, NOT baked into this empty-room plate. The wall hook carries a plain cloth tote (neutral), never the apron.

---

## 2. Method (per [[00-README-ENV]] §2.6)
- **Master generated first, no reference-image.** The MEJA derivative uploads `E05_sudutkerja_master.png` as reference + rewrites ONLY the `shot` block → same room, new camera. (At authoring time the derivative only carries the `environment_reference` token; the file is attached at generate time.)
- **Same house as E01/E02/E03**, register pushed to a working home-kitchen-production corner (stainless prep + chest freezers) — differentiates function without breaking the house gestalt (matte plaster, IKEA flat-pack, ceramic floor remain).
- **NO computer here** (Erik 2026-07-01): Ratna's fixed desktop lives in E02 ruang-keluarga (`03:49/54`); at this work corner she uses a **tablet on a stand** (mobile device, matches SC04/SC10 tablet usage). SC08 canon updated all-in-one → tablet in `03`.
- **NO framed artwork** (Erik 2026-07-01): drop the Hokusai print so E05 reads distinctly; back wall = plain ceramic splashback. E05 EXITS the Hokusai allocation (E01 Great Wave · E02 Red Fuji · E03 Kajikazawa · E06 Black Fuji remain).
- **Frozen-food equipment = researched, not guessed** (browsed 2026-07-01): chest freezer(s) + stainless prep table + vacuum sealer + hand sealer + food-grade pouches + digital scale + stove/stockpot/steamer + stainless wall rack + sink + food-grade tubs. Curated for plate legibility + melt-safety (generic forms, no logos).
- **Token-per-token values** — no conjunctions inside JSON token values (b.119); comma-delimited clusters only. Negation ban absolute. Camera-relative direction (camera-LEFT/RIGHT), no abstract left/right.
- ADDENDUM A1: zero graphics, tablet screen off. Neutral grade (warm at GATE B).

---

## 3. Plate matrix — full prompts per angle (scoped-angle, per `03` SEQ3-SC08 shot-list)
Each cell is a COMPLETE copy-paste-ready prompt, zero scaffold. §1 is the canonical identity-lock; the cells are what you paste. Scoped to E05's two plates: MASTER (establishing MW, serves SH01) · MEJA (prep-worktable MS, serves SH02/SH03/SH04/SH05 — both the 50mm mediums and the 85mm tablet-screen inserts crop into it). The MEJA derivative uploads `E05_sudutkerja_master.png` as reference-image at generate time.

### Cell M — MASTER · establishing MW → `E05_sudutkerja_master.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Full room geography — the anchor plate. Establishes prep-worktable + tablet on the back wall, two chest freezers + fulfillment shelf camera-RIGHT, cook counter + sink + doorway camera-LEFT.
```json
{
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "home frozen-food micro-business work corner, urban middle-class family home, kitchen-adjacent production nook, IKEA-style flat-pack laminate furniture, stainless steel prep surfaces, chest freezers, matte painted plaster walls, ceramic wall splashback, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "midday",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "home frozen-food work corner, stainless steel prep worktable, far back wall, centered, slim tablet on a small angled tablet stand, screen off dark neutral, on the worktable, one white lid-top chest freezer, camera-RIGHT, plain stool tucked at the worktable",
    "subject_material": "matte painted plaster walls muted off-white, white ceramic splashback tiles, brushed stainless steel surfaces, white chest-freezer enamel, raw pine open shelving, food-grade translucent plastic, ceramic-tiled floor, plain desaturated woven textiles",
    "supporting_objects": {
      "prep_table": "stainless steel prep worktable, far back wall, centered, slim tablet on a small angled stand, screen off dark neutral, tabletop vacuum sealer machine, hand impulse sealer, roll of clear food-grade vacuum pouches, small digital kitchen scale, stainless mixing bowl, short order notebook, working frozen-food prep station",
      "freezers": "one white lid-top chest freezer, camera-RIGHT wall, lid closed, plain enamel, frozen-food storage",
      "cook_counter": "short tiled cook counter, camera-LEFT wall, two-burner gas stove, large stainless stockpot, stacked steamer pot, otherwise tidy",
      "wall_rack": "brushed stainless steel wall rack, above the prep worktable, far back wall, food-grade translucent plastic tubs stacked, lidded containers, sealed labeled vacuum pouches, neat",
      "fulfillment_shelf": "IKEA IVAR raw pine open shelving unit, camera-RIGHT wall, plain unbranded brown cardboard parcel boxes, several stacked, several sealed labeled ready-to-ship, packing tape dispenser, bundled flyers, small pile of sealed labeled parcels on the floor below the unit camera-RIGHT, working fulfillment stock",
      "sink": "small stainless steel sink, camera-LEFT wall, plain mixer tap, ceramic splashback tiles over it",
      "rug": "small plain flat-weave grey low-pile rug, on the open ceramic floor, before the prep worktable",
      "window_dressing": "IKEA LILL white sheer net curtains, far back wall, camera-right of the prep worktable",
      "openings": "open doorway, camera-LEFT wall, light switch plate beside the doorway",
      "lighting_fixture": "plain ceiling lamp switched off, slim under-shelf strip light switched off",
      "wall_hook": "modest wall hook, camera-LEFT wall, beside the doorway, plain cloth tote bag"
    },
    "human_absence_signal": "unoccupied, still, stool tucked in, tablet screen dark, freezer lid closed, room empty, quiet"
  },
  "shot": {
    "composition": "full room geography, one frame, stainless prep worktable, tablet on a stand screen off, brushed-stainless wall rack above, plain ceramic-tiled splashback back wall, curtained window camera-right of the worktable, one white lid-top chest freezer, camera-RIGHT wall, IVAR pine fulfillment shelf camera-RIGHT, ready-to-ship parcels, short tiled cook counter, stove, stockpot, camera-LEFT wall, stainless sink, open doorway, light switch, camera-LEFT wall, small rug, open floor centre, working frozen-food corner read, legible",
    "framing": "MWS establishing, floor visible bottom 20%, ceiling line visible top",
    "angle": "eye-level slight low angle",
    "camera_position": "front of room, looking toward far back splashback wall, freezer-shelf wall camera-right, cook-counter doorway wall camera-left",
    "camera_direction": "straight down the room, prep worktable, tablet, wall rack, window, far back wall, chest freezer, fulfillment shelf camera-right, cook counter, sink, doorway camera-left, open floor centre",
    "camera": "28mm prime spherical, deep focus front to back",
    "lighting": "soft diffused midday daylight key from the curtained window wall, soft ambient bounce fill, even matte rendering",
    "aspect_ratio": "16:9"
  },
  "production_designer": "Eugenio Caballero", "production_design_style": "Roma-style middle-class domestic realism, class-accurate dressing",
  "interior_designer": "Ilse Crawford", "interior_design_style": "warm human-centred tactile lived-in, unpretentious frugal materiality"
}
```

### Cell MEJA — PREP WORKTABLE / work-station MS → `E05_sudutkerja_meja.png` · ✅ prompt LOCKED · generate PENDING (sesi baru)
Serves SEQ3-SC08-SH03/SH05 (M Ratna at the prep worktable, 50mm) + provides the background for the SH02/SH04 CU tablet-screen inserts (85mm crop into the same tablet-on-stand). The prep station at a seated/standing adult's height, the tablet-on-stand the focal mid-ground, screen OFF (UI in AE).
```json
{
  "environment_reference": "attached reference plate E05_sudutkerja_master.png, same home frozen-food work corner, identical equipment, identical layout, identical materials, plain ceramic splashback back wall, faithful room match, new camera per shot block only",
  "mood": "neutral reference clarity, calm empty domestic stillness",
  "color_grade": "neutral true-to-life color, balanced white-point",
  "style": "photorealistic interior reference plate, architectural photography clarity, ARRI Alexa Mini LF, clean prime spherical lens, Kodak Portra rendering",
  "scene": "home frozen-food micro-business work corner, urban middle-class family home, kitchen-adjacent production nook, IKEA-style flat-pack laminate furniture, stainless steel prep surfaces, chest freezers, matte painted plaster walls, ceramic wall splashback, plain desaturated textiles, lived-in working-family",
  "location": "indoor",
  "time_of_day": "midday",
  "atmosphere": "quiet lived-in domestic calm",
  "subject_anchor": {
    "primary_subject": "home frozen-food work corner, stainless steel prep worktable, far back wall, centered, slim tablet on a small angled tablet stand, screen off dark neutral, on the worktable, one white lid-top chest freezer, camera-RIGHT, plain stool tucked at the worktable",
    "subject_material": "matte painted plaster walls muted off-white, white ceramic splashback tiles, brushed stainless steel surfaces, white chest-freezer enamel, raw pine open shelving, food-grade translucent plastic, ceramic-tiled floor, plain desaturated woven textiles",
    "supporting_objects": {
      "prep_table": "stainless steel prep worktable, far back wall, centered, slim tablet on a small angled stand, screen off dark neutral, tabletop vacuum sealer machine, hand impulse sealer, roll of clear food-grade vacuum pouches, small digital kitchen scale, stainless mixing bowl, short order notebook, working frozen-food prep station",
      "freezers": "one white lid-top chest freezer, camera-RIGHT wall, lid closed, plain enamel, frozen-food storage",
      "cook_counter": "short tiled cook counter, camera-LEFT wall, two-burner gas stove, large stainless stockpot, stacked steamer pot, otherwise tidy",
      "wall_rack": "brushed stainless steel wall rack, above the prep worktable, far back wall, food-grade translucent plastic tubs stacked, lidded containers, sealed labeled vacuum pouches, neat",
      "fulfillment_shelf": "IKEA IVAR raw pine open shelving unit, camera-RIGHT wall, plain unbranded brown cardboard parcel boxes, several stacked, several sealed labeled ready-to-ship, packing tape dispenser, bundled flyers, small pile of sealed labeled parcels on the floor below the unit camera-RIGHT, working fulfillment stock",
      "sink": "small stainless steel sink, camera-LEFT wall, plain mixer tap, ceramic splashback tiles over it",
      "rug": "small plain flat-weave grey low-pile rug, on the open ceramic floor, before the prep worktable",
      "window_dressing": "IKEA LILL white sheer net curtains, far back wall, camera-right of the prep worktable",
      "openings": "open doorway, camera-LEFT wall, light switch plate beside the doorway",
      "lighting_fixture": "plain ceiling lamp switched off, slim under-shelf strip light switched off",
      "wall_hook": "modest wall hook, camera-LEFT wall, beside the doorway, plain cloth tote bag"
    },
    "human_absence_signal": "unoccupied, still, stool tucked in, tablet screen dark, freezer lid closed, room empty, quiet"
  },
  "shot": {
    "composition": "medium framing on the prep worktable station, stainless prep worktable, tablet on a stand screen off dark neutral, dominant centre, vacuum sealer, digital scale, mixing bowl, plain stool tucked at the worktable, brushed-stainless wall rack above, plain ceramic splashback back wall, curtained window camera-right behind, sliver of chest freezer, camera-RIGHT edge, compressed back wall",
    "framing": "MS, prep station fills frame, seated standing adult height, room compressed behind",
    "angle": "eye-level, adult working height",
    "camera_position": "in front of the prep worktable, pushed in from establishing wide, adult working height",
    "camera_direction": "toward the prep worktable, tablet on its stand, wall rack, curtained window, far back wall",
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
| M | establishing MW | `E05_sudutkerja_master.png` | SC08-SH01 | ✅ DONE — accepted `E05_sudutkerja_master.png` (frozen-food kitchen-adjacent: chest freezer + stainless prep + tablet-on-stand OFF, no computer, no print, neutral grade; v1 sterile + v2 office-no-kitchen rejected → `_rejected/`). Render = ONE freezer (spec reconciled 2→1). |
| MEJA | prep-worktable MS (+ tablet-screen insert bg) | `E05_sudutkerja_meja.png` | SC08-SH02/03/04/05 | ✅ DONE — accepted `E05_sudutkerja_meja.png` (consistent push-in of master; vacuum sealer + scale + frozen-food tubs legible; tablet-OFF, neutral grade) |

Storage: `environment-images/E05_sudutkerja/` (+ `_rejected/`). Naming: `E05_sudutkerja_<angle>.png`.
Generate M first (no reference-image). Then MEJA via the `shot`-only-rewrite method: upload `E05_sudutkerja_master.png` as reference + paste §1 verbatim + the cell's `shot` block. Verify each prop against the master image before locking. Tablet screen renders OFF/polos (A1); UI in After Effects. Appliances generic (no logo, anti-melt).

---

*E05 Sudut Kerja Ratna environment sheet — Fase-2 prompts LOCKED (generate PENDING, sesi baru) · Explainer Video 2 · 2026-07-01 · INT same house E01–E03, frozen-food kitchen-adjacent work corner (chest freezers + stainless prep + vacuum sealer, researched equipment) · tablet-on-stand (no computer, computer in E02) · NO framed art (E05 exits Hokusai allocation) · tablet screen-OFF (A1) · token-per-token · camera-relative direction.*
