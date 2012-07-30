=== 基本的 Wiki 语法 ===

{{{
= 一级标题 =  
== 二级标题 ==
=== 三级标题 ===
此次类推。

当标题前面有空白时，标题文本居中对齐。
       = 我是居中的标题 =

*<b>粗体</b>*  _<i>斜体</i>_  ~~<del>删除线</del>~~   `<code>Some Code 代码</code>` 

<b>注意</b> 这几个针对文本格式的标签，都要求左右留有空白。
请注意你的代码高亮，一般来说，有了相应的高亮，你用的wiki标签才生效。

^<sup>上</sup>^标  ,,<sub>下</sub>,,标

    四个空格缩进的内容会被转成blockquote
    
\{\{\{ class="brush:php"
这中间的内容会被放到一个 pre 里，适合贴代码。
上面的 class 是可选的，一般用来安排代码高亮。
事实上，这一块代码展示就是放在了一个 pre 里。
请无视下面一行的反斜杠
\}\}\}

<code>WikiItem</code>  大写开头的驼峰英文会被自动当作一个维基词条，并添加链接
<code>[[Wiki Item]]</code>  这是手动建立维基词条的方式
<code>[[wiki item|description]]</code>  输出HTML时显示description，链到 wiki item
<code>http://ktmud.com/</code>  外部URL会被自动转换成链接
<code>[http://ktmud.com Ktmud]</code>  带文字的外链
<code>[images/hello.jpg]</code> 输出 <img src="images/hello.jpg" />
<code>[[images/hello.jpg]]</code> 输出图片，并链向图片地址

* 无序列表 条目一
* 无序列表 条目二 
  - 子列表 条目一
  - 自列表 条目二

# 有序列表 条目一
# 有序列表 条目二

* 和 - 是等价的，后面必须跟一个空格

}}}


*参考* `:h vimwiki-syntax` 
