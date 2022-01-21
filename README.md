# ACEQuestion
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
