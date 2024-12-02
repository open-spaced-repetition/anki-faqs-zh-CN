# 声音 / 图片媒体文件丢失了！

> 原
> 文：[Sound/image media files have gone missing!](https://faqs.ankiweb.net/sounds-or-images-have-gone-missing.html)

Anki 将你的卡片的音频和图像文件存储在你的计算机中，位于
[Anki 文件夹](https://open-spaced-repetition.github.io/anki-manual-zh-CN/files.html#file-locations)的
User 1/collection.media 中。如果你删除了该文件夹中的任何文件，Anki 会记录它们已被移除，并在下次同步
时也会从你的其他设备中移除它们。有时会发生用户在电脑上整理文件，意外删除卡片使用的音频和图像，导致音
频无法播放或图像无法显示的情况。在 Mac 上使用 Finder 的「所有我的文件」功能时，特别容易不小心删除，
但在其他平台上也可能发生。

你可以使用 Anki 的 工具>检查媒体 功能，通过查看「使用于卡片但在媒体文件夹中缺失」部分，找出集合中缺
少的图像。

如果你不小心删除了卡片使用的文件，你可以尝试从回收站中恢复它们，如果回收站尚未被清空的话。将它们放回
collection.media 文件夹应该会使媒体再次正常工作。

如果你无法从任何设备上恢复你的媒体文件，如果这些文件是最近被删除的，我们可能可以从 AnkiWeb 的备份中
为你恢复它们。

如果你丢失了音频和图像，但这些是从共享牌组中获取的，且该共享牌组仍然可用，你可以将其导入到一个新的用
户档案中，然后从中复制音频和图像到你的原始集合中以恢复数据。

编辑字段时，Anki 会显示音频文件的名称。要查看图像文件的名称，你可以在光标位于图像的字段中时按
ctrl+shift+x（在 Mac 上为 cmd+shift+x）。要使图像或音频文件正常工作，具有完全相同文件名的文件必须位
于 collection.media 文件夹中。
