# 奈势AI v1.3 对比度检查报告

生成：`node scripts/build.mjs` · 2026-11-12 · 标准：WCAG 2.x 相对亮度对比度。半透明值先合成到所在底色再算。对比度向下取两位小数（4.497 记 4.49，不四舍五入成 4.50）。

等级：**AAA 正文** ≥7；**AA 正文** ≥4.5；**仅大字/图形** 3–4.5（中文按 ≥24px 常规或 ≥19px 粗体算大字；图形与控件边界门槛也是 3）；**仅装饰** <3（不能承载信息）。

结果：✅ 满足预期用途；⚠️ 受限 = 不改品牌原值、用使用规则约束（见文末）；❌ 不达标需改值。

## 浅色模式（59 组：不达标 0，受限 6）

| 前景 | 背景 | 前景值 | 背景值 | 对比度 | 等级 | 预期用途 | 结果 |
|---|---|---|---|---|---|---|---|
| text-primary | background-body | #262626 | #F6F6F8 | 14.02 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-primary | background-surface | #262626 | #FFFFFF | 15.13 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-primary | background-card | #262626 | #FFFFFF | 15.13 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-primary | background-popover | #262626 | #FFFFFF | 15.13 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-primary | background-muted | #262626 | #F6F6F8 | 14.02 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | background-body | #6E6E73 | #F6F6F8 | 4.69 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | background-surface | #6E6E73 | #FFFFFF | 5.07 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | background-card | #6E6E73 | #FFFFFF | 5.07 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | background-popover | #6E6E73 | #FFFFFF | 5.07 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | background-muted | #6E6E73 | #F6F6F8 | 4.69 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-accent | background-body | #6857E7 | #F6F6F8 | 4.73 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-accent | background-surface | #6857E7 | #FFFFFF | 5.11 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-accent | background-card | #6857E7 | #FFFFFF | 5.11 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-accent | background-popover | #6857E7 | #FFFFFF | 5.11 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-accent | background-muted | #6857E7 | #F6F6F8 | 4.73 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-highlight | background-body | #FF604A | #F6F6F8 | 2.76 | 仅装饰 | 大字 ≥3 | ⚠️ 受限 |
| text-success | background-body | #08755F | #F6F6F8 | 5.23 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-warning | background-body | #A15204 | #F6F6F8 | 5.22 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-error | background-body | #B42318 | #F6F6F8 | 6.09 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-info | background-body | #6857E7 | #F6F6F8 | 4.73 | AA 正文 | 正文 ≥4.5 | ✅ |
| border-emphasized | background-body | #87878C | #F6F6F8 | 3.31 | 仅大字/图形 | 图形/边界 ≥3 | ✅ |
| border-accent | background-body | #6857E7 | #F6F6F8 | 4.73 | AA 正文 | 图形/边界 ≥3 | ✅ |
| accent | background-body | #6857E7 | #F6F6F8 | 4.73 | AA 正文 | 图形/边界 ≥3 | ✅ |
| highlight | background-body | #FF604A | #F6F6F8 | 2.76 | 仅装饰 | 图形/边界 ≥3 | ⚠️ 受限 |
| border | background-body | #E8E8EB | #F6F6F8 | 1.13 | 仅装饰 | 装饰线（不要求） | ✅ |
| text-highlight | background-card | #FF604A | #FFFFFF | 2.98 | 仅装饰 | 大字 ≥3 | ⚠️ 受限 |
| text-success | background-card | #08755F | #FFFFFF | 5.64 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-warning | background-card | #A15204 | #FFFFFF | 5.63 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-error | background-card | #B42318 | #FFFFFF | 6.57 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-info | background-card | #6857E7 | #FFFFFF | 5.11 | AA 正文 | 正文 ≥4.5 | ✅ |
| border-emphasized | background-card | #87878C | #FFFFFF | 3.57 | 仅大字/图形 | 图形/边界 ≥3 | ✅ |
| border-accent | background-card | #6857E7 | #FFFFFF | 5.11 | AA 正文 | 图形/边界 ≥3 | ✅ |
| accent | background-card | #6857E7 | #FFFFFF | 5.11 | AA 正文 | 图形/边界 ≥3 | ✅ |
| highlight | background-card | #FF604A | #FFFFFF | 2.98 | 仅装饰 | 图形/边界 ≥3 | ⚠️ 受限 |
| border | background-card | #E8E8EB | #FFFFFF | 1.22 | 仅装饰 | 装饰线（不要求） | ✅ |
| text-disabled | background-card | #A2A2A7 | #FFFFFF | 2.54 | 仅装饰 | 不要求 | ✅ |
| text-primary | background-brand | #262626 | #F1F0FD | 13.42 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | background-brand | #6E6E73 | #F1F0FD | 4.49 | 仅大字/图形 | 正文 ≥4.5 | ⚠️ 受限 |
| on-accent-muted | background-brand | #3C237C | #F1F0FD | 10.80 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-primary | accent-muted | #262626 | #F1F0FD | 13.42 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | accent-muted | #6E6E73 | #F1F0FD | 4.49 | 仅大字/图形 | 正文 ≥4.5 | ⚠️ 受限 |
| on-accent-muted | accent-muted | #3C237C | #F1F0FD | 10.80 | AAA 正文 | 正文 ≥4.5 | ✅ |
| on-accent | accent | #FFFFFF | #6857E7 | 5.11 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-accent | accent-hover | #FFFFFF | #5F4AD4 | 6.14 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-accent | accent-pressed | #FFFFFF | #5743B7 | 7.26 | AAA 正文 | 正文 ≥4.5 | ✅ |
| on-highlight | highlight | #262626 | #FF604A | 5.06 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-highlight-muted | highlight-muted | #262626 | #FFECE8 | 13.27 | AAA 正文 | 正文 ≥4.5 | ✅ |
| on-success | success | #FFFFFF | #08755F | 5.64 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-success-muted | success-muted | #035846 | #D5FBEE | 7.58 | AAA 正文 | 正文 ≥4.5 | ✅ |
| on-warning | warning | #FFFFFF | #B45F06 | 4.58 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-warning-muted | warning-muted | #773701 | #FFEDE1 | 7.91 | AAA 正文 | 正文 ≥4.5 | ✅ |
| on-error | error | #FFFFFF | #B42318 | 6.57 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-error-muted | error-muted | #8F0201 | #FFECE8 | 8.45 | AAA 正文 | 正文 ≥4.5 | ✅ |
| on-info | info | #FFFFFF | #6857E7 | 5.11 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-info-muted | info-muted | #3C237C | #F1F0FD | 10.80 | AAA 正文 | 正文 ≥4.5 | ✅ |
| on-dark | background-emphasized | #FFFFFF | #3C237C | 12.18 | AAA 正文 | 正文 ≥4.5 | ✅ |
| on-emphasized-secondary | background-emphasized | #BBBBFE | #3C237C | 6.76 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-highlight | background-emphasized | #FF604A | #3C237C | 4.07 | 仅大字/图形 | 大字 ≥3 | ✅ |
| text-primary | background-inverted | #262626 | #262626 | 1.00 | 仅装饰 | 不要求 | ✅ |

## 深色模式（59 组：不达标 0，受限 2）

| 前景 | 背景 | 前景值 | 背景值 | 对比度 | 等级 | 预期用途 | 结果 |
|---|---|---|---|---|---|---|---|
| text-primary | background-body | #F6F6F8 | #262626 | 14.02 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-primary | background-surface | #F6F6F8 | #262626 | 14.02 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-primary | background-card | #F6F6F8 | #313030 | 12.19 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-primary | background-popover | #F6F6F8 | #3D3C3C | 10.18 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-primary | background-muted | #F6F6F8 | #1B1B1B | 15.95 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | background-body | #BDBDC1 | #262626 | 8.08 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | background-surface | #BDBDC1 | #262626 | 8.08 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | background-card | #BDBDC1 | #313030 | 7.02 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | background-popover | #BDBDC1 | #3D3C3C | 5.87 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | background-muted | #BDBDC1 | #1B1B1B | 9.19 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-accent | background-body | #BBBBFE | #262626 | 8.39 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-accent | background-surface | #BBBBFE | #262626 | 8.39 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-accent | background-card | #BBBBFE | #313030 | 7.30 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-accent | background-popover | #BBBBFE | #3D3C3C | 6.10 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-accent | background-muted | #BBBBFE | #1B1B1B | 9.55 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-highlight | background-body | #FF604A | #262626 | 5.06 | AA 正文 | 大字 ≥3 | ✅ |
| text-success | background-body | #84C9B4 | #262626 | 7.92 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-warning | background-body | #F4A468 | #262626 | 7.46 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-error | background-body | #FF9989 | #262626 | 7.32 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-info | background-body | #BBBBFE | #262626 | 8.39 | AAA 正文 | 正文 ≥4.5 | ✅ |
| border-emphasized | background-body | #949499 | #262626 | 5.01 | AA 正文 | 图形/边界 ≥3 | ✅ |
| border-accent | background-body | #BBBBFE | #262626 | 8.39 | AAA 正文 | 图形/边界 ≥3 | ✅ |
| accent | background-body | #6857E7 | #262626 | 2.95 | 仅装饰 | 图形/边界 ≥3 | ⚠️ 受限 |
| highlight | background-body | #FF604A | #262626 | 5.06 | AA 正文 | 图形/边界 ≥3 | ✅ |
| border | background-body | #3B3B3B | #262626 | 1.35 | 仅装饰 | 装饰线（不要求） | ✅ |
| text-highlight | background-card | #FF604A | #313030 | 4.40 | 仅大字/图形 | 大字 ≥3 | ✅ |
| text-success | background-card | #84C9B4 | #313030 | 6.88 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-warning | background-card | #F4A468 | #313030 | 6.48 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-error | background-card | #FF9989 | #313030 | 6.37 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-info | background-card | #BBBBFE | #313030 | 7.30 | AAA 正文 | 正文 ≥4.5 | ✅ |
| border-emphasized | background-card | #949499 | #313030 | 4.35 | 仅大字/图形 | 图形/边界 ≥3 | ✅ |
| border-accent | background-card | #BBBBFE | #313030 | 7.30 | AAA 正文 | 图形/边界 ≥3 | ✅ |
| accent | background-card | #6857E7 | #313030 | 2.57 | 仅装饰 | 图形/边界 ≥3 | ⚠️ 受限 |
| highlight | background-card | #FF604A | #313030 | 4.40 | 仅大字/图形 | 图形/边界 ≥3 | ✅ |
| border | background-card | #454444 | #313030 | 1.35 | 仅装饰 | 装饰线（不要求） | ✅ |
| text-disabled | background-card | #7B7B7F | #313030 | 3.12 | 仅大字/图形 | 不要求 | ✅ |
| text-primary | background-brand | #F6F6F8 | #3C237C | 11.28 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | background-brand | #BDBDC1 | #3C237C | 6.50 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-accent-muted | background-brand | #BBBBFE | #3C237C | 6.76 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-primary | accent-muted | #F6F6F8 | #3C237C | 11.28 | AAA 正文 | 正文 ≥4.5 | ✅ |
| text-secondary | accent-muted | #BDBDC1 | #3C237C | 6.50 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-accent-muted | accent-muted | #BBBBFE | #3C237C | 6.76 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-accent | accent | #FFFFFF | #6857E7 | 5.11 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-accent | accent-hover | #FFFFFF | #5F4AD4 | 6.14 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-accent | accent-pressed | #FFFFFF | #5742B8 | 7.30 | AAA 正文 | 正文 ≥4.5 | ✅ |
| on-highlight | highlight | #262626 | #FF604A | 5.06 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-highlight-muted | highlight-muted | #F6F6F8 | #4D302C | 10.96 | AAA 正文 | 正文 ≥4.5 | ✅ |
| on-success | success | #262626 | #6EBDA6 | 6.84 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-success-muted | success-muted | #99D5C3 | #2C3F3A | 6.73 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-warning | warning | #262626 | #E89454 | 6.33 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-warning-muted | warning-muted | #FFB37C | #483628 | 6.53 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-error | error | #262626 | #F78676 | 6.21 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-error-muted | error-muted | #FFAFA2 | #4B3330 | 6.55 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-info | info | #FFFFFF | #6857E7 | 5.11 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-info-muted | info-muted | #BBBBFE | #3C237C | 6.76 | AA 正文 | 正文 ≥4.5 | ✅ |
| on-dark | background-emphasized | #FFFFFF | #3C237C | 12.18 | AAA 正文 | 正文 ≥4.5 | ✅ |
| on-emphasized-secondary | background-emphasized | #BBBBFE | #3C237C | 6.76 | AA 正文 | 正文 ≥4.5 | ✅ |
| text-highlight | background-emphasized | #FF604A | #3C237C | 4.07 | 仅大字/图形 | 大字 ≥3 | ✅ |
| text-primary | background-inverted | #F6F6F8 | #F6F6F8 | 1.00 | 仅装饰 | 不要求 | ✅ |

## 受限组合与使用规则

- **浅色 · text-highlight**：浅色底上珊瑚橙字 <3:1：不能单独承载信息。浅色版面里珊瑚橙用作填充块（块内墨黑字）、圆点或线条，旁边必须有文字。
- **浅色 · highlight**：珊瑚橙色块在白/浅灰底 <3:1：作提示块时块内必须有墨黑文字，不能只靠颜色表意。
- **浅色 · text-secondary 在 background-brand**：中灰字在雾紫底 4.497:1，差 0.003 到 4.5：雾紫底上的说明文字改用 on-accent-muted（深紫）或 text-primary。
- **浅色 · text-secondary 在 accent-muted**：同上：选中底上的副文字用 on-accent-muted。
- **深色 · accent**：深色底上奈势紫填充 <3:1：主按钮靠白字（5.11:1）识别没问题；纯图形选中态（复选框、开关、进度）在深色下改用 border-accent（薰衣草）。

## 原始品牌色组合（设计稿、视频、海报直接取色时参考）

| 组合 | 前景 | 背景 | 对比度 | 等级 |
|---|---|---|---|---|
| 白字压珊瑚橙 | #FFFFFF | #FF604A | 2.98 | 仅装饰 |
| 珊瑚橙字在白底 | #FF604A | #FFFFFF | 2.98 | 仅装饰 |
| 珊瑚橙字在浅灰底 | #FF604A | #F6F6F8 | 2.76 | 仅装饰 |
| 珊瑚橙字在墨黑底 | #FF604A | #262626 | 5.06 | AA 正文 |
| 珊瑚橙字在深紫底 | #FF604A | #3C237C | 4.07 | 仅大字/图形 |
| 薰衣草字在深紫底 | #BBBBFE | #3C237C | 6.76 | AA 正文 |
| 薰衣草字在墨黑底 | #BBBBFE | #262626 | 8.39 | AAA 正文 |
| 薰衣草字在奈势紫底 | #BBBBFE | #6857E7 | 2.83 | 仅装饰 |
| 薰衣草在白底 | #BBBBFE | #FFFFFF | 1.80 | 仅装饰 |
| 奈势紫字在墨黑底 | #6857E7 | #262626 | 2.95 | 仅装饰 |
| 奈势紫字在深紫底 | #6857E7 | #3C237C | 2.38 | 仅装饰 |
| 白字在奈势紫底 | #FFFFFF | #6857E7 | 5.11 | AA 正文 |
| 中灰字在雾紫底 | #6E6E73 | #F1F0FD | 4.49 | 仅大字/图形 |
| 中灰字在浅灰底 | #6E6E73 | #F6F6F8 | 4.69 | AA 正文 |
| 中灰字在墨黑底 | #6E6E73 | #262626 | 2.98 | 仅装饰 |
| 深紫字在薰衣草底 | #3C237C | #BBBBFE | 6.76 | AA 正文 |
| 墨黑字在薰衣草底 | #262626 | #BBBBFE | 8.39 | AAA 正文 |
| 白字在深紫底 | #FFFFFF | #3C237C | 12.18 | AAA 正文 |

## 1.3.1 / 1.3.2 补充（2026-11-12，手工核算，同一算法）

| 前景 | 背景 | 前景值 | 背景值 | 对比度 | 用途 | 结果 |
|---|---|---|---|---|---|---|
| on-button-danger | button-danger（浅/深） | #262626 | #FF604A | 5.06 | 危险按钮正文 | ✅ |
| on-button-danger | button-danger-hover | #262626 | #FA5B46 | 4.79 | 危险按钮悬停 | ✅ |
| on-button-danger | button-danger-pressed | #262626 | #F75742 | 4.60 | 危险按钮按下 | ✅ |
| 白字 | button-danger | #FFFFFF | #FF604A | 2.98 | 禁止 | ❌ 不采用 |
| 深色 · 错误 Toast 文字 | background-error-inverted | #F6F6F8 | #B42318 | 6.09 | Toast 正文 | ✅ |
| 深色 · on-error | error | #262626 | #E8705F | 4.98 | error 强填充 | ✅ |
| 深色 · text-error | background-body | #F78676 | #262626 | 6.21 | 状态文字 | ✅ |
| 深色 · text-error | background-card | #F78676 | #313030 | 5.40 | 状态文字 | ✅ |
| 品牌大字 Create | 白底 | #E5503A | #FFFFFF | 3.79 | ≥48px 大字 | ✅ 仅大字 |

上表取代正文里深色 `on-error / error`（#262626 / #F78676，6.21）一行和深色错误 Toast 旧值 #DD6858。品牌站物料示意图：Partner 12px 白字 .7 透明度 5.11；紫底日期 #5743B7 上 12px 白字 .85 透明度 5.75（开发实测，见 `site-preview/redesign/review-fix-measures.json`）。
