sources = $(wildcard *.Rmd)
targets = $(sources:.Rmd=.html)

.PHONY: all
all: $(targets)

%.html: %.Rmd
	Rscript -e 'rmarkdown::render("$<")'

.PHONY: clean
clean:
	rm -f $(targets)
