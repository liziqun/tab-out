# Tab Out

**掌控你的标签页。**

Tab Out 是一款 Chrome 新标签页扩展，将你的新标签页转变为简洁高效的项目仪表盘。帮助你在繁杂的浏览器标签中保持专注与条理。

无服务器。无账户。无外部 API 调用。只是一个纯粹的 Chrome 扩展。

---

## 功能特性

- **Google 搜索栏** — 页面顶部集成 Google 搜索入口，快速发起搜索
- **标签页仪表盘** — 按域名分组展示当前打开的标签页，一目了然
- **主页分组** — 将 Gmail、X、YouTube、LinkedIn、GitHub 等主页归类到同一卡片
- **优雅关闭** — 关闭标签页时伴随音效与彩纸动画
- **重复检测** — 自动标记重复打开的页面，一键清理
- **稍后阅读** — 将标签页保存到待办清单，稍后再处理
- **归档管理** — 已完成的标签页自动归档，支持逐条删除清理
- **本地端口分组** — 显示端口号，轻松区分本地开发项目
- **可展开分组** — 首屏展示前 8 个标签，点击「+N more」展开更多
- **100% 本地运行** — 数据永不离开你的设备

---

## 主题风格

Tab Out 提供三套精心设计的主题风格，右上角调色盘图标可随时切换：

| 主题 | 说明 |
|------|------|
| **Auto**（默认） | 跟随系统深浅色模式自动切换。浅色模式采用 Notion 风格，深色模式采用 Dark Minimal 风格 |
| **Minimal** | 暖色调经典风格，米色纸张质感，琥珀色点缀，DM Sans + Newsreader 字体组合 |
| **Cyber** | 赛博朋克风格，深紫背景配霓虹青光，扫描线特效，卡片悬停发光，Space Grotesk 字体 |

主题选择会保存到 localStorage，下次打开自动应用。

---

## 截图

<!-- 在此处添加截图 -->
> 📸 截图待补充：主界面、主题切换、搜索栏

---

## 安装方法

### 方式一：手动安装（开发者模式）

**1. 克隆仓库**

```bash
git clone https://github.com/liziqun/tab-out.git
```

**2. 加载 Chrome 扩展**

1. 打开 Chrome 浏览器，访问 `chrome://extensions`
2. 开启右上角的 **开发者模式**
3. 点击 **加载已解压的扩展程序**
4. 选择项目中的 `extension/` 文件夹

**3. 打开新标签页**

打开一个新标签页，即可看到 Tab Out 仪表盘。

---

## 工作原理

```
打开新标签页
  → Tab Out 展示当前打开的标签页（按域名分组）
  → 主页（Gmail、X 等）归入顶部专属分组
  → 点击任意标签标题直接跳转
  → 关闭已完成的分组（伴随音效与彩纸动画）
  → 保存稍后处理的标签页
```

所有功能都在扩展内运行，无需外部服务器、无需 API 调用、数据不会发送到任何地方。保存的标签页存储在 `chrome.storage.local` 中。

---

## 技术栈

| 组件 | 技术 |
|------|------|
| 扩展框架 | Chrome Manifest V3 |
| 数据存储 | chrome.storage.local / localStorage |
| 音效 | Web Audio API（程序合成，无文件） |
| 动画 | CSS 过渡 + JS 彩纸粒子 |
| 依赖 | 无框架，纯 HTML / CSS / JavaScript |

---

## 项目结构

```
tab-out/
├── extension/           # 扩展核心目录
│   ├── index.html       # 新标签页页面
│   ├── app.js           # 主逻辑代码
│   ├── style.css        # 样式与主题变量
│   ├── background.js    # Service Worker
│   ├── manifest.json    # 扩展配置
│   └── icons/           # 扩展图标
└── style-demos/         # 主题风格演示页面
```

---

## 许可证

[MIT License](LICENSE)

---

## 致谢

本项目基于 [zarazhangrui/tab-out](https://github.com/zarazhangrui/tab-out) 二次开发，增加了多主题支持与 Google 搜索入口等功能。
