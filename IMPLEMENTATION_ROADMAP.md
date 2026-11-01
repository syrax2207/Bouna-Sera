# 5. Eight-Batch Implementation Roadmap

## Execution rule

Execute one batch at a time in Google AI Studio Build mode. Before modifying code, inspect the current implementation. Preserve working features. Do not regenerate the entire project unnecessarily.

At the end of every batch, AI Studio must report changed files, checks run, known issues and whether the batch acceptance criteria passed.

## Batch 1 — Project inspection & creative foundation

Tasks:
- Inspect project framework, files, dependencies and scripts.
- Read the installed frontend-design skill.
- Confirm skill is actually available to the Build agent.
- Establish design direction and tokens.
- Define responsive principles.
- Define section architecture and content data model.
- Record business information gaps.
- Create project documentation in the repository.

Do not build the whole site.

Acceptance:
- Existing app setup understood.
- Design system documented.
- Architecture documented.
- No unrelated files changed.
- No unverified business facts invented.

## Batch 2 — Design system & core components

Tasks:
- Add global design tokens and typography.
- Configure fonts/fallbacks.
- Create reusable container, button, section heading and image components.
- Add motion helpers only where useful.
- Implement accessible focus styles.
- Check responsive base layout.

Acceptance:
- Consistent visual tokens.
- Core components work.
- No horizontal overflow at mobile widths.
- Keyboard focus visible.

## Batch 3 — Navigation & hero

Tasks:
- Build desktop navigation.
- Build mobile navigation drawer.
- Implement hero composition.
- Add headline reveal and image entrance.
- Add primary/secondary CTA.
- Add scroll state for header.
- Add reduced-motion behavior.

Acceptance:
- Navigation links work.
- Drawer opens/closes and is keyboard accessible.
- Hero is legible at all breakpoints.
- No animation blocks content.

## Batch 4 — Editorial homepage sections

Tasks:
- Brand introduction.
- Signature experiences.
- Story/atmosphere section.
- Editorial image/text compositions.
- Scroll reveal and restrained hover motion.

Acceptance:
- Distinct composition per section.
- No repetitive template layout.
- Content is verified or clearly placeholder.
- Mobile order and spacing are deliberate.

## Batch 5 — Interactive menu

Tasks:
- Build data-driven menu.
- Category switching.
- Search.
- Verified dietary filters only.
- Dish detail dialog.
- Empty state and reset.
- Responsive controls.
- Accessible keyboard/focus handling.

Acceptance:
- Category and search filters work together correctly.
- Dish details are accurate.
- Modal works with keyboard and touch.
- No fake order/cart functionality.
- Menu data is separate from UI.

## Batch 6 — Gallery & reviews

Tasks:
- Build asymmetric gallery.
- Add responsive images.
- Add lightbox.
- Add next/previous and keyboard support.
- Add touch support where feasible.
- Add genuine reviews only if verified.

Acceptance:
- Lightbox opens/closes correctly.
- Keyboard support works.
- Gallery images have appropriate alt text.
- Review sources are attributed.
- Omit review section if no genuine material is available.

## Batch 7 — Visit/contact & conversion

Tasks:
- Add verified address.
- Add directions link/map.
- Add confirmed hours.
- Add call/WhatsApp links.
- Add reservation enquiry only if supported.
- Add mobile quick-action bar.
- Check every CTA.

Acceptance:
- No placeholder contact link presented as real.
- Directions resolve to correct business.
- Hours are current and owner-confirmed.
- Forms have real destinations or are explicitly demo-only.

## Batch 8 — QA, SEO & launch readiness

Tasks:
- Test desktop/tablet/mobile.
- Check accessibility and reduced motion.
- Check all interactive states.
- Run production build.
- Fix console errors.
- Check image sizes and loading.
- Add metadata and structured data using verified fields.
- Check title, description, canonical and social metadata.
- Check sitemap/robots if appropriate.
- Test links and contact actions.
- Prepare owner-review handover.

Acceptance:
- Build passes.
- No critical console errors.
- No broken controls.
- No mobile overflow.
- No fabricated claims.
- Remaining limitations documented.

## Quota-efficiency protocol

- Use one prompt per batch.
- Avoid repeated full-app redesigns.
- Ask the agent to inspect before editing.
- Request focused fixes with exact file/component scope.
- Do not ask it to re-explain completed work.
- Keep a concise `PROJECT_STATUS.md` with completed batches and known issues.
