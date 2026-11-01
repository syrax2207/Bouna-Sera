# 2. Creative Direction & Design System

## 2.1 Creative concept

**Contemporary Italian Editorial Dining**

The visual experience should feel like a carefully art-directed dining journal: warm, tactile, elegant, photographic and human.

It should not look like:
- A generic restaurant template.
- A food-delivery marketplace.
- A SaaS dashboard.
- A neon cyberpunk landing page.
- A gallery of identical rounded cards.

The design must remain appropriate to the real venue. If owner-provided branding conflicts with the proposed direction, adapt the system rather than forcing the concept.

## 2.2 Proposed palette

These are concept tokens, not verified brand colors.

| Token | Hex | Usage |
|---|---|---|
| Background | `#F5F0E7` | Main page background |
| Surface | `#EAE2D4` | Alternate sections |
| Text | `#262820` | Primary text |
| Olive | `#596449` | Primary accent |
| Terracotta | `#B66B4E` | Secondary accent |
| Muted gold | `#B69A68` | Fine decorative details |
| White | `#FFFCF6` | Light surfaces |
| Border | `#D8D0C3` | Subtle separators |
| Muted text | `#716F65` | Secondary text |

### Color rules
- Use warm ivory as the main canvas.
- Use dark charcoal/olive for strong contrast.
- Terracotta is an accent, not a dominant background.
- Gold should be used sparingly.
- Ensure all text/background combinations meet WCAG AA contrast where practical.
- Do not rely on color alone to communicate state.

## 2.3 Typography

Proposed type pairing:
- Display: **Cormorant Garamond**
- Body/UI: **DM Sans**
- Micro-labels: **DM Mono**

### Hierarchy
- H1: expressive, large, restrained line length.
- H2: editorial section headings.
- H3: dish/feature titles.
- Body: comfortable reading size and line height.
- Labels: uppercase or small caps only when legible.
- Buttons: clear, concise, high contrast.

Use locally hosted or reliable font loading where feasible. Include sensible system fallbacks. Avoid loading unnecessary font weights.

## 2.4 Layout system

- Max content width: approximately 1240–1360px.
- Wide editorial sections may break out of the main container.
- Desktop grid: 12 columns where useful.
- Tablet: 8-column or simplified grid.
- Mobile: single-column flow with deliberate image/text ordering.
- Use generous section spacing, but avoid excessive empty space that hides content.
- Prefer asymmetry and varied composition over repetitive card grids.

Suggested spacing scale:
`4, 8, 12, 16, 24, 32, 48, 64, 80, 112, 144` pixels.

Suggested radius:
- Small controls: 4–8px.
- Image frames: 0–4px or deliberately varied.
- Large card rounding should be rare.

## 2.5 Photography direction

Prioritize real, owner-approved photographs:
- Hero: strongest real ambience or signature-food photograph.
- Food: clear, appetizing, natural light, truthful presentation.
- Interior: seating, lighting, materials and atmosphere.
- Gallery: mix of wide, portrait and detail images.

Image rules:
- Never imply stock imagery depicts the actual venue.
- Track image source, permission and intended use.
- Avoid watermarked images.
- Use optimized WebP/AVIF where supported.
- Define focal points for responsive crops.
- Provide descriptive alt text for meaningful images.
- Decorative images should use empty alt text.

## 2.6 Composition principles

- One dominant visual idea per section.
- Use typography as a visual element.
- Keep CTAs obvious.
- Balance text and photography.
- Avoid placing text over busy photos without a legibility treatment.
- Use thin rules, small labels and editorial numbering selectively.
- Keep decorative elements subordinate to food and business information.

## 2.7 Component styling

Buttons:
- Primary: olive/dark fill, light text.
- Secondary: transparent or ivory with border.
- Hover: subtle color shift and 1–2px movement.
- Focus: clearly visible outline.
- Active: small pressed feedback.

Links:
- Underline or arrow reveal where appropriate.
- No misleading hover effects on non-clickable text.

Menu items:
- Prefer editorial list or mixed image/text layout.
- Avoid identical cards for every dish.
- Price alignment must be clear.
- Dietary labels only if verified.

## 2.8 Design quality guardrails

- No arbitrary gradients.
- No excessive glassmorphism.
- No huge cursor-following effects.
- No scroll hijacking.
- No autoplay audio/video.
- No motion that delays access to content.
- No tiny low-contrast labels.
- No mobile horizontal overflow.
