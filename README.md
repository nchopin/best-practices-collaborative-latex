# Best practices for collaborative LaTeX # 

## Course ##

This repository contains course materials for a short course on "best practices
for collaborative LaTeX" for PhD students at CREST. (PhD students from
other institutions are welcome.)

The target audience is first-year PhD students, who are already a bit familiar
with LaTeX (often through Overleaf), and would like to learn tips on how to use
LaTeX effectively, in particular to write scientific papers, jointly with
collaborators.

Covered topics:

* encodings
* (AMS) math: single and multi-line equations, math operators, theorems
* macros
* cross-references
* figures
* LaTeX and git
* bibtex
* latexmk, latexdiff
* slides (using quarto)

## Slides ##

You can preview the slides of the course
[here](https://html-preview.github.io/?url=https%3A%2F%2Fgithub.com%2Fnchopin%2Fbest-practices-collaborative-latex%2Fblob%2Fmaster%2Fslides%2Fslides.html#/title-slide).

These slides were generated with [quarto](https://quarto.org/). Assuming you
have installed quarto, you can generate the html file like this:
```{bash}
quarto render slides.qmd --to revealjs
```

Replace `revealjs` by `beamer` if you'd rather generate the slides in pdf
(beamer) format. There is also a `Makefile` with these commands, in case you
are familiar with the Unix command `make`.

## Template paper ##

Folder `paper` contains a paper template, which you can use as starting point
to write your paper; it imports all the LaTeX packages discussed during the
course.

## Template PhD thesis ## 

TODO 

## .gitignore

As explained in the course, when you use git to keep track of a LaTeX document,
it is best to keep track of the **source files** (i.e., *.tex, *.bib, plus
figures typically in pdf format) only. We want to tell git to ignore: 

* the intermediary files  generated during compilation (log, aux, etc.).

* the output file (i.e., paper.pdf), but on the other hand, we do not want to
  ignore the pdf files that are included as images.

The `.gitignore` (do not forget the dot) file of this repository does precisely
that. You can copy it to the root of your own git repository, and adapt it to
your needs. (This version assumes that the tex files are in folder `paper/` and
the figures are in `paper/figs/`)


## Author ## 

Nicolas Chopin (nicolas.chopin@ensae.fr), Professor of data sciences at the
ENSAE, and LaTeX expert, in the following sense:

"An expert is a person who has found out by his own painful experience all the
mistakes that one can make in a very narrow field.” Niels Bohr 

Comments most welcome.
