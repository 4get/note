
= 快捷操作 =
在vim里面编译:make，然后:cw看编译的结果，一般会跳到报error的那一行，回车就可以看到代码。

写代码的时候ctrl+p/n补全已经有的标号(token)。

光标放在文件路径上，gf进入。

光标放在路径上，gd跳到定义。

ctrl+6 在打开的两个文件间切换，
:ls 查看打开的文件， :b1跳到相应的文件。

ctrl+5匹配括弧。

ctrl+v列选择，按c删除选择并插入，按i插入。

光标放在标号上 ]I 列出全部匹配

shirt+~ 大小写改变



= tag =
ctrl+]进入函数，ctrl+t返回。

:tj xxx 跳到xxx。

:ts 查看跳转栈。


标签功能

[http://liyanrui.is-programmer.com/posts/1857.html]
- :tabnew filename
- :tabf filename_re
- map <S-Left> :tabp<CR>
- map <S-Right> :tabn<CR>

