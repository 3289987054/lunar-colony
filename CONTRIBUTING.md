# Contributing to LUNAR COLONY

首先，感谢你愿意为 LUNAR COLONY 贡献力量！🎉

本项目欢迎任何形式的贡献：Bug 报告、功能建议、代码优化、文档改进、美术资源等。

## 📋 贡献流程

### 报告 Bug

1. 在 [Issues](../../issues) 页面搜索是否已有相同问题
2. 如未找到，点击 **New Issue** 创建新 Issue
3. 使用 Bug 报告模板，填写以下信息：
   - 操作系统与浏览器版本
   - 复现步骤
   - 预期行为与实际行为
   - 如有，附上截图或控制台日志

### 提交功能建议

1. 在 [Issues](../../issues) 页面创建新 Issue
2. 选择 **Feature request** 模板
3. 描述功能使用场景、期望效果、替代方案

### 提交代码

1. **Fork** 本仓库
2. 创建特性分支：
   ```bash
   git checkout -b feat/your-feature-name
   ```
3. 编写代码，确保：
   - 保持单文件 HTML 的核心特色（`index.html` 必须可独立运行）
   - 不引入外部依赖（CDN、npm 包等）
   - 代码风格与现有代码保持一致
   - 如新增功能，同步更新 `README.md` 和 `CHANGELOG.md`
4. 提交 commit，使用规范化的提交信息：
   ```
   feat: 添加音效系统
   fix: 修复士气计算溢出问题
   docs: 更新 README 截图
   refactor: 重构资源生成逻辑
   ```
5. 推送到你的 Fork，提交 **Pull Request**
6. 在 PR 描述中关联相关 Issue（如 `Closes #12`）

## 🎮 项目特色与约束

LUNAR COLONY 的核心定位是 **单文件 HTML 游戏**：

- `index.html` 必须能脱离服务器、无依赖地独立运行
- 所有 HTML/CSS/JavaScript 都内联在 `index.html` 中
- 不依赖任何外部资源（字体、图片、脚本、CDN）
- 部署门槛极低：双击文件即玩，或丢到任意静态服务器

如果你要新增功能，请优先考虑：
- 能否用原生 HTML/CSS/JS 实现？
- 是否破坏单文件可玩性？
- 在移动端是否可用？

## 🎨 代码风格

- HTML：4 空格缩进
- CSS：BEM-ish 命名，CSS 变量统一在 `:root` 定义
- JavaScript：
  - 使用 ES6+ 语法
  - 函数名使用 camelCase
  - 常量使用 UPPER_SNAKE_CASE
  - 注释使用中文，关键算法必须注释说明

## ✅ PR 检查清单

提交 PR 前请确认：

- [ ] `index.html` 可双击独立运行
- [ ] 在 Chrome / Firefox / Safari 最新版均测试通过
- [ ] 移动端 viewport 下无明显布局错乱
- [ ] 如修改了游戏数值，在 CHANGELOG 中说明
- [ ] commit 信息符合规范
- [ ] 关联了相关 Issue

## 🌿 分支模型

- `main`：稳定版本，只接受通过 PR 合并的代码
- `feat/*`：新功能开发
- `fix/*`：Bug 修复
- `docs/*`：文档更新
- `refactor/*`：代码重构

## 📄 许可证

提交的代码将遵循 [MIT License](LICENSE)。
