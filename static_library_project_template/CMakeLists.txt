# Setting cmake minimum version required
cmake_minimum_required(VERSION 3.25)

# Setting project name and the initial version with their languages
project(
  static_library_project_template
  VERSION
  1.0.0
  LANGUAGES
  C CXX
)

# -- Adding modules --

# FetchContent is a module that allows to download and include external projects
include(FetchContent)

# Including fmt module
FetchContent_Declare(
        fmt
        GIT_REPOSITORY https://github.com/fmtlib/fmt
        GIT_TAG 10.2.1
        GIT_SHALLOW TRUE
)
FetchContent_MakeAvailable(fmt)

# Including Catch2 module
FetchContent_Declare(
        Catch2
        GIT_REPOSITORY https://github.com/catchorg/Catch2
        GIT_TAG v3.6.0
        GIT_SHALLOW TRUE
)
FetchContent_MakeAvailable(Catch2)

# Including spdlog module
FetchContent_Declare(
        spdlog
        GIT_REPOSITORY https://github.com/gabime/spdlog
        GIT_TAG v1.14.1
        GIT_SHALLOW TRUE
)
FetchContent_MakeAvailable(spdlog)

# -- Setting environment variables --
set(LIBRARY_NAME helloWorldLibrary)
set(EXECUTABLE_NAME static_library_app)

# Every subdirectories included on my project
add_subdirectory(lib)
add_subdirectory(src)
