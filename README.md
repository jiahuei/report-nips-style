# report-nips-style
A LaTex template for reports, based on the elegant NIPS 2018 style.

This template retains the clean look of the single-column NIPS style, with the addition of a few extra options suitable for reports.

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

To avoid loading the natbib package, add option nonatbib:
```TeX
\usepackage[nonatbib]{report_2019_JiaHuei}
```

By default without options, the package will add line numbers and generate A4 size pages
For preprint, pass "preprint". For anonymised submission, pass "anonymise". For letter size, pass "letter".
To generate final version, pass "final".

```TeX\usepackage{report_2019_JiaHuei}
\usepackage[options1,options2]{report_2019_JiaHuei}
```

