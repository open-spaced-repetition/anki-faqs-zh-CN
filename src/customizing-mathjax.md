# 自定义 MathJax

Anki 自带的 MathJax 支持在你的卡片内容加载之前加载，因此如果你想自定义 MathJax，需要以特定的方式进
行。

对于最近版本的 Anki，请使用如下代码：

```html
<script>
  MathJax.config.tex["macros"] = {
    R: "{\\mathbb {R}}",
  };
  if (typeof is_already_run == "undefined") {
    is_already_run = true;
    MathJax.startup.getComponents();
  }
</script>
```

对于较早版本的 Anki：

```html
<script>
  MathJax.Hub.Config({
  ...
  });
  MathJax.Hub.Configured();
</script>
```

注意：

- 请避免将标准的打开/关闭标签（`\(` 和 `\[`）更改为类似 `$` 和 `$$` 的其他符号，因为 Anki 为完形填空
  删除有特殊的逻辑，如果你更改了分隔符，该功能将不起作用。
