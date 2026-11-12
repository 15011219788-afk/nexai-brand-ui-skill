# 奈势AI 品牌规范 v1.3（定稿，tokens 1.3.2）· 语义 token 与审美调性

> 状态：定稿，Xiangjun 已于 2026-11-12 确认。
> 范围：升级规范和 token（语义层、色阶、深色模式、间距/圆角/阴影/动效/字号）；命名已对齐 Astryx，`tokens.json` 是唯一来源。主题包 `theme-nexai` 由「开发」从 `tokens.json` 生成并维护（含安卓颜色资源），不手改主题包里的值。
> 参考：Meta Astryx（meta/astryx@4705e676）的 theme-tokens、theme-authoring-contract、docs/design 下 8 篇设计原则，以及 Neutral / Stone / Butter / Matcha 四套主题。

## 0. 不变的东西

- 品牌色原值全部不变：#6857E7 奈势紫、#3C237C 深紫、#BBBBFE 薰衣草、#F1F0FD 雾紫、#FF604A 珊瑚橙、#262626 墨黑、#6E6E73 中灰、#F6F6F8 浅灰、#FFFFFF。
- Logo 渐变 #7417FF→#FE6702 只出现在 Logo 图形标里。#F26322、微信绿禁用。
- 字体 MiSans；禁用像素方块辅助图形、菱形网格背景；小奈不压文字。
- 品牌个性：开放、伙伴、创造。

## 1. 结构：三层 token

| 层 | 命名 | 谁用 | 说明 |
|---|---|---|---|
| 原始色 | `--nx-purple`、`--nx-ink`… | 只给语义层引用 | v1.2 原值，一个不改 |
| 色阶 | `--nx-purple-45`、`--nx-neutral-dk-20`… | 只给语义层引用 | astryx-oklch-v1 生成，品牌色是 exact 锚点；`-dk-` 是深色模式色阶 |
| 语义 | `--nx-color-text-primary`、`--nx-color-accent`… | 组件、页面、模板 | 按用途命名，浅色/深色两套值 |

**规则：组件和页面只用语义层。** 换主题、做深色模式时只改语义层的映射，组件不动。

**与 Astryx 对齐：** `--nx-X` 去掉 `nx-` 就是 Astryx 的 `--X`（如 `--nx-color-accent` ⇄ `--color-accent`，`--nx-radius-container` ⇄ `--radius-container`）。Astryx 没有的叫「本地 token」，主题包里放进 `localTokens`。逐项对照见 `astryx-mapping.md`，覆盖率 179 / 211（84.8%）。

**深色模式用法：** `<html data-theme="dark">` 强制深色；不写时跟随系统；`data-theme="light"` 可以把局部区域固定成浅色。

## 2. 审美调性：这次收了哪几处

对照 Astryx 四套主题的做法：Neutral 最克制（纯灰、只用一个强调）；Stone 用带紫调的中性灰，阴影用主题深色调低透明度；Butter 圆角 8/12、阴影同 Stone；Matcha 留白最大（间距整体 ×1.5）、圆角最软（12/18/42）。四套共同点是：**底子安静，强调稀缺，阴影只表达层级，圆角按角色分档**。奈势 v1.2 的问题正好在反面：圆角 10 档、间距 18 档都是零散 px，阴影偏重（0 14px 40px，13–16% 墨黑），悬停直接跳到深紫，强调色没有落到 token 规则里。

1. **中性灰带一点奈势紫的冷调。** 整条灰阶以中灰 #6E6E73 的色相（OKLCH H≈286°，C≈0.008）生成，墨黑 #262626 和浅灰 #F6F6F8 原值锚定。做法同 Stone 的紫调中性灰：灰和紫放在一起不打架，页面整体更「同一家」。
2. **阴影更轻，带深紫调，只给浮起来的东西。** 三档 `low / med / high`，最高一档 `0 4px 8px 墨黑 5% + 0 16px 40px 深紫 10%`（v1.2 浮层是 0 14px 40px 墨黑 13%，站点里还有 16%）。静止的卡片只用 1px 描边、不加阴影（Astryx「一种边界语言为主」原则）。深色模式的阴影加 1px 内描边（白 6–10%），否则黑底上看不出层级。
3. **圆角从 10 个值收成 4 档 + 胶囊，嵌套时保持同心。** inner 6 / element 10 / container 16 / page 28 / full。嵌套规则：内圆角 = 外圆角 − 间距（例：28 的大面板内边距 12，里面的卡片用 16）。比 Astryx 默认（4/8/12/28）稍软，比 Matcha（12/18/42）收着，符合「伙伴」的亲和但不幼稚。
4. **留白更大、间距成体系。** 间距统一为 N × 0.25rem（4px 网格，跟随用户根字号）。分组间距逐级放大：紧密 8 → 同组 16 → 组间 32 → 区块 96（v1.2 最大只有 68px）；卡片内边距默认 32（紧凑卡片 24）。先用间距分组，再考虑加卡片和描边。
5. **字号按 1.25 比率走，标题收一档字重。** 16 为正文基准：12 / 14 / 16 / 20 / 24 / 30 / 38 / 48 / 60。网页标题默认 Semibold 600（v1.2 Display 是 700），大标题字距 −0.01 ~ −0.02em；正文行高 1.75，行宽 ≤ 36 字。Bold 700 留给视频字幕、社媒封面这类远看场景。
6. **强调稀缺写成规则。** 每个操作组只有一个奈势紫主按钮；珊瑚橙每版一处，作填充时块内用墨黑字；主按钮悬停从「跳到深紫 #3C237C」改为色阶相邻档 purple-40 #5F4AD4，按下 purple-35 #5743B7，反馈更细腻，深紫留给大色块。

## 3. 强调色使用规则

- **奈势紫（accent）：** 一个操作组只有一个主行动。次按钮用 `neutral` 浅填充，第三级用幽灵按钮（text-accent）。
- **珊瑚橙（highlight）：** 每版一处（同一屏、同一页、同一张图只出现一个珊瑚橙元素），只用于截止、限时、增长、需要注意的点。
  - 浅色底上珊瑚橙字只有 2.77–2.99:1，**不能单独承载信息**：用作填充块（块内墨黑字，5.06:1）、圆点、线条，旁边要有文字。
  - 白字压珊瑚橙 2.99:1，禁止。
  - 深色底（#262626）上珊瑚橙字 5.06:1，可以直接当文字用。
  - 例外：白底上的品牌大字（≥48px，如品牌理念页的「Create」）用单独定值 #E5503A（对白 3.79），只用于这一种大字；色块、图形、按钮仍用 #FF604A。该值不进色阶。
- **危险按钮（破坏性/强调）：** 浅色和深色都用珊瑚橙 #FF604A 配墨黑字（5.06），悬停 #FA5B46（4.79），按下 #F75742（4.60）；白字只有 2.98，禁止。它是按钮专用的本地 token `--nx-color-button-danger*`，不改全局 error。
- **珊瑚橙不是状态色。** 错误态用 `error` 系列（#B42318），而且必须配图标和文字。两者色相接近（浅底都是 #FFECE8），靠图标区分。
- **信息态（info）** 复用奈势紫，必须带图标。这是有意偏离 Astryx「信息态独立于 accent」的约定：奈势是单色相品牌，不再引入蓝色。

## 4. 语义映射表（给「开发」照着重写代码）

浅色、深色两列都是最终值，小字是引用的色阶变量。

<!--GEN:semantic-->
| 分组 | 奈势 token | Astryx 对应 | 浅色 | 深色 | 用途 |
|---|---|---|---|---|---|
| 背景 | `--nx-color-background-body` | `--color-background-body` | #F6F6F8<br><sub>nx-surface</sub> | #262626<br><sub>nx-ink</sub> | 页面底（最底层） |
| 背景 | `--nx-color-background-surface` | `--color-background-surface` | #FFFFFF<br><sub>nx-white</sub> | #262626<br><sub>nx-ink</sub> | 主画布、导航、与页面同层的大面板 |
| 背景 | `--nx-color-background-card` | `--color-background-card` | #FFFFFF<br><sub>nx-white</sub> | #313030<br><sub>nx-neutral-dk-20</sub> | 卡片、列表容器（比页面高一层） |
| 背景 | `--nx-color-background-popover` | `--color-background-popover` | #FFFFFF<br><sub>nx-white</sub> | #3D3C3C<br><sub>nx-neutral-dk-25</sub> | 菜单、弹窗、浮层（最高层） |
| 背景 | `--nx-color-background-muted` | `--color-background-muted` | #F6F6F8<br><sub>nx-surface</sub> | #1B1B1B<br><sub>nx-neutral-dk-10</sub> | 卡片内的次级分区、代码块、输入框静止底 |
| 背景 | `--nx-color-background-inverted` | `--color-background-inverted` | #262626<br><sub>nx-ink</sub> | #F6F6F8<br><sub>nx-surface</sub> | 反相块（toast 等） |
| 背景 | `--nx-color-background-error-inverted` | `--color-background-error-inverted` | #B42318<br><sub>nx-danger</sub> | #B42318<br><sub>nx-danger</sub> | 反相面上的错误填充（错误 Toast 底）；浅/深都用 #B42318，配 #F6F6F8 字 |
| 背景 | `--nx-color-background-brand` | 本地 | #F1F0FD<br><sub>nx-mist</sub> | #3C237C<br><sub>nx-purple-deep</sub> | 品牌浅底面板（雾紫；深色下为深紫） |
| 背景 | `--nx-color-background-emphasized` | 本地 | #3C237C<br><sub>nx-purple-deep</sub> | #3C237C<br><sub>nx-purple-deep</sub> | 深紫强调色块：封面、Hero、数据大字块 |
| 文字 | `--nx-color-text-primary` | `--color-text-primary` | #262626<br><sub>nx-ink</sub> | #F6F6F8<br><sub>nx-surface</sub> | 标题、正文 |
| 文字 | `--nx-color-text-secondary` | `--color-text-secondary` | #6E6E73<br><sub>nx-gray</sub> | #BDBDC1<br><sub>nx-neutral-dk-75</sub> | 说明、元信息 |
| 文字 | `--nx-color-text-disabled` | `--color-text-disabled` | #A2A2A7<br><sub>nx-neutral-65</sub> | #7B7B7F<br><sub>nx-neutral-dk-50</sub> | 不可用文字（豁免对比度，须配合其他不可用提示） |
| 文字 | `--nx-color-text-accent` | `--color-text-accent` | #6857E7<br><sub>nx-purple</sub> | #BBBBFE<br><sub>nx-lavender</sub> | 链接、品牌强调文字 |
| 文字 | `--nx-color-on-dark` | `--color-on-dark` | #FFFFFF<br><sub>nx-white</sub> | #FFFFFF<br><sub>nx-white</sub> | 深色面（深紫块、墨黑块、图片）上的文字 |
| 文字 | `--nx-color-on-light` | `--color-on-light` | #262626<br><sub>nx-ink</sub> | #262626<br><sub>nx-ink</sub> | 浅色面（薰衣草、珊瑚橙、白图）上的文字 |
| 文字 | `--nx-color-on-emphasized-secondary` | 本地 | #BBBBFE<br><sub>nx-lavender</sub> | #BBBBFE<br><sub>nx-lavender</sub> | 深紫色块上的副标题/强调字 |
| 文字 | `--nx-color-text-highlight` | 本地 | #FF604A<br><sub>nx-coral</sub> | #FF604A<br><sub>nx-coral</sub> | 珊瑚橙字：浅色下仅装饰（<3:1），深色下可作大字；每版一处 |
| 图标 | `--nx-color-icon-primary` | `--color-icon-primary` | #262626<br><sub>nx-ink</sub> | #F6F6F8<br><sub>nx-surface</sub> |  |
| 图标 | `--nx-color-icon-secondary` | `--color-icon-secondary` | #6E6E73<br><sub>nx-gray</sub> | #BDBDC1<br><sub>nx-neutral-dk-75</sub> |  |
| 图标 | `--nx-color-icon-disabled` | `--color-icon-disabled` | #A2A2A7<br><sub>nx-neutral-65</sub> | #7B7B7F<br><sub>nx-neutral-dk-50</sub> |  |
| 图标 | `--nx-color-icon-accent` | `--color-icon-accent` | #6857E7<br><sub>nx-purple</sub> | #BBBBFE<br><sub>nx-lavender</sub> |  |
| 边框 | `--nx-color-border` | `--color-border` | #E8E8EB<br><sub>nx-neutral-90</sub> | rgba(246, 246, 248, 0.10) | 分隔线、卡片描边（装饰性） |
| 边框 | `--nx-color-border-emphasized` | `--color-border-emphasized` | #87878C<br><sub>nx-neutral-55</sub> | #949499<br><sub>nx-neutral-dk-60</sub> | 控件边界：输入框、复选框（≥3:1） |
| 边框 | `--nx-color-border-accent` | 本地 | #6857E7<br><sub>nx-purple</sub> | #BBBBFE<br><sub>nx-lavender</sub> | 选中描边；深色下的纯图形选中态 |
| 主行动 | `--nx-color-accent` | `--color-accent` | #6857E7<br><sub>nx-purple</sub> | #6857E7<br><sub>nx-purple</sub> | 主按钮、选中、开关；每个操作组只有一个 |
| 主行动 | `--nx-color-on-accent` | `--color-on-accent` | #FFFFFF<br><sub>nx-white</sub> | #FFFFFF<br><sub>nx-white</sub> |  |
| 主行动 | `--nx-color-accent-muted` | `--color-accent-muted` | #F1F0FD<br><sub>nx-mist</sub> | #3C237C<br><sub>nx-purple-deep</sub> | 选中底、品牌标签底 |
| 主行动 | `--nx-color-on-accent-muted` | 本地 | #3C237C<br><sub>nx-purple-deep</sub> | #BBBBFE<br><sub>nx-lavender</sub> | 选中底上的文字 |
| 主行动 | `--nx-color-accent-hover` | 本地 | #5F4AD4<br><sub>nx-purple-40</sub> | #5F4AD4<br><sub>nx-purple-dk-40</sub> | 主行动悬停（Astryx 用 overlay 叠加实现，见映射表） |
| 主行动 | `--nx-color-accent-pressed` | 本地 | #5743B7<br><sub>nx-purple-35</sub> | #5742B8<br><sub>nx-purple-dk-35</sub> | 主行动按下 |
| 主行动 | `--nx-color-accent-muted-hover` | 本地 | #E0DFFD<br><sub>nx-purple-90</sub> | #462D8F<br><sub>nx-purple-dk-25</sub> | 浅底悬停 |
| 强调 | `--nx-color-highlight` | 本地 | #FF604A<br><sub>nx-coral</sub> | #FF604A<br><sub>nx-coral</sub> | 珊瑚橙填充：截止、限时、增长；每版一处 |
| 强调 | `--nx-color-on-highlight` | 本地 | #262626<br><sub>nx-ink</sub> | #262626<br><sub>nx-ink</sub> | 珊瑚橙上的文字：必须墨黑（白字仅 2.99:1） |
| 强调 | `--nx-color-highlight-pressed` | 本地 | #EF4F3B<br><sub>nx-coral-55</sub> | #ED523C<br><sub>nx-coral-dk-55</sub> |  |
| 危险按钮 | `--nx-color-button-danger` | 本地 | #FF604A<br><sub>nx-coral</sub> | #FF604A<br><sub>nx-coral</sub> | 破坏性/强调按钮填充：奈势标准珊瑚橙 #FF604A。白字仅 2.99:1，必须配墨黑字（5.06:1）。不改全局 --color-error，以免影响 Toast 与状态色。浅色与深色相同。 |
| 危险按钮 | `--nx-color-on-button-danger` | 本地 | #262626<br><sub>nx-ink</sub> | #262626<br><sub>nx-ink</sub> | 危险按钮上的文字与图标：品牌墨黑 #262626。浅色与深色均 5.06:1。 |
| 危险按钮 | `--nx-color-button-danger-hover` | 本地 | #FA5B46 | #FA5B46 | 危险按钮悬停：沿珊瑚色阶 60→55 加深到 #FA5B46。下一档 coral-55 #EF4F3B 配墨黑仅 4.22:1，不采用；本色配墨黑 4.80:1。浅色与深色相同。 |
| 危险按钮 | `--nx-color-button-danger-pressed` | 本地 | #F75742 | #F75742 | 危险按钮按下：沿珊瑚色阶 60→55 再深到 #F75742，配墨黑 4.60:1。浅色与深色相同。 |
| 强调 | `--nx-color-highlight-muted` | 本地 | #FFECE8<br><sub>nx-coral-95</sub> | #4D302C | 珊瑚橙浅底提示条 |
| 强调 | `--nx-color-on-highlight-muted` | 本地 | #262626<br><sub>nx-ink</sub> | #F6F6F8<br><sub>nx-surface</sub> | 珊瑚浅底上的文字（配珊瑚圆点） |
| 状态 | `--nx-color-success` | `--color-success` | #08755F<br><sub>nx-success</sub> | #6EBDA6<br><sub>nx-success-dk-70</sub> | success 强填充 |
| 状态 | `--nx-color-on-success` | `--color-on-success` | #FFFFFF<br><sub>nx-white</sub> | #262626<br><sub>nx-ink</sub> |  |
| 状态 | `--nx-color-success-muted` | `--color-success-muted` | #D5FBEE<br><sub>nx-success-95</sub> | #2C3F3A | 浅底 |
| 状态 | `--nx-color-on-success-muted` | `--color-on-success-muted` | #035846<br><sub>nx-success-30</sub> | #99D5C3<br><sub>nx-success-dk-80</sub> |  |
| 状态 | `--nx-color-text-success` | `--color-text-success` | #08755F<br><sub>nx-success</sub> | #84C9B4<br><sub>nx-success-dk-75</sub> | 页面/卡片上的状态文字 |
| 状态 | `--nx-color-icon-success` | `--color-icon-success` | #08755F<br><sub>nx-success</sub> | #84C9B4<br><sub>nx-success-dk-75</sub> |  |
| 状态 | `--nx-color-border-success` | `--color-border-success` | #08755F<br><sub>nx-success</sub> | #84C9B4<br><sub>nx-success-dk-75</sub> |  |
| 状态 | `--nx-color-warning` | `--color-warning` | #B45F06<br><sub>nx-warning</sub> | #E89454<br><sub>nx-warning-dk-70</sub> | warning 强填充 |
| 状态 | `--nx-color-on-warning` | `--color-on-warning` | #FFFFFF<br><sub>nx-white</sub> | #262626<br><sub>nx-ink</sub> |  |
| 状态 | `--nx-color-warning-muted` | `--color-warning-muted` | #FFEDE1<br><sub>nx-warning-95</sub> | #483628 | 浅底 |
| 状态 | `--nx-color-on-warning-muted` | `--color-on-warning-muted` | #773701<br><sub>nx-warning-30</sub> | #FFB37C<br><sub>nx-warning-dk-80</sub> |  |
| 状态 | `--nx-color-text-warning` | `--color-text-warning` | #A15204<br><sub>nx-warning-40</sub> | #F4A468<br><sub>nx-warning-dk-75</sub> | 页面/卡片上的状态文字 |
| 状态 | `--nx-color-icon-warning` | `--color-icon-warning` | #A15204<br><sub>nx-warning-40</sub> | #F4A468<br><sub>nx-warning-dk-75</sub> |  |
| 状态 | `--nx-color-border-warning` | `--color-border-warning` | #A15204<br><sub>nx-warning-40</sub> | #F4A468<br><sub>nx-warning-dk-75</sub> |  |
| 状态 | `--nx-color-error` | `--color-error` | #B42318<br><sub>nx-danger</sub> | #E8705F | error 强填充（危险按钮底）；深色为 #E8705F，配墨黑字 |
| 状态 | `--nx-color-on-error` | `--color-on-error` | #FFFFFF<br><sub>nx-white</sub> | #262626<br><sub>nx-ink</sub> |  |
| 状态 | `--nx-color-error-muted` | `--color-error-muted` | #FFECE8<br><sub>nx-error-95</sub> | #4B3330 | 浅底 |
| 状态 | `--nx-color-on-error-muted` | `--color-on-error-muted` | #8F0201<br><sub>nx-error-30</sub> | #FFAFA2<br><sub>nx-error-dk-80</sub> |  |
| 状态 | `--nx-color-text-error` | `--color-text-error` | #B42318<br><sub>nx-danger</sub> | #F78676<br><sub>nx-error-dk-70</sub> | 页面/卡片上的状态文字 |
| 状态 | `--nx-color-icon-error` | `--color-icon-error` | #B42318<br><sub>nx-danger</sub> | #F78676<br><sub>nx-error-dk-70</sub> |  |
| 状态 | `--nx-color-border-error` | `--color-border-error` | #B42318<br><sub>nx-danger</sub> | #FF9989<br><sub>nx-error-dk-75</sub> |  |
| 状态 | `--nx-color-info` | `--color-info` | #6857E7<br><sub>nx-purple</sub> | #6857E7<br><sub>nx-purple</sub> | 信息态复用奈势紫（单色相品牌），必须带图标 |
| 状态 | `--nx-color-on-info` | `--color-on-info` | #FFFFFF<br><sub>nx-white</sub> | #FFFFFF<br><sub>nx-white</sub> |  |
| 状态 | `--nx-color-info-muted` | `--color-info-muted` | #F1F0FD<br><sub>nx-mist</sub> | #3C237C<br><sub>nx-purple-deep</sub> |  |
| 状态 | `--nx-color-on-info-muted` | `--color-on-info-muted` | #3C237C<br><sub>nx-purple-deep</sub> | #BBBBFE<br><sub>nx-lavender</sub> |  |
| 状态 | `--nx-color-text-info` | `--color-text-info` | #6857E7<br><sub>nx-purple</sub> | #BBBBFE<br><sub>nx-lavender</sub> |  |
| 状态 | `--nx-color-icon-info` | `--color-icon-info` | #6857E7<br><sub>nx-purple</sub> | #BBBBFE<br><sub>nx-lavender</sub> |  |
| 状态 | `--nx-color-border-info` | `--color-border-info` | #6857E7<br><sub>nx-purple</sub> | #BBBBFE<br><sub>nx-lavender</sub> |  |
| 交互 | `--nx-color-neutral` | `--color-neutral` | rgba(38, 38, 38, 0.06) | rgba(246, 246, 248, 0.12) | 中性浅填充（次按钮底、中性标签底） |
| 交互 | `--nx-color-overlay` | `--color-overlay` | rgba(38, 38, 38, 0.40) | rgba(0, 0, 0, 0.56) | 弹窗遮罩 |
| 交互 | `--nx-color-overlay-hover` | `--color-overlay-hover` | rgba(38, 38, 38, 0.05) | rgba(246, 246, 248, 0.06) | 悬停叠加（叠在原底上，不替换） |
| 交互 | `--nx-color-overlay-pressed` | `--color-overlay-pressed` | rgba(38, 38, 38, 0.09) | rgba(246, 246, 248, 0.10) | 按下叠加 |
| 交互 | `--nx-color-tint-hover` | `--color-tint-hover` | #262626<br><sub>nx-ink</sub> | #F6F6F8<br><sub>nx-surface</sub> | color-mix 用的悬停基色（Astryx 约定：浅色深、深色浅） |
| 交互 | `--nx-color-tint-brand-hover` | 本地 | rgba(104, 87, 231, 0.08) | rgba(187, 187, 254, 0.10) | 品牌色悬停叠加（列表项、幽灵按钮） |
| 交互 | `--nx-color-shadow` | `--color-shadow` | rgba(60, 35, 124, 0.10) | rgba(0, 0, 0, 0.30) | 阴影色（深紫调） |
| 交互 | `--nx-color-skeleton` | `--color-skeleton` | #E8E8EB<br><sub>nx-neutral-90</sub> | #3D3C3C<br><sub>nx-neutral-dk-25</sub> | 骨架屏 |
| 交互 | `--nx-color-track` | `--color-track` | #E8E8EB<br><sub>nx-neutral-90</sub> | #3D3C3C<br><sub>nx-neutral-dk-25</sub> | 进度条/滑轨底 |
<!--/GEN-->

**分类色**（Astryx 的 `--color-{background,border,icon,text}-{purple,gray}`）：紫 = 品牌紫，灰 = 中性灰，值见 tokens.json。其余 8 族（蓝、青、绿、橙、粉、红、蓝绿、黄）奈势没有定义，见第 11 节。

### 迁移对照（v1.2 写法 → v1.3 语义 token）

| v1.2 常见写法 | 改成 |
|---|---|
| `background: var(--nx-surface)`（页面底） | `var(--nx-color-background-body)` |
| `background: #fff / var(--nx-white)`（卡片） | `var(--nx-color-background-card)` |
| `color: var(--nx-ink)` | `var(--nx-color-text-primary)` |
| `color: var(--nx-gray)` | `var(--nx-color-text-secondary)` |
| `background: var(--nx-purple)` 按钮 | `var(--nx-color-accent)` + `color: var(--nx-color-on-accent)` |
| `:hover { background: var(--nx-purple-deep) }` | `var(--nx-color-accent-hover)` |
| `background: var(--nx-mist)` 标签/选中 | `var(--nx-color-accent-muted)` + `color: var(--nx-color-on-accent-muted)` |
| `border: 1px solid var(--nx-line)` | `var(--nx-color-border)`；输入框用 `var(--nx-color-border-emphasized)` |
| `box-shadow: 0 0 0 3px var(--nx-focus)` | `outline: var(--nx-focus-outline-width) solid var(--nx-focus-outline-color); outline-offset: var(--nx-focus-outline-offset)` |
| `var(--nx-shadow-floating)` | `var(--nx-shadow-high)`（浮层）或 `--nx-shadow-med`（菜单） |
| `var(--nx-radius-card)` 等 10 档 | `--nx-radius-inner / element / container / page / full` |
| `var(--nx-space-7)` 等 18 档 px | `--nx-spacing-N`（N × 4px） |
| `var(--nx-coral)` 作底 + 白字 | `var(--nx-color-highlight)` + `color: var(--nx-color-on-highlight)`（墨黑） |

v1.2 的旧变量全部保留为兼容别名，而且保持原值（旧页面不会跳）。新代码不要再用。

## 5. 色阶

生成方法：Astryx `astryx-oklch-v1`（OKLCH 色彩空间里按人眼亮度均匀取 21 档，0 黑、100 白），代码原样复用（`scripts/vendor/`，MIT）。参数：vibrancy 50；中性灰用 custom 档，以 #6E6E73 为种子；品牌色设为 exact 锚点（原值命中，脚本里有断言）。锚点位置按各色的感知亮度就近取档：深紫 20、奈势紫 45、薰衣草 80、雾紫 95；墨黑 15、中灰 45、浅灰 95；珊瑚橙 60。两种模式都单调递增，相邻档最小色差 2.6–4.0。

<!--GEN:palette-->
| 色系 | 模式 | 5 | 10 | 15 | 20 | 25 | 30 | 35 | 40 | 45 | 50 | 55 | 60 | 65 | 70 | 75 | 80 | 85 | 90 | 95 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 奈势紫 | 浅 | #130732 | #220F4D | #301866 | **#3C237C** | #462C8F | #4F38A4 | #5743B7 | #5F4AD4 | **#6857E7** | #7366F2 | #7E74FA | #8981FF | #9390FF | #A09DFF | #ADACFF | **#BBBBFE** | #CDCCFE | #E0DFFD | **#F1F0FD** |
| 奈势紫 | 深 | #13092E | #21114B | #301A66 | **#3C237C** | #462D8F | #4E38A3 | #5742B8 | #5F4AD4 | **#6857E7** | #7365F1 | #7E73F7 | #8982FB | #948FFD | #9F9DFF | #ADACFF | **#BBBBFE** | #CDCCFE | #E0DFFD | **#F1F0FD** |
| 中性灰 | 浅 | #111111 | #1B1B1B | **#262626** | #313030 | #3D3C3C | #4B4848 | #575457 | #636166 | **#6E6E73** | #7B7B80 | #87878C | #94949A | #A2A2A7 | #B0B0B4 | #BDBDC1 | #CCCCCF | #DADADD | #E8E8EB | **#F6F6F8** |
| 中性灰 | 深 | #111111 | #1B1B1B | **#262626** | #313030 | #3D3C3C | #4A4848 | #575457 | #636265 | **#6E6E73** | #7B7B7F | #87878C | #949499 | #A1A1A6 | #B0B0B3 | #BDBDC1 | #CBCBCE | #D9D9DD | #E7E7EA | **#F6F6F8** |
| 珊瑚橙 | 浅 | #2C0000 | #3E0000 | #500000 | #620000 | #750200 | #880500 | #9D0900 | #B01B0A | #C52D1C | #DB3E2B | #EF4F3B | **#FF604A** | #FF7A66 | #FF8E7C | #FFA08F | #FFB1A3 | #FFC4B9 | #FFD8D1 | #FFECE8 |
| 珊瑚橙 | 深 | #2B0000 | #3E0000 | #500000 | #620000 | #730A01 | #83160A | #942315 | #A72E20 | #BE3927 | #D74531 | #ED523C | **#FF604A** | #FF7B66 | #FF8F7C | #FFA08F | #FFB1A3 | #FFC4B9 | #FFD8D1 | #FFECE8 |
<!--/GEN-->

粗体为锚点（品牌原值）。珊瑚橙只给必要档：60 原色、55 按下、95 浅底；深色浅底由 #FF604A 以 18% 叠在 #262626 上得到 #4D302C。功能色（成功/警示/危险）以 v1.2 原值为锚点，生成浅底和深色模式用档，全部在 tokens.json。

## 6. 深色模式

- **底色：** 页面底和主画布是墨黑 #262626；卡片 #313030（neutral-dk-20）；浮层 #3D3C3C（neutral-dk-25）。层级越高越亮，配合阴影里的 1px 内描边。
- **品牌面：** 选中底、品牌浅底、信息浅底改为深紫 #3C237C，上面的字用薰衣草 #BBBBFE（6.76:1）。
- **文字：** 主文字浅灰 #F6F6F8（14.0:1），次文字 #BDBDC1，链接/强调字用薰衣草（8.40:1）。
- **主按钮：** 仍是奈势紫 #6857E7 配白字（5.11:1），品牌识别不变。注意：奈势紫在深色底上只有 2.96:1，纯图形选中态（复选框、开关、进度条）在深色下用 `border-accent`（薰衣草）。
- **状态色：** 强填充换成色阶 70 档并配墨黑字，文字用 75 档，浅底是状态色以 20% 叠在墨黑上。

## 7. 字号与字重

MiSans。基准 16px，比率约 1.25：`--nx-font-size-xs/sm/base/lg/xl/2xl/3xl/4xl/5xl` = 12/14/16/20/24/30/38/48/60px（`2xs` 10px 只给英文微标，中文最小 12px）。名字与 Astryx 同档位对齐，数值不同（Astryx 是 14px、1.2 比率）。

<!--GEN:type-->
| 角色 | 字号 | 字重 | 行高 | 字距 | 用途 |
|---|---|---|---|---|---|
| display-1 | 60px | semibold | 1.1 | -0.02em | 首屏大标题（桌面；移动端用 3xl） |
| display-2 | 48px | semibold | 1.15 | -0.015em | 区块大标题、封面 |
| display-3 | 38px | semibold | 1.2 | -0.01em | 大数字、引语 |
| heading-1 | 38px | semibold | 1.2 | -0.01em | 页面标题 |
| heading-2 | 30px | semibold | 1.3 | -0.005em | 一级区块标题 |
| heading-3 | 24px | semibold | 1.35 | 0em | 卡片标题、二级标题 |
| heading-4 | 20px | semibold | 1.4 | 0em | 小节标题 |
| heading-5 | 16px | semibold | 1.5 | 0em | 列表组标题 |
| heading-6 | 14px | semibold | 1.5 | 0em | 表头、分组小标题 |
| large | 18px | normal | 1.7 | 0em | 导语、引言 |
| body | 16px | normal | 1.75 | 0em | 正文（中文段落） |
| label | 14px | medium | 1.4 | 0.01em | 按钮、表单标签、导航 |
| supporting | 12px | normal | 1.5 | 0.01em | 注释、来源、时间戳 |
| code | 14px | normal | 1.6 | 0em | 代码 |
<!--/GEN-->

- 同一版面不超过 3 个字号层级、2 种字重（沿用 v1.2）。
- 移动端：display-1 用 3xl（38px），display-2 用 2xl（30px）。
- 印刷、PPT、竖屏视频的字号沿用 v1.2 表格；视频、社媒封面标题仍用 Bold 700。

## 8. 间距

<!--GEN:spacing-->
| token | Astryx | 值 | 像素 | 说明 |
|---|---|---|---|---|
| `--nx-spacing-0` | `--spacing-0` | 0rem | 0px |  |
| `--nx-spacing-0-5` | `--spacing-0-5` | 0.125rem | 2px |  |
| `--nx-spacing-1` | `--spacing-1` | 0.25rem | 4px |  |
| `--nx-spacing-1-5` | `--spacing-1-5` | 0.375rem | 6px |  |
| `--nx-spacing-2` | `--spacing-2` | 0.5rem | 8px |  |
| `--nx-spacing-3` | `--spacing-3` | 0.75rem | 12px |  |
| `--nx-spacing-4` | `--spacing-4` | 1rem | 16px |  |
| `--nx-spacing-5` | `--spacing-5` | 1.25rem | 20px |  |
| `--nx-spacing-6` | `--spacing-6` | 1.5rem | 24px |  |
| `--nx-spacing-7` | `--spacing-7` | 1.75rem | 28px |  |
| `--nx-spacing-8` | `--spacing-8` | 2rem | 32px |  |
| `--nx-spacing-9` | `--spacing-9` | 2.25rem | 36px |  |
| `--nx-spacing-10` | `--spacing-10` | 2.5rem | 40px |  |
| `--nx-spacing-11` | `--spacing-11` | 2.75rem | 44px |  |
| `--nx-spacing-12` | `--spacing-12` | 3rem | 48px |  |
| `--nx-spacing-16` | 本地 | 4rem | 64px | 奈势本地：区块级大间距 |
| `--nx-spacing-20` | 本地 | 5rem | 80px | 奈势本地：区块级大间距 |
| `--nx-spacing-24` | 本地 | 6rem | 96px | 奈势本地：区块级大间距 |
| `--nx-space-tight` | 本地 | var(--nx-spacing-2) | 8px | 8px · 标签与字段、图标与文字 |
| `--nx-space-related` | 本地 | var(--nx-spacing-4) | 16px | 16px · 同组元素之间 |
| `--nx-space-group` | 本地 | var(--nx-spacing-8) | 32px | 32px · 组与组之间 |
| `--nx-space-section` | 本地 | var(--nx-spacing-24) | 96px | 96px · 页面区块之间（移动端 spacing-16 = 64px） |
| `--nx-space-card` | 本地 | var(--nx-spacing-8) | 32px | 32px · 卡片内边距（紧凑卡片 spacing-6） |
| `--nx-space-control-x` | 本地 | var(--nx-spacing-4) | 16px | 16px · 按钮/输入框水平内边距 |
<!--/GEN-->

## 9. 圆角、阴影、焦点、控件高度

<!--GEN:radius-->
| token | Astryx | 值 | 用途 |
|---|---|---|---|
| `--nx-radius-none` | `--radius-none` | 0px |  |
| `--nx-radius-inner` | `--radius-inner` | 0.375rem | 6px · 嵌套在控件/卡片里的元素、代码片段 |
| `--nx-radius-element` | `--radius-element` | 0.625rem | 10px · 按钮、输入框、下拉、小图 |
| `--nx-radius-container` | `--radius-container` | 1rem | 16px · 卡片、弹窗、提示条、菜单 |
| `--nx-radius-page` | `--radius-page` | 1.75rem | 28px · Hero、特性大面板、封面卡 |
| `--nx-radius-chat` | `--radius-chat` | var(--nx-radius-page) | 对话气泡容器，同 page |
| `--nx-radius-full` | `--radius-full` | 9999px | 胶囊：标签、头像、开关 |
<!--/GEN-->

<!--GEN:shadow-->
| token | 浅色 | 深色 | 用途 |
|---|---|---|---|
| `--nx-shadow-low` | 0 1px 2px rgba(38, 38, 38, 0.04), 0 2px 8px rgba(60, 35, 124, 0.05) | 0 1px 2px rgba(0, 0, 0, 0.30), 0 2px 8px rgba(0, 0, 0, 0.30), inset 0 0 0 1px rgba(246, 246, 248, 0.06) | 悬停抬起的卡片、吸顶栏 |
| `--nx-shadow-med` | 0 2px 4px rgba(38, 38, 38, 0.04), 0 8px 20px rgba(60, 35, 124, 0.07) | 0 2px 4px rgba(0, 0, 0, 0.35), 0 8px 20px rgba(0, 0, 0, 0.45), inset 0 0 0 1px rgba(246, 246, 248, 0.08) | 下拉菜单、气泡、浮动工具条 |
| `--nx-shadow-high` | 0 4px 8px rgba(38, 38, 38, 0.05), 0 16px 40px rgba(60, 35, 124, 0.10) | 0 4px 8px rgba(0, 0, 0, 0.45), 0 16px 40px rgba(0, 0, 0, 0.60), inset 0 0 0 1px rgba(246, 246, 248, 0.10) | 弹窗、抽屉（最高层） |
| `--nx-shadow-inset-hover` | inset 0 0 0 2px rgba(38, 38, 38, 0.15) | inset 0 0 0 2px rgba(246, 246, 248, 0.20) | 输入框状态环（不是层级阴影） |
| `--nx-shadow-inset-selected` | inset 0 0 0 2px rgba(104, 87, 231, 0.50) | inset 0 0 0 2px rgba(187, 187, 254, 0.50) | 输入框状态环（不是层级阴影） |
| `--nx-shadow-inset-success` | inset 0 0 0 2px rgba(8, 117, 95, 0.30) | inset 0 0 0 2px rgba(110, 189, 166, 0.30) | 输入框状态环（不是层级阴影） |
| `--nx-shadow-inset-warning` | inset 0 0 0 2px rgba(180, 95, 6, 0.30) | inset 0 0 0 2px rgba(244, 164, 104, 0.30) | 输入框状态环（不是层级阴影） |
| `--nx-shadow-inset-error` | inset 0 0 0 2px rgba(180, 35, 24, 0.30) | inset 0 0 0 2px rgba(247, 134, 118, 0.30) | 输入框状态环（不是层级阴影） |
<!--/GEN-->

- 焦点环：2px 实线、外偏移 2px，颜色是 `border-accent`（浅色奈势紫，深色薰衣草），替换 v1.2 的 30% 透明光晕（光晕只有约 1.5:1，键盘用户看不清）。
- 控件高度：sm 32 / md 40 / lg 48px（Astryx 是 28/32/36；奈势以营销页和移动端为主，取更大的触控尺寸）。
- 边框统一 1px。

## 10. 动效

取 Astryx Neutral 主题这一组：快 125ms、中 300ms、慢 700ms，每档的 min/max 按 0.75 比率得出。比 Astryx 核心默认（175/410/975）更利落，符合工具产品的节奏。

<!--GEN:motion-->
| token | 值 | 用途 |
|---|---|---|
| `--nx-duration-fast-min` | 95ms |  |
| `--nx-duration-fast` | 125ms | 悬停、按下、开关、颜色变化 |
| `--nx-duration-fast-max` | 165ms |  |
| `--nx-duration-medium-min` | 225ms |  |
| `--nx-duration-medium` | 300ms | 浮层进出、展开收起 |
| `--nx-duration-medium-max` | 400ms |  |
| `--nx-duration-slow-min` | 525ms |  |
| `--nx-duration-slow` | 700ms | 大面积转场、首屏入场（每页至多一处） |
| `--nx-duration-slow-max` | 935ms |  |
| `--nx-duration-exit` | var(--nx-duration-fast) | 退出比进入快 |
| `--nx-ease-standard` | cubic-bezier(0.24, 1, 0.4, 1) | 默认减速：到达与状态变化 |
| `--nx-ease-entrance` | cubic-bezier(0.24, 1, 0.4, 1) | 入场（不回弹） |
| `--nx-ease-move` | cubic-bezier(0.24, 1, 0.4, 1) | 位移、尺寸变化 |
| `--nx-ease-exit` | cubic-bezier(0.3, 0, 0.6, 0.6) | 离场：从静止加速离开 |
<!--/GEN-->

- 退出比进入快（exit = fast），离场用加速曲线。
- 入场不回弹，不做弹性动画。
- `prefers-reduced-motion` 下，中、慢档降为快档。

## 11. 对比度检查结论

脚本：`scripts/build.mjs`，报告：`contrast-report.md`。浅色、深色各 59 组语义组合：**不达标 0 组**，受限 8 组（浅色 6、深色 2），都按「不改品牌原值、用规则约束」处理：

| 组合 | 对比度 | 规则 |
|---|---|---|
| 珊瑚橙字/色块在白底、浅灰底 | 2.99 / 2.77 | 不能单独承载信息：作填充时块内墨黑字，作文字时只当装饰 |
| 中灰字 #6E6E73 在雾紫底 #F1F0FD | 4.497 | 差 0.003 到 4.5：雾紫底上的说明文字用深紫 `on-accent-muted` |
| 深色：奈势紫填充在 #262626 / #313030 | 2.96 / 2.57 | 主按钮靠白字没问题；纯图形选中态改用薰衣草 |

原始色组合里还要注意（设计稿、视频、海报直接取色时）：薰衣草在奈势紫上 2.84、奈势紫在深紫上 2.38、中灰在墨黑上 2.98、薰衣草在白底上 1.80，都只能做装饰。深底上的薰衣草可以放心当正文：深紫底 6.76、墨黑底 8.40。

## 12. 与 Astryx 的对齐和差异

- 映射表：`astryx-mapping.md`。211 个核心 token 中对上 179 个（84.8%）。对不上的 32 个全部是 8 族多色分类色（`--color-{background,border,icon,text}-{blue,cyan,green,orange,pink,red,teal,yellow}`），奈势规范里没有。
- `tokens.json` 自足：`tokens.css`、`astryx-mapping.md` 和本文的表格都只从 tokens.json 生成。主题包取 `color.*.light/dark.value` 写成 `[浅, 深]` 元组，取 `tokens.*.value` 写单值，`astryx` 为 null 的进 `localTokens`，`palette.families` 可直接作为 `palette.generated`。
- 名字相同、用法不同的几处（主按钮悬停、info 复用紫色、字号数值、控件高度等），映射表第 4 节逐条列出。

## 13. 与 v1.2 的变更清单

**新增**
- 语义色层 `--nx-color-*`，81 个，浅色和深色两套，命名对齐 Astryx。
- 色阶：奈势紫、中性灰、珊瑚橙各 19 档 × 浅/深两套；功能色补了浅底和深色档。
- 深色模式：`[data-theme="dark"]` 加跟随系统。
- 字号 token（10 档）、文字角色 token（14 个角色的字号、字重、行高、字距）、`--nx-measure` 行宽。
- 间距 `--nx-spacing-N`（rem）以及 6 个用途间距（tight / related / group / section / card / control-x）。
- 圆角四档加胶囊，带同心规则。
- 阴影 low/med/high（浅/深两套），以及输入框状态环 `shadow-inset-*`。
- 动效：时长 10 个、缓动 4 个，加 reduced-motion 规则。
- 焦点环、控件高度、边框宽度。
- 对比度检查脚本和报告；Astryx 映射表。

**改动**
- 主按钮悬停：深紫 #3C237C → purple-40 #5F4AD4；按下 purple-35 #5743B7。
- 焦点：30% 紫色光晕 → 2px 实线外描边。
- 阴影：最重一档从墨黑 13–16% 改为深紫 10%；静止卡片不再加阴影。
- 网页标题字重 700 → 600；正文行高统一 1.75。
- 分隔线从 `rgba(0,0,0,.09)` 改为实色 neutral-90 #E8E8EB（与冷紫调灰一致）。
- `--nx-font`、`--nx-weight-*` 改为指向新的 `--nx-font-family-*`、`--nx-font-weight-*`，值不变。

**保留**
- 所有品牌原色、Logo 渐变、禁用项。
- v1.2 全部旧变量名（圆角、间距、阴影、`--nx-line` 等）作为兼容别名，保持原值。

## 14. Xiangjun 的决定（2026-11-12）

1. 主按钮悬停用相邻的紫 #5F4AD4，按下用 #5743B7。
2. 深色模式背景用中性墨黑 #262626，品牌感靠深紫选中面来出。
3. 暂不新增奈势分类色，主题包里 32 个分类色 token 继承 Astryx 默认值。
4. 网页标题字重用 600；视频封面和社媒仍用 700。
5. 视频封面大字「17%」从 #6857E7 改为 #BBBBFE（深紫底上对比度从 2.38 提到 6.76）。
6. （1.3.1）深色错误 Toast 底色改为 #B42318，与浅色一致，配 #F6F6F8 字（6.09）；深色 `--nx-color-error` 改为 #E8705F 配墨黑（4.98）；深色错误文字和图标用 #F78676（墨黑底 6.21，卡片底 5.40）；深色错误边框仍为 #FF9989。
7. （1.3.2）组件库的危险按钮统一用珊瑚橙 #FF604A 配墨黑，浅深相同，取代 1.3.1 里的深色危险按钮 #E8705F；全局 error 与 Toast 不变。
8. 组件库并入品牌规范网站：brand.nexai.link/components.html（第 7/10 章，排在应用规范之后），/ui/ 301 跳转过来。

## 15. 文件与重新生成

```
v1.3/
  tokens.json            唯一来源（主题包也从这里生成）
  tokens.css             由 tokens.json 生成
  spec.md                本文（表格由 tokens.json 生成）
  astryx-mapping.md      Astryx 核心 token 映射，含覆盖率
  contrast-report.md     WCAG 对比度报告
  preview.html / preview.png / preview-light.png / preview-dark.png
  scripts/
    palette.mjs          色阶请求与锚点
    build.mjs            语义映射与非颜色 token 定义 → tokens.json + contrast-report.md
    emit.mjs             tokens.json → tokens.css + astryx-mapping.md
    spec-tables.mjs      tokens.json → spec.md 表格
    preview.mjs, render.py  预览页与截图（playwright + /usr/bin/google-chrome）
    vendor/              Astryx 色阶生成器原文件（MIT）与核心 token 清单
```

重新生成：`node scripts/build.mjs && node scripts/emit.mjs && node scripts/spec-tables.mjs && node scripts/preview.mjs && python3 scripts/render.py`
