# Theme: Gradient (渐变)

现代渐变色、视觉冲击力强。适合产品发布、发布会风格、品牌宣传。灵感来源: Apple Keynote + Linear 设计风格。

## 容器 (Container)

- max-width: 780px
- padding: 24px 28px
- background: #ffffff
- margin: 0 auto

## 文字 (Text)

- color: #1d1d1f
- secondary-color: #86868b
- font-family: -apple-system, BlinkMacSystemFont, 'SF Pro Display', 'PingFang SC', sans-serif
- font-size: 16px
- line-height: 1.8
- letter-spacing: 0.02em

## 标题 (Headings)

### H1 (仅博客平台)
- font-size: 36px
- font-weight: 700
- background: linear-gradient(135deg, #667eea 0%, #764ba2 100%)
- -webkit-background-clip: text
- -webkit-text-fill-color: transparent
- text-align: center
- margin: 48px 0 24px

### H2
- font-size: 24px
- font-weight: 700
- color: #1d1d1f
- margin: 36px 0 16px
- padding: 8px 16px
- background: linear-gradient(135deg, #667eea08 0%, #764ba208 100%)
- border-left: 4px solid
- border-image: linear-gradient(180deg, #667eea, #764ba2) 1

### H3
- font-size: 18px
- font-weight: 600
- color: #667eea
- margin: 24px 0 12px

### H4
- font-size: 16px
- font-weight: 600
- color: #1d1d1f
- margin: 20px 0 10px

## 段落 (Paragraph)

- margin: 16px 0
- padding: 0

## 强调 (Emphasis)

- strong-color: #667eea
- em-color: #764ba2
- highlight-background: linear-gradient(135deg, #667eea15, #764ba215)
- highlight-padding: 2px 6px
- highlight-border-radius: 4px

## 列表 (List)

- margin: 16px 0
- padding-left: 2em
- item-spacing: 6px

## 引用块 (Blockquote)

- margin: 20px 0
- padding: 16px 20px
- border-left: 4px solid
- border-image: linear-gradient(180deg, #667eea, #764ba2) 1
- background: #f5f5f7
- color: #1d1d1f
- font-size: 15px
- border-radius: 0 8px 8px 0

## 代码块 (Code Block)

- margin: 16px 0
- border-radius: 12px
- background: #1d1d1f
- font-size: 13px
- padding: 16px
- mac-decoration: true
- 默认代码主题: one-dark

## 行内代码 (Inline Code)

- background: #f5f5f7
- color: #667eea
- padding: 2px 8px
- border-radius: 6px
- font-size: 0.9em

## 表格 (Table)

- font-size: 14px
- header-background: #f5f5f7
- header-color: #1d1d1f
- border-color: #e8e8ed
- cell-padding: 10px 14px
- row-even-background: #fafafa

## 图片 (Image)

- border-radius: 12px
- caption-color: #86868b
- caption-font-size: 13px

## 水平线 (HR)

- background: linear-gradient(90deg, #667eea, #764ba2)
- height: 2px
- margin: 28px 0
- border-radius: 1px

## 脚注 (Footnote)

- color: #667eea
- separator-color: #e8e8ed
- font-size: 13px

## 链接 (Link)

- color: #667eea
- text-decoration: none
- border-bottom: 1px solid #667eea

---

## HTML 渲染模板

### 容器

```html
<section id="nice" style="max-width: 780px; margin: 0 auto; padding: 24px 28px; background: #ffffff; color: #1d1d1f; font-family: -apple-system, BlinkMacSystemFont, 'SF Pro Display', 'PingFang SC', sans-serif; font-size: 16px; line-height: 1.8; letter-spacing: 0.02em; word-break: break-word; overflow-wrap: break-word;">
```

### H2 标题（渐变左边框 + 浅色背景）

注意：微信不支持 `border-image`，降级为纯色。

```html
<!-- 微信版（降级纯色） -->
<h2 style="font-size: 24px; font-weight: 700; color: #1d1d1f; margin: 36px 0 16px; padding: 8px 16px; background: rgba(102, 126, 234, 0.04); border-left: 4px solid #667eea;">标题文本</h2>

<!-- 博客版（完整渐变） -->
<h2 style="font-size: 24px; font-weight: 700; color: #1d1d1f; margin: 36px 0 16px; padding: 8px 16px; background: linear-gradient(135deg, rgba(102,126,234,0.04), rgba(118,75,162,0.04)); border-left: 4px solid; border-image: linear-gradient(180deg, #667eea, #764ba2) 1;">标题文本</h2>
```

### H3 标题（紫蓝色文字）

```html
<h3 style="font-size: 18px; font-weight: 600; color: #667eea; margin: 24px 0 12px;">标题文本</h3>
```

### 段落

```html
<p style="margin: 16px 0; padding: 0; color: #1d1d1f; font-size: 16px; line-height: 1.8; letter-spacing: 0.02em;">段落文本</p>
```

### 粗体强调

```html
<strong style="color: #667eea; font-weight: bold;">粗体文本</strong>
```

### 引用块（渐变左边框）

```html
<!-- 微信版（降级纯色） -->
<blockquote style="margin: 20px 0; padding: 16px 20px; border-left: 4px solid #667eea; background: #f5f5f7; color: #1d1d1f; font-size: 15px; line-height: 1.8; border-radius: 0 8px 8px 0;">
  <p style="margin: 0; font-size: 15px;">引用内容</p>
</blockquote>
```

### 代码块（深色 + 大圆角 + macOS 装饰）

```html
<section style="margin: 16px 0; border-radius: 12px; overflow: hidden; background: #1d1d1f;">
  <section style="padding: 8px 16px; display: flex; align-items: center; gap: 6px; background: #161617;">
    <span style="width: 10px; height: 10px; border-radius: 50%; background: #ff5f57; display: inline-block;"></span>
    <span style="width: 10px; height: 10px; border-radius: 50%; background: #febc2e; display: inline-block;"></span>
    <span style="width: 10px; height: 10px; border-radius: 50%; background: #28c840; display: inline-block;"></span>
    <span style="flex: 1;"></span>
    <span style="font-size: 12px; color: #86868b; font-family: monospace;">语言</span>
  </section>
  <section style="padding: 12px 16px; overflow-x: auto; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 13px; line-height: 1.6; color: #cdd6f4;">
    代码内容
  </section>
</section>
```

### 行内代码

```html
<code style="background: #f5f5f7; color: #667eea; padding: 2px 8px; border-radius: 6px; font-family: 'Menlo', 'Monaco', monospace; font-size: 0.9em;">code</code>
```

### 水平线（渐变色线）

```html
<!-- 微信版（降级纯色） -->
<hr style="border: none; height: 2px; background: #667eea; margin: 28px 0; border-radius: 1px;">

<!-- 博客版（完整渐变） -->
<hr style="border: none; height: 2px; background: linear-gradient(90deg, #667eea, #764ba2); margin: 28px 0; border-radius: 1px;">
```
