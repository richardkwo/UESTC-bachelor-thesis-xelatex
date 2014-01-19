UESTC Bachelor's Thesis with XeLaTeX
================================
Adapted by Richard (Fangjian) Guo ( https://github.com/richardkwo ), graduate of UESTC.

Distributed uner LPPL (http://www.latex-project.org/lppl.txt ).

此模板基于 Shi Fujun (shifujun at foxmail.com) 的 UESTCthesis 模板 (https://github.com/shifujun/UESTCthesis )，在此向原作者表达谢意。

我在2013年夏天写毕业论文的时候做了一些改进，这里是改进后的版本。主要改进的地方包括：

* 使用 XeLaTeX 来排版中文。停止使用过时的CJK解决方案。
* 对原模板本科论文的格式做了调整。（我自己的论文正文是英文，因此模板用来**写英文的本科毕业论文是没有问题的，中文没有测试过**）
* 可以原生地使用 xelatex 和 bibtex 编译。抛弃了命令行脚本。
* 替换了一些过时的宏包，如kmath
* 用natbib生成参考文献，并修改了引用样式
* **由于相隔快一年，我实际上也忘了我做了什么....**

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

依赖环境
------------------------
win/linux/osx 在安装tex发行后都可以顺利编译。

bibtex，一般的tex发行中包含。

xelatex，一般的tex发行中包含，请确认安装了中文字体。参考

* http://linux-wiki.cn/wiki/zh-hans/LaTeX%E4%B8%AD%E6%96%87%E6%8E%92%E7%89%88%EF%BC%88%E4%BD%BF%E7%94%A8XeTeX%EF%BC%89


使用方法
------------------------

1.  将此 repo 克隆或下载到本地。可以使用命令

        git clone https://github.com/richardkwo/UESTC-bachelor-thesis-xelatex.git

2.  确保你可以正确编译样例论文 Thesis_Guo2013.tex。Thesis_Guo2013.pdf 是我得到的结果，你可以先移去它。
    运行编译命令（一般的tex编辑器会提供这些命令）

        xelatex Thesis_Guo2013.tex
        bibtex Thesis_Guo2013.tex
        xelatex Thesis_Guo2013.tex
        xelatex Thesis_Guo2013.tex

    两次以上的编译才能保证交叉引用正确。检查 Thesis_Guo2013.pdf 是否看起来正确。

3.  修改 **文件说明** 里面打 * 的部分，再按照上面的命令编译，就可以排版出自己的论文啦。

**注意**

* 可以复制一份 Thesis_Guo2013.tex 并重命名，作为你的毕业论文的主文件。

* 样例的四个章节各自写成了单独的文件， \include 到了主文件中。由于毕业论文的长度，推荐这种写法。章节的文件名可以任意。

* 样例把所有的插图都放在 figures/ 里，插图命令需要指示这个目录。你也可以放在别的地方。figures/ 里面已有的那些文件是样例所用的，可以删去。但是，不要删去根目录下的 logo.pdf，因为是我大成电校徽啊！

* contents/ 目录下的文件名是固定的，不要自行修改。

* 参考文献用 bib 格式放在 contents/publications.bib 里面。

* 本科毕业设计要求在最后附上一篇英文文献及其翻译。请将 contents/original.pdf 替换为英文原文，将 contents/translation.pdf 替换为译文。

* 编译可能产生很多 warning ，在不影响结果的情况下可以忽略。

* 如果用于排版中文正文的毕业论文，可能需要手动修改 uestcthesis.cls (sorry...)。I guess you can figure it out and do it by yourself! :)


