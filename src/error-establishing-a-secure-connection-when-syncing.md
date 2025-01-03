# 「建立安全连接时出错」同步错误

> 原
> 文：["Error establishing a secure connection." when syncing](https://faqs.ankiweb.net/error-establishing-a-secure-connection-when-syncing.html)

此错误发生在 Anki 尝试连接到 AnkiWeb 并且收到无效响应时。可能是由以下原因导致的：

- 你机器上的防病毒软件或防火墙
- 工作和学校网络中常见的过滤网络连接
- 不可靠的网络连接

**防病毒/防火墙/VPN/代理**

防病毒、防火墙和 VPN 程序在过滤网络流量时往往会引发问题。

首先尝试为 Anki 添加例外。

如果这不起作用，尝试暂时禁用你的防病毒软件。

不幸的是，有些防病毒程序在被禁用时无法完全停止运行。我们曾见过唯一解决问题的方法是完全卸载防病毒程
序。我们并不期望你为了运行 Anki 而停止使用防病毒程序，但如果先前的建议无效，你可以尝试卸载并重启计算
机，看看是否能解决问题。如果能，请联系你的防病毒公司，并向他们报告此问题。

**不可靠的网络**

如果你的 wifi 或互联网连接存在问题，来自 AnkiWeb 的消息可能会被破坏或无法到达，从而导致出现此错误消
息。可以尝试检查是否存在数据包丢失：

<https://open-spaced-repetition.github.io/anki-faqs-zh-CN/syncing-failed-connection-timed-out-errors-when-syncing.html>
