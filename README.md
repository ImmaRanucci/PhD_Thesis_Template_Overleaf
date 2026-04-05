# PhD Thesis LaTeX Template

**University of Florence – PhD in Development Economics and Local Systems (DELoS)**

---

## Overview

This repository provides a structured LaTeX template for writing a PhD thesis in accordance with the guidelines of the University of Florence, specifically for the DELoS PhD program.

The template is designed for:

* Multi-chapter theses (article-based or monograph)
* Chapter-specific bibliographies
* Clean frontmatter and appendix organization
* Professional formatting with minimal setup required

---

## Features

* Type of document: book, divided into chapters
* A4 layout with predefined margins
* Times-like font with consistent math formatting
* Chapter-level bibliographies using `biblatex`
* Custom chapter author support
* Fully structured frontmatter (abstract, lists, acknowledgments)
* Built-in support for tables, figures, and appendices
* Hyperlinked references and table of contents
* Modular structure (separate files for chapters and sections)

---

## Project Structure

```
.
├── main.tex
├── references.bib
├── Frontmatter/
│   ├── frontespizio_tesi_eng.pdf
│   ├── Abstract.tex
│   ├── Acronyms.tex
│   └── Acknowledgments.tex
├── Chapter/
│   ├── Chapt0_intro/
│   ├── Chapt1/
│   ├── Chapt2/
│   ├── Chapt3/
│   └── Chapt4_conclusions/
```
* Notice that there is only one references.bib file for the whole document. 
* Make sure there is no duplicate entries in the references.bib file.
---

## Compilation

This template uses `biblatex`, so you must compile with:

```
pdflatex main.tex
biber main
pdflatex main.tex
pdflatex main.tex
```

Alternatively, use an editor like Overleaf or configure your IDE accordingly.

---

## Frontmatter

The frontmatter includes:

* Cover page (PDF inclusion)
* Abstract
* Table of contents
* List of figures
* List of tables
* Acronyms (manual)
* Acknowledgments

### Notes

* The cover page must be prepared separately and included as a PDF.
* The package includes the official template page provided by the University of Florence (a.y. 2025-2026).
* Page numbering is in Roman numerals in this section.

---

## Chapters

Each chapter is structured as follows:

* Chapter title (short and long versions supported)
* Optional footnote for acknowledgments
* Chapter authors (custom command) - notice that authors also appear in the table of contents for each chapter.
* Chapters' content is recalled in the main.tex via `\input{}`


## Bibliography

* Chapter-specific bibliography, with References included at the end of every chapter. 
* Managed with `biblatex`
* Uses author-year citation style


## Appendices

* Organized by chapter
* Located at the end of the documents.
* Automatically labeled with letters (A, B, C, …)
* It is possible to have multiple appendixes for chapter (i.e., one methodological appendix and one with figures and tables)
* Supports:

  * Figures and tables numbering by section
  * Separate bibliographies per appendix

---


## Notes & Recommendations

* Acronyms are **not automatically generated** – update manually.
* Reset counters (e.g., footnotes) manually when needed in appendices.
* Use modular files (`\input`) to keep the project clean.


## Requirements

Make sure your LaTeX distribution includes:

* `biblatex` + `biber`
* Standard AMS packages
* `frontespizio` (for Italian-style cover pages)
* `fancyhdr`, `geometry`, `hyperref`

---

## License / Usage

This template is provided for academic use.
Adapt and modify as needed to comply with your department’s requirements.

---

## Acknowledgments

This template is inspired by the formatting guidelines of the University of Florence, PhD program in Development Economics and Local Systems (DELoS).  
I thank Giovanni Poli and Lisa Braito for providing a background template that served as the foundation for this work.

---
