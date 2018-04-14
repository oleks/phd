base:=master

all:
	./latexrun \
	  --latex-args="-shell-escape" \
	  --bibtex-cmd="biber" \
	  $(base).tex

clean:
	rm -f $(base).pdf
	rm -rf _minted-$(base)
	rm -rf latex.out

.PHONY: all clean
