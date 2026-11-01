---
name: nexai-brand-ui
description: Apply the NexAI product and brand UI system to product planning, UX/UI design, frontend implementation, and design QA. Use for NexAI pages, components, prototypes, extensions, redesigns, reviews, and cross-team handoffs.
---

# NexAI Brand UI

Use this skill whenever a task changes or extends a NexAI / 奈势 AI product surface. It packages the current product language, interaction constraints, content trust boundaries, and acceptance criteria used by the NexAI prototype.

The goal is not to make every screen look identical. The goal is to make every screen feel like the same product: restrained, evidence-driven, builder-oriented, trustworthy, and unmistakably NexAI.

## 1. Source-of-truth order

Resolve conflicts in this order:

1. Explicit requirements in the current user/task request.
2. Existing route, component behavior, and real content in the active NexAI repository.
3. This skill and its packaged references.
4. Saved screenshots under `assets/` as visual examples.
5. External references such as Apple, Codex, DeepLearning.AI, X, Kimi, Udacity, or Watcha.

External products may provide topology, interaction cues, or density references. They must never replace NexAI’s brand, content model, trust boundary, or naming.

## 2. Required reading by task

Read only the references needed for the task, but read each selected file completely.

- Any visual or frontend work: `references/design-tokens.md` and `references/components.md`.
- New page, route, or large redesign: also read `references/page-patterns.md`.
- Certification, AI Passport, evidence, projects, jobs, community identity, or AI review: also read `references/content-and-trust.md`.
- Implementation or review: also read `references/qa-checklist.md`.
- Early product definition: start from `templates/screen-brief.md`.

## 3. NexAI experience principles

Every meaningful product flow should reinforce this loop:

`真实任务 → 可检查交付物 → 过程证据 → 反馈 / 人工复核 → 我的 AI 护照 → 项目或岗位机会`

Apply these principles:

- Outcome before feature: explain what the user will make, prove, or unlock before listing tools.
- Real work over passive consumption: courses and tutorials must lead to a project, artifact, decision, or demonstrable capability.
- Evidence over decoration: verified evidence, contribution, review status, and project provenance are functional information, not badges for visual excitement.
- AI collaboration with user control: AI assists, proposes, organizes, and pre-reviews; the user confirms consequential actions and high-trust claims.
- Human accountability: formal certification and other high-stakes conclusions require named human review.
- One primary action per region: preserve hierarchy and avoid CTA competition.
- Progressive disclosure: keep default screens calm; expand directories, details, evidence, tools, and secondary panes only when needed.
- Brand restraint: purple is a signal, not a background habit. Orange indicates urgency or growth momentum, not routine navigation.

## 4. Visual non-negotiables

- Reuse the official NexAI logo from `assets/nexai-ai-logo.svg`. Never redraw or approximate it.
- Primary product purple is `#7417FF`. Product action orange is `#F26322`; the logo gradient may use canonical `#FE6702`.
- Default surfaces are white, parchment gray, or pale blue-violet. Dark navy/charcoal surfaces are reserved for immersive heroes, project creation, or high-focus evidence areas.
- Do not add decorative gradients to UI surfaces. The logo gradient and photographic treatment are exceptions.
- Do not use routine card shadows. Separate content with spacing, surface tone, and `1px` borders. A restrained shadow is allowed only for floating overlays, modals, sticky translucent bars, or image-led marketing heroes.
- Use rounded geometry consistently: 10–12px controls, 16–18px cards, 20–24px major panels, and full pills only for pills/filters/buttons that are intentionally capsule-shaped.
- Use Phosphor Icons in the product implementation. Match stroke weight and never mix icon families on one screen.
- Avoid card overload. If every block becomes a rounded white rectangle, pause and re-establish hierarchy using sections, dividers, lists, or one dominant surface.
- Avoid fake data, fake accreditation, automatic-authorship claims, and unsupported job guarantees.

## 5. Button and control grammar

- Primary: one compact purple action, normally 44px high. Use a pill in the core product shell; use an 10–12px rounded rectangle in editorial/certification heroes when the selected pattern calls for it.
- Secondary: white or transparent surface with purple or context-appropriate outline.
- Quiet action: text link or icon button; do not compete with the primary CTA.
- Icon control: 44 × 44px target where space permits. Smaller visible icons still need a touch target near 40–44px.
- Pressed feedback: `scale(.97)` or `scale(.95)` for about 100ms. Avoid bounce or playful spring motion in high-trust workflows.
- Focus: visible 3px purple-tinted ring with 2px offset.
- Disabled: visually muted and non-interactive; never remove the label needed to understand the unavailable action.

## 6. Role-specific workflow

### Product manager

1. Fill `templates/screen-brief.md`.
2. Define the real user outcome and the primary action.
3. Identify the deliverable, evidence, review owner, and opportunity connection.
4. Select an existing page pattern before inventing a new one.
5. Mark facts, assumptions, and changing market data separately.
6. Hand off acceptance criteria including desktop, intermediate, and mobile behavior.

### UI / product designer

1. Start from the token and component files, not a blank aesthetic exploration.
2. Reuse an existing topology from `references/page-patterns.md`.
3. Use brand purple for identity, selected state, and the single primary action.
4. Define default, hover, focus, pressed, expanded/collapsed, empty, loading, success, and error states where relevant.
5. Check the layout at wide desktop, intermediate desktop, and mobile before handoff.
6. Include real Chinese copy and realistic data density. Do not design with lorem ipsum.

### Frontend engineer

1. Inspect existing components, CSS tokens, routes, and assets before adding new primitives.
2. Extend shared tokens rather than hardcoding near-duplicate colors, radii, or spacing.
3. Preserve established runtime, routing, accessibility semantics, and build/deployment files.
4. Implement the main conversion/task flow end to end; visible core controls cannot be static decoration.
5. Keep responsive behavior explicit. Do not proportionally shrink desktop UI until text becomes unreadable.
6. Build, test, visually inspect, check console errors, and complete `references/qa-checklist.md`.

## 7. Page selection rules

Choose the closest packaged pattern:

- Marketing/home aggregation: home sequence pattern.
- Course-like real project: project-detail pattern.
- Guided AI creation: full-screen project follow room.
- Personal evidence and growth: AI Passport board.
- Community: focused information feed.
- Certification: career-proof detail page.
- Jobs/opportunities: evidence-to-role connection, with changing market data clearly labeled.

Do not combine several patterns into one screen unless the user journey genuinely requires it.

## 8. Content and naming rules

- User-facing name: `我的 AI 护照` or `AI护照`; never restore `AI地图`.
- Primary navigation label: `项目`; contextual labels may use `PBL 实战项目`.
- Primary navigation label: `社区`; legacy route names may remain internal.
- Primary navigation label: `机会`; avoid switching back to `职业` as the channel name.
- Brand line: `Empower Every AI Builder` / `成就每一位 AI 创造者`.
- Explain certification as evidence plus human review. Do not call it a degree, international-standard credential, or guaranteed employment outcome.
- Label salary, hiring demand, rankings, and market figures with source/date context and a change disclaimer.

## 9. Output contract

For a NexAI design/build task, return or produce:

1. The selected page pattern and user outcome.
2. Reused tokens/components and any justified extensions.
3. Working responsive implementation or a clear implementation spec.
4. Main interaction states.
5. Evidence/trust handling notes when relevant.
6. Verification result using `references/qa-checklist.md`.
7. Explicit remaining assumptions or unavailable source material.

## 10. Stop conditions

Stop and request direction when:

- a requested external style would overwrite NexAI identity rather than inform layout;
- the action would publish, submit, certify, or expose user data without authorization;
- a formal certification claim lacks a human review path;
- a logo, partner mark, job figure, certification fact, or source asset is missing and guessing would create a false claim;
- a major new route has no clear user outcome or primary action.

## 11. Packaged artifacts

- `NexAI-品牌UI规范.html` — browsable team guideline.
- `references/design-tokens.md` — color, type, spacing, radius, elevation, motion, responsive rules.
- `references/components.md` — reusable component anatomy and states.
- `references/page-patterns.md` — route and layout patterns.
- `references/content-and-trust.md` — evidence, certification, AI, privacy, and job-data constraints.
- `references/qa-checklist.md` — shared acceptance gate.
- `templates/screen-brief.md` — PM/design/engineering kickoff template.
- `assets/` — official logo and representative validated screenshots.
- `examples/` — browsable UI style examples for the packaged page patterns; start at `examples/index.html`.

