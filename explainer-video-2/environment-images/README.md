# environment-images/ — GATE 0-ENV reference plates

Empty-room environment reference plates (interior + exterior), parallel to `character-images/`. Used as Kling 3.0 reference-lock + the `scene`/`scene_depth` spatial anchor for GATE B keyframe prompts. Method + registry: `../09-environment-sheet/00-README-ENV.md`.

## Convention
- One subfolder per environment: `E<NN>_<slug>/` (e.g. `E01_kamar/`).
- Plate file names: `E<NN>_<slug>_<angle>.png` — angles: `master` (establishing wide), `bed3q`/`reverse`/`corner`/`detail`/etc. as scoped to that env's `03` shot-list.
- Rejected generations go to `E<NN>_<slug>/_rejected/`.
- Only plates that pass GATE 0-ENV review (geometry, dressing, continuity, neutral grade) are kept at the top level.

## Locked rules (see 00-README-ENV)
- Empty room, NO characters (composited later from `character-images/`).
- Neutral true-to-life grade (warm video grade applied at keyframe, not baked).
- ADDENDUM A1: zero graphics; device screens off/neutral.
- Three mandatory anchors per prompt: owner social class + international brand register + international interior-designer pair (Caballero + Ilse Crawford for the home).

## Registry (14 env)
E01_kamar · E02_ruangkeluarga · E03_ruangbelajar · E04_dapur · E05_sudutkerja · E06_ruangmakan · E07_gerbangwarung · E08_kantor · E09_kafe · E10_ruangkreator · E11_balaiwarga · E12_ekskul · E13_terminal · E14_warung
