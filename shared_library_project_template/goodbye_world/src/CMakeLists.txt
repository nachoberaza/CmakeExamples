add_executable(
        ${EXECUTABLE_GOODBYE_WORLD_NAME}
        main.c
)

target_link_libraries(
        ${EXECUTABLE_GOODBYE_WORLD_NAME}
        PUBLIC
        ${LIBRARY_NAME}
)