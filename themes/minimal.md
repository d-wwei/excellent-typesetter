# Theme: Minimal (极简)

极简、大留白、注重排版节奏。适合短文/思考/随笔。灵感来源: Swiss Typography + wechat-format 简约风。

## 容器 (Container)

- max-width: 680px
- padding: 24px 32px
- background: #ffffff
- margin: 0 auto

## 文字 (Text)

- color: #333333
- secondary-color: #999999
- font-family: -apple-system, BlinkMacSystemFont, 'PingFang SC', 'Helvetica Neue', sans-serif
- font-size: 16px
- line-height: 2.0
- letter-spacing: 0.04em

## 标题 (Headings)

### H1 (仅博客平台)
- font-size: 28px
- font-weight: 300
- color: #333333
- text-align: left
- margin: 48px 0 28px
- letter-spacing: 0.08em

### H2
- font-size: 20px
- font-weight: 700
- color: #333333
- margin: 40px 0 20px
- padding: 0
- letter-spacing: 0.06em
- prefix-style: display: none;
- content-style: ;
- suffix-style: display: none;

### H3
- font-size: 16px
- font-weight: 700
- color: #333333
- margin: 32px 0 14px
- padding: 0
- text-transform: uppercase
- letter-spacing: 0.1em
- font-size: 13px

### H4
- font-size: 16px
- font-weight: 400
- color: #666666
- margin: 24px 0 10px
- font-style: italic

## 段落 (Paragraph)

- margin: 20px 0
- padding: 0

## 强调 (Emphasis)

- strong-color: #111111
- em-color: #666666
- highlight-background: #f5f5f5
- highlight-padding: 2px 4px
- highlight-border-radius: 0

## 列表 (List)

- margin: 20px 0
- padding-left: 1.5em
- item-spacing: 8px

## 引用块 (Blockquote)

- margin: 24px 0
- padding: 16px 24px
- border-left: 2px solid #dddddd
- background: transparent
- color: #666666
- font-size: 15px
- font-style: italic

## 代码块 (Code Block)

- margin: 20px 0
- border-radius: 0
- background: #f8f8f8
- font-size: 13px
- padding: 16px 20px
- border: 1px solid #eeeeee
- mac-decoration: false

## 行内代码 (Inline Code)

- background: #f5f5f5
- color: #333333
- padding: 2px 6px
- border-radius: 0
- font-size: 0.9em
- border: 1px solid #eeeeee

## 表格 (Table)

- font-size: 14px
- header-background: transparent
- header-color: #333333
- border-color: #dddddd
- cell-padding: 10px 16px
- row-even-background: transparent
- header-border-bottom: 2px solid #333333

## 图片 (Image)

- border-radius: 0
- caption-color: #999999
- caption-font-size: 12px
- caption-letter-spacing: 0.08em
- caption-text-transform: uppercase

## 水平线 (HR)

- color: #dddddd
- margin: 32px 0

## 脚注 (Footnote)

- color: #666666
- separator-color: #dddddd
- font-size: 13px

## 链接 (Link)

- color: #333333
- text-decoration: underline
- text-underline-offset: 3px

---

## HTML 渲染模板

### 容器

```html
<section id="nice" style="max-width: 680px; margin: 0 auto; padding: 24px 32px; background: #ffffff; color: #333333; font-family: -apple-system, BlinkMacSystemFont, 'PingFang SC', 'Helvetica Neue', sans-serif; font-size: 16px; line-height: 2.0; letter-spacing: 0.04em; word-break: break-word; overflow-wrap: break-word;">
```

### TL;DR / 摘要（无背景，纯文字弱化）

```html
<p style="margin: 20px 0; padding: 0; color: #666666; font-size: 16px; line-height: 2.0;"><strong style="color: #111111; font-weight: bold;">TL;DR</strong>：摘要内容</p>
```

### H2 标题（纯文字，无装饰）

```html
<h2 style="font-size: 20px; font-weight: 700; color: #333333; margin: 40px 0 20px; padding: 0; letter-spacing: 0.06em;">标题文本</h2>
```

### H3 标题（大写小字）

```html
<h3 style="font-size: 13px; font-weight: 700; color: #333333; margin: 32px 0 14px; padding: 0; text-transform: uppercase; letter-spacing: 0.1em;">标题文本</h3>
```

### 段落

```html
<p style="margin: 20px 0; padding: 0; color: #333333; font-size: 16px; line-height: 2.0; letter-spacing: 0.04em;">段落文本</p>
```

### 粗体强调

```html
<strong style="color: #111111; font-weight: bold;">粗体文本</strong>
```

### 引用块（极简：细线 + 透明背景 + 斜体）

```html
<blockquote style="margin: 24px 0; padding: 16px 24px; border-left: 2px solid #dddddd; background: transparent; color: #666666; font-size: 15px; line-height: 2.0; font-style: italic;">
  <p style="margin: 0; font-size: 15px;">引用内容</p>
</blockquote>
```

### 无序列表

```html
<ul style="margin: 20px 0; padding-left: 1.5em;">
  <li style="margin-bottom: 8px;"><section style="color: #333333; font-size: 16px; line-height: 2.0;">列表项内容</section></li>
</ul>
```

### 代码块（浅灰底 + 细边框，无 macOS 装饰，无圆角）

```html
<section style="margin: 20px 0; overflow: hidden; background: #f8f8f8; border: 1px solid #eeeeee;">
  <section style="padding: 12px 20px; overflow-x: auto; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 13px; line-height: 1.6; color: #333333;">
    代码内容（单色：全部用 #333，注释用 #999）
  </section>
</section>
```

### 行内代码

```html
<code style="background: #f5f5f5; color: #333333; padding: 2px 6px; border-radius: 0; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 0.9em; border: 1px solid #eeeeee;">code</code>
```

### 水平线

```html
<hr style="border: none; height: 1px; background: #dddddd; margin: 32px 0; transform: scale(1, 0.5);">
```
