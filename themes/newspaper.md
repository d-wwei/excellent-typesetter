# Theme: Newspaper (报纸)

经典报纸印刷风、衬线字体、严肃权威感。适合深度报道、长文评论、行业分析。灵感来源: NYT/Economist 排版。

## 容器 (Container)

- max-width: 720px
- padding: 24px 32px
- background: #faf9f6
- margin: 0 auto

## 文字 (Text)

- color: #1a1a1a
- secondary-color: #6b6b6b
- font-family: 'Noto Serif SC', 'Source Han Serif CN', Georgia, 'Times New Roman', serif
- font-size: 17px
- line-height: 1.9
- letter-spacing: 0.02em

## 标题 (Headings)

### H1 (仅博客平台)
- font-size: 32px
- font-weight: 900
- color: #1a1a1a
- text-align: center
- margin: 48px 0 16px
- font-family: 'Noto Serif SC', Georgia, serif
- letter-spacing: 0.04em

### H2
- font-size: 24px
- font-weight: 700
- color: #1a1a1a
- margin: 36px 0 12px
- padding-bottom: 8px
- border-bottom: 2px solid #1a1a1a

### H3
- font-size: 19px
- font-weight: 700
- color: #1a1a1a
- margin: 28px 0 10px
- font-style: italic

### H4
- font-size: 17px
- font-weight: 700
- color: #4a4a4a
- margin: 20px 0 8px

## 段落 (Paragraph)

- margin: 16px 0
- padding: 0
- text-indent: 2em

## 强调 (Emphasis)

- strong-color: #1a1a1a
- em-color: #1a1a1a
- highlight-background: #fff8dc
- highlight-padding: 2px 4px
- highlight-border-radius: 0

## 列表 (List)

- margin: 16px 0
- padding-left: 2em
- item-spacing: 6px

## 引用块 (Blockquote)

- margin: 24px 0
- padding: 20px 24px
- border-left: none
- border-top: 2px solid #1a1a1a
- border-bottom: 1px solid #d0d0d0
- background: transparent
- color: #4a4a4a
- font-size: 18px
- font-style: italic

## 代码块 (Code Block)

- margin: 20px 0
- border-radius: 0
- background: #f4f3ef
- font-size: 13px
- padding: 16px 20px
- border: 1px solid #d0d0d0
- mac-decoration: false

## 行内代码 (Inline Code)

- background: #f4f3ef
- color: #c7254e
- padding: 2px 6px
- border-radius: 0
- font-size: 0.85em

## 表格 (Table)

- font-size: 14px
- header-background: transparent
- header-color: #1a1a1a
- border-color: #1a1a1a
- cell-padding: 10px 14px
- row-even-background: transparent
- header-border-bottom: 2px solid #1a1a1a

## 图片 (Image)

- border-radius: 0
- caption-color: #6b6b6b
- caption-font-size: 13px
- caption-font-style: italic

## 水平线 (HR)

- color: #1a1a1a
- margin: 32px auto
- width: 40%

## 脚注 (Footnote)

- color: #6b6b6b
- separator-color: #1a1a1a
- font-size: 13px

## 链接 (Link)

- color: #1a1a1a
- text-decoration: underline
- text-decoration-style: dotted

---

## HTML 渲染模板

### 容器

```html
<section id="nice" style="max-width: 720px; margin: 0 auto; padding: 24px 32px; background: #faf9f6; color: #1a1a1a; font-family: 'Noto Serif SC', 'Source Han Serif CN', Georgia, 'Times New Roman', serif; font-size: 17px; line-height: 1.9; letter-spacing: 0.02em; word-break: break-word; overflow-wrap: break-word;">
```

### H2 标题（粗体 + 粗底线，报纸风）

```html
<h2 style="font-size: 24px; font-weight: 700; color: #1a1a1a; margin: 36px 0 12px; padding-bottom: 8px; border-bottom: 2px solid #1a1a1a;">标题文本</h2>
```

### H3 标题（斜体）

```html
<h3 style="font-size: 19px; font-weight: 700; color: #1a1a1a; margin: 28px 0 10px; font-style: italic;">标题文本</h3>
```

### 段落（首行缩进，报纸特色）

```html
<p style="margin: 16px 0; padding: 0; color: #1a1a1a; font-size: 17px; line-height: 1.9; letter-spacing: 0.02em; text-indent: 2em;">段落文本</p>
```

### 粗体强调

```html
<strong style="color: #1a1a1a; font-weight: 700;">粗体文本</strong>
```

### 引用块（上粗线 + 下细线，无左边框）

```html
<blockquote style="margin: 24px 0; padding: 20px 24px; border-left: none; border-top: 2px solid #1a1a1a; border-bottom: 1px solid #d0d0d0; background: transparent; color: #4a4a4a; font-size: 18px; font-style: italic; line-height: 1.9;">
  <p style="margin: 0; font-size: 18px; font-style: italic;">引用内容</p>
</blockquote>
```

### 代码块（方正无圆角，报纸风）

```html
<section style="margin: 20px 0; overflow: hidden; background: #f4f3ef; border: 1px solid #d0d0d0;">
  <section style="padding: 16px 20px; overflow-x: auto; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 13px; line-height: 1.6; color: #1a1a1a;">
    代码内容
  </section>
</section>
```

### 行内代码

```html
<code style="background: #f4f3ef; color: #c7254e; padding: 2px 6px; border-radius: 0; font-family: 'Menlo', 'Monaco', monospace; font-size: 0.85em;">code</code>
```

### 水平线（短居中线，报纸分隔风格）

```html
<hr style="border: none; height: 1px; background: #1a1a1a; margin: 32px auto; width: 40%;">
```
