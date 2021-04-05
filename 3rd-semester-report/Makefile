base:=master
makedir:=$(dir $(lastword $(MAKEFILE_LIST)))

all: references.bib
	$(makedir)latexrun \
	  --latex-args="-shell-escape" \
	  --bibtex-cmd="biber" \
	  $(makedir)$(base).tex

references.bib:
	mkdir -p references
	find \
		"$(makedir)references/" \
		-iname "*.bib" \
		-exec cat {} \; > $@

clean:
	$(makedir)latexrun --clean-all

.PHONY: all clean references.bib
