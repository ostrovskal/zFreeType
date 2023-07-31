
cmake_minimum_required(VERSION 3.22.1)

project(zFreeType VERSION 1.0.0 LANGUAGES C)

include_directories(D:/Dev/Include/)

set(FT2_BUILD_LIBRARY "1")

add_library(freetype STATIC
	autofit/autofit.c
	base/basepic.c
	base/ftapi.c
	base/ftbase.c
	base/ftbbox.c
	base/ftbitmap.c
	base/ftdbgmem.c
	base/ftdebug.c
	base/ftglyph.c
	base/ftinit.c
	base/ftpic.c
	base/ftstroke.c
	base/ftsynth.c
	base/ftsystem.c
	cff/cff.c
	pshinter/pshinter.c
	psnames/psnames.c
	raster/raster.c
	sfnt/sfnt.c
	smooth/smooth.c
	truetype/truetype.c 
)

target_include_directories(freetype PUBLIC include)
target_link_libraries(freetype android log)
