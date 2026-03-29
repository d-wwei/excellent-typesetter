# Remix Provenance — Typeset Skill v1.0.0

Generated: 2026-03-28
Method: Remix v0.2.0 (agent-driven synthesis)
Profile: skill

---

## Brief

- **Target**: 全能编辑器排版 Skill — 将 Markdown 转换为多平台兼容的精美排版 HTML
- **Target Job**: 融合 6+ 个最佳排版方案，创建最强编辑器排版 Skill
- **Success Criteria**:
  1. 支持微信/知乎/掘金/博客四大平台
  2. 内置 5+ 高质量主题
  3. 完整 WeChat 兼容性（编译自所有已知技巧）
  4. 代码高亮 + Callout + 脚注等技术特性
  5. 可选人性化（去 AI 味）处理
  6. 无外部 API 依赖（核心渲染）
  7. 自包含、可复用的 Claude Code Skill

---

## Sources Analyzed

### Source 1: md2wechat-skill (geekjourneyx)
- **版本**: v2.0.5 (2026-03-26)
- **语言**: Go CLI
- **评分**: 渲染 7 | 平台 6 | 主题 7 | 技术 5 | CJK 8 | 反AI 10 | 发布 10
- **关键贡献**: Humanizer (24 模式, 5 维评分, 3 强度), 图片 Provider 抽象, Writer 风格引擎
- **局限**: 主题系统薄（YAML 元数据指针，非完整 CSS），依赖 md2wechat.cn API 或 AI 模式

### Source 2: baoyu-markdown-to-html (jimliu)
- **版本**: 基于 marked v15.0.6
- **语言**: TypeScript/Bun
- **评分**: 渲染 9 | 平台 7 | 主题 8 | 技术 10 | CJK 9 | 反AI 0 | 发布 3
- **关键贡献**: 10 个 marked 扩展 (alerts, footnotes, ruby, TOC, PlantUML, KaTeX, slider), CJK 预处理, 73 代码主题, CSS 内联管道 (juice)
- **局限**: 需 Bun 运行时，数学渲染需浏览器环境

### Source 3: wechat-article-formatter-skill (iamzifei)
- **版本**: MIT
- **语言**: SKILL.md + CSS
- **评分**: 渲染 7 | 平台 6 | 主题 5 | 技术 3 | CJK 7 | 反AI 0 | 发布 10
- **关键贡献**: 完整微信发布管道 (Token/Upload/Draft), bm.md API 参考, 实战坑位总结
- **局限**: 依赖 bm.md 外部渲染服务, 单一 CSS 风格

### Source 4: mdnice/markdown-nice
- **版本**: 4.6k stars
- **语言**: React + MobX + markdown-it + juice
- **评分**: 渲染 10 | 平台 9 | 主题 10 | 技术 8 | CJK 9 | 反AI 0 | 发布 2
- **关键贡献**: 四层可组合 CSS 架构, 标题三段式 span (prefix/content/suffix), 10+ WeChat 技巧 (禁 #000, li>section, 去 pre, 链接脚注化, 表格滚动, 图片流), 多平台输出 (微信/知乎/掘金), 社区主题生态
- **局限**: Web 应用非 Skill, 需二次封装

### Source 5: lyricat/wechat-format
- **版本**: 4.5k stars (已停止维护)
- **语言**: Vue.js + marked.js
- **评分**: 渲染 7 | 平台 7 | 主题 3 | 技术 3 | CJK 7 | 反AI 0 | 发布 0
- **关键贡献**: 渲染时直接生成内联样式 (最可靠), 列表自定义字符方案, 代码块 section+ul 方案, transform:scale(0.5) 亚像素技巧, 微信域内链接保留
- **局限**: 仅 2 个主题, 功能简单, 已停维护

### Source 6: obsidian-markdown (kepano)
- **版本**: 17.6k stars
- **语言**: SKILL.md
- **评分**: 格式标准 9 | 扩展性 8
- **关键贡献**: Callout 分类法 (13 类型 + 别名), Frontmatter 元数据规范, Wikilink/Embed 语法, ==高亮== 和 %%注释%% 语法
- **局限**: Obsidian 专用，非排版工具

### Source 7: MarkItDown (Microsoft)
- **版本**: 92.7k stars
- **语言**: Python
- **评分**: 输入覆盖 10 | 质量 6
- **关键贡献**: 23 种格式转 Markdown, 优先级分发器, 输出规范化
- **局限**: 面向 LLM 消费，非排版

---

## Synthesis Strategy

**Balanced (全管道融合)** — 取每个源的最强维度，组装为完整排版管道：

| 管道阶段 | 主要来源 | 具体贡献 |
|---|---|---|
| 主题架构 | mdnice | 四层可组合 (基础/内容/代码/字体) |
| 渲染可靠性 | wechat-format | 渲染时直接内联样式 |
| WeChat 兼容 | mdnice + wechat-format | 14 条编译规则 (全量) |
| 技术特性 | baoyu | Callout/脚注/代码高亮/CJK |
| Callout 标准 | obsidian | 13 类型分类法 |
| 反 AI 处理 | md2wechat | 24 模式/5 维评分/3 强度 |
| 发布参考 | formatter | 微信 API 管道 + 实战坑位 |
| 代码高亮 | baoyu + 自研 | 3 内置主题, token 分类规则 |

**被拒绝的策略**:
- **Conservative (仅渲染)**: 跳过人性化和发布，不够 "最好的"
- **Forward-Port (纯 Skill 无依赖)**: 技术特性受限太多

---

## Decision Log

| 决策 | 选择 | 原因 |
|---|---|---|
| 渲染方式 | 渲染时内联 (wechat-format) | 比后处理内联 (mdnice/juice) 更可靠，且无运行时依赖 |
| 主题定义格式 | 结构化 Markdown | Claude 可直接读取和应用，无需 JSON/YAML 解析 |
| 代码高亮 | 内联 color 着色 | 微信不支持 JS，必须静态着色 |
| Callout 语法 | GFM + Obsidian 双支持 | 覆盖最广用户群 |
| 公式处理 | 降级方案 | Claude 无法运行 KaTeX/MathJax，给出替代策略 |
| Mermaid/PlantUML | 标注 + 替代 | 同上原因 |
| 人性化 | 可选模块 | 不是所有用户都需要，保持灵活 |
| 微信发布 | 仅参考，不内置 | 需要 API 密钥和 IP 白名单，超出排版 Skill 范畴 |

---

## Risk Register

| 风险 | 级别 | 缓解 |
|---|---|---|
| 主题样式值过多，Claude 可能遗漏 | 中 | 主题文件结构化、样式值精确到具体 CSS 属性 |
| 微信渲染引擎更新可能打破兼容技巧 | 低 | 技巧基于多年社区验证，核心原则不变 |
| 代码高亮准确性取决于 Claude 的 token 识别 | 中 | 提供明确 token 分类规则，常见语言覆盖良好 |
| 公式/图表无法完美渲染 | 中 | 明确标注降级策略，用户预期管理 |

---

## Verification Checklist

- [x] SKILL.md 包含完整工作流 (5 步)
- [x] 4 平台配置 (微信/知乎/掘金/博客)
- [x] 5 内置主题 (default/elegant/tech/minimal/vibrant)
- [x] 14 条 WeChat 兼容规则 (编译自全部源)
- [x] 3 代码高亮主题 + token 分类规则
- [x] 13 种 Callout 类型 (来源: obsidian)
- [x] 人性化处理模块 (24 模式/5 维/3 强度)
- [x] 脚注双向链接 (来源: baoyu)
- [x] 标题三段式装饰 (来源: mdnice)
- [x] 元素渲染规范 (含 HTML 模板)
- [x] 来源声明和溯源文档
