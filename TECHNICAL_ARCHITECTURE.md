# 4. Technical Architecture

## 4.1 Proposed stack

- React
- Vite (if supported by the existing AI Studio project)
- Tailwind CSS (only if already configured or correctly integrated)
- Motion for React (`motion`)
- Lucide React (`lucide-react`)

Do not replace the project's framework or build setup without inspecting it first. AI Studio may generate a project with an existing configuration; preserve working foundations.

## 4.2 Dependencies

Potential additions:
```bash
npm install motion lucide-react
```

Only install if not already present and compatible.

Do not add GSAP, Three.js, multiple icon libraries or a component framework without a concrete requirement.

## 4.3 Suggested structure

```text
src/
  components/
    layout/
      SiteHeader.jsx
      SiteFooter.jsx
      MobileActionBar.jsx
    navigation/
      DesktopNavigation.jsx
      MobileNavigation.jsx
    sections/
      HeroSection.jsx
      IntroductionSection.jsx
      SignatureSection.jsx
      StorySection.jsx
      ReviewsSection.jsx
      VisitSection.jsx
    menu/
      MenuSection.jsx
      MenuFilters.jsx
      MenuItem.jsx
      MenuDialog.jsx
    gallery/
      GallerySection.jsx
      GalleryLightbox.jsx
    ui/
      Button.jsx
      SectionHeading.jsx
      Container.jsx
  data/
    business.js
    menu.js
    gallery.js
    reviews.js
  hooks/
  animations/
  styles/
  utils/
  App.jsx
  main.jsx
```

Keep architecture proportionate. Do not create files/components that add no value.

## 4.4 Data separation

Keep business content separate from presentation:
- `business.js`: approved name, address, phone, hours, links, social profiles.
- `menu.js`: approved categories and dishes.
- `gallery.js`: image paths, alt text, source/permission notes.
- `reviews.js`: genuine approved excerpts and source links.

Use explicit status markers during development, e.g. `verified`, `needs_confirmation`, `placeholder`. Do not accidentally render internal status labels to customers.

## 4.5 State management

Local React state is sufficient for:
- Mobile menu open/closed.
- Active menu category.
- Search query.
- Dietary filter.
- Selected dish.
- Gallery index/open state.

No global state library is needed for the initial prototype.

## 4.6 Routing

A single-page website can use anchor navigation initially. Add routing only if separate pages become necessary, such as a dedicated full menu page or privacy page.

## 4.7 Contact actions

- Phone: `tel:` link using confirmed number.
- WhatsApp: `https://wa.me/` using confirmed international-format number.
- Maps: owner-confirmed Google Maps URL or verified place link.
- Social: official profile URLs only.

Never fabricate URLs or use a personal number without permission.

## 4.8 Forms and backend

No backend in initial prototype.

A form must not pretend to submit if it has no destination. Options:
1. Use a real approved form endpoint.
2. Use a WhatsApp enquiry handoff with user-visible confirmation.
3. Keep it as a clearly labelled non-production demo and do not collect data.

Do not collect unnecessary personal information.

## 4.9 Images and assets

- Prefer owner-supplied assets.
- Track licensing/permission.
- Optimize large photos.
- Use responsive `srcset`/appropriate image sizing where feasible.
- Reserve image dimensions/aspect ratios to reduce layout shift.
- Lazy-load below-the-fold images.
- Hero image should be optimized and not lazy-loaded if it is the main LCP element.

## 4.10 Security and privacy

- No exposed API keys or secrets in frontend code.
- No unnecessary tracking scripts.
- Obtain owner approval before analytics or third-party embeds.
- Use HTTPS in production.
- Validate and sanitize any future form input.
- Avoid collecting payment or customer account information in this prototype.
