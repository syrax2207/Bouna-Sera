# 3. UX, Page Structure & Interaction Specification

## 3.1 Global navigation

### Desktop
- Brand wordmark on left.
- Anchor navigation in centre/right.
- Primary “Visit Us” or “Explore Menu” CTA.
- Transparent over hero if contrast remains accessible.
- Transitions to solid/ivory background after scroll.

### Mobile
- Wordmark left, menu control right.
- Accessible drawer or full-screen menu.
- Focus management while open.
- Escape closes the menu.
- Selecting an anchor closes the menu and scrolls to section.
- Body scroll is appropriately managed while drawer is open.

### Motion
- Underline reveal.
- Background/contrast transition.
- Staggered menu links.
- Short, interruptible transitions.

## 3.2 Hero

Purpose: communicate the cafe's identity immediately and create a clear route into the menu or visit information.

Elements:
- Optional eyebrow label.
- Large headline.
- Short supporting sentence.
- Primary menu CTA.
- Secondary directions CTA, only with verified destination.
- Strong photograph.
- Scroll cue.

Proposed headline direction (must be adapted to verified brand):
“Good food. Beautiful moments.”

Motion:
- Headline line reveal or staggered fade/translate.
- Background image slow scale from approximately 1.04 to 1.0.
- CTA fade/translate.
- Optional subtle desktop parallax only if performance remains good.

No intro animation should block content or navigation.

## 3.3 Brand introduction

- Two-column editorial composition.
- Real venue/food image.
- Section number or eyebrow.
- Owner-approved story.
- Short supporting copy.
- Optional anchor to menu.

Do not invent founding date, founder story, heritage or mission.

## 3.4 Signature experiences

- Three or four featured items/experiences, only after menu verification.
- Use varied editorial layouts.
- Dish name, short factual description and price only if confirmed.
- CTA links to relevant menu category.
- Hover image scale and subtle arrow movement.
- Scroll reveal with reduced-motion alternative.

## 3.5 Interactive menu

### Data model
Each menu item may contain:
- `id`
- `name`
- `category`
- `description`
- `price`
- `image`
- `dietaryTags`
- `availability`
- `allergenNote`
- `sourceStatus`

Only populate factual fields from owner-approved/current menu data.

### Features
- Category tabs/chips.
- Search by item name.
- Optional dietary filter, only when verified.
- Dish detail dialog.
- Clear empty state.
- Reset filters.
- Mobile horizontal category scroller with visible focus.
- No fake cart or ordering function unless real ordering is implemented.

### Interaction behavior
- Category changes update visible items.
- Motion transitions should not cause layout jumps.
- Modal closes via close button, Escape and backdrop click where appropriate.
- Focus is trapped/managed while modal is open and returned to trigger on close.
- Search input has a programmatic label.

## 3.6 Atmosphere/story section

- Owner-approved description.
- Real interior photographs.
- Seating/ambience claims only when verified.
- One large image and supporting details.
- Gentle reveal, minimal parallax.

## 3.7 Gallery

- Asymmetric grid.
- Responsive image sizes.
- Lightbox with previous/next.
- Escape to close.
- Arrow-key navigation.
- Touch swipe support where feasible.
- Image counter and accessible labels.
- Lazy-load non-critical images.
- Prevent background scrolling while open.

## 3.8 Reviews

- Use only genuine reviews.
- Preserve meaning; avoid misleading edits.
- Include source attribution and link where possible.
- Do not invent names, dates, stars or review totals.
- If verified reviews are unavailable, omit the section or replace it with a non-testimonial photo/story section.

## 3.9 Visit/contact

- Exact owner-confirmed address.
- Verified map destination.
- Confirmed phone and WhatsApp number.
- Confirmed operating hours.
- Reservation enquiry only if reservations are accepted.
- Form must have a real delivery destination before being presented as functional.
- If no backend exists, use an explicit WhatsApp enquiry flow or clearly state that the form is a demo.

### Mobile quick actions
A small bottom action bar may contain:
- Directions.
- Call.
Only render actions with verified destinations. Ensure it does not cover content or browser controls.

## 3.10 Footer

- Wordmark.
- Navigation.
- Address and contact.
- Hours.
- Social links only if official.
- Copyright.
- Back-to-top action.

## 3.11 Motion system

Use Motion for React for orchestrated/complex transitions and CSS for simple hover/focus states.

Suggested timing:
- Micro-interactions: 120–220ms.
- Component transitions: 220–450ms.
- Large section reveals: 450–750ms.
- Avoid long sequences that delay interaction.

Suggested easing:
- Smooth ease-out for entrances.
- Gentle spring only for small UI feedback.
- Avoid overshoot on large text and layout elements.

### Reduced motion
Respect `prefers-reduced-motion`. Disable or simplify parallax, large transforms and staggered reveals. Content must remain immediately readable.

## 3.12 Interaction intensity

| Area | Intensity | Reason |
|---|---|---|
| Hero | High | Brand impression |
| Navigation | Medium | Orientation |
| Menu | High | Core utility |
| Featured dishes | Medium | Visual discovery |
| Story | Low/medium | Reading comfort |
| Gallery | High | Photo exploration |
| Reviews | Low | Trust/readability |
| Contact | Low | Task completion |
| Footer | Low | Calm ending |
