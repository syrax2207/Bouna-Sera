# Design System

> Provisional concept system for the Buona Sera Cafe website. Not an official brand guide.

## 1. Foundations

### Colour tokens

```css
:root {
  --color-ivory: #F4F0E8;
  --color-olive: #303B2F;
  --color-terracotta: #B76545;
  --color-espresso: #241F1B;
  --color-sage: #A5AA91;
  --color-soft-white: #FCFAF6;
}
```

Validate text/background contrast before use. Do not assume every palette pairing is accessible.

### Typography

- Display: one editorial serif.
- Interface/body: one neutral sans-serif.
- Body line height: comfortable and readable.
- Use tabular numerals for prices and numeric information where useful.
- Use balanced headings (`text-balance`) when supported.
- Avoid more font weights than the design requires.

### Spacing

Use a consistent spacing scale based on Tailwind spacing tokens. Prefer generous section spacing, consistent content gutters and predictable component gaps. Avoid arbitrary one-off values unless visually justified.

### Layout

- Mobile-first.
- Use a consistent maximum content width.
- Use CSS Grid/Flexbox for layout.
- Avoid fixed widths that cause overflow.
- Maintain readable text measure.
- Use responsive image aspect ratios and intentional crops.

## 2. Component principles

Build reusable components only when they have a clear repeated purpose. Likely components:
- `SiteHeader`
- `MobileNavigation`
- `HeroSection`
- `SectionHeading`
- `StorySection`
- `MenuExplorer`
- `MenuCategoryTabs`
- `MenuItem`
- `GalleryGrid`
- `Lightbox`
- `VisitSection`
- `ContactCTA`
- `SiteFooter`

Keep components focused. Keep business content in structured data rather than embedding it throughout JSX.

## 3. Interaction states

Every interactive component must define:
- Default
- Hover (where applicable)
- Focus-visible
- Active/pressed
- Disabled (where applicable)
- Loading/error (only if asynchronous behaviour exists)

Do not communicate state by colour alone.

## 4. Buttons and links

- Use semantic `<button>` for actions.
- Use `<a>` for navigation and external destinations.
- Ensure labels describe the action.
- Provide visible focus rings.
- Avoid using clickable `div` elements.
- Ensure touch targets are comfortably usable.

## 5. Menu interaction

- Prefer simple accessible buttons for category selection.
- Expose selected state (`aria-pressed` or a suitable tab pattern).
- Keep category changes predictable and keyboard operable.
- Do not hide the entire menu behind hover-only interaction.
- Preserve content access when JavaScript is unavailable where practical.

## 6. Gallery / modal

- Use semantic controls.
- Provide accessible names for previous/next/close controls.
- Manage focus when opening and closing.
- Close with Escape.
- Return focus to the invoking element.
- Prevent background interaction while modal is open.
- Respect reduced motion.

## 7. Responsive breakpoints

Use the project's Tailwind v4 defaults unless there is a documented reason to customise them. Test actual content at:
- 320–360 px narrow mobile
- 375–430 px common mobile
- 768 px tablet
- 1024 px small desktop
- 1280–1440 px desktop
- 1600 px wide desktop

These are test widths, not a requirement to add custom breakpoints.

## 8. Motion tokens

Keep durations short and purposeful. Define a small set of reusable durations/easings rather than inventing unique animation timing for every component. Never animate layout-heavy properties continuously. Prefer transform and opacity for movement/transition.

## 9. Anti-patterns

- Generic gradient backgrounds unrelated to the concept.
- Excessive rounded pills and floating glass cards.
- Overloaded hero with several competing CTAs.
- Tiny low-contrast metadata.
- Hover-only controls.
- Unnecessary parallax.
- Auto-playing audio/video.
- Long preloader or intro animation.
- Decorative cursor effects that harm usability.
- Unverified social proof or fabricated review content.
