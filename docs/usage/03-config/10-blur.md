# 配置 blur 函数

配置`blur`函数之后，如果当前有手动获取焦点的富文本并且鼠标点击富文本以外的区域，则会触发`blur`函数执行。

```html
<div id="div1">
    <p>欢迎使用 wangEditor 富文本编辑器</p>
</div>

<p>手动触发 onchange 函数执行</p>
<button id="btn1">change</button>

<script type="text/javascript" src="/wangEditor.min.js"></script>
<script type="text/javascript">
    var E = window.wangEditor
    var editor = new E('#div1')
    editor.customConfig.blur = function (html) {
        // html 即编辑器中的内容
        console.log(html)
    }
    editor.create()

</script>
```

