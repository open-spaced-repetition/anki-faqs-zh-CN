# Anki 必须能够连接到本地端口

> 原
> 文：[Anki must be able to connect to a local port](https://faqs.ankiweb.net/anki-must-be-able-to-connect-to-a-local-port.html)

当 Anki 2.1 启动时，它会在本地主机的一个端口上监听来自用户界面的请求。如果你的机器上配置了代理服务
器，请进入你的代理设置，确保「对本地地址不使用代理服务器」已启用，否则 Anki 的用户界面将通过代理重定
向其本地通信，这将导致 Anki 无法正常工作。

更多信息：<https://superuser.com/a/261434>

如果你的机器上运行了阻止本地连接的防火墙，或者使用了错误重定向本地流量的 VPN，这个问题也可能发生。
