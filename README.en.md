<div align="center">

# 🌙 LUNAR COLONY

**Build your colony on the Moon. Manage resources, research, and crew to survive.**

A single-file HTML pixel-art colony simulation game. **Zero dependencies, just open and play.**

[![CI](https://github.com/3289987054/lunar-colony/actions/workflows/ci.yml/badge.svg)](https://github.com/3289987054/lunar-colony/actions/workflows/ci.yml)
[![Deploy](https://github.com/3289987054/lunar-colony/actions/workflows/deploy.yml/badge.svg)](https://github.com/3289987054/lunar-colony/actions/workflows/deploy.yml)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-Single_File-orange.svg)](https://developer.mozilla.org/en-US/docs/Glossary/HTML5)
[![i18n](https://img.shields.io/badge/i18n-zh%20%7C%20en-blue.svg)](#-internationalization)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

🌐 [简体中文](./README.md) | **English**

</div>

---

## 🎮 Features

| System | Description |
|---|---|
| 🏗 **Building** | 17 building types: solar panels, oxygen generators, mines, greenhouses, labs, comm towers, lunar core, etc. |
| 📊 **Resources** | 7 resources to balance: energy, oxygen, mineral, food, credit, research, expiry points |
| 🔬 **Research** | 23-tech research tree driving progression |
| 👤 **Crew** | Recruit and assign crew members to buildings |
| 🎲 **Events** | 23 random events triggered via comm tower |
| 💪 **Morale** | Keep morale high or the colony collapses |
| ⏰ **Time** | Points start expiring from Day 5 — the pressure mounts |
| 🌐 **i18n** | Toggle between Chinese and English on the title screen |

## 🚀 Quick Start

### Option 1: Direct

Download `index.html` and open it in any browser. No installation required.

### Option 2: Live Demo

Visit [GitHub Pages](https://3289987054.github.io/lunar-colony/) (auto-deployed via GitHub Actions).

### Option 3: Local Server

```bash
python -m http.server 8000
# or
npx serve
# Open http://localhost:8000
```

## 🎯 Objective

**Build the Lunar Core and reach 20 crew.**

Sounds simple, but you must balance resources, handle random events, maintain morale, and race against the expiry mechanic.

## 🌐 Internationalization

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

## 🖥 Tech

- **Vanilla HTML/CSS/JavaScript** — zero dependencies, zero external resources
- **Canvas pixel rendering** — retro sci-fi FUI style
- **Single-file deployment** — `index.html` does everything
- **Mobile-friendly** — touch support, responsive layout
- **No backend** — fully client-side, no data collection

## 📥 Deploy

Drop `index.html` onto any static host:

- Nginx / Apache: drop into web root
- GitHub Pages: fork and enable Pages
- Vercel / Netlify / Cloudflare Pages: connect repo, auto-deploy
- Local: `python -m http.server`

### Embed

```html
<iframe src="path/to/index.html" width="440" height="800"
  style="border:none;overflow:hidden"></iframe>
```

## 🛠 Development

### Requirements

- Any modern browser (Chrome 90+ / Firefox 90+ / Safari 15+)
- Git
- A text editor (VS Code recommended)

### Local Dev

```bash
git clone https://github.com/3289987054/lunar-colony.git
cd lunar-colony
# Just open index.html in a browser
```

### Structure

```
lunar-colony/
├── index.html              # 🎮 Main game file (single-file, standalone)
├── README.md               # Chinese README
├── README.en.md            # This file
├── CHANGELOG.md            # Changelog
├── CONTRIBUTING.md         # Contributing guide
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── LICENSE                 # MIT
└── .github/
    ├── workflows/
    │   ├── ci.yml          # CI: HTML validation, size check
    │   └── deploy.yml      # GitHub Pages auto-deploy
    ├── ISSUE_TEMPLATE/
    ├── PULL_REQUEST_TEMPLATE.md
    └── FUNDING.yml
```

### Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md). Contributions welcome:

- 🐛 [Report Bug](../../issues/new?assignees=&labels=bug&template=bug_report.md)
- 💡 [Request Feature](../../issues/new?assignees=&labels=enhancement&template=feature_request.md)
- 💬 [Discuss](../../issues/new?assignees=&labels=discussion&template=discussion.md)
- 🔧 [Open a Pull Request](../../compare)

## 🗺 Roadmap

- [x] v0.1.0: Initial release
- [x] v0.2.0: Chinese-English i18n
- [ ] v0.3.0: Sound effects
- [ ] v0.4.0: Save import/export
- [ ] v0.5.0: Achievement expansion
- [ ] v0.6.0: More languages (日本語 / Español)
- [ ] v1.0.0: Full release

See [Issues](../../issues) with the `roadmap` label.

## 📄 License

[MIT License](LICENSE) © 2026 [3289987054](https://github.com/3289987054)

## 🙏 Acknowledgements

- Inspired by: SimCity, RimWorld, Oxygen Not Included
- Pixel art: FUI style paying homage to sci-fi movie HUDs
- All playtesters and feedback providers

---

<div align="center">

**If you like this project, please ⭐ Star it!**

[Report Bug](../../issues/new?assignees=&labels=bug&template=bug_report.md) · [Request Feature](../../issues/new?assignees=&labels=enhancement&template=feature_request.md) · [Discussions](../../issues)

</div>
