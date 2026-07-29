# NexAI Design Tokens

This file defines the current product UI baseline. Use semantic tokens; do not copy hex values throughout feature CSS.

## 1. Brand assets

- Official packaged logo: `../assets/nexai-ai-logo.svg`
- Logo mark: purple-to-orange gradient contained inside the official SVG.
- Minimum digital lockup height: 24px. Recommended product-shell height: 28–32px.
- Preserve clear space around the mark equal to at least half the mark height.
- On a collapsed rail, crop/display the mark portion of the official horizontal SVG. Do not squeeze the full wordmark.
- Never recolor, redraw, rotate, add effects to, or place competing graphics behind the logo.

## 2. Semantic colors

```css
:root {
  --nx-purple: #7417ff;
  --nx-purple-hover: #6310df;
  --nx-purple-soft: #f1eaff;
  --nx-purple-tint: #f5f1ff;

  --nx-orange: #f26322;
  --nx-logo-orange: #fe6702;

  --nx-ink: #1d1d1f;
  --nx-ink-strong: #17171c;
  --nx-muted: #6e6e73;
  --nx-subtle: #9a9aa0;

  --nx-canvas: #ffffff;
  --nx-surface: #f6f6f8;
  --nx-surface-2: #efeff3;
  --nx-surface-violet: #eef1ff;
  --nx-surface-parchment: #f4f2ee;

  --nx-line: rgba(0, 0, 0, .09);
  --nx-line-strong: rgba(0, 0, 0, .14);
  --nx-focus: rgba(116, 23, 255, .25);

  --nx-success: #08755f;
  --nx-warning: #b45f06;
  --nx-danger: #b42318;

  --nx-dark-navy: #081425;
  --nx-dark-panel: #0b1422;
  --nx-dark-neutral: #17171c;
}
```

### Color usage

- Purple: primary actions, selected navigation, active tabs, identity accents, verified/product-progress emphasis.
- Purple-soft: selected background, lightweight highlighting, informative certification/evidence panels.
- Orange: time-sensitive opportunity, deadline, momentum, or growth signal. Do not use orange as a second primary CTA.
- Success green: completed/validated state. It does not automatically mean formal certification.
- Dark navy/charcoal: immersive hero, focused project workbench, serious evidence/certification moments.
- White/gray: default application background and information surfaces.

### Gradient rule

Do not add decorative CSS gradients to product surfaces. Allowed cases:

1. the gradient already embedded in the official logo;
2. a supplied/generated photographic asset;
3. a specifically approved marketing illustration.

## 3. Typography

```css
--nx-font-text: "SF Pro Text", system-ui, -apple-system, BlinkMacSystemFont,
  "PingFang SC", "Microsoft YaHei", sans-serif;
--nx-font-display: "SF Pro Display", system-ui, -apple-system,
  "PingFang SC", sans-serif;
```

Use optical restraint. Chinese copy needs more line height than short English labels.

| Role | Desktop | Mobile | Weight | Line height | Tracking |
|---|---:|---:|---:|---:|---:|
| Display hero | 48–60 | 34–38 | 680–720 | 1.05–1.12 | -0.04em to -0.055em |
| Page title | 34–48 | 28–36 | 650–700 | 1.08–1.16 | -0.03em to -0.045em |
| Section title | 28–40 | 26–32 | 650–700 | 1.10–1.20 | -0.025em to -0.045em |
| Card title | 15–19 | 15–18 | 600–680 | 1.25–1.35 | -0.01em to -0.025em |
| Primary body | 13–15 | 14–16 | 400–500 | 1.55–1.75 | 0 |
| Dense body | 11–12 | 12–14 | 400–500 | 1.5–1.65 | 0 |
| Label/meta | 9–11 | 10–12 | 560–700 | 1.3–1.5 | 0–0.12em |

Rules:

- Do not make primary explanatory text smaller than 12px on desktop or 14px on mobile.
- 8–10px type is restricted to timestamps, short metadata, dense rails, and secondary proof labels.
- Use uppercase/letter-spaced English only for short eyebrow labels, never paragraphs.
- Avoid centered long paragraphs. Centering is reserved for short empty states or compact banners.
- Use real Chinese content when judging wrap and density.

## 4. Spacing

The product uses a 2px/4px-derived scale with repeated 8, 14, 16, 18, 22, 24, 28, 34, 44, and 68px intervals.

```css
--nx-space-1: 4px;
--nx-space-2: 6px;
--nx-space-3: 8px;
--nx-space-4: 10px;
--nx-space-5: 12px;
--nx-space-6: 14px;
--nx-space-7: 16px;
--nx-space-8: 18px;
--nx-space-9: 20px;
--nx-space-10: 22px;
--nx-space-11: 24px;
--nx-space-12: 28px;
--nx-space-13: 30px;
--nx-space-14: 34px;
--nx-space-15: 40px;
--nx-space-16: 44px;
--nx-space-17: 56px;
--nx-space-18: 68px;
```

Usage:

- 4–8px: icon/label and inline micro spacing.
- 10–14px: compact controls and dense rows.
- 14–18px: card gaps and component padding.
- 20–28px: primary card/panel padding.
- 30–44px: hero inner spacing and major content groups.
- 56–68px: editorial section separation.
- AI Passport free-board visual gap: exactly 14px.

## 5. Radius

```css
--nx-radius-xs: 5px;
--nx-radius-sm: 8px;
--nx-radius-control: 10px;
--nx-radius-control-lg: 12px;
--nx-radius-card: 16px;
--nx-radius-card-lg: 18px;
--nx-radius-panel: 20px;
--nx-radius-hero: 22px;
--nx-radius-feature: 24px;
--nx-radius-pill: 999px;
```

- Do not use one radius everywhere.
- Pills are for filters, compact status, avatars, and intentionally capsule-shaped buttons.
- Editorial certification CTAs may use 10–12px corners instead of pills.

## 6. Borders, depth, and transparency

- Default separation: `1px solid var(--nx-line)`.
- Active outline: `1px solid var(--nx-purple)`.
- Cards should not rely on shadow for separation.
- Allowed floating shadow: `0 14px 40px rgba(23,23,28,.13)` for overlays/companions.
- Allowed hero/image shadow: restrained, under 0.12 opacity, only when the hero needs separation from the canvas.
- Sticky bars and sidebars may use a translucent white surface plus blur when performance permits.
- Provide a solid white fallback under `prefers-reduced-transparency`.

## 7. Layout and grids

- App sidebar: 176px expanded, 64px compact.
- Standard page: `min(1240px, 100%)`, with 30px desktop horizontal padding.
- Certification/editorial page: up to 1380px in the current prototype.
- Desktop content grids: normally 2–4 tracks; choose based on reading order, not card count.
- Project workspace: compact learning rail + operation canvas + collapsible output pane.
- Community: focused two-column feed; do not add a redundant internal channel rail.

## 8. Responsive breakpoints

Current product baseline:

- Wide desktop: above 1080px.
- Intermediate desktop/tablet: 721–1080px.
- Mobile: 720px and below.
- Minimum supported width: 320px.

Rules:

- Mobile uses a top bar and off-canvas primary navigation.
- Convert multi-column information into one readable column; do not merely shrink frames.
- Keep primary actions full width when stacked.
- Horizontal tab strips may scroll when labels must remain intact.
- Disable free drag/resize when AI Passport enters a responsive single-column flow.
- Collapse the project output pane by default; keep the learning/task rail accessible.

## 9. Motion

- Hover/color transition: 160–200ms.
- Press: 100ms, `scale(.97)`; `.95` is acceptable for clearly tactile Apple-style controls.
- Sidebar/layout transition: about 240ms.
- Use smooth scrolling for in-page anchors.
- Respect `prefers-reduced-motion` and remove nonessential transform/scroll animation.
- Do not use bounce, continuous floating, or decorative parallax in certification, evidence, or job flows.

## 10. Accessibility

- Text contrast should meet WCAG AA.
- Focus ring: `3px solid var(--nx-focus)` with `2px` offset.
- Touch target: target 44px; never below 38px for a visible interactive control.
- Icon-only buttons require accessible names.
- Selection cannot depend only on color; use border, weight, indicator, or `aria-selected`.
- Use semantic landmarks, headings, lists, tabs, dialogs, and labels.

