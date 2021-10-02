sources = $(wildcard *.Rmd)
targets = $(sources:.Rmd=.pdf)

.PHONY: all
all: $(targets)

%.pdf: %.Rmd
	Rscript -e 'rmarkdown::render("$<")'

.PHONY: clean
clean:
	rm -f $(targets)
