# Implementation Roadmap

## Phase 0 — Documentation and environment verification
- [ ] Confirm documentation package reviewed.
- [ ] Inspect actual project tree and `package.json`.
- [ ] Confirm React, Tailwind and Motion versions.
- [ ] Confirm installed skills remain readable.
- [ ] Record current baseline; do not overwrite starter files unnecessarily.

**Exit condition:** Environment and current code state are understood.

## Phase 1 — Content and asset verification
- [ ] Verify business name and spelling.
- [ ] Verify address and map destination.
- [ ] Verify phone and WhatsApp permission.
- [ ] Verify hours.
- [ ] Obtain current approved menu and prices.
- [ ] Confirm reservation/contact expectations.
- [ ] Obtain logo and approved photography or decide on clearly labelled concept assets.
- [ ] Update `CONTENT_MODEL.md` and `ASSET_MANIFEST.md`.

**Exit condition:** Every visible factual claim has a status and source.

## Phase 2 — Design specification
- [ ] Review `CREATIVE_DIRECTION.md`.
- [ ] Finalise palette and type pairing after contrast and layout checks.
- [ ] Define desktop and mobile layout for each section.
- [ ] Define interaction states.
- [ ] Define motion intensity and reduced-motion behaviour.
- [ ] Create a page-level wireframe or section map.

**Exit condition:** Design direction is specific enough to implement without guessing.

## Phase 3 — Foundation
- [ ] Set up design tokens.
- [ ] Establish responsive container and typography utilities.
- [ ] Build shared header/footer/navigation.
- [ ] Confirm keyboard focus and semantic structure.
- [ ] Run an early responsive check.

**Exit condition:** Stable visual and technical foundation.

## Phase 4 — Core sections
- [ ] Hero.
- [ ] Story/introduction.
- [ ] Menu explorer.
- [ ] Gallery/lightbox.
- [ ] Visit information.
- [ ] Contact CTA.
- [ ] Footer.

**Exit condition:** All sections work with verified content or clearly marked private-demo placeholders.

## Phase 5 — Motion and polish
- [ ] Add only purposeful transitions.
- [ ] Check compositor-friendly animation properties.
- [ ] Test reduced motion.
- [ ] Check mobile performance.
- [ ] Avoid excessive scroll effects.

**Exit condition:** Motion enhances rather than obstructs the experience.

## Phase 6 — Audit and testing
- [ ] Run `improve-ui` read-only audit.
- [ ] Validate all links and controls.
- [ ] Test keyboard navigation and modal focus.
- [ ] Test responsive widths.
- [ ] Check image loading and layout shift.
- [ ] Check console/build output.
- [ ] Fix prioritised issues and re-audit.
- [ ] Complete `TEST_PLAN.md`.

**Exit condition:** No critical functional, accessibility or factual issues remain.

## Phase 7 — Portfolio packaging
- [ ] Capture desktop and mobile screenshots.
- [ ] Record project objective and concept status.
- [ ] Document actual features implemented.
- [ ] Document stack and design decisions.
- [ ] Do not claim business results or client approval.
- [ ] Add a clear concept-project disclosure to the VEYRO portfolio entry.

**Exit condition:** Portfolio presentation is honest and review-ready.

## Quota-conscious AI workflow

- Give the agent one bounded phase at a time.
- Ask it to inspect before editing.
- Request a plan and affected-file list before broad changes.
- Batch related small tasks into one implementation pass.
- Avoid repeatedly regenerating entire files.
- Ask for concise verification summaries and exact file paths.
- Preserve this documentation as the shared source of truth across AI tools.
