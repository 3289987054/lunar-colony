<div align="center">

# 🌙 月球基地 · LUNAR COLONY

**在月球上建立你的殖民地，管理资源、科研和船员，努力生存下去。**

*Build your colony on the Moon. Manage resources, research, and crew to survive.*

一个纯单文件 HTML 像素风殖民地建设模拟游戏。**零依赖，打开即玩。**

*A single-file HTML pixel-art colony simulation game. **Zero dependencies, just open and play.***

[![CI](https://github.com/3289987054/lunar-colony/actions/workflows/ci.yml/badge.svg)](https://github.com/3289987054/lunar-colony/actions/workflows/ci.yml)
[![Deploy](https://github.com/3289987054/lunar-colony/actions/workflows/deploy.yml/badge.svg)](https://github.com/3289987054/lunar-colony/actions/workflows/deploy.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-Single_File-orange.svg)](https://developer.mozilla.org/zh-CN/docs/Glossary/HTML5)
[![i18n](https://img.shields.io/badge/i18n-zh%20%7C%20en-blue.svg)](#-internationalization)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

🌐 **简体中文** | [English](./README.en.md)

</div>

---

<p align="center">
  <em>English</em><br>
  <img src="./docs/screenshots/game-en.png" alt="Lunar Colony English Screenshot" width="480">
</p>

<p align="center">
  <em>简体中文</em><br>
  <img src="./docs/screenshots/game-zh.png" alt="月球基地中文截图" width="480">
</p>

## 🎮 游戏特色 / Features

| 系统 | 描述 / Description |
|---|---|
| 🏗 **建造系统 / Building** | 太阳能板、制氧机、矿场、温室、实验室、通讯塔、月球核心等 17 种建筑 *17 building types: solar panels, oxygen generators, mines, greenhouses, labs, comm towers, lunar core, etc.* |
| 📊 **资源管理 / Resources** | 能源、氧气、矿物、食物、信用点、科研点、过期积分，7 大资源平衡发展 *7 resources to balance* |
| 🔬 **科研系统 / Research** | 23 项科技驱动的科技树 *23-tech research tree* |
| 👤 **船员管理 / Crew** | 招募和管理殖民地成员，分配工作岗位 *Recruit and assign crew to buildings* |
| 🎲 **随机事件 / Events** | 通讯塔触发 23 种事件，影响殖民地命运 *23 random events triggered via comm tower* |
| 💪 **士气系统 / Morale** | 保持船员士气，否则殖民地会崩溃 *Keep morale high or the colony collapses* |
| ⏰ **时间机制 / Time** | 第 5 天起积分开始过期，节奏越来越紧张 *Points start expiring from Day 5* |
| 🌐 **中英文切换 / i18n** | 标题画面一键切换 中文 / English *Toggle between Chinese and English on the title screen* |

## 🚀 快速开始 / Quick Start

### 方式一：直接打开 / Option 1: Direct

下载 `index.html`，双击用浏览器打开即可游玩。**无需安装任何东西。**

*Download `index.html` and open it in any browser. No installation required.*

### 方式二：在线 Demo / Option 2: Live Demo

访问 [GitHub Pages 在线 Demo](https://3289987054.github.io/lunar-colony/)（由 GitHub Actions 自动部署）。

*Visit [GitHub Pages](https://3289987054.github.io/lunar-colony/) (auto-deployed via GitHub Actions).*

### 方式三：本地服务器 / Option 3: Local Server

```bash
python -m http.server 8000
# 或 / or
npx serve
# 浏览器访问 / Open http://localhost:8000
```

## 🎯 游戏目标 / Objective

**建造月球核心，并拥有 20 名船员。**

听起来简单，但你需要在有限的资源下平衡发展、应对随机事件、维持士气，并在积分过期机制启动后加速推进。

*Build the Lunar Core and reach 20 crew. Sounds simple, but you must balance resources, handle random events, maintain morale, and race against the expiry mechanic.*

## 🌐 Internationalization / 国际化

The game supports **Chinese (default)** and **English**, toggleable from the title screen. Language preference is saved in `localStorage`.

- `T(zh)` — translate a Chinese string to the current language
- `TF('第%s日', 5)` — translate with `%s` placeholders
- 324 translation entries covering buildings, techs, resources, events, achievements, UI labels, and messages

To add a new language, extend the `I18N` object in `index.html`:

```javascript
const I18N = {
  lang: 'zh',          // 'zh' | 'en'
  en: { /* 324 entries */ },
  // ja: { ... }       // add your language here
};
```

## 🖥 技术特点 / Tech

- **纯原生 HTML/CSS/JavaScript**，零依赖，零外部资源 *Vanilla HTML/CSS/JS, zero dependencies*
- **Canvas 像素渲染**，复古科幻 FUI 风格 *Canvas pixel rendering, retro sci-fi FUI style*
- **单文件部署**，`index.html` 一个文件搞定一切 *Single-file deployment*
- **移动端适配**，支持触屏操作 *Mobile-friendly with touch support*
- **无后端**，所有逻辑在浏览器本地运行 *No backend, fully client-side*

## 📥 安装与部署 / Deploy

### 网页游戏部署 / Web Game

将 `index.html` 丢到任意静态服务器即可：

*Drop `index.html` onto any static host:*

- Nginx / Apache：直接放到 web root
- GitHub Pages：Fork 本仓库，启用 Pages *Fork and enable Pages*
- Vercel / Netlify / Cloudflare Pages：连接仓库自动部署
- 本地：`python -m http.server`

### 嵌入到其他页面 / Embed

```html
<iframe src="path/to/index.html" width="440" height="800"
  style="border:none;overflow:hidden"></iframe>
```

## 🛠 开发 / Development

### 环境要求 / Requirements

- 任意现代浏览器（Chrome 90+ / Firefox 90+ / Safari 15+）
- Git
- 文本编辑器（VS Code 推荐）

### 本地开发 / Local Dev

```bash
git clone https://github.com/3289987054/lunar-colony.git
cd lunar-colony
# 直接用浏览器打开 index.html 即可 / Just open index.html in a browser
```

### 项目结构 / Structure

```
lunar-colony/
├── index.html              # 🎮 游戏主文件（单文件，可独立运行）/ Main game file
├── README.md               # 项目说明（中文）/ This file
├── README.en.md            # English README
├── CHANGELOG.md            # 版本变更记录 / Changelog
├── CONTRIBUTING.md         # 贡献指南 / Contributing guide
├── CODE_OF_CONDUCT.md      # 行为准则
├── SECURITY.md             # 安全策略
├── LICENSE                 # MIT 许可证
└── .github/
    ├── workflows/
    │   ├── ci.yml          # CI：HTML 验证、大小检查
    │   └── deploy.yml      # GitHub Pages 自动部署
    ├── ISSUE_TEMPLATE/     # Issue 模板
    ├── PULL_REQUEST_TEMPLATE.md
    └── FUNDING.yml
```

### 提交贡献 / Contributing

请阅读 [CONTRIBUTING.md](CONTRIBUTING.md)。欢迎任何形式的贡献：

- 🐛 [报告 Bug / Report Bug](../../issues/new?assignees=&labels=bug&template=bug_report.md)
- 💡 [提出功能建议 / Request Feature](../../issues/new?assignees=&labels=enhancement&template=feature_request.md)
- 💬 [参与讨论 / Discuss](../../issues/new?assignees=&labels=discussion&template=discussion.md)
- 🔧 [提交 Pull Request](../../compare)

## 🗺 Roadmap

- [x] v0.1.0：初始发布 / Initial release
- [x] v0.2.0：中英文切换 / Chinese-English i18n
- [ ] v0.3.0：音效系统 / Sound effects
- [ ] v0.4.0：存档导入 / 导出 / Save import/export
- [ ] v0.5.0：成就系统扩展 / Achievement expansion
- [ ] v0.6.0：更多语言（日本語 / Español）/ More languages
- [ ] v1.0.0：完整版发布 / Full release

详见 [Issues](../../issues) 中的 `roadmap` 标签。

## 📄 许可证 / License

[MIT License](LICENSE) © 2026 [3289987054](https://github.com/3289987054)

## 🙏 致谢 / Acknowledgements

- 灵感来源：SimCity、RimWorld、Oxygen Not Included
- 像素美术：FUI 风格致敬科幻电影 HUD
- 所有测试与反馈的玩家

---

<div align="center">

**如果这个项目对你有帮助，欢迎 ⭐ Star 支持！**

*If you like this project, please ⭐ Star it!*

[Report Bug](../../issues/new?assignees=&labels=bug&template=bug_report.md) · [Request Feature](../../issues/new?assignees=&labels=enhancement&template=feature_request.md) · [Discussions](../../issues)

</div>
