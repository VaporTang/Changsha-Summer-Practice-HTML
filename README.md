# 湘当红小队 - 社会实践项目展示网站

![License](https://img.shields.io/badge/license-MIT-blue.svg)

欢迎来到**湘当红小队**的官方项目展示网站！该网站是为记录和展示**北京林业大学2025年“青春向党”红色教育专项实践团队**在湖南长沙的社会实践活动而创建的。

**项目宗旨**: 重走长沙红色足迹，赓续湖湘革命精神。

> **线上访问地址**: [湘当红小队](https://bjfu.vaporfiles.eu.org)

## ✨ 主要功能

本网站是一个纯静态页面，采用现代化设计，旨在提供流畅、美观且信息丰富的浏览体验。

* **🎨 现代响应式设计**: 完美适配桌面、平板和手机等不同尺寸的设备，确保在任何屏幕上都有最佳的视觉效果。
* **🚀 流畅的交互动画**:
    * 页面加载时的**预加载动画**，提升用户体验。
    * 元素随滚动**渐进式载入**（Fade-in on scroll），使页面过渡更自然。
    * 卡片、按钮等元素的**悬停（Hover）特效**，提供及时的视觉反馈。
* **🚩 沉浸式导航**:
    * 顶置固定导航栏，方便随时在页面各部分之间跳转。
    * 移动端专属的**抽屉式导航菜单**，带有流畅的滑入动画。
    * 点击导航链接后页面**平滑滚动**至对应区域。
* **🎬 丰富的多媒体展示**:
    * **Vlog视频廊**: 以卡片形式展示每日Vlog，点击即可在弹窗中无跳转播放。
    * **原创设计展**:
        * 团队旗帜和Logo展示。
        * **纪念明信片**区域采用独特的**3D翻转效果**，在桌面端悬停或移动端点击即可查看正反面设计。
* **📄 详细行程规划**:
    * 以图文并茂的卡片形式展示每日行程。
    * 点击行程卡片可**弹窗预览**详细的Word文档规划（通过Office Online服务）。
* **⚡️ 性能优化**:
    * 对明信片等图片资源采用**懒加载**技术，加快页面初始加载速度。
    * 使用原生JavaScript，无任何重型框架依赖，轻量且高效。

---

## 🛠️ 技术栈

本项目完全使用前端基础技术构建，易于理解和维护。

* **HTML5**: 采用语义化标签构建页面结构。
* **CSS3**:
    * 使用 **CSS变量 (Variables)** 进行全局样式管理，方便主题色彩的统一修改。
    * 广泛应用 **Flexbox** 和 **Grid** 布局，实现复杂的响应式页面结构。
    * 利用 **Transitions** 和 **Keyframe Animations** 实现各种动态效果。
* **Vanilla JavaScript (ES6+)**:
    * 负责所有DOM操作和交互逻辑，如菜单切换、弹窗控制、平滑滚动等。
    * 使用 **Intersection Observer API** 实现元素的滚动监听和懒加载。

---

## 📂 项目结构

本项目是一个单页面应用，所有代码都包含在 `index.html` 文件中，结构清晰。

```
.
└── index.html      # 包含HTML结构、CSS样式和JavaScript脚本
└── README.md       # 项目说明文件
└── LICENSE         # 项目许可证
```

**代码模块划分 (在 `index.html` 内部):**
* **`<style>` 标签**: 包含了所有的CSS代码，从基础重置、工具类、变量定义到各个组件和响应式媒体查询的样式。
* **`<body>` 标签**: 包含了所有的HTML内容结构，按功能区分为导航栏(`<nav>`)、头部(`<header>`)、主内容区(`<main>`)和页脚(`<footer>`)。
* **`<script>` 标签**: 包含了所有的JavaScript交互逻辑，实现了包括导航、弹窗、懒加载、动画等所有动态功能。

---

## 🚀 如何运行

由于这是一个纯静态网站，您无需复杂的构建过程即可在本地运行。

1.  **克隆仓库**
    ```bash
    git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)
    ```

2.  **打开文件**
    进入项目目录，直接在您喜欢的浏览器中打开 `index.html` 文件即可。

    > **💡 提示**: 为了获得最佳体验并避免潜在的CORS（跨域资源共享）问题（尤其是在加载外部文档时），推荐使用一个本地服务器来运行项目。如果您使用VS Code，可以安装 [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) 插件，右键点击 `index.html` 并选择 "Open with Live Server"。

---

## 🔧 如何定制

您可以轻松地修改此模板以适应您自己的项目。

* **修改内容**: 直接在 `index.html` 文件中找到对应的HTML部分（如 `id="about"` 的 `section`）并修改文本和图片链接。
* **修改颜色主题**: 在 `<style>` 标签的顶部，修改 `:root` 选择器下的CSS变量值即可改变网站的全局配色。
    ```css
    :root {
        --primary-color: #c41e3a; /* 主题色 */
        --text-color: #333;       /* 文本颜色 */
        /* ... 其他颜色变量 */
    }
    ```
* **更新Vlog和行程文件**:
    * **Vlog**: 在 `id="vlogs"` 的 `section` 中，修改 `onclick` 事件中的视频URL、标题和描述。
    * **行程**: 在JavaScript代码块中，找到 `scheduleFiles` 对象，修改其中的Word文档链接。
* **更新明信片**: 在 `id="designs"` 的 `section` 中，找到明信片项目，替换 `data-bg` 属性中的图片链接和下方的描述文本。

---

## 📜 开源协议

本项目采用 **MIT License**。

```
MIT License

Copyright (c) 2025 Jin Liang Tang

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```