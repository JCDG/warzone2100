AM_CPPFLAGS = -DYY_NO_INPUT $(WZ_CPPFLAGS) $(QT4_CFLAGS)
AM_CFLAGS = $(WZ_CFLAGS)
AM_CXXFLAGS = $(WZ_CXXFLAGS) $(QT4_CFLAGS)
AM_LFLAGS = $(FLEX_FLAGS)
AM_YFLAGS = -d

MOCHEADER = wzapp.h
MOCEDFILES = $(MOCHEADER:%.h=%_moc.cpp)

%_moc.cpp: %.h
	$(MOC4) -o $@ $<

BUILT_SOURCES = \
	resource_parser.h \
	strres_parser.h

CLEANFILES = \
	$(MOCEDFILES)

EXTRA_DIST = \
	cocoa_wrapper.h cocoa_wrapper.mm

noinst_LIBRARIES = libframework.a
noinst_HEADERS = \
	$(MOCHEADER) \
	wzapp_c.h \
	crc.h \
	cursors.h \
	debug.h \
	file.h \
	fixedpoint.h \
	frame.h \
	frameint.h \
	frameresource.h \
	geometry.h \
	i18n.h \
	input.h \
	lexer_input.h \
	listmacs.h \
	math_ext.h \
	opengl.h \
	physfs_ext.h \
	resly.h \
	stdio_ext.h \
	string_ext.h \
	strres.h \
	strresly.h \
	treap.h \
	trig.h \
	types.h \
	utf.h \
	vector.h \
	config-macosx.h \
	endian_hack.h \
	gettext.h \
	macros.h \
	wzapp_c.h \
	wzfs.h \
	wzglobal.h

nodist_libframework_a_SOURCES = \
	wzapp_moc.cpp

libframework_a_SOURCES = \
	wzapp.cpp \
	resource_lexer.lpp \
	resource_parser.ypp \
	strres_lexer.lpp \
	strres_parser.ypp \
	crc.cpp \
	debug.cpp \
	frame.cpp \
	frameresource.cpp \
	geometry.cpp \
	i18n.cpp \
	lexer_input.cpp \
	stdio_ext.cpp \
	strres.cpp \
	treap.cpp \
	trig.cpp \
	utf.cpp

