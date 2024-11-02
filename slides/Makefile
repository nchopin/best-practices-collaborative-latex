all: pdf html

html: slides.qmd
	quarto render slides.qmd --to revealjs

pdf: slides.qmd
	quarto render slides.qmd --to beamer
