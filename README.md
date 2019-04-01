# report-nips-style
A LaTex template for reports, based on the elegant NIPS 2018 style.

This template retains the clean look of the single-column NIPS style, with the addition of a few extra options suitable for reports.

---

# Options

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
\usepackage[options1]{report_2019_JH}
\usepackage[options1,options2]{report_2019_JH}
```

## Title page

If the "titlepage" option is used, the name and logo of the university can be set via:
```TeX
\global\newcommand{\universityLogo}{images/logo.png}            % Put university logo path here
\global\newcommand{\university}{My university name}             % Put university name here
```

---

# Citation

To use squared citation format:
```TeX
\PassOptionsToPackage{square, numbers}{natbib}
\bibliographystyle{elsarticle-harv}
```

To use APA citation format:
```TeX
\PassOptionsToPackage{round}{natbib}
\bibliographystyle{apa}
```

To avoid loading the natbib package, add option "nonatbib":
```TeX
\usepackage[nonatbib]{report_2019_JH}
```

---

# Subsections

Subsections are numbered down until level 4 (x.x.x.x) by using either one of these:
```TeX
\paragraph{Subsection name}
\subsubsubsection{Subsection name}
```

Subsections of level 5 are not numbered:
```TeX
\subparagraph{Subsection name}
\subsubsubsubsection{Subsection name}
```

