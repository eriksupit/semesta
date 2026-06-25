---
title: Attachment Production Backlog — Environment & Character Plates
tags: [explainer-video-2, production, attachment, environment, character, plate, backlog, gate0]
status: active
created: 2026-06-25
updated: 2026-06-25
aliases: [plate-backlog, attachment-backlog, generate-list]
---

# Attachment Production Backlog — Environment & Character Plates

Definitive, shot-driven generate-list for the **attachment plates** (environment + character) that every scene keyframe will reference. Derived from `03-scene-detail.md` (19 scenes / 56 shots) cross-checked against on-disk assets. Governed by **`../prompt-rules-text-image-to-image.md`**: a MASTER is generated from-scratch (Mode A, via `../prompt-rules-image-generation.md` 6-layer); every derivative/orientation is generated with the master attached (Mode B/C).

## Locked decisions (this backlog assumes them)
- **Angle coverage = shot-list-driven, NOT 360.** Generate only the camera orientations the scenes actually film. (Replaces the retracted "360 for spatial understanding" premise.)
- **One master per room = the consistency/identity anchor** (primary establishing wide, eye-level, straight/orthographic). A second "sub-master" only for an opposing orientation the master cannot show.
- **Character plate standard = FULL-BODY + CLOSE-UP, multi-angle. MEDIUM dropped** (archived, not deleted). Orientation set is shot-driven (front / profileA=camera-left / profileB=camera-right).
- **Plate = identity anchor (who/what), not composition anchor (where).** Figure placement in a keyframe still follows subject-count (≤1 face-locked + softened) + coordinates + iterative-build.
- **SEQ1-SC02 subuh prayer = shot FACING the camera (faces visible)** — locks the covered-prayer plates (peci/mukena) AND makes the 4-face qiyam (SH03) the prime test of Rule 8a iterative-build.

## Status legend
✅ exists & accepted · ♻️ exists but REGEN · ⬜ to generate

---

## Production order (story order — no skipping)
1. **Attachments first, by dependency** (just-in-time per scene is fine): regen E01 master (straight) → env masters → derivatives → character plates (covered-prayer + figuran), produced as the current scene needs them.
2. **Keyframes in STORY ORDER from SEQ1-SC01**, filling the 3-mode skeletons in `10-gateB-keyframes/`. Per-shot cycle: author (mode A/B/C + manifest) → user generates → review (REVIEW-CHECKLIST G0–G6 + 8 criteria) → ACCEPT → rename `scene-images/sc<NN>/sc<NN>_sh<MM>_{start,end}.png` + write the proven prompt into the scene-file slot.
3. **The `03-scene-detail.md` scene order IS the production order.** Never jump ahead. SEQ1-SC01 (single subject) validates Mode A/B/C + camera-lock cheaply; the iterative-build (Rule 8a) test then falls naturally at SEQ1-SC02 (scene 2) — no need to jump to it.
4. Note: SEQ1-SC01 has 8 old-method renders in `scene-images/sc01/` (archive; prompts were cleared as non-compliant) — decide reuse vs re-render with the user when authoring SC01.

## ENVIRONMENT PLATES (14 rooms → 41-plate final set; 27 to generate)

| Env | Room | Scenes (orientations driven by) | Plates | To gen |
|---|---|---|---|---|
| **E01** | Kamar Herman | SEQ1-SC01, SEQ6-SC03 | ♻️ master (oblique→regen straight) · ✅ bed3q · ✅ nightstand · ✅ wallart_reverse | **1** |
| **E02** | Ruang keluarga | SEQ1-SC02, SEQ6-SC02 | ✅ master · ✅ screen · ✅ reverse · ✅ reverse_prayer · ✅ reverse_prayer_subuh · ✅ prayer_high · ✅ floorseat | **0** |
| **E03** | Ruang belajar | SEQ2-SC03 | ✅ master · ✅ desk · ✅ doorway · ✅ tablet | **0** |
| **E04** | Dapur Ratna | SEQ3-SC01 (live-selling) | ⬜ master (kitchen establishing) · ⬜ work-counter (MS + OTS packing) | **2** |
| **E05** | Sudut kerja Ratna | SEQ3-SC02 (bank tenant) | ⬜ master (work corner + box stacks) · ⬜ OTS-to-screen | **2** |
| **E06** | Ruang makan | SEQ6-SC01 | ⬜ master (dining establishing WS, family of four) | **1** |
| **E07** | Gerbang + warung Darto (EXT) | SEQ2-SC01 | ⬜ master (gate + pos satpam + street) · ⬜ warung storefront (MS Darto) | **2** |
| **E08** | Kantor ekspor-impor | SEQ2-SC02 + SEQ3-SC03 + SEQ4-SC01 (3 scenes, 8 shots) | ⬜ master (office + route-map wall) · ⬜ Herman-desk frontal · ⬜ OTS-to-monitor · ⬜ two-person MS | **4** |
| **E09** | Kafe | SEQ2-SC04 | ⬜ master (cafe + window table) · ⬜ OTS-to-laptop · ⬜ Lisa-facing reverse (MCU recording) | **3** |
| **E10** | Ruang kreator | SEQ3-SC04 + SEQ4-SC02 | ⬜ master (toward screen-wall + seating) · ⬜ sub-master reverse (toward audience) · ⬜ seating MS · ⬜ OTS-to-device | **4** |
| **E11** | Balai warga | SEQ4-SC03 | ⬜ master (hall + chair circle) · ⬜ two-person MS (in circle) | **2** |
| **E12** | Ruang ekskul | SEQ4-SC04 | ⬜ master (room establishing / MWS) · ⬜ group-table MS | **2** |
| **E13** | Terminal TransJakarta | SEQ5-SC01 | ⬜ master (concourse + OOH wall) · ⬜ tap-gate · ⬜ platform/peron (overhead OOH) | **3** |
| **E14** | Warung kelontong (EXT) | SEQ5-SC02 | ⬜ master (storefront, evening) | **1** |

**Env totals:** exists 14 · regen 1 · new 26 · **to generate = 27** · final set = 41.

**Flags:** E08 SEQ4-SC01 (sore/orange) reuses E08 geometry — warmth at keyframe, no new plate. E10 may need a per-scene re-dressed master if workshop vs masterclass dressing differs materially (resolve at authoring). E14 add 1 reverse derivative if SH03 reads as a true reverse onto the owner behind the counter.

---

## CHARACTER PLATES (new full+closeup standard; ~14 core to generate)

### Main characters
| Char | Scenes | Reuse | ⬜ Generate (full+closeup unless noted) |
|---|---|---|---|
| **Herman** (50) | SEQ1-SC01/02, SEQ2-SC02, SEQ3-SC03, SEQ4-SC01, SEQ6-SC01/03 | front full+closeup · profileA full+closeup | **peci front full+closeup (2)** |
| **Ratna** (45, hijabi) | SEQ1-SC02, SEQ2-SC03, SEQ3-SC01/02, SEQ4-SC03, SEQ5-SC02, SEQ6-SC01/02 | uncovered front full+closeup (anchor) · hijab_front_closeup | **hijab_front_full (1, missing on disk) · mukena front full+closeup (2)** |
| **Lisa** (20) | SEQ2-SC01/04, SEQ3-SC04, SEQ4-SC02, SEQ5-SC01, SEQ6-SC01, (thin SEQ1-SC02 saf) | front full+closeup | **mukena front full (+closeup optional) (2)** |
| **Andi** (10) | SEQ2-SC03, SEQ4-SC04, SEQ6-SC01/02, (thin SEQ1-SC02 saf) | front full+closeup | **peci front full+closeup (2)** |

Mains: every shot is frontal except Herman SEQ1-SC01-SH04 (profileA, side-of-bed). ProfileB unused → archive. All `_medium` archived. **Mains to generate = 9.**

### Figurans (appear only MS/OTS/CU — no full-body; closeup anchors + roster gaps)
| Figuran | Scenes | Reuse | ⬜ Generate |
|---|---|---|---|
| Pak Darto (warung) | SEQ2-SC01 | front_full | **front_closeup (1)** |
| Tika (helper) | SEQ3-SC01 | front_medium | **front_closeup (1)** (full never shown) |
| Petugas bank | SEQ3-SC02 (video-call bust) | front_closeup | 0 |
| Rian (kolega) | SEQ3-SC03 (side-peek) | front_closeup | **profileA closeup (1)** |
| Pembina muda | SEQ4-SC04 (MWS) | front_full | closeup optional |
| **Petugas instansi** (gov, video-call) | SEQ4-SC01 | — (roster gap) | **front_closeup (1)** |
| **Pemilik warung kelontong** | SEQ5-SC02 | — (roster gap) | **front_closeup (1)** |

Figurans core to generate = 5 (Darto, Tika, Rian, petugas instansi, pemilik warung).
**No face plate needed (back/OTS/crowd):** office colleague (SEQ2-SC02 / SEQ4-SC01 OTS), SUV neighbor (SEQ2-SC01-SH03, behind glass), and all generic crowds (UMKM workshop, koperasi ibu senior, terminal crowd, ekskul friends).

**Character totals:** core to generate = **14** (mains 9 + figurans 5); optional +2 (Lisa mukena closeup, pembina closeup). Archive: all `_medium` (~14) + mains' profileB sets.

---

## PRODUCTION ORDER (critical)
1. **Validate Rule 8a iterative-build EARLY**, on the SEQ1-SC02 qiyam saf (4 faces toward camera) — it is the hardest frame and the only safe path is build-by-single-figure-addition. If iterative-build fails here, learn it BEFORE 40+ other plates are produced.
2. Then complete the env masters (foundational anchors) → derivatives → covered-prayer character plates.
3. Only after the attachment library is complete: author scene keyframes (master+derivative pattern, 3-mode grammar).

## Open production decisions (provisional calls — correct if wrong)
- Andi wears peci also in SEQ6-SC02 ngaji (recommended: yes → covered by the peci plates already listed).
- E10 re-dressed master if dressing differs; E14 reverse derivative if SH03 is a true reverse.

## Changelog
- **2026-06-25** — Backlog created from `03-scene-detail.md` shot-mapping (two parallel mapping agents, Priority-1). Prayer-camera-side decision = faces toward camera (locks covered-prayer plates + makes SH03 the Rule 8a test). Env 27 to generate / 41 final; characters ~14 core. Governed by `../prompt-rules-text-image-to-image.md`.
