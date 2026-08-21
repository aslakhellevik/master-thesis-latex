# Master's Thesis
## Network Effects of Social Media Use on Well-Being

This repository contains the LaTeX source for Aslak Hellevik's University of Oslo master's thesis:

**Network Effects of Social Media Use on Well-Being**  
*From Agent-Based Models to Statistical Inference*

The repository contains the final manuscript, bibliography, figures, and bundled UiO class files needed to compile the document.

The published thesis (PDF) is openly available at
[NVA](https://nva.sikt.no/registration/019fdb8244e4-e2b85e96-eac5-46e1-a84f-bf7f265abef4),
and the code reproducing every figure and table lives in
[master-thesis-code](https://github.com/aslakhellevik/master-thesis-code).

## Repository Layout

```text
main.tex                 Main entry point
preamble.tex             Packages, macros, theorem environments, and settings
references.bib           Bibliography database
main.pdf                 Latest compiled PDF

frontmatter/
  abstract.tex
  acknowledgements.tex
  ai_declaration.tex
  notation.tex

chapters/
  ch1_introduction.tex
  ch2_background.tex
  ch3_abm_investigation.tex
  ch4_recursive_model.tex
  ch5_estimation.tex
  ch6_monte_carlo.tex
  ch7_simultaneous.tex
  ch8_discussion_and_conclusion.tex

appendices/
  appA_code_documentation.tex

figures/                 Thesis figures used throughout the manuscript
uio-templates/           UiO class/style/logo files used by the document
```

## Thesis Structure

The current manuscript is organised as follows:

1. Introduction
2. Background theory
3. Agent-based model investigation
4. The recursive CoMO model
5. Estimation of the recursive CoMO model
6. Monte Carlo study
7. The simultaneous CoMO model
8. Discussion and conclusion

The appendix covers computational details and numerical verification.

## Build Notes

`main.tex` is the root document. It already points LaTeX to `uio-templates/`, so the UiO class files do not need to be installed separately as long as you keep the repository structure intact.

The document uses:

- `uiomasterthesis` and `uiomasterfp` from `uio-templates/`
- `biblatex` with the `biber` backend
- `graphicspath{{figures/}{uio-templates/}}` from `preamble.tex`

## Compile Locally

Use a LaTeX distribution with `pdflatex` and `biber` available.

```bash
pdflatex main
biber main
pdflatex main
pdflatex main
```

The extra LaTeX pass resolves cross-references and bibliography links.

## Compile in Overleaf

1. Upload the repository as-is.
2. Set `main.tex` as the main file.
3. Use `pdfLaTeX` as the compiler.
4. Recompile; Overleaf will handle the `biber` step automatically.

Do not remove the `uio-templates/` folder, since `main.tex` depends on it for the UiO class and front-page assets.

## Current Front Matter Setup

`main.tex` includes:

- abstract
- acknowledgements
- AI usage declaration
- table of contents
- list of figures
- list of tables
- notation/abbreviations

## License

The text and figures of this thesis are licensed under the [Creative Commons Attribution 4.0 International License (CC-BY-4.0)](https://creativecommons.org/licenses/by/4.0/). See [LICENSE](LICENSE) for the full text.

The `uio-templates/` directory contains University of Oslo template and logo files redistributed under their original terms; the CC-BY-4.0 license does not apply to those files.
