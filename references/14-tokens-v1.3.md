# 14 设计 Token v1.3.2

界面色值、字号、间距、圆角、阴影与动效以 `assets/tokens/tokens.json`（v1.3.2）为唯一数据源。`tokens.css` 与 Astryx 主题包、安卓颜色资源都由它生成。完整表格见 `spec-v1.3.md`，对比度见 `contrast-report.md`，Astryx 对照见 `astryx-mapping.md`。

## 三层

1. **原始色** `--nx-*`：v1.2 品牌原值，不改。奈势紫 `#6857E7`、深紫 `#3C237C`、薰衣草 `#BBBBFE`、雾紫 `#F1F0FD`、珊瑚橙 `#FF604A`、墨黑 `#262626`、中灰 `#6E6E73`、浅灰 `#F6F6F8`、白 `#FFFFFF`，以及仅限界面状态的成功 / 警示 / 危险。
2. **色阶** `--nx-<色系>-<stop>`：Astryx `astryx-oklch-v1` 生成，深色模式用 `--nx-<色系>-dk-<stop>`。组件不要直接取色阶，除非规范写明（例如主按钮悬停 `purple-40`）。
3. **语义色** `--nx-color-*`：组件只使用这一层。浅色写在 `:root`，深色写在 `[data-theme="dark"]` 与系统深色偏好中。

v1.2 的旧变量名（`--nx-purple-hover`、`--nx-orange`、`--nx-dark-navy` 等）全部保留为兼容别名，新代码不要再用。

## 深色模式

- 同时支持 `<html data-theme="dark">` 和 `prefers-color-scheme: dark`。
- `data-theme="light"` 固定浅色；不写 `data-theme` 时跟随系统。
- 品牌站开关把选择存在 `localStorage` 键 `nx-theme`。为避免闪白，在首屏绘制前用头部脚本读取并写到 `data-theme`。
- 深色页面底是中性墨黑 `#262626`，卡片 `#313030`，浮层略浅；主按钮仍是奈势紫配白字。不要用紫底做页面背景。

## 关键语义色（浅 / 深）

| 用途 | Token | 浅色 | 深色 |
|---|---|---|---|
| 主按钮 | `--nx-color-accent` | #6857E7 | #6857E7 |
| 主按钮悬停 | `--nx-color-accent-hover` | #5F4AD4 | #5F4AD4 |
| 主按钮按下 | `--nx-color-accent-pressed` | #5743B7 | #5742B8（深色色阶 purple-dk-35） |
| 主按钮文字 | `--nx-color-on-accent` | #FFFFFF | #FFFFFF |
| 破坏性/强调按钮 | `--nx-color-button-danger` | #FF604A | #FF604A |
| 其上文字 | `--nx-color-on-button-danger` | #262626（5.06:1） | 同左 |
| 强调按钮悬停 | `--nx-color-button-danger-hover` | #FA5B46（墨黑 4.79:1） | 同左 |
| 强调按钮按下 | `--nx-color-button-danger-pressed` | #F75742（墨黑 4.60:1） | 同左 |
| 错误 Toast 底 | `--nx-color-background-error-inverted` | #B42318 | #B42318（配 #F6F6F8 字，6.09:1） |
| 错误文字/图标 | `--nx-color-text-error` / `--nx-color-icon-error` | #B42318 | #F78676 |
| error 强填充 | `--nx-color-error` | #B42318 | #E8705F（配墨黑 4.98:1；不作强调按钮） |

破坏性/强调按钮是本地 token，不改全局 `--color-error`，以免影响 Toast 与状态色。白字在珊瑚橙上只有 2.98:1，禁止。

## 独立定值 #E5503A（不进色阶）

白底不用 `#FF604A` 做文字。唯一例外：品牌大字（≥48px，如品牌理念页「Create」）用 **#E5503A**（对白 3.79:1）。它不是 ramp 档，不写入 `tokens.json` 的 palette / primitive；色块、图形、按钮仍用 `#FF604A`。

## 对比度门槛

WCAG 2.x 相对亮度，对比度**向下取两位小数**（4.497 记 4.49，不四舍五入）。正文 ≥4.5；大字（中文 ≥24px 常规或 ≥19px 粗体）与图标、控件边界 ≥3；小于 3 只能做装饰，不能单独承载信息。完整报告见 `contrast-report.md`。

## Astryx 主题包

包名 `@nexai/theme-nexai`，当前版本 1.3.2，对齐 `meta/astryx@4705e676`、`@astryxdesign/core` 0.7.15（Beta，需 React 19）。本包不发布到 npm，用 tarball 安装：

```bash
pnpm add ./nexai-theme-nexai-1.3.2.tgz @astryxdesign/core@0.7.15
```

文件在 `assets/theme/nexai-theme-nexai-1.3.2.tgz`，也可从 https://brand.nexai.link/downloads.html 下载。

```tsx
import {Theme} from '@astryxdesign/core/theme';
import {nexaiTheme} from '@nexai/theme-nexai/built';
import '@nexai/theme-nexai/theme.css';

<Theme theme={nexaiTheme} mode="system">  {/* 'system' | 'light' | 'dark' */}
  <App />
</Theme>
```

破坏性/强调按钮走 `button['variant:destructive']`（IconButton 同款）。字体要自己加载：Astryx 只设置 `--font-family-*`，MiSans 从 https://hyperos.mi.com/font 下载后用 `@font-face` 自托管。

不用 React 的项目直接引用 `tokens.css`，并用 `data-theme` 切换深浅色。命名规则：`--nx-X` 去掉 `nx-` 就是 Astryx 的 `--X`。未映射的 32 个多色分类色继承 Astryx 默认值。

## 安卓

`assets/android/nexai-android-colors-v1.3.2.zip` 提供 `res/values/colors_nexai.xml` 与 `values-night/`。代码里只用 `nx_color_*` 语义色。

## 组件对照

品牌规范网站组件库：https://brand.nexai.link/components.html（第 7 章，排在「应用规范」之后；旧地址 `/ui/` 会跳转过来）。
