Purpose & context
Erik is building "Semesta Digital" (working title, final name pending investor/stakeholder approval) — an integrated-marketplace superapp for the Indonesian market. Core differentiators: a fairness engine as the central operating principle, NU as a visual-only co-founder (strict no-verbal-mention policy; visual representation only), and a syariah opt-in mode. The project spans four verticals: goods marketplace, virtual office, financial trading, and education/masterclass channels.
Immediate production goal: an investor deck requiring 18 cinematic illustrations (S0–S17) generated via ChatGPT/GPT Image 2. Parallel asset: a 5-minute explainer video functioning as a sales tool for ad providers (logic chain: video → ad provider sees traffic potential → approaches brands → brands fund pre-development). The explainer video is hybrid AI scenes + live actor, featuring 7 characters.
Erik communicates in informal Bahasa Indonesia; all vault documents are written in English. Communication style is terse — "approve," "kunci," "go," "oke" mean full green-light, execute immediately, no re-confirmation needed.

Current state

Illustration pipeline: 14 of 17 scenes approved (S0–S12 + S12b — updated 2026-06-10 Sesi 12). Deck grew to 17 scenes (S12b = ADDED: elder pausing for worship, sharia opt-in / values-aware feature; companion to S12). S15 (post-production composite) and S16 (typography only) are SKIPPED. Deck illustrations COMPLETE: 19/19 (S0–S14 + S12b + S14b + S17 + S17b). S17b = female mirror closer of S17 (M/F bookend). Lesson: a companion scene's super must REINFORCE, not duplicate, its pair's super (S17 = structure "One Ecosystem./One Set of Rules for Everyone"; S17b = human payoff "A Place for Everyone./Belonging by Design"). S15/S16 removed from deck (video-only beats, video docs untouched). Claude Design handoff DONE (2026-06-10): handoff/HANDOFF-CLAUDE-DESIGN-2026-06-10.md (upload via "Upload a doc") + handoff/INITIAL-PROMPT-CLAUDE-DESIGN-2026-06-10.txt (paste in chat). Adapted to the Claude Design UI: it cannot read a filesystem, so the handoff is self-contained and uses a dual-key image manifest (filename + content description) for the 19 attachments — zero filepath references. Special tasks baked in: S6 Rp 340.000 card composite, optional ecosystem montage from the 7 character images, S16 as native typography, financials only from the operator's uploaded copy doc. Deck illustration project COMPLETE (19/19) + handoff ready. S14b approved (17/18): added hijabi-ibu culinary-for-business scene filling the middle-aged-hijabi representation gap (grep confirmed zero hijab before); new rule — a device screen facing the subject (back to camera) must NOT embed UI; show its content as a FLOATING screen-preview card. Deck grew to 18 scenes (ADDED S12b + S14b). After S17 → 18/18 → Claude Design handoff. S14 approved (16/17): corporate two-person wall-display interaction, finger on large screen clean, negations removed, garment specified, off-axis added. S13 approved: turn-back portrait + active pose + flipped subject-right/graphic-left, because slight off-center alone does NOT break presenter monotony — vary angle+pose+side together. After all approved → Claude Design handoff (PNGs + Section 1–4 of 08). Key new rules locked this session: (1) unspecified visible garment + ethnic token → model auto-fills batik; specify every garment affirmatively, correct by specification not negation (validated S12 A/B). (2) Two graphics in one frame is valid — diegetic ID push-notification banner + English investor frosted card — if you differ the visual TYPE and separate positions (validated S12b); never two twin frosted cards. (3) Abstract/devotional meaning must not rest 100% on text — add a non-text visual cue. S12b naskah added to 06-storyline.md (Beat 2b). S10 lesson: large screen + finger-on-screen is safe from hand-melt (inverse of small-phone S6); Teknik 3 embedded dashboard + Teknik 2 floating card both legible on one large monitor; "two people reading the same screen" = strong B2B interaction. S11 lesson: presenter full-body validated in a populated open operations floor — "rebuild solo workspace → populated professional floor" (S5/S7) pattern holds; every presenter scene must use a different populated room. S12 pre-patched: dead-center→off-axis low-angle OTS, tablet face-grid softened to avoid melt. DECK TONE STANDARD (locked): every color_grade = `cool midtones desaturated, cool-dominant zero amber push`; all ungenerated prompts already rolled to it. Super/graphic text must be UNIQUE per scene (no duplicates). Always verify a scene's APPROVED marker against the actual PNG in `rough-presentation-image/` — text markers can go stale.
Workflow: Erik generates images externally in ChatGPT/GPT Image 2 and uploads results; Claude writes, iterates, and approves prompts. Approved images are moved to explainer-video/rough-presentation-image/.
Session bootstrap: Read scope.md → context.md → lessons.md → latest HANDOFF-*.md before any response. Next session initial prompt: handoff/INITIAL-PROMPT-2026-06-10-S10.txt (latest authoritative handoff).
Active living documents: prompt-rules-image-generation.md (root vault, single source of truth for all prompt rules) and explainer-video/08-investor-deck-brief.md (Section 5 contains all 18 prompts, currently at v1.4+).


On the horizon

Complete S5–S17 illustrations; all 18 approved images become the asset base for a Claude Design session to build the full presentation deck.
Final project name confirmation pending investor/stakeholder input.
RAB platform AI totaling ~$1,214 USD: Midjourney Pro, Kling Premier, Runway, Seedance/fal.ai, Suno, Claude Max 20x, ChatGPT Pro, Gemma 4/OpenRouter — all paid tiers.


Key learnings & principles

Image model spatial logic: Models read spatial positioning like CSS/compositing logic, not human directional language. Floating UI overlays require CSS-style tokens (center-x aligned, pixel offsets, dimensions, z-index) — not "above/below/left/right."
Culturally specific labels fail in image models: Terms like "Nahdliyin" are not recognized; replace with concrete facial/body feature descriptions and broad ethnic anchors (Javanese commoner, Sundanese, mixed urban Indonesian).
BANNED prompt tokens: "amber-ochre shadows," terracotta wardrobe, "HD makeup"/"HD setting powder" (triggers high-contrast specular highlights/oiliness drift). Yellow tone drift caused by warm shadow + warm wardrobe combinations.
Negation tokens are prohibited in all prompts — token strings only, no negations.
Angle anti-cliché: for live-actor full-body scenes, never use "subject centered frame" + eye-level (standard presenter look). Push subject to right/left-third, camera low to one side, let the environment recede on a diagonal as leading lines (validated S3).
Color-grade one-temperature rule: never combine two midtones-temperature tokens in one color_grade — a warm token ("slightly warmer midtones") plus "cool-dominant zero amber push" lets warm win and the frame goes golden (S3 iteration-1). Pick ONE; for night/indoor-warm-practical scenes match S2 exactly: "cool midtones desaturated, cool-dominant zero amber push".
Cross-scene tone consistency is judged by comparing directly against the previously-approved PNG, not per-scene in isolation.
No confabulation in vault writes: append-not-overwrite, specificity over generality, negative lessons treated as first-class entries.
Filesystem MCP write reliability: str_replace fails silently on non-ASCII characters (em-dashes, special quotes). Reliable pattern: read_file full content → rebuild complete file → write_file entire file → verify with read_text_file using head parameter.
Binary files cannot be written via Filesystem MCP write_file (string-only). Binary delivery requires present_files for manual download.
Bash tool runs in cloud container, not on the Mac filesystem — writes via bash_tool do not reach the vault. Only Filesystem MCP write_file reliably writes to the Mac.
Session memory is continuous, not end-of-session: validated preferences, corrections, and new insights must be written to vault immediately, never deferred.
Seedance 2.0: technically superior but requires fal.ai third-party API wrapper for real human face workflows. oMLX: rejected for this project (requires local model storage + minimum 16GB unified memory, MacBook spec unconfirmed). Gemma 4: vision-language model (text output only), functions as prompt reasoning layer feeding Midjourney — not a text-to-image generator.


Approach & patterns

Single recommendation + one approval gate: never offer option menus; always close with one clear recommendation and one approval trigger.
Defensible over optimistic: budget figures and claims must be defensible, not optimistic.
Prompt standard — 6-layer architecture (defined in prompt-rules-image-generation.md):

Layer 1: mood / color_grade / style
Layer 2: scene / location / time_of_day / atmosphere
Layer 3: character_identity + character_style — FIXED
Layer 4: action / pose / gesture / expression — VARIABLE
Layer 5: graphic (optional; floating UI uses on_screen_graphic + graphic_proximity with CSS-style tokens)
Layer 6: framing / camera / lighting + 6 crew pairs (director, lighting_director, production_designer, interior_designer, costume_designer, makeup_artist)
Format: token strings, no negations, C2 adjective-dense


Character briefs: structured JSON with explicit fields for face, body, clothing, environment, palette, style modifiers.
Session close protocol: every session must produce a handoff document + initial prompt in handoff/, and update context.md, scope.md, lessons.md, Superapp — Home.md.
/session-anchors skill: governs all reads/writes to the four memory anchor files. Protocol A = READ at session open; Protocol B = WRITE continuously on any validated preference/correction/insight; Protocol C = FULL CLOSE with handoff + initial-prompt artifacts. Co-invokes /confidence, /anti-sycophancy, /brave, /research-before-dispatch.


Tools & resources

Obsidian vault: /Users/eriksupit/Desktop/superapps/ — single source of truth, connected via Filesystem MCP

Superapp — Home.md (hub)
knowledge-base/ (Executive Brief, Ikhtisar Naratif, Proyeksi NU)
explainer-video/ (00-charter, 01-concept, 02-production-brief, 03-rab, 04-pipeline-ai-production, 08-investor-deck-brief, rough-presentation-image/)
handoff/ (HANDOFF-.md and INITIAL-PROMPT-.txt artifacts)
raw-kb/
context.md, scope.md, lessons.md (root)
prompt-rules-image-generation.md (root)
.claude/skills/session-anchors/SKILL.md


Image generation: ChatGPT Pro / GPT Image 2 (primary illustration pipeline)
AI video: Kling Premier, Runway Gen-4.5, Seedance 2.0 via fal.ai
Prompt reasoning layer: Gemma 4 via OpenRouter
Music: Suno AI
Primary AI assistant: Claude Max 20x
PDF generation: ReportLab (Python, bash environment); output to /mnt/user-data/outputs/
Filesystem access fallback: when MCP connector is inactive, upload files directly (accessible at /mnt/user-data/uploads/[filename])