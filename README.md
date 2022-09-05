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
## Subscript and Superscript
To use subscrit of superscript we need to change to math mode using '$'.
```latex
$V_T$ % subscript
$V^s$ % superscript
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
Oder list are made useing the 'itemize' enviromnet.
```latex
Lists are easy to create:
\begin{itemize}
  \item List entries start with the \verb|\item| command.
  \item Individual entries are indicated with a black dot, a so-called bullet.
  \item The text in the entries may be of any length.
\end{itemize}
```
## Order Lists
Oder list are made useing the 'enumerate' enviromnet.
```latex
\begin{enumerate}
  \item List entries start with the \verb|\item| command.
  \item Individual entries are indicated with a black dot, a so-called bullet.
  \item The text in the entries may be of any length.
\end{enumerate}
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
## Bibliology and references
Below is an exmple of 'refs.bib' file that has the refenece database.
```latex
@book{latex2e,
  author = {Leslie Lamport},
  year = {1994},
  title = {{\LaTeX}: a Document Preparation System},
  publisher = {Addison Wesley},
  address = {Massachusetts},
  edition = {2}
}

@article{knuth:1984,
  title={Literate Programming},
  author={Donald E. Knuth},
  journal={The Computer Journal},
  volume={27},
  number={2},
  pages={97--111},
  year={1984},
  publisher={Oxford University Press}
}

@inproceedings{lesk:1977,
  title={Computer Typesetting of Technical Journals on {UNIX}},
  author={Michael Lesk and Brian Kernighan},
  booktitle={Proceedings of American Federation of
             Information Processing Societies: 1977
             National Computer Conference},
  pages={879--888},
  year={1977},
  address={Dallas, Texas}
}
@manual{pb840:technical,
	title={Puritan Bennett™ 800 Series Ventilator System Operator’s and Technical Reference Manual},
	organization={Covidien},
	?_author		= {},
	?_address	= {},
	?_edition	= {},
	year		= {2011},
	?_month		= {},
	?_note		= {},
}
```
We can site this references in our main latex document, using '\cite{}':
```latex
We need to site the book\cite{latex2e} so that it shows in the reference, otherwise it will not show.
% referneces
\bibliographystyle{plain} % We choose the "plain" reference style
\bibliography{refs} % Entries are in the refs.bib file
```
