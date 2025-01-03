# 时区处理的变化

> 原文：[Timezone handling changes](https://faqs.ankiweb.net/timezone-handling-changes.html)

Anki 2.1.22+、AnkiMobile 2.0.57+ 和 AnkiDroid 2.15+ 包含了对 Anki 计算经过天数方式的可选更改。此更改
解决了一些极端情况，即时区变更（包括夏令时）可能导致 Anki 向前或向后推移一天的问题，并解决了一些用户
在与 AnkiWeb 同步时卡片被解除搁置 / 每日计数被重置的问题。

对于大多数用户，新算法应生成与旧算法相同的经过天数。对于某些用户，启用此代码可能会使 Anki 向前或向后
推移一天，但这只会发生一次，并且 Anki 之后将更能应对时区变化。

**请确保在启用新代码之前，你正在运行上述版本。** 如果你的任何 Anki 客户端尚未更新，则在启用此功能时
你将无法同步它们。

要启用新的计算，请确保：

- 你的设备已同步
- 你正在运行 Anki 2.1.22+
- 在首选项界面中启用了 2.1 调度程序或更高版本

然后，要启用新的时区代码，请勾选『新时区』复选框。

请关闭窗口并同步，然后同步你的其他设备以完成此过程。

如果你注意到新的处理存在任何问题，请告知我们。
