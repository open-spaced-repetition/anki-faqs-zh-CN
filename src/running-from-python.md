# 从 Python 运行

如果你在使用 Anki 的打包版本时遇到启动问题或崩溃，并且无法解决，你可以尝试最后的办法，直接通过
Python 运行。

以下说明是为 Windows 用户提供的，因为这些问题在 Windows 上似乎最为普遍，但在其他平台上也可以采取类似
的方法。

1. 安装 <https://www.python.org/ftp/python/3.9.13/python-3.9.13-amd64.exe>。自定义安装位置，选择
   `c:\python`
2. 打开开始菜单，并打开命令提示符。
3. 输入以下内容并按回车：

```
\python\python -m venv \anki-venv
```

4. 然后输入以下内容，这将需要一些时间：

```
\anki-venv\scripts\pip install aqt orjson pyqt6-webengine
```

5. 最后：

```
\anki-venv\scripts\anki
```

如果这解决了你的问题，你可以通过重复步骤 2 和步骤 5 再次启动 Anki。

如果问题仍然存在，你可以尝试更改 Qt 版本：

```
\anki-venv\scripts\pip install pyqt5==5.15 pyqtwebengine==5.15.0
```

如果这也没有帮助，并且你已经按照[当问题发生时](./when-problems-occur.md)中的所有步骤进行操作，那么你
可能不走运了。
