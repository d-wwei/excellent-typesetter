# Theme: Default (默认)

专业、均衡、蓝色调。适合通用文章。

## 容器 (Container)

- max-width: 780px
- padding: 20px 24px
- background: #ffffff
- margin: 0 auto

## 文字 (Text)

- color: #3f3f3f
- secondary-color: #888888
- font-family: -apple-system, BlinkMacSystemFont, 'Helvetica Neue', 'PingFang SC', 'Microsoft YaHei', sans-serif
- font-size: 16px
- line-height: 1.8
- letter-spacing: 0.04em

## 标题 (Headings)

### H1 (仅博客平台)
- font-size: 26px
- font-weight: 700
- color: #1a1a2e
- text-align: center
- margin: 40px 0 24px
- padding-bottom: 12px
- border-bottom: 2px solid #0f4c81

### H2
- font-size: 22px
- font-weight: 700
- color: #1a1a2e
- margin: 32px 0 16px
- padding: 0
- prefix-style: display: inline-block; width: 4px; height: 22px; background: #0f4c81; margin-right: 10px; vertical-align: middle; border-radius: 2px;
- content-style: vertical-align: middle;
- suffix-style: display: none;

### H3
- font-size: 18px
- font-weight: 700
- color: #1a1a2e
- margin: 24px 0 12px
- padding-left: 12px
- border-left: 3px solid #0f4c81

### H4
- font-size: 16px
- font-weight: 700
- color: #3f3f3f
- margin: 20px 0 10px

## 段落 (Paragraph)

- margin: 16px 0
- padding: 0

## 强调 (Emphasis)

- strong-color: #0f4c81
- em-color: #0f4c81
- highlight-background: #fff3cd
- highlight-padding: 2px 4px
- highlight-border-radius: 2px

## 列表 (List)

- margin: 16px 0
- padding-left: 2em
- item-spacing: 6px

## 引用块 (Blockquote)

- margin: 16px 0
- padding: 12px 16px
- border-left: 4px solid #0f4c81
- background: #f0f4f8
- color: #555555
- font-size: 15px

## 代码块 (Code Block)

- margin: 16px 0
- border-radius: 8px
- background: #f6f8fa (GitHub Light 默认)
- font-size: 13px
- padding: 16px
- mac-decoration: true

## 行内代码 (Inline Code)

- background: rgba(27, 31, 35, 0.05)
- color: #0f4c81
- padding: 2px 6px
- border-radius: 4px
- font-size: 0.9em

## 表格 (Table)

- font-size: 14px
- header-background: #f0f4f8
- header-color: #1a1a2e
- border-color: #e1e4e8
- cell-padding: 8px 12px
- row-even-background: #fafbfc

## 图片 (Image)

- border-radius: 4px
- caption-color: #888888
- caption-font-size: 13px

## 水平线 (HR)

- color: #e1e4e8
- margin: 24px 0

## 脚注 (Footnote)

- color: #0f4c81
- separator-color: #e1e4e8
- font-size: 13px

## 链接 (Link)

- color: #0f4c81
- text-decoration: none
- border-bottom: 1px solid #0f4c81

---

## HTML 渲染模板

以下是关键元素的精确 HTML 内联样式模板。渲染时直接复制并替换内容文本。

### 容器

```html
<section id="nice" style="max-width: 780px; margin: 0 auto; padding: 20px 24px; background: #ffffff; color: #3f3f3f; font-family: -apple-system, BlinkMacSystemFont, 'Helvetica Neue', 'PingFang SC', 'Microsoft YaHei', sans-serif; font-size: 16px; line-height: 1.8; letter-spacing: 0.04em; word-break: break-word; overflow-wrap: break-word;">
```

### TL;DR / 摘要高亮

```html
<p style="margin: 16px 0; padding: 10px 16px; background: #f0f4f8; border-radius: 6px; color: #3f3f3f; font-size: 16px; line-height: 1.8; letter-spacing: 0.04em;"><strong style="color: #0f4c81; font-weight: bold;">TL;DR</strong>：摘要内容</p>
```

### H2 标题（蓝色竖条前缀）

```html
<h2 style="font-size: 22px; font-weight: 700; color: #1a1a2e; margin: 32px 0 16px; padding: 0; display: flex; align-items: center;"><span style="display: inline-block; width: 4px; height: 22px; background: #0f4c81; margin-right: 10px; vertical-align: middle; border-radius: 2px;"></span><span style="vertical-align: middle;">标题文本</span><span style="display: none;"></span></h2>
```

### H3 标题（左侧蓝色边框）

```html
<h3 style="font-size: 18px; font-weight: 700; color: #1a1a2e; margin: 24px 0 12px; padding-left: 12px; border-left: 3px solid #0f4c81;">标题文本</h3>
```

### 段落

```html
<p style="margin: 16px 0; padding: 0; color: #3f3f3f; font-size: 16px; line-height: 1.8; letter-spacing: 0.04em;">段落文本</p>
```

### 粗体强调

```html
<strong style="color: #0f4c81; font-weight: bold;">粗体文本</strong>
```

### 引用块

```html
<blockquote style="margin: 16px 0; padding: 12px 16px; border-left: 4px solid #0f4c81; background: #f0f4f8; color: #555555; font-size: 15px; line-height: 1.8; border-radius: 0 4px 4px 0;">
  <p style="margin: 0; font-size: 15px; line-height: 1.8;">引用内容</p>
</blockquote>
```

### 无序列表

```html
<ul style="margin: 16px 0; padding-left: 2em;">
  <li style="margin-bottom: 6px;"><section style="color: #3f3f3f; font-size: 16px; line-height: 1.8;">列表项内容</section></li>
</ul>
```

### 代码块（GitHub Light + macOS 装饰）

```html
<section style="margin: 16px 0; border-radius: 8px; overflow: hidden; background: #f6f8fa;">
  <section style="padding: 8px 16px; display: flex; align-items: center; gap: 6px; background: #f0f2f5;">
    <span style="width: 10px; height: 10px; border-radius: 50%; background: #ff5f57; display: inline-block;"></span>
    <span style="width: 10px; height: 10px; border-radius: 50%; background: #febc2e; display: inline-block;"></span>
    <span style="width: 10px; height: 10px; border-radius: 50%; background: #28c840; display: inline-block;"></span>
    <span style="flex: 1;"></span>
    <span style="font-size: 12px; color: #999; font-family: monospace;">语言</span>
  </section>
  <section style="padding: 12px 16px; overflow-x: auto; font-family: 'Menlo', 'Monaco', 'Consolas', 'Courier New', monospace; font-size: 13px; line-height: 1.6; color: #24292e;">
    代码内容（逐 token 着色）
  </section>
</section>
```

### 行内代码

```html
<code style="background: rgba(27, 31, 35, 0.05); color: #0f4c81; padding: 2px 6px; border-radius: 4px; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 0.9em;">code</code>
```

### 水平线

```html
<hr style="border: none; height: 1px; background: #e1e4e8; margin: 24px 0; transform: scale(1, 0.5);">
```

### 脚注引用

```html
<sup style="font-size: 0.7em; color: #0f4c81; vertical-align: super;"><a href="#fn-1" style="color: #0f4c81; text-decoration: none;">[1]</a></sup>
```
