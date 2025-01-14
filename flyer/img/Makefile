IMAGES_SVG= stackchan.svg stackchan-photo.svg
IMAGES_PNG= cosense.png discord.png X.png \
  Stackchan_flyer.png stackchan-many.png stackchan-salespoint.png
IMAGES_JPG= stackchans.jpg
IMAGES_EPS= $(IMAGES_PNG:%.png=%.eps) $(IMAGES_JPG:%.jpg=%.eps) $(IMAGES_SVG:%.svg=%.eps)
.SUFFIXES: .png .eps .jpg .svg

all: ${IMAGES_EPS}

clean:
	rm *.eps

# SUFFIX rules
.png.eps:
	magick convert $< $@
.jpg.eps:
	magick convert $< $@
.svg.eps:
	magick convert $< $@
