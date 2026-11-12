# 奈势AI 品牌规范 Skill（v1.3.2）

> NexAI (奈势AI) brand guidelines packaged as an Agent Skill — colours, semantic tokens, dark mode, MiSans type, logo, mascot 小奈 and do/don't rules for any AI agent doing design work.

把《奈势AI 品牌规范 v1.3.2》压缩成 AI Agent 可直接执行的规则 + 官方素材。让 Cursor、Claude Code 或任意 Agent 做海报、PPT、社媒图、网页 / 产品界面、文案时，自动遵守奈势的色彩、语义 token、深色模式、字体、Logo、小奈与禁用规则，并在交付前按清单自检。

- 可视化规范官网：**https://brand.nexai.link**
- 组件库（排在「应用规范」后）：**https://brand.nexai.link/components.html**
- 大文件下载（Token、Astryx 主题包、安卓颜色、PPT 模板、PDF 手册、完整素材包、表情包、微信表情投稿包）：https://brand.nexai.link/downloads.html
- Skill 入口（raw）：https://raw.githubusercontent.com/15011219788-afk/nexai-brand-ui-skill/main/SKILL.md

## 最快用法：复制这段话发给你的 Agent

```text
请先完整阅读奈势AI品牌规范 Skill：https://raw.githubusercontent.com/15011219788-afk/nexai-brand-ui-skill/main/SKILL.md
（完整仓库含 references/ 细则与 assets/ 官方素材：https://github.com/15011219788-afk/nexai-brand-ui-skill）
接下来为奈势AI做的所有设计、PPT、社媒图、网页和文案，都严格按它执行：色彩只用官方色（主色奈势紫 #6857E7，悬停 #5F4AD4，按下 #5743B7），界面引用 tokens.css 的语义层 --nx-color-*，字体用 MiSans，网页标题字重 600，Logo 和小奈只用官方文件、不变形不改色不重画，遵守全部禁用规则。破坏性/强调按钮用珊瑚橙 #FF604A 配墨黑字，不要用白字。白底不用珊瑚橙做文字（≥48px 品牌大字用独立定值 #E5503A）。
交付前按 SKILL.md 的触点清单逐项自检，并告诉我哪些地方是你新增或假设的。
拿不准时，以品牌规范官网 https://brand.nexai.link 和组件库 https://brand.nexai.link/components.html 为准，素材从官网下载页获取。
```

## 安装为本地 Skill

```bash
git clone https://github.com/15011219788-afk/nexai-brand-ui-skill.git

# Cursor（项目级；也可放到用户目录下的 .cursor/skills/）
mkdir -p .cursor/skills && cp -r nexai-brand-ui-skill .cursor/skills/naishi-brand

# Claude Code（项目级；也可放到用户目录下的 .claude/skills/）
mkdir -p .claude/skills && cp -r nexai-brand-ui-skill .claude/skills/naishi-brand
```

其他 Agent（ChatGPT、Codex、Gemini、Coze 等）：不用安装，把上面那段话或 raw SKILL.md 链接发给它即可；需要素材时让它按 `https://raw.githubusercontent.com/15011219788-afk/nexai-brand-ui-skill/main/<路径>` 读取。

安装后，在任务里说「按奈势品牌规范 / 使用 naishi-brand skill」即可触发。

使用 Meta Astryx（React 19）的项目：把 `assets/theme/nexai-theme-nexai-1.3.2.tgz` 装进项目，再用 `<Theme theme={nexaiTheme}>` 包住应用。说明见 `references/14-tokens-v1.3.md`。

## 目录

| 路径 | 内容 |
|---|---|
| `SKILL.md` | 入口：固定信息、执行步骤、硬规则、各触点自检清单、停下来问的情况 |
| `references/01–13` | 细则：基础、Logo、色彩、字体、图形与图片、小奈、数字产品、社媒、PPT、印刷与物料、活动、办公、治理 |
| `references/14-tokens-v1.3.md` | v1.3 三层 token、深色模式、关键语义色、Astryx 主题包用法 |
| `references/spec-v1.3.md` | v1.3.2 完整规范（设计同步稿） |
| `references/astryx-mapping.md` | Astryx 核心 token 映射 |
| `references/contrast-report.md` | WCAG 对比度报告 |
| `references/changelog.md` | 版本变更、待确认清单与资料缺口 |
| `assets/logo/` | 官方 Logo SVG（全部版本）与常用 PNG（600 / 1200w） |
| `assets/color/`、`assets/tokens/` | 色板与设计 token（CSS / JSON；默认与 `tokens-v1.3.2.*` 相同，另归档 `tokens-v1.2.*`） |
| `assets/theme/` | Astryx 主题包 `nexai-theme-nexai-1.3.2.tgz` |
| `assets/android/` | 安卓颜色资源 zip（values / values-night） |
| `assets/mascot/` | 小奈标准形象、圆形头像、12 枚表情、12 枚动态表情 GIF、8 个动作 |
| `assets/photo/`、`assets/social/` | 图片处理与社媒模板 |

为保持仓库轻量，PPT 模板、PDF 手册、2400w 大图、480 高清动态表情和微信投稿包不放在仓库里，请到 https://brand.nexai.link/downloads.html 下载。

## 版本

- v1.3.2（2026-11-12）：危险/强调按钮统一为珊瑚橙 #FF604A 配墨黑字（5.06:1）；悬停 #FA5B46（4.79:1）、按下 #F75742（4.60:1）。组件库并入品牌规范网站 https://brand.nexai.link/components.html。白底品牌大字（≥48px）可用独立定值 #E5503A（3.79:1），不是色阶档。
- v1.3.1（2026-11-12）：深色错误 Toast 底改为 #B42318，配 #F6F6F8 字（6.09:1）；深色 error 强填充 #E8705F 配墨黑（4.98:1）；深色错误文字和图标用 #F78676。
- v1.3.0（2026-11-12）：语义 token 三层、深色模式（`[data-theme=dark]` + `prefers-color-scheme`）、主按钮悬停 #5F4AD4 / 按下 #5743B7、深色中性背景 #262626、网页标题字重 600、Astryx 主题包 theme-nexai。品牌原色、Logo、MiSans 与 v1.2 相同。
- v1.2（2026-11）：品牌色以奈势紫 #6857E7 为主色、珊瑚橙 #FF604A 为点缀；字体统一 MiSans；新增小奈表情、动态表情、延展动作与各触点清单。
- v1.0.0（2026-07，NexAI Brand UI，旧色值 #7417FF / #FE6702）已废弃，仅保留在 git 历史（commit `9019e91`）中，请勿再使用。
