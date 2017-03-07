SRC := $(wildcard *.md)
HTML := $(SRC:.md=.html)
PDF := $(SRC:.md=.pdf)

.PHONY: clean

all:	html pdf

html:
	pandoc -f markdown -t html5 -s -S -o $(HTML) $(SRC)

pdf:
	pandoc -f markdown -s -S -o $(PDF) $(SRC)

clean:
	rm -f $(HTML) $(PDF)
