# LaTeX 使用技巧 (Last update:5/22/2019 6:24:08 PM)
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





### LaTeX参考文献

**Latex小白入门（2）——如何用.bib文件自动生成论文Reference**     
🚪 https://blog.csdn.net/tmylzq187/article/details/51355261

基本方法如下：
    
1. 首先利用谷歌学术制作.bib文件：在谷歌学术中搜索引文，然后点击应用中的bibtex，将内容复制到文本文档中，然后修改文件类型为.bib；（可以使用**JafRef**软件来生成和管理bib文件，简洁方便！）
2. 然后在.tex文件中（\begin{document}之后）加入以下内容：  


    \bibliographystyle{IEEEtran}       %IEEEtran为给定模板格式定义文件名    
    \bibliography{ref}                 %ref为.bib文件名


3. 在.tex文件相应位置插入索引\cite{标签}，其中*标签*为bib文件中每个参考文献的第一项内容；
4. 编译生成Reference，顺序为：PDFLaTex ——>BibTex——>PDFLaTex——>PDFLaTex，正常情况下就会在PDF文件末尾显示出带有编号的参考文献了。



**LaTex如何自动生成参考文献**    
🚪 https://blog.csdn.net/qq_33033367/article/details/81461029


**【实用】使用BibTex格式时缩小参考文献的字体**    
🚪 https://cloud.tencent.com/developer/article/1012569




### Latex注释快捷键

1. 注释    
"Ctrl" + "T"
 
2. 去除注释    
“Ctrl” + "U"




