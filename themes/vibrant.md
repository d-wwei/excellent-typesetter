# Theme: Vibrant (活力)

活力、绿色调、视觉丰富。适合公众号品牌文/营销/运营类文章。灵感来源: wechat-article-formatter green-simple + mdnice 活泼主题。

## 容器 (Container)

- max-width: 780px
- padding: 20px 24px
- background: #ffffff
- margin: 0 auto

## 文字 (Text)

- color: #595959
- secondary-color: #888888
- font-family: 'Optima', -apple-system, 'PingFang SC', 'Microsoft YaHei', sans-serif
- font-size: 15px
- line-height: 1.8
- letter-spacing: 0.04em

## 标题 (Headings)

### H1 (仅博客平台)
- font-size: 24px
- font-weight: 700
- color: #35b378
- text-align: center
- margin: 36px 0 24px

### H2
- font-size: 18px
- font-weight: 700
- color: #ffffff
- margin: 28px 0 16px
- padding: 4px 14px
- background: #333333
- display: inline-block
- border-radius: 4px
- prefix-style: display: none;
- content-style: ;
- suffix-style: display: none;

### H3
- font-size: 20px
- font-weight: 700
- color: #35b378
- margin: 24px 0 12px
- padding: 0

### H4
- font-size: 16px
- font-weight: 700
- color: #595959
- margin: 20px 0 10px

## 段落 (Paragraph)

- margin: 16px 0
- padding: 0

## 强调 (Emphasis)

- strong-color: #35b378
- em-color: #35b378
- highlight-background: #e6f9f0
- highlight-padding: 2px 6px
- highlight-border-radius: 4px

## 列表 (List)

- margin: 16px 0
- padding-left: 2em
- item-spacing: 6px

## 引用块 (Blockquote)

- margin: 16px 0
- padding: 12px 16px
- border-left: 4px solid #35b378
- background: #fbf9fd
- color: #595959
- font-size: 15px
- border-radius: 0 4px 4px 0

## 代码块 (Code Block)

- margin: 16px 0
- border-radius: 8px
- background: #282c34
- font-size: 12px
- padding: 16px
- mac-decoration: true
- 默认代码主题: one-dark

## 行内代码 (Inline Code)

- background: rgba(27, 31, 35, 0.05)
- color: rgba(30, 107, 184, 1)
- padding: 2px 6px
- border-radius: 4px
- font-size: 0.9em

## 表格 (Table)

- font-size: 14px
- header-background: #35b378
- header-color: #ffffff
- border-color: #e1e4e8
- cell-padding: 8px 12px
- row-even-background: #f8f8f8

## 图片 (Image)

- border-radius: 4px
- caption-color: #888888
- caption-font-size: 13px

## 水平线 (HR)

- color: #35b378
- margin: 24px 0
- opacity: 0.3

## 脚注 (Footnote)

- color: #35b378
- separator-color: #e1e4e8
- font-size: 13px

## 链接 (Link)

- color: #35b378
- text-decoration: none
- font-weight: bold
- border-bottom: 1px solid #35b378

---

## HTML 渲染模板

### 容器

```html
<section id="nice" style="max-width: 780px; margin: 0 auto; padding: 20px 24px; background: #ffffff; color: #595959; font-family: 'Optima', -apple-system, 'PingFang SC', 'Microsoft YaHei', sans-serif; font-size: 15px; line-height: 1.8; letter-spacing: 0.04em; word-break: break-word; overflow-wrap: break-word;">
```

### TL;DR / 摘要高亮

```html
<p style="margin: 16px 0; padding: 10px 16px; background: #e6f9f0; border-radius: 6px; border-left: 3px solid #35b378; color: #595959; font-size: 15px; line-height: 1.8;"><strong style="color: #35b378; font-weight: bold;">TL;DR</strong>：摘要内容</p>
```

### H2 标题（黑底白字标签）

```html
<h2 style="font-size: 18px; font-weight: 700; color: #ffffff; margin: 28px 0 16px; padding: 4px 14px; background: #333333; display: inline-block; border-radius: 4px;">标题文本</h2>
```

### H3 标题（绿色文字）

```html
<h3 style="font-size: 20px; font-weight: 700; color: #35b378; margin: 24px 0 12px; padding: 0;">标题文本</h3>
```

### 段落

```html
<p style="margin: 16px 0; padding: 0; color: #595959; font-size: 15px; line-height: 1.8; letter-spacing: 0.04em;">段落文本</p>
```

### 粗体强调

```html
<strong style="color: #35b378; font-weight: bold;">粗体文本</strong>
```

### 引用块（绿色边框 + 浅紫背景）

```html
<blockquote style="margin: 16px 0; padding: 12px 16px; border-left: 4px solid #35b378; background: #fbf9fd; color: #595959; font-size: 15px; line-height: 1.8; border-radius: 0 4px 4px 0;">
  <p style="margin: 0; font-size: 15px;">引用内容</p>
</blockquote>
```

### 无序列表

```html
<ul style="margin: 16px 0; padding-left: 2em;">
  <li style="margin-bottom: 6px;"><section style="color: #595959; font-size: 15px; line-height: 1.8;">列表项内容</section></li>
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
  <section style="padding: 12px 16px; overflow-x: auto; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 12px; line-height: 1.6; color: #abb2bf;">
    代码内容（One Dark 配色）
  </section>
</section>
```

### 行内代码

```html
<code style="background: rgba(27, 31, 35, 0.05); color: rgba(30, 107, 184, 1); padding: 2px 6px; border-radius: 4px; font-family: 'Menlo', 'Monaco', 'Consolas', monospace; font-size: 0.9em;">code</code>
```

### 水平线

```html
<hr style="border: none; height: 1px; background: #35b378; margin: 24px 0; transform: scale(1, 0.5); opacity: 0.3;">
```
