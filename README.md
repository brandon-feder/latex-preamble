# Brandon's Preamble

This repository contains the preamble I use most of the time I am writing up a LaTeX document (or Beamer slideshow). Feel free to use!

## Preamble Settings

You can change basic settings by defining certain variables *before* inputting `brandons-preamble.tex`:

* To turn off custom styling, define `\optionNoStyling`.
* To use number theorems, definition, etc. by section (resp. subsection), define `\optionThrmNumberingBySection` (resp `\optionThrmNumberingBySubsection`).
* To turn off custom theorem coloring, define `\optionNoTheoremColoring`
* To number problem environments seperetly from other environments, define `\probNumeringSeperate`.
* To color theorem environments gray-scale, define `\optionTheoremColoringGray`
* For a less colorful theorem environements (only theorems, problems, and definitions are colored), define `\optionTheoremLessColoring`.
* To enable the mandelbrot set background image, set `\optionEnableBgImage`

## FontsoptionTheoremColoringGray

* To use [Antykwa Toruńska](https://www.tug.org/FontCatalogue/antykwatorunska/), add `\usepackage[light,math]{anttor}`.
* To use [MLModern](https://tug.org/FontCatalogue/mlmodern/), add `\usepackage{mlmodern}`.
* To use adobe utopia [Adobe Utopia](https://tug.org/FontCatalogue/utopia-mathdesign/), add `\usepackage[adobe-utopia]{mathdesign}`.

## Adding to texmf directory

```{bash}
cd ./preamble
latexpand ./brandons-preamble.tex > ../expanded/brandons-preamble.sty
cp ../expanded/brandons-preamble.sty ~/texmf/tex/latex/
cp ./mandelbrot-bg.jpg ~/texmf/tex/latex/
texhash ~/texmf

# all in one
cd ./preamble; latexpand ./brandons-preamble.tex > ../expanded/brandons-preamble.sty; cp ../expanded/brandons-preamble.sty ~/texmf/tex/latex/; cp ./mandelbrot-bg.jpg ~/texmf/tex/latex/; texhash ~/texmf
```
