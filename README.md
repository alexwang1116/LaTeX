# LaTeX 使用技巧 (Last update:5/21/2019 4:55:28 PM)
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





