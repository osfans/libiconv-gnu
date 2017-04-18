project(ICONV)

configure_file(
  include/iconv.h
  ${CMAKE_BINARY_DIR}/include/iconv.h
  COPYONLY)
  
set(ICONV_SOURCES
  libcharset/lib/localcharset.c
  lib/iconv.c
  lib/relocatable.c
  )
include_directories(./ lib libcharset/include)
add_library(iconv ${ICONV_SOURCES})
