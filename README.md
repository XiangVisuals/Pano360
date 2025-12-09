# 🌐 Immersive VR Panorama / 沉浸式 VR 全景体验

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg) ![License](https://img.shields.io/badge/license-MIT-green.svg) ![Status](https://img.shields.io/badge/status-Stable-success)

**[English]** A lightweight, high-performance web-based 360° panorama viewer optimized for mobile devices. It features a modern "Glassmorphism" UI, gyroscope motion control, and smooth scene transitions using the Pannellum engine.

**[中文]** 一个轻量级、高性能的基于 Web 的 360° 全景浏览体验，专为移动端设备优化。项目采用现代化的“毛玻璃”UI 设计，支持陀螺仪体感控制，并基于 Pannellum 引擎实现了流畅的场景切换。

---

## ✨ Features / 功能特性

* **📱 Mobile-First Design / 移动优先设计**
    * Responsive layout with touch optimization.
    * **Gyroscope Control:** Move your phone to look around (Motion sensors).
    * **Orientation Hint:** Smart overlay suggesting landscape mode for the best experience.
    * 响应式布局，触摸优化。
    * **陀螺仪控制：** 支持移动手机进行体感查看。
    * **横屏提示：** 智能检测并建议用户在横屏模式下获得最佳体验。

* **🎨 Modern UI / 现代 UI 界面**
    * **Glassmorphism:** Frosted glass effects on landing pages and HUDs.
    * **Immersive Landing:** Dynamic background that blurs the panorama preview.
    * **HUD Controls:** Floating bottom bar for quick actions (Auto-rotate, Gyro, Fullscreen).
    * **毛玻璃特效：** 启动页和 HUD 控制栏采用磨砂玻璃质感。
    * **沉浸式启动页：** 动态模糊背景，无缝衔接全景图。
    * **HUD 控制栏：** 底部悬浮栏，提供自动旋转、体感开关、全屏等快捷操作。

* **🖼️ Multi-Scene System / 多场景系统**
    * Supports multiple panoramic scenes with a thumbnail gallery.
    * Smooth fade-in/out transitions between scenes.
    * 支持多个全景场景切换，配有缩略图画廊。
    * 场景切换时具有平滑的淡入淡出过渡效果。

* **⚡ Performance / 性能优化**
    * CDN pre-connections and lazy loading logic.
    * Loading spinners and toast notifications for user feedback.
    * CDN 预连接与懒加载逻辑。
    * 加载动画与 Toast 提示，提供良好的交互反馈。

---

## 🛠️ Tech Stack / 技术栈

* **Core:** HTML5, CSS3, JavaScript (Vanilla ES6+)
* **Engine:** [Pannellum](https://pannellum.org/) (v2.5.6) - A lightweight 360° panorama viewer for the web.
* **Analytics:** Microsoft Clarity (Integrated)
* **Hosting:** Compatible with any static web server (Nginx, Apache, Vercel, GitHub Pages).

---

## 🚀 Quick Start / 快速开始

### Prerequisites / 前置条件

Due to browser security policies regarding WebGL and cross-origin textures (CORS), **you cannot simply double-click the `index.html` file to run it.** You must run it via a local web server.

由于浏览器对 WebGL 和跨域纹理 (CORS) 的安全策略，**您不能直接双击 `index.html` 文件运行。** 您必须通过本地 Web 服务器运行它。

### Setup / 启动步骤

1.  **Clone or Download** the repository.
    下载或克隆本项目。

2.  **Run with a Local Server / 使用本地服务器运行**:

    * **VS Code (Recommended):** Install the "Live Server" extension, right-click `index.html`, and select "Open with Live Server".
    * **Python:**
        ```bash
        # Python 3
        python -m http.server 8000
        ```
    * **Node.js (http-server):**
        ```bash
        npx http-server .
        ```

3.  **Access / 访问**: Open `http://localhost:8000` in your browser.

---

## ⚙️ Configuration / 配置说明

To add or change panoramic images, modify the `SCENE_LIST` array inside the `<script>` tag in `index.html`.

如需添加或更改全景图片，请修改 `index.html` 中 `<script>` 标签内的 `SCENE_LIST` 数组。

```javascript
const SCENE_LIST = [
    { 
        id: 0, 
        name: "Scene Name / 场景名称", 
        // Full resolution panorama image (Equirectangular)
        // 全分辨率全景图 (等距柱状投影)
        url: "https://path/to/your/panorama.jpg", 
        // Thumbnail image for the gallery
        // 画廊缩略图
        thumb: "https://path/to/your/thumb.jpg" 
    },
    // Add more scenes here...
    // 在此添加更多场景...
];
