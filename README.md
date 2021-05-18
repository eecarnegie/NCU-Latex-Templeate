# NCU-Latex-Templeate

## 編譯順序

>* 順序=Xelatex + Bibtex + makeindex + Xelatex + Xelatex
>	
>* 如果沒有使用Bibtex請拿掉
>	
>* 使用window用戶可以直接跑Script.bat，會自動幫你編譯Main.tex，
>	
>* 如果主檔案更名，請改把主tex檔案拖拉到Script上

### MAC使用者的編譯順序

Xelatex --> Bibtex --> Xelatex

![Step1](https://github.com/eecarnegie/NCU-Latex-Templeate/blob/ADD_example/pic/Step1.png)

![Step2](https://github.com/eecarnegie/NCU-Latex-Templeate/blob/ADD_example/pic/Step2.png)

![Step3](https://github.com/eecarnegie/NCU-Latex-Templeate/blob/ADD_example/pic/Step3.png)


## build成功的範例檔案為
>* [NCU_thesis_sample.pdf](https://github.com/RainJayTsai/NCU-Latex-Templeate/blob/master/NCU_thesis_sample.pdf)
    

## Todo List 用法
用法

* `\todo[inline]{需要記錄的事情}`

當完稿時請把
* `\usepackage[]{todonotes}`% 約在第四行

改成
* `\usepackage[disable]{todonotes}`% 約在第四行
    
        
		
## cover Logo
*  `\logo{NCUlogo}   %中央校徽在封面`

* ##### 不要封面有校徽請註解掉
    

## 浮水印
1. 在mypreamble.tex中取消下面註解

    * `\usepackage{background} %取消整串註解，`
        
2. 並在ncuthesisXe.cls檔案中找出
 
    * `\renewcommand\bg@material{}  %並取消註解，以確保cover不會產生浮水印`
    

## 換段落
>請案兩次enter
    

## 章節結構
	\chapter{章名} % 宣告某章開始
		\section{節名一} % 宣告某節開始
		\section{節名二}
			\subsection{小節名} % 宣告小節開始
				\subsubsection{小小節名} % 宣告小小節開始

## 使用範例(Best-Practices)
1. 如何插入圖片
```
\begin{figure}[h]
\includegraphics{test.png}
\caption{test.png}\label{ex1}
\end{figure}
```
2. 如何插入表格
```
\begin{table}[ht]
\centering
\caption{Default parameters used for Monte Carlo Model.}
\label{tab:default}
\begin{tabular}{|l|c|}
\hline
  \multicolumn{2}{|c|}{Default Parameters} \\
  \hline
Disk Purchase cost & $\$100$ \\
Disk Operating Cost & $\$66$ \\
Flash Purchase Cost & $\$500$\\
Flash Operating cost & $\$20$\\
Duration & 100 years\\
$K_r$& .15\\
\hline
\end{tabular}
\end{table}
```

## 參考文件(Reference)
[大家來學LATEX.pdf](http://jupiter.math.nctu.edu.tw/~smchang/latex/latex123.pdf) \
[BibTex範本](https://web.mit.edu/rsi/www/pdfs/bibtex-format.pdf) \
