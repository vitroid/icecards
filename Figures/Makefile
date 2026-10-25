inkscape=/Volumes/Shared/Applications2/Inkscape.app/Contents/Resources/bin/inkscape-bin --without-gui

ices:
	for j in png svg; do for i in 0 1h 2 3 4R 5 6 7 12 16 17 iceR iceT iceT2 i xFAU[2] CS1; do echo $$i.X0.$$j $$i.Y0.$$j $$i.Z0.$$j $$i.dx.$$j; done; done | xargs make -j 4 -k


all: 1h.0.svg 2d.0.svg 3.0.svg 4R.x.svg 5.x.svg 6.0.svg 7.0.svg 12.0.svg 16.0.svg 17.0.svg iceR.d.svg iceT.dx.svg iceT2.dx.svg\
1h.0.png 2d.0.png 3.0.png 4R.x.png 5.x.png 6.0.png 7.0.png 12.0.png 16.0.png 17.0.png iceR.d.png iceT.dx.png iceT2.dx.png



%.Z0.svg:
	genice $* -f svg[shadow:O=0.05] > $@
%.Y0.svg:
	genice $* -f svg[shadow:O=0.05:rotatex=90] > $@
%.X0.svg:
	genice $* -f svg[shadow:O=0.05:rotatey=90] > $@

%.0.svg: Makefile
	genice $* -f svg[shadow:O=0.05:rotatex=8:rotatey=-8] > $@
%.x.svg: 
	genice $* -f svg[shadow:rotatex=8:rotatey=-8:rotatex=90:O=0.05] > $@
%.d.svg:
	genice $* -f svg[shadow:rotatex=35:rotatey=-135:O=0.05] > $@
%.dx.svg:
	genice $* -f svg[shadow:rotatex=35:rotatey=-135:rotatex=90:O=0.05] > $@
%.png: %.svg
	cairosvg $< -o $@
