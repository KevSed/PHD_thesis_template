SHELL=bash
OUTDIR=build
MATPLOTLIBRC=plots/matplotlibrc
DATADIR=../data

all: build/phd_thesis.pdf

build/phd_thesis.pdf: FORCE
	latexmk \
		--lualatex \
		--interaction=nonstopmode \
		--halt-on-error \
		--output-directory=build \
		phd_thesis.tex
	cp $@ .

preview: FORCE
	latexmk \
		--lualatex \
		--interaction=nonstopmode \
		--halt-on-error \
		--output-directory=build \
		-pvc \
		phd_thesis.tex

FORCE:

clean:
	rm -rf build


.PHONY: all clean FORCE
