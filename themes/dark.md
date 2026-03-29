# Theme: Dark (深色)

深色背景、护眼、沉浸式阅读。适合技术社区、夜间阅读、开发者受众。灵感来源: GitHub Dark + One Dark Pro。

## 容器 (Container)

- max-width: 780px
- padding: 24px 28px
- background: #1e1e2e
- margin: 0 auto

## 文字 (Text)

- color: #cdd6f4
- secondary-color: #7f849c
- font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC', 'Microsoft YaHei', sans-serif
- font-size: 16px
- line-height: 1.8
- letter-spacing: 0.03em

## 标题 (Headings)

### H1 (仅博客平台)
- font-size: 26px
- font-weight: 700
- color: #cba6f7
- text-align: left
- margin: 40px 0 24px

### H2
- font-size: 22px
- font-weight: 700
- color: #89b4fa
- margin: 32px 0 16px
- padding-bottom: 8px
- border-bottom: 1px solid #313244

### H3
- font-size: 18px
- font-weight: 600
- color: #a6e3a1
- margin: 24px 0 12px

### H4
- font-size: 16px
- font-weight: 600
- color: #cdd6f4
- margin: 20px 0 10px

## 段落 (Paragraph)

- margin: 16px 0
- padding: 0

## 强调 (Emphasis)

- strong-color: #f9e2af
- em-color: #f5c2e7
- highlight-background: rgba(249, 226, 175, 0.15)
- highlight-padding: 2px 4px
- highlight-border-radius: 2px

## 列表 (List)

- margin: 16px 0
- padding-left: 2em
- item-spacing: 6px

## 引用块 (Blockquote)

- margin: 16px 0
- padding: 12px 16px
- border-left: 4px solid #89b4fa
- background: #181825
- color: #bac2de
- font-size: 15px

## 代码块 (Code Block)

- margin: 16px 0
- border-radius: 8px
- background: #11111b
- font-size: 13px
- padding: 16px
- mac-decoration: true
- 默认代码主题: one-dark

## 行内代码 (Inline Code)

- background: #313244
- color: #f38ba8
- padding: 2px 6px
- border-radius: 4px
- font-size: 0.9em

## 表格 (Table)

- font-size: 14px
- header-background: #313244
- header-color: #cdd6f4
- border-color: #45475a
- cell-padding: 8px 12px
- row-even-background: #181825

## 图片 (Image)

- border-radius: 6px
- caption-color: #7f849c
- caption-font-size: 13px

## 水平线 (HR)

- color: #313244
- margin: 24px 0

## 脚注 (Footnote)

- color: #89b4fa
- separator-color: #313244
- font-size: 13px

## 链接 (Link)

- color: #89b4fa
- text-decoration: none
- border-bottom: 1px dashed #89b4fa

---

## HTML 渲染模板

### 容器

```html
<section id="nice" style="max-width: 780px; margin: 0 auto; padding: 24px 28px; background: #1e1e2e; color: #cdd6f4; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'PingFang SC', 'Microsoft YaHei', sans-serif; font-size: 16px; line-height: 1.8; letter-spacing: 0.03em; word-break: break-word; overflow-wrap: break-word;">
```

### H2 标题（蓝色文字 + 底部细线）

```html
<h2 style="font-size: 22px; font-weight: 700; color: #89b4fa; margin: 32px 0 16px; padding-bottom: 8px; border-bottom: 1px solid #313244;">标题文本</h2>
```

### H3 标题（绿色文字）

```html
<h3 style="font-size: 18px; font-weight: 600; color: #a6e3a1; margin: 24px 0 12px;">标题文本</h3>
```

### 段落

```html
<p style="margin: 16px 0; padding: 0; color: #cdd6f4; font-size: 16px; line-height: 1.8; letter-spacing: 0.03em;">段落文本</p>
```

### 粗体强调

```html
<strong style="color: #f9e2af; font-weight: bold;">粗体文本</strong>
```

### 引用块

```html
<blockquote style="margin: 16px 0; padding: 12px 16px; border-left: 4px solid #89b4fa; background: #181825; color: #bac2de; font-size: 15px; line-height: 1.8; border-radius: 0 4px 4px 0;">
  <p style="margin: 0; font-size: 15px; line-height: 1.8;">引用内容</p>
</blockquote>
```

### 代码块（深色背景 + macOS 装饰）

```html
<section style="margin: 16px 0; border-radius: 8px; overflow: hidden; background: #11111b;">
  <section style="padding: 8px 16px; display: flex; align-items: center; gap: 6px; background: #181825;">
    <span style="width: 10px; height: 10px; border-radius: 50%; background: #ff5f57; display: inline-block;"></span>
    <span style="width: 10px; height: 10px; border-radius: 50%; background: #febc2e; display: inline-block;"></span>
    <span style="width: 10px; height: 10px; border-radius: 50%; background: #28c840; display: inline-block;"></span>
    <span style="flex: 1;"></span>
    <span style="font-size: 12px; color: #7f849c; font-family: monospace;">语言</span>
  </section>
  <section style="padding: 12px 16px; overflow-x: auto; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 13px; line-height: 1.6; color: #cdd6f4;">
    代码内容
  </section>
</section>
```

### 行内代码

```html
<code style="background: #313244; color: #f38ba8; padding: 2px 6px; border-radius: 4px; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 0.9em;">code</code>
```

### 水平线

```html
<hr style="border: none; height: 1px; background: #313244; margin: 24px 0;">
```
