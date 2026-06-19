---
title: AI Production Pipeline — Video Explainer Semesta Digital (working title)
tags: [explainer-video, pipeline, production, ai-workflow]
status: draft-v1
created: 2026-06-08
updated: 2026-06-17
aliases: [pipeline-doc, ai-pipeline]
---

# AI Production Pipeline
## Video Explainer Semesta Digital *(working title)*
*Draft v1.0 · 8 Juni 2026*

---

## Overview

This document is the operational blueprint for the AI-assisted production of the Semesta Digital explainer video. It specifies the exact sequence of tools, decisions, and handoffs from raw concept through final assembly. Every operator and session working on this production must read this document before beginning any generation work.

**Total video duration:** 300 seconds (5 minutes)
**AI-generated content:** 220 seconds (7 characters + cold open)
**Live actor content:** 90 seconds (8 segments)
**Post-production assembly:** 25 seconds (convergence + data segment)

**Reference documents (read before executing any stage):**
- `00-project-charter.md` -- all locked decisions D-006 to D-017
- `01-concept-document.md` -- arc, characters, visual language, exclusion rules
- `02-production-brief.md` -- word-for-word VO scripts and AI scene descriptions per segment
- `03-rab-produksi-ai.md` -- platform budget and credit allocation

---

## Platform Architecture

| Layer | Platform | Role | Access Method |
|---|---|---|---|
| Prompt Reasoning | Gemma 4 26B via OpenRouter | Generate and evaluate Midjourney prompts | Python harness (API) |
| Text-to-Image | Midjourney v8.1 Pro | Generate anchor still images for all characters | Manual -- web UI only |
| Image-to-Video A | Kling AI Premier -- **model 3.0** (draft on 2.6) | Dynamic scenes: characters 2, 3, 5 | Manual -- web UI |
| Image-to-Video B | Runway Gen-4.5 | Consistent-face scenes: characters 1, 4, 6, 7 + cold open | Manual -- web UI |
| Video Fallback | Seedance 2.0 via fal.ai | Backup if Kling/Runway fails after 3 attempts | Python harness (API) |
| Scoring | Suno AI Pro | Music -- three stems matching visual arc | Manual -- web UI |
| LLM | Claude Max 20x | Prompt engineering, script iteration, session continuity | claude.ai |
| LLM | ChatGPT Pro | Creative variation, cross-validation | chat.openai.com |

---

## Critical Platform Constraints

> These constraints are non-negotiable. Violating them risks ToS violation, account ban, or production failure.

**Gemma 4 (OpenRouter):**
- Gemma 4 outputs TEXT ONLY. It is a vision-language model used as a prompt reasoning layer.
- It does NOT generate images. It reads anchor images and outputs structured text prompts.
- Do not describe Gemma 4 as an image generator in any documentation or pitch material.

**Midjourney:**
- There is NO official Midjourney API. All Midjourney operations are manual via web UI at midjourney.com.
- Do not use unofficial API wrappers -- ToS violation, high ban risk.
- Python harness in this pipeline is for Gemma 4 (OpenRouter) and Seedance (fal.ai) only. Midjourney is excluded from automation.
- Stealth Mode must be active throughout production (included in Pro plan).

**Seedance 2.0 via fal.ai:**
- Seedance is FALLBACK ONLY. Do not use as primary platform.
- Access via fal.ai API only -- not Seedance's official channels (real human face content restriction on official CapCut/Volcengine route).
- Activate only after 3 failed attempts on Kling or Runway for a given scene.

---

## Stage 1 -- Pre-Production Setup (One-Time)

### 1.1 Platform Account Verification

Confirm all accounts are active and credits are loaded before any generation begins:

| Platform | Check |
|---|---|
| Midjourney Pro (Stealth Mode ON) | Verify subscription active, Stealth enabled in settings |
| Kling AI Premier | Verify subscription, check credit balance (target: 8,000 credits) |
| Runway Gen-4.5 Max -> Pro sequence | Verify Max subscription active |
| fal.ai account | Verify top-up loaded ($20 minimum), API key obtained |
| OpenRouter account | Verify top-up loaded ($20 minimum), API key obtained |
| Suno AI Pro | Verify subscription active |

### 1.2 Python Harness Setup

Two separate harnesses are required. Both are lightweight scripts (~30-50 lines each).

**Harness A -- Gemma 4 Prompt Reasoner (OpenRouter)**

Purpose: Send scene brief + anchor image -> receive structured Midjourney prompt.

```python
# gemma_prompt_reasoner.py
import requests
import base64
import json

OPENROUTER_API_KEY = "YOUR_KEY_HERE"
MODEL = "google/gemma-4-26b-a4b-it"

def encode_image(image_path):
    with open(image_path, "rb") as f:
        return base64.b64encode(f.read()).decode("utf-8")

def generate_prompt(scene_brief: str, anchor_image_path: str = None):
    messages = []
    user_content = []

    if anchor_image_path:
        user_content.append({
            "type": "image_url",
            "image_url": {
                "url": f"data:image/jpeg;base64,{encode_image(anchor_image_path)}"
            }
        })

    user_content.append({
        "type": "text",
        "text": f"""You are a visual prompt architect for Midjourney v8.1.

Given the following scene brief and reference image (if provided), output a single optimized Midjourney prompt.

Rules:
- Output ONLY the prompt text. No explanation, no preamble.
- Include: subject description, environment, lighting, mood, camera style, aspect ratio.
- Target style: cinematic, realistic, warm color palette (except cold open scenes).
- End with: --ar 16:9 --style raw --v 8.1

Scene brief:
{scene_brief}

Output the Midjourney prompt now:"""
    })

    messages.append({"role": "user", "content": user_content})

    response = requests.post(
        "https://openrouter.ai/api/v1/chat/completions",
        headers={
            "Authorization": f"Bearer {OPENROUTER_API_KEY}",
            "Content-Type": "application/json"
        },
        json={
            "model": MODEL,
            "messages": messages,
            "max_tokens": 500
        }
    )

    result = response.json()
    return result["choices"][0]["message"]["content"].strip()

# Usage:
# prompt = generate_prompt("Indonesian woman 45-55, warm kitchen...", "anchors/char1_ref.jpg")
# print(prompt)
```

**Harness B -- Seedance Fallback (fal.ai)**

Purpose: Submit image-to-video generation request when Kling/Runway fails 3x on a scene.

```python
# seedance_fallback.py
import fal_client
import os

FAL_KEY = "YOUR_FAL_KEY_HERE"
os.environ["FAL_KEY"] = FAL_KEY

def generate_video_fallback(
    image_url: str,
    prompt: str,
    duration: int = 10,
    scene_id: str = "unknown"
):
    print(f"[Seedance Fallback] Submitting scene: {scene_id}")

    result = fal_client.subscribe(
        "fal-ai/seedance-v2",
        arguments={
            "image_url": image_url,
            "prompt": prompt,
            "duration": duration,
            "resolution": "1080p",
            "motion_intensity": "medium"
        },
        with_logs=True
    )

    print(f"[Seedance Fallback] Done. Output: {result['video']['url']}")
    return result["video"]["url"]

# Usage:
# url = generate_video_fallback(
#     image_url="https://...",
#     prompt="Indonesian woman packaging food, warm kitchen light, soft motion...",
#     duration=10,
#     scene_id="K1-shot2"
# )
```

### 1.3 File Organization

Create this folder structure before any generation begins:

```
production/
|-- anchors/
|   |-- char1-ibu/
|   |-- char2-pemuda/
|   |-- char3-kurir/
|   |-- char4-profesional/
|   |-- char5-pengusaha/
|   |-- char6-tokoh/
|   `-- char7-eksekutif/
|-- video-clips/
|   |-- S0-cold-open/
|   |-- S2-char1/
|   |-- S4-char2/
|   |-- S6-char3/
|   |-- S8-char4/
|   |-- S10-char5/
|   |-- S12-char6/
|   `-- S14-char7/
|-- live-actor/          <- from live shoot, not AI
|-- scoring/
|   |-- stem-phase1-cold/
|   |-- stem-phase2-warm/
|   `-- stem-phase3-swell/
|-- assembly/
|   |-- S15-convergence/
|   |-- S16-data-segment/
|   `-- final-cut/
`-- prompts-log/         <- save every Gemma 4 output here
```

---

## Stage 2 -- Character Anchor Image Generation (Midjourney)

Anchor images are the visual foundation for all AI video. Every character must have 4 approved anchor angles before video generation begins.

### 2.1 Workflow Per Character

```
Step 1:  Write scene brief for character (from 02-production-brief.md)
Step 2:  Run Gemma 4 harness -> receive structured Midjourney prompt
Step 3:  Log prompt to prompts-log/char[N]-anchor-prompts.txt
Step 4:  Paste prompt manually into Midjourney web UI
Step 5:  Generate -> evaluate 4 outputs -> select best 1
Step 6:  If none acceptable: refine brief -> repeat from Step 2
Step 7:  Generate 4 angles of approved character: front, 3/4, profile, back-3/4
Step 8:  Save all 4 to anchors/char[N]-[name]/
Step 9:  Run Gemma 4 evaluation: send all 4 images -> check visual consistency
Step 10: If consistency passes -> proceed to video generation
         If consistency fails -> iterate on 1-2 problematic angles only
```

### 2.2 Character Anchor Briefs (Input for Gemma 4)

Feed the following JSON objects as `scene_brief` to `gemma_prompt_reasoner.py`. Each field maps directly to a Midjourney prompt dimension. Gemma 4 will synthesize into a single optimized prompt string.

> **Operator note:** Do NOT simplify these briefs before feeding to Gemma 4. The density is intentional -- Gemma 4 uses the full field set to reason prompt weight and token order.

---

**Character 1 -- Ibu Rumah Tangga (Anchor)**
```json
{
  "role": "anchor character, most screen time, emotional register for entire video",
  "subject": "Indonesian woman",
  "age_range": "45-55",
  "ethnicity_broad": "Javanese commoner",
  "face": {
    "shape": "round to oval, full cheeks, soft jawline",
    "skin": "medium warm brown, sun-touched, not flawless -- lived-in texture",
    "eyes": "dark brown, slightly hooded, crow's feet at corners, warm gaze",
    "nose": "broad, flat bridge, rounded tip",
    "lips": "medium, natural color, unpainted",
    "expression": "privately triumphant -- the quiet smile of someone who just proved something to themselves, not to anyone else"
  },
  "body": {
    "build": "stocky, full-figured, strong hands from manual work",
    "posture": "grounded, no performative straightness -- natural weight-forward stance of someone comfortable in their own space"
  },
  "clothing": {
    "top": "simple printed batik or plain cotton blouse, slightly worn at collar",
    "bottom": "kain jarik or dark cotton skirt",
    "head": "no hijab -- or simple cotton hijab if present, practical not fashion",
    "style": "working clothes, not dressed up, authentic not costumed"
  },
  "environment": {
    "location": "Indonesian home kitchen, lived-in -- not staged",
    "props": "ceramic jars, wooden shelves, handmade food products partially packaged, small gas stove visible in background",
    "light": "warm golden afternoon, single side window, dust motes in light beam"
  },
  "palette": "ochre, warm wood brown, soft amber, faded fabric pattern",
  "style_modifiers": "cinematic, shallow depth of field, realistic, intimate, documentary warmth",
  "aspect": "--ar 16:9 --style raw --v 8.1"
}
```

---

**Character 2 -- Pemuda Komunitas**
```json
{
  "role": "learning and ambition -- generasi muda entering digital economy",
  "subject": "Indonesian young man",
  "age_range": "22-28",
  "ethnicity_broad": "Javanese",
  "face": {
    "shape": "oval, lean, slightly angular jaw",
    "skin": "medium brown, smooth, young but not boyish",
    "eyes": "dark, alert, forward-focused -- someone thinking ahead",
    "nose": "medium, slightly flat bridge",
    "lips": "thin to medium, closed, composed",
    "expression": "focused concentration with a current of restrained ambition -- not smiling, thinking"
  },
  "body": {
    "build": "lean, medium height, upright but not stiff",
    "posture": "slightly forward lean over laptop -- active engagement, not slouch"
  },
  "clothing": {
    "top": "batik kemeja short-sleeve, simple pattern, neatly worn -- not ironed-crisp, lived-in",
    "bottom": "dark trousers or dark jeans",
    "optional": "sarung worn loosely around waist if seated in traditional setting",
    "style": "informal but intentional -- this person made a choice to look presentable"
  },
  "environment": {
    "location": "shaded outdoor area or open veranda of traditional community building",
    "architecture": "weathered wood pillars, clay tile roof edge visible, potted plants",
    "props": "laptop open on low table, glass of tea nearby",
    "light": "dappled natural light through overhead canopy, late afternoon warmth"
  },
  "palette": "deep green, earth brown, warm amber shadow, muted batik pattern",
  "style_modifiers": "cinematic, realistic, warm depth of field, documentary tone",
  "aspect": "--ar 16:9 --style raw --v 8.1"
}
```

---

**Character 3 -- Kurir / Pekerja Logistik**
```json
{
  "role": "dignified labor -- every delivery is a fair transaction",
  "subject": "Indonesian courier, male or female -- operator chooses per shoot plan",
  "age_range": "28-38",
  "ethnicity_broad": "mixed Indonesian urban -- no dominant regional marker",
  "face": {
    "shape": "square to round, weather-exposed skin",
    "skin": "medium to dark brown, sun-darkened, slightly oily -- outdoor worker",
    "eyes": "alert, pragmatic, no-nonsense gaze -- not tired, not performing happiness",
    "nose": "broad, flat",
    "lips": "medium, set in a neutral line -- professional composure",
    "expression": "calm professional focus -- the face of someone doing a job they own, not endure"
  },
  "body": {
    "build": "medium, wiry or sturdy, physically capable -- not gym-built, work-built",
    "posture": "confident upright on motorcycle, weight balanced, helmet tilted back"
  },
  "clothing": {
    "outer": "practical courier jacket, slightly worn, no specific brand visible",
    "helmet": "open-face helmet pushed back on head or chin-strapped loose",
    "gloves": "thin riding gloves, optional",
    "style": "utilitarian, not degraded -- this is a uniform worn with self-respect"
  },
  "environment": {
    "location": "roadside stop, tier-2 Indonesian city street",
    "background": "shophouses, slight traffic blur, afternoon haze",
    "props": "motorcycle with phone holder mount on handlebar, phone showing map",
    "light": "direct warm late afternoon sun, slight lens flare acceptable"
  },
  "palette": "asphalt gray, warm golden city light, dust haze, jacket muted tones",
  "style_modifiers": "cinematic, motion-aware framing, realistic, warm contrast, slightly gritty",
  "aspect": "--ar 16:9 --style raw --v 8.1"
}
```

---

**Character 4 -- Profesional Perempuan Urban**
```json
{
  "role": "knowledge work, virtual office -- competence without performance",
  "subject": "Indonesian professional woman",
  "age_range": "30-40",
  "ethnicity_broad": "Sundanese or mixed urban Indonesian",
  "face": {
    "shape": "oval, defined cheekbones, clean jawline",
    "skin": "medium warm brown, well-maintained, minimal makeup if any",
    "eyes": "bright, sharp, composed -- reading something off-screen with focus",
    "nose": "medium, straight bridge",
    "lips": "medium, natural lip color or minimal gloss",
    "expression": "calm competence -- no need to prove anything, just executing"
  },
  "body": {
    "build": "slim to medium, composed posture -- grounded, not rigid",
    "posture": "upright at desk, slight forward tilt while typing -- active not passive"
  },
  "clothing": {
    "top": "smart casual blouse or blazer -- muted tones: slate, soft teal, warm gray",
    "style": "professional without being corporate -- someone who chose this for herself, not a dress code"
  },
  "environment": {
    "location": "personal home workspace -- not open office",
    "props": "laptop open, small indoor plant beside monitor, a few books on shelf, natural light from window left of frame",
    "light": "clean diffused natural daylight, slightly warm, no harsh shadows"
  },
  "palette": "clean white walls, green plant accent, warm wood desk, cool gray laptop",
  "style_modifiers": "cinematic, sharp focus on face, clean aesthetic, warm naturalistic",
  "aspect": "--ar 16:9 --style raw --v 8.1"
}
```

---

**Character 5 -- Pengusaha Menengah**
```json
{
  "role": "mid-scale business growth -- access without connections",
  "subject": "Indonesian business owner, male or female -- operator chooses per shoot plan",
  "age_range": "35-50",
  "ethnicity_broad": "Chinese-Indonesian or mixed urban Indonesian -- either works",
  "face": {
    "shape": "square or broad oval, slightly thick neck",
    "skin": "medium tan, slightly weathered, pragmatic -- not polished",
    "eyes": "analytical squint, slight crow's feet -- someone who reads numbers",
    "nose": "medium to broad",
    "lips": "medium, closed, brief half-smile of someone seeing their hypothesis confirmed",
    "expression": "quiet analytical satisfaction -- reading a dashboard, recognizing a pattern, allowing one brief nod"
  },
  "body": {
    "build": "medium to stocky, solid, physically grounded -- business-owner body not desk-worker",
    "posture": "standing, weight shifted to one hip, arms loosely crossed or one hand on chin"
  },
  "clothing": {
    "top": "plain batik kemeja long-sleeve or smart casual collared shirt -- no tie",
    "bottom": "dark chinos or trousers",
    "style": "functional authority -- dressed to walk the floor, not sit in a meeting"
  },
  "environment": {
    "location": "warehouse or showroom -- products visible on shelves behind, no readable brand names",
    "props": "large monitor on desk showing simple dashboard, some product packaging nearby",
    "light": "warm industrial -- overhead fluorescent mixed with window, yellow-warm cast"
  },
  "palette": "warm iron gray, wood brown, product packaging colors muted, warm lamp yellow",
  "style_modifiers": "cinematic, slightly wide, realistic, warm industrial texture",
  "aspect": "--ar 16:9 --style raw --v 8.1"
}
```

---

**Character 6 -- Tokoh Komunitas**
```json
{
  "role": "trust and authority earned over decades -- knowledge that multiplies when shared",
  "subject": "Indonesian elder man",
  "age_range": "55-65",
  "ethnicity_broad": "Javanese, rural-origin features",
  "face": {
    "shape": "broad, round, full cheeks softened by age",
    "skin": "dark medium brown, deeply lined -- forehead furrows, deep nasolabial folds, age spots acceptable",
    "eyes": "dark, heavy-lidded, slow and deliberate -- the gaze of someone who has seen enough to speak with weight",
    "nose": "broad, flat, rounded -- wide nostril base",
    "lips": "medium, slightly thickened with age, often closed in a firm but not unkind set",
    "beard_hair": "short white or salt-and-pepper beard acceptable, close-cropped or thinning white hair",
    "expression": "dignified warmth -- the face of an elder who knows he is trusted and holds that responsibility carefully"
  },
  "body": {
    "build": "medium to stocky, slightly hunched at shoulders from age -- not frail, rooted",
    "posture": "seated upright, elbows on knees or one hand resting on tablet -- commanding without effort"
  },
  "clothing": {
    "top": "plain white or off-white long-sleeve shirt under a dark vest or surjan (Javanese traditional jacket)",
    "head": "peci (black or dark velvet Indonesian cap) -- present, worn naturally",
    "style": "traditional daily wear -- this is how he dresses every day, not a costume for the camera"
  },
  "environment": {
    "location": "shaded outdoor area of traditional community building -- pendopo or similar",
    "props": "tablet in hand, wooden chair or low bench, potted plant, weathered wooden structure behind",
    "light": "soft diffused shadow of overhead roof, warm ambient green from surrounding trees"
  },
  "palette": "deep shadow green, ochre earth, white cloth, dark wood, soft warm ambient",
  "style_modifiers": "cinematic, intimate medium shot, realistic, documentary warmth, deep shadow texture",
  "aspect": "--ar 16:9 --style raw --v 8.1"
}
```

---

**Character 7 -- Eksekutif Korporat**
```json
{
  "role": "strategic reach -- the largest scale actor in the ecosystem, but not the most important",
  "subject": "Indonesian corporate executive, male or female -- operator chooses per shoot plan",
  "age_range": "40-55",
  "ethnicity_broad": "mixed urban Indonesian -- cosmopolitan, non-regional",
  "face": {
    "shape": "defined oval or slightly square, clean jaw",
    "skin": "medium warm brown, well-maintained, minimal visible aging -- professional presentation",
    "eyes": "focused, strategic -- reading the map on screen, not looking at camera",
    "nose": "straight medium bridge, refined",
    "lips": "medium, closed, slight upward set -- satisfaction not performance",
    "expression": "strategic satisfaction -- touching a point on a map, watching a system respond, the quiet pleasure of scale working correctly"
  },
  "body": {
    "build": "medium, upright, controlled -- not physically imposing, intellectually present",
    "posture": "standing at wall-mounted TV, one hand extended toward screen -- engaged, not frozen"
  },
  "clothing": {
    "top": "well-fitted collared shirt or smart blazer -- no tie -- muted confident tones: deep navy, charcoal, warm gray",
    "style": "executive casual -- serious without being stiff, modern without being tech-bro"
  },
  "environment": {
    "location": "modern meeting room -- clean, no visible corporate logos",
    "props": "large wall-mounted TV showing Indonesia map with glowing city dots and single large growth number",
    "light": "warm office light, slight warm bounce from wood panel wall"
  },
  "palette": "clean white wall, dark wood accent, warm office ambient, screen blue-green map glow",
  "style_modifiers": "cinematic, professional, warm realistic, slight wide angle to include TV in frame",
  "aspect": "--ar 16:9 --style raw --v 8.1"
}
```

---

### 2.3 Cold Open -- Abstract Visual Stills (Midjourney -> Runway)

```
Abstract digital abstraction: cold blue light, data stream, small white and blue
numbers falling like thin rain (not Matrix-style), notification icons appearing
and disappearing without sender, large glowing screen showing moving numbers and
auto-clicking cursor with no human hand. No faces. No warm light sources.
Color palette: #0A0F1E, #1A2340, #4A9EFF cold neon, #E8EDF5 dim white.
Style: cinematic, slow, unsettling, impersonal. --ar 16:9 --style raw --v 8.1
```

---

## Stage 3 -- AI Video Generation

### 3.1 Platform Assignment by Scene

| Segment | Character | Platform | Rationale |
|---|---|---|---|
| S0 | Cold open (abstract) | Runway Gen-4.5 | High visual control for abstract motion |
| S2 | Char 1 -- Ibu rumah tangga | Runway Gen-4.5 | Anchor consistency -- highest importance, 40 sec |
| S4 | Char 2 -- Pemuda komunitas | Kling AI Premier | Dynamic scene -- laptop interaction, natural motion |
| S6 | Char 3 -- Kurir | Kling AI Premier | Dynamic scene -- motorcycle tracking shot |
| S8 | Char 4 -- Profesional perempuan | Runway Gen-4.5 | Consistent face, workspace intimacy |
| S10 | Char 5 -- Pengusaha menengah | Kling AI Premier | Dynamic -- showroom walk, dashboard interaction |
| S12 | Char 6 -- Tokoh komunitas | Runway Gen-4.5 | Consistent face, authoritative presence |
| S14 | Char 7 -- Eksekutif korporat | Runway Gen-4.5 | Consistent face, final character impression |

### 3.2 Runway Generation Workflow (Scenes: S0, S2, S8, S12, S14)

**Draft phase (Gen-4 Turbo, 50 credits/10 sec):**
```
Step 1: Upload approved anchor image as reference
Step 2: Input scene prompt (from 02-production-brief.md, adapted)
Step 3: Generate draft at Turbo quality
Step 4: Evaluate: motion naturalness, face consistency, mood match
Step 5: If pass -> lock prompt text -> proceed to Final
         If fail -> adjust prompt -> re-draft (max 3 attempts at Turbo)
         If 3x fail -> activate Seedance fallback (see Stage 3.4)
```

**Final phase (Gen-4.5, 250 credits/10 sec):**
```
Step 6:  Use locked prompt from draft phase
Step 7:  Upload same anchor image reference
Step 8:  Generate at Gen-4.5 quality
Step 9:  Evaluate final output: cinematic quality, color consistency, arc match
Step 10: If pass -> save to video-clips/S[N]-char[N]/
          If fail -> one re-attempt at Gen-4.5 with minor prompt adjustment
          If still fail -> activate Seedance fallback
```

### 3.3 Kling Generation Workflow (Scenes: S4, S6, S10)

Model strategy: draft on **Kling 2.6** (cheaper) to lock prompt/motion, then final render on **Kling 3.0** using reference-image character locking (upload 3-5 anchor stills + optional voice sample via Elements / Director Mode). 3.0's reference locking is the consistency feature 2.6 lacks -- it is the reason dynamic-face scenes route here on 3.0.

Generation unit: **5-second segments** (production standard). Per-credit cost is identical to 10s (linear, no per-clip overhead: 60 cr per 5s vs 120 cr per 10s at 1080p audio-on), but a failed 5s generation wastes only 60 credits and gives tighter start->end keyframe control. A 30s scene = 6x 5s segments.

```
Step 1: Upload approved anchor image(s) -- start frame; for 3.0 also load 3-5 reference stills for character locking
Step 2: (Optional) set end frame anchor for start->end keyframe interpolation
Step 3: Input scene prompt with motion direction (from 02-production-brief.md)
Step 4: Draft on Kling 2.6 to validate motion; once locked, render final on Kling 3.0
Step 5: Generate -- Kling 3.0, 1080p, native audio ON (12 credits/sec = 60 cr per 5s segment)
Step 6: Evaluate: motion quality, character integrity, dramatic composition
Step 7: If pass -> save to video-clips/
         If fail -> adjust motion prompt -> retry (max 3 attempts)
         If 3x fail -> activate Seedance fallback
```

> Capacity reference (one Premier subscribe = 8,000 credits, 1080p audio-on): ~666s gross (~11 min), ~433s net usable at 65% success. Project need is ~90s net (3 dynamic scenes), so one subscribe amply covers main production. NOTE: the 50% success-rate figure in 03-rab is an old-generation benchmark -- re-benchmark on 10-15 Kling 3.0 test generations before locking subscribe count.

### 3.4 Seedance Fallback Protocol (fal.ai)

Trigger conditions:
- Kling failed 3x on a specific scene, OR
- Runway failed 3x on a specific scene (including Turbo draft phase)

```
Step 1: Upload approved anchor image to a public URL (use fal.ai storage or imgbb)
Step 2: Run seedance_fallback.py with scene prompt and duration
Step 3: Retrieve output URL from result
Step 4: Download and evaluate
Step 5: If pass -> use as final clip, log fallback used for this scene
         If fail -> adjust prompt -> one more attempt
         If still fail -> escalate to human decision (likely re-anchor or accept best available)
```

**Seedance budget gate:**
Track cumulative spend against $20 fal.ai budget. Stop fallback use if cumulative exceeds $15 (reserve $5 for final assembly phase surprises).

### 3.5 Shot Count and Credit Tracking

Maintain a live credit log during production. Use this template:

```
CREDIT LOG
==========
Platform: Kling AI Premier (8,000 credits available)
Date | Scene | Shots Generated | Credits Used | Running Balance | Notes
-----|-------|-----------------|--------------|-----------------|------

Platform: Runway Gen-4.5 (Max: 9,500 cr | Pro: 2,250 cr)
Date | Scene | Phase (Draft/Final) | Credits Used | Running Balance | Notes
-----|-------|---------------------|--------------|-----------------|------

Platform: Seedance/fal.ai ($20 budget)
Date | Scene | Duration | Cost | Running Spend | Notes
-----|-------|----------|------|---------------|------
```

---

## Stage 4 -- Scoring Production (Suno AI)

### 4.1 Three Stems Required

| Stem | Phase | Duration Reference | Character |
|---|---|---|---|
| Phase 1 -- Cold/Electronic | Cold open (0-10 sec) | ~10 sec loop | Single low drone ~80Hz, pulsing every 2 sec, no melody, subtly dissonant |
| Phase 2 -- Organic Warm | Characters (10-270 sec) | ~260 sec, builds | Acoustic guitar entering first -> gamelan light -> strings -> rhythm section -> full warm band. Builds to crescendo before S15 |
| Phase 3 -- Full Swell | Convergence + close (270-300 sec) | ~30 sec | Full orchestra swell -> sudden near-silence at data segment -> warm chord resolve at tagline |

### 4.2 Suno Generation Workflow

```
Step 1: Generate Phase 1 stem -- minimal drone
        Prompt example: "low electronic drone 80hz pulse ambient, dissonant,
        no melody, dark blue palette, cold, slow pulse, 30 seconds loop"

Step 2: Generate Phase 2 stem -- building warmth
        Prompt example: "Indonesian acoustic guitar opening, solo, warm,
        then gamelan light enters, then strings, tempo builds slowly,
        Indonesian cultural roots subtle not explicit, cinematic, builds to
        emotional crescendo 4 minutes"

Step 3: Generate Phase 3 stem -- swell and resolve
        Prompt example: "full orchestral swell climax, all instruments,
        tempo peaks, then sudden near-silence, single warm low note sustains,
        then resolves to single warm major chord, fade slowly"

Step 4: Export each stem as separate audio file (WAV preferred, MP3 acceptable)
Step 5: Label clearly: stem-phase1.wav, stem-phase2.wav, stem-phase3.wav
Step 6: Generate 2-3 variants of Phase 2 for stakeholder selection
Step 7: Save all to scoring/ folder
```

---

## Stage 5 -- Assembly Sequence

### 5.1 Recommended Production Order

Execute in this exact order to minimize rework:

```
1. Live actor shoot (complete before any AI assembly)
   -> All 8 segments in one day
   -> Deliver: S1, S3, S5, S7, S9, S11, S13, S17 as raw footage

2. AI generation batch 1 -- Runway scenes (S0, S2, S8, S12, S14)
   -> Start with S2 (anchor character, most important, 40 sec)
   -> Cold open last (different pipeline, no anchor dependency)

3. AI generation batch 2 -- Kling scenes (S4, S6, S10)
   -> Can run in parallel with Runway batch if operator capacity allows

4. Scoring stems (parallel to AI generation)
   -> Begin Phase 2 stem generation while waiting for AI renders

5. Rough assembly (linear edit)
   -> Arrange all segments in sequence per D-016 blueprint
   -> Use draft-quality AI clips for timing validation
   -> VO dubbing session after rough assembly locked

6. Convergence scene (S15) -- Post-production
   -> Cut 2-3 sec loops from each character's best clip
   -> Compose 7-panel grid/mosaic
   -> Animate panel merge to single frame
   -> Apply warm center light effect

7. Data segment (S16) -- Motion graphics
   -> Clean white type on black
   -> Fade-in per line: line 1 (0-3 sec), line 2 (3-6 sec), line 3 (6-10 sec)
   -> Verify actual numbers before committing

8.  Final assembly with approved AI clips + live footage
9.  Score layering: match stem transitions to exact frame timestamps
10. VO dubbing sync
11. Color grade: maintain warm/cool contrast as specified in D-013
12. Sound mix: VO + scoring + ambient
13. Final export
```

### 5.2 Segment Timing Reference for Editor

| Segment | In Point | Out Point | Duration | Format |
|---|---|---|---|---|
| S0 -- Cold open | 0:00 | 0:10 | 10 sec | Runway AI |
| S1 -- Live actor open | 0:10 | 0:30 | 20 sec | Live |
| S2 -- Char 1 ibu | 0:30 | 1:10 | 40 sec | Runway AI |
| S3 -- Live transition 1 | 1:10 | 1:20 | 10 sec | Live |
| S4 -- Char 2 pemuda | 1:20 | 1:50 | 30 sec | Kling AI |
| S5 -- Live transition 2 | 1:50 | 2:00 | 10 sec | Live |
| S6 -- Char 3 kurir | 2:00 | 2:30 | 30 sec | Kling AI |
| S7 -- Live transition 3 | 2:30 | 2:40 | 10 sec | Live |
| S8 -- Char 4 profesional | 2:40 | 3:10 | 30 sec | Runway AI |
| S9 -- Live transition 4 | 3:10 | 3:20 | 10 sec | Live |
| S10 -- Char 5 pengusaha | 3:20 | 3:50 | 30 sec | Kling AI |
| S11 -- Live transition 5 | 3:50 | 4:00 | 10 sec | Live |
| S12 -- Char 6 tokoh | 4:00 | 4:30 | 30 sec | Runway AI |
| S13 -- Live transition 6 | 4:30 | 4:40 | 10 sec | Live |
| S14 -- Char 7 eksekutif | 4:40 | 5:10 | 30 sec | Runway AI |
| S15 -- Convergence | 5:10 | 5:25 | 15 sec | Post-prod |
| S16 -- Data segment | 5:25 | 5:35 | 10 sec | Motion graphics |
| S17 -- Live actor close | 5:35 | 5:55 | 20 sec | Live |
| **Total** | | | **300 sec** | |

> Note: The segment sequence above reflects the D-016 revised blueprint totaling 300 seconds. Editor should verify S1 starts at 0:10 (not 0:00) -- cold open occupies 0:00-0:10.

---

## Stage 6 -- Quality Gates

### Gate 1 -- Anchor Approval (before any video generation)
- [ ] All 7 characters have 4 approved anchor angles saved
- [ ] Gemma 4 consistency evaluation passed for each character
- [ ] Visual contrast rule verified: chars 1-7 all warm palette, cold open blue only

### Gate 2 -- Clip Approval (before assembly)
- [ ] All AI clips reviewed against scene description in 02-production-brief.md
- [ ] Platform split respected (Kling vs Runway assignment not swapped without reason)
- [ ] Seedance fallbacks logged and justified
- [ ] No explicit UI shown (only ambient glow, minimal floating text, or single contextual element)

### Gate 3 -- Assembly Review (before VO session)
- [ ] Rough cut timing matches D-016 blueprint exactly
- [ ] Arc visual: cold open cold -> characters warm -> convergence full -> data black -> close warm
- [ ] No religious organization names or logos visible in any frame
- [ ] No competitor names or logos visible in any frame
- [ ] Word "bayangkan" not present in any VO or on-screen text

### Gate 4 -- Pre-Publish (before any external sharing)
- [ ] Segment 16 numbers verified against actual data (not placeholder)
- [ ] VO dubbing synced to video
- [ ] Scoring stems mixed and transitioned correctly
- [ ] Color grade: warm/cold contrast maintained
- [ ] Total runtime: 300 seconds +/- 2 seconds

---

## Prompt Engineering Notes

### Midjourney Prompt Structure
Every Midjourney prompt should follow this structure:
```
[Subject description], [age/gender if applicable], [clothing/appearance],
[environment], [lighting], [mood/expression], [camera style],
[color palette note], --ar 16:9 --style raw --v 8.1
```

### What NOT to Include in AI Prompts
- Names of religious organizations (NU, Muhammadiyah, etc.)
- Names of competing platforms (Tokopedia, Shopee, Gojek, etc.)
- Political symbols or party references
- Identifiable brand logos (except as generic "product packaging" without readable text)

### Gemma 4 Best Use Cases in This Production
1. **Initial prompt generation:** Feed scene brief JSON -> receive optimized Midjourney prompt
2. **Anchor consistency evaluation:** Send 4 anchor images -> receive consistency score and suggestions
3. **Prompt variation:** Feed rejected prompt + reason -> receive adjusted version
4. **Cross-character color check:** Send 2+ anchor images -> confirm warm palette consistency

---

## Risk Log and Mitigation

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Kling face consistency failure on dynamic shots | High | Medium | Platform assignment already routes consistent-face scenes to Runway. Kling handles dynamic motion only. |
| Runway credit exhaustion before all scenes complete | Medium | High | Draft on Turbo first (80% savings). Monitor credit log daily. |
| Seedance $20 budget exceeded | Low | Low | Seedance is fallback for 3x failures only. $20 covers 7 full scenes at $0.14/scene average. |
| Cold open prompts too literal (referencing Matrix) | Medium | Medium | Prompts explicitly state "not Matrix-style." Use Gemma 4 to evaluate abstraction quality. |
| Scoring stems too explicitly Indonesian (folk music) | Low | Medium | Brief specifies "subtly rooted, not explicit." Generate 3 variants; select via stakeholder review. |
| Segment 16 numbers not updated before publish | Low | Critical | Gate 4 checklist -- mandatory verification. Numbers are placeholder until production data confirmed. |

---

*AI Production Pipeline v1.0 · Semesta Digital (working title) · 8 Juni 2026*
*Anchored to: 00-project-charter.md D-006 to D-017 · 02-production-brief.md*
*Next document: 05-storyboard-rough.md*
