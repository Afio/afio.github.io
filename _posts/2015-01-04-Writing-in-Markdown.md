---
layout: post
title:  "Writing in Markdown "
date:   2015-01-04 20:00:00
categories: markdown
header-img: "img/post-bg-02-mrakdown.jpg"
---

### Markdown 介绍

> The overriding design goal for Markdown’s formatting syntax is to make it as readable as possible. *John Gruber*

Markdown 是一种轻量级标记语言，致力于使阅读和创作文档变得容易。它可以使用易读易写的纯文本格式写文档，然后转换成 HTML 及 PDF 等其他通用格式文档。另外 Markdown 兼容 HTML ，可以直接在文档里面用 HTML 标签，不需要额外标注这是 HTML 或是 Markdown。

### Markdown 编辑器

大概11年-12年接触到 Markdown，那时候编辑器工具和生态远没有现在丰富，简单找一圈发现最好用的是网页版编辑器  `dillinger.io` （当时用了一阵就转投 `Workflowy` 了，再后来又重新回归 `Evernote` ）直到 <a href="http://25.io/mou" target="_blank">Mou</a> 出现后才一直作为本地编辑器使用。

*update：Mou 不支持 Mac OS 10.12 以上版本，现在用  <a href="https://macdown.uranusjr.com" target="_blank">Macdown</a> 代替了，界面见下*

![macdown_screenshot](https://xqimg.imedao.com/16be49a10daa3fec1db2ee35.jpg)

### Markdown 常用语法

因为目前 GitHub Pages 已统一只支持 kramdown 作为唯一的 Markdown 解析引擎（据说解析速度最快），在常用语法上 kramdown 语法与通用 Markdown 基本一致，但个别地方还是有细微不同，下面具体备注了。

**1. 标题**

用井号代表对应分级标题，井号越多标题越小，效果等同于  `<h1><h2><h3>` 标签。 不过在 kramdown 语法中，标题前须有一个空格。

~~~
# 一级标题           
## 二级标题          
### 三级标题      
~~~
<br>
**2. 列表**

无序列表使用星号 * 加号 + 或减号 - 来做为列表的项目标记（已养成下意识按出减号的习惯），有序列表使用数字加英文句号。对于列表 List 来说格式非常自然，效果等同于 `<ul><ol><li>` 标签。另外注意列表符号与内容中间都需要一个英文空格。

~~~
 - 无序列表a       1. 有序列表1      
 - 无序列表b       2. 有序列表2   
 - 无序列表c       3. 有序列表3     
~~~
<br>

**3. 字体**

- 粗体：`**加粗文字**` （等同于`<b><em><strong>`标签）
- 斜体：`*斜体文字*` （等同于`<i>`标签）
- 删除线：`~~删除线文字~~` （等同于`<s><del>`标签）
<br>
**4. 代码**

行内代码直接用单个反引号 \` 引起来部分为代码块，效果等同于 `<code>` 标签。成块的代码可以用三个反引号（ kramdown语法中用 \~~~ 来上下包裹且行内代码前后不能有空格），如需按指定语言高亮可在开头反引号后添加代码语言。

\~~~ sql<br>
SELECT * from default.sample LIMIT 10<br>
\~~~ 

**5. 外链**

格式为 `[链接内容](链接地址)`  ，效果等同于 `<a href="链接地址">链接内容</a>` 。习惯新标签页面打开的话，可以在 `<a>` 标签内加上 `target="_blank"` 属性。  

**6. 插图**

类似外链，格式为 `![描述](图片链接地址)` ，效果等同于 `<img src="图片链接地址" alt="描述">`。

如有指定图片尺寸大小或居中等自定义排版需求可使用 HTML 标签如 `<img src="图片链接地址" alt="描述" align="right" width="100" height="100">` 来实现。

**7. 引用**

使用 `>` 代表引用格式，注意需保留一个空格，效果等同于 `<blockquote>` 标签。引用内嵌套引用可使用 `>>` ，另外在引用中也支持其他 Markdown 语法。

**8. 表格**

直接在 Excel 或 Numbers 里搞好然后截图展示吧，既省时兼容性又好 :-)

**9. 分割线**

使用三个或更多的星号 `***`  或下划线 `---` 即可，效果等同于 `<hr>` 标签。

<br>
**Reference**

- <a href="https://www.appinn.com/markdown/" target="_blank">Markdown 语法说明 (简体中文版)</a>
- <a href="https://spec.commonmark.org/0.29/" target="_blank">Markdown 官方网站</a>
- <a href="https://zh.wikipedia.org/wiki/Markdown" target="_blank">Markdown 维基百科</a>
- <a href="https://kramdown.gettalong.org/syntax.html" target="_blank">kramdown官方语法</a>

