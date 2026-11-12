---
name: naishi-brand
description: 奈势AI（NexAI）品牌规范执行包。凡是为奈势AI / NexAI 做任何设计、文案或制作——网站、App、小程序、社交媒体与自媒体（X、小红书、公众号、视频号、抖音、B站、LinkedIn）、PPT、名片海报画册等对外物料、活动物料（背景板、易拉宝、展台、胸牌、礼品）、办公环境标识——在动手前使用本 Skill，并在交付前按清单自检。
---

# 奈势AI 品牌规范（naishi-brand）

本 Skill 把《奈势AI 品牌规范 v1.3.2》（品牌规范官网 https://brand.nexai.link + 组件库 https://brand.nexai.link/components.html）压缩成可执行规则。色彩与 Logo 以品牌视觉板 SVG 原文件为唯一来源（用户确认）；界面色值、深色模式与组件以 `tokens.json`（v1.3.2）为唯一数据源。目标不是让每件作品长得一样，而是让每件作品一眼就是奈势AI：**开放（Open）· 伙伴（Partner）· 创造（Create）**。

## 0. 固定信息（原文照用，不改写）

| 项目 | 内容 |
|---|---|
| 中文品牌名 | **奈势AI**（无空格，AI 大写） |
| 英文品牌名 | **NexAI**（不写 Nex AI / NEXAI / Nexai） |
| 使命 | **成就每一位AI创造者**（英文 Empower Every AI Builder） |
| 愿景 | **全球领先的下一代AI共创平台** |
| 口号 | **一起热爱，一起成长！**（全角逗号与感叹号） |
| 官网 | **nexai.link**；需可点击链接时 **https://nexai.link**（全小写、无 www、无结尾斜杠） |
| 品牌规范站 | **https://brand.nexai.link**（组件库 https://brand.nexai.link/components.html；下载 https://brand.nexai.link/downloads.html） |
| 品牌个性 | **Open 开放 · Partner 伙伴 · Create 创造**（v1.2 起品牌个性与核心价值合并为这一组） |
| 吉祥物 | 小奈；产品内 AI 伙伴称"小奈同学" |

愿景与口号暂无官方英文，不要自行翻译；需要时向用户/品牌组确认。

## 1. 执行步骤

1. **识别触点**：确定是 数字产品 / 社媒 / PPT / 印刷物料 / 活动 / 办公 中的哪一类，打开下方对应 reference（只读需要的，但要读完整）。做网站 / App / 组件时同时读 `references/07-digital-product.md`、`references/spec-v1.3.md` 和官网组件库。
2. **先取官方素材，不重画**：Logo、小奈（标准形象 / 圆形头像 / 表情 / 动态表情 / 动作）、token、模板全部来自 `assets/`；仓库里没有的大文件（PPT 模板、PDF 手册、2400w Logo、素材包）从 https://brand.nexai.link/downloads.html 下载。若只拿到本文件（未克隆仓库），素材按 `https://raw.githubusercontent.com/15011219788-afk/nexai-brand-ui-skill/main/<路径>` 读取。
3. **定版式骨架**：Logo 位置 → 一个标签 → 一个大标题 → 说明 → 小奈/图片 → 官网。先划"文字区"和"小奈区"，两区不重叠。一个版面只讲一件事、只有一个主行动。
4. **按色彩语义上色**：白灰为空间，奈势紫 #6857E7 为身份与主行动，珊瑚橙 #FF604A 是唯一强调色（时间性/增长，也是破坏性/强调按钮底），墨黑 #262626 做文字和深色背景；Logo 渐变只在 Logo 里。界面不要硬编码近似色，引用 `assets/tokens/tokens.css` 的语义变量 `--nx-color-*`。
5. **写文案**：动词 + 结果开头，平实具体；固定信息照抄第 0 节；数据标来源与日期。
6. **按第 3 节清单自检**，列出你新增或假设的内容，交给用户确认。

## 2. 硬规则（任何触点都适用）

### Logo
- 只用 `assets/logo/svg/` 中的官方文件：横版（首选）→ 竖版 → 图形标。
- 三种官方色彩版本（视觉板）：彩色版（渐变标 + #262626 字）用白底，也可用 #F6F6F8 / #F1F0FD 浅底；反白版（渐变标 + 白字）用墨黑 #262626 底；全白版用奈势紫 #6857E7 底，也用于深紫 #3C237C 底与照片；单色黑 #000000 只用于黑白印刷。没有单色紫图形标。
- 比例（视觉板实测）：字标高 ≈ 0.60 H，图形标与字标间距 ≈ 0.21 H（H = 图形标高）。
- 安全空间 X = 图形标高 × 0.5；屏幕最小横版高 24px、图形标 16px；印刷最小横版宽 25mm、图形标 6mm。
- 禁止：拉伸、旋转、改色、加特效/描边/投影、调换位置、用字体重打"奈势AI"、放在复杂图片或低对比背景、被小奈或其他元素压住、自拼英文字标、**放在菱形网格 / 像素底纹上**（v1.2）。Logo 背景只用干净纯色或平静照片区域。

### 色彩（品牌原色唯一来源：视觉板 SVG；界面语义色唯一来源：tokens.json v1.3.2）
- 紫色色阶：奈势紫 #6857E7（主行动/选中/身份）、深紫 #3C237C（深色强调块）、薰衣草紫 #BBBBFE（装饰、墨黑底强调文字）、雾紫 #F1F0FD（浅底面板）。
- 主按钮：底 #6857E7、字白；悬停 #5F4AD4、按下 #5743B7（不要再用深紫 #3C237C 做悬停）。语义 token：`--nx-color-accent` / `--nx-color-accent-hover` / `--nx-color-accent-pressed`，字 `--nx-color-on-accent`。
- 强调与破坏性/强调按钮：珊瑚橙 #FF604A，配墨黑字 #262626（5.06:1）。悬停 #FA5B46（墨黑 4.79:1）、按下 #F75742（墨黑 4.60:1）。白字在珊瑚橙上只有 2.98:1，禁止。用本地 token `--nx-color-button-danger*`，不要改全局 `--nx-color-error`（以免影响 Toast 与状态色）。每版只出现一处珊瑚橙。
- 中性：墨黑 #262626、中灰 #6E6E73、浅灰 #F6F6F8、白 #FFFFFF。深色模式页面底是中性墨黑 #262626，不是紫底。
- 比例：白灰约 55%，墨黑约 20%，奈势紫 ≤ 10%，珊瑚橙 ≤ 5%。营销物料可用墨黑做主背景。
- Logo 渐变 #7417FF 25% → #FE6702 只存在于 Logo 图形标内；#7417FF、#FE6702 不是独立品牌色（v1.0 的旧行动橙、旧深海蓝也已废弃），不得用于按钮、文字、底色或装饰图形。#F26322 不是品牌色，任何场景不用。
- 功能色（成功 #08755F / 警示 #B45F06 / 危险 #B42318）仅限产品界面状态，视觉板未定义，不进营销物料。
- 深色错误 Toast：底 #B42318（与浅色相同），字 #F6F6F8（6.09:1），token `--nx-color-background-error-inverted`。深色错误文字和图标用 #F78676（`--nx-color-text-error` / `--nx-color-icon-error`）。深色 error 强填充 #E8705F 配墨黑（4.98:1）只用于状态填充，不作强调按钮。
- **白底不用珊瑚橙 #FF604A 做文字。** 唯一例外：品牌大字（≥48px，如品牌理念页「Create」）用独立定值 **#E5503A**（对白 3.79:1）。#E5503A 不是色阶档，不进 palette，也不在 `tokens.json` 的 ramp 里；色块、图形、按钮仍用 #FF604A。
- 对比度（WCAG 2.x，向下取两位小数，不四舍五入）：正文 ≥4.5，大字（中文 ≥24px 常规或 ≥19px 粗体）与图标/控件边界 ≥3。完整对照见 `references/contrast-report.md`。奈势紫底白字 5.11 ✓；墨黑底不用奈势紫文字（2.95 ✕，改用 #BBBBFE 或白色）。

### 设计 Token 与深色模式（v1.3）
- 三层，组件只使用语义层：原始色 `--nx-*` → 色阶 `--nx-<色系>-<stop>`（深色色阶 `--nx-<色系>-dk-<stop>`）→ 语义 `--nx-color-*`。
- 引用 `assets/tokens/tokens.css`（与 `tokens-v1.3.2.css` 相同）或 `tokens.json`；v1.2 旧变量名全部保留为兼容别名。细则见 `references/14-tokens-v1.3.md` 与 `references/spec-v1.3.md`。
- 深色模式同时支持 `<html data-theme="dark">` 与 `prefers-color-scheme`。品牌站开关把选择存在 `localStorage` 键 `nx-theme`（`light` / `dark` / 未设则跟随系统）；为避免闪白，须在首屏绘制前用头部脚本读这个键并写到 `data-theme`。`data-theme="light"` 固定浅色。
- 使用 Meta Astryx（React 19，`@astryxdesign/core` 0.7.15）的项目：安装 `assets/theme/nexai-theme-nexai-1.3.2.tgz`，用 `<Theme theme={nexaiTheme}>` 包住应用，破坏性按钮走 `variant:destructive`。映射表见 `references/astryx-mapping.md`。不用 React 的项目直接引用 `tokens.css`。

### 字体（v1.2：MiSans；v1.3：网页标题字重 600）
- 所有触点统一使用 **MiSans**（小米出品，可免费商用，下载 https://hyperos.mi.com/font，按小米 MiSans 许可协议使用）。
- 字体栈：`MiSans, 'PingFang SC', 'Microsoft YaHei', sans-serif`；字重 Regular 400 / Medium 500 / Semibold 600 / Bold 700。
- **网页标题默认字重 600**（`--nx-font-weight-semibold`）。Bold 700 只用于视频字幕、社媒封面等远看场景。
- PPT 主题字体 MiSans，对外导出 PDF 内嵌字体；印刷与视频交付前转曲或嵌入。
- 不再使用 v1.1 的思源黑体 / Inter / 微软雅黑分场景方案。

### 辅助图形（v1.2：像素方块停用）
- 像素方块 L 形 / 台阶形辅助图形、菱形网格（像素场）底纹**全部停用**，不出现在任何新物料中。
- 像素元素只存在于 Logo 图形标与小奈犄角、袖标、口袋图案中；装饰用留白、纯色块、大标题、小奈。

### 小奈
- 只用官方文件（`assets/mascot/`）：标准形象 `xiaonai-standard@*`、圆形头像 `avatar/`、12 枚表情 `expressions/`、12 枚动态表情 `animated/`（GIF）、8 个动作 `poses/`。
- **圆形头像**：小奈居中、完整头部（犄角、双耳、下巴都在圆内）；只用 `avatar/xiaonai-avatar-circle-*` 或方形版交平台裁圆，不自己裁全身图。
- **小奈不压文字，文字不压小奈**：文字区与小奈区分开（左右分栏 / 上下分区 / 独立卡片），间距 ≥ 1 个图形标高。
- 表情贴纸配字在小奈下方；要换配字用 `expressions/no-text/`，把字排在小奈外。严肃场景不发表情。
- 保留像素犄角、袖口像素 Logo、口袋像素图案、紫色卫衣、紫色眼睛；不拉伸、不改色、不镜像、不去色、不切掉犄角/头部、不放在奈势紫底或复杂照片上。
- 不出现在认证结论、证书、薪资数据旁边暗示担保；不代言合作方。
- 与 Logo 组合：间距 ≥ 2X，小奈高度 ≥ Logo 高度 3 倍；小奈单独出现时画面中仍需有"奈势AI"。
- 表情与动作为 v1.2 延展设计稿，大规模商用前由品牌组验收；需要库里没有的新动作时停下来问。

### 文案与可信边界
- 禁止：空泛口号（重塑未来/颠覆）、保证就业或薪资、"国际标准认证"、学位等价、把 AI 预审写成认证、把链接写成原创证明、假数据与假合作方。
- 中英文之间加半角空格（品牌名与使命/愿景原文除外）；产品栏目沿用"我的 AI 护照 / AI护照、项目、社区、机会"。

## 3. 触点清单（交付前逐项打勾）

**通用**：□ 官方 Logo 未变形 □ 安全空间与最小尺寸达标 □ 固定信息原文 □ 官网写作 nexai.link □ 紫/橙用法符合语义 □ 对比度达标（正文 ≥4.5，大字/图标/边框 ≥3） □ 无虚假数据/承诺 □ 新增内容已标注待确认

**网站 / App / 小程序** → `references/07-digital-product.md`；组件样式对照 https://brand.nexai.link/components.html
□ 引用 `tokens.css` 语义层 `--nx-color-*`，无硬编码近似色 □ 每区一个紫色主按钮 44px，悬停 #5F4AD4、按下 #5743B7 □ 破坏性/强调按钮用珊瑚橙配墨黑，不用白字 □ 白底大字不用 #FF604A（≥48px 品牌大字才用 #E5503A） □ 卡片用 1px 边框不用常规阴影 □ 网页标题字重 600 □ MiSans 字体栈 □ 深色模式（`data-theme` + 系统偏好）已检查 □ Phosphor 图标 □ 1440 / 中屏 / 390 均检查、无横向溢出 □ 小程序避让胶囊 □ App 图标只用图形标 □ 证据等级与人工复核表述正确

**社交媒体 / 自媒体 / 视频** → `references/08-social-media.md`
□ 尺寸与安全区符合平台 □ Logo 左上、标题 ≤ 16 字 □ 小奈与文字分区、互不遮挡 □ 无像素方块 / 菱形底纹 □ 圆形头像用 v1.2 版 □ 底部官网 □ 字幕 MiSans、避开底部 UI 区 □ 片尾：竖版 Logo + 口号 + nexai.link □ 话题 ≤ 5、emoji ≤ 3 □ 远看标题可用字重 700

**PPT** → `references/09-ppt.md`
□ 使用 PPT 模板 v1.2（https://brand.nexai.link/downloads.html 下载 `奈势AI-PPT模板-v1.2.pptx`）示例版式、主题字体 MiSans □ 标题写结论 □ 每页一个结构、≤ 3 要点 □ 封面/结尾的口号、使命、官网未改 □ 对外发 PDF

**对外物料（名片/单页/海报/画册/邮件签名）** → `references/10-collateral.md`
□ 出血与最小字号 □ CMYK 输出并打样 □ 名片背面口号 + 官网 □ 二维码 ≥ 25mm □ 邮件签名纯文本信息

**活动物料** → `references/11-events.md`
□ 背景板关键信息在上 2/3 □ 合作方 Logo 小于奈势AI 并置于底部 □ 易拉宝底部 20cm 不放信息 □ 胸牌身份色 □ 礼品一件一个主元素、先打样

**办公环境** → `references/12-workplace.md`
□ Logo 墙中心 1.6–1.8m、宽 ≤ 墙宽 50% □ 会议室按名校简称命名（不用校徽校色） □ 门牌格式 楼层-编号 + 主名 + 副名 + 人数，MiSans □ 导视墨黑白字 □ 文化墙用原文

**审批与归档** → `references/13-governance.md`
□ 判定 A/B/C 审批级别 □ 文件名 `NexAI_类别_名称_规格_版本_日期` □ 源文件入素材库

## 4. References（按章拆分，规则优先）

- `references/01-foundation.md` 品牌基础、语气、名称与网址写法
- `references/02-logo.md` Logo 版本、尺寸、背景、错误用法
- `references/03-color.md` 色值、比例、对比度、印刷参考值（含 v1.3.2 语义色与按钮规则）
- `references/04-typography.md` MiSans 与授权、字号层级、排版（网页标题字重 600）
- `references/05-graphics.md` 停用的像素辅助图形、图标、摄影、AI 生成图
- `references/06-mascot.md` 小奈形象、圆形头像、12 表情、8 动作、不压文字、组合
- `references/07-digital-product.md` 网站 / App / 小程序、设计 token、深色模式、组件库
- `references/08-social-media.md` 头像、尺寸、模板、视频、语气
- `references/09-ppt.md` 母版版式与制作规则
- `references/10-collateral.md` 名片、单页、海报、画册、邮件签名
- `references/11-events.md` 背景板、易拉宝、展台、胸牌、门票、礼品
- `references/12-workplace.md` 前台、门牌、导视、名校会议室、工位、文化墙
- `references/13-governance.md` 审批、命名、素材库、FAQ
- `references/14-tokens-v1.3.md` v1.3 三层 token、深色模式、关键语义色与主题包用法
- `references/spec-v1.3.md` v1.3.2 完整规范（设计同步稿，表格来自 tokens.json）
- `references/astryx-mapping.md` Astryx 核心 token 映射与覆盖率
- `references/contrast-report.md` WCAG 对比度报告（含 1.3.1 / 1.3.2 补充表）
- `references/changelog.md` 新增规范 / 建议稿 / 待确认清单与资料缺口

## 5. Assets

- `assets/logo/svg/`：`nexai-logo-horizontal-{color,reverse,white,black}.svg`、`nexai-logo-vertical-*.svg`、`nexai-mark-{color,white,black}.svg`
- `assets/logo/png/`：同上 PNG（600/1200w，图形标 256/512w；2400w / 1024w 大图在官网下载页的素材包里）
- `assets/mascot/`：`xiaonai-standard@{500,1000}h.{png,webp}`
- `assets/mascot/avatar/`：圆形头像（雾紫 / 白，400 / 1024）、方形头像
- `assets/mascot/expressions/`：`sticker/`（12 枚带字贴纸 512×600）、`no-text/`（无字版 512×512）
- `assets/mascot/animated/`：12 枚动态表情 `NN-<名>.gif`（240×240 透明 GIF、带字、循环，单个 ≤ 300KB，可直接用于聊天 / 社群 / 网页）；无字版、480 高清版和微信表情投稿包见官网下载页
- `assets/mascot/poses/`：8 个延展动作（768×1024 透明 PNG）
- `assets/tokens/tokens.css`、`tokens.json`：当前规范（v1.3.2）；同目录另有 `tokens-v1.3.2.*` 与归档 `tokens-v1.2.*`
- `assets/theme/nexai-theme-nexai-1.3.2.tgz`：Astryx 主题包（`pnpm add ./nexai-theme-nexai-1.3.2.tgz`）
- `assets/android/nexai-android-colors-v1.3.2.zip`：安卓 `values` / `values-night` 颜色资源
- `assets/color/` ASE / GPL / JSON 色板（品牌原色，v1.3 未变）
- `assets/social/`：各平台 HTML 模板（改字后用浏览器按 meta size 截图导出）
- PPT 模板、PDF 手册、完整素材包、表情包 zip：不放仓库，从 https://brand.nexai.link/downloads.html 下载
- 完整可视化规范：品牌规范官网 **https://brand.nexai.link**；组件库 **https://brand.nexai.link/components.html**（排在「应用规范」后；旧地址 `/ui/` 会跳转过来）。拿不准时以官网为准。

## 6. 何时停下来问

- 需要的 Logo 版本、英文字标、小奈动作 / 表情在 `assets/` 中不存在；
- 有人要求使用像素方块辅助图形、菱形网格底纹或让小奈压字；
- 需要写公司数据、排名、合作关系、认证结论、薪资等事实而没有来源；
- 需求要求改动 Logo、使命、愿景、口号或官网写法；
- 外部风格参考会覆盖奈势AI 的颜色、字体或命名；
- 要对外发布、提交或印刷 A 级物料（见 governance）而未经审批。

## 7. 输出约定

交付时说明：① 触点与所用模板；② 使用的素材与 token（注明 v1.3.2）；③ 清单自检结果；④ 你新增或假设的内容（标注"待确认"）；⑤ 无法获得的素材。
