add_subdirectory(shared)

set(LIBRARY_SOURCES shared/hello_lib/hello.c shared/goodbye_lib/goodbye.c)
set(LIBRARY_HEADERS shared/hello_lib/hello.h shared/goodbye_lib/goodbye.h
        ../goodbye_world/src/main.c)

# Declare the library
add_library(
        ${LIBRARY_NAME}
        SHARED
        ${LIBRARY_SOURCES}
        ${LIBRARY_HEADERS}
)

target_include_directories(${LIBRARY_NAME} PUBLIC "./")