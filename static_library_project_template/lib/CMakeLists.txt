set(LIBRARY_SOURCES my_lib.c my_another_lib.c)
set(LIBRARY_HEADERS my_lib.h my_another_lib.h)

# Declare the library
add_library(
  ${LIBRARY_NAME}
  STATIC 
  ${LIBRARY_SOURCES}
  ${LIBRARY_HEADERS}
)

target_include_directories(${LIBRARY_NAME} PUBLIC "./")