# Excellent Typesetter

把 Markdown 转换为多平台兼容的排版 HTML，支持 7 个发布平台。一个通用 AI Agent Skill，兼容 Claude Code、Codex、Gemini CLI 等任何能读取 prompt 文件的 Agent。

[English](README.md)

---

## 为什么需要它

你用 Markdown 写了一篇文章，要发微信公众号。微信会剥离 `<style>` 标签、外部链接不可点击、列表样式被重置、纯黑色 `#000000` 被吞掉。发 Medium，只支持两级标题，代码块没有语法高亮。发 LinkedIn，大部分 CSS 直接被干掉。

每个平台都有自己的渲染引擎、自己的限制、自己的绕法。Excellent Typesetter 把这些全部编码好了 — 14 条微信规则、Medium 的样式覆盖、LinkedIn 的激进剥离 — Markdown 写一次，HTML 对哪个平台都是对的。

---

## 快速开始

```bash
# 1. 克隆
git clone https://github.com/d-wwei/excellent-typesetter.git

# 2. 加载到 Agent（以 Claude Code 为例）
ln -s /path/to/excellent-typesetter ~/.claude/skills/typeset

# 3. 排版
/typeset 文章.md --platform wechat --theme minimal

# 4. 浏览器打开输出的 HTML，Cmd+A 全选，Cmd+C 复制，粘贴到平台编辑器
```

---

## 核心能力

- **7 个平台一键排版** — 微信公众号、知乎、掘金、Medium、LinkedIn、X Articles、通用博客。每个平台有独立的渲染配置：CSS 约束、链接处理、代码块格式、表格支持。

- **9 个内置主题** — minimal（默认）、default、elegant、tech、vibrant、dark、notion、newspaper、gradient。打开 `themes/preview.html` 可以并排对比所有主题。

- **任意文档格式输入** — 直接读 Markdown，也支持 PDF、DOCX、PPTX、XLSX、HTML、CSV、图片（OCR）、音频（转录）等，通过 [MarkItDown](https://github.com/microsoft/markitdown) 自动预处理。

- **代码语法高亮** — 3 套代码主题（GitHub Light、One Dark、Kimbie Light），逐 token 内联着色。不依赖 JavaScript — 微信里也能正常渲染。

- **去 AI 味** — 可选 `--humanize` 标志，检测并重写 5 大类 AI 写作模式。三个强度可选。

- **链接自动脚注化** — 微信平台上，外部链接自动转为编号引用 + 文末参考文献区。其他平台保留可点击链接。

---

## 使用方式

```
/typeset <文件路径或文本> [--platform wechat|zhihu|juejin|medium|linkedin|x|blog] [--theme <主题名>] [--humanize] [--code-theme github|one-dark|kimbie]
```

默认值：`--platform wechat`，`--theme minimal`，`--code-theme github`。

---

## 平台支持

| 平台 | 参数 | 链接 | 代码块 | 表格 | 核心约束 |
|------|------|------|--------|------|----------|
| 微信公众号 | `wechat` | 转脚注（禁 `<a>`） | `<section>` + span | 滚动容器 | 全内联 CSS，禁 `<pre>`，禁 `#000` |
| 知乎 | `zhihu` | 保留 | `<pre><code>` | 正常 | 内联 CSS |
| 掘金 | `juejin` | 保留 | `<pre><code>` | 正常 | 内联 CSS |
| Medium | `medium` | 保留 | `<pre>`（无高亮） | 不支持 | Medium 覆盖样式，仅 H1+H2 |
| LinkedIn | `linkedin` | 保留 | 不支持 | 不支持 | 大部分 CSS 被剥离，图片需手动上传 |
| X Articles | `x` | 保留 | `<pre><code>` | 有限 | 需 X Premium |
| 博客 | `blog` | 保留 | `<pre><code>` + highlight.js | 正常 | 完整 HTML 文档，支持 `<style>` 标签 |

---

## 主题

| 主题 | 风格 | 适用场景 |
|------|------|----------|
| `minimal` | 极简排版，大量留白（**默认**） | 通用文章、短文 |
| `default` | 专业蓝，竖条标题装饰 | 正式报告、技术文章 |
| `elegant` | 暖色衬线，深色徽章标题 | 人文/商业/叙事 |
| `tech` | 冷青色调，深色代码块 (One Dark) | 技术教程 |
| `vibrant` | 活力绿，黑底标签标题 | 品牌文/营销 |
| `dark` | 深色背景，护眼沉浸 | 技术社区、夜间阅读 |
| `notion` | Notion 风格，干净利落 | 知识库、内部文档 |
| `newspaper` | 报纸印刷，衬线经典 | 深度报道、长文评论 |
| `gradient` | 现代渐变，视觉冲击 | 产品发布、发布会风格 |

主题预览：浏览器打开 `themes/preview.html`。

自定义主题：在 `themes/` 目录下按相同格式创建 `.md` 文件。

---

## 主题架构

4 层结构（源自 mdnice）：

| 层 | 作用 |
|---|------|
| **基础层** | 容器、排版基础（所有主题共享） |
| **内容层** | 标题、段落、列表、引用 — 视觉风格 |
| **代码层** | 语法高亮（通过 `--code-theme` 独立切换） |
| **字体层** | 字体族覆盖（可选） |

---

## 安装

**前置条件：**
- 任何 AI Agent（Claude Code、Codex、Gemini CLI、OpenCode 等）
- Python 3.12+ 和 [MarkItDown](https://github.com/microsoft/markitdown)（可选，用于非 Markdown 输入）

```bash
git clone https://github.com/d-wwei/excellent-typesetter.git

# 可选：安装 MarkItDown 支持 PDF/DOCX/PPTX
pipx install 'markitdown[all]' --python python3.12
```

**各 Agent 配置方式：**

| Agent | 配置 |
|-------|------|
| Claude Code | `ln -s /path/to/excellent-typesetter ~/.claude/skills/typeset` — 自动注册为 `/typeset` |
| Codex | 复制到项目根目录或在 `AGENTS.md` 中引用 |
| Gemini CLI | 在 `GEMINI.md` 中引用 `SKILL.md` |
| 其他 Agent | 将 `SKILL.md` 作为 system prompt 或 context 文件加载 |

---

## 文件结构

```
excellent-typesetter/
├── SKILL.md                      # Skill 定义：工作流、路由、默认值
├── references/
│   ├── platform-rules.md         # 各平台渲染约束
│   ├── element-specs.md          # HTML 元素模板 + 主题变量
│   ├── code-themes.md            # 语法高亮色表
│   └── humanizer.md              # AI 模式检测与重写规则
├── themes/
│   ├── minimal.md                # 默认主题
│   ├── default.md
│   ├── elegant.md
│   ├── tech.md
│   ├── vibrant.md
│   ├── dark.md
│   ├── notion.md
│   ├── newspaper.md
│   ├── gradient.md
│   └── preview.html              # 主题并排对比
├── README.md                     # English
├── README_ZH.md                  # 中文（本文件）
└── remix-provenance.md           # 来源归属与审计记录
```

Reference 文件在排版时按需加载，不会预加载到 Agent 上下文。

---

## 来源

通过 [Remix](https://github.com/d-wwei/remix) 方法论构建。来源项目：

| 来源 | 贡献 |
|------|------|
| mdnice/markdown-nice | 四层主题架构、标题 prefix/content/suffix 装饰、WeChat CSS |
| baoyu-markdown-to-html | Callout/脚注/代码高亮扩展、CJK 空格处理 |
| lyricat/wechat-format | 渲染时生成内联样式、列表兼容、亚像素边框 |
| geekjourneyx/md2wechat-skill | 人性化模块（24 模式/5 大类） |
| kepano/obsidian-skills | Callout 分类法（13 类型） |
| microsoft/markitdown | 多格式输入预处理（16+ 格式） |

---

## 许可

MIT
