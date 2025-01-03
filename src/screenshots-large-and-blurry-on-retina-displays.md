# Retina 显示屏上截图过大且模糊

> 原
> 文：[Screenshots large and blurry on retina displays](https://faqs.ankiweb.net/screenshots-large-and-blurry-on-retina-displays.html)

如果你编辑一张卡片，点击卡片，然后在样式部分的最底部放置以下内容，它将把截图缩小到合适的大小：

```
img[src*="Screen"] {
  zoom: 50%;
}
```

这段代码通过定位文件名中包含「Screen」的文件来工作——这适用于 macOS 使用的默认「Screen Shot」名称。如
果你的截图使用不同但一致的名称，你可以调整上面的那行代码。

如果你的截图名称没有一致的模式，你可以去掉方括号及其中的文本，这将导致匹配所有图像。来自高分辨率显示
屏的图片现在看起来是正确的，但从其他来源获取的图片可能会显得过小。不幸的是，目前对此问题并没有很好的
解决方案——Anki 使用的 Web 技术不能检测哪些图像需要调整大小。在将图像添加到 Anki 之前调整它们的大小，
将允许你混合和匹配其他图像，但这需要一些设
置：<https://www.quora.com/How-can-I-get-my-retina-Mac-to-not-take-screenshots-that-are-too-big>
