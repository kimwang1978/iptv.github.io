[返回主页面](..)

# 🌸 Kazumi：跨平台番剧采集与观看神器

🎬 **Kazumi** 是一个基于 **Flutter** 开发的 **开源跨平台番剧采集与在线观看工具**，支持多种设备，包括：

🖥️ Windows｜🍎 macOS｜🐧 Linux（实验性）｜📱 Android｜📱 iOS（需自签）

---

## ✨ 项目亮点

### 🧩 自定义采集规则（Xpath）

Kazumi 最大的亮点之一是其 **自定义采集规则系统**：

- 📌 用户可使用多达 5 行 Xpath 选择器，提取网页结构中所需的番剧信息。
- 🔁 支持导入导出规则，便于社区分享和交流。
- 🌐 可适配多种番剧资源站，实现真正的“自助采集”。

🎯 **这意味着**：你可以按自己的需求定制信息来源，而不再受限于固定的站点。

---

### 📺 流媒体播放 + 💬 弹幕支持

Kazumi 内置流媒体播放器，支持番剧在线观看，同时支持弹幕显示功能：

- 🔊 播放器界面简洁，操作流畅；
- 💬 弹幕支持 DanDan API，只需配置 Token 即可；
- 🎛️ 可自定义播放清晰度、加载速度、弹幕密度等设置。

🎉 **沉浸式追番体验，一站搞定！**

---

### 🧠 Anime4K 实时超分辨率处理（可选）

如果你喜欢高清画质，Kazumi 还支持 Anime4K 实时处理：

- 🚀 实时将低分辨率视频提升到高清级别；
- 🎨 在大屏幕设备上观看尤其明显；
- 🧩 动态加载，可根据设备性能自动选择是否启用。

---

## 🧪 多平台支持，一套代码跑遍全端！

| 平台       | 支持情况       | 特殊说明          |
|------------|----------------|-------------------|
| 🖥️ Windows | ✅ 正式支持    | 推荐 Windows 10+  |
| 🍎 macOS   | ✅ 正式支持    | macOS 10.15+      |
| 🐧 Linux   | 🧪 实验性支持  | 某些功能可能不稳定 |
| 📱 Android | ✅ 支持        | Android 10+       |
| 📱 iOS     | ✅（需自签）   | 无法上传 App Store |

⚙️ 使用 Flutter 构建，跨平台 UI 统一，性能表现出色。

---

## 🛠️ 技术架构与实现

Kazumi 使用以下技术构建：

- 🧱 **Flutter**：核心 UI 框架，统一多平台界面；
- 🎞️ **media_kit**（可能）或其他插件：播放引擎；
- ⛓️ **Xpath** + 正则：强大的网页数据解析；
- 🧬 **Anime4K**：实时视频增强；
- 🤖 **GitHub Actions**：持续集成与构建发布。

---

## 🔓 开源 & 社区

Kazumi 完全开源，托管在 GitHub：[Predidit/Kazumi](https://github.com/Predidit/Kazumi)

- 📬 有问题？可以开 issue；
- 🙌 有建议？欢迎提交 PR；
- 🔧 有规则？可以分享你的自定义采集规则文件！

📣 **典型社区建议示例**：
> “能不能在追番收藏页中添加时间表功能？” —— ✅ 已被开发者采纳！

---

## 📸 项目截图（示意）

| 播放界面 | 规则编辑器 | 弹幕体验 |
|----------|--------------|------------|
| ![播放界面](https://raw.githubusercontent.com/Predidit/Kazumi/refs/heads/main/static/screenshot/img_1.png) | ![规则编辑](https://raw.githubusercontent.com/Predidit/Kazumi/refs/heads/main/static/screenshot/img_6.png) | ![弹幕演示](https://raw.githubusercontent.com/Predidit/Kazumi/refs/heads/main/static/screenshot/img_4.png) |

> 📌 *注：截图来源于 GitHub 仓库中的 `screenshots` 目录。*

---

## 📦 安装与构建

- 📥 下载预构建版本（Release 页面）：
  👉 [Releases · Predidit/Kazumi](https://github.com/Predidit/Kazumi/releases)
- 🧑‍💻 自行构建：
  ```bash
  git clone https://github.com/Predidit/Kazumi.git
  cd Kazumi
  flutter pub get
  flutter run


---

### 其他推荐：
*   [新手入门系列：（安卓）OK影视](./docs/022_OK_Pro.md)
*   [新手入门系列：（安卓）影视仓](../docs/017_YingShiCang.md)

## 获取更多，欢迎关注公众号：百宝箱箱
<img src="../assets/GongZhongHao.png" style="max-width:100%; height:auto;">

[返回](..)
