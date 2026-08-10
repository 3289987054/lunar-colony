# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.4.0] - 2026-08-05

### Fixed
- 🐛 **Bug 修复 / Bug fixes**
  - `C.accent` 未定义错误 → 改用 `C.yellow`（选中建筑高亮）
  - 成就计数 `/8` → `/15`（与实际 15 个成就一致）
  - `demolish()` 中 `Sound.demolish()` 调用位置修正（移到 `b` 存在检查之后）
  - 积分过期提示 `第5天` → `第15天`（中英文同步修正）

### Added
- 📊 Game Over 面板增加事件次数统计 / Event count in Game Over panel
- 💀 Game Over 图标改为像素骷髅头 / Pixel skull icon on Game Over
- ⌨️ 键盘快捷键 / Keyboard shortcuts: `Esc` 取消/关闭，`0/1/3/5` 切换速度
- 🏗️ 建造菜单显示已建数量 / Building count (×N) in build menu
- ⏱️ 菜单状态行增加游玩时间统计 / Play time in menu status
- 💧 菜单资源动态加入水循环站氧气节省逻辑 / Water recycler O₂ savings in resource panel

### Changed
- 🔄 事件贸易弹窗从 4 种扩展为 6 种方案，接入 `tradeMult` 科技加成
- 🕗 过期积分在第 15 天前隐藏 / Expiry score hidden before Day 15
- 🌐 胜利面板 / 积分过期警告国际化 / Win panel & expiry warning i18n
- 📝 i18n 补充缺失翻译条目 / Fill in missing translation entries

## [0.4.1] - 2026-08-06

### Changed
- 🌐 **i18n 翻译完善 / Improved English translations**
  - 新增 23 条翻译条目（UI 文案、引导提示、状态行等）
  - 音效开关 `开启/关闭` → `ON/OFF`（英文模式更地道）
  - 补充带前导空格的字符串翻译（事件描述、状态提示）
  - 补充产量/消耗/船员/建筑/科技/事件等状态行翻译
  - 补充新游戏引导提示、放置建筑提示翻译

## [0.4.2] - 2026-08-07

### Fixed
- 🐛 **语言切换后无需刷新 / No page refresh needed after language switch**
  - `setLang()` 现在自动检测并刷新打开的面板（建造/科研/船员/菜单/贸易）
  - 选中建筑时切换语言也会实时刷新 `showSelInfo`
  - `BDEF`/`RDEF` 的 `name`/`desc` 移除初始化时的 `T()` 包裹
    改为裸字符串，避免字典加载前翻译失败
  - 修复语言切换后部分文本不更新的问题

## [0.4.3] - 2026-08-08

### Fixed
- 🐛 **事件图标修复 / Event Icon Bug Fix**
  - 23 个事件全部缺少 `icon` 属性，导致 `drawEventIcon` 始终走 else 分支画黄色方块
  - 给每个事件添加了对应的 `icon` 类型（meteor/ice/solar/trade/immigrant/failure/research 等）

### Changed
- 🎨 **drawEventIcon 代码清理**
  - 229 行重复分支压缩为 80 行（ice×2、research×5、failure×4 等重复定义合并）
  - 每个 icon 保留一个定义，新增 13 个缺失的 icon 分支

### Added
- 🚀 **2 个新事件（25 种）**
  - 太空垃圾：废弃卫星坠落，回收获得矿物+能量
  - 流浪者：流浪宇航员请求加入（需有居住舱空位）
- 🏗 **新建筑 + 新科技**
  - 太空港（第 18 种建筑）：每 60 秒自动空投随机资源
  - 含像素绘图：发射台、控制塔、跑道、浮动火箭+火焰
  - 太空港建设（第 25 项科技）：解锁太空港建造

## [0.4.4] - 2026-08-09

### Added
- 🏗️ **建造菜单分类 / Build Menu Categories**
  - 18 种建筑分为「基础/高级/终极」三组，带分类标题
  - 资源不足时红色标注具体缺什么资源
- ☀️ **白天/夜晚指示 / Day-Night Indicator**
  - 时间后面加太阳/月亮图标，一眼看出太阳能板是否工作
- 👤 **招募船员预览 / Crew Recruit Preview**
  - 招募按钮下方显示下一个船员的名字和四维属性
  - 预览值即实际招募值，不再盲抽
- 🏆 **新成就：太空枢纽 / New Achievement: Space Hub**
  - 建造太空港解锁，成就总数 15→16
- 📋 **事件日志 / Event Log**
  - 菜单新增事件日志面板，显示最近 8 条事件（✅/❌ + 日期 + 标题）

### Changed
- 💰 **资源不足具体提示 / Specific Resource Shortage Hint**
  - 建造时资源不足从"资源不足！"改为"资源不足！(矿物不足)"等具体提示

## [0.4.5] - 2026-08-10

### Added
- 📊 **资源栏净产量箭头 / Net Production Arrows**
  - 顶部每个资源后显示 ▲▼· 箭头，绿/红/灰三色
  - 一眼看出哪些资源在增长、哪些在消耗
- ⏩ **速度切换 toast 提示 / Speed Toggle Toast**
  - 点击暂停/1x/3x/5x 时弹出当前速度提示

### Changed
- ♻️ **代码去重 / Code Dedup**
  - 新增 `calcRates()` 统一计算函数
  - 菜单"资源动态"面板复用同一函数（去重约 30 行代码）

## [Unreleased]

### Planned
- 存档导入/导出 / Save import/export
- 成就系统扩展 / Achievement expansion
- 移动端手势优化 / Mobile gesture optimization
- 更多语言（日本語 / Español）/ More languages

## [0.3.0] - 2026-08-04

### Added
- 🔊 **音效系统增强 / Enhanced Sound System**
  - Master volume control via WebAudio GainNode, persisted to `localStorage`
  - Ambient background music: dual-oscillator drone with LFO-modulated lowpass filter
    and randomized chime notes every 9 seconds
  - 7 new sound effects: `demolish`, `recruit`, `research`, `trade`, `achieve`, `warning`, `levelup`
  - Refactored audio panel in menu: sound toggle, volume slider, music toggle, test button
  - BGM auto-starts on new game if `musicOn=true`
  - Added i18n entries: 音量/Volume, 背景音乐/Music, 测试/Test

### Changed
- Achievement unlock now plays `Sound.achieve()` instead of generic `success()`
- Research completion now plays `Sound.research()` instead of generic `success()`
- Recruit now plays `Sound.recruit()` instead of generic `success()`
- Demolish now plays `Sound.demolish()`
- `loadGame()` restores volume/music preferences from `localStorage`

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
