# 语音合成支持

> 原文：[Text-to-speech support](https://faqs.ankiweb.net/text-to-speech-support.html)

<h1>适用于 Anki 2.1.20+</h1>

请参见
<https://open-spaced-repetition.github.io/anki-manual-zh-CN/templates/fields.html#单个字段的文字转语音>

<h1>适用于 AnkiMobile 2.0.56+</h1>

请参见 <https://docs.ankimobile.net/tts.html>

<h1>适用于 AnkiDroid</h1>

请在 AnkiDroid 使用手册中搜索 TTS。

<h1>适用于旧版 Anki</h1>

有一个受欢迎的插件叫做 AwesomeTTS，支持多种语音合成程序和服务。你可以在这里了解更多信息：

<https://ankiweb.net/shared/info/814349176>

它通过将音频下载到你的集合中工作，这样当你与 AnkiWeb 同步时，你的其他设备也可以访问这些音频。

如果你想在电脑版本之外使用生成的文件，请确保使用存储文件模式而不是『即时生成』。

虽然 AnkiMobile 2.0.56 以下版本没有官方的设备端 TTS 支持，但苹果在 iOS7 中引入了 TTS 支持，可以访问
它。以下是基于用户贡献的解决方案。

```html
<span id="word">{{Word}}</span>

<script>
  var w = document.getElementById("word");
  window.setTimeout("speak(w.innerHTML)", 500);

  function speak(word) {
    var speech = new SpeechSynthesisUtterance();
    speech.text = word;
    speech.volume = 1; // 0 到 1
    speech.rate = 1; // 0.1 到 9
    speech.pitch = 1; // 0 到 2，1 表示正常
    speech.voice = window.speechSynthesis.getVoices().filter((v) => v.lang == "en-GB")[0];
    speechSynthesis.cancel();
    speechSynthesis.speak(speech);
  }
</script>
```

你可以将 en-GB 更改为其他语言，如 en-US、de-DE、ja-JP、zh-HK 等。你可以使用以下页面的示例部分来查看
所有不同的语言。<https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesis/getVoices>

你可能需要为要播放的语言安装增强音频文件，你可以通过设置应用，然后是通用、辅助功能、语音和声音来进行
安装。
