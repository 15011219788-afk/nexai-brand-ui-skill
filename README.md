# NexAI Brand UI Skill

面向产品经理、UI / 产品设计师与前端工程师的 NexAI 产品设计系统包。

## 使用方法

1. 将整个 `nexai-brand-ui-skill` 目录复制到团队所使用的 Agent Skills 目录中。
2. 保持目录名、`SKILL.md`、`references/`、`templates/` 与 `assets/` 的相对关系不变。
3. 在任务中直接说明“使用 nexai-brand-ui skill”，并提供目标页面、用户目标和现有代码路径。
4. 产品立项先填写 `templates/screen-brief.md`；设计与开发按 `SKILL.md` 的 Required reading 路由读取对应参考。
5. 交付前逐项执行 `references/qa-checklist.md`。

## 推荐提示词

```text
使用 nexai-brand-ui skill，基于现有 NexAI 产品设计系统，为【目标用户】设计/实现【页面或功能】。
用户核心目标是【目标】，主要交付物是【成果】，需要沉淀的证据是【证据】，主要行动是【CTA】。
请保留现有路由、品牌资产、内容信任边界和响应式规则，最后按 QA 清单验收。
```

## 文件说明

- `SKILL.md`：Agent 执行入口与硬性约束。
- `NexAI-品牌UI规范.html`：团队浏览版规范。
- `references/`：详细设计、内容与验收规则。
- `templates/screen-brief.md`：跨角色需求模板。
- `assets/`：官方 Logo 与代表性页面截图。

## 版本

- Version: 1.0.0
- Baseline: 当前 `codex-奈势产品001号/prototype` 产品语言
- Updated: 2026-07-29

