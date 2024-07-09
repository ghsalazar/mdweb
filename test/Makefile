.POSIX:

TARGET = hello

all: $(TARGET).c $(TARGET).pdf

.SUFFIXES: .c .mdw .pdf .tex

.mdw.c:
	notangle -R$@ $< > $@

.mdw.tex:
	../src/mdw2nw $< | noweave -delay > $@

.tex.pdf:
	latexmk -xelatex -pdf $<
	latexmk -c $<

clean:
	rm -f $(TARGET).c $(TARGET).md
