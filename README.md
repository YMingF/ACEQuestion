# ACEQuestion
#非常有可能的原因
> 没有给对应标签设置一个固定的高度！！！！
# 写法1
```

var htmEditor;
$.getScript('//cdnjs.cloudflare.com/ajax/libs/ace/1.1.3/ace.js',function(){
  $.getScript('//cdnjs.cloudflare.com/ajax/libs/ace/1.1.3/ext-language_tools.js',function(){

      ace.require("ace/ext/language_tools");
    
      htmEditor = ace.edit("htmEditor");
      htmEditor.getSession().setMode("ace/mode/html");
      htmEditor.setTheme("ace/theme/merbivore");
      htmEditor.setOptions({
            enableBasicAutocompletion: true,
            enableSnippets: true
      });
      
      htmEditor.setShowPrintMargin(false);
      htmEditor.setHighlightActiveLine(false);
      
      
  });
});
```

# 确保已包含适当的ACE js脚本，并为其容器设置了特定的高度。

## 方法3
```
>检查Ace是否已将其他div添加到< div id =“ editor”>中,如果没有,则控制台中一定存在js错误.
>如果Ace存在但不可见,请从< div id =“ editor”>中删除所有文本.并在ace.edit行中注释掉以查看ace的尺寸(ace尝试匹配该div的高度)
>如果问题确实是Ace获得height = 0,则可以在编辑器div中添加明确的高度,
>,或者如果您希望它适合文本,请设置maxLines和minLines选项,如https://github.com/ajaxorg/ace-builds/blob/v1.1.6/demo/autoresize.html#L41-L43所示,但是建议不要将maxLines设置得太大,因为它会禁用仅绘制可见文本的优化,并且会使大型文档的编辑器变慢.
```
