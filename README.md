# Latex
## Text
- Text  
	Ref: https://www.overleaf.com/learn/latex/Bold%2C_italics_and_underlining
	- Bold text : `\textbf{text}`
	- Italicized text : `\emph{text}`
	- underlined text : `\underline{text}`
- Paragraph   
	Ref: https://www.overleaf.com/learn/latex/Line_breaks_and_blank_spaces
	- Line breaks : '\\', '\break'
	- Paragraph break : twice enter
- text alignment  
	Ref: https://www.overleaf.com/learn/latex/Text_alignment
- itemization   
	Ref : https://www.overleaf.com/learn/latex/Articles/How_to_change_paragraph_spacing_in_LaTeX
	```
	\begin{itemize}
	\item The value of \verb|\baselineskip| is \texttt{\the\baselineskip}
	\item The value of \verb|\parskip| is \texttt{\the\parskip}
	\end{itemize}
	\end{document}
	```

## Hyperlinks
Ref: https://www.overleaf.com/learn/latex/Hyperlinks
```
% set up
\usepackage{blindtext}
\usepackage{hyperref}
\hypersetup{
    colorlinks=true,
    linkcolor=blue,
    filecolor=magenta,      
    urlcolor=cyan,
    pdftitle={Overleaf Example},
    pdfpagemode=FullScreen,
    }
\urlstyle{same}


\href{http://www.overleaf.com}{Something Linky} 
\href{mailto:leesunjae@gist.ac.kr}{Sunjae Lee}
```

## Figure
- To set the figure directory.   
	Ref: https://tex.stackexchange.com/questions/301494/how-to-use-includegraphics   
	https://texblog.org/2017/12/05/the-path-to-your-figures/   
	```
	\usepackage{graphicx} 
	\graphicspath{{images/}}
	```
- To add figure
	```
	% for subplot setting
	\usepackage{caption}
	\usepackage{subcaption}
	\captionsetup{compatibility=false}
	```
	```
	% To add figure
	\begin{figure}[t]
			\centering
			\includegraphics[width=0.9\textwidth]{GNN_architecture.png}
			\caption{Illustration of the graph neural network architecture.}
			\label{fig:GNN_architecture}
	\end{figure}
	```
- Referencing figure  
	Ref : https://www.overleaf.com/learn/latex/Referencing_Figures
	```
	% To add reference on text
	\ref{fig:GNN_architecture}
	```

Figure with subplot  
Ref: https://latex-tutorial.com/subfigure-latex/  
https://www.overleaf.com/learn/latex/How_to_Write_a_Thesis_in_LaTeX_(Part_3)%3A_Figures%2C_Subfigures_and_Tables  
```
\begin{figure}[htbp]
    \centering
    \begin{subfigure}[b]{0.45\textwidth}
        \centering
        \includegraphics[width=\textwidth]{tSNEplot_predicted(dpi=1200).png}
        \caption{Predicted labels}
        \label{fig:tSNEplot predicted}
    \end{subfigure}
    \hfill
    \begin{subfigure}[b]{0.45\textwidth}
        \includegraphics[width=\textwidth]{tSNEplot_label(dpi=1200).png}
        \caption{True labels}
        \label{fig:tSNEplot label}
    \end{subfigure}
        \caption{tSNE plot of GINE}
        \label{tSNE plot}
\end{figure}

```


## Table
Ref: https://www.overleaf.com/learn/latex/Tables  
```
\begin{table}[ht]
\caption{Graph model performance comparison}
  \begin{tabular}{ccccc}
    \hline
       & Accuracy  & Precision   & Recall   & F1 \\ \hline
    GCN & \textbf{86.584} & \textbf{85.179} & 71.204 & 77.567 \\
    GraphSAGE & 84.916 & 74.058  & \textbf{85.617} & \textbf{79.419} \\
    GAT & 84.916 & 81.698 & 71.666 & 76.354 \\ 
    GIN & 86.412 & 82.817 & 75.706 & 79.102 \\ 
    GINE & \textbf{86.584} & 83.815 & 74.991 & 79.158 \\ \hline
    \label{table:Graph model performance comparison}
  \end{tabular}
\end{table}
```

# Mathematical equations and notations
Ref : https://oeis.org/wiki/List_of_LaTeX_mathematical_symbols
```
\usepackage{amsfonts} % \mathbb{R}


$ $
\in
\sum
\cdot

\alpha_{i,j}
\Tilde{D}
\alpha \in \mathbb{R}^{2d}

\begin{equation}\label{Graph convolutional network}
\begin{aligned}[b]
      H^{(l+1)} = ReLU(\Tilde{D}^{-1/2}\Tilde{A}\Tilde{D}^{-1/2}H^{(l)}W^{(l)})
\end{aligned}
\end{equation}

```

- Fractions and binomials   
	Ref : https://www.overleaf.com/learn/latex/Fractions_and_Binomials

```
\%
```

## citation
```
\cite{hamilton2017inductive}
```
