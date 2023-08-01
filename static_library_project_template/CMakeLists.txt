# Setting cmake minimum version required
cmake_minimum_required(VERSION 3.25)

# Setting project name and the initial version with their languages
project(
  static_library_project_template
  VERSION 
  1.0.0 
  LANGUAGES 
  C
)

# -- Setting environment variables --
set(LIBRARY_NAME helloWorldLibrary)
set(EXECUTABLE_NAME static_library_app)

# Every subdirectories included on my project
add_subdirectory(lib)
add_subdirectory(src)