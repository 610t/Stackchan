IMAGES_PNG= img/cosense.png img/discord.png img/X.png img/stackchan-salespoint.png
IMAGES_JPG= img/stackchan-body-history.jpg
IMAGES_EPS= $(IMAGES_PNG:%.png=%.eps) $(IMAGES_JPG:%.jpg=%.eps)
.SUFFIXES: .tex .dvi .pdf .png .eps .jpg

all: flyer.pdf ${IMAGES_EPS}

clean:
	rm *.pdf *.dvi *.log *.aux ${IMAGES_EPS}

# SUFFIX rules
.tex.dvi:
	platex $<
	#platex $<
	#platex $<
.dvi.pdf:
	dvipdfmx $<
.png.eps:
	magick convert $< $@
.jpg.eps:
	magick convert $< $@
