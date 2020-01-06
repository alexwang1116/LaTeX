# LaTeX 使用技巧 (Last update:1/6/2020 3:20:07 PM)
📢 Learn to use LaTeX 🔔


### LaTeX图片

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

----------


### LaTeX表格

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
  

**Latex减少图片、表格与文字之间的空白间隙**    
🚪 https://blog.csdn.net/u011089523/article/details/83270994 

论文中图与文字之间的空白间隙过大，导致排版不大美观。解决方法是在\begin{document}前定义\textfloatsep的长度，例如定义为5pt：

    \setlength{\textfloatsep}{5pt}



----------



### LaTeX公式    

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



----------

### LaTeX算法


**LaTeX算法排版例子**    
🚪 https://blog.csdn.net/lqhbupt/article/details/8723478


**Latex写算法的伪代码排版**    
🚪 https://blog.csdn.net/lwb102063/article/details/53046265







----------

### LaTeX参考文献

**Latex小白入门（2）——如何用.bib文件自动生成论文Reference**     
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



----------


### Latex多行注释快捷键

1. 注释    
"Ctrl" + "T"
 
2. 去除注释    
“Ctrl” + "U"








----------


### 使用VSCode编写LaTeX

🚪 https://zhuanlan.zhihu.com/p/38178015

### 编写中文Latex(VSCode+TexLive)

🚪 https://zhuanlan.zhihu.com/p/43133114 

### Win10下 VS code+LaTeX 环境的构建

🚪 https://zhuanlan.zhihu.com/p/36285613

