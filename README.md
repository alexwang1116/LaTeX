# LaTeX 使用技巧 (Last update:5/21/2019 12:01:17 PM)
📢 Good good study day day up！🔔


### LaTeX图片

【实用】Latex中插图总结（一）        
🚪 https://blog.csdn.net/chichoxian/article/details/52588833    

使用的方法如下所示：

    \begin{figure}[ht]
    \centering
    \includegraphics[scale=0.6]{fullscreen.png}
    \caption{this is a figure demo}
    \label{fig:label}
    \end{figure}




【多图片插入】LaTeX图片插入        
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


