<!-- SEED: re-run /impeccable document once there's code to capture the actual tokens and components. -->

---
name: git.test
description: A test repository exploring elegant, restrained frontend design.
---

# Design System: git.test

## 1. Overview

**Creative North Star: "The Object in Light"**

A single object, perfectly lit, in a room with nothing else. The design does not compete with the content — it frames it, gives it room to breathe, and then gets out of the way. Every pixel of whitespace is intentional; every animation serves the narrative of revealing something worth seeing.

The visual language is Apple-informed but not Apple-derived: restrained color (neutral-dominant, one accent at ≤10% surface), a single sans-serif family working across all roles through weight and size alone, and choreographed motion that unfolds the page as a sequence of deliberate reveals rather than a static document.

**Key Characteristics:**
- Content as the only hero — design recedes
- Whitespace as compositional element, not empty space
- One type family, many voices — weight and scale do the work
- Motion as narrative — each scroll brings something into the light
- No decoration that doesn't earn its place

This system explicitly rejects SaaS landing-page clichés (gradient text, hero metrics, identikit card grids, tiny uppercase eyebrow labels above every section), AI-generated design tells (cream-warm backgrounds, Fraunces/Playfair, numbered section markers), and any decoration that exists because "landing pages do this."

## 2. Colors

**The Restrained Rule.** One accent color occupies ≤10% of any given screen. Its rarity is the point. The rest of the palette is neutral: true off-white, near-black, and a short gray ramp connecting them. No warm-tinted backgrounds — the neutrality lets content and imagery carry the warmth.

### Primary
- **[to be resolved during implementation]** (#HEX): The sole accent. Used on primary CTAs, selected states, and the rare deliberate highlight. Appears on ≤10% of surface at any moment.

### Neutral
- **Ink** (#HEX): Body text and primary content. Near-black, not pure #000.
- **Paper** (#HEX): Page background. True off-white at chroma 0, not warm-tinted.
- **Surface** (#HEX): Card or elevated surface backgrounds when needed.
- **Faint** (#HEX): Borders, dividers, subtle separations.
- **Muted** (#HEX): Secondary text, captions. Must still pass 4.5:1 on Paper.

## 3. Typography

**Font Family:** Single sans-serif. [font pairing to be chosen at implementation]

**Character:** Weight contrast replaces font contrast. A single well-chosen sans family with committed weight/size differentiation is stronger than a timid display+body pair. Light display weights for headlines, regular for body, medium for emphasis — all from one family, each with a clear role.

### Hierarchy
- **Display** (Light, clamp(2.5rem, 6vw, 5rem), line-height: 1): Hero headlines only. Maximum one per page.
- **Headline** (Regular, clamp(1.5rem, 4vw, 2.5rem), line-height: 1.15): Section titles.
- **Title** (Medium, 1.25rem, line-height: 1.3): Card titles, feature labels.
- **Body** (Regular, 1rem, line-height: 1.6): Running text. Cap at 65–75ch. `text-wrap: pretty` for prose, `text-wrap: balance` for h1–h3.
- **Label** (Medium, 0.875rem, letter-spacing: 0.02em, uppercase): Buttons, navigation, metadata.

### Named Rules
**The One Voice Rule.** One type family across the entire surface. No second font for "variety." Variety comes from the content, the spacing, and the motion — not from mixing typefaces.

## 4. Elevation

Motion energy is Choreographed, so the system uses a layered elevation model — but sparingly. Surfaces are flat at rest. Elevation (shadows, transforms) appears only as a response to state: hover lifts, modals float, sticky nav gains a subtle backdrop blur on scroll. The default is flat; depth is earned by interaction.

**The Flat-By-Default Rule.** No permanent shadows on static elements. Elevation is a state, not a property. Cards, if used, sit flush with the page until interacted with.

## 5. Components

*No components exist yet. This section will be populated when `/impeccable document` re-runs in scan mode against real code.*

## 6. Do's and Don'ts

### Do:
- **Do** let content occupy the majority of visual weight on every screen
- **Do** use generous, asymmetric whitespace — rhythm beats uniformity
- **Do** keep the accent rare — one colored element per fold, maximum
- **Do** animate entrance as revelation — content coming into the light, not sliding in from the dark
- **Do** respect `prefers-reduced-motion` with instant or crossfade alternatives

### Don't:
- **Don't** use SaaS landing-page clichés: gradient text, hero metric templates, icon+heading+text card grids, tiny uppercase tracked eyebrows above every section
- **Don't** warm-tint the page background — cream, sand, beige, "paper" warmth is the saturated AI default of 2026
- **Don't** use gradient text (`background-clip: text`) — emphasis comes from weight, size, or position, never from gradient fills
- **Don't** place side-stripe borders (>1px `border-left`/`border-right`) as colored accents on cards or list items
- **Don't** use glassmorphism, backdrop-blur cards, or decorative blurs
- **Don't** add numbered section markers (01 / 02 / 03) unless the sections form a genuine ordered sequence
- **Don't** gate content visibility on animation — every element must render legibly before any animation fires
- **Don't** use monospace as a decorative "technical" signal — this is not a developer-tool brand
