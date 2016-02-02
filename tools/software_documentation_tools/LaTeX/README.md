
###TeX

`TeX` is a `typesetting language`. Instead of visually formatting your text, you enter your manuscript text intertwined with TeX commands in a plain text file. You then run TeX to produce formatted output, such as a PDF file. Thus, in contrast to standard word processors, your document is a separate file that does not pretend to be a representation of the final typeset output, and so can be easily edited and manipulated. 

[https://en.wikipedia.org/wiki/TeX](https://en.wikipedia.org/wiki/TeX)

[https://www.tug.org/texlive/doc/texlive-zh-cn/texlive-zh-cn.pdf](https://www.tug.org/texlive/doc/texlive-zh-cn/texlive-zh-cn.pdf)

###LaTeX

* Document markup language for TeX

	* TeX is a typesetting program written by Donald Knuth since 1978
	
* Install a LaTeX distribution
	* For English, install MikTeX (on Windows)
		
		[http://miktex.org/](http://miktex.org/)
	
	* For Chinese support, install CTeX
	
		[http://www.ctex.org/](http://www.ctex.org/)
	
	* Or Tex Live (MacTeX, on Mac OSX)
	
		[https://www.tug.org/texlive/](https://www.tug.org/texlive/)


###Learn LaTeX

* LaTeX Wikibook

	[http://en.wikibooks.org/wiki/LaTeX](http://en.wikibooks.org/wiki/LaTeX)

	[http://zh.wikibooks.org/wiki/LaTeX](http://zh.wikibooks.org/wiki/LaTeX) (partially translated to Chinese)
	














```
\documentclass{article}


3\. Save as test.tex

4\. Click typeset green button (or Ctrl + T)

5\. test.pdf is generated and shown in preview window

![2.png](https://github.com/gerryyang/mac-utils/blob/master/tools/software_documentation_tools/LaTeX/pic/2.png) 

###Edit With Sublime Text

* Install LaTeXTools with Package Control
	* Syntax lighting, build, seek to cursor... 
	[https://packagecontrol.io/packages/LaTeXTools](https://packagecontrol.io/packages/LaTeXTools)

####Structure
```
\documentclass{...}
\usepackage{...}
\begin{document}
...
\end{document}
```

####Front Matter
```
\documentclass{article}
```
![3.png](https://github.com/gerryyang/mac-utils/blob/master/tools/software_documentation_tools/LaTeX/pic/3.png)

####Chapters/Sections
```
\begin{document}
\maketitle
\tableofcontents
\chapter{Introduction}
...
\section{History}
...
\chapter{Related Works}
...
\end{document}
```

####Lists

```
\documentclass{article}
\usepackage{geometry}
\usepackage{fancyhdr}
\usepackage{amsmath,amsthm,amssymb}
\usepackage{graphicx}
\usepackage{hyperref}
\begin{document}
Hello world!
\begin{itemize}
	\item The first item
	\item The second item
	\item The third etc \dots
\end{itemize}
\end{document}
```
![4.png](https://github.com/gerryyang/mac-utils/blob/master/tools/software_documentation_tools/LaTeX/pic/4.png)

```
\documentclass{article}
\usepackage{geometry}
\usepackage{fancyhdr}
\usepackage{amsmath,amsthm,amssymb}
\usepackage{graphicx}
\usepackage{hyperref}
\begin{document}
Hello world!
\begin{enumerate}
	\item The first item
	\item The second item
	\item The third etc \dots
\end{enumerate}
\end{document}
```
![5.png](https://github.com/gerryyang/mac-utils/blob/master/tools/software_documentation_tools/LaTeX/pic/5.png)

####Mathematics
```
\documentclass{article}
\usepackage{geometry}
\usepackage{fancyhdr}
\usepackage{amsmath,amsthm,amssymb}
\usepackage{graphicx}
\usepackage{hyperref}
\begin{document}
Hello world!
The length $u$ is $\sqrt{x^2+y^2}$.
\[\cos(2\theta)=\cos^2\theta-\sin^2\theta\]
\end{document}
```
![6.png](https://github.com/gerryyang/mac-utils/blob/master/tools/software_documentation_tools/LaTeX/pic/6.png)

[公式书写工具](http://www.codecogs.com/latex/eqneditor.php)

####Code
Use `\verb` and `\begin{verbatim}...\end{verbatim}`

Use `listings` package if need syntax highlighting

```
\documentclass{article}
\usepackage{geometry}
\usepackage{fancyhdr}
\usepackage{amsmath,amsthm,amssymb}
\usepackage{graphicx}
\usepackage{hyperref}
\usepackage{listings}
\begin{document}
Hello world!
\lstset{language=c++}
The class \lstinline!Foo! is a base class...
\begin{lstlisting}
class Foo {
	...
};
\end{lstlisting}
\end{document}
```
![7.png](https://github.com/gerryyang/mac-utils/blob/master/tools/software_documentation_tools/LaTeX/pic/7.png)


####Multiple files
Like a C/C++ source file, LaTeX can include other .tex files by `\input{}`

```
\begin{document}
\input{introduction}
\input{approach]
\end{document}
```

-------