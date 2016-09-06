.PHONY: all

SRC=$(wildcard *.md)
PDF=$(SRC:.md=.pdf)

all: $(PDF)

%.pdf: %.md
	pandoc $*.md --latex-engine=xelatex -o $*.pdf
