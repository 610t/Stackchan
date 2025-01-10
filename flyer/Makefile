IMAGES= img/cosense.png
IMAGES_EPS= $(IMAGES:%.png=%.eps)
.SUFFIXES: .tex .dvi .pdf .png .eps

all: flyer.pdf ${IMAGES_EPS}

clean:
	rm *.pdf *.dvi *.log *.aux ${IMAGES_EPS}

# SUFFIX rules
.tex.dvi:
	platex $<
	platex $<
	platex $<
.dvi.pdf:
	dvipdfmx $<
.png.eps:
	magick convert $< $@
