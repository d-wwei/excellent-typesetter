# Excellent Typesetter

Converts Markdown to platform-compatible HTML for 7 publishing platforms. An AI agent skill — works with Claude Code, Codex, Gemini CLI, or any agent that reads prompt files.

[中文文档](README_ZH.md)

---

## Why

You wrote an article in Markdown. WeChat strips `<style>` tags, kills external links, resets list styles, and swallows `#000000` colors. Medium only supports two heading levels and ignores your syntax highlighting. LinkedIn strips most CSS entirely.

Each platform has its own rendering engine, its own broken behaviors, its own workarounds. Excellent Typesetter encodes all of them — 14 WeChat rules, Medium's style overrides, LinkedIn's aggressive stripping — so you write Markdown once and get correct HTML for any target.

---

## Quick Start

```bash
# 1. Clone
git clone https://github.com/d-wwei/excellent-typesetter.git

# 2. Load into your agent (Claude Code example)
ln -s /path/to/excellent-typesetter ~/.claude/skills/typeset

# 3. Typeset
/typeset article.md --platform wechat --theme minimal

# 4. Open the output HTML in a browser, Cmd+A, Cmd+C, paste into the platform editor
```

---

## What You Can Do

- **Typeset for 7 platforms** — WeChat, Zhihu, Juejin, Medium, LinkedIn, X Articles, and generic blog. Each has its own rendering profile: CSS constraints, link handling, code block format, table support.

- **Choose from 9 built-in themes** — minimal (default), default, elegant, tech, vibrant, dark, notion, newspaper, gradient. Open `themes/preview.html` to compare them side by side.

- **Feed it any document format** — Markdown directly, or PDF, DOCX, PPTX, XLSX, HTML, CSV, images (OCR), audio (transcription), and more via [MarkItDown](https://github.com/microsoft/markitdown) preprocessing.

- **Get syntax-highlighted code blocks everywhere** — 3 code themes (GitHub Light, One Dark, Kimbie Light) with per-token inline coloring. No JavaScript — works in WeChat's restricted environment.

- **Remove AI writing patterns** — Optional `--humanize` flag detects and rewrites AI-typical phrasing across 5 categories. Three intensity levels.

- **Auto-convert links to footnotes** — On WeChat, external links become numbered references with a bibliography section. Other platforms keep clickable links.

---

## Usage

```
/typeset <file-or-text> [--platform wechat|zhihu|juejin|medium|linkedin|x|blog] [--theme <name>] [--humanize] [--code-theme github|one-dark|kimbie]
```

Defaults: `--platform wechat`, `--theme minimal`, `--code-theme github`.

---

## Platforms

| Platform | Flag | Links | Code Blocks | Tables | Key Constraint |
|----------|------|-------|-------------|--------|----------------|
| WeChat | `wechat` | Footnotes (no `<a>`) | `<section>` + spans | Scroll container | All CSS inline, no `<pre>`, no `#000` |
| Zhihu | `zhihu` | Preserved | `<pre><code>` | Standard | Inline CSS |
| Juejin | `juejin` | Preserved | `<pre><code>` | Standard | Inline CSS |
| Medium | `medium` | Preserved | `<pre>` (no highlighting) | Not supported | Medium overrides styles, H1+H2 only |
| LinkedIn | `linkedin` | Preserved | Not supported | Not supported | Most CSS stripped, images need manual upload |
| X Articles | `x` | Preserved | `<pre><code>` | Limited | X Premium required |
| Blog | `blog` | Preserved | `<pre><code>` + highlight.js | Standard | Full HTML document with `<style>` tags |

---

## Themes

| Theme | Style | Best For |
|-------|-------|---------|
| `minimal` | Swiss typography, maximum whitespace (**default**) | General articles, short-form |
| `default` | Professional blue, vertical bar headings | Formal reports, tech articles |
| `elegant` | Warm serif, dark badge headings | Essays, business writing |
| `tech` | Cool teal, dark code blocks (One Dark) | Technical tutorials |
| `vibrant` | Green energy, black label headings | Brand content, marketing |
| `dark` | Dark background, eye-friendly | Tech communities, night reading |
| `notion` | Notion-style, clean and functional | Knowledge bases, internal docs |
| `newspaper` | Classic print, serif typography | Long-form journalism, deep analysis |
| `gradient` | Modern gradients, visual impact | Product launches, keynote style |

Preview all themes: open `themes/preview.html` in your browser.

Custom themes: create a `.md` file in `themes/` following the same format as existing themes.

---

## Theme Architecture

4-layer system (adapted from mdnice):

| Layer | Role |
|-------|------|
| **Base** | Container, typography fundamentals (shared across all themes) |
| **Content** | Headings, paragraphs, lists, blockquotes — visual identity |
| **Code** | Syntax highlighting (swappable independently via `--code-theme`) |
| **Font** | Font family overrides (optional) |

---

## Installation

**Prerequisites:**
- Any AI agent (Claude Code, Codex, Gemini CLI, OpenCode, etc.)
- Python 3.12+ with [MarkItDown](https://github.com/microsoft/markitdown) (optional, for non-Markdown input)

```bash
git clone https://github.com/d-wwei/excellent-typesetter.git

# Optional: install MarkItDown for PDF/DOCX/PPTX support
pipx install 'markitdown[all]' --python python3.12
```

**Per-agent setup:**

| Agent | Setup |
|-------|-------|
| Claude Code | `ln -s /path/to/excellent-typesetter ~/.claude/skills/typeset` — registers as `/typeset` |
| Codex | Copy to project root or reference in `AGENTS.md` |
| Gemini CLI | Reference `SKILL.md` in `GEMINI.md` |
| Other agents | Load `SKILL.md` as system prompt or context file |

---

## File Structure

```
excellent-typesetter/
├── SKILL.md                      # Skill definition: workflow, routing, defaults
├── references/
│   ├── platform-rules.md         # Per-platform rendering constraints
│   ├── element-specs.md          # HTML element templates with theme variables
│   ├── code-themes.md            # Syntax highlighting color tables
│   └── humanizer.md              # AI pattern detection and rewriting rules
├── themes/
│   ├── minimal.md                # Default theme
│   ├── default.md
│   ├── elegant.md
│   ├── tech.md
│   ├── vibrant.md
│   ├── dark.md
│   ├── notion.md
│   ├── newspaper.md
│   ├── gradient.md
│   └── preview.html              # Side-by-side theme comparison
├── README.md                     # English (this file)
├── README_ZH.md                  # 中文
└── remix-provenance.md           # Source attribution and remix audit trail
```

Reference files are loaded on demand during typesetting, not preloaded into agent context.

---

## Provenance

Built using the [Remix](https://github.com/d-wwei/remix) methodology. Sources:

| Source | Contribution |
|--------|-------------|
| mdnice/markdown-nice | 4-layer theme architecture, heading prefix/content/suffix decoration, WeChat CSS |
| baoyu-markdown-to-html | Callout/footnote/code highlighting extensions, CJK spacing |
| lyricat/wechat-format | Inline style generation, list compatibility, sub-pixel borders |
| geekjourneyx/md2wechat-skill | Humanizer module (24 patterns, 5 categories) |
| kepano/obsidian-skills | Callout taxonomy (13 types) |
| microsoft/markitdown | Multi-format input preprocessing (16+ formats) |

---

## License

MIT
