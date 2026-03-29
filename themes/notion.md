# Theme: Notion (Notion 风格)

Notion 风格、干净利落、功能感强。适合知识库、内部文档、Wiki 类内容。灵感来源: Notion 默认排版。

## 容器 (Container)

- max-width: 720px
- padding: 20px 0
- background: #ffffff
- margin: 0 auto

## 文字 (Text)

- color: #37352f
- secondary-color: #9b9a97
- font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC', sans-serif
- font-size: 16px
- line-height: 1.7
- letter-spacing: 0

## 标题 (Headings)

### H1 (仅博客平台)
- font-size: 30px
- font-weight: 700
- color: #37352f
- text-align: left
- margin: 40px 0 4px

### H2
- font-size: 24px
- font-weight: 600
- color: #37352f
- margin: 32px 0 8px
- padding: 0

### H3
- font-size: 20px
- font-weight: 600
- color: #37352f
- margin: 24px 0 8px

### H4
- font-size: 16px
- font-weight: 600
- color: #37352f
- margin: 20px 0 6px

## 段落 (Paragraph)

- margin: 4px 0
- padding: 3px 0

## 强调 (Emphasis)

- strong-color: #37352f
- em-color: #37352f
- highlight-background: #fef3c0
- highlight-padding: 0 2px
- highlight-border-radius: 2px

## 列表 (List)

- margin: 4px 0
- padding-left: 1.6em
- item-spacing: 2px

## 引用块 (Blockquote)

- margin: 8px 0
- padding: 4px 14px
- border-left: 3px solid #37352f
- background: transparent
- color: #37352f
- font-size: 16px

## 代码块 (Code Block)

- margin: 8px 0
- border-radius: 4px
- background: #f7f6f3
- font-size: 14px
- padding: 16px 20px
- mac-decoration: false

## 行内代码 (Inline Code)

- background: rgba(135, 131, 120, 0.15)
- color: #eb5757
- padding: 2px 4px
- border-radius: 3px
- font-size: 0.9em

## 表格 (Table)

- font-size: 14px
- header-background: #f7f6f3
- header-color: #37352f
- border-color: #e9e9e7
- cell-padding: 8px 12px
- row-even-background: transparent

## 图片 (Image)

- border-radius: 2px
- caption-color: #9b9a97
- caption-font-size: 13px

## 水平线 (HR)

- color: #e9e9e7
- margin: 16px 0

## 脚注 (Footnote)

- color: #9b9a97
- separator-color: #e9e9e7
- font-size: 13px

## 链接 (Link)

- color: #37352f
- text-decoration: underline
- text-decoration-color: rgba(55, 53, 47, 0.4)

---

## HTML 渲染模板

### 容器

```html
<section id="nice" style="max-width: 720px; margin: 0 auto; padding: 20px 0; background: #ffffff; color: #37352f; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC', sans-serif; font-size: 16px; line-height: 1.7; word-break: break-word; overflow-wrap: break-word;">
```

### H2 标题（大号粗体，无装饰）

```html
<h2 style="font-size: 24px; font-weight: 600; color: #37352f; margin: 32px 0 8px; padding: 0;">标题文本</h2>
```

### H3 标题

```html
<h3 style="font-size: 20px; font-weight: 600; color: #37352f; margin: 24px 0 8px;">标题文本</h3>
```

### 段落（紧凑间距，Notion 特色）

```html
<p style="margin: 4px 0; padding: 3px 0; color: #37352f; font-size: 16px; line-height: 1.7;">段落文本</p>
```

### 粗体强调

```html
<strong style="color: #37352f; font-weight: 600;">粗体文本</strong>
```

### 引用块（简洁左边框）

```html
<blockquote style="margin: 8px 0; padding: 4px 14px; border-left: 3px solid #37352f; background: transparent; color: #37352f; font-size: 16px; line-height: 1.7;">
  <p style="margin: 0; font-size: 16px;">引用内容</p>
</blockquote>
```

### 代码块（暖灰底色，无装饰）

```html
<section style="margin: 8px 0; border-radius: 4px; overflow: hidden; background: #f7f6f3;">
  <section style="padding: 16px 20px; overflow-x: auto; font-family: 'SFMono-Regular', 'Menlo', 'Consolas', monospace; font-size: 14px; line-height: 1.6; color: #37352f;">
    代码内容
  </section>
</section>
```

### 行内代码

```html
<code style="background: rgba(135, 131, 120, 0.15); color: #eb5757; padding: 2px 4px; border-radius: 3px; font-family: 'SFMono-Regular', 'Menlo', monospace; font-size: 0.9em;">code</code>
```

### 水平线

```html
<hr style="border: none; height: 1px; background: #e9e9e7; margin: 16px 0;">
```
