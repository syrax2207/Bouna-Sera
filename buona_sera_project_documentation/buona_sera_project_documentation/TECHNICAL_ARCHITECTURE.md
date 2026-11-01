# Technical Architecture

## 1. Reported environment

The AI Studio installation report states:
- React 19
- Tailwind CSS v4
- `motion` dependency `^12.23.24`
- Node.js, npm, npx, git and shell access
- Project-level skill discovery through `SKILL.md` files and project instructions

**Before implementation:** inspect `package.json`, lockfile, `src/`, build configuration and current app entry points. Treat the report as environment-provided evidence, not a substitute for checking the current repository.

## 2. Architecture approach

Use a small client-side React application appropriate for a single-page café concept. Avoid introducing a backend or complex state management without a demonstrated requirement.

Suggested separation:

```text
src/
  app/
    App.tsx
  components/
    layout/
    navigation/
    ui/
  sections/
    HeroSection.tsx
    StorySection.tsx
    MenuSection.tsx
    GallerySection.tsx
    VisitSection.tsx
    ContactSection.tsx
  data/
    business.ts
    menu.ts
    gallery.ts
  hooks/
  lib/
  styles/
    index.css
```

Adjust to the actual existing project structure; do not force this exact tree if the starter template differs.

## 3. Data architecture

Keep business facts separate from presentation:
- `business.ts`: name, address, hours, phone, map URL and verification metadata.
- `menu.ts`: categories and menu items with name, description, price, availability and verification status.
- `gallery.ts`: image path, alt text, source, licence/permission and whether it depicts the actual café.

Never place unverified facts into the production-facing data object.

## 4. State

Use local React state for:
- Mobile navigation open/closed.
- Selected menu category.
- Gallery/lightbox open state and selected image.

Avoid global state libraries for this scope.

## 5. Styling

Use Tailwind CSS v4 conventions already present in the project. Keep design tokens centralised in the main stylesheet or the project's existing token mechanism.

The installed `baseline-ui` skill mentions a `cn` helper using `clsx` and `tailwind-merge`. Those packages are optional and were not installed according to the report. Do not import them unless dependencies are deliberately added and verified. Use simple class composition or a small local helper if needed.

## 6. Motion

Use the existing `motion` package only where useful. Confirm its import API against the installed version and package documentation before implementation. Use transform/opacity for most animated transitions. Avoid layout-thrashing effects.

## 7. External services

Potential external destinations:
- Google Maps directions link.
- `tel:` phone link.
- WhatsApp click-to-chat link.

Only wire a destination after confirming the correct URL/number and the business's preferred contact method. No API keys should be embedded in frontend source.

## 8. SEO and metadata

Use the existing system `applet_seo` skill. Ensure:
- Accurate title and description.
- Canonical URL only when a real approved domain exists.
- Open Graph/Twitter metadata.
- LocalBusiness/Restaurant structured data only with verified fields.
- No fabricated ratings, price range, hours or social profiles.

## 9. Performance

- Use appropriately sized images and modern formats where supported.
- Lazy-load below-the-fold images.
- Prioritise the hero asset without overloading it.
- Set image dimensions/aspect ratios to reduce layout shift.
- Avoid large dependencies and excessive animation.
- Check mobile performance on a throttled connection.

## 10. Security and privacy

- Do not collect personal data in the concept.
- Do not create a form that appears to submit unless it actually does.
- Do not store contact details or user submissions.
- Do not expose secrets, API keys or private business information.
- External links should use safe link attributes where relevant.
