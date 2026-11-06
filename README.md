# 奈势AI 品牌规范 Skill（naishi-brand v1.2）

把《奈势AI 品牌规范 v1.2》整理成 AI 助手 / Agent 可以直接执行的技能包：一份主文件 + 8 份分章细则 + 官方素材（Logo、小奈、Token、社媒模板）。

- 规范官网：<https://brand.nexai.link>
- 适用对象：Cursor / Claude Code / ChatGPT / Codex / WorkBuddy / 扣子 等支持 Skill 的助手

## 怎么用

**方式一：放进技能目录**（推荐）

```bash
git clone https://github.com/15011219788-afk/nexai-brand-ui-skill.git ~/.claude/skills/naishi-brand
# 或复制到你的 Agent 技能目录，例如 ~/.workbuddy/skills/naishi-brand
```

**方式二：直接加进对话**

> 请先完整阅读奈势AI品牌规范 Skill：https://raw.githubusercontent.com/15011219788-afk/nexai-brand-ui-skill/main/SKILL.md
> 接下来为奈势AI做的所有设计、文案、PPT、社媒图和网页，都严格按它执行；动手前按需读 references/，交付前用第 6 节清单自检。

## 目录

```
SKILL.md                 主文件：10 条硬规则、固定信息、五步工作流、自检清单
references/
  01-brand.md            品牌理念 · 命名 · 语气 · 定位
  02-logo.md             Logo 版本 · 安全空间 · 尺寸 · 背景 · 误用
  03-color.md            色值 · 比例 · 对比度 · 印刷
  04-typography.md       MiSans 授权与字体栈 · 字号层级 · 排版
  05-mascot.md           小奈形象 · 头像 · 12 表情 · 8 动作 · 不压字
  06-applications.md     网站 / App / 小程序 / 社媒 / 视频 / PPT / 印刷 / 活动 / 办公
  07-dont.md             全量禁用清单（含 v1.2 停用项）
  08-governance.md       审批分级 · 命名 · FAQ · 版本记录
assets/
  logo/                  SVG（首选）+ PNG，横竖版与图形标的彩 / 反白 / 全白 / 黑
  mascot/                标准形象、新版圆形与方形头像、12 静态表情、12 动态 GIF、8 动作
  tokens/                tokens.css / tokens.json（颜色、圆角、间距、阴影、动效）
  color/                 ASE / GPL / JSON 色板（9 个品牌色）
  social/                各平台 HTML 模板（改字后按 meta size 截图导出）
  photo/                 示例平静场景图
```

## 三条底线

1. **只用官方素材**——Logo 不重绘、小奈不重画、素材不截图；
2. **只用官方色与 MiSans**——#6857E7 主色、#FF604A 唯一强调色、渐变只在 Logo 里；
3. **小奈与文字永不重叠**——先分区，再排版。

## 不随仓库分发的大件

PPT 模板、PDF 手册、完整素材包、表情包 ZIP、2400w Logo 请从 <https://brand.nexai.link/downloads.html> 下载。

## 版本

v1.2（2026-11-02）。旧版 v1.1 / v1.0 的字体方案、旧版裁切头像与像素辅助图形均已停用。
