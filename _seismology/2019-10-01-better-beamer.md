---
title: 'Better Beamer Presentations the Easy Way'
date: 2019-10-01
permalink: /seismology/2019/10/better-beamer
excerpt_separator: <!--more-->
toc: true
tags:
  - latex
  - beamer
  - github
---

Everyone knows that Beamer makes frankly terrible presentations without a good deal of help. A well crafted Beamer presentation can be a thing of beauty, especially since you can use knitr or R Markdown to automatically generate tables and figures, but it takes *a lot* of work.
<!--more-->
We all have our own little tricks to do things like get more space between items in a list (ending every `\item` line with `\\~\\`) and the simple but repetitive tasks we have to do every single slide (opening a `\Large` environment to make text more readable).

# Three little tricks

I finally got tired of all this and decided to waste a lot of time now to save even more time later. To do that, I headed to Stack Exchange and started digging into the Beamer documentation.

## Give me some space

We'll start with the base Beamer class. There are a number of Beamer [themes](https://hartwork.org/beamer-theme-matrix/) that are much better than the default theme, but I'm going to focus on things we can do to improve even the default theme. Here's our humble starting point.

```latex
\documentclass{beamer}

\begin{document}
	
\begin{frame}[fragile]{My default slide}
	\begin{itemize}
		\item Foo
		\item Bar
		\begin{itemize}
			\item Below is an equation
			\[ y = mx + b \]
			\item It is very hard to read
		\end{itemize}
		\item Baz
	\end{itemize}
\end{frame}

\end{document}
```
