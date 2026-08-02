<div align="center">

# 🌙 月球基地 · LUNAR COLONY

**在月球上建立你的殖民地，管理资源、科研和船员，努力生存下去。**

一个纯单文件 HTML 像素风殖民地建设模拟游戏。**零依赖，打开即玩。**

[![CI](https://github.com/3289987054/lunar-colony/actions/workflows/ci.yml/badge.svg)](https://github.com/3289987054/lunar-colony/actions/workflows/ci.yml)
[![Deploy](https://github.com/3289987054/lunar-colony/actions/workflows/deploy.yml/badge.svg)](https://github.com/3289987054/lunar-colony/actions/workflows/deploy.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-Single_File-orange.svg)](https://developer.mozilla.org/zh-CN/docs/Glossary/HTML5)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

</div>

---

## 🎮 游戏特色

| 系统 | 描述 |
|---|---|
| 🏗 **建造系统** | 太阳能板、制氧机、矿场、温室、实验室、通讯塔、月球核心等多种建筑 |
| 📊 **资源管理** | 能源、氧气、矿物、食物、信用点、科研点，六大资源平衡发展 |
| 🔬 **科研系统** | 解锁更高级的建筑和能力，科技树驱动发展 |
| 👤 **船员管理** | 招募和管理殖民地成员，分配工作岗位 |
| 🎲 **随机事件** | 通讯塔触发事件，影响殖民地命运 |
| 💪 **士气系统** | 保持船员士气，否则殖民地会崩溃 |
| ⏰ **时间机制** | 第 15 天起积分开始过期，节奏越来越紧张 |

## 🚀 快速开始

### 方式一：直接打开（最简单）

下载 `index.html`，双击用浏览器打开即可游玩。**无需安装任何东西。**

### 方式二：在线 Demo

访问 [GitHub Pages 在线 Demo](https://3289987054.github.io/lunar-colony/)（由 GitHub Actions 自动部署）。

### 方式三：本地服务器

```bash
# Python
python -m http.server 8000

# Node.js
npx serve

# 然后浏览器访问 http://localhost:8000
```

## 🎯 游戏目标

**建造月球核心，并拥有 20 名船员。**

听起来简单，但你需要在有限的资源下平衡发展、应对随机事件、维持士气，并在积分过期机制启动后加速推进。

## 🖥 技术特点

- **纯原生 HTML/CSS/JavaScript**，零依赖，零外部资源
- **Canvas 像素渲染**，复古科幻 FUI（Fictional UI）风格
- **单文件部署**，`index.html` 一个文件搞定一切，适合嵌入任何平台
- **移动端适配**，支持触屏操作，响应式布局
- **无后端**，所有逻辑在浏览器本地运行，无数据收集

## 📸 截图

> 游戏画面将在 GitHub Pages 上展示

| 标题画面 | 游戏主界面 |
|---|---|
| 待补充 | 待补充 |

## 📥 安装与部署

### 作为网页游戏部署

将 `index.html` 丢到任意静态服务器即可：

- Nginx / Apache：直接放到 web root
- GitHub Pages：Fork 本仓库，启用 Pages
- Vercel / Netlify / Cloudflare Pages：连接仓库自动部署
- 内网穿透：直接用 `python -m http.server`

### 嵌入到其他页面

```html
<iframe src="path/to/index.html" width="440" height="800"
  style="border:none;overflow:hidden"></iframe>
```

## 🛠 开发

### 环境要求

- 任意现代浏览器（Chrome 90+ / Firefox 90+ / Safari 15+）
- Git（版本控制）
- 文本编辑器（VS Code 推荐）

### 本地开发

```bash
git clone https://github.com/3289987054/lunar-colony.git
cd lunar-colony
# 直接用浏览器打开 index.html 即可
```

### 项目结构

```
lunar-colony/
├── index.html              # 🎮 游戏主文件（单文件，可独立运行）
├── README.md               # 项目说明
├── CHANGELOG.md            # 版本变更记录
├── CONTRIBUTING.md         # 贡献指南
├── CODE_OF_CONDUCT.md      # 行为准则
├── SECURITY.md             # 安全策略
├── LICENSE                 # MIT 许可证
└── .github/
    ├── workflows/
    │   ├── ci.yml          # CI：HTML 验证、大小检查
    │   └── deploy.yml      # GitHub Pages 自动部署
    ├── ISSUE_TEMPLATE/     # Issue 模板
    ├── PULL_REQUEST_TEMPLATE.md
    └── FUNDING.yml         # 赞助信息
```

### 提交贡献

请阅读 [CONTRIBUTING.md](CONTRIBUTING.md)。欢迎任何形式的贡献：

- 🐛 [报告 Bug](../../issues/new?assignees=&labels=bug&template=bug_report.md)
- 💡 [提出功能建议](../../issues/new?assignees=&labels=enhancement&template=feature_request.md)
- 💬 [参与讨论](../../issues/new?assignees=&labels=discussion&template=discussion.md)
- 🔧 [提交 Pull Request](../../compare)

## 🗺 Roadmap

- [ ] v0.2.0：音效系统
- [ ] v0.3.0：多语言支持（English / 日本語）
- [ ] v0.4.0：存档导入 / 导出
- [ ] v0.5.0：成就系统扩展
- [ ] v0.6.0：移动端手势优化
- [ ] v1.0.0：完整版发布

详见 [Issues](../../issues) 中的 `roadmap` 标签。

## 📄 许可证

[MIT License](LICENSE) © 2026 [3289987054](https://github.com/3289987054)

## 🙏 致谢

- 灵感来源：SimCity、RimWorld、Oxygen Not Included
- 像素美术：FUI 风格致敬科幻电影 HUD
- 所有测试与反馈的玩家

---

<div align="center">

**如果这个项目对你有帮助，欢迎 ⭐ Star 支持！**

[Report Bug](../../issues/new?assignees=&labels=bug&template=bug_report.md) · [Request Feature](../../issues/new?assignees=&labels=enhancement&template=feature_request.md) · [Discussions](../../issues)

</div>
