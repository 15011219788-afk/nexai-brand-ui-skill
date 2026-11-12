# 奈势AI v1.3 ⇄ Astryx 核心 token 映射

由 `scripts/emit.mjs` 从 `tokens.json` 生成。Astryx 版本：meta/astryx@4705e676（2026-11-12 clone）；核心 token 清单取自 `packages/core/src/theme/tokens.stylex.ts`（共 211 个，不含 syntax / data 两个领域层）。

**覆盖率：179 / 211（84.8%）**。对不上 32 个，全部是多色分类色（见第 2 节）。

命名规则：奈势变量 `--nx-X` 去掉 `nx-` 就是 Astryx 的 `--X`。主题包（theme-nexai）里写 `tokens: {'--X': [浅色值, 深色值]}`，值直接取 tokens.json 里的 `value`。单值 token（间距、圆角、动效等）两种模式相同。

## 1. 映射表

### 边框（1/1）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--border-width` | `--nx-border-width` | 1px | 同浅色 |

### 颜色（66/98）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--color-accent` | `--nx-color-accent` | #6857E7 (nx-purple) | #6857E7 (nx-purple) |
| `--color-accent-muted` | `--nx-color-accent-muted` | #F1F0FD (nx-mist) | #3C237C (nx-purple-deep) |
| `--color-background-blue` | ❌ 对不上 | — | — |
| `--color-background-body` | `--nx-color-background-body` | #F6F6F8 (nx-surface) | #262626 (nx-ink) |
| `--color-background-card` | `--nx-color-background-card` | #FFFFFF (nx-white) | #313030 (nx-neutral-dk-20) |
| `--color-background-cyan` | ❌ 对不上 | — | — |
| `--color-background-error-inverted` | `--nx-color-background-error-inverted` | #B42318 (nx-danger) | #DD6858 (nx-error-dk-60) |
| `--color-background-gray` | `--nx-color-background-gray` | #E8E8EB (nx-neutral-90) | #3D3C3C (nx-neutral-dk-25) |
| `--color-background-green` | ❌ 对不上 | — | — |
| `--color-background-inverted` | `--nx-color-background-inverted` | #262626 (nx-ink) | #F6F6F8 (nx-surface) |
| `--color-background-muted` | `--nx-color-background-muted` | #F6F6F8 (nx-surface) | #1B1B1B (nx-neutral-dk-10) |
| `--color-background-orange` | ❌ 对不上 | — | — |
| `--color-background-pink` | ❌ 对不上 | — | — |
| `--color-background-popover` | `--nx-color-background-popover` | #FFFFFF (nx-white) | #3D3C3C (nx-neutral-dk-25) |
| `--color-background-purple` | `--nx-color-background-purple` | #F1F0FD (nx-mist) | #3C237C (nx-purple-deep) |
| `--color-background-red` | ❌ 对不上 | — | — |
| `--color-background-surface` | `--nx-color-background-surface` | #FFFFFF (nx-white) | #262626 (nx-ink) |
| `--color-background-teal` | ❌ 对不上 | — | — |
| `--color-background-yellow` | ❌ 对不上 | — | — |
| `--color-border` | `--nx-color-border` | #E8E8EB (nx-neutral-90) | rgba(246, 246, 248, 0.10) |
| `--color-border-blue` | ❌ 对不上 | — | — |
| `--color-border-cyan` | ❌ 对不上 | — | — |
| `--color-border-emphasized` | `--nx-color-border-emphasized` | #87878C (nx-neutral-55) | #949499 (nx-neutral-dk-60) |
| `--color-border-error` | `--nx-color-border-error` | #B42318 (nx-danger) | #FF9989 (nx-error-dk-75) |
| `--color-border-gray` | `--nx-color-border-gray` | #CCCCCF (nx-neutral-80) | #575457 (nx-neutral-dk-35) |
| `--color-border-green` | ❌ 对不上 | — | — |
| `--color-border-info` | `--nx-color-border-info` | #6857E7 (nx-purple) | #BBBBFE (nx-lavender) |
| `--color-border-orange` | ❌ 对不上 | — | — |
| `--color-border-pink` | ❌ 对不上 | — | — |
| `--color-border-purple` | `--nx-color-border-purple` | #BBBBFE (nx-lavender) | #5743B7 (nx-purple-35) |
| `--color-border-red` | ❌ 对不上 | — | — |
| `--color-border-success` | `--nx-color-border-success` | #08755F (nx-success) | #84C9B4 (nx-success-dk-75) |
| `--color-border-teal` | ❌ 对不上 | — | — |
| `--color-border-warning` | `--nx-color-border-warning` | #A15204 (nx-warning-40) | #F4A468 (nx-warning-dk-75) |
| `--color-border-yellow` | ❌ 对不上 | — | — |
| `--color-error` | `--nx-color-error` | #B42318 (nx-danger) | #F78676 (nx-error-dk-70) |
| `--color-error-muted` | `--nx-color-error-muted` | #FFECE8 (nx-error-95) | #4B3330 |
| `--color-icon-accent` | `--nx-color-icon-accent` | #6857E7 (nx-purple) | #BBBBFE (nx-lavender) |
| `--color-icon-blue` | ❌ 对不上 | — | — |
| `--color-icon-cyan` | ❌ 对不上 | — | — |
| `--color-icon-disabled` | `--nx-color-icon-disabled` | #A2A2A7 (nx-neutral-65) | #7B7B7F (nx-neutral-dk-50) |
| `--color-icon-error` | `--nx-color-icon-error` | #B42318 (nx-danger) | #FF9989 (nx-error-dk-75) |
| `--color-icon-gray` | `--nx-color-icon-gray` | #6E6E73 (nx-gray) | #BDBDC1 (nx-neutral-dk-75) |
| `--color-icon-green` | ❌ 对不上 | — | — |
| `--color-icon-info` | `--nx-color-icon-info` | #6857E7 (nx-purple) | #BBBBFE (nx-lavender) |
| `--color-icon-orange` | ❌ 对不上 | — | — |
| `--color-icon-pink` | ❌ 对不上 | — | — |
| `--color-icon-primary` | `--nx-color-icon-primary` | #262626 (nx-ink) | #F6F6F8 (nx-surface) |
| `--color-icon-purple` | `--nx-color-icon-purple` | #6857E7 (nx-purple) | #BBBBFE (nx-lavender) |
| `--color-icon-red` | ❌ 对不上 | — | — |
| `--color-icon-secondary` | `--nx-color-icon-secondary` | #6E6E73 (nx-gray) | #BDBDC1 (nx-neutral-dk-75) |
| `--color-icon-success` | `--nx-color-icon-success` | #08755F (nx-success) | #84C9B4 (nx-success-dk-75) |
| `--color-icon-teal` | ❌ 对不上 | — | — |
| `--color-icon-warning` | `--nx-color-icon-warning` | #A15204 (nx-warning-40) | #F4A468 (nx-warning-dk-75) |
| `--color-icon-yellow` | ❌ 对不上 | — | — |
| `--color-info` | `--nx-color-info` | #6857E7 (nx-purple) | #6857E7 (nx-purple) |
| `--color-info-muted` | `--nx-color-info-muted` | #F1F0FD (nx-mist) | #3C237C (nx-purple-deep) |
| `--color-neutral` | `--nx-color-neutral` | rgba(38, 38, 38, 0.06) | rgba(246, 246, 248, 0.12) |
| `--color-on-accent` | `--nx-color-on-accent` | #FFFFFF (nx-white) | #FFFFFF (nx-white) |
| `--color-on-dark` | `--nx-color-on-dark` | #FFFFFF (nx-white) | #FFFFFF (nx-white) |
| `--color-on-error` | `--nx-color-on-error` | #FFFFFF (nx-white) | #262626 (nx-ink) |
| `--color-on-error-muted` | `--nx-color-on-error-muted` | #8F0201 (nx-error-30) | #FFAFA2 (nx-error-dk-80) |
| `--color-on-info` | `--nx-color-on-info` | #FFFFFF (nx-white) | #FFFFFF (nx-white) |
| `--color-on-info-muted` | `--nx-color-on-info-muted` | #3C237C (nx-purple-deep) | #BBBBFE (nx-lavender) |
| `--color-on-light` | `--nx-color-on-light` | #262626 (nx-ink) | #262626 (nx-ink) |
| `--color-on-success` | `--nx-color-on-success` | #FFFFFF (nx-white) | #262626 (nx-ink) |
| `--color-on-success-muted` | `--nx-color-on-success-muted` | #035846 (nx-success-30) | #99D5C3 (nx-success-dk-80) |
| `--color-on-warning` | `--nx-color-on-warning` | #FFFFFF (nx-white) | #262626 (nx-ink) |
| `--color-on-warning-muted` | `--nx-color-on-warning-muted` | #773701 (nx-warning-30) | #FFB37C (nx-warning-dk-80) |
| `--color-overlay` | `--nx-color-overlay` | rgba(38, 38, 38, 0.40) | rgba(0, 0, 0, 0.56) |
| `--color-overlay-hover` | `--nx-color-overlay-hover` | rgba(38, 38, 38, 0.05) | rgba(246, 246, 248, 0.06) |
| `--color-overlay-pressed` | `--nx-color-overlay-pressed` | rgba(38, 38, 38, 0.09) | rgba(246, 246, 248, 0.10) |
| `--color-shadow` | `--nx-color-shadow` | rgba(60, 35, 124, 0.10) | rgba(0, 0, 0, 0.30) |
| `--color-skeleton` | `--nx-color-skeleton` | #E8E8EB (nx-neutral-90) | #3D3C3C (nx-neutral-dk-25) |
| `--color-success` | `--nx-color-success` | #08755F (nx-success) | #6EBDA6 (nx-success-dk-70) |
| `--color-success-muted` | `--nx-color-success-muted` | #D5FBEE (nx-success-95) | #2C3F3A |
| `--color-text-accent` | `--nx-color-text-accent` | #6857E7 (nx-purple) | #BBBBFE (nx-lavender) |
| `--color-text-blue` | ❌ 对不上 | — | — |
| `--color-text-cyan` | ❌ 对不上 | — | — |
| `--color-text-disabled` | `--nx-color-text-disabled` | #A2A2A7 (nx-neutral-65) | #7B7B7F (nx-neutral-dk-50) |
| `--color-text-error` | `--nx-color-text-error` | #B42318 (nx-danger) | #FF9989 (nx-error-dk-75) |
| `--color-text-gray` | `--nx-color-text-gray` | #6E6E73 (nx-gray) | #BDBDC1 (nx-neutral-dk-75) |
| `--color-text-green` | ❌ 对不上 | — | — |
| `--color-text-info` | `--nx-color-text-info` | #6857E7 (nx-purple) | #BBBBFE (nx-lavender) |
| `--color-text-orange` | ❌ 对不上 | — | — |
| `--color-text-pink` | ❌ 对不上 | — | — |
| `--color-text-primary` | `--nx-color-text-primary` | #262626 (nx-ink) | #F6F6F8 (nx-surface) |
| `--color-text-purple` | `--nx-color-text-purple` | #6857E7 (nx-purple) | #BBBBFE (nx-lavender) |
| `--color-text-red` | ❌ 对不上 | — | — |
| `--color-text-secondary` | `--nx-color-text-secondary` | #6E6E73 (nx-gray) | #BDBDC1 (nx-neutral-dk-75) |
| `--color-text-success` | `--nx-color-text-success` | #08755F (nx-success) | #84C9B4 (nx-success-dk-75) |
| `--color-text-teal` | ❌ 对不上 | — | — |
| `--color-text-warning` | `--nx-color-text-warning` | #A15204 (nx-warning-40) | #F4A468 (nx-warning-dk-75) |
| `--color-text-yellow` | ❌ 对不上 | — | — |
| `--color-tint-hover` | `--nx-color-tint-hover` | #262626 (nx-ink) | #F6F6F8 (nx-surface) |
| `--color-track` | `--nx-color-track` | #E8E8EB (nx-neutral-90) | #3D3C3C (nx-neutral-dk-25) |
| `--color-warning` | `--nx-color-warning` | #B45F06 (nx-warning) | #E89454 (nx-warning-dk-70) |
| `--color-warning-muted` | `--nx-color-warning-muted` | #FFEDE1 (nx-warning-95) | #483628 |

### 动效时长（10/10）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--duration-exit` | `--nx-duration-exit` | var(--nx-duration-fast) | 同浅色 |
| `--duration-fast` | `--nx-duration-fast` | 125ms | 同浅色 |
| `--duration-fast-max` | `--nx-duration-fast-max` | 165ms | 同浅色 |
| `--duration-fast-min` | `--nx-duration-fast-min` | 95ms | 同浅色 |
| `--duration-medium` | `--nx-duration-medium` | 300ms | 同浅色 |
| `--duration-medium-max` | `--nx-duration-medium-max` | 400ms | 同浅色 |
| `--duration-medium-min` | `--nx-duration-medium-min` | 225ms | 同浅色 |
| `--duration-slow` | `--nx-duration-slow` | 700ms | 同浅色 |
| `--duration-slow-max` | `--nx-duration-slow-max` | 935ms | 同浅色 |
| `--duration-slow-min` | `--nx-duration-slow-min` | 525ms | 同浅色 |

### 缓动（4/4）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--ease-entrance` | `--nx-ease-entrance` | cubic-bezier(0.24, 1, 0.4, 1) | 同浅色 |
| `--ease-exit` | `--nx-ease-exit` | cubic-bezier(0.3, 0, 0.6, 0.6) | 同浅色 |
| `--ease-move` | `--nx-ease-move` | cubic-bezier(0.24, 1, 0.4, 1) | 同浅色 |
| `--ease-standard` | `--nx-ease-standard` | cubic-bezier(0.24, 1, 0.4, 1) | 同浅色 |

### 焦点环（4/4）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--focus-outline-color` | `--nx-focus-outline-color` | var(--nx-color-border-accent) | 同浅色 |
| `--focus-outline-offset` | `--nx-focus-outline-offset` | 2px | 同浅色 |
| `--focus-outline-style` | `--nx-focus-outline-style` | solid | 同浅色 |
| `--focus-outline-width` | `--nx-focus-outline-width` | 2px | 同浅色 |

### 字体（3/3）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--font-family-body` | `--nx-font-family-body` | MiSans, 'PingFang SC', 'Microsoft YaHei', sans-serif | 同浅色 |
| `--font-family-code` | `--nx-font-family-code` | "JetBrains Mono", "SF Mono", Menlo, Consolas, monospace | 同浅色 |
| `--font-family-heading` | `--nx-font-family-heading` | var(--nx-font-family-body) | 同浅色 |

### 字号（12/12）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--font-size-2xl` | `--nx-font-size-2xl` | 1.875rem | 同浅色 |
| `--font-size-2xs` | `--nx-font-size-2xs` | 0.625rem | 同浅色 |
| `--font-size-3xl` | `--nx-font-size-3xl` | 2.375rem | 同浅色 |
| `--font-size-3xs` | `--nx-font-size-3xs` | var(--nx-font-size-2xs) | 同浅色 |
| `--font-size-4xl` | `--nx-font-size-4xl` | 3rem | 同浅色 |
| `--font-size-4xs` | `--nx-font-size-4xs` | var(--nx-font-size-2xs) | 同浅色 |
| `--font-size-5xl` | `--nx-font-size-5xl` | 3.75rem | 同浅色 |
| `--font-size-base` | `--nx-font-size-base` | 1rem | 同浅色 |
| `--font-size-lg` | `--nx-font-size-lg` | 1.25rem | 同浅色 |
| `--font-size-sm` | `--nx-font-size-sm` | 0.875rem | 同浅色 |
| `--font-size-xl` | `--nx-font-size-xl` | 1.5rem | 同浅色 |
| `--font-size-xs` | `--nx-font-size-xs` | 0.75rem | 同浅色 |

### 字重（4/4）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--font-weight-bold` | `--nx-font-weight-bold` | 700 | 同浅色 |
| `--font-weight-medium` | `--nx-font-weight-medium` | 500 | 同浅色 |
| `--font-weight-normal` | `--nx-font-weight-normal` | 400 | 同浅色 |
| `--font-weight-semibold` | `--nx-font-weight-semibold` | 600 | 同浅色 |

### 圆角（7/7）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--radius-chat` | `--nx-radius-chat` | var(--nx-radius-page) | 同浅色 |
| `--radius-container` | `--nx-radius-container` | 1rem | 同浅色 |
| `--radius-element` | `--nx-radius-element` | 0.625rem | 同浅色 |
| `--radius-full` | `--nx-radius-full` | 9999px | 同浅色 |
| `--radius-inner` | `--nx-radius-inner` | 0.375rem | 同浅色 |
| `--radius-none` | `--nx-radius-none` | 0px | 同浅色 |
| `--radius-page` | `--nx-radius-page` | 1.75rem | 同浅色 |

### 阴影（8/8）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--shadow-high` | `--nx-shadow-high` | 0 4px 8px rgba(38, 38, 38, 0.05), 0 16px 40px rgba(60, 35… | 0 4px 8px rgba(0, 0, 0, 0.45), 0 16px 40px rgba(0, 0, 0, … |
| `--shadow-inset-error` | `--nx-shadow-inset-error` | inset 0 0 0 2px rgba(180, 35, 24, 0.30) | inset 0 0 0 2px rgba(247, 134, 118, 0.30) |
| `--shadow-inset-hover` | `--nx-shadow-inset-hover` | inset 0 0 0 2px rgba(38, 38, 38, 0.15) | inset 0 0 0 2px rgba(246, 246, 248, 0.20) |
| `--shadow-inset-selected` | `--nx-shadow-inset-selected` | inset 0 0 0 2px rgba(104, 87, 231, 0.50) | inset 0 0 0 2px rgba(187, 187, 254, 0.50) |
| `--shadow-inset-success` | `--nx-shadow-inset-success` | inset 0 0 0 2px rgba(8, 117, 95, 0.30) | inset 0 0 0 2px rgba(110, 189, 166, 0.30) |
| `--shadow-inset-warning` | `--nx-shadow-inset-warning` | inset 0 0 0 2px rgba(180, 95, 6, 0.30) | inset 0 0 0 2px rgba(244, 164, 104, 0.30) |
| `--shadow-low` | `--nx-shadow-low` | 0 1px 2px rgba(38, 38, 38, 0.04), 0 2px 8px rgba(60, 35, … | 0 1px 2px rgba(0, 0, 0, 0.30), 0 2px 8px rgba(0, 0, 0, 0.… |
| `--shadow-med` | `--nx-shadow-med` | 0 2px 4px rgba(38, 38, 38, 0.04), 0 8px 20px rgba(60, 35,… | 0 2px 4px rgba(0, 0, 0, 0.35), 0 8px 20px rgba(0, 0, 0, 0… |

### 控件高度（3/3）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--size-element-lg` | `--nx-size-element-lg` | 48px | 同浅色 |
| `--size-element-md` | `--nx-size-element-md` | 40px | 同浅色 |
| `--size-element-sm` | `--nx-size-element-sm` | 32px | 同浅色 |

### 间距（15/15）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--spacing-0` | `--nx-spacing-0` | 0rem | 同浅色 |
| `--spacing-0-5` | `--nx-spacing-0-5` | 0.125rem | 同浅色 |
| `--spacing-1` | `--nx-spacing-1` | 0.25rem | 同浅色 |
| `--spacing-1-5` | `--nx-spacing-1-5` | 0.375rem | 同浅色 |
| `--spacing-10` | `--nx-spacing-10` | 2.5rem | 同浅色 |
| `--spacing-11` | `--nx-spacing-11` | 2.75rem | 同浅色 |
| `--spacing-12` | `--nx-spacing-12` | 3rem | 同浅色 |
| `--spacing-2` | `--nx-spacing-2` | 0.5rem | 同浅色 |
| `--spacing-3` | `--nx-spacing-3` | 0.75rem | 同浅色 |
| `--spacing-4` | `--nx-spacing-4` | 1rem | 同浅色 |
| `--spacing-5` | `--nx-spacing-5` | 1.25rem | 同浅色 |
| `--spacing-6` | `--nx-spacing-6` | 1.5rem | 同浅色 |
| `--spacing-7` | `--nx-spacing-7` | 1.75rem | 同浅色 |
| `--spacing-8` | `--nx-spacing-8` | 2rem | 同浅色 |
| `--spacing-9` | `--nx-spacing-9` | 2.25rem | 同浅色 |

### 文字角色（42/42）

| Astryx token | 奈势 token | 浅色 | 深色 |
|---|---|---|---|
| `--text-body-leading` | `--nx-text-body-leading` | 1.75 | 同浅色 |
| `--text-body-size` | `--nx-text-body-size` | var(--nx-font-size-base) | 同浅色 |
| `--text-body-weight` | `--nx-text-body-weight` | var(--nx-font-weight-normal) | 同浅色 |
| `--text-code-leading` | `--nx-text-code-leading` | 1.6 | 同浅色 |
| `--text-code-size` | `--nx-text-code-size` | var(--nx-font-size-sm) | 同浅色 |
| `--text-code-weight` | `--nx-text-code-weight` | var(--nx-font-weight-normal) | 同浅色 |
| `--text-display-1-leading` | `--nx-text-display-1-leading` | 1.1 | 同浅色 |
| `--text-display-1-size` | `--nx-text-display-1-size` | var(--nx-font-size-5xl) | 同浅色 |
| `--text-display-1-weight` | `--nx-text-display-1-weight` | var(--nx-font-weight-semibold) | 同浅色 |
| `--text-display-2-leading` | `--nx-text-display-2-leading` | 1.15 | 同浅色 |
| `--text-display-2-size` | `--nx-text-display-2-size` | var(--nx-font-size-4xl) | 同浅色 |
| `--text-display-2-weight` | `--nx-text-display-2-weight` | var(--nx-font-weight-semibold) | 同浅色 |
| `--text-display-3-leading` | `--nx-text-display-3-leading` | 1.2 | 同浅色 |
| `--text-display-3-size` | `--nx-text-display-3-size` | var(--nx-font-size-3xl) | 同浅色 |
| `--text-display-3-weight` | `--nx-text-display-3-weight` | var(--nx-font-weight-semibold) | 同浅色 |
| `--text-heading-1-leading` | `--nx-text-heading-1-leading` | 1.2 | 同浅色 |
| `--text-heading-1-size` | `--nx-text-heading-1-size` | var(--nx-font-size-3xl) | 同浅色 |
| `--text-heading-1-weight` | `--nx-text-heading-1-weight` | var(--nx-font-weight-semibold) | 同浅色 |
| `--text-heading-2-leading` | `--nx-text-heading-2-leading` | 1.3 | 同浅色 |
| `--text-heading-2-size` | `--nx-text-heading-2-size` | var(--nx-font-size-2xl) | 同浅色 |
| `--text-heading-2-weight` | `--nx-text-heading-2-weight` | var(--nx-font-weight-semibold) | 同浅色 |
| `--text-heading-3-leading` | `--nx-text-heading-3-leading` | 1.35 | 同浅色 |
| `--text-heading-3-size` | `--nx-text-heading-3-size` | var(--nx-font-size-xl) | 同浅色 |
| `--text-heading-3-weight` | `--nx-text-heading-3-weight` | var(--nx-font-weight-semibold) | 同浅色 |
| `--text-heading-4-leading` | `--nx-text-heading-4-leading` | 1.4 | 同浅色 |
| `--text-heading-4-size` | `--nx-text-heading-4-size` | var(--nx-font-size-lg) | 同浅色 |
| `--text-heading-4-weight` | `--nx-text-heading-4-weight` | var(--nx-font-weight-semibold) | 同浅色 |
| `--text-heading-5-leading` | `--nx-text-heading-5-leading` | 1.5 | 同浅色 |
| `--text-heading-5-size` | `--nx-text-heading-5-size` | var(--nx-font-size-base) | 同浅色 |
| `--text-heading-5-weight` | `--nx-text-heading-5-weight` | var(--nx-font-weight-semibold) | 同浅色 |
| `--text-heading-6-leading` | `--nx-text-heading-6-leading` | 1.5 | 同浅色 |
| `--text-heading-6-size` | `--nx-text-heading-6-size` | var(--nx-font-size-sm) | 同浅色 |
| `--text-heading-6-weight` | `--nx-text-heading-6-weight` | var(--nx-font-weight-semibold) | 同浅色 |
| `--text-label-leading` | `--nx-text-label-leading` | 1.4 | 同浅色 |
| `--text-label-size` | `--nx-text-label-size` | var(--nx-font-size-sm) | 同浅色 |
| `--text-label-weight` | `--nx-text-label-weight` | var(--nx-font-weight-medium) | 同浅色 |
| `--text-large-leading` | `--nx-text-large-leading` | 1.7 | 同浅色 |
| `--text-large-size` | `--nx-text-large-size` | 1.125rem | 同浅色 |
| `--text-large-weight` | `--nx-text-large-weight` | var(--nx-font-weight-normal) | 同浅色 |
| `--text-supporting-leading` | `--nx-text-supporting-leading` | 1.5 | 同浅色 |
| `--text-supporting-size` | `--nx-text-supporting-size` | var(--nx-font-size-xs) | 同浅色 |
| `--text-supporting-weight` | `--nx-text-supporting-weight` | var(--nx-font-weight-normal) | 同浅色 |

## 2. 对不上的核心 token

| Astryx token | 原因与处理 |
|---|---|
| `--color-background-blue` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-background-cyan` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-background-green` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-background-orange` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-background-pink` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-background-red` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-background-teal` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-background-yellow` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-border-blue` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-border-cyan` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-border-green` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-border-orange` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-border-pink` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-border-red` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-border-teal` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-border-yellow` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-icon-blue` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-icon-cyan` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-icon-green` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-icon-orange` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-icon-pink` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-icon-red` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-icon-teal` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-icon-yellow` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-text-blue` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-text-cyan` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-text-green` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-text-orange` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-text-pink` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-text-red` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-text-teal` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |
| `--color-text-yellow` | 奈势规范只有紫/灰两族分类色，未定义多色分类色（图表/标签多色）。主题包先继承 Astryx 默认值，或由 Xiangjun 决定是否新增图表色。 |

## 3. 奈势本地 token（Astryx 没有，主题包放进 localTokens 或组件覆盖）

| 奈势 token | 浅色 | 深色 | 用途 |
|---|---|---|---|
| `--nx-color-background-brand` | #F1F0FD | #3C237C | 品牌浅底面板（雾紫；深色下为深紫） |
| `--nx-color-background-emphasized` | #3C237C | #3C237C | 深紫强调色块：封面、Hero、数据大字块 |
| `--nx-color-on-emphasized-secondary` | #BBBBFE | #BBBBFE | 深紫色块上的副标题/强调字 |
| `--nx-color-text-highlight` | #FF604A | #FF604A | 珊瑚橙字：浅色下仅装饰（<3:1），深色下可作大字；每版一处 |
| `--nx-color-border-accent` | #6857E7 | #BBBBFE | 选中描边；深色下的纯图形选中态 |
| `--nx-color-on-accent-muted` | #3C237C | #BBBBFE | 选中底上的文字 |
| `--nx-color-accent-hover` | #5F4AD4 | #5F4AD4 | 主行动悬停（Astryx 用 overlay 叠加实现，见映射表） |
| `--nx-color-accent-pressed` | #5743B7 | #5742B8 | 主行动按下 |
| `--nx-color-accent-muted-hover` | #E0DFFD | #462D8F | 浅底悬停 |
| `--nx-color-highlight` | #FF604A | #FF604A | 珊瑚橙填充：截止、限时、增长；每版一处 |
| `--nx-color-on-highlight` | #262626 | #262626 | 珊瑚橙上的文字：必须墨黑（白字仅 2.99:1） |
| `--nx-color-highlight-pressed` | #EF4F3B | #ED523C |  |
| `--nx-color-highlight-muted` | #FFECE8 | #4D302C | 珊瑚橙浅底提示条 |
| `--nx-color-on-highlight-muted` | #262626 | #F6F6F8 | 珊瑚浅底上的文字（配珊瑚圆点） |
| `--nx-color-tint-brand-hover` | rgba(104, 87, 231, 0.08) | rgba(187, 187, 254, 0.10) | 品牌色悬停叠加（列表项、幽灵按钮） |
| `--nx-text-display-1-tracking` | -0.02em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-display-2-tracking` | -0.015em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-display-3-tracking` | -0.01em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-heading-1-tracking` | -0.01em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-heading-2-tracking` | -0.005em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-heading-3-tracking` | 0em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-heading-4-tracking` | 0em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-heading-5-tracking` | 0em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-heading-6-tracking` | 0em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-large-tracking` | 0em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-body-tracking` | 0em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-label-tracking` | 0.01em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-supporting-tracking` | 0.01em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-code-tracking` | 0em | 同浅色 | 字距（奈势本地；Astryx 无此 token） |
| `--nx-text-body-sm-size` | var(--nx-font-size-sm) | 同浅色 | 紧凑正文、表格（奈势本地） |
| `--nx-measure` | 36em | 同浅色 | 中文段落行宽上限 ≈ 36 字 |
| `--nx-spacing-16` | 4rem | 同浅色 | 奈势本地：区块级大间距 |
| `--nx-spacing-20` | 5rem | 同浅色 | 奈势本地：区块级大间距 |
| `--nx-spacing-24` | 6rem | 同浅色 | 奈势本地：区块级大间距 |
| `--nx-space-tight` | var(--nx-spacing-2) | 同浅色 | 8px · 标签与字段、图标与文字 |
| `--nx-space-related` | var(--nx-spacing-4) | 同浅色 | 16px · 同组元素之间 |
| `--nx-space-group` | var(--nx-spacing-8) | 同浅色 | 32px · 组与组之间 |
| `--nx-space-section` | var(--nx-spacing-24) | 同浅色 | 96px · 页面区块之间（移动端 spacing-16 = 64px） |
| `--nx-space-card` | var(--nx-spacing-8) | 同浅色 | 32px · 卡片内边距（紧凑卡片 spacing-6） |
| `--nx-space-control-x` | var(--nx-spacing-4) | 同浅色 | 16px · 按钮/输入框水平内边距 |
| `--nx-page-max` | 1240px | 同浅色 |  |
| `--nx-sidebar` | 176px | 同浅色 |  |
| `--nx-sidebar-compact` | 64px | 同浅色 |  |

## 4. 语义差异（名字对上了，但用法与 Astryx 默认不同，开发写主题包时注意）

- `--color-accent` 深色模式仍是 #6857E7（Astryx 默认深色会提亮）。白字 5.11:1 没问题，但它在深色底上只有 2.96:1，纯图形选中态请在组件覆盖里改用 `--nx-color-border-accent`（薰衣草）。
- 主按钮悬停/按下：Astryx 用 `--color-overlay-hover/pressed` 叠在填充上；奈势定了实色 `accent-hover`（purple-40）/`accent-pressed`（purple-35），主题包里在 `components.button['variant:primary'][':hover']` 覆盖 backgroundColor。
- `--color-accent-muted`：Astryx 是半透明蓝，奈势是实色雾紫 #F1F0FD / 深紫 #3C237C。
- `--color-info` 系列：Astryx 要求信息态独立于 accent；奈势是单色相品牌，信息态复用奈势紫，靠图标区分。这是对 Astryx INV11「Info 不默认指向 accent」的有意偏离。
- `--color-error` 与珊瑚橙色相接近（浅底 error-95 与 coral-95 都是 #FFECE8）：错误态必须带图标和文字，珊瑚橙不用于任何状态。
- `--color-border-emphasized` 按 Astryx 约定 ≥3:1，用于控件边界；装饰性分隔线用 `--color-border`。
- `--font-size-*` 同名不同值：Astryx 以 14px 为 base、1.2 比率；奈势以 16px 为 base、约 1.25 比率（xs 12 / sm 14 / base 16 / lg 20 / xl 24 / 2xl 30 / 3xl 38 / 4xl 48 / 5xl 60）。3xs、4xs 奈势不用，指向 2xs（10px）。
- `--size-element-sm/md/lg`：Astryx 28/32/36px，奈势 32/40/48px（营销页与移动端触控更友好）。
- `--radius-*`：Astryx 默认 4/8/12/28，奈势 6/10/16/28。
- `--duration-*`：取 Astryx Neutral 主题同一组（125/300/700，ratio 0.75），比 Astryx 核心默认（175/410/975）更利落。
