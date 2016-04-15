TARGET := ALERT-TagDVCS

default: pdf

pdf: 
	pdflatex $(TARGET).tex
	bibtex  $(TARGET).aux
	#makeindex $(TARGET)
	pdflatex $(TARGET).tex
	pdflatex $(TARGET).tex

embed_font:
	gs -o temp.pdf   -sDEVICE=pdfwrite   -dPDFSETTINGS=/prepress  $(TARGET).pdf
	mv temp.pdf $(TARGET).pdf


dvi:
	latex 

.PHONY: all clean

clean: 
	rm -f $(TARGET).pdf
	rm -f *.aux
	rm -f *.log
	rm -f $(TARGET).lof
	rm -f $(TARGET).lot
	rm -f $(TARGET).toc
	rm -f $(TARGET).idx
	rm -f $(TARGET).out
	rm -f $(TARGET).bbl
	rm -f $(TARGET).blg


