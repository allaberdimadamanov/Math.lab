SRC = presentation.md
FILES += $(patsubst %.md, %.pdf, $(wildcard *.md))

FILTERS =
PDF_ENGINE =
PDF_OPTIONS =
PDF_FORMAT_OPTIONS = -t beamer --slide-level=2

FILTERS += --citeproc

PDF_ENGINE += --pdf-engine=xelatex
PDF_OPTIONS += --number-sections

REVEALJS_THEME = beige

%.pdf: %.md
	-@pandoc "$<" $(FILTERS) $(PDF_ENGINE) $(PDF_OPTIONS) $(PDF_FORMAT_OPTIONS) -o "$@"

all: $(FILES)

clean:
	-@rm $(FILES) *~

cleanall: clean