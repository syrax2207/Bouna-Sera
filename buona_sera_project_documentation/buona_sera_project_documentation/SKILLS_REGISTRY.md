# Skills Registry & Usage Policy

## 1. Purpose

This file records the installed skill set reported by Google AI Studio and defines when each skill should be consulted. It does not replace the source `SKILL.md` files.

## 2. Installed skill inventory

| Skill | Path | Responsibility |
|---|---|---|
| System `frontend-design` | `/skills/system_skills/frontend_design/SKILL.md` | Visual direction, design quality and frontend design principles |
| Project `baseline-ui` | `/skills/baseline-ui/SKILL.md` | Component discipline, Tailwind conventions and UI engineering |
| Project `fixing-motion-performance` | `/skills/fixing-motion-performance/SKILL.md` | Animation performance and compositor-friendly motion |
| Project `fixing-accessibility` | `/skills/fixing-accessibility/SKILL.md` | Accessibility, keyboard support, focus and semantic controls |
| System `applet_seo` | `/skills/system_skills/applet_seo/SKILL.md` | SEO and metadata |
| Project `improve-ui` | `/skills/improve-ui/SKILL.md` | Read-only UI audit and evidence-based remediation planning |

Supporting files reported:
- `/skills/improve-ui/references/plan-template.md`
- `/skills/improve-ui/agents/openai.yaml`

The AI Studio report states these files were read back and verified. Re-verify paths if the workspace is reset or moved.

## 3. Activation triggers

- **Visual concept, layout, typography, colour, page composition:** consult `frontend-design`.
- **Component creation, responsive implementation, Tailwind patterns:** consult `baseline-ui`.
- **Animation, transitions, scroll-linked behaviour, performance issues:** consult `fixing-motion-performance`.
- **Forms, navigation, menus, dialogs, keyboard/focus or accessibility work:** consult `fixing-accessibility`.
- **Metadata, structured data, indexing and social cards:** consult `applet_seo`.
- **Design review or visual quality audit:** run `improve-ui` as a read-only audit first.

## 4. Authority and conflict resolution

1. Safety, factual integrity, privacy and user trust override all design preferences.
2. Accessibility and functional correctness override purely aesthetic preferences.
3. `frontend-design` guides creative direction.
4. `baseline-ui` governs implementation conventions.
5. `fixing-motion-performance` governs animation implementation and performance.
6. `fixing-accessibility` governs accessibility requirements.
7. `applet_seo` governs SEO/metadata.
8. `improve-ui` audits and reports; it must not directly modify product code during its audit phase.

If two skills conflict, identify the exact conflict, explain the impact and choose the more restrictive rule for accessibility, performance and data integrity. Do not silently discard a skill instruction.

## 5. Audit workflow

1. Ask `improve-ui` to inspect the target UI and gather evidence.
2. Require contract/structure checks and runtime verification where applicable.
3. Falsify suspected issues before accepting them.
4. Produce a prioritised top-three action plan.
5. Do not let the audit skill edit application code.
6. Implement approved fixes using the relevant engineering/accessibility/motion skills.
7. Re-run the audit and tests.

## 6. Dependency discipline

The installed skills are instructions, not proof that every optional package exists. Before importing any package, inspect `package.json` and lockfile. Do not add `clsx`, `tailwind-merge`, Radix, Base UI or other packages unless the project requires them and the user approves the dependency change.
