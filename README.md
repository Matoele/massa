# Massa - Professional Brewing & Extraction Equipment

This is the official website for Massa, a leading manufacturer and supplier of high-quality brewing and extraction equipment for commercial use.

## Features

- Responsive design for optimal viewing on all devices
- Modern and professional interface
- Detailed product information for commercial clients
- Contact form for business inquiries

## Products

- Craft Beer Brewing Equipment
- Cold Brew Coffee Equipment
- Cold Water Extraction Systems

## Development

This website is built with:
- HTML5
- CSS3
- JavaScript (vanilla)
- Font Awesome for icons

## Getting Started

1. Clone this repository
2. Open `index.html` in your browser
3. No build process required - pure HTML, CSS, and JavaScript

## License

All rights reserved. This website is for demonstration purposes.

# Massa 公司网站多语言功能实现文档

## 项目概述

Massa 是一家专业的醸造和提取设备制造商，提供工艺啤酒醸造系统、冷萃咖啡设备和冷水提取系统。本项目实现了 Massa 公司网站的多语言功能，支持英文（默认）、日语和韩语三种语言版本。

## 多语言实现方式

本项目采用基于目录结构的多语言实现方案，而非动态切换内容的方式。这种实现方式有以下优点：

1. **SEO 友好**：每种语言有独立的 URL，有利于搜索引擎索引
2. **性能更佳**：无需 JavaScript 动态加载内容，页面加载更快
3. **用户体验更好**：用户可以直接保存或分享特定语言版本的链接
4. **实现简单**：不需要复杂的翻译系统或数据库支持

## 目录结构

```
/                       # 根目录（英文版本）
├── index.html          # 英文首页
├── pages/              # 英文页面目录
│   ├── about.html      # 关于我们
│   ├── products.html   # 产品
│   ├── process.html    # 工艺流程
│   └── contact.html    # 联系我们
├── lang/               # 其他语言版本
│   ├── ja/             # 日语版本
│   │   ├── index.html  # 日语首页
│   │   ├── about.html  # 关于我们（日语）
│   │   ├── products.html # 产品（日语）
│   │   ├── process.html # 工艺流程（日语）
│   │   └── contact.html # 联系我们（日语）
│   └── ko/             # 韩语版本
│       ├── index.html  # 韩语首页
│       ├── about.html  # 关于我们（韩语）
│       ├── products.html # 产品（韩语）
│       ├── process.html # 工艺流程（韩语）
│       └── contact.html # 联系我们（韩语）
├── images/             # 图片资源（所有语言共用）
└── styles.css          # 样式表（所有语言共用）
```

## 语言切换实现

每个页面的导航栏中都包含一个语言切换下拉菜单，用户可以通过点击切换到对应的语言版本。

### 导航栏语言切换组件

```html
<li class="language-selector">
    <a href="#"><i class="fas fa-globe"></i> EN <i class="fas fa-chevron-down"></i></a>
    <ul class="language-dropdown">
        <li><a href="../../index.html" data-lang="en">English</a></li>
        <li><a href="../ja/index.html" data-lang="ja">日本語</a></li>
        <li><a href="../ko/index.html" data-lang="ko">한국어</a></li>
    </ul>
</li>
```

每个语言版本显示不同的语言标识：
- 英文版：EN
- 日语版：JP
- 韩语版：KR

### 链接路径处理

为确保语言切换正确，每个页面中的语言切换链接都需要根据当前页面的位置进行相应调整：

1. **英文版页面**（根目录）：
   - 英文链接指向 `index.html` 或相应页面
   - 日语链接指向 `lang/ja/index.html` 或相应页面
   - 韩语链接指向 `lang/ko/index.html` 或相应页面

2. **日语/韩语版页面**（lang 目录下）：
   - 英文链接指向 `../../index.html` 或相应页面
   - 日语链接指向 `../ja/index.html` 或相应页面
   - 韩语链接指向 `../ko/index.html` 或相应页面

## 多语言 SEO 优化

每个语言版本的页面都包含适当的 SEO 元标签：

1. **语言标记**：每个页面都通过 `<html lang="xx">` 标签明确指定页面语言
   ```html
   <html lang="en"> <!-- 英文 -->
   <html lang="ja"> <!-- 日语 -->
   <html lang="ko"> <!-- 韩语 -->
   ```

2. **元描述**：每个页面都有对应语言的元描述
   ```html
   <meta name="description" content="..."> <!-- 根据语言提供不同的描述 -->
   ```

3. **页面标题**：每个页面都有对应语言的标题
   ```html
   <title>Products - Massa</title> <!-- 英文 -->
   <title>製品 - Massa</title> <!-- 日语 -->
   <title>제품 - Massa</title> <!-- 韩语 -->
   ```

## 共享资源

为了提高网站性能和维护效率，所有语言版本共享以下资源：

1. **样式表**：`styles.css`
2. **图片资源**：`images/` 目录下的所有图片
3. **外部库**：如 Font Awesome 图标库

## 页面内容翻译

所有页面内容（包括导航菜单、页面标题、正文内容和按钮文本）都已翻译成对应的语言。每个语言版本保持相同的页面结构和功能，但使用该语言的文本内容。

## 维护建议

1. **添加新页面**：添加新页面时，需要在所有语言版本中创建对应的页面
2. **更新内容**：更新内容时，需要同步更新所有语言版本
3. **添加新语言**：添加新语言时，需要在 `lang/` 目录下创建新的语言子目录，并复制所有页面进行翻译
4. **更新共享资源**：更新共享资源（如样式表或图片）时，所有语言版本会自动使用更新后的资源

## 测试

在发布前，建议测试以下功能：

1. **语言切换**：确保所有页面的语言切换功能正常工作
2. **链接正确性**：确保所有内部链接在不同语言版本间正确指向
3. **响应式设计**：确保所有语言版本在不同设备上都能正常显示
4. **内容完整性**：确保所有内容都已正确翻译，没有遗漏 