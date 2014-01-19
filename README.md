UESTC Bachelor's Thesis with XeLaTeX
================================
adapted by Richard (Fangjian) Guo <<richardkwo at gmail.com>>.

此模板基于 Shi Fujun <shifujun at foxmail.com> 的 UESTCthesis 模板 (https://github.com/shifujun/UESTCthesis).

我在2013年夏天写毕业论文的时候做了一些改进，这里是改进后的版本。主要改进的地方包括：

* 使用 XeLaTeX 来排版中文。停止使用过时的CJK解决方案。
* 对原模板本科论文的格式做了调整。（我自己的论文正文是英文，因此模板用来写英文的本科毕业论文是没有问题的，中文没有测试过）
* 可以原生地使用 xelatex 和 bibtex 编译。抛弃了命令行脚本。
* 替换了一些过时的宏包，如kmath
* 用natbib生成参考文献，并修改了引用样式

文件说明
-------------------------

    ├── uestcthesis.bst    参考文献格式定义
    ├── uestcthesis.cls    documentclass 定义
    ├── Ch1_Introduction.tex    样例 Thesis_Guo2013 的第一章 *
    ├── Ch2_DivergingMomentAsymptotics.tex    样例 Thesis_Guo2013 的第二章 *
    ├── Ch3_MemoryConstraints.tex    样例 Thesis_Guo2013 的第三章 *
    ├── Ch4_Conclusion.tex    样例 Thesis_Guo2013 的第四章 *
    ├── Thesis_Guo2013.tex    样例 Thesis_Guo2013 的主文件 *
    ├── contents/    
    │   ├── Cabstract.tex    中文摘要 *
    │   ├── Eabstract.tex    英文摘要 *
    │   ├── acknowledgements.tex    致谢 *
    │   ├── appendix.tex    附录 *
    │   ├── original.pdf    译文原文（附在本科论文结尾） *
    │   ├── publications.bib    个人文章发表情况（可不用）
    │   ├── reference.bib    参考文献数据库 *
    │   ├── titlepage.tex    标题页 *
    │   └── translation.pdf    译文（附在本科论文结尾） *
    ├── figures/    插图目录 *
    ├── logo.pdf    校徽
    ├── logo.tex    校徽tex定义

其中 * 表明需要用户修改的文件。

使用方法
------------------------

The above header should be an H2 tag. Now, for a list of fruits:

* Red Apples
* Purple Grapes
* Green Kiwifruits

Let's get crazy:

1.  This is a list item with two paragraphs. Lorem ipsum dolor
    sit amet, consectetuer adipiscing elit. Aliquam hendrerit
    mi posuere lectus.

    Vestibulum enim wisi, viverra nec, fringilla in, laoreet
    vitae, risus. Donec sit amet nisl. Aliquam semper ipsum
    sit amet velit.

2.  Suspendisse id sem consectetuer libero luctus adipiscing.

What about some code **in** a list? That's insane, right?

1. In Ruby you can map like this:

        ['a', 'b'].map { |x| x.uppercase }

2. In Rails, you can do a shortcut:

        ['a', 'b'].map(&:uppercase)

Some people seem to like definition lists

<dl>
  <dt>Lower cost</dt>
  <dd>The new version of this product costs significantly less than the previous one!</dd>
  <dt>Easier to use</dt>
  <dd>We've changed the product so that it's much easier to use!</dd>
</dl>

I am a robot
------------

Maybe you want to print `robot` to the console 1000 times. Why not?

    def robot_invasion
      puts("robot " * 1000)
    end

You see, that was formatted as code because it's been indented by four spaces.

How about we throw some angle braces and ampersands in there?

    <div class="footer">
        &copy; 2004 Foo Corporation
    </div>

Set in stone
------------

Preformatted blocks are useful for ASCII art:

<pre>
             ,-. 
    ,     ,-.   ,-. 
   / \   (   )-(   ) 
   \ |  ,.>-(   )-< 
    \|,' (   )-(   ) 
     Y ___`-'   `-' 
     |/__/   `-' 
     | 
     | 
     |    -hrr- 
  ___|_____________ 
</pre>

Playing the blame game
----------------------

If you need to blame someone, the best way to do so is by quoting them:

> I, at any rate, am convinced that He does not throw dice.

Or perhaps someone a little less eloquent:

> I wish you'd have given me this written question ahead of time so I
> could plan for it... I'm sure something will pop into my head here in
> the midst of this press conference, with all the pressure of trying to
> come up with answer, but it hadn't yet...
>
> I don't want to sound like
> I have made no mistakes. I'm confident I have. I just haven't - you
> just put me under the spot here, and maybe I'm not as quick on my feet
> as I should be in coming up with one.

Table for two
-------------

<table>
  <tr>
    <th>ID</th><th>Name</th><th>Rank</th>
  </tr>
  <tr>
    <td>1</td><td>Tom Preston-Werner</td><td>Awesome</td>
  </tr>
  <tr>
    <td>2</td><td>Albert Einstein</td><td>Nearly as awesome</td>
  </tr>
</table>

Crazy linking action
--------------------

I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"
