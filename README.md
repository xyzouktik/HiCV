<div align="center">

# HiCV

**A clean, Overleaf-ready LaTeX curriculum vitae.**
One source, versioned on GitHub, typeset for print.

[Portfolio](https://xyzouktik.github.io/) · [LinkedIn](https://www.linkedin.com/in/youktik-sajjan) · [GitHub](https://github.com/xyzouktik)

</div>

---

## Overview

HiCV is the LaTeX source of my curriculum vitae. It is written for [Overleaf](https://www.overleaf.com/) and kept here so the document has a history, a home, and a single point of truth. The layout is deliberately quiet: black ink on white paper, generous margins, and a clear hierarchy that lets the work speak.

The web edition remains at **[xyzouktik.github.io/cv.html](https://xyzouktik.github.io/cv.html)**.

## Files

| Path | Purpose |
| --- | --- |
| `cv.tex` | The CV source. This is the main document. |
| `cv.pdf` | The compiled two-page CV. |
| `.github/workflows/build.yml` | Compiles the CV on every push and uploads the PDF as an artifact. |
| `README.md` | This file. |

## Open in Overleaf

1. Create a new Overleaf project and choose **Upload Project**.
2. Upload `cv.tex`, or the repository as a ZIP.
3. Set **Menu → Compiler** to **pdfLaTeX**.
4. Recompile.

To keep Overleaf and GitHub in sync, use **New Project → Import from GitHub** and select `xyzouktik/HiCV`.

## Build locally

A TeX distribution with `latexmk` is all that is required.

```bash
latexmk -pdf cv.tex
```

The result is `cv.pdf`. To clean the auxiliary files afterwards:

```bash
latexmk -C
```

## Editing

- **Contact details and links** live in the header block of `cv.tex`, inside `\href{...}`.
- **Sections** are introduced with `\cvsection{...}` and entries with `\cventry{title}{date}{body}`.
- **Skills** use `\skill{label}{details}`.
- **Hyperlinks** are ordinary `\href{url}{text}` links. They stay clickable in the PDF without colouring the text, so the printed page remains black and white.

## Design

A4 paper · 10 pt Latin Modern · small-caps rules · 0.72 in margins · two pages.

---

<div align="center"><sub>Maintained by <a href="https://github.com/xyzouktik">Youktik Sajjan</a> · Kolkata, India</sub></div>
