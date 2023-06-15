<%* if (tp.file.title.startsWith("Hello")) { %>
This is a hello file !
<%* } else { %>
This is a normal file !
<%* } %>
    
<%* if (tp.frontmatter.type === "seedling") { %>
This is a seedling file !
<%* } else { %>
This is a normal file !
<%* } %>
    
<%* if (tp.file.tags.contains("#todo")) { %>
This is a todo file !
<%* } else { %>
This is a finished file !
<%* } %>

<%*
function log(msg) {
    console.log(msg);
}
%>
<%* log("Title: " + tp.file.title) %>
    
<%* tR += tp.file.content.replace(/stuff/, "things"); %>
***
来源：[Execution Commands - Templater (silentvoid13.github.io)](https://silentvoid13.github.io/Templater/commands/execution-command.html)
心得：
- <%* R = 123 %> //这个 < %* 是同步执行，不输出
- <% R %> //这个< % 将输输出R的值
- await 多线程执行 异步
- 标记 （） **开头**的下划线将修剪命令**之前****的所有**空格`_``< %_`
- 标记 （） **末尾**的下划线将修剪命令**后****的所有**空格`_``_%>`
- 标记 （） **开头**的短划线将修剪命令**前****的一个**换行符`-``< %-`
- 标记 （） **末尾**的短划线将修剪命令**后****的一个**换行符。`-``-%>`

<%* 
const nameVar = "0"
const templateVar = tp.file.find_tfile("411_日记模板")
await tp.file.create_new(templateVar, nameVar)
%>
