# Overview

This repository contains a computer-readable version (in
[LaTeX](https://www.tug.org/texlive/) format) of one of the many reports on the
U.S. Department of Defense’s struggle with software acquisition.

The report here, the 1987 Defense Science Board report (led by Fred Brooks,
famous for [Brooks’s Law](https://en.wikipedia.org/wiki/Brooks%27s_law)), is
available today from the DoD's [DTIC
website](https://apps.dtic.mil/dtic/tr/fulltext/u2/a188561.pdf) as a scanned
PDF. Although the text is already OCR’d (which made it possible to convert), it
was scanned from a poor quality original and as a result is both hard to read
at times and very large to download.

So I took it upon myself to make a version that I could post on a Github.

Right now there is just the LaTeX source and the generated PDF itself. Later I
might try to do an HTML conversion but for now I am happy with where it is at.

# Generating the PDF

The generated PDF should be available [directly from the
repository](https://github.com/mpyne-navy/dsb-report/blob/master/dsb-report.pdf)
but if you make changes to the LaTeX source you’ll probably want to be able to
rebuild yourself.

If you want to generate a PDF version yourself after making changes, here’s all
I did:

    xelatex dsb-report.tex
    xelatex dsb-report.tex

The result is saved as `dsb-report.pdf` if everything goes well.

You have to run LaTeX twice to adapt to the possibility of new citations, new
sections renumbering LaTeX counters, etc.

## Fonts

As you can tell from the command line, I used the XeTeX/XeLaTeX variant, which
permits direct use of Unicode (such as the “fancy quotes” for proper
typography) and easier support for modern fonts. In this case I used [Crimson
Text](https://fonts.google.com/specimen/Crimson+Text?selection.family=Crimson+Text:400,400i,700,700i)
from Google Fonts, and those fonts need to be present in the same directory for
this to work with XeLaTeX.

---

 - Michael Pyne, Feb. 2020
