# Theme: Elegant (优雅)

文艺、精致、暖色调。适合人文/商业/叙事类文章。灵感来源: baoyu grace + 经典中式排版。

## 容器 (Container)

- max-width: 740px
- padding: 24px 28px
- background: #fefefe
- margin: 0 auto

## 文字 (Text)

- color: #2c3e50
- secondary-color: #7f8c8d
- font-family: 'Noto Serif SC', 'Source Han Serif CN', 'STSongti-SC', Georgia, 'Times New Roman', serif
- font-size: 16px
- line-height: 1.9
- letter-spacing: 0.06em

## 标题 (Headings)

### H1 (仅博客平台)
- font-size: 28px
- font-weight: 700
- color: #2c3e50
- text-align: center
- margin: 48px 0 28px
- padding-bottom: 16px
- border-bottom: 1px solid #c0392b

### H2
- font-size: 22px
- font-weight: 700
- color: #ffffff
- margin: 36px 0 18px
- padding: 6px 16px
- background: #2c3e50
- display: inline-block
- border-radius: 2px
- prefix-style: display: none;
- content-style: ;
- suffix-style: display: none;

### H3
- font-size: 18px
- font-weight: 700
- color: #c0392b
- margin: 28px 0 14px
- padding: 0
- border-bottom: 1px dashed #c0392b
- padding-bottom: 6px

### H4
- font-size: 16px
- font-weight: 700
- color: #2c3e50
- margin: 20px 0 10px
- font-style: italic

## 段落 (Paragraph)

- margin: 18px 0
- padding: 0
- text-indent: 0

## 强调 (Emphasis)

- strong-color: #c0392b
- em-color: #8e44ad
- highlight-background: #fde8e8
- highlight-padding: 2px 6px
- highlight-border-radius: 2px

## 列表 (List)

- margin: 16px 0
- padding-left: 2em
- item-spacing: 8px

## 引用块 (Blockquote)

- margin: 20px 0
- padding: 16px 20px
- border-left: 3px solid #c0392b
- background: #fdf2f2
- color: #555555
- font-size: 15px
- border-radius: 0 6px 6px 0

## 代码块 (Code Block)

- margin: 18px 0
- border-radius: 6px
- background: #fbebd4 (Kimbie Light 默认)
- font-size: 13px
- padding: 16px
- mac-decoration: false

## 行内代码 (Inline Code)

- background: #fdf2f2
- color: #c0392b
- padding: 2px 6px
- border-radius: 3px
- font-size: 0.9em

## 表格 (Table)

- font-size: 14px
- header-background: #2c3e50
- header-color: #ffffff
- border-color: #d5dbdb
- cell-padding: 10px 14px
- row-even-background: #fdfefe

## 图片 (Image)

- border-radius: 6px
- caption-color: #7f8c8d
- caption-font-size: 13px
- caption-font-style: italic

## 水平线 (HR)

- color: #d5dbdb
- margin: 28px 0

## 脚注 (Footnote)

- color: #c0392b
- separator-color: #d5dbdb
- font-size: 13px

## 链接 (Link)

- color: #c0392b
- text-decoration: none
- border-bottom: 1px solid #c0392b

---

## HTML 渲染模板

### 容器

```html
<section id="nice" style="max-width: 740px; margin: 0 auto; padding: 24px 28px; background: #fefefe; color: #2c3e50; font-family: 'Noto Serif SC', 'Source Han Serif CN', 'STSongti-SC', Georgia, 'Times New Roman', serif; font-size: 16px; line-height: 1.9; letter-spacing: 0.06em; word-break: break-word; overflow-wrap: break-word;">
```

### TL;DR / 摘要高亮

```html
<p style="margin: 18px 0; padding: 12px 18px; background: #fdf2f2; border-radius: 6px; border-left: 3px solid #c0392b; color: #2c3e50; font-size: 16px; line-height: 1.9;"><strong style="color: #c0392b; font-weight: bold;">TL;DR</strong>：摘要内容</p>
```

### H2 标题（深底白字徽章）

```html
<h2 style="font-size: 22px; font-weight: 700; color: #ffffff; margin: 36px 0 18px; padding: 6px 16px; background: #2c3e50; display: inline-block; border-radius: 2px;">标题文本</h2>
```

### H3 标题（红色虚线下边框）

```html
<h3 style="font-size: 18px; font-weight: 700; color: #c0392b; margin: 28px 0 14px; padding: 0; border-bottom: 1px dashed #c0392b; padding-bottom: 6px;">标题文本</h3>
```

### 段落

```html
<p style="margin: 18px 0; padding: 0; color: #2c3e50; font-size: 16px; line-height: 1.9; letter-spacing: 0.06em;">段落文本</p>
```

### 粗体强调

```html
<strong style="color: #c0392b; font-weight: bold;">粗体文本</strong>
```

### 引用块（红色边框 + 圆角）

```html
<blockquote style="margin: 20px 0; padding: 16px 20px; border-left: 3px solid #c0392b; background: #fdf2f2; color: #555555; font-size: 15px; line-height: 1.9; border-radius: 0 6px 6px 0;">
  <p style="margin: 0; font-size: 15px; font-style: italic;">引用内容</p>
</blockquote>
```

### 无序列表

```html
<ul style="margin: 16px 0; padding-left: 2em;">
  <li style="margin-bottom: 8px;"><section style="color: #2c3e50; font-size: 16px; line-height: 1.9;">列表项内容</section></li>
</ul>
```

### 代码块（Kimbie Light 暖色调，无 macOS 装饰）

```html
<section style="margin: 18px 0; border-radius: 6px; overflow: hidden; background: #fbebd4;">
  <section style="padding: 12px 16px; overflow-x: auto; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 13px; line-height: 1.6; color: #84613d;">
    代码内容（Kimbie Light 配色：keyword=#98676a string=#889b4a comment=#a57a4c function=#f79a32）
  </section>
</section>
```

### 行内代码

```html
<code style="background: #fdf2f2; color: #c0392b; padding: 2px 6px; border-radius: 3px; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 0.9em;">code</code>
```

### 水平线

```html
<hr style="border: none; height: 1px; background: #d5dbdb; margin: 28px 0; transform: scale(1, 0.5);">
```
