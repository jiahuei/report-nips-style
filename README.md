# Latex class for NIPS-style report
===================
A LaTex template for reports, based on the elegant NIPS 2018 style.

This template retains the clean look of the single-column NIPS style, with the addition of a few extra options suitable for reports.

See `example_minimal.pdf` and its TeX file for a short demonstration.

---

## Options

By default without options, the package will add line numbers and generate A4 size pages.
List of options:
1. _none_ : Draft version, with line numbers.
1. titlepage : Produce a title page, with university name and logo.
1. letter : For letter sized page.
1. preprint : Preprint version.
1. anonymise: For anonymised submission. Will also add line numbers.
1. final : To generate final version without line numbers.

```TeX
\usepackage{report_2019_JH}
\usepackage[]{report_2019_JH}
\usepackage[options1]{report_2019_JH}
\usepackage[options1,...,optionsN]{report_2019_JH}
```

---

## Authors

Multiple authors can be placed in the following format:
```TeX
\author{Your Name \\ \textit{ID / Some text}  \AND
        Co-author \\ \textit{Supervisor}      \AND
        Co-author \\ \textit{Co-supervisor}   \And
        Co-author \\ \textit{Co-supervisor}   \And
        Co-author \\ \textit{Co-supervisor}}
```
Authors are separated using `\AND` and `\And`.
The difference between them is:
* `\AND` forces a line break.
* `\And` leaves it to LaTeX to determine where to break the lines.

In the most minimal case:
```TeX
\author{Your Name}
```

---

## Title page

If the "titlepage" option is used, the name and logo of the university can be set via:
```TeX
\newcommand{\universityLogo}{images/logo1.png}              % Put university logo path here
\newcommand{\university}{My University / Faculty Name}      % Put university name here
```

---

## Citation

### Squared citation format
```TeX
\usepackage[square, numbers]{natbib}
\bibliographystyle{elsarticle-harv}

\begin{document}

\cite{xu2015show}
```

### IEEE citation format
```TeX
\usepackage[square, numbers]{natbib}
\bibliographystyle{IEEEtran}

\begin{document}

\cite{xu2015show}
```

### APA citation format
```TeX
\usepackage[round]{natbib}
\bibliographystyle{apa}

\begin{document}

\citep{xu2015show}    % wraps citation in parentheses:   (Xu et al., 2015)
\citet{xu2015show}    % in-line citation:   Xu et al. (2015)
```

---

## Subsections

Subsections are numbered down until level 4 (x.x.x.x), and will appear in Table of Contents. Created by using either one of these:
```TeX
\paragraph{Subsection name}
\subsubsubsection{Subsection name}
```

Subsections of level 5 are not numbered, and will NOT appear in Table of Contents:
```TeX
\subparagraph{Subsection name}
\subsubsubsubsection{Subsection name}
```

