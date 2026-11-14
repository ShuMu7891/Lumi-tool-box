<div align="center">

# 💡 LumiBox · Windows 综合工具箱

**一站式 Windows 效率工具箱 · 液态玻璃 UI · 全部本地离线运行**

PySide6 / Python 构建 · 无需联网 · 无需登录 · 数据不上传

[![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-blue)](#)
[![Python](https://img.shields.io/badge/python-3.10%2B-blueviolet)](#)
[![PySide6](https://img.shields.io/badge/GUI-PySide6%20%2F%20Qt6-orange)](#)
[![License](https://img.shields.io/badge/license-MIT-green)](#)
[![Release](https://img.shields.io/badge/version-v1.2.0-red)](#)

[功能总览](#-功能总览) · [快速开始](#-快速开始) · [打包为 exe](#-打包为-exe) · [截图预览](#-截图预览) · [项目结构](#-项目结构)

</div>

---

## 📸 截图预览

<div align="center">
<img src="preview/01_overview.png" alt="LumiBox 概览" width="800"/>
<p><em>概览工作台：实时时钟、CPU / 内存 / 系统盘监控与快捷入口</em></p>
</div>

> 更多截图见下方 [截图预览](#-截图预览) 一节。

---

## ✨ 为什么是 LumiBox？

- **🚫 零联网、零登录**：所有计算均在本地完成，无账号体系、无数据上传、无遥测。
- **🎨 液态玻璃界面**：无边框窗口 + 亚克力质感 + 明暗双主题一键切换。
- **🧰 大而全**：13 个功能页，覆盖系统监控、文件管理、开发辅助、文档转换等日常场景。
- **📦 开箱即用**：提供一键安装脚本，也可用 PyInstaller 打成单文件 exe 直接拷走。

---

## 🧰 功能总览

| 模块 | 功能 |
| --- | --- |
| 🖥 **系统信息 & 监控** | CPU / 内存 / 磁盘 / 网卡实时监控（基于 psutil，真实数据） |
| 📝 **文本与开发** | SHA 哈希计算、Base64 编解码、URL / JSON / 正则工具 |
| 🖼 **图片与颜色** | 图片压缩、缩放、变换、格式转换、屏幕取色与配色 |
| 🌐 **网络与效率** | 时间戳转换、密码生成、单位换算、IP 检测 |
| 🧮 **计算器** | 标准四则、科学函数、程序员模式（进制 / 位运算 / 位视图）、计算历史 |
| 🧰 **开发者工具** | 进制转换、随机数、编码转换、UUID 批量生成、反编译辅助、剪贴板工具 |
| 🛠 **实用工具** | 二维码生成 / 解析（zxing 本地解码）、转盘决定、局域网扫描、磁盘健康、PDF / PPT / PPTX 互转 |
| 📁 **文件管家** | 重复文件去重、批量重命名、文件粉碎、hosts 编辑器 |
| ⚙ **系统增强** | 启动项 / 服务管理、定时任务、端口扫描测速、窗口与托盘控制 |
| 📄 **文档工坊** | YAML / TOML / JSON 格式互转、Markdown 预览导出 PDF、OCR、密码保险箱（AES 加密） |
| 🎯 **截图 & 效率** | 屏幕截图 / 贴图（`Ctrl+Alt+S` 全局快捷键）、番茄钟、待办清单 |

---

## 🚀 快速开始

### 方式一：一键运行（推荐普通用户）

1. 安装 [Python 3.10+](https://www.python.org/downloads/)（安装时勾选 **Add Python to PATH**）
2. 双击 `一键安装运行环境.bat`（首次运行自动装好全部依赖）
3. 双击 `run.bat` 启动 LumiBox

### 方式二：命令行运行（开发者）

```bash
git clone https://github.com/<你的用户名>/LumiBox.git
cd LumiBox
pip install -r requirements.txt
python main.py
```

### 环境要求

| 依赖 | 版本 |
| --- | --- |
| Windows | 10 / 11 |
| Python | 3.10 或更高 |
| 核心依赖 | PySide6、psutil、Pillow、qrcode、requests 等，见 `requirements.txt` |

<details>
<summary><b>可选依赖（自动探测，缺失不影响使用）</b></summary>

| 依赖 | 作用 |
| --- | --- |
| `tesseract-ocr` + 中文语言包 | 文档工坊 OCR 功能（系统级安装，非 pip 包） |
| `opencv-python-headless` / `pyzbar` | 二维码解析备用引擎 |
| `uncompyle6` / `decompyle3` / `pycdc` | 反编译页的外部源码还原工具 |
| `send2trash` | 重复文件清理时送入回收站（否则直接删除） |

</details>

---

## 📦 打包为 exe

双击 `build.bat`，或手动执行：

```bash
pip install -r requirements.txt
python -m PyInstaller --noconfirm --clean --onefile --windowed LumiBox.spec
```

构建完成后可执行文件位于 **`dist\LumiBox.exe`**，单文件绿色版，可直接复制到任意 Windows 电脑运行。

---

## 🖼 截图预览

| 系统 | 文本 | 图片 |
| --- | --- | --- |
| ![系统监控](preview/02_system_monitor.png) | ![文本工具](preview/03_text_tools.png) | ![图片取色](preview/04_image_color.png) |
| 系统信息 & 监控 | 文本与开发 | 图片与颜色 |

| 网络 | 开发者 | 二维码 |
| --- | --- | --- |
| ![网络工具](preview/05_network_tools.png) | ![开发者](preview/06_dev_base_random.png) | ![二维码](preview/09_qrcode_wheel.png) |
| 网络与效率 | 开发者工具 | 二维码 & 转盘 |

| 文件 | 文档 | 计算器 |
| --- | --- | --- |
| ![文件管家](preview/15_files_duplicates.png) | ![文档工坊](preview/11_pdf_ppt_convert.png) | ![计算器](preview/12_calculator.png) |
| 重复文件清理 | PDF / PPT 转换 | 计算器 |

| 编码 | 暗色主题 | 文件粉碎 |
| --- | --- | --- |
| ![编码](preview/07_dev_encoding_uuid.png) | ![暗色](preview/14_dark_developer.png) | ![粉碎](preview/17_files_shred.png) |
| 编码 & UUID | 暗色主题 | 文件粉碎 |

---

## 🗂 项目结构

```
LumiBox/
├── main.py                  # 程序入口
├── app/
│   ├── main_window.py       # 主窗口（无边框玻璃外壳、侧边导航、页面栈）
│   ├── theme.py             # 明暗主题 / 液态玻璃样式
│   ├── glass.py             # 亚克力 / 毛玻璃效果
│   ├── power.py             # 系统电源相关
│   ├── utils.py             # 通用工具（图标、提示等）
│   └── pages/               # 13 个功能页面
│       ├── home_page.py     # 概览
│       ├── system_page.py   # 系统信息 & 监控
│       ├── text_page.py     # 文本与开发
│       ├── image_page.py    # 图片与颜色
│       ├── net_page.py      # 网络与效率
│       ├── dev_page.py      # 开发者工具
│       ├── tools_page.py    # 实用工具
│       ├── calc_page.py     # 计算器
│       ├── files_page.py    # 文件管家
│       ├── sys_page.py      # 系统增强
│       ├── doc_page.py      # 文档工坊
│       ├── focus_page.py    # 截图 & 效率
│       └── about_page.py    # 关于
├── assets/                  # 应用图标
├── preview/                 # README 截图
├── build.bat                # 一键打包为 exe
├── run.bat                  # 一键运行
├── 一键安装运行环境.bat        # 一键安装依赖
├── requirements.txt
└── LumiBox.spec             # PyInstaller 打包配置
```

---

## 🛣 Roadmap

- [ ] 便携版绿色发布（GitHub Releases 附 exe）
- [ ] 多语言支持（i18n）
- [ ] 插件化页面架构，方便第三方扩展
- [ ] 自动更新检查

> 欢迎提 Issue / PR！

## 🤝 参与贡献

1. Fork 本仓库并新建分支：`git checkout -b feature/xxx`
2. 提交更改：`git commit -m "feat: xxx"`
3. 推送并发起 Pull Request

## 📄 开源协议

本项目基于 [MIT License](LICENSE) 开源发布。

---

<div align="center">

**如果 LumiBox 对你有帮助，欢迎点个 ⭐ Star 支持一下！**

</div>
