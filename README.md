# Minecraft Shortcut Transfer

## 这个程序能做什么？

这个程序可以帮助你快速输入Minecraft传送指令，你只需要将坐标和名称写在文档中就可以了，在1.2版本之后可以实现跨维度传送，你再也不需要去记又长又难记的指令了。

## 准备

本项目使用Python语言进行编写，所需依赖库如下：

- `pygetwindow`
- `win32gui`（`win32`）
- `pyautogui`

请确保您的Python环境和上述依赖库已经安装和配置完成。

## 实现方式

1. 使用`win32gui`获取当前窗口的标题，以确保程序在Minecraft游戏窗口中运行。
2. 读取`coordinate.txt`文件中的内容，该文件需要位于当前目录下。
3. 利用`pyautogui`自动输入Minecraft指令。

## 使用方法

1. 编写`coordinate.txt`文件，格式为 `序号, 名称, 坐标`，示例： `1, home, -373, 69, 857`。
2. 运行`Minecraft_transfer.py`，程序会自动读取`coordinate.txt`的内容，请确保格式正确，否则会报错退出。
3. 请先输入你要传送的维度再输入您要传送的位置序号或名称，输入完成后请在2秒内切换回Minecraft窗口，请保持不动键盘的状态2秒，程序将自动输入指令。

   **注意：请确保游戏未处于暂停状态。**

### 示范

![这是GIF](/img/a.gif "GIF示范")

## 已知问题

- 窗口检测可能出错
- 无法使用中文名称
- 程序运行时如果用户进行键盘操作，可能导致输入错误
- 如果大写状态下或者输入法状态下会导致输入失败

## 未来功能

- ~~添加维度传送功能~~(已实现)
- 添加维度分组功能
- 添加当前坐标提取功能
- 增加更多的指令功能
