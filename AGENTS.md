# 开发者指南 - socgerlia 个人作品集网站

## 项目概述
静态 HTML/CSS 个人作品集网站，无需构建工具。

## 命令
- **查看站点**: 在浏览器中打开 `index.html` 或使用 live server 扩展
- **无 lint/测试命令** - 纯静态文件，无框架依赖

## 文件结构
```
www/
├── index.html   # 主 HTML 页面
└── style.css    # 暗色系游戏主题样式表
```

## 代码风格指南

### HTML (index.html)
- 使用语义化 HTML5 元素 (`<header>`, `<nav>`, `<section>`, `<article>`, `<footer>`)
- 遵循 BEM-like 命名规范：`block__element--modifier`（如 `.game-card.featured`）
- 各区块用注释标记分隔：`<!-- =====Section====== -->`
- 使用 data 属性存储动态内容 (`data-label="游戏作品"`)
- img 标签正确自闭合

### CSS (style.css)
- 按区块组织，用清晰注释分隔代码块
- 适当使用 CSS 自定义属性进行主题定制
- 移动端优先的响应式设计，`@media` 查询放在文件末尾
- 交互元素添加过渡效果 (`:hover`, `.game-card:hover`)
- 卡片交互添加阴影和变换动画

### 命名规范
- ID：`#g-header`, `#hero`, `#games`, `#about`, `#contact`, `#footer`
- 类名：`.inner`, `.logo-area`, `.main-nav`, `.game-grid`, `.game-card`, `.card-content`
- 整个项目保持一致性和描述性

### 设计模式
- 暗色系主题配渐变背景 (`linear-gradient(135deg, #1a1a2e...)`)
- 强调色：`#e74c3c` (红色), `#e67e22` (橙色) 用于高亮
- 毛玻璃效果：`backdrop-filter: blur()`, 半透明背景
- 响应式卡片布局使用网格系统

### 最佳实践
- CSS Reset 放在样式表顶部
- box-sizing reset: `* { box-sizing: border-box; }`
- 使用系统字体栈提升性能
- viewport meta 标签确保移动端适配
- 可访问性：语义化结构，图片添加 alt 文本

## 现有 Cursor/Copilot 规则
仓库中未检测到。
