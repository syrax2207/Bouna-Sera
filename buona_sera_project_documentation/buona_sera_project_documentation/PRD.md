# Product Requirements Document (PRD)

## 1. Summary

Create a polished, responsive, single-page café website concept for Buona Sera Cafe. It should introduce the experience, help visitors explore the menu and atmosphere, and make practical visit/contact information easy to find.

The work is an independent VEYRO concept, not an authorised business website.

## 2. Problem statement

A potential café visitor often needs to answer a few questions quickly:
- What kind of place is this?
- What food and drinks can I expect?
- What does the atmosphere look like?
- Where is it?
- When can I visit?
- How can I contact the business?

A well-structured website can bring these answers together in a branded, mobile-friendly experience. The current digital footprint and exact gaps must be verified; do not claim the café has no website or lacks particular services without checking.

## 3. Goals

### Primary goals
1. Communicate the café's identity and experience clearly.
2. Make menu discovery easy.
3. Show atmosphere through approved imagery.
4. Provide accurate visit information.
5. Offer a clear, low-friction contact/enquiry path.

### Secondary goals
- Demonstrate VEYRO's visual design and frontend engineering quality.
- Showcase considered motion and interaction.
- Establish a reusable process for future hospitality projects.

## 4. Non-goals

- Online checkout or payment processing.
- Food delivery marketplace integration.
- Live table inventory or confirmed reservation engine.
- Customer accounts or loyalty system.
- Unverified ordering, booking or delivery promises.
- Admin/CMS backend in the first concept iteration.
- Copying another café's identity or using VEYRO's studio identity as the café's identity.
- Publishing the concept as the official business website without permission.

## 5. Primary users and jobs

| User | Job to be done |
|---|---|
| First-time visitor | Understand the café and decide whether to visit |
| Returning visitor | Find current menu and practical details |
| Nearby visitor | Locate the café and contact it |
| Group organiser | Find a contact route to ask about group arrangements, if offered |

## 6. Information architecture

Single-page structure, with anchored navigation:

1. Header / navigation
2. Hero
3. Introduction / café story
4. Signature experience or food highlights
5. Menu explorer
6. Atmosphere / gallery
7. Visit information
8. Contact / enquiry call-to-action
9. Footer

Optional sections such as events, private dining, delivery or reservations are excluded unless confirmed by the business.

## 7. Functional requirements

### FR-01 Navigation
- Provide clear navigation to the main page sections.
- On small screens, provide an accessible mobile navigation control.
- Indicate active/hover/focus states.
- Navigation must not obscure content or trap keyboard users.

### FR-02 Hero
- Communicate the café name and a concise concept introduction.
- Use an approved image or clearly identified temporary concept image.
- Include one primary action, such as “Explore the menu”.
- A secondary visit/contact action may be included only when the destination is real and verified.

### FR-03 Story
- Provide a short, factual introduction.
- Until owner-approved copy exists, label text as concept copy or use neutral placeholder content.
- Do not invent founding dates, founders, heritage, sourcing claims or culinary credentials.

### FR-04 Menu explorer
- Organise menu content into categories only when supported by a verified menu.
- Category switching must work by mouse, touch and keyboard.
- Show item name and price only when verified.
- Do not invent dish descriptions, dietary labels, availability or prices.
- If no approved menu is available, show a clearly labelled sample layout in the private demo, not as a live claim.

### FR-05 Gallery
- Display approved photos or assets with usage rights.
- Provide accessible image descriptions.
- If a lightbox is implemented, support close control, Escape, focus management and sensible focus return.
- Do not imply AI-generated food imagery is a photograph of the actual café.

### FR-06 Visit details
- Display address, opening hours, map link and phone only after verification.
- Use a map/directions link that points to the verified business location.
- Make phone links usable on mobile.
- Do not display stale third-party review counts as live data.

### FR-07 Contact / enquiry
- Use only verified contact destinations.
- A WhatsApp CTA may be used only if the business number is confirmed and the channel is appropriate.
- Pre-filled message text must be transparent and must not imply a confirmed booking/order.
- Do not create fake checkout, order confirmation or booking confirmation flows.

### FR-08 Responsive behaviour
- Support narrow mobile, standard mobile, tablet, laptop and wide desktop.
- No horizontal overflow at supported widths.
- Touch targets and text remain usable on mobile.

### FR-09 Motion
- Use motion to clarify hierarchy and provide feedback, not as decoration that delays tasks.
- Respect `prefers-reduced-motion`.
- Follow `fixing-motion-performance` constraints.

## 8. Non-functional requirements

- Accessibility target: WCAG 2.2 AA practices where applicable.
- Semantic HTML and keyboard operability.
- Responsive layout and readable type.
- Optimised images and minimal layout shift.
- No console errors in normal user flows.
- No broken links or nonfunctional controls.
- Good Core Web Vitals practices.
- No unnecessary dependencies or heavy animation libraries beyond the existing project setup without approval.

## 9. Content and trust requirements

Every business-specific claim must be traceable to an approved source. Maintain status labels:
- `VERIFIED`: confirmed from current authoritative source or owner.
- `NEEDS_CONFIRMATION`: plausible research finding not approved.
- `CONCEPT_COPY`: invented only as design placeholder; not a business claim.
- `PLACEHOLDER`: must be replaced before public launch.

## 10. Acceptance criteria

The concept is ready for review when:
- All planned sections are present and navigable.
- The layout is responsive and has no horizontal overflow.
- Menu interactions work and use only approved data or visibly marked sample content.
- Gallery controls work with keyboard and touch.
- Contact links point to verified destinations or are disabled/marked in demo.
- Reduced-motion preferences are respected.
- Keyboard focus is visible and modal focus is managed correctly.
- Images have appropriate alternative text.
- No fake testimonials, ratings, offers, prices, business claims or conversion results exist.
- The project is clearly labelled as a VEYRO concept.
- The test plan has been completed and known defects documented.
