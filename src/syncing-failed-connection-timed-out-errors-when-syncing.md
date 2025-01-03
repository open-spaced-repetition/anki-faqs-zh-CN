# 「同步失败：连接超时」错误

> 原
> 文：['Syncing failed: Connection timed out' errors when syncing](https://faqs.ankiweb.net/syncing-failed-connection-timed-out-errors-when-syncing.html)

**Windows 上的杀毒软件/防火墙和公司/学校网络**

如果同步似乎从未取得任何进展，可能是 Anki 完全被阻止连接到互联网。在这种情况下，你可能需要在杀毒软件
/防火墙中添加一个例外，或者请网络管理员协助。更多信息，请参阅

<https://open-spaced-repetition.github.io/anki-faqs-zh-CN/error-establishing-a-secure-connection-when-syncing.html>

**如果同步似乎有一些进展**

当你进行同步时，Anki 会向 AnkiWeb 发送消息，这些消息通常需要经过多个网络和国家才能到达 AnkiWeb。如果
你和 AnkiWeb 服务器之间的某个网络出现问题，可能会导致连接速度变慢或突然中断。

通常造成这种情况的原因是你的互联网服务提供商在其国际连接中出现了问题。当这种情况发生时，你可能会发现
可以正常访问其他大多数网站，因为那些网站的托管地点不同，因此连接到它们使用的是不同的网络。此类问题通
常需要几个小时到几天才能解决。

有时问题可能更本地化。如果你使用的是一个遥远或拥挤的 wifi 网络，也会导致与 AnkiWeb 的连接变得不稳
定。

传输的数据越多，不稳定的连接越容易显现。如果你遇到数据包丢失的情况，你可能会发现大多数时间仍能正常加
载 ankiweb.net，但在同步时仍会遇到问题——特别是当你需要传输大量数据时。

**解决问题的方法**

最好的方法是尝试在不同的网络上进行同步——例如，使用手机的移动网络，或者使用工作单位或学校的 wifi 网
络。在许多情况下，这可以解决问题，并且在等待几个小时到几天后，家庭网络的问题应该会消失。

**确定数据包丢失**

一个名为『mtr』的工具可以用于确定数据包丢失。

- Windows: <https://sourceforge.net/projects/winmtr/>
- Mac: <https://www.reddit.com/r/TagPro/comments/2j6qx7/how_to_run_an_mtr_on_mac/>
- Linux: 从软件包管理器中安装『mtr』

安装后，你应该使用 mtr 访问『ankiweb.net』，并让它运行大约 15 分钟。如果从你的设备到 AnkiWeb 服务器
之间的任何步骤显示数据包丢失超过 0%，则表明连接不稳定。

如果你没有看到任何数据包丢失但仍然在同步时遇到问题，你可能遇到了不同的问题——请联系我们并告知我们。
