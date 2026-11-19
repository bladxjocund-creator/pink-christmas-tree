# Pink Christmas Tree · 粉金星愿 🎄

An interactive pink particle Christmas tree made with Python.  
Python 粉色粒子圣诞树，支持鼠标互动、自定义祝福和 Windows EXE。

**[English](#english) | [简体中文](#简体中文)**

![Christmas tree preview · 圣诞树效果预览](preview.png)

## English

### Features

- Soft pink and champagne glows, a rotating 3D light ribbon, layered snowfall, and fading greetings.
- Drag with the left mouse button to rotate the tree; use the mouse wheel to zoom gently.
- Click the star for a golden wish effect, or click elsewhere for floating particle hearts.
- Subtle mouse parallax and a soft stardust trail.
- On-screen controls for pause, reset view, fullscreen, and greeting customization.
- Greeting changes are saved and applied immediately while the tree animation continues.

### Windows app — no Python installation needed

Check [Releases](https://github.com/bladxjocund-creator/pink-christmas-tree/releases) for published Windows builds.
Download and fully extract the app ZIP, then double-click `粉金星愿.exe`.
Keep `祝福文字.txt` next to the EXE if you want to share your customized greetings.

The current app interface is in Chinese. Greetings can be written in English;
the button translations and editable configuration example below help you customize it.

### Run from source

Requirements: **Python 3.11+**, a working **Tkinter / Tcl/Tk** installation, and Pillow.
The current version has been tested on Windows with Python 3.15.

Download and extract this repository, open a terminal in the project folder, then run:

```bash
python -m pip install -r requirements.txt
python christmas_tree.py
```

Tkinter is Python's standard GUI interface and is not installed by `requirements.txt`.
If you get an error such as `Can't find a usable init.tcl`, repair or reinstall Python
with Tcl/Tk support, or use the Windows EXE build.

Pillow enables the soft-glow renderer. Without Pillow, the app falls back to standard-library
drawing; appearance and performance will differ.

### Write your own English greetings

**Option 1: use the app's settings window.**

1. Click **修改祝福** — **Edit wishes** — at the bottom of the app.
2. Enter your own text in the four fields listed below.
3. Click **保存并应用** — **Save & Apply**.

| Chinese field | Meaning | Maximum length |
| --- | --- | --- |
| 主祝福 | Main greeting | 24 characters |
| 副祝福 | Secondary greeting | 48 characters |
| 英文标题 | Large heading | 40 characters |
| 顶部小字 | Small top heading | 40 characters |

Font sizes adapt automatically. Spaces and punctuation count toward the character limits.
**恢复默认** means **Restore defaults**; changes are saved only after you click **Save & Apply**.

**Option 2: edit the text file.**

Close the app and open `祝福文字.txt` with a text editor, such as Windows Notepad.
Change only the text to the **right** of each `=` sign. Keep the filename and the Chinese
keys on the left unchanged. For example:

```text
主祝福=Merry Christmas, Alex!
副祝福=Wishing you joy, warmth and love.
英文标题=Merry Christmas
顶部小字=WINTER WISHES
```

Save the file as UTF-8 and reopen the app. You do not need to edit Python code or rebuild the EXE.

![Greeting editor · 修改祝福窗口](settings.png)

### Mouse and keyboard controls

| Action | Result |
| --- | --- |
| Hold the left mouse button and drag horizontally | Rotate the tree |
| Mouse wheel | Zoom in / out slightly |
| Click the top star | Golden wish particles |
| Click elsewhere in the scene | Floating pink particle hearts |
| Move the mouse | Subtle parallax and stardust |
| 暂停 / 继续 | Pause / Resume |
| 重置视角 | Reset view |
| 全屏 / 退出全屏 | Enter / Exit fullscreen |
| Space | Pause / Resume |
| F11 | Toggle fullscreen |
| Esc | Exit fullscreen; close the app in windowed mode |

### Performance

`FPS = 60` near the top of `christmas_tree.py` is a target, not a guaranteed frame rate.
Actual performance depends on your computer, window size, and background applications.
For a slower computer, try `QUALITY = 0.7` or `FPS = 30`.

### Build a Windows EXE

First make sure the source runs normally in your Windows Python environment, then run:

```bash
python -m pip install pyinstaller
python -m PyInstaller --onefile --windowed --name PinkChristmasTree christmas_tree.py
```

The generated EXE is in `dist`. Put `祝福文字.txt` next to it when distributing customized greetings.
When distributing an EXE containing third-party runtime components, retain their license notices.

### License

The project source is licensed under the [MIT License](LICENSE).
Python, Tcl/Tk, and Pillow retain their respective licenses.

---

## 简体中文

### 功能

- 粉金柔光粒子、三维旋转灯带、分层飘雪和渐显祝福。
- 鼠标左键拖动旋转，滚轮轻微缩放。
- 点击树顶星星触发许愿星光，点击其他画面位置绽放爱心。
- 鼠标移动产生轻微视差与星尘尾迹。
- 底部按钮支持暂停、重置视角、全屏和修改祝福。
- 修改祝福立即生效并自动保存，树身与灯光动画继续播放。

### Windows 程序：无需安装 Python

在 [Releases](https://github.com/bladxjocund-creator/pink-christmas-tree/releases) 中查看发布版本。
下载 Windows 程序压缩包后完整解压，双击 `粉金星愿.exe` 运行。
分享自己的祝福时，可以把同目录的 `祝福文字.txt` 一起发送。

目前程序界面为中文，祝福文字支持自行填写英文。上方英文说明提供了中文按钮对照及英文配置示例。

### 从源码运行

需要 **Python 3.11 或更新版本**、可用的 **Tkinter / Tcl/Tk** 和 Pillow。
当前版本已在 Windows / Python 3.15 上测试。

下载仓库并解压，在项目文件夹中打开终端，依次运行：

```bash
python -m pip install -r requirements.txt
python christmas_tree.py
```

Tkinter 是 Python 的标准 GUI 接口，不通过 `requirements.txt` 安装。
如果出现 `Can't find a usable init.tcl` 等错误，请修复或重新安装包含 Tcl/Tk 的 Python，
或使用 Windows EXE 版本。

有 Pillow 时启用柔光合成渲染；未安装 Pillow 时使用标准库绘制，效果与性能会有所不同。

### 修改名字与祝福

**方法一：在程序中修改。**

点击窗口底部的 **修改祝福**，填写后点击 **保存并应用**。

| 项目 | 长度上限 |
| --- | --- |
| 主祝福 | 24 个字 |
| 副祝福 | 48 个字 |
| 英文标题 | 40 个字 |
| 顶部小字 | 40 个字 |

文字会自动适应字号；空格和标点也计入长度。
**恢复默认** 会先填回默认文字，点击 **保存并应用** 后才会保存。

**方法二：用记事本修改。**

关闭程序，打开同目录的 `祝福文字.txt`。
只修改每行等号右边的内容，保留文件名和等号左边的中文名称。
以 UTF-8 编码保存后，重新打开程序即可，不需要修改代码或重新打包 EXE。

```text
主祝福=愿你天天开心
副祝福=愿你的每一天，都被温柔与爱包围
英文标题=Merry Christmas
顶部小字=WINTER WISHES
```

### 操作

| 操作 | 效果 |
| --- | --- |
| 按住鼠标左键左右拖动 | 转动圣诞树 |
| 鼠标滚轮 | 轻微放大 / 缩小 |
| 点击树顶星星 | 金色许愿星光 |
| 点击其他画面位置 | 粉色粒子爱心 |
| 移动鼠标 | 轻微视差与星尘尾迹 |
| 底部按钮 | 修改祝福、暂停 / 继续、重置视角、全屏 |
| 空格 | 暂停 / 继续 |
| F11 | 切换全屏 |
| Esc | 退出全屏；普通窗口下关闭程序 |

### 性能设置

源码顶部的 `FPS = 60` 是目标帧率，实际帧率取决于电脑、窗口尺寸和后台程序。
电脑较慢时，可以把 `QUALITY = 1.0` 改为 `QUALITY = 0.7`，或把目标帧率设为 `FPS = 30`。

### 自行打包 Windows EXE

在已能正常运行源码的 Windows Python 环境中执行：

```bash
python -m pip install pyinstaller
python -m PyInstaller --onefile --windowed --name PinkChristmasTree christmas_tree.py
```

生成的程序位于 `dist` 文件夹。将 `祝福文字.txt` 放到 EXE 旁边即可随程序分发。
包含第三方运行组件的 EXE 发行包还应保留相应组件的许可信息。

### 许可

项目源码采用 [MIT License](LICENSE)。Python、Tcl/Tk 和 Pillow 等依赖遵循各自的许可。
