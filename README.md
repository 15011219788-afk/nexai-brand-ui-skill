# 奈势AI 品牌规范 Skill（v1.2）

> NexAI (奈势AI) brand guidelines packaged as an Agent Skill — colours, MiSans type, logo, mascot 小奈 and do/don't rules for any AI agent doing design work.

把《奈势AI 品牌规范 v1.2》压缩成 AI Agent 可直接执行的规则 + 官方素材。让 Cursor、Claude Code 或任意 Agent 做海报、PPT、社媒图、网页 / 产品界面、文案时，自动遵守奈势的色彩、字体、Logo、小奈与禁用规则，并在交付前按清单自检。

- 可视化规范官网：**https://brand.nexai.link**
- 大文件下载（PPT 模板、PDF 手册、完整素材包、表情包、微信表情投稿包）：https://brand.nexai.link/downloads.html
- Skill 入口（raw）：https://raw.githubusercontent.com/15011219788-afk/nexai-brand-ui-skill/main/SKILL.md

## 最快用法：复制这段话发给你的 Agent

```text
请先完整阅读奈势AI品牌规范 Skill：https://raw.githubusercontent.com/15011219788-afk/nexai-brand-ui-skill/main/SKILL.md
（完整仓库含 references/ 细则与 assets/ 官方素材：https://github.com/15011219788-afk/nexai-brand-ui-skill）
接下来为奈势AI做的所有设计、PPT、社媒图、网页和文案，都严格按它执行：色彩只用官方色（主色奈势紫 #6857E7），字体用 MiSans，Logo 和小奈只用官方文件、不变形不改色不重画，遵守全部禁用规则。
交付前按 SKILL.md 的触点清单逐项自检，并告诉我哪些地方是你新增或假设的。
拿不准时，以品牌规范官网 https://brand.nexai.link 为准，素材从官网下载页获取。
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

## 目录

| 路径 | 内容 |
|---|---|
| `SKILL.md` | 入口：固定信息、执行步骤、硬规则、各触点自检清单、停下来问的情况 |
| `references/01–13` | 细则：基础、Logo、色彩、字体、图形与图片、小奈、数字产品、社媒、PPT、印刷与物料、动效、文案、治理；`changelog.md` 为版本变更 |
| `assets/logo/` | 官方 Logo SVG（全部版本）与常用 PNG（600 / 1200w） |
| `assets/color/`、`assets/tokens/` | 色板与设计 token（CSS / JSON） |
| `assets/mascot/` | 小奈标准形象、圆形头像、12 枚表情、12 枚动态表情 GIF、8 个动作 |
| `assets/photo/`、`assets/social/` | 图片处理与社媒模板 |

为保持仓库轻量，PPT 模板、PDF 手册、2400w 大图、480 高清动态表情和微信投稿包不放在仓库里，请到 https://brand.nexai.link/downloads.html 下载。

## 版本

- v1.2（2026-11）：品牌色以奈势紫 #6857E7 为主色、珊瑚橙 #FF604A 为点缀；字体统一 MiSans；新增小奈表情、动态表情、延展动作与各触点清单。
- v1.0.0（2026-07，NexAI Brand UI，旧色值 #7417FF / #FE6702）已废弃，仅保留在 git 历史（commit `9019e91`）中，请勿再使用。
