# 声音 / 图片未在 AnkiWeb 或移动客户端上显示

> 原
> 文：[Sounds/images are not appearing on AnkiWeb or the mobile clients](https://faqs.ankiweb.net/sounds-or-images-are-not-appearing-on-ankiweb-or-the-mobile-clients.html)

如果你通过从文本文件导入创建你的牌组，或者下载了以这种方式创建的共享牌组，那么 Anki 中的文件名可能与
计算机上的文件名不匹配。一些计算机会把「file.jpg」、「file.JPG」和「FILE.JPG」视为相同的文件，但其他
计算机则不会。这意味着如果牌组中引用了「dog.jpg」，但磁盘上的文件是「dog.JPG」，某些设备（包括
AnkiWeb）将无法显示图像。

你可以通过在计算机版本中编辑未正确显示的卡片来确认这是问题所在。如果音频没有正常工作，你会看到类似于
`[sound:hello.mp3]` 的链接。如果你看到一个损坏的图片链接，点击该字段，然后按右上角的下箭头，选择「编
辑 HTML」，并找到类似以下的文本：

```html
<img src="cat.jpg" />
```

记下文件的名称。

然后打开你的集合的媒体文件夹
（<https://open-spaced-repetition.github.io/anki-manual-zh-CN/files.html#文件位置>）并找到引用的文
件。如果文件没有使用完全相同的小写或大写字母组合，你就找到了问题所在。

另外，请确保你已
经[进行了媒体检查](https://open-spaced-repetition.github.io/anki-manual-zh-CN/media.html#手动添加媒体)。

如果这是一个共享牌组，请将问题报告给共享牌组的作者。如果大小写不同是规律性的，你可以尝试使用 Anki 的
浏览器中的查找和替换功能来解决问题。例如，如果链接是「dog.JPG」但磁盘上的文件是「dog.jpg」，你可以点
击浏览，选择所有卡片，并使用查找和替换功能将 JPG 替换为 jpg。

如果这没有解释你的问题，请检查你所用的计算机是否没有使用 vfat/fat32 文件系统。Anki 目前无法检测出当
媒体文件夹在此类文件系统上时的更改，因此媒体同步在这种情况下不起作用。未来的发行版中计划提供一个解决
方案。
