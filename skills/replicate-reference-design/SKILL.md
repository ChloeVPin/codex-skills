---
name: replicate-reference-design
description: Reconstruct a web or product interface from one or more attached reference images with high visual fidelity. Use when Codex must copy, reproduce, rebuild, or closely match a screenshot, mockup, landing page, portfolio, dashboard, mobile screen, or visual design in code while preserving its hierarchy, composition, typography, color roles, imagery, component anatomy, responsive intent, motion cues, and accessibility.
---

# Replicate Reference Design

Rebuild the attached reference as a functioning interface. Treat the image as the visual source of truth and the user’s explicit requirements as the behavioral source of truth. Recover the system behind the pixels; do not substitute a familiar template or merely imitate the mood.

## Contract

Deliver the closest implementation the available evidence, assets, runtime, and viewport support.

Preserve, in priority order:

1. Section order and chapter boundaries
2. First-viewport composition and dominant idea
3. Relative geometry, alignment axes, and density
4. Typography roles, scale relationships, wrapping, and rhythm
5. Color roles, surface transitions, and contrast
6. Image treatment, crops, material, and visual world
7. Component anatomy and repetition
8. Responsive semantic equivalence
9. Visible interaction and defensible motion
10. Micro-detail: radii, borders, shadows, texture, and icon treatment

Do not claim exact recovery of hidden source values. A screenshot supports high-confidence conclusions about visible hierarchy and relative geometry; it does not prove the exact font, CSS pixels, framework, breakpoint, hover behavior, or animation timing.

## Evidence discipline

Classify observations before implementation:

```yaml
high_confidence:
  - raster_dimensions
  - section_order
  - dominant_first_viewport_idea
  - background_transitions
  - relative_alignment
  - component_repetition
  - visible_text
  - dominant_color_strategy
medium_confidence:
  - likely_grid
  - container_width_range
  - type_scale_range
  - responsive_intent
  - interaction_affordance
low_confidence:
  - exact_font_family
  - exact_css_pixels
  - original_framework
  - hidden_states
  - hover_behavior_not_shown
  - animation_timing
```

Implement high-confidence evidence directly. Use coherent approximations for medium-confidence evidence. For low-confidence evidence, choose the smallest defensible option that preserves the visible result.

Never invent illegible copy, unseen pages, proprietary assets, hidden interactions, testimonials, metrics, or brand facts. Use the user’s supplied assets, extract high-confidence visible text, or create clearly marked structural substitutes.

## Required workflow

### 1. Inspect the target and environment

Before changing code:

- Open every attached reference at the highest useful detail.
- Record image dimensions and apparent viewport class.
- Determine whether the image is a full-page capture, cropped screen, composite, or mobile reference.
- Inspect the existing repository, framework, routes, components, tokens, fonts, and assets.
- Identify the requested route and output format.
- Preserve existing project conventions unless they prevent faithful reproduction.
- Confirm which reference controls when multiple images disagree.

Do not ask for information recoverable from the image or repository. Ask one focused question only when a missing decision would produce materially different designs.

### 2. Build a reference map

Segment the image into ordered chapters before coding. For each chapter, record:

```text
Chapter:
Purpose:
Surface:
Height behavior:
Primary alignment:
Content hierarchy:
Media treatment:
Repeated component:
Transition to next chapter:
Confidence:
```

Use chapter boundaries visible through:

- Hard background changes
- Full-bleed media transitions
- New grid anatomy
- Typography scale shifts
- Repeated-component runs
- Proof or conversion transitions
- Large changes in density or whitespace

Recover the page narrative, not only the isolated sections.

### 3. Recover the grid and geometry

Estimate relationships before absolute values:

- Outer inset as a viewport percentage
- Container behavior: bounded, near-full-width, or full bleed
- Likely column count
- Repeated vertical and horizontal axes
- Gutter range
- Copy-to-media ratio
- Reading width
- Section height behavior
- Overlap, crop, and negative-space rules

Prefer statements such as “copy occupies roughly one third; media occupies the remaining two thirds” over unsupported exact dimensions.

Use a coherent grid family:

- Editorial 12-column grid for asymmetric copy/media compositions
- Narrow reading column for manifesto or product-tour narratives
- Full-bleed stage with a nested content grid for cinematic pages
- Spatial grid for object stages and anchored collages
- Dense utility grid for technical interfaces and product proof

Do not average conflicting grid systems into a generic centered container. Preserve intentional asymmetry, cropping, and whitespace.

### 4. Recover typography by role

Do not guess an exact commercial font unless the repository, metadata, or a verified brand source establishes it. Match the visual archetype:

- Neutral neo-grotesk for body, navigation, metrics, ledgers, and product UI
- Rounded geometric grotesk for friendly product, care, education, and human AI
- Condensed identity grotesk for giant names, wordmarks, and poster-scale statements
- High-contrast editorial serif for strategy, culture, beauty, books, and speculative narrative
- Monospaced technical face for code, status, coordinates, and engineering metadata

Recover:

- Display/body/utility relationship
- Relative size scale
- Line-height and vertical fit
- Tracking
- Weight and contrast
- Italic or mixed-family role
- Line breaks and measure
- Alignment and crop behavior

Typography is architecture. Match title footprint and wrapping before refining decoration. If the exact font is unavailable, choose a metrically and stylistically close substitute and adjust width, size, tracking, and line-height to reproduce the silhouette.

### 5. Recover color by role

Separate interface colors from colors inside photography or illustration.

Map:

```yaml
primary_surface:
secondary_surface:
primary_text:
muted_text:
action_accent:
status_accent:
border_or_rule:
decorative_palette:
photographic_palette:
```

Preserve the reference’s strategy:

- Monochrome editorial
- Warm paper with one signal color
- Nature-led trust palette
- Dark technical workspace
- Neutral base with one fluorescent chapter
- Atmospheric dream palette
- Muted mineral or physical-material palette

Do not promote every sampled image color into a token. Use one coherent accent logic and one neutral temperature unless the reference visibly establishes otherwise.

### 6. Recover shape, surfaces, and texture

Determine the geometry family:

- Square editorial
- Technical small-radius
- Friendly product radius
- Soft cinematic radius
- Capsule controls

Match radius relationships, not one arbitrary radius applied everywhere. Preserve whether grouping is achieved through cards, spacing, rules, surface changes, or physical objects.

Recover:

- Border strength and frequency
- Shadow family
- Elevation logic
- Film grain, paper noise, grid, watercolor, or material texture
- Blur and translucency
- Object lighting and shadow direction

Reject generic gradient blobs, card shells, and shadows when the reference relies on typography, rules, imagery, or empty space instead.

### 7. Analyze the hero as the anchor

The first viewport establishes category, identity, emotional tone, action, expected proof, and scroll motivation. Identify exactly one dominant idea.

Classify the hero when useful:

- Oversized identity
- Centered manifesto
- Scenic overlay
- Framed billboard
- Isolated object stage
- Split product proof
- Cinematic personal introduction
- Emotional illustration

Reproduce the hero’s anatomy and hierarchy. Do not replace an isolated object stage with a centered SaaS hero, a billboard with generic text beside an image, or a product-first hero with abstract decoration.

If three elements compete equally, fix hierarchy rather than preserving accidental ambiguity.

### 8. Recover components by purpose

Name and implement components by behavior, not appearance. Examples:

- `editorial-case-study-index`
- `recognition-ledger`
- `strategic-question-matrix`
- `capability-accordion-with-preview`
- `alternating-product-step`
- `integration-orbit`
- `scenic-conversion-card`
- `mega-wordmark-footer`

A component is reusable only when its anatomy remains stable across content.

For each visible component, specify:

```text
Purpose
Anatomy
Desktop geometry
Mobile transformation
States
Interaction
Accessibility
Source evidence
```

Preserve repeated anatomy. Do not reduce distinct components to one universal card.

### 9. Reproduce imagery and art direction

Use supplied assets whenever available. Search the repository before sourcing or synthesizing replacements.

Classify the reference treatment:

- Documentary photography
- Editorial product cutout or macro
- Illustration world
- Physical or 3D object
- Product interface artifact
- Cultural collage
- Video or kinetic stage

Match:

- Crop and aspect ratio
- Subject scale and placement
- Safe zones for text
- Color treatment
- Lighting/material consistency
- Edge behavior and overflow
- Relationship to the grid

If an exact asset is unavailable, preserve the composition with a clearly marked substitute. Do not invent fake customer logos, people, products, awards, or case-study proof.

Do not shrink complex product UI until it becomes illegible. Use crops, overflow, callouts, or step-based reveals to preserve its function.

### 10. Infer motion conservatively

Implement motion only when visible evidence or component anatomy supports it. Use likely mechanics:

- Mask or line reveal for monumental type
- Subtle media scale on hover/focus
- Arrow translation for row actions
- Slow parallax for layered scenes
- Manual or pausable rails
- Pointer tilt for physical object stages
- Accordion height transitions
- Product-step sequencing

Do not invent a cinematic animation system from a static reference. Preserve layout and hierarchy first.

Every motion system must include:

- Reduced-motion behavior
- Keyboard-equivalent access
- Pause controls for autoplay
- No essential information available only in motion
- Stable layout without avoidable shift
- Static fallback for WebGL, particles, video, or complex canvas work

### 11. Recompose responsively

Do not treat mobile as “stack everything.” Recover semantic intent:

- Preserve reading order.
- Reframe media around the meaningful subject.
- Move absolute annotations into normal flow.
- Convert rails to controlled snap scrollers or grids.
- Convert ledgers and tables to labeled rows or disclosures.
- Replace complex 3D/video systems with useful static fallbacks when needed.
- Keep giant decorative type separate from the semantic heading.
- Preserve the primary action and essential context.

When only a desktop image is provided, infer mobile from purpose and component anatomy, not from arbitrary breakpoint conventions.

### 12. Preserve accessibility without flattening the design

Check:

- Functional text contrast
- Text over media in every crop
- Focus visibility
- Keyboard order
- Touch targets
- Carousel controls and status
- Autoplay pause
- Video captions
- Semantic lists, tables, and ledgers
- Color-independent state
- Decorative giant type semantics
- Reduced motion
- Content hidden in canvas, WebGL, or imagery

Low-contrast decorative type may remain only when equivalent semantic text exists. Functional microcopy must remain legible. Do not claim conformance from visual inspection alone.

## Implementation rules

- Use the project’s existing stack and dependencies.
- Inspect package manifests before importing libraries.
- Reuse existing tokens and primitives when they can match the target.
- Create new abstractions only for genuinely repeated anatomy.
- Keep semantic document structure separate from decorative layers.
- Prefer CSS Grid for explicit two-dimensional composition.
- Use absolute positioning only when the reference requires spatial layering and provide a deterministic mobile transformation.
- Keep DOM order semantic even when the visual order changes.
- Preserve real copy and assets supplied by the user.
- Do not introduce unrelated features, routes, dependencies, or redesign decisions.

## Fidelity loop

After the first implementation:

1. Render at the reference viewport or closest defensible viewport.
2. Capture a screenshot.
3. Compare reference and implementation side by side.
4. List mismatches by severity.
5. Correct in this order:
   - page and section geometry
   - hero scale and first viewport
   - typography footprint and line breaks
   - alignment and spacing
   - image crop and visual weight
   - surfaces and color
   - component anatomy
   - borders, radii, shadows, texture
   - motion and microinteraction
6. Repeat until the largest remaining differences are asset- or evidence-limited.

Do not stop after producing plausible code. Visual inspection is mandatory when rendering tools are available.

## Comparison report

Use this compact table during iteration:

| Area | Reference evidence | Current mismatch | Correction | Status |
| --- | --- | --- | --- | --- |

Do not expose hidden chain-of-thought. Report observable evidence, decisions, and corrections.

## Rejection criteria

Reject or revise the result when:

- It captures the mood but not the geometry.
- It substitutes a generic hero for the reference’s dominant idea.
- It uses a centered max-width template despite visible asymmetry.
- It turns every section into cards.
- It chooses convenient icons or decoration absent from the reference.
- Typography roles or line breaks materially change the composition.
- Image crops move the subject or destroy text-safe zones.
- The palette drifts between unrelated neutral or accent families.
- Mobile merely shrinks desktop spatial positioning.
- Motion is invented without evidence or lacks a fallback.
- Placeholder content changes layout behavior.
- The implementation omits visible proof, conversion, or footer chapters.
- The design is not rendered and compared despite available tools.

## Completion gate

Finish only when:

- All visible chapters are implemented in order.
- The first viewport has the same dominant idea and weight distribution.
- Repeated alignment axes and component anatomy match.
- Typography, color, image treatment, and geometry form the same system.
- Responsive transformations preserve meaning.
- Relevant states and accessibility fallbacks exist.
- The target route renders without console, build, or interaction errors.
- A final screenshot comparison has been completed.
- Remaining mismatches are explicitly attributed to unavailable assets, hidden behavior, or unprovable source values.

Return the implemented path, validation performed, fidelity limitations, and remaining evidence gaps.
