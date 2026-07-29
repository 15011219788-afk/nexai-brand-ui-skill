# NexAI Component Grammar

## 1. Primary navigation

### Expanded sidebar

- Width: 176px.
- White/translucent surface with a 1px right border.
- Official logo, optional `测试版` marker, seven or fewer visible channels.
- Navigation row: 38–44px high, 10–12px radius.
- Active state: purple text/icon on purple-soft background.
- Footer contains brand line and login/account action.

### Compact sidebar

- Width: 64px.
- Show the official mark crop, not a compressed full wordmark.
- Icon-only rows retain accessible labels/tooltips.

### Mobile navigation

- 58px fixed top bar.
- Centered official logo; menu and account controls at the edges.
- Main sidebar becomes off-canvas.

## 2. Buttons

### Primary

- Height: 44px default, 48px in large hero/checkout moments.
- Purple fill, white label, 14px default type.
- One primary action per region.

### Secondary

- White/transparent background with purple or contextual outline.
- Same height and comparable padding as the paired primary action.

### Quiet/text

- Purple text, no filled surface.
- Use for details, navigation, and low-risk alternatives.

### Circular icon

- 44 × 44px preferred.
- Use for arrows, close, expand/collapse, and utility actions.

Required states: default, hover, focus-visible, pressed, disabled, loading where relevant.

## 3. Cards and panels

### Standard card

- White surface, 1px neutral border, 16–18px radius.
- 16–24px padding.
- Title → description → evidence/status → action.
- Avoid equal visual weight for every card on the page.

### Major feature panel

- 20–24px radius.
- Image-led, dark focus, or pale violet treatment.
- Use one dominant message and one primary action.

### Evidence panel

- Calm trust styling: icon/label, claim, source/provenance, review status, date or version, optional reviewer.
- Green means completed/validated state; formal certification must still say who reviewed it.

### Empty state

- Short heading, one explanatory sentence, one recovery action.
- No decorative illustration is required unless an approved brand asset exists.

## 4. Hero patterns

### Image-led career/certification hero

- Dark navy left copy region and authentic right-weighted work image.
- Eyebrow/breadcrumb, strong outcome headline, one primary + one secondary CTA, audience metadata.
- Follow immediately with a proof strip.
- Never imply degree status, accreditation, or employment guarantee without evidence.

### Project detail hero

- Immersive dark panel with breadcrumb, level/duration metadata, project title, evidence statement, primary `开始实战` CTA, and image/video panel.
- Convert course language into real task, deliverable, evidence, human review, AI Passport, and opportunity semantics.

### Home banner

- Image-led but compact; home is an aggregation surface, not a landing-page scroll marathon.
- The content order below the banner is fixed in `page-patterns.md`.

## 5. Section heading

- Title and short description share a compact baseline when space allows.
- Optional quiet action aligns to the right.
- Typical top gap: 28–34px for application pages, 56–68px for editorial certification sections.

## 6. Filter pills and tabs

- Filter row: compact 38px controls, 6–8px gaps.
- Default state is quiet gray; selected state uses purple text plus purple-soft surface.
- Sticky filter bars may use translucent white and restrained floating shadow.
- Tabs need `role=tab`, `aria-selected`, and a non-color selection indicator.
- Mobile tab strips may scroll horizontally rather than wrap into unreadable labels.

## 7. Forms and inputs

- Input height: 40–48px; textarea sized to task complexity.
- Border: neutral 1px; focus uses purple ring and/or border.
- Labels remain visible; placeholder is not a replacement for a label.
- Autosave state should be quiet but explicit.
- Consequential AI actions explain what files/data will change and what requires confirmation.

## 8. Progress and directory

- Progress is compact: label, `current / total`, track, and current step.
- Do not duplicate the same progress in multiple columns.
- In the project follow room, progress and project directory are one compact collapsible card.
- Directory labels describe actual tasks, not generic module numbers only.

## 9. AI companion and workbench

### XiaoNai companion

- Persistent but collapsible.
- Learns context through explicit user answers and voluntary connections.
- Never implies silent reading of external accounts.
- Lightweight ability checks are advisory, not certification.

### Project follow room

- Left: project progress/directory, teaching video, ~100-character expandable transcript, complete current-task form and run action.
- Middle: Codex-like operation canvas. It stays blank before action and shows operation results afterward.
- Right: preview/files/evidence pane, collapsed by default and opened on demand.
- Do not move teaching transcript or task form into the middle operation canvas.
- Do not turn the workbench into a generic chat summary page.

## 10. AI Passport board

- Cards are directly draggable/resizable on wide desktop; no separate edit mode.
- Invisible resize hot zones on four edges plus bottom-right corner.
- 14px visual gap, magnetic alignment, collision-aware reflow, no accidental vertical holes.
- Cards sharing a row align top and bottom.
- Maximize control appears only on hover/focus and is reversible.
- System-generated `AI 能力卡` is first and cannot be deleted.
- At intermediate widths, switch to a readable single-column flow and disable drag/resize.

## 11. Community post

- Focused feed plus recommendation rail.
- Header contains recommendation/following tabs only.
- Post footer has four outlined capsule actions: like, comment, star, smile.
- Verified evidence is a calm trust label, not an oversized celebratory badge.

## 12. Certification and jobs

- Sequence: outcome hero → proof strip → learning experience → modules → real project → assessment → credential output → related roles.
- Show concrete learning modes and deliverables.
- Formal result requires human review.
- Job tabs may show salary, education, experience, demand, skills, qualities, and path.
- Salary/demand data must state that it changes with the market.
- Certification is not an employment guarantee.

