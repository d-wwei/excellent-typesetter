# Theme: Tech (技术)

现代、冷色调、代码友好。适合技术文章/教程。灵感来源: baoyu modern + GitHub 风格。

## 容器 (Container)

- max-width: 800px
- padding: 20px 24px
- background: #ffffff
- margin: 0 auto

## 文字 (Text)

- color: #1f2937
- secondary-color: #6b7280
- font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC', 'Microsoft YaHei', sans-serif
- font-size: 15px
- line-height: 1.75
- letter-spacing: 0.02em

## 标题 (Headings)

### H1 (仅博客平台)
- font-size: 28px
- font-weight: 800
- color: #111827
- text-align: left
- margin: 40px 0 20px
- padding-bottom: 12px
- border-bottom: 3px solid #0891b2

### H2
- font-size: 22px
- font-weight: 700
- color: #111827
- margin: 32px 0 16px
- padding-left: 14px
- border-left: 4px solid #0891b2
- prefix-style: display: none;
- content-style: ;
- suffix-style: display: none;

### H3
- font-size: 18px
- font-weight: 600
- color: #0891b2
- margin: 24px 0 12px
- padding: 0

### H4
- font-size: 15px
- font-weight: 600
- color: #374151
- margin: 20px 0 8px
- text-transform: uppercase
- letter-spacing: 0.05em
- font-size: 13px

## 段落 (Paragraph)

- margin: 14px 0
- padding: 0

## 强调 (Emphasis)

- strong-color: #111827
- em-color: #0891b2
- highlight-background: #ecfdf5
- highlight-padding: 2px 4px
- highlight-border-radius: 2px

## 列表 (List)

- margin: 14px 0
- padding-left: 2em
- item-spacing: 4px

## 引用块 (Blockquote)

- margin: 16px 0
- padding: 12px 16px
- border-left: 4px solid #0891b2
- background: #f0fdfa
- color: #1f2937
- font-size: 14px
- border-radius: 0 4px 4px 0

## 代码块 (Code Block)

- margin: 16px 0
- border-radius: 8px
- background: #282c34 (One Dark 默认)
- font-size: 13px
- padding: 16px
- mac-decoration: true
- 默认代码主题: one-dark

## 行内代码 (Inline Code)

- background: #f0fdfa
- color: #0891b2
- padding: 2px 6px
- border-radius: 4px
- font-size: 0.85em
- font-weight: 500

## 表格 (Table)

- font-size: 13px
- header-background: #f3f4f6
- header-color: #111827
- border-color: #e5e7eb
- cell-padding: 8px 12px
- row-even-background: #f9fafb
- font-family: monospace (for data cells)

## 图片 (Image)

- border-radius: 6px
- border: 1px solid #e5e7eb
- caption-color: #6b7280
- caption-font-size: 12px
- caption-font-family: monospace

## 水平线 (HR)

- color: #e5e7eb
- margin: 24px 0

## 脚注 (Footnote)

- color: #0891b2
- separator-color: #e5e7eb
- font-size: 12px
- font-family: monospace

## 链接 (Link)

- color: #0891b2
- text-decoration: none
- border-bottom: 1px dashed #0891b2

---

## HTML 渲染模板

### 容器

```html
<section id="nice" style="max-width: 800px; margin: 0 auto; padding: 20px 24px; background: #ffffff; color: #1f2937; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC', 'Microsoft YaHei', sans-serif; font-size: 15px; line-height: 1.75; letter-spacing: 0.02em; word-break: break-word; overflow-wrap: break-word;">
```

### TL;DR / 摘要高亮

```html
<p style="margin: 14px 0; padding: 10px 16px; background: #f0fdfa; border-radius: 6px; border: 1px solid #ccfbf1; color: #1f2937; font-size: 15px; line-height: 1.75;"><strong style="color: #0891b2; font-weight: bold;">TL;DR</strong>：摘要内容</p>
```

### H2 标题（粗左边框）

```html
<h2 style="font-size: 22px; font-weight: 700; color: #111827; margin: 32px 0 16px; padding-left: 14px; border-left: 4px solid #0891b2;">标题文本</h2>
```

### H3 标题（青色文字）

```html
<h3 style="font-size: 18px; font-weight: 600; color: #0891b2; margin: 24px 0 12px; padding: 0;">标题文本</h3>
```

### 段落

```html
<p style="margin: 14px 0; padding: 0; color: #1f2937; font-size: 15px; line-height: 1.75; letter-spacing: 0.02em;">段落文本</p>
```

### 粗体强调

```html
<strong style="color: #111827; font-weight: bold;">粗体文本</strong>
```

### 引用块

```html
<blockquote style="margin: 16px 0; padding: 12px 16px; border-left: 4px solid #0891b2; background: #f0fdfa; color: #1f2937; font-size: 14px; line-height: 1.75; border-radius: 0 4px 4px 0;">
  <p style="margin: 0; font-size: 14px;">引用内容</p>
</blockquote>
```

### 无序列表

```html
<ul style="margin: 14px 0; padding-left: 2em;">
  <li style="margin-bottom: 4px;"><section style="color: #1f2937; font-size: 15px; line-height: 1.75;">列表项内容</section></li>
</ul>
```

### 代码块（One Dark + macOS 装饰）

```html
<section style="margin: 16px 0; border-radius: 8px; overflow: hidden; background: #282c34;">
  <section style="padding: 8px 16px; display: flex; align-items: center; gap: 6px; background: #21252b;">
    <span style="width: 10px; height: 10px; border-radius: 50%; background: #ff5f57; display: inline-block;"></span>
    <span style="width: 10px; height: 10px; border-radius: 50%; background: #febc2e; display: inline-block;"></span>
    <span style="width: 10px; height: 10px; border-radius: 50%; background: #28c840; display: inline-block;"></span>
    <span style="flex: 1;"></span>
    <span style="font-size: 12px; color: #636d83; font-family: monospace;">语言</span>
  </section>
  <section style="padding: 12px 16px; overflow-x: auto; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 13px; line-height: 1.6; color: #abb2bf;">
    代码内容（One Dark 配色：keyword=#c678dd string=#98c379 comment=#5c6370 function=#61afef）
  </section>
</section>
```

### 行内代码

```html
<code style="background: #f0fdfa; color: #0891b2; padding: 2px 6px; border-radius: 4px; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 0.85em; font-weight: 500;">code</code>
```

### 水平线

```html
<hr style="border: none; height: 1px; background: #e5e7eb; margin: 24px 0; transform: scale(1, 0.5);">
```
