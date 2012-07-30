
[https://github.com/vimcn vimcn]

- <leader>ww 在当前窗口打开维基首页
- <leader>wt 在新tab打开维基首页
- <leader>w<leader>w 打开/新建当天日记
- <leader>w<keader>t 在新tab打开/新建当天日记
- <leader>ws 选择维基项目
- <leader>w<leader>i 生成日记的索引


编辑时的按键

尚未建立的词条会被显示为红色（或其他你的 Vim 语法高亮定义的错误颜色），在词条上敲回车键，可以编辑这个词条。<br/>  

点击 Shift-回车，在新的分割窗口编辑该词条。编辑好以后点击退格（Backspace）键，可以返回链入页 

Tab 键，可以跳到下一个维基词条或链接，使用 Shift-Tab 跳到上一个 插入模式下使用Shift-Enter，插入 <br> 并换行

在标题上点击 - 和 = （也就是 - 和 + ），可以分表提升和降低标题层级

另有条目管理相关的快捷键 <leader>wd 和 <leader>wr ，分表代表删除和重命名当前条目。其中重命名条目很强大，
还能更改所有其他条目内引用了该条目的链接。 重命名之后别忘了重新生成所有条目的HTML。 

----
markdown语法也可以在vimwiki中使用，配置很方便修改，但有些不伦不类的感觉，放弃折腾。

wiki链接替换成markdown链接
:%s/\[\[/\[/g
:%s/\]\]/\]\()/g

[markdown链接语法的修改](vimwiki_markdown_link_modify.patch)
