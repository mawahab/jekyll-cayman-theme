---
layout:     post
title:      "LateX tips"
date:       2017-07-10 12:00:00
author:     "MAW"
header-img: "img/post-bg-02.jpg"
---

Here are a few tips for Latex.

- Include the following package to obtain \toprule and \midrule commands inside a latex document.
  booktabs package 

	```latex
	\usepackage{booktabs}
	```

- To adjust the width of table, use adjustbox package which allows to force the table to the specified width 
	```latex
	\usepackage{adjustbox}
	```

 Example usage : 

	```latex
	\begin{table}
		\begin{adjustbox}{max width=\textwidth}
			\begin{tabular}{llrcr}
			\end{tabular}
		\end{adjustbox}
	\end{table}
	```

- Just a reminder, the label in a figure or table applies to the caption so it should be put after the \caption command ! 

	```latex
	\caption{}
	\label{}
	```

- To avoid an empty page after a \page or \chapter, simply add `oneside` in the `documentclass` options like :

	```latex
 	\documentclass[oneside]{memoir}
	```

- To add abbreviations, use `nomenclature` package and follow the descriptions provide at the following [link](http://www.xm1math.net/doculatex/nomenclature.html)

- To strike through (bar) the text, use this : 

	```latex
 	\usepackage[normalem]{ulem}
 	%if overlay is needed
 	\renewcommand<>{\sout}[1]{
   	\alt#2{\beameroriginal{\sout}{#1}}{#1}
 	}	
	```

- To delete headline on top of each frame in beamer, simply add 

	```latex
 	\setbeamertemplate{headline}{}
	```

- To add outline at the beginning of each section, just use the following code (tip found on [link](https://nickhigham.wordpress.com/2013/01/18/top-5-beamer-tips/)) :

	```latex
 	\setbeamerfont{myTOC}{series=\bfseries,size=\Large}
 	\AtBeginSection[]{\frame{\frametitle{Outline}%
                   \usebeamerfont{myTOC}\tableofcontents[current]}}
	```

- To add source code in latex, use the [link](https://en.wikibooks.org/wiki/LaTeX/Source_Code_Listings)
- Convert text with special characters into Latex recognized text, use the [link](http://w2.syronex.com/jmr/latex-symbols-converter)
- Spell checking .tex files ...

 	```aspell --lang=en --mode=tex check file.tex```
