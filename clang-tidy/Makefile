all: clang-tidy.slidy.html clang-tidy.dz.html # clang-tidy.pdf

%.slidy.html: %.md em.pandoc.slidy em.slidy.css Makefile
	pandoc --output $@ --slide-level=1 --highlight-style pygments \
		--template=./em.pandoc.slidy -t slidy --css ./em.slidy.css --standalone $<

%.dz.html: %.md
	pandoc --output $@ --slide-level=1 --highlight-style pygments -t dzslides --standalone $<

%.pdf: %.md
	pandoc --output $@ --latex-engine=xelatex --slide-level=1 --highlight-style pygments -t beamer --standalone $<
