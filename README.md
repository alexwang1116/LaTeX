# LaTeX 使用技巧 (Last update:12/12/2020 2:23:51 PM)
📢 Learn to use LaTeX 🔔

## 目录：
1. [LaTeX图片](#1)
2. [LaTeX表格](#2)
3. [LaTeX公式](#3)
4. [LaTeX算法](#4)
5. [LaTeX参考文献](#5)
6. [Latex多行注释快捷键](#6)
7. [LaTeX转Word](#7)



----------


### <h3 id="1">LaTeX图片</h3>

**【实用】Latex中插图总结（一）**        
🚪 https://blog.csdn.net/chichoxian/article/details/52588833    

使用的方法如下所示：

    \begin{figure}[ht]
    \centering
    \includegraphics[scale=0.6]{fullscreen.png}
    \caption{this is a figure demo}
    \label{fig:label}
    \end{figure}




**【多图片插入】LaTeX图片插入**        
🚪 https://www.jianshu.com/p/d41546dff228    

使用的方法如下所示：

    \begin{figure}[H]
    \centering
    \subfigure[场景1]{
    \includegraphics[width=0.45\textwidth]{wolf2} 
    }
    \subfigure[场景2]{
    \includegraphics[width=0.45\textwidth]{wolf4}
    }
    \caption{狼伴归途场景}
    \label{wolf2}
    \end{figure}


显示的效果如下：    

![](https://upload-images.jianshu.io/upload_images/3478485-6839a37e479fbc69.png?imageMogr2/auto-orient/strip|imageView2/2/w/387)



**【实用】解决LaTex中插入Visio画图有多余边框的问题**   
🚪 https://www.polarxiong.com/archives/%E8%A7%A3%E5%86%B3LaTex%E4%B8%AD%E6%8F%92%E5%85%A5Visio%E7%94%BB%E5%9B%BE%E6%9C%89%E5%A4%9A%E4%BD%99%E8%BE%B9%E6%A1%86%E7%9A%84%E9%97%AE%E9%A2%98.html    


**【实用】在线png/jpeg图片转eps/pdf格式 Convert PNG/JPEG (Raster) to EPS/PDF (Vector) Format**     
🚪 http://www.tlhiv.org/rast2vec/     

----------


### <h3 id="2">LaTeX表格</h3>

**【实用】Latex基本表格绘制**   
🚪 https://blog.csdn.net/JueChenYi/article/details/77116011

常见表格使用的方法如下所示：

    \begin{tabular}{|l|c|r|} % 通过添加 | 来表示是否需要绘制竖线，l(left)居左显示 r(right)居右显示 c居中显示
    \hline  %在表格最上方绘制横线
    Name&Steve&Bill\\ %用&来分隔每个表格中的内容
    \hline %在第一行和第二行之间绘制横线
    Matlab&Mathmatica&Maple\\
    \hline %在表格最下方绘制横线
    \end{tabular}

显示的效果如下：

![](https://img-blog.csdn.net/20170812125307589?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvSnVlQ2hlbllp/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)


**LaTeX各种表格**    
🚪 https://blog.csdn.net/golden1314521/article/details/40891515  

**LaTeX改变单元格的对齐方式（某一行跨单元格对齐）** ❤️   
🚪 http://tigersoldier.is-programmer.com/posts/2304.html
  

**Latex减少图片、表格与文字之间的空白间隙** ❤️❤️❤️   
🚪 https://blog.csdn.net/u011089523/article/details/83270994 

论文中图与文字之间的空白间隙过大，导致排版不大美观。解决方法是在\begin{document}前定义\textfloatsep的长度，例如定义为5pt：

    \setlength{\textfloatsep}{5pt}



----------



### <h3 id="3">LaTeX公式</h3>    

**怎样用LaTeX优雅地打印数学的一切**  
🚪 https://www.jianshu.com/p/f5d475d6904e

**LaTeX大括号公式和一般括号总结**    
🚪 https://blog.csdn.net/miao0967020148/article/details/78712811

**LaTeX集合相关符号：实数集，整数集，并，包含，真包含**    
🚪 https://blog.csdn.net/robert_chen1988/article/details/76209634


**LaTeX 符号命令大全** ❤️    
🚪 https://www.cnblogs.com/Coolxxx/p/5982439.html

 
使用方法如下所示：

    $\left(  \right)$ %小括号
    $\left[ \right]$ %中括号
    $\left\{   \right\}$ %大括号
     

**LaTeX特殊字符** ❤️     
🚪 https://shaoweicai.wordpress.com/2010/01/12/latex特殊字符/ 

     和"\"字符一起, $ & % # _ ^ { } ~ 是TeX的保留字符, 如果要在文章中输出以上字符, 分别应该用\backslash, \$, \&,\%, \#, \_, \^{}, \{, \}, \~{}来表出.
        $ 是数学环境的分界符
        & 在制表中和数学环境中, 用来对齐各列的
        % 表示之后的为注释, TeX忽略该行此符号之后的内容
        # TeX定义命令时, #1–#9表示第几个参数
        _ 数学公式中的下标
        ^ 数学公式中的上标
        { } 分组的开始和结束
        ~ 用在英文排版中, 表示不可断行的空格




**LaTeX输入带圈数字**    
🚪 https://www.jianshu.com/p/f9ce0367a1dd  
  
🚪 https://stone-zeng.github.io/2019-02-09-circled-numbers/  

🚪 https://sikouhjw.gitee.io/2020/03/17/2020-03-17-Circle-around-letter/      

命令的定义
   
    \usepackage{tikz}
    \newcommand*{\circled}[1]{\lower.7ex\hbox{\tikz\draw (0pt, 0pt)%
    circle (.5em) node {\makebox[1em][c]{\small #1}};}}

使用示例

    \circled{1} 萤火虫叔叔\\
    \circled{2} 萤火虫\\
    \circled{3} 萤\\

效果截图    

![](https://upload-images.jianshu.io/upload_images/8484958-b2be87bada8e4b4f.png?imageMogr2/auto-orient/strip|imageView2/2/format/webp)





**【实用】LaTeX不会写的符号手写自动输出对应命令**         
🚪 http://detexify.kirelabs.org/classify.html




**希腊字母发音对照表及其latex命令**    
🚪 https://blog.csdn.net/lanchunhui/article/details/49819445

   

 
|小写| 大写 |LaTex小写|LaTex大写|
|:----:|:----:|:----:|:----:|
| α | A | \alpha|
|β	|B	|\beta|
|γ	|Γ	|\gamma|\Gamma|
|δ	|Δ	|\delta|\Delta|
|ϵ	|E	|\epsilon|
|ζ	|Z	|\zeta|
|ν	|N	|\nu|
|ξ	|Ξ	|\xi|\Xi|
|ο	|O	|\omicron|
|π	|Π	|\pi|\Pi|
|ρ	|P	|\rho|
|σ	|Σ	|\sigma|\Sigma|
|η	|H	|\eta|
|θ	|Θ	|\theta|\Theta|
|ι	|I	|\iota|
|κ	|K	|\kappa|
|λ	|Λ	|\lambda|\Lambda|
|μ	|M	|\mu|
|τ	|T	|\tau|
|υ	|Υ	|\upsilon|\Upsilon|
|ϕ	|Φ	|\phi,（φ：\varphi）|\Phi|
|χ	|X	|\chi|
|ψ	|Ψ	|\psi|\Psi|
|ω	|Ω	|\omega|\Omega|








----------

### <h3 id="4">LaTeX算法</h3>


**LaTeX算法排版例子**    
🚪 https://blog.csdn.net/lqhbupt/article/details/8723478


**Latex写算法的伪代码排版**    
🚪 https://blog.csdn.net/lwb102063/article/details/53046265


**LaTeX/Algorithms 伪代码**    
🚪 http://hustsxh.is-programmer.com/posts/38801.html   


**LaTeX伪代码编辑模板**     
🚪 https://www.omegaxyz.com/2018/10/07/latex_-pseudocode/ 












----------

### <h3 id="5">LaTeX参考文献</h3>

**Latex小白入门（2）——如何用.bib文件自动生成论文Reference**❤️❤️❤️     
🚪 https://blog.csdn.net/tmylzq187/article/details/51355261

基本方法如下：
    
1. 首先利用谷歌学术制作.bib文件：在谷歌学术中搜索引文，然后点击应用中的bibtex，将内容复制到文本文档中，然后修改文件类型为.bib；（可以使用**JafRef**软件来生成和管理bib文件，简洁方便！JafRef的中文使用教程 https://blog.csdn.net/zd0303/article/details/7676807 ）
2. 然后在.tex文件中（\begin{document}之后）加入以下内容：  


        \bibliographystyle{IEEEtran}   %IEEEtran为给定模板格式定义文件名
        \bibliography{ref}             %ref为.bib文件名


3. 在.tex文件相应位置插入索引\cite{标签}，其中*标签*为bib文件中每个参考文献的第一项内容；
4. 编译生成Reference，顺序为：PDFLaTex ——>BibTex——>PDFLaTex——>PDFLaTex，正常情况下就会在PDF文件末尾显示出带有编号的参考文献了。



**LaTex如何自动生成参考文献**    
🚪 https://blog.csdn.net/qq_33033367/article/details/81461029


**【实用】使用BibTex格式时缩小参考文献的字体**    
🚪 https://cloud.tencent.com/developer/article/1012569


**【多篇参考文献的合并】latex中同一处引用多篇文献**    
🚪 https://blog.csdn.net/lqhbupt/article/details/49925911

方法如下：

在文档开始前加上下面的包即可参考文献中间用破折号连起来，比如[6,7,8,9]变成[6-9]，如果没有此命令，则会显示为[6]-[9]。   
    
    \usepackage[numbers,sort&compress]{natbib}



**【实用】LaTeX参考文献双栏对齐**    
🚪 https://www.cnblogs.com/qq952693358/p/9445756.html    
方法1：    
    在开头引用balance：
`\usepackage{balance}` ,在文末、参考文献前，加上:
`\balance`

方法2：    
在开头引用flushend：`\usepackage{flushend}`


**【实用】LaTeX在参考文献中引用网页**    
🚪 https://blog.xulihang.me/cite-webpage-in-latex/

需要用到这个包\usepackage{url}，bib文件中写入的示例如下：

    @misc{ETSI17MEC,
    author = {ETSI},
    url = {https://www.etsi.org/technologies/multi-access-edge-computing},
    urldate = {September, 2017},
    title = {Multi-access Edge Computing (MEC)},
    year = {2017}
    }

最终生成的参考文献如下：

    ETSI, “Multi-access edge computing (mec),” 2017. [Online]. Available:    
    https://www.etsi.org/technologies/multi-access-edge-computing


**【实用biber问题汇总】LaTeX/Bibliographies with biblatex and biber**    
🚪 https://en.wikibooks.org/wiki/LaTeX/Bibliographies_with_biblatex_and_biber    


**【实用biber配置问题汇总】Biblatex with Biber: Configuring my editor to avoid undefined citations**    
🚪 https://tex.stackexchange.com/questions/154751/biblatex-with-biber-configuring-my-editor-to-avoid-undefined-citations%7C



**Latex的biography中作者照片的插入**    
🚪 https://blog.csdn.net/lj695242104/article/details/47946919    

以IEEE Trans模板为例，假设作者的名字是ZhangSan，首先应该在这个tex文件所在的文件夹里放上这个作者的照片，假设照片的文件名为zhangsan.eps，那么tex文件里格式如下：

    \begin{IEEEbiography}[{\includegraphics[width=1in,height=1.25in,clip,keepaspectratio]{zhangsan.eps}}]{Zhang San}
    
    Biography of Zhangsan should be here.
    
    \end{IEEEbiography}


**Latex 作者上角标，通讯作者的小信封标记**     
🚪 https://blog.csdn.net/u010682375/article/details/79732977    

添加方式如下：

    \author{Lily\textsuperscript{1}        \and
        Alexw\textsuperscript{2}  }

显示为：

![](https://img-blog.csdn.net/20180328195546362?watermark/2/text/aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3UwMTA2ODIzNzU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70)





----------


### <h3 id="6">Latex多行注释快捷键</h3>

1. 注释    
"Ctrl" + "T"
 
2. 去除注释    
“Ctrl” + "U"




----------

### <h3 id="7">LaTeX转Word</h3>
**【实用】怎么用Pandoc把Latex转换成MS Word文档**   
🚪 https://www.jianshu.com/p/dc62b915920e     

**Latex 转 Word**  
🚪 https://www.jianshu.com/p/ed0713582de2


**Latex转Word在线公式编辑器转mathml复制**    
🚪 https://latexlive.com/     


**Word中使用bib管理参考文献**    
🚪 http://www.scholat.com/vpost.html?pid=72303   


  	
  	
   
  	
  
 	
 






----------

### LaTeX论文格式问题解决方法汇总

**解决 The gutter between columns is x inches wide (on page x), but should be at least 0.2 inches. 问题**     
🚪 https://www.cnblogs.com/qq952693358/p/8856602.html        
🚪 https://tex.stackexchange.com/questions/428853/the-gutter-between-columns-is-0-155-inches-wide-on-page-4-but-should-be-at-le     

解决方法是在`\begin{document}`前加上`\columnsep 0.2in`的定义即可。








----------

### 【实用】简单粗暴 LaTeX（Note-by-LaTeX含各种操作命令pdf）    
    
**Note-by-LaTeX GIthub项目网址**❤️❤️❤️     
🚪 https://github.com/wklchris/Note-by-LaTeX    

**Note-by-LaTeX PDF版本地址**❤️❤️❤️❤️❤️❤️     
🚪 http://static.latexstudio.net/wp-content/uploads/2017/08/Note-by-LaTeX-cn.pdf


----------
### 【教程】【1天玩转LaTeX】【写论文不怕格式出错啦！！！】
🚪 https://www.bilibili.com/video/BV15b411j7Au?p=11&share_medium=iphone&share_plat=ios&share_source=COPY&share_tag=s_i&timestamp=1591793477&unique_k=15n6OR


----------


### 使用VSCode编写LaTeX

🚪 https://zhuanlan.zhihu.com/p/38178015

### 编写中文Latex(VSCode+TexLive)

🚪 https://zhuanlan.zhihu.com/p/43133114 

### Win10下 VS code+LaTeX 环境的构建

🚪 https://zhuanlan.zhihu.com/p/36285613

