# latex_cheaksheet
A template and common elements used in latex, for quick reference.

## Template

```latex
\documentclass{article} % create a document
\title{Title of the article}
\author{Author Name}
\date{\today}
\begin{document}
\maketitle
\section{Intruduction}
The text in this section.
\end{document}
```

## Bold, italics and underlining

### Bold Text

```latex
Some of the \textbf{greatest} 
discoveries in science 
were made by accident.
```

### Underlining Text

```latex
Some of the greatest 
discoveries in \underline{science} 
were made by accident.
```

### Emphasising text (italics )

```latex
Some of the greatest \emph{discoveries} 
in science 
were made by accident.
```

## Sections

The article document class in latex is organized in sections.(There are other classes of documents).

| 1    | `\section{section}`             |
| ---- | ------------------------------- |
| 2    | `\subsection{subsection}`       |
| 3    | `\subsubsection{subsubsection}` |

## Unordered Lists

```latex
Lists are easy to create:
\begin{itemize}
  \item List entries start with the \verb|\item| command.
  \item Individual entries are indicated with a black dot, a so-called bullet.
  \item The text in the entries may be of any length.
\end{itemize}
```
## Pictures and Figures
To insert pictures we need to use the 'graphicx' package also we need to specify the image path. Inclue the package after the documentclass:
```latex
\documentclass{article} % create a document
\usepackage{graphicx}
\graphicspath{ {./images/} }
\title{Some Title}
```
Blow we include the 'smd_pkg_04' image in the document, with scaling of 0.3.
```latex
\begin{figure}[h]
\caption{Picture of Analog Devices Gyroscopes that uses Kyocera vacuum-sealed package.}
\includegraphics[scale=0.3]{smd_pkg_04}
\end{figure}
```
