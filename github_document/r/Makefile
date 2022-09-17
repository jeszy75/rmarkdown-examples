sources = $(wildcard *.Rmd)
targets = $(sources:.Rmd=.md)

.PHONY: all
all: $(targets)

%.md: %.Rmd
	Rscript -e 'rmarkdown::render("$<")'

.PHONY: clean
clean:
	rm -rf $(targets:.md=_files)
	rm -f $(targets:.md=.html)
	rm -f $(targets)
	rm -rf rosm.cache
