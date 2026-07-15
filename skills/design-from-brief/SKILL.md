---
name: design-from-brief
description: Design and implement a distinctive, award-caliber web or product interface from a written brief without a reference image. Use when Codex must create a landing page, portfolio, SaaS site, product experience, developer tool, care or education interface, editorial product, campaign, or other digital design with coherent art direction, strong hierarchy, proof architecture, responsive semantic behavior, accessible motion, and non-generic visual systems.
---

# Design From Brief

Create a complete interface from the user’s brief. Convert product meaning into one coherent visual system and a deliberate page narrative. Do not assemble fashionable effects or average several design styles together.

## Design thesis

Before designing or coding, write one sentence:

```text
Design thesis: [product] for [audience] will feel [specific qualities] by using [one typographic voice], [one visual world], [one grid logic], and [one proof strategy] to drive [primary conversion or task].
```

The thesis must explain mechanics, not only adjectives.

Weak:

```text
Modern, clean, premium SaaS website.
```

Strong:

```text
A technical code-review product for engineering teams will feel rigorous and inspectable through a dark graph-paper workspace, live product artifacts, restrained fluorescent state color, ruled proof modules, and a direct trial path.
```

## Required inputs

Recover or infer:

```yaml
product_or_subject: required
audience: required
primary_task_or_conversion: required
category: required
tone: required
proof_available:
  - product_screens
  - photography
  - illustration
  - 3d
  - code
  - metrics
  - customers
  - testimonials
  - experts
  - awards
  - funding
  - events
  - none
existing_assets:
  - logo
  - colors
  - typography
  - imagery
  - design_system
  - codebase
constraints:
  - platform
  - framework
  - accessibility
  - performance
  - localization
  - deadline
```

Inspect supplied code and assets before choosing the system. Do not ask for information already present. If one unresolved decision would produce materially different directions, ask one focused question; otherwise state assumptions and proceed.

## System selection

Select exactly:

- One primary typography archetype plus an optional utility face
- One color strategy
- One hero pattern
- One grid family
- One radius family
- One shadow/material family
- One image or illustration grammar
- Six to ten major component chapters for a substantial page
- At least three distinct proof types when evidence exists
- One contextual conversion moment plus one final conversion moment

Do not merge every attractive pattern into one page. Coherence is more valuable than variety.

## Category direction matrix

### Creative agency or studio

Prefer:

- Oversized identity, environmental billboard, or isolated object hero
- Editorial case-study index, portfolio media wall, service stack, client constellation, recognition ledger
- Square editorial geometry
- Monochrome or warm-paper system with one signal color
- Typography and work as architecture

Avoid generic feature cards, vague manifesto copy before proof, and decorative agency futurism unrelated to capability.

### Developer or technical product

Prefer:

- Split product hero or immediate product artifact
- Code panel, product demo, preset grid, diagnostic module, platform selector, integration proof
- Technical small-radius geometry
- Dark technical or disciplined light workspace
- Fluorescent color reserved for state and causality
- Claims followed quickly by runnable-looking evidence

Avoid glossy SaaS decoration, illegible screenshots, empty security claims, and generic testimonials where code or performance proof is available.

### Human AI, care, education, or behavior product

Prefer:

- Scenic overlay or emotional illustration hero
- Nature, documentary humans, archival illustration, or a coherent symbolic world
- Alternating workflow steps, human proof, expert evidence, integration ecosystem, outcome metrics
- Friendly but controlled radii
- Trust palette outside sterile corporate blue when appropriate

Separate emotional meaning, workflow proof, and scientific or operational authority into distinct chapters.

### Early-stage or speculative product

Prefer:

- Scenic overlay or isolated object hero
- One sustained metaphor rather than rotating concepts
- Narrative interlude, milestone, audience statement, hiring or waitlist conversion
- Soft cinematic geometry and controlled ambiguity

State the audience and value plainly even when product proof is limited. Use funding only as verified momentum proof.

### Personal portfolio

Prefer:

- Oversized identity, cinematic personal, or isolated object hero
- Portfolio wall, case-study index, project constellation, recognition ledger, process statement, contact poster
- A repeated material, motion, or shelf anatomy that orders diverse work
- Personal imagery or identity framing at the beginning and close

The interface may demonstrate capability, but project access and contact must remain discoverable.

### Book, culture, research, or thought leadership

Prefer:

- Isolated physical object or manifesto hero
- Numbered editorial benefits, contributor ecosystem, expert quotes, events ledger, author profile, testimonial rail
- Square editorial geometry
- Tactile photography, macro material, cultural collage, or disciplined monochrome

Treat the object or thesis as a cultural artifact, not a generic ecommerce SKU.

### Civic, industrial, or physical product

Prefer:

- Spatial product universe, documentary environment, full-bleed application storytelling
- Taxonomy menu, technical proof, material specification, job or event ledger
- Restrained grid and civic palette
- Real environments and engineering evidence

Use technical drawings, sustainability evidence, and application context to convert visual interest into confidence.

## Typography system

Choose by role, not trend.

### Neutral neo-grotesk

Use for body, navigation, metrics, product UI, and editorial ledgers. Target restrained tracking, readable measure, and a clear weight hierarchy.

### Rounded geometric grotesk

Use for friendly AI, education, care, consumer products, and illustrated systems. Keep warmth without weakening operational clarity.

### Condensed identity grotesk

Use for one monumental identity gesture per viewport. Treat it as a graphic layer, not a normal heading step.

### High-contrast editorial serif

Use for strategic manifestos, culture, beauty, books, speculative narratives, and selected mixed headlines. Do not use thin cuts for functional small text.

### Monospaced technical

Use for code, coordinates, status, labels, and engineering metadata. Do not use it as the sole long-form marketing face.

Define:

- Body and reading width
- Display scale and line-height
- Utility text
- Weight and tracking
- Mixed-family relationship
- Giant decorative versus semantic text
- Mobile clamps and line-break behavior

Typography must establish layout before decoration.

## Color strategy

Choose one strategy and adapt it to the brand:

- Monochrome editorial for authority and cultural confidence
- Warm paper with one signal color for approachable intelligence
- Nature-led trust for human AI, care, robotics, and CX
- Dark technical workspace for developer credibility
- Neutral system with one fluorescent chapter for a memorable climax
- Atmospheric dream palette for poetic or pre-product narrative
- Muted mineral or material palette for physical and 3D stages

Define semantic roles:

```yaml
surface_primary:
surface_secondary:
text_primary:
text_muted:
action_accent:
status_positive:
status_warning:
status_negative:
border:
focus:
decorative_palette:
```

Keep photographic color separate from interface tokens. Use dark text on fluorescent light surfaces. Test every functional text/surface pair; pastel does not imply readable.

## Grid and density

Choose a coherent grid family:

- 12-column editorial for asymmetry and varied media spans
- Narrow single-column narrative for manifesto, product tour, or creator-native directness
- Full-bleed cinematic stage with nested reading grid
- Spatial object grid with anchored annotations
- Dense technical grid for comparison, monitoring, and product mechanics

Control density over the page:

- Sparse stages create focus.
- Dense proof modules establish substance.
- Chapter contrast prevents monotony.
- Density should change with content, not remain uniformly airy or packed.

Use repeated alignment axes. Change density, surface, or media mode every one to three chapters when the narrative supports it.

## Hero design

Choose exactly one dominant first-viewport idea.

### Oversized identity

Use when the brand or person is the differentiator. Pair monumental type with micro navigation, compact positioning, and selective work preview.

### Centered manifesto

Use when one strategic statement must lead. Keep the proposition narrow and attach one meaningful motif or object.

### Scenic overlay

Use when a complete visual world can humanize or explain the product. Establish a text-safe zone and one compact action.

### Framed billboard

Use for campaigns and agencies where the proposition should appear as authored work rather than generic marketing copy.

### Isolated object stage

Use for physical products, books, creative technology, or collectible artifacts. Let material, light, and negative space carry value.

### Split product

Use for technical products that require comprehension and proof immediately. Show a readable artifact, not decorative pseudo-UI.

### Cinematic personal

Use for portfolios where authored video, portraiture, identity, and work previews form one system.

### Emotional illustration

Use for care, education, behavior, and human services when a symbolic gesture should establish meaning before workflow detail.

If the hero contains three equal messages, redesign it.

## Art direction

Create one ownable visual world connected to product meaning.

Choose:

- Documentary photography for operational credibility
- Editorial product photography for tactile or prestige value
- A single illustration grammar across hero, proof, and conversion
- One physical material and lighting model for 3D stages
- Product UI artifacts for technical evidence
- Cultural collage for research, fashion, or strategy
- Motion or video when capability is inherently kinetic

Do not use generic gradient blobs as the only visual concept. Do not mix watercolor, clay 3D, stock photography, and neon diagrams without a thesis that requires all four.

Use consistent crop, lighting, material, and color treatment across chapters. Repeat the hero world at the final conversion when it creates closure.

## Component architecture

Select components by purpose. Use six to ten major components for a substantial page; use fewer when the brief is smaller.

| Purpose | Component families |
| --- | --- |
| Navigation | Micro utility navigation; capsule navigation; edge navigation only with a conventional mobile transformation |
| Proof | Logo rail; recognition or events ledger; metric cluster; expert quote; controlled testimonial rail; media recognition grid; product, code, performance, or security artifact |
| Work | Editorial case-study index; artifact vignette; portfolio media wall; selected-work carousel; capability shelf; campaign triptych |
| Information architecture | Strategic question matrix; industry ledger; capability accordion with preview; service stack; taxonomy count menu |
| Product education | Numbered process; alternating product steps; live preset grid; code/API panel; diagnostic module; integration orbit; platform selector; narrative bento grid |
| Narrative and media | Asymmetric research collage; floating image constellation; human photo ribbon; social video stage; dark discovery chapter; particle or physical-material stage |
| Conversion | Inline capture; scenic conversion card; oversized contact poster; milestone; quiet conversation CTA |
| Footer | Saturated mega footer; deep brand field; mega wordmark footer |

Layer proof. Logos alone are insufficient when outcomes, experts, work, integrations, events, or operational evidence are available.

Repeat at least one component anatomy three or more times to establish a system. Do not make every component a rounded card.

## Page narrative

Build a sequence, not a stack of sections:

```text
Identity or proposition
→ immediate category comprehension
→ first tangible artifact
→ adoption or authority proof
→ workflow or capability explanation
→ outcomes and human evidence
→ deeper work, culture, or ecosystem
→ contextual conversion
→ final brand-world conversion
→ memorable footer
```

Adapt the sequence to the available proof. Do not fabricate missing proof. If little evidence exists, build credibility through transparent process, product mechanics, team authority, or clearly stated limitations.

## Copy direction

- State what the product does, for whom, and why it matters.
- Replace abstract claims with mechanisms, outcomes, or evidence.
- Use short labels and specific calls to action.
- Avoid interchangeable phrases such as “empower,” “revolutionize,” “seamless,” and “next-generation” unless immediately substantiated.
- Do not invent testimonials, metrics, customer logos, funding, awards, or product capabilities.
- Use real or clearly labeled representative content because content length controls layout.

## Motion

Use motion to expose capability, causality, navigation, depth, or sequence.

Use restrained patterns:

- 400–900ms reveals with deliberate easing
- 8–32px reveal distance
- 1.02–1.04 media hover scale
- 4–8px arrow translation
- 8–32px parallax with stable text
- 20–45s marquees with pause controls
- 1–4° object tilt
- 250–450ms accordion transitions

These are research-derived starting ranges, not requirements. Match the product’s motion character.

Every animated system needs reduced motion, keyboard equivalence, pause control where applicable, stable layout, and a static fallback for video, particles, WebGL, or canvas.

## Responsive semantic design

Do not shrink desktop composition.

- Preserve semantic reading order.
- Recompose billboard artwork for portrait crops.
- Move spatial annotations into flow.
- Convert media rails to manual snap or grids.
- Convert ledgers to labeled rows.
- Convert complex tables to disclosures only when comparison is preserved.
- Keep product artifacts readable through crops, overflow, or step reveals.
- Separate decorative giant type from semantic text.
- Preserve primary action and essential proof.
- Replace complex 3D/video with a meaningful poster where performance or motion preferences require it.

## Accessibility baseline

- Target WCAG AA contrast for functional content.
- Do not encode status by color alone.
- Provide visible focus.
- Preserve keyboard navigation.
- Use meaningful alt text for informative media.
- Provide captions and controls for video.
- Keep carousel movement manual or pausable.
- Use semantic rows, lists, tables, and headings.
- Hide duplicate decorative giant type from assistive technology.
- Provide reduced-motion and reduced-transparency behavior.
- Keep essential content outside canvas or WebGL.

Do not claim conformance without appropriate testing.

## Implementation discipline

- Inspect existing code, dependencies, components, and tokens first.
- Use the project’s framework and conventions.
- Reuse stable primitives without shipping their unmodified default appearance.
- Use CSS Grid for intentional two-dimensional composition.
- Use absolute positioning only for purposeful spatial designs with a mobile transformation.
- Keep semantic DOM order independent from decorative positioning.
- Verify third-party dependencies before importing them.
- Use one icon family and one geometry system.
- Build all relevant loading, empty, error, disabled, success, and permission states.
- Do not add unrelated product features.

## Anti-slop rejection gate

Reject or revise when:

- The page could represent another product after replacing nouns.
- The hero mixes several equal ideas.
- Every section is a centered rounded-card grid.
- Aesthetic effects are disconnected from product meaning.
- The visual world changes without narrative reason.
- Typography roles drift between chapters.
- The page has no proof beyond generic logos.
- Product UI is too small to read.
- Mobile is a shrunken desktop collage.
- Motion lacks reduced-motion behavior.
- Functional text is low contrast or too small.
- Conversion appears only in the footer.
- Copy contains unsupported claims or generic calls to action.
- The design uses novelty without operational clarity.

## Render and critique loop

After implementation:

1. Render the primary route.
2. Inspect the full page and key viewports.
3. Check the first viewport, chapter rhythm, density, type architecture, media treatment, proof sequence, and conversion path.
4. Test responsive transformations and interaction states.
5. Run accessibility, type, lint, build, and smoke checks available to the project.
6. Revise until the design thesis is visible in every major chapter.

Use this critique table:

| Area | Intended system | Observed result | Correction | Status |
| --- | --- | --- | --- | --- |

## Completion gate

Finish only when:

- One dominant hero idea is clear.
- One typographic voice, visual world, grid logic, and proof architecture are coherent.
- Density changes deliberately.
- Six to ten purpose-led chapters—or a proportionate smaller set—form a complete narrative.
- Proof follows claims.
- A contextual and final conversion path exists when conversion is relevant.
- Responsive order preserves meaning.
- Accessibility and motion fallbacks are defined.
- The implemented interface is rendered and inspected.
- The route builds and functions without relevant errors.

Return the design thesis, implemented path, key system choices, validation performed, assumptions, and blockers.
