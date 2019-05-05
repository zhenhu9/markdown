<div id="markdown-headline" />

# Markdown 指北 (Markdown Tutorial)

## 概述 (Overview)

Markdown 是一种轻量级标记语言，创于2004年，关键人物：[John Gruber] 与 [Aaron Swartz]。它的设计旨在可以使人们以易读、易写的纯文本格式写作，并且可以很容易的转换为 PDF、HTML、DOC 或 XHTML 等其他文件格式。Markdown 常应用于格式化自述文件和在线论坛写消息。

由于其简单易用的特性，使其成为世界上最流行的轻量级标记语言之一，并在各类平台上获得了广泛支持，如 GitHub，Bitbucket 等。各平台的衍生版本语法不尽相同，但对基础语法支持很好，而对 Markdown 扩展及其它语法支持和渲染效果有差异化。

[John Gruber]: https://en.wikipedia.org/wiki/John_Gruber

[Aaron Swartz]: https://en.wikipedia.org/wiki/Aaron_Swartz

---

## 打赏或赞助 (Donation)

以上内容都是本小虾收集与整理的，如果您觉得有帮助，欢迎您对我说：“来，喝瓶水！”。

[来，喝瓶水！](https://www.paypal.me/haojiangzhu/5 '来，喝瓶水!')

---

[![LICENSE](https://img.shields.io/badge/license-Anti%20996-blue.svg?style=flat-square)](https://github.com/996icu/996.ICU/blob/master/LICENSE)
<a href="https://996.icu"><img src="https://img.shields.io/badge/link-996.icu-red.svg" alt="996.icu"></a> 

---

## 目录 (Table of Contents)

#### [基础语法 (Basic Syntax)](#anchor-bsyn)

1. [标题 (Headings)](#11-标题-headings)
2. [字体样式 (Decorated Fonts)](#12-字体样式-decorated-fonts)
    * 粗体 (Bold)
    * 斜体 (Italic)
    * 删除线 (Strikethrough)
    * 粗体加斜体 (Bold and Italic)
    * 粗体加删除线 (Bold and Strikethrough)
    * 斜体加删除线 (Italic and Strikethrough)
3. [换行 (Line Breaks)](#13-换行-line-breaks)
4. [文字段落 (Paragraphs)](#14-文字段落-paragraphs)
5. [水平线 (Horizontal Rules)](#15-水平线-horizontal-rules)
6. [块引用 (Blockquotes)](#16-块引用-blockquotes)
7. [列表 (Lists)](#17-列表-lists)
    - 有序列表 (Ordered Lists)
    - 无序列表 (Unordered Lists)
    - 嵌套列表 (Nested Lists)
8. [超链接 (Links)](#18-超链接-Links)
    - 行内样式链接 (Inline-style Links) 
    - 引用样式链接 (Reference-style Links)
    - 自动链接 (Automatic Links)
    - 锚点 (Anchors) 
9.  [图片 (Images)](#19-图片-images)
    - 行内样式图片 (Inline-style Images)
    - 引用样式图片 (Reference-style Images)
    - 图片链接 (Linking Images)
10. [代码 (Codes)](#110-代码-codes)
    - 行内代码 (Inline-style Codes)
    - 代码块 (Code Blocks)
11. [跳脱字符 (Escaping Characters)](#111-跳脱字符-escaping-characters)

#### [扩展语法 (Extended Syntax)](#anchor-esyn)

1. [表格 (Tables)](#21-表格-tables)
2. [标题ID (Heading IDs)](#22-标题ID-heading-ids)
3. [脚注 (Footnotes)](#23-脚注-footnotes)
4. [代码块及语法高亮 (Code Blocks and Syntax Highlighting)](#24-代码块及语法高亮-code-blocks-and-syntax-highlighting)
5. [任务列表 (Task Lists)](#25-任务列表-task-lists)

#### [参考 (References)](#ref)

---

<div id='anchor-bsyn' />

## 基础语法 (Basic Syntax)

#### 1.1 标题 (Headings)

使用字符井号 ‘#’，空格，然后紧接标题名称来设置标题。支持六个级别的标题，字符 ‘#’ 的数量表示相应级别的标题。

一级标题还可以在标题名称紧接着的下一行使用 N 个符号 ‘=’ 来替代井号，二级标题同样可以用 N 个符号 ‘-’ 来替代井号。

示例：

    # H1 一级标题
    ## H2 二级标题
    ### H3 三级标题
    #### H4 四级标题
    ##### H5 五级标题
    ###### H6 六级标题
    H1 一级标题
    =
    H2 二级标题
    -

渲染效果如下：

# H1 一级标题
## H2 二级标题
### H3 三级标题
#### H4 四级标题
##### H5 五级标题
###### H6 六级标题
<h1>H1 一级标题</h1>
<h2>H2 二级标题</h2>

[回到目录](#目录-table-of-contents)

---

#### 1.2 字体样式 (Decorated Fonts)

a. **粗体**  (Bold)
  
在文字左右分别用两个同样字符 ‘*’ 或 ‘_’ 围起来表示应用粗体。

b. **斜体** (Italic)
 
在文字左右分别用单个字符 ‘*’ 或 ‘_’ 围起来表示应用斜体。

c. **删除线** (Strikethrough)

在文字左右分别用两个同样字符 ‘~’ 围起来表示应用删除线。

d. **粗体加斜体**  (Bold and Italic)

粗体加斜体，为嵌套应用。分解为 ‘**’ 和 ‘*’ 。

e. **粗体加删除线** (Bold and Strikethrough)

粗体加删除线，为嵌套应用。分解为 ‘~~’ 和 ‘**’ 。

f. **斜体加删除线** (Italic and Strikethrough)

斜体加删除线，为嵌套应用。分解为 ‘~~’ 和 ‘*’ 。

示例：

    **这是加粗的文字**
    *这是倾斜的文字*
    ~~这是加删除线的文字~~
    ***这是斜体加粗的文字***
    ~~**这是粗体加删除线的文字**~~
    ~~*这是斜体加删除线的文字*~~


渲染效果如下：

**这是加粗的文字**  
*这是倾斜的文字*  
~~这是加删除线的文字~~  
***这是斜体加粗的文字***  
~~**这是粗体加删除线的文字**~~  
~~*这是斜体加删除线的文字*~~  

[回到目录](#目录-table-of-contents)

---

#### 1.3 换行 (Line Breaks)

在行尾使用两个空格加回车来表示换行。

示例：

    虽然此行文字不太长，但我要在此处换行  
    这是换行后的第二行。

渲染效果如下：

虽然此行文字不太长，但我要在此处换行  
这是换行后的第二行。

[回到目录](#目录-table-of-contents)

---

#### 1.4 文字段落 (Paragraphs)

在要设为段落文字下方，使用空行来将其设为段落。

示例：

    这是第一个段落

    这个第二个段落


渲染效果如下：

这是第一个段落

这是第二个段落

[回到目录](#目录-table-of-contents)

---

#### 1.5 水平线 (Horizontal Rules)

使用三个及以上字符 ‘-’ ，‘*’ 或 ‘_’ 都可以创建水平线。

示例：

    ---
    ***
    ___

三种方式其渲染效果等同如下：

---

[回到目录](#目录-table-of-contents)

---

#### 1.6 块引用 (Blockquotes)

在文字行或段落前加符号 ‘>’ 表示块引用。块引用可以嵌套，标示符号数量代表其嵌套层级。

示例：

    >这是引用的内容  
    来个两行
    >>这是嵌套引用的内容
    >>>***这是另一个嵌套引用的内容***
    >>>>>>~~**这是最深层嵌套引用的内容**~~

渲染效果如下：

>这是引用的内容  
来个两行
>>这是嵌套引用的内容
>>>***这是另一个嵌套引用的内容***
>>>>>>~~**这是最深层嵌套引用的内容**~~

__注：__ _块引用可以结合多种其它元素使用。_

[回到目录](#目录-table-of-contents)

---

#### 1.7 列表 (Lists)

a. **有序列表** (Ordered Lists)

在列表条目前使用数字和符号 ‘.’ 表示有序列表 ，符号 ‘.’ 和列表条目之间要有空格。

    1. 列表内容
    2. 列表内容
    3. 列表内容

渲染效果如下：

1. 列表内容
2. 列表内容
3. 列表内容


b. **无序列表** (Unordered lists)

在列表条目前使用单个符号 ‘-’ ， ‘+’ 或 ‘*’ 表示无序列表，列表条目和符号之间要有空格。

    - 列表内容
    + 列表内容
    * 列表内容

渲染效果如下：

- 列表内容
+ 列表内容
* 列表内容


c. **列表嵌套** (Nested Lists)

TAB 缩进或 4 个空格都起到嵌套作用。

    1. 一级有序列表内容
        - 二级无序列表内容
        - 二级无序列表内容

        此处插入一个段落。  
        **多种***元素*。

        - 二级无序列表内容
    2. 一级有序列表内容
        1. 二级有序列表内容
        2. 二级有序列表内容
        >这里是块引用。

**注**： *在有些编辑器中 TAB 健已被设置为代表 4 个空格输出。*

渲染效果如下：

1. 一级有序列表内容
    - 二级无序列表内容
    - 二级无序列表内容

        此处插入一个段落。  
        **多种***元素*。

    - 二级无序列表内容
2. 一级有序列表内容
    1. 二级有序列表内容
    2. 二级有序列表内容
    >这里是块引用。

**注：** *列表可以结合多种其它元素使用。*

[回到目录](#目录-table-of-contents)

---

#### 1.8 超链接 (Links)

a. **行内样式链接** (Inline-style Links)

    [超链接名](超链接地址 "超链接标题 title")

示例：

    [此处为行内样式链接](https://bing.com)

    [此处为具有标题 title 的行内样式链接](http://google.com "权利与傲慢")

渲染效果如下：

[此处为行内样式链接](https://bing.com)

[此处为具有标题 title 的行内样式链接](https://google.com "权利与傲慢")

b. **引用样式链接** (Reference-style Links)

引用样式链接分为两个文本块：

`引用文本块：[超链接名][引用目标]`

`被引用文本块：[被引用目标]: </超链接地址/> "/'/(超链接 title)/'/"`

**注**： *被引用文本块可以单行放在文档任何位置。如果 `[超链接名]` 与 `[被引用目标]` 文本块内容相同，引用文本块的 `[引用目标]` 就可以省略，否则 `[引用目标]`和 `[被引用目标]` 的文本内容必须相同。*

*用来围住超链接的符号 ‘<>’ 可以省略。`超链接标题 titile` 可以用符号 ‘"’ ， ‘'’ 或 ‘()’ 围起来。*

示例：

    [此处为引用样式链接][任意不区分大小写文本或数字]

    [任意不区分大小写文本或数字]: https://www.facebook.com '面子的成本'

    [我和引用目标同名]

    [我和引用目标同名]: <https://www.twitter.com> "道场"

渲染效果如下：

[此处为引用样式链接][任意不区分大小写文本或数字]

[任意不区分大小写文本或数字]: https://www.facebook.com '面子的成本'

[我和引用目标同名]

[我和引用目标同名]: <https://www.twitter.com> "道场"

c. **自动链接** (Automatic Links)

示例：

    欢迎使用域名样例网站： <http://www.example.com>

    如有疑问请联系：<iana@iana.org>

    直接使用链接地址同样有效 http://www.example.com



渲染效果如下：

欢迎使用域名样例网站：<http://www.example.com>

如有疑问请联系： <iana@iana.org>

直接使用链接地址同样有效： http://www.example.com

d. **锚点** (Anchors)

锚点，也叫命名锚记，是页面内的定位器，通过链接访问可以直接跳转到页面的锚点部位。

在 markdown 中标题可以直接作为锚点，其它处可用 html 标记来生成锚点。

    html锚点:

    <a name="anchor1">你在找我吗？</a>
    或任何其它具有 id 的 html 标签，如：
    <div id="anchor2">你还在找我吗？</div>
    <a id="anchor3">你真的在找我吗？</a>

渲染效果如下：

html锚点:

<a name="anchor1">你在找我吗？</a>  

或任何其它具有 id 的 html 标签，如：
<div id="anchor2">你还在找我吗？</div>  
<a id="anchor3">你真的在找我吗？</a>


锚点引用方式如下：

    [超链接名称](#锚点)

**注**：*当标题作为锚点在引用时，锚点内容中大写字母要转为小写；中文不变；半角标点符号要直接去掉（虽然在某些平台的 markdwon 中可以不去掉也有效）；全角标点符号各平台 markdown 中解析有差异，不建议使用；空白字符要替换为符号 ‘-’ 。*

示例：

    [跳转到此小结标题处](#18-超链接-links)
    [我在找你啊](#anchor1)  
    [我还在找你啊](#anchor2)  
    [我真的在找你啊](#anchor3)

渲染效果如下：

[跳转到此小结标题处](#18-超链接-links)  
[我在找你啊](#anchor1)  
[我还在找你啊](#anchor2)  
[我真的在找你啊](#anchor3)

[回到目录](#目录-table-of-contents)

---

#### 1.9 图片 (Images)

a. **行内样式图片** (Inline-style Images)

    ![图片 alt](图片地址 "图片 title")

`图片 alt` 是当图片无法显示时的替代文字。  
`图片 title` 是图片的标题，当鼠标移到图片上时显示的文字内容。  
`图片 title` 非必需。

b. **引用样式图片** (Reference-style Images)

    ![图片 alt][引用目标]

    [被引用目标] </图片地址>/ "/'/(图片 title)/'/"

**注**： *引用样式图片与引用样式链接类似，引用块前有个符号 ‘!’。*

示例：

    ![beautiful sky](http://www.ottawafamilyliving.com/writeable/editor_uploads/images/images/manalone.jpg "璀璨星空")

    ![beautiful sky](./images/manalone.jpg "璀璨星空")

    ![beautiful sky][beau-sky]

    [beau-sky]：./images/manalone.jpg "璀璨星空"

渲染效果如下：(三种方式的效果相同)

![beautiful][beau-skyone]

[beau-skyone]: ./images/manalone.jpg "璀璨星空"

c. **图片链接** (Linking Images)

    [![图片 alt](图片地址 "图片 title")](图片链接地址 "链接 title")

**注:** *链接语法嵌套图片语法。*

    [![勇敢者的游戏](images/freesolo.jpg "勇敢者的游戏")](https://www.nationalgeographic.com/films/free-solo/)

渲染效果如下:

[![勇敢者的游戏](images/freesolo.jpg "勇敢者的游戏")](https://www.nationalgeographic.com/films/free-solo/)

[回到目录](#目录-table-of-contents)

---

#### 1.10 代码 (codes)

a. **行内代码** (Inline-style Codes)

代码两边分别用一个符号反引号 ‘`’ 围起来。

    `代码内容`

**注**：*当代码内容中有反引号时，在代码内容两边使用两个反引号。*

示例：

    `echo "Hello World!"`
    ``create `database` example;``

渲染效果如下：

`echo "Hello World!"`  
 ``create `database` example;``


b. **代码块** (Code blocks)

在每行代码行前使用 TAB 缩进或 4 个空格。如果在列表中就必须使用两个 TAB 缩进或 8 个空格。

渲染效果如下：

    #!/bin/bash
    function say_hello(){
        echo "Hello World!";
    }
    say_hello

**注**: *在扩展语法中，将介绍另一种代码块语法，并能实现指定语法高亮。*

[回到目录](#目录-table-of-contents)

---

#### 1.11 跳脱字符 (Escaping Characters)

为了显示功能性字符，要取消其功能性作用，就需对相应字符进行转义。转义字符为 ‘\’。

示例:

    \*\*二级标题
    \- 无序列表
    \-\-\- 水平线

渲染效果如下：

\*\*二级标题  
\- 无序列表  
\-\-\- 水平线

**可以被转义的字符表**

| 字符 | 名称   | 英文对照            |
| ---- | ------ | ------------------- |
| \    | 反斜线 | backslash           |
| `    | 反引号 | backtick (back quote) |
| *    | 星号   | asterisk            |
| _    | 下划线 | underscore          |
| {}   | 大括号 | curly braces        |
| []   | 中括号 | brackets            |
| ()   | 括号   | parentheses         |
| #    | 井号   | pound sign (hash)   |
| +    | 加号   | plus sign           |
| -    | 减号   | minus sign (hyphen) |
| .    | 点     | dot                 |
| !    | 感叹号 | exclamation mark    |
| \|   | 管道   | pipe                |

**注**： *为了在表单中显示管道，对其进行转义* `\|`*，也可以直接使用其 HTML代码 `&#124;`，也可以达到同样效果。*

[回到目录](#目录-table-of-contents)

---

<div id='anchor-esyn' />

## 扩展语法 (Extended Syntax)

#### 2.1 表格 (Tables)

    | 表头   | 表头   | 表头   |
    | :----- | :----: | -----: |
    | 表单元 | 表单元 | 表单元 |

1. 字符 ‘|’ 分隔表列。
2. 字符 ‘-’ 三个或三个以上表示其上一行为表头。
3. 字符 ‘:’ 在左边表示左对齐，右边为右对齐。两边都有，表示居中。缺省为左对齐。
4. 字符 ‘|’ 在列表每行首尾可以省略。


示例:

    Markdown 综合属性

    | 特点 | 应用的网络平台    | 编辑器       | 关联软件及语言 |
    | ---- | ---------------- | ------------- | -------------- |
    | 轻量 | [Github]         | [VScode]      | [Git]          |
    | 简单 | [WordPress]      | [Atom]        | [Pandoc]       |
    | 易学 | [Stack Overflow] | [MarkdownPad] | [HTML]         |

    [Github]: https://github.com/
    [WordPress]: https://wordpress.com/
    [Stack Overflow]: https://stackoverflow.com/
    [VScode]: https://code.visualstudio.com/?wt.mc_id=DX_841432
    [Atom]: https://atom.io/
    [MarkdownPad]: http://markdownpad.com/
    [Git]: https://git-scm.com/
    [Pandoc]: http://www.pandoc.org/
    [HTML]: https://www.w3.org/html/

效果如下：

Markdown 综合属性
    
| 特点 | 应用的网络平台   | 编辑器        | 关联软件及语言 |
| ---- | ---------------- | ------------- | -------------- |
| 轻量 | [Github]         | [VScode]      | [Git]          |
| 简单 | [WordPress]      | [Atom]        | [Pandoc]       |
| 易学 | [Stack Overflow] | [MarkdownPad] | [HTML]         |

[Github]: https://github.com/
[WordPress]: https://wordpress.com/
[Stack Overflow]: https://stackoverflow.com/
[VScode]: https://code.visualstudio.com/?wt.mc_id=DX_841432
[Atom]: https://atom.io/
[MarkdownPad]: http://markdownpad.com/
[Git]: https://git-scm.com/
[Pandoc]: http://www.pandoc.org/
[HTML]: https://www.w3.org/html/

**注**： *可以在表单中结合其它元素。*

[回到目录](#目录-table-of-contents)

---

#### 2.2 标题ID (Heading IDs)

标题ID本质上说是属于HTML标题标签的id属性，其具有唯一性，方便引用于其它操作。正如我们在链接中的锚点中引用一样，当我们可以设置标题引用目标，就不用去转换大小写字母等等繁琐步骤了。

标题部分：  #### 标题内容 {#自定义id名称}

链接标题：　\[链接名称\]\(#自定义id名称\)

示例：

    #### 样例标题 {#soeasyid}

    [一点就到样例标题了](#soeasyid)

渲染效果如下：

<h4 id="soeasyid">样例标题</h4>

<a href="#soeasyid">一点就到样例标题了</a>

**注**： *示例生成的两行 html 代码分别为：`<h4 id="soeasyid">样例标题</h4>`，`<a href="#soeasyid">一点就到样例标题了</a>`*。

[回到目录](#目录-table-of-contents)

---

#### 2.3 脚注 (Footnotes)

脚注类似于引用样式链接，也分为两部分：

引用部分： [^引用目标]

被引用部分：[^引用目标]： 被引用文本内容

**注**： *被引用文本的段落可以通过使用 TAB 行首缩进或 4 个空格持续添加。*

示例：

    此处有一个脚注，[^1] 这里还有一个更长的脚注。[^bignote]

    [^1]: 1.这是第一个脚注。

    [^bignote]: 2.这是一个包含多个段落和代码的脚注。

        使用TAB缩进或四个空格包含这些段落到脚注中。

        `{ my code }`

        您可以持续添加您需要的文本段落。

渲染效果如下:

<p>此处有一个脚注，<a href="#fn1" class="footnote-ref" id="fnref1"><sup>1</sup></a> 这里还有一个更长的脚注。<a href="#fn2" class="footnote-ref" id="fnref2"><sup>2</sup></a></p>
<hr />
<ol>
<li id="fn1"><p>这是第一个脚注。<a href="#fnref1" class="footnote-back">↩</a></p></li>
<li id="fn2"><p>这是一个包含多个段落和代码的脚注。</p>
<p>使用TAB缩进或四个空格包含这些段落到脚注中。</p>
<p><code>{ my code }</code></p>
<p>您可以持续添加您需要的文本段落。<a href="#fnref2" class="footnote-back">↩</a></p></li>
</ol>

[回到目录](#目录-table-of-contents)

---

#### 2.4 代码块及语法高亮 (Code Blocks and Syntax Highlighting)

在基础语法中，我们在每行代码前使用TAB或4个空格来表示代码块。扩展语法中我们还可以在代码段首尾分别用三个字符 ‘`’ 或 ‘~’ 围起来，且各自独占一行。

如果我们在代码块语法的首个三个字符后指定代码语言，还能实现相应代码的高亮效果。

    ```
    代码...
    代码...
    代码...
    ```

示例：

    ```bash
    #!/bin/bash
    function say_hello(){
        echo "Hello World!";
    }
    say_hello();
    ```

渲染效果如下：

```bash
#!/bin/bash
function say_hello(){
    echo "Hello World!";
}
say_hello
```

[回到目录](#目录-table-of-contents)

---

#### 2.5 任务列表 (Task Lists)

任务列表使用字符 ‘-’ ，‘[　]’ 和列表条目三个部分来表示一行列表，三个部分之间要有空格。第二个部分 ‘[　]’ 表示未选任务列表， ‘[x]’ 表示已选任务列表。

示例：

    - [x] 已选列表条目1
    - [x] 已选列表条目2
    - [ ] 未选列表条目3

渲染效果如下：

- [x] 已选列表条目1
- [x] 已选列表条目2
- [ ] 未选列表条目3

[回到目录](#目录-table-of-contents)

---

<div id="ref" />

## 参考 (References)

[Markdown](https://en.wikipedia.org/wiki/Markdown) wiki百科

[Markdown Guide](https://www.markdownguide.org) Matt Cone

[Markdown-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) Adam Pritchard

---

[回到页首](#markdown-headline)
