
bin_PROGRAMS = gnome-fixpng-thumbnailer

gnome_fixpng_thumbnailer_SOURCES = gnome-fixpng-thumbnailer.c gnome-thumbnailer-skeleton.c gnome-thumbnailer-skeleton.h
gnome_fixpng_thumbnailer_CPPFLAGS =		\
	$(THUMBNAILER_CFLAGS)			\
	-DTHUMBNAILER_RETURNS_PIXBUF		\
	-DTHUMBNAILER_USAGE="\"Thumbnail iOS-optimised PNGs\""
gnome_fixpng_thumbnailer_LDADD = $(THUMBNAILER_LIBS)

thumbnailerdir = $(datadir)/thumbnailers/
thumbnailer_DATA = gnome-fixpng-thumbnailer.thumbnailer
gnome-fixpng-thumbnailer.thumbnailer: gnome-fixpng-thumbnailer.thumbnailer.in Makefile
	$(AM_V_GEN) $(SED) -e "s|\@bindir\@|$(bindir)|" $< > $@

EXTRA_DIST = gnome-fixpng-thumbnailer.thumbnailer.in AUTHORS COPYING README

CLEANFILES = gnome-fixpng-thumbnailer.thumbnailer
