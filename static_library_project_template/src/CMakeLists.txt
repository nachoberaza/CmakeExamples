# Setting environment variables
set(EXE_SOURCES main.c)

# Declare the executable
add_executable(
        ${EXECUTABLE_NAME}
        ${EXE_SOURCES}
)

# Link the library with the executable
target_link_libraries(
        ${EXECUTABLE_NAME}
        PUBLIC
        ${LIBRARY_NAME}
)
