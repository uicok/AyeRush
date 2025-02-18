AyeRush 是一个用于监控 Warframe 的 EE.log 文件，实时解析赏金任务和月球密室生成情况的工具。该工具通过图形界面（GUI）显示任务名称及任务阶段信息，并采用增量刷新机制，只读取日志中新添加的内容，从而避免重复显示旧内容。

功能特点
实时日志监控
利用全局文件偏移量，实现每次刷新只读取新增日志内容。

赏金任务解析
从日志中提取完整任务名称（例如“希图斯 (地球) - 捕获 Grineer 指挥官”）和任务阶段，自动匹配对应平原的任务链。

月球密室检测
统计月球密室的生成情况，并在 GUI 中显示检测结果。

图形界面
使用 Tkinter 构建简洁直观的 GUI，支持手动刷新和检测。

安装依赖
Python 3.x
Tkinter（通常内置于 Python 安装中）
watchdog
安装方法：
sh
复制
编辑
pip install watchdog
使用方法
配置日志路径
默认代码读取路径为 LOCALAPPDATA\Warframe\EEE.log，请确保 Warframe 安装在默认位置，或修改代码中 LOG_PATH 变量。

运行程序
在命令行中运行：

sh
复制
编辑
python AyeRush.py
或将代码打包为单个 exe 文件后运行。

打包为 exe
推荐使用 PyInstaller 打包为无终端窗口的 exe 文件：

sh
复制
编辑
pyinstaller -F -w AyeRush.py
打包成功后，生成的 exe 文件位于 dist 目录中。

刷新日志

点击 GUI 上的【刷新日志】按钮时，程序将从上次读取位置开始读取新增日志，并更新赏金任务和月球密室信息。
如果没有检测到新增内容，GUI 上会保留当前显示，不会清空内容。






### 导致2035本人概不负责
