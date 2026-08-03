# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Planned
- 音效系统 / Sound effects
- 存档导入/导出 / Save import/export
- 成就系统扩展 / Achievement expansion
- 移动端手势优化 / Mobile gesture optimization
- 更多语言（日本語 / Español）/ More languages

## [0.2.0] - 2026-08-03

### Added
- 🌐 **中英文切换 / Chinese-English i18n**
  - Global `I18N` module with 324 translation entries (zh/en)
  - `T()` and `TF()` translation functions with `%s` placeholder support
  - Language toggle button on title screen
  - Language preference persisted in `localStorage`
  - Refactored `drawEventIcon` to use `ev.icon` field instead of title text

### Changed
- README 双语化 / Bilingual README (zh + en)
- 仓库 topics 增加 `i18n`, `localization`, `html5-game`, `single-file`
- 设置 GitHub Pages homepage URL

### Translated
- 16 building names/descriptions
- 23 tech names/descriptions
- 7 resource names
- 23 event titles/descriptions (+ new `ev.icon` field)
- 15 achievement names
- Crew names (commander + Greek letters)
- 18 toast messages, 22 floatText calls
- UI buttons, menu sections, win/lose panels, title screen

## [0.1.0] - 2026-08-01

### Added
- 🌙 初始版本发布 / Initial release
- 单文件 HTML 像素风月球殖民地建设模拟游戏 / Single-file HTML pixel-art colony simulation
- 六大资源系统：能源、氧气、矿物、食物、信用点、科研点 / 6 resources
- 建造系统：17 种建筑 / 17 building types
- 科研系统：23 项科技 / 23-tech research tree
- 船员管理：招募、分配工作岗位 / Crew management
- 随机事件系统：23 种事件 / 23 random events
- 士气系统 / Morale system
- 时间机制：第 5 天起积分开始过期 / Expiry mechanic from Day 5
- Canvas 像素渲染，复古科幻 FUI 风格 / Canvas pixel rendering, retro FUI
- 移动端适配，支持触屏操作 / Mobile-friendly, touch support
- MIT 许可证 / MIT license
