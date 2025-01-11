IMAGES_PNG= img/cosense.png img/discord.png img/X.png \\
	img/stackchan-salespoint.png img/Stackchan_flyer.png \\
	img/stackchan-many.png
IMAGES_JPG= img/stackchan-body-history.jpg img/stackchans.jpg
IMAGES_EPS= $(IMAGES_PNG:%.png=%.eps) $(IMAGES_JPG:%.jpg=%.eps)
.SUFFIXES: .tex .dvi .pdf .png .eps .jpg

all: flyer.pdf ${IMAGES_EPS}

deploy: flyer.pdf
	scp flyer.pdf sacraya.610t.org:/usr/local/www/nginx/Stackchan/

clean:
	rm *.pdf *.dvi *.log *.aux ${IMAGES_EPS}

# SUFFIX rules
.tex.dvi:
	uplatex $<
	#uplatex $<
	#uplatex $<
.dvi.pdf:
	dvipdfmx $<
.png.eps:
	magick convert $< $@
.jpg.eps:
	magick convert $< $@
