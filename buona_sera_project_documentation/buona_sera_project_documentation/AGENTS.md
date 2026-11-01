# Agent Instructions

## Mission

Build a polished, trustworthy and accessible VEYRO concept website for Buona Sera Cafe, following the project documentation and installed skill system.

## Before every implementation task

1. Read `README.md`, `PROJECT_CONTEXT.md`, `PRD.md` and the relevant design/technical documents.
2. Inspect the current code and dependencies before proposing changes.
3. Identify which installed skills apply and read their actual `SKILL.md` files.
4. State the task scope, files likely to change and any assumptions.
5. Do not begin broad edits until the plan is clear.

## Required skill usage

- Visual design: `/skills/system_skills/frontend_design/SKILL.md`
- UI implementation: `/skills/baseline-ui/SKILL.md`
- Motion: `/skills/fixing-motion-performance/SKILL.md`
- Accessibility: `/skills/fixing-accessibility/SKILL.md`
- SEO: `/skills/system_skills/applet_seo/SKILL.md`
- Audit: `/skills/improve-ui/SKILL.md`

Use `SKILLS_REGISTRY.md` for activation and conflict rules.

## Non-negotiable rules

- This is an uncommissioned concept until the user explicitly states otherwise.
- Never imply the business has approved or commissioned the website.
- Never invent business details, menu items, prices, opening hours, offers, reviews, facilities or policies.
- Never present AI-generated or stock imagery as actual café photography.
- Keep unverified content out of public-facing factual UI.
- Do not create fake ordering, booking, payment or success flows.
- Do not add packages without checking the current dependency tree and obtaining approval where required.
- Do not overwrite existing project files without inspecting them.
- Do not expose secrets or collect visitor personal data unnecessarily.
- Preserve responsive, keyboard-accessible and reduced-motion behaviour.

## Implementation discipline

- Prefer small, focused components.
- Keep content data separate from UI.
- Use semantic HTML.
- Use buttons for actions and anchors for navigation.
- Provide visible focus styles.
- Use motion purposefully and avoid layout-thrashing animations.
- Avoid unnecessary abstractions and dependencies.
- Keep code readable and easy to hand off between AI tools.

## Audit discipline

`improve-ui` is read-only during audit. It must inspect, gather evidence, falsify false positives and produce a prioritised action plan. Product code changes happen only in a separate approved implementation step.

## Completion report

After each phase, report:
1. What changed.
2. Exact files changed.
3. Skills consulted.
4. Tests performed and results.
5. Known issues.
6. Any assumptions or unverified content.
7. Whether scope expanded.

Do not claim tests passed unless they were actually run.
