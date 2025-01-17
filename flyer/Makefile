SUBDIRS= img/
.SUFFIXES: .tex .dvi .pdf

all: flyer.pdf 

flyer.dvi: flyer.tex
	(cd img;make)
	uplatex $<

deploy: flyer.pdf
	scp flyer.pdf sacraya.610t.org:/usr/local/www/nginx/Stackchan/

clean:
	(cd img;make clean)
	rm *.pdf *.dvi *.log *.aux ${IMAGES_EPS}

$(SUBDIRS) : FORCE
	(cd $<; make)

FORCE:

# SUFFIX rules
.tex.dvi:
	uplatex $<
	#uplatex $<
	#uplatex $<
.dvi.pdf:
	dvipdfmx $<
