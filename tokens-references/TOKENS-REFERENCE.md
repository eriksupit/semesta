---
title: Tokens Reference — Image Generation · Semesta Digital
tags: [tokens-reference, image-generation, prompt-engineering]
status: active
created: 2026-06-10
updated: 2026-06-10
aliases: [tokens-ref, prompt-tokens]
---

# Tokens Reference — Image Generation
## Semesta Digital (working title)
*Source: StudioBinder, PetaPixel, Paul Mitchell, Brushstroke MUA, Anuprerna, Koby Photography*
*Apply these tokens in prompts to produce varied, non-generic visuals. Model responds to industry convention terminology.*

---

## 1. SHOT SIZE (framing field)

Use abbreviation + description for maximum model recognition.

| Token | Full Name | Subject Framing | Best Use |
|---|---|---|---|
| `EWS` | Extreme Wide Shot | Subject tiny in environment | Scale, isolation, establishing |
| `WS` | Wide Shot / Long Shot | Full body + generous space above/below | Subject in context |
| `FS` | Full Shot | Full body, subject fills frame | Character intro, multiple subjects |
| `MWS` | Medium Wide Shot | Knees up | Action + environment balance |
| `CS` | Cowboy Shot | Mid-thigh up | Dynamic, hands + waist visible |
| `MS` | Medium Shot | Waist up | Dialogue, interaction, versatile |
| `MCU` | Medium Close-Up | Chest/shoulders up | Emotional intensity, speech |
| `CU` | Close-Up | Face fills frame | Peak emotion, reaction |
| `ECU` | Extreme Close-Up | Eyes, lips, single feature | Maximum intimacy |

**Full body token (validated S3):**
`full body shot, subject full height crown to sneaker sole visible, floor visible below feet, generous headroom above crown`

**BANNED:** `head to toe` — ambiguous when subject wears trousers (toe = shoe obscured)

---

## 2. CAMERA ANGLE (angle field)

Position of camera relative to subject.

| Token | Description | Effect |
|---|---|---|
| `eye-level` | Camera at subject's eye height | Neutral, relatable, natural |
| `slight low angle` | Camera slightly below eye level | Subtle authority, confidence |
| `low angle worm's eye` | Camera very low, looking up | Power, dominance, heroic |
| `high angle bird's eye` | Camera above, looking down | Vulnerability, scale, overview |
| `dutch angle` | Camera tilted on axis | Tension, unease, dynamic energy |
| `over-the-shoulder` | Camera behind one subject facing another | Conversation, perspective |
| `POV` | Camera = subject's eyes | Immersion, first person |

**Standard for live actors (validated):** `eye-level slight low angle, subject centered frame`

---

## 3. COMPOSITION (composition field — for benda mati / scene shots)

| Token | Technique | Description |
|---|---|---|
| `rule of thirds` | Place subject on grid intersections | Natural, dynamic, off-center |
| `centered symmetrical` | Subject dead center | Authority, stability, architecture |
| `Kubrick one-point perspective` | Single vanishing point centered | Symmetry + depth, corridor feel |
| `foreground interest depth` | Object close to lens, subject behind | 3D depth, layered frame |
| `frame within a frame` | Arch/window/doorway frames subject | Depth, context, layers |
| `leading lines` | Lines guide eye to subject | Direction, depth, movement |
| `diagonal dynamic tension` | Diagonal lines across frame | Energy, instability, drama |
| `negative space isolation` | Subject small in empty field | Loneliness, focus, minimalism |
| `golden ratio spiral` | Fibonacci composition | Classical, organic, balanced |
| `rule of odds` | Odd number of subjects | Natural, visually comfortable |
| `layered depth foreground midground background` | Three distinct depth planes | Richness, cinematic depth |

---

## 4. POSE (pose field)

Sourced from lifestyle/portrait photography convention.

### Standing poses
| Token | Description |
|---|---|
| `contrapposto` | Weight on one leg, hips offset, natural S-curve |
| `three-quarter stance body 45 degrees` | Body turned 45° to camera, face forward |
| `neutral standing feet shoulder-width` | Balanced, centered, composed |
| `weight shifted one hip` | Casual lean, relaxed authority |
| `arms crossed chest` | Confident, self-contained |
| `one hand on hip other relaxed` | Casual confidence |
| `leaning against wall one shoulder` | Relaxed, approachable |
| `walking mid-stride` | Dynamic, forward energy |
| `mid-step weight shifting forward` | Decisive movement, purpose |

### Seated poses
| Token | Description |
|---|---|
| `perched desk edge one leg extended` | Casual authority, relaxed |
| `seated upright slight forward lean` | Engaged, attentive |
| `seated legs crossed` | Relaxed, composed |
| `seated elbows on knees leaning forward` | Intensity, focus |

### Action-based poses (for dramatic scenes)
| Token | Description |
|---|---|
| `both palms flat on desk arms locked weight forward` | Decisive, mid-decision |
| `one hand raised open palm presenting` | Presenting, offering, showing |
| `arms natural swing mid-motion` | Walking natural energy |
| `hands clasped loosely at waist` | Still, composed, waiting |
| `fingertip approaching screen mid-touch` | Interacting with technology |
| `both hands cradling device screen-up` | Intimate with technology |

---

## 5. GESTURE (gesture field)

Specific hand/arm positions. Always concrete, never abstract.

| Token | Description |
|---|---|
| `one hand raised open palm presenting forward` | Offering/showing something |
| `both hands open palms facing up` | Openness, invitation |
| `one hand gesturing forward index finger point` | Directing, asserting |
| `hands clasped loosely at waist` | Composed stillness |
| `arms natural swing forward momentum` | Walking, motion |
| `both palms flat on surface fingers spread` | Decisive lean |
| `fingertip near screen mid-interaction` | Digital action |
| `both hands cradling device from below` | Intimate device use |
| `one hand on hip other relaxed at side` | Casual confidence |
| `arms slightly away from body open stance` | Openness, presence |

**BANNED:** `hands relaxed` without specific position

---

## 6. EXPRESSION (expression field)

Always physical description, never emotion label.

| Token | Physical Description | Register |
|---|---|---|
| `Duchenne smile eyes crinkled outer corners cheeks lifted` | Genuine full smile | Warm, authentic |
| `closed-mouth soft smile jaw relaxed cheeks slightly lifted` | Subtle satisfaction | Private, composed |
| `mouth open mid-speech lifted brows animated direct gaze` | Speaking, engaging | Presenting, alive |
| `direct unflinching gaze jaw set mouth closed tight` | Conviction | Decisive, resolved |
| `brows slightly furrowed jaw relaxed focused gaze` | Concentration | Mid-task, absorbed |
| `eyes softened outer corners private downward gaze` | Private moment | Intimate, unperformed |
| `slight upturn mouth corners eyes ahead analytical` | Quiet satisfaction | Professional calm |
| `mouth just opening brows beginning to lift` | About to speak | Tension before release |
| `composed direct gaze unhurried stillness` | Full presence | Authority, earned |

**BANNED:** `happy`, `confident`, `warm smile`, `natural smile`, any single-word emotion label

---

## 7. MAKEUP (makeup sub-field in character_style)

Three layers mandatory: base + features + finish. Add 1–2 industry technique tokens.

### Base layer tokens
| Token | Description |
|---|---|
| `full-coverage foundation pore-blurring primer effect seamless blended base` | Full coverage |
| `medium-coverage satin foundation poreless smooth canvas` | Medium coverage |
| `light tinted moisturizer natural coverage` | Minimal coverage |
| `BB cream sheer luminous coverage` | Natural/dewy |

### Feature layer tokens
| Token | Description |
|---|---|
| `soft contour cheekbones defined arched brows nude satin lipstick peach cream blush` | Polished feminine |
| `defined brows lash-lengthening mascara nude glossy lip soft bronzer` | Fresh feminine |
| `softly defined brows clear lip balm minimal blush flush` | Domestic/natural |
| `groomed brows spoolie-brushed natural arch light concealer even skin tone` | Male groomed |

### Finish layer tokens (MANDATORY — prevents oily/lushy skin)
| Token | Description |
|---|---|
| `baked setting powder long-wearing matte finish oil-controlled complexion zero shine` | Matte set |
| `translucent loose powder set long-wearing matte finish oil-controlled complexion zero shine` | Natural set |
| `matte setting powder baked complexion zero shine` | Male finish |
| `airbrushed poreless skin zero shine` | High-definition |

### Industry technique markers (add 1–2 per prompt)
| Token | Technique |
|---|---|
| `strobing highlight bridge of nose and brow bone` | Strobing — highlight technique |
| `colour-corrected under-eye` | Colour correction |
| `baking technique set concealer` | Baking — powder setting |
| `contouring sculpted cheekbone definition` | Contouring |
| `airbrush finish seamless coverage` | Airbrush technique |

**BANNED:** `HD makeup`, `HD setting powder` — trigger specular highlights/glossy skin

---

## 8. WARDROBE (wardrobe sub-field in character_style)

Always: fabric + construction + fit/silhouette + colorway desaturated. Add 1 designation token.

### Fabric tokens
| Token | Type |
|---|---|
| `linen-cotton blend` | Natural, breathable |
| `oxford cloth` | Classic shirt fabric |
| `cotton twill` | Structured trouser |
| `polyester-wool blend` | Suiting |
| `matte nylon shell` | Technical outerwear |
| `cotton jersey` | Casual knit |
| `rayon` | Flowy, drape |
| `polyester crepe` | Structured dress |
| `technical nylon` | Performance |

### Construction/silhouette designation tokens
| Token | Description |
|---|---|
| `MA-1 bomber silhouette` | Flight jacket, ribbed cuffs/hem |
| `notched lapel two-button front` | Classic blazer construction |
| `single-breasted two-button front` | Suit jacket |
| `French tuck at front hem` | Styling convention — tuck front only |
| `Oxford cloth button-down` | OCBD shirt |
| `raglan sleeves` | Sportswear sleeve |
| `dropped shoulders` | Relaxed/oversized |
| `chest patch pocket` | Casual utility |
| `stand collar zip-front` | Technical/performance |
| `spread collar dress shirt` | Formal shirt |
| `mid-rise tapered leg` | Modern trouser |
| `high-rise wide-leg` | Fashion trouser |
| `slim-fit single-dart` | Tailored trouser |

### Fit tokens
| Token |
|---|
| `slim fit` |
| `relaxed fit` |
| `oversized relaxed fit` |
| `tailored slim fit` |
| `straight fit` |

### Colorway tokens (desaturated only — no pure color names)
| Token |
|---|
| `muted slate-grey` |
| `charcoal grey` |
| `faded sage-grey` |
| `off-white` |
| `muted slate-blue` |
| `dark navy` |
| `pale blue solid` |
| `cream` |

**BANNED:** batik, paisley, ikat, floral, ethnic print, terracotta, ochre, amber, golden

---

## 9. HAIR (hair sub-field in character_style)

Always: cut + styling technique + finish. Add 1 barbering/salon term.

### Female hair tokens
| Token | Style |
|---|---|
| `voluminous bouncy blowout deep side part shoulder-length glossy finish` | Professional glamour |
| `sleek straight collarbone length high shine centre part` | Corporate polish |
| `low loose bun face-framing wisps natural texture matte finish` | Casual domestic |
| `soft layered cut collarbone length body-wave texture glossy finish` | Relaxed professional |
| `textured lob blunt ends shoulder-length matte finish` | Modern casual |

### Male hair tokens
| Token | Style |
|---|---|
| `short textured crop low fade sides natural parting matte pomade finish` | Urban professional |
| `short side-part slick natural texture matte finish` | Corporate clean |
| `short natural crop low-fade sides matte finish` | Casual young |
| `short textured quiff styled back matte clay finish` | Fashion forward |

### Salon/barbering technique markers (add 1 per prompt)
| Token | Technique |
|---|---|
| `low fade sides` | Barbering — graduated fade |
| `high skin fade` | Barbering — sharp fade |
| `blowout voluminous` | Blowdry styling |
| `matte pomade finish` | Product finish |
| `matte clay finish` | Product finish |
| `glossy serum finish` | Product finish |
| `deep side part` | Parting technique |

**BANNED:** `natural black hair shoulder length` (generic), `soft blowout` without `glossy`

---

## 10. FOOTWEAR (footwear sub-field in character_style)

Standalone field — separate from wardrobe. Always: silhouette + material + sole + branding level.

### Token library
| Token | Style |
|---|---|
| `low-profile clean leather sneakers white rubber cupsole minimal branding` | Urban casual clean |
| `white leather common projects aesthetic minimal branding` | Premium minimalist |
| `suede low-top sneakers gum rubber sole` | Casual heritage |
| `clean white canvas sneakers rubber sole` | Casual everyday |
| `derby shoes polished leather cap-toe black leather sole` | Professional formal |
| `loafers horsebit hardware leather sole` | Smart casual elevated |
| `chelsea boots pull-tab suede leather sole` | Smart casual urban |
| `running shoes mesh upper cushioned midsole` | Athletic/courier |
| `sandals flat leather strap minimal` | Casual outdoor |

**Framing note:** Always pair with `crown to sneaker sole visible` in framing field to ensure footwear renders

---

## 11. ATMOSPHERE (atmosphere field — Lapis 2)

Spatial energy of the scene — not weather, not lighting.

| Token | Register | Best For |
|---|---|---|
| `lively bustling crowd energy` | Urban public space, active | S3 bazaar, S6 street |
| `intimate quiet domestic` | Home, personal, private | S2 kitchen |
| `dramatic urban pulse` | Night city, motion | S3 night |
| `calm professional focus` | Office, workspace | S8 desk |
| `communal gathering warmth` | Pavilion, community | S12 elder |
| `clinical empty stillness` | No people, eerie | S0 cold open |
| `industrial purposeful hum` | Warehouse, functional | S10 entrepreneur |
| `corporate controlled precision` | Meeting room, executive | S14 eksekutif |
| `focused solitary determination` | Solo work, study | S4 pemuda |
| `dignified unhurried presence` | Authority, earned calm | S12 tokoh |

---

## 12. SCENE DEPTH (scene_depth field — Lapis 2)

Three depth planes as explicit sub-fields. Mandatory for all scenes with environment, crowd, or background activity. Controls what the model populates at each depth layer independently.

```json
"scene_depth": {
  "foreground": "[physical elements 0–2m from lens]",
  "midground": "[primary subject + immediate environment 2–5m]",
  "background": "[depth, population, atmosphere 5m+]"
}
```

### Foreground token examples
| Token | Scene |
|---|---|
| `motorcycle handlebar lower frame, phone mount bracket, asphalt surface` | S6 kurir |
| `desk surface lower frame, ceramic mug, laptop edge` | S8 profesional |
| `countertop lower edge, smartphone cradled both hands` | S2 ibu RT |
| `low wooden bench table surface worn grain` | S4 pemuda |
| `dark wood veneer table edge lower frame` | S14 eksekutif |

### Midground token examples
| Token | Scene |
|---|---|
| `courier seated on parked motorcycle, helmet visor up, courier bag strap across chest` | S6 |
| `professional woman seated at desk, hands on laptop lid` | S8 |
| `homemaker standing at kitchen counter, both hands cradling smartphone` | S2 |

### Background token examples
| Token | Scene |
|---|---|
| `dense Jakarta urban street fully populated — 10+ motorcycles cars mid-traffic, pedestrians on sidewalk, warung signage, low-rise shophouse facades, trees overhanging` | S6 |
| `built-in open bookshelf books potted plants, fixed-pane window city view, pendant lamp` | S5/S7/S9 home office |
| `industrial steel shelving product boxes stacked, polished concrete depth, warehouse high ceiling` | S10 |
| `timber post-and-beam structure, dense tropical foliage canopy, compacted earth` | S4/S12 |
| `recessed LED ceiling, wall display map, upholstered conference chairs partially visible` | S14 |

### Rules
- Background must always be explicitly described — model default is empty/sparse
- BANNED: negation tokens in any sub-field (`NO X`, `without X`, `absent X`) — describe what IS present
- BANNED for S0 and S16 — these scenes use subject_anchor, no depth layers needed
- Validated S6: populated background eliminates empty-world problem

---

## 13. COMPOSITION TECHNIQUES FOR CHARACTER SCENES

Apply to `framing` or `composition` field for scene-level composition direction.

| Token | Technique | Effect |
|---|---|---|
| `subject dominant foreground rule of thirds` | Subject at grid intersection | Natural, dynamic |
| `subject centered symmetrical` | Dead center | Authority, stability |
| `foreground subject midground crowd background architecture` | Three depth planes | Cinematic richness |
| `leading lines converging behind subject` | Lines lead to subject | Depth, direction |
| `negative space above subject generous headroom` | Empty space above | Breathing room, scale |
| `frame within frame doorway arch` | Environmental framing | Context, depth |
| `diagonal dynamic tension` | Off-axis elements | Energy, drama |
| `layered bokeh foreground midground background` | Depth through focus | Professional cinema |

---

## 13. QUICK REFERENCE — FIELD STRUCTURE PER SCENE TYPE

### Character scene (6-layer order)
```
Lapis 1: mood → color_grade → style
Lapis 2: scene → location → time_of_day → atmosphere
Lapis 3: character_identity { role, ethnicity, beauty, age, facial_features, body_features }
         character_style { makeup, wardrobe, hair, footwear }
Lapis 4: subject_state → action → pose → gesture → expression
Lapis 5: on_screen_graphic → graphic_proximity [opsional]
Lapis 6: framing → angle → camera → lighting → aspect_ratio
```

### Benda mati / scene kosong
```
Lapis 1: mood → color_grade → style
Lapis 2: scene → location → time_of_day → atmosphere
Lapis 3: subject_anchor { primary_subject, subject_material, supporting_objects, human_absence_signal }
Lapis 4: subject_state → action
Lapis 6: framing → composition → angle → camera → lighting → aspect_ratio
```

---

## 14. DIVERSITY CHECKLIST — AVOID VISUAL MONOTONY

Use this checklist before generating consecutive scenes:

- [ ] Shot size varied (not all MCU or MS)
- [ ] Angle varied (not all eye-level)
- [ ] Atmosphere varied (not all `calm professional focus`)
- [ ] Time of day varied (not all `afternoon indoor`)
- [ ] Pose varied (not all `contrapposto body 45 degrees`)
- [ ] Expression varied (not all `mouth open mid-speech`)
- [ ] Framing varied (not all `medium long shot knees to head`)
- [ ] Footwear visible when fullbody shot

---

*Tokens Reference v1.0 · Semesta Digital · 10 Juni 2026*
*Sources: StudioBinder (camera shots), PetaPixel (composition), Paul Mitchell (hair), Brushstroke MUA (makeup), Anuprerna (fashion), Koby Photography (poses)*
