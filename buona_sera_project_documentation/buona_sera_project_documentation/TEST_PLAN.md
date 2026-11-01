# Test Plan

## 1. Test objectives

Verify that the concept is factually responsible, usable, responsive, accessible and performant.

## 2. Functional tests

| ID | Test | Expected result |
|---|---|---|
| F-01 | Click each desktop navigation link | Correct section is reached |
| F-02 | Open/close mobile navigation | Works by pointer and keyboard; state is announced |
| F-03 | Change menu category | Correct category content appears |
| F-04 | Use menu controls by keyboard | All controls are reachable and operable |
| F-05 | Open gallery item | Correct image and accessible dialog appear |
| F-06 | Close gallery with Escape | Dialog closes and focus returns to trigger |
| F-07 | Use previous/next gallery controls | Correct image appears; controls have accessible names |
| F-08 | Click map link | Opens verified map destination |
| F-09 | Click phone/WhatsApp CTA | Opens only verified contact destination |
| F-10 | Check footer links | No broken or placeholder public links |

## 3. Responsive tests

Test at 320, 360, 390, 430, 768, 1024, 1280, 1440 and 1600 px widths.

Check:
- No horizontal overflow.
- No clipped headings or controls.
- Images retain intentional crops.
- Navigation remains usable.
- Menu items remain readable.
- CTA buttons fit narrow screens.
- Footer columns collapse sensibly.

## 4. Accessibility tests

- Keyboard-only navigation.
- Visible focus indicator on every interactive control.
- Logical heading hierarchy.
- Semantic landmarks.
- Accessible names for icon-only controls.
- Sufficient text and control contrast.
- Correct image alt text.
- Dialog focus management and Escape behaviour.
- Reduced-motion preference.
- No colour-only communication of state.
- Screen-reader review of navigation and menu interactions.

Target WCAG 2.2 AA practices. Automated tools are useful but do not replace manual keyboard and screen-reader checks.

## 5. Motion and performance tests

- Confirm animations primarily use transform and opacity where appropriate.
- Check no repeated layout thrashing.
- Confirm reduced-motion mode removes or substantially reduces nonessential movement.
- Check scroll performance on a mid-range mobile device.
- Check image sizes, loading priority and layout shift.
- Inspect browser console and network failures.
- Use Lighthouse or equivalent as a diagnostic, not as the sole quality measure.

## 6. Content integrity tests

- Every displayed business fact has a verification status.
- No fake review quotes or ratings.
- No invented menu prices or availability.
- No invented opening hours or services.
- No fake reservation/order confirmation.
- No stock/AI image represented as an actual café photo.
- Concept status is disclosed in portfolio/demo context.

## 7. Browser coverage

At minimum, test current versions of:
- Chrome desktop and Android Chrome.
- Safari on iOS, if available.
- Firefox desktop.
- Edge desktop.

## 8. Defect severity

- **P0 Blocker:** data/privacy risk, misleading business claim, site unusable.
- **P1 Critical:** core navigation or primary CTA broken; major accessibility failure.
- **P2 Major:** responsive layout defect or important interaction failure.
- **P3 Minor:** visual inconsistency or low-impact polish issue.

## 9. Test report template

| Test ID | Result | Evidence | Defect | Follow-up |
|---|---|---|---|---|
| F-01 | NOT RUN | — | — | — |
