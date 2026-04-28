# 华容道（Klotski）单文件演示

简体中文说明 — 基于 Vue 3（CDN）、Tailwind 与 SweetAlert2 的单文件静态小游戏。

## 项目简介
- 名称：华容道（Klotski）单文件演示
- 说明：一个无需构建工具的单文件网页游戏，所有逻辑集中在 `index.html`，通过浏览器 localStorage 保存游戏记录（键：`klotski_history_v1`）。

## 主要功能
- 单按钮控制：开始 / 暂停 / 继续（计时从点击“开始”后启动）。
- 独立重置按钮：立即还原初始棋盘并停止计时。
- 完成后自动存档：保存用时、步数与本地化时间字符串。
- 历史面板：滑出样式，展示最近 10 条记录与前三名高亮。

## 快速启动
1. 直接打开：在文件管理器双击 `index.html`（适合快速本地调试）。
2. 推荐（使用轻量服务器）：在项目目录运行以下命令并在浏览器打开对应地址：

```bash
# Node 环境（推荐）
npx http-server . -c-1 -p 8080

# Python 3（备用）
python -m http.server 8000
```

访问：`http://localhost:8080` 或 `http://localhost:8000`

## 使用说明
- 开始：加载页面后点击“开始”按钮，计时开始。
- 暂停 / 继续：再次点击同一按钮可暂停或继续计时。
- 移动方块：点击可移动方块进行操作。
- 重置：点击“重置”按钮，停止计时并重置棋盘。
- 完成：达到目标时会弹出完成提示，记录会保存到 localStorage 中。
- 查看历史：点击“查看历史记录”打开滑出面板，查看最近 10 条记录与前三名。

## 本地数据
- localStorage 键名：`klotski_history_v1`
- 存储字段示例：{ seconds, moves, timestamp, localeDate, localeShortDate }
- 清理：在浏览器控制台执行 `localStorage.removeItem('klotski_history_v1')` 或在 DevTools → Application 手动删除。

## 开发说明
- 代码入口：`index.html`（单文件，含模板、样式与脚本）。
- 样式：使用 Tailwind CDN，已将页面外层 padding 从 `p-4` 调整为 `py-2 px-4` 以靠近上下边距。
- 性能小提示：历史记录的时间字符串在保存时已预先格式化，渲染时避免重复 new Date() 调用。

## 常见问题与排查
- 历史面板事件无响应：确认该面板 DOM 在 Vue 管理的 `#app` 内，否则 Vue 指令无效。
- 记录看起来重复或时间异常：检查 localStorage 中是否有旧版本数据或被手动修改。

## 许可
- 个人演示项目，可自由使用与修改。

---
文件：`index.html` 位于项目根目录，README 已添加并提交到本地仓库。
# 数字华容道 - klotski

![GitHub](https://img.shields.io/badge/license-MIT-blue) ![GitHub stars](https://img.shields.io/github/stars/yviscool/klotski?style=social)

**数字华容道** 是一款经典的益智游戏，通过移动数字方块，将它们按顺序排列。本项目使用现代前端技术实现，支持多种难度选择和动态效果，提供流畅的游戏体验。

🌐 **项目地址**: [https://github.com/yviscool/klotski](https://github.com/yviscool/klotski)

---

## 🎮 功能特点

- **多种难度选择**：支持 2x3、3x3、4x4 等多种难度模式。
- **动态效果**：方块移动流畅，带有音效和动画。
- **计时与步数统计**：实时记录游戏时间和步数。
- **胜利提示**：游戏完成后显示烟花效果和胜利弹窗。
- **响应式设计**：适配桌面和移动设备，随时随地畅玩。

---

## 🚀 使用方法

### 在线体验
直接访问 [klotski](https://digital-puzzle.vercel.app/) 即可在线体验。

### 本地运行
1. 克隆项目到本地：
   ```bash
   git clone https://github.com/yviscool/klotski.git
   ```
2. 进入项目目录：
   ```bash
   cd klotski
   ```
3. 打开 `index.html` 文件即可运行。

---

## 🛠️ 技术栈

- **HTML5**：页面结构与内容。
- **CSS3**：样式与动画效果。
- **JavaScript**：游戏逻辑与交互。
- **SweetAlert2**：美化弹窗提示。
- **tsParticles**：实现烟花效果。

---

## 📸 截图

![游戏界面](screenshot.png)

---

## 📜 许可证

本项目基于 **MIT 许可证** 开源。详情请参阅 [LICENSE](LICENSE) 文件。

---

## 🤝 贡献指南

欢迎贡献代码！如果您有任何建议或发现问题，请提交 Issue 或 Pull Request。

1. Fork 本项目。
2. 创建新分支 (`git checkout -b feature/YourFeature`)。
3. 提交更改 (`git commit -m 'Add some feature'`)。
4. 推送分支 (`git push origin feature/YourFeature`)。
5. 提交 Pull Request。

---

## 📧 联系

如有任何问题，请联系：  
📩 **Email**: [your-email@example.com](mailto:your-email@example.com)  
🌐 **GitHub**: [yviscool](https://github.com/yviscool)

---

**Enjoy the game! 🎉**

---
