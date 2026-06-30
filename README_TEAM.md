# README_TEAM — Explainer Video "Satu Keluarga, Satu Hari Penuh"
**Production handover for the image → image-to-video team.**
Last updated: 2026-07-01 · Status: **all prompts authored; image generation in progress (plates partial, keyframes pending).**

This document is the single entry point for the team that will: (a) generate the still images from the locked prompts, (b) feed each shot's start/end image pair into image-to-video, (c) composite graphics/UI in After Effects, and (d) assemble the film. It tells you what exists, where it lives, the rules that must not be broken, and what is still to do.

All paths are relative to the repo root (`/`). The explainer-video work lives under `explainer-video-2/`.

---

## 1. Main story (scene details)

The film follows **one family — Herman (father), Ratna (mother), Lisa (eldest, university student), Andi (son, age 10)** — across **one full day**: Subuh → Pagi → Siang → Sore → Senja → Malam. Each scene shows the superapp serving a different need (devotion, commerce, logistics, work, study, wellbeing, banking, health, government, fitness, transit) **at fair, equal terms for anyone**, and the film closes on **family warmth at the dinner table** — the app going quiet at the call to Isya prayer ("Bersih Saat Sakral"). The thesis: *technology as a tool (wasilah) that knows when to serve and when to step back; humans hold control.*

- **Canonical story (full prose, per-scene VO, ad-beat, production notes):** `explainer-video-2/03-scene-detail.md` — **READ THIS FIRST.**
- **13 scenes (SC01–SC13), ~5 shots each = ~65 shots.** Day arc: SEQ1 (SC01 bedroom waking · SC02 dawn prayer) · SEQ2 (SC03 gate+warung · SC04 courier pickup · SC05 office · SC06 study · SC07 campus mentor) · SEQ3 (SC08 bank-as-tenant · SC09 telemedicine) · SEQ4 (SC10 gov-as-tenant + commodity dashboard · SC11 park/fitness) · SEQ5 (SC12 transit terminal) · SEQ6 (SC13 dinner FINALE).

---

## 2. Scene → shot → prompt map (all documented)

Every scene has **two docs** in `explainer-video-2/10-gateB-keyframes/`:
- `SEQ<n>-SC<nn>.md` = **narrative / shot-list** (beats, camera, framing, UI-graphics notes, production notes).
- `Prompt-SEQ<n>-SC<nn>.md` = **the locked GATE-B prompts** (per shot: START full prompt + END edit-in-place + attachment list + per-scene generate-order + status board).

| Scene | Setting | Narrative doc | **Prompt doc** | Shots | Environment |
|---|---|---|---|---|---|
| SC01 | Kamar (waking, subuh) | `…/SEQ1-SC01.md` | `…/Prompt-SEQ1-SC01.md` | 5 | E01 ✅ |
| SC02 | Ruang keluarga (sholat subuh) | `…/SEQ1-SC02.md` | `…/Prompt-SEQ1-SC02.md` | 5 | E02 ✅ |
| SC03 | Gerbang + warung (EXT) | `…/SEQ2-SC03.md` | `…/Prompt-SEQ2-SC03.md` | 5 | E07 ⏳ |
| SC04 | Depan rumah + kurir (EXT/INT) | `…/SEQ2-SC04.md` | `…/Prompt-SEQ2-SC04.md` | 5 | E15 ⏳ |
| SC05 | Kantor (pagi) | `…/SEQ2-SC05.md` | `…/Prompt-SEQ2-SC05.md` | 5 | E08 ⏳ |
| SC06 | Ruang belajar | `…/SEQ2-SC06.md` | `…/Prompt-SEQ2-SC06.md` | 5 | E03 ✅ |
| SC07 | Selasar kampus (mentor) | `…/SEQ2-SC07.md` | `…/Prompt-SEQ2-SC07.md` | 5 | E09 ⏳ |
| SC08 | Sudut kerja (bank) | `…/SEQ3-SC08.md` | `…/Prompt-SEQ3-SC08.md` | 5 | E05 ✅ |
| SC09 | Selasar kampus (telemedicine) | `…/SEQ3-SC09.md` | `…/Prompt-SEQ3-SC09.md` | 5 | E09 ⏳ |
| SC10 | Kantor (sore + dashboard) | `…/SEQ4-SC10.md` | `…/Prompt-SEQ4-SC10.md` | 5 | E08 ⏳ |
| SC11 | Taman kota (fitness) | `…/SEQ4-SC11.md` | `…/Prompt-SEQ4-SC11.md` | 5 | E16 ⏳ |
| SC12 | Terminal (senja, OOH) | `…/SEQ5-SC12.md` | `…/Prompt-SEQ5-SC12.md` | 5 | E13 ⏳ |
| SC13 | Ruang makan (FINALE) | `…/SEQ6-SC13.md` | `…/Prompt-SEQ6-SC13.md` | 5 | E06 ✅ |

✅ = environment plate(s) already generated · ⏳ = environment plate(s) still to generate (see §5).
`…` = `explainer-video-2/10-gateB-keyframes/`.

---

## 3. Shot principles (locked — do not deviate)

These are the rules baked into every prompt. The canonical method docs are at the bottom of this section.

**A. Each shot = a START/END keyframe PAIR.** Every shot produces **two stills**: a START frame and an END frame. They are the in/out endpoints of one image-to-video segment.

**B. Camera-lock between START and END.** Within a shot, **camera angle + framing are IDENTICAL** in start and end (camera-move = none). **Only the subject changes** (a gesture, gaze, pose, or one motivated practical such as a lamp turning on). Never change the angle/framing between start and end; never have a subject "pop-in" at END (present them in START), and never have a subject/vehicle walk or drive out of frame (that needs a moving camera → breaks the lock). Locomotion scenes are staged as **beat-pauses** (subject paused, motion implied), not traverses across frame.

**C. START = full prompt; END = edit-in-place.** The START is a complete from-scratch prompt (the "master"). The END is produced by **editing the accepted START render** (small token delta + an "everything-else unchanged" lock-list), NOT by re-generating from scratch — this keeps the camera locked. Re-generating an END from the plates alone causes drift.

**D. Master-parent for angles.** Within a scene, the establishing shot is the visual master; other shots reuse its space via the environment plate. A genuinely new camera angle clones the master's prompt and swaps the angle reference — it is not invented from zero.

**E. Framing ladder (W → M → CU alternating).** Each scene alternates shot sizes cut-to-cut (wide / medium / close-up) so the edit stays dynamic even though the camera is static. Each `Prompt-…` doc states its scene's ladder.

**F. Plates are NEUTRAL; the look is in the keyframe.** Environment + character reference plates are rendered at a neutral grade with screens OFF. The **warm/dusk/golden grade, practical lighting, and time-of-day mood are applied at the keyframe (GATE-B) prompt**, not in the plate.

**G. ADDENDUM A1 — every screen is OFF / plain; ALL graphics are After Effects.** Phones, tablets, monitors, the office wall dashboard, and the giant OOH terminal display all render as **plain/neutral/off slabs**. Every UI element — app screens, notifications, ad cards, dashboards, the "Jawaban Tepat ⭐" badge, the "Mode Syariah" opt-in, OOH ads — is composited in **After Effects**, NOT generated and NOT in the image-to-video. (Hands/objects may occlude a screen in-frame; that is fine.)

**H. Brand-safety + content constraints (hard rules):**
- **No coal / extractive glorification.** The SC10 commodity dashboard (AE) shows sector/mineral/nickel-downstream only — never coal.
- **Modesty (mahram axis):** Ratna is uncovered only in mahram-only home moments (SC01, SC06, SC13); she wears a headscarf in public or when a non-mahram sees her via camera (SC04, SC08, SC11). Mukena for prayer (SC02). Cross-gender non-mahram help uses **non-touch gestures** (SC12: a nod + cupped hands, polite distance). Touch only between same-gender or mahram.
- **Named public-domain artwork:** only E01 (Great Wave), E02 (Red Fuji), E03 (Kajikazawa) carry a Hokusai print; E05/E06 and all exteriors are print-free.
- **Token discipline** is already audited in every prompt (comma-delimited clusters, no negation, no motion verbs, camera-relative directions).

**Canonical method docs (consult before changing any prompt):**
`prompt-rules-image-generation.md` · `prompt-rules-text-image-to-image.md` · `explainer-video-2/06-konvensi-naratif.md` · `explainer-video-2/PROMPT-AUDIT-CHECKLIST.md`.

---

## 4. Keyframe images — NOT yet generated

**No final keyframe stills exist yet.** All 13 `Prompt-…` docs are authored and audit-clean, but the start/end images for the ~65 shots are still to be generated (this is the next production phase).

- **Target storage for keyframe stills:** `explainer-video-2/scene-images/sc<NN>/sc<NN>_sh<NN>_{start,end}.png` (e.g. `scene-images/sc01/sc01_sh01_start.png`).
- `scene-images/sc01/` and `sc02/` contain **old renders from an earlier 4-shot structure — SUPERSEDED.** Do not reuse; regenerate from the current `Prompt-…` docs.
- **Each `Prompt-…` doc's status board + per-shot attachment list tells you exactly which plates to attach** for that shot.

---

## 5. Character prompts + images

**Prompts:** all character reference-plate prompts are authored in `explainer-video-2/08-character-sheet/` (`H-herman.md`, `R-ratna.md`, `L-lisa.md`, `A-andi.md`, `F-figurans.md`, method in `00-README.md`).
**Image storage:** `explainer-video-2/character-images/<TAG>/`.

| Character | Sheet | Image dir | Plates | Status |
|---|---|---|---|---|
| Herman | `H-herman.md` | `character-images/H_herman/` | 12 | ✅ done |
| Ratna | `R-ratna.md` | `character-images/R_ratna/` | 17 (incl. hijab) | ✅ done |
| Lisa | `L-lisa.md` | `character-images/L_lisa/` | 12 | ✅ done |
| Andi | `A-andi.md` | `character-images/A_andi/` | 12 | ✅ done |
| Darto (warung) | `F-figurans.md` | `character-images/F_darto/` | 3 | ✅ done |
| Rian (rekan kantor) | `F-figurans.md` | `character-images/F_rian/` | 3 | ✅ done |
| Petugas bank | `F-figurans.md` | `character-images/F_petugasbank/` | 3 | ✅ done |
| Tika / Pembina | `F-figurans.md` | `character-images/F_tika`, `F_pembina/` | 2 / 3 | ✅ done |
| **F6 ojek** | `F-figurans.md` | `character-images/F_ojek/` | 0 | ⏳ **pending** |
| **F7 kurir** | `F-figurans.md` | `character-images/F_kurir/` | 0 | ⏳ **pending** |
| **F8 mentor** | `F-figurans.md` | `character-images/F_mentor/` | 0 | ⏳ **pending** |
| **F9 ibu petugas** | `F-figurans.md` | `character-images/F_ibupetugas/` | 0 | ⏳ **pending** (verify rendered **aged ~55**, not de-aged) |
| **F10 bapak desa** | `F-figurans.md` | `character-images/F_bapakdesa/` | 0 | ⏳ **pending** (verify rendered **aged ~62**) |

Each figuran plate set = `front_full` + `front_medium` (studio-isolated, no attachment).

---

## 6. Environment prompts + images

**Prompts:** all environment reference-plate prompts are authored in `explainer-video-2/09-environment-sheet/` (one `E<nn>-<name>.md` per location; method in `00-README-ENV.md`).
**Image storage:** `explainer-video-2/environment-images/E<nn>_<name>/`.

| Env | Sheet | Image dir | Plates on disk | Status |
|---|---|---|---|---|
| E01 kamar | `E01-kamar.md` | `E01_kamar/` | master, bed3q, bed4q, nightstand | ✅ done |
| E02 ruang keluarga | `E02-ruangkeluarga.md` | `E02_ruangkeluarga/` | master, screen, reverse, reverse_prayer, reverse_prayer_subuh, +2 | ✅ done |
| E03 ruang belajar | `E03-ruangbelajar.md` | `E03_ruangbelajar/` | master, desk, doorway, tablet | ✅ done |
| E05 sudut kerja | `E05-sudutkerja.md` | `E05_sudutkerja/` | master, meja | ✅ done |
| E06 ruang makan | `E06-ruangmakan.md` | `E06_ruangmakan/` | master | ✅ done (MEJA cell dropped — frame off master) |
| **E07 gerbang + warung** | `E07-gerbangwarung.md` | `E07_gerbangwarung/` | 0 | ⏳ **pending** (M, WAR, GTE) |
| **E08 kantor** | `E08-kantor.md` | `E08_kantor/` | 0 | ⏳ **pending** (M, MEJA, DASBOR) |
| **E09 selasar kampus** | `E09-selasarkampus.md` | `E09_selasarkampus/` | 0 | ⏳ **pending** (M, BANGKU, BANGKU2) |
| **E13 terminal** | `E13-terminal.md` | `E13_terminal/` | 0 | ⏳ **pending** (M, PERON) |
| **E15 depan rumah** | `E15-depanrumah.md` | `E15_depanrumah/` | 0 | ⏳ **pending** (M, PINTU) |
| **E16 taman kota** | `E16-tamankota.md` | `E16_tamankota/` | 0 | ⏳ **pending** (M, JALUR) |

Per env: generate the **MASTER first (no reference image)**, accept it, then each derivative uploads the accepted master as the reference and rewrites only its camera. Plates render at neutral grade, screens off.

---

# 7. [RECOMMENDED ADDITIONS — what else the team needs] *(my proposal; trim if you disagree)*

These are NOT in your 6 points but are required for the team to take this end-to-end to image-to-video + assembly without coming back to ask.

### 7.1 Production order (critical dependency)
The pipeline is **plate → keyframe → image-to-video → After Effects → assemble**, and within image generation the order is strict:
1. **Generate the pending plates first** (the ⏳ env + figuran above). A keyframe cannot reference-lock a plate that doesn't exist yet.
2. **Then generate the keyframe pairs** (START full prompt → accept → END edit-in-place on the accepted START).
3. Each `Prompt-…` doc states its own intra-scene generate-order (e.g. SC01: SH04 before SH05 because SH05 matches SH04's grade).

### 7.2 Two images per shot are the segment endpoints
Each shot's **START image and END image are the first and last frame** the image-to-video step interpolates between. Author/accept them as a matched pair: same camera, subject-only delta (§3-B). (How the i2v tool is driven is your call — not specified here.)

### 7.3 After Effects is a separate, mandatory layer
Every screen renders blank; **all UI, ad cards, dashboards, notifications, OOH content, supers, and the per-scene graphic beats are added in AE** after image-to-video. The narrative docs (`SEQ…` "Grafis UI (AE)" lines) specify each graphic + its copy text. Plan AE time for all 13 scenes; SC13 carries the film's **last** commercial graphic ("Mode Syariah" opt-in), after which graphics go to zero.

### 7.4 Audio / VO (not image, but part of the deliverable)
Each scene's narrative doc carries its **VO line** (single calm male voice) where one exists, plus diegetic audio cues (e.g. the **azan Isya** in SC13, call-to-prayer reminder in SC01). The opening/closing VO bookend the film. The team needs these for the final mix even though they are out of image scope.

### 7.5 Format + runtime
All frames are **16:9**. Target ~5 seconds per shot → ~65 shots ≈ a 5–6 minute film. Audience = **ad providers** (the film is a sales tool demonstrating brand-safe ad inventory across verticals).

### 7.6 Naming + accept/reject workflow
- Plates: `E<nn>_<name>_<angle>.png` / `F_<name>_<view>.png` in their image dirs; rejects go to a `_rejected/` subfolder.
- Keyframes: `sc<NN>_sh<NN>_{start,end}.png` in `scene-images/sc<NN>/`.
- Verify each render against its prompt's checklist before accepting (geometry, screens-off, neutral plate grade, identity match, aged figurans, modesty).

### 7.7 Scenes closest to "ready to shoot now"
All plates already on disk for: **SC01, SC02, SC06, SC08, SC13** (env + characters done). These can be keyframed immediately. The other 8 scenes wait on their ⏳ plates.

### 7.8 Hardest shots (stage carefully)
4-subject WIDE frames (SC02 saf, SC13 finale) and rear-view group frames are the most failure-prone in image generation; the prompts mitigate via rear plates + baked prayer mats, but expect extra rolls.

---

## 8. Progress snapshot (2026-07-01)

| Layer | State |
|---|---|
| Story (GATE A) | ✅ complete (13 scenes) |
| Shot breakdown (GATE A2) | ✅ complete (65 shots) |
| Character plate prompts | ✅ complete |
| Environment plate prompts | ✅ complete |
| **Keyframe (GATE B) prompts** | ✅ **complete — all 13 scenes, ~130 start/end prompts, audited** |
| Character plate images | 🟡 core cast done; **5 figurans pending** (F6–F10) |
| Environment plate images | 🟡 E01/E02/E03/E05/E06 done; **6 envs pending** (E07/E08/E09/E13/E15/E16) |
| Keyframe images | 🔴 **not started** (next phase) |
| Image-to-video | 🔴 not started |
| After Effects graphics | 🔴 not started |
| Assembly + audio mix | 🔴 not started |

**Next action for the team:** generate the pending plates (§5, §6) → generate keyframe pairs from the `Prompt-…` docs → image-to-video → AE → assemble.

---

*Maintained alongside the project governance (`scope.md`, `context.md`, `lessons.md`). Questions about a specific shot: open that scene's `Prompt-SEQ<n>-SC<nn>.md` — it is self-contained (prompt + attachments + generate-order + status).*
