# Setting cmake minimum version required
cmake_minimum_required(VERSION 3.25)

# Setting project name and the initial version with their languages
project(
  shared_library_project_template
  VERSION 
  1.0.0 
  LANGUAGES 
  C
)

# -- Setting environment variables --
set(LIBRARY_NAME shared_library)
set(EXECUTABLE_HELLO_WORLD_NAME hello_world)
set(EXECUTABLE_GOODBYE_WORLD_NAME goodbye_world)

# Every subdirectories included on my project
add_subdirectory(shared_lib)
add_subdirectory(hello_world)
add_subdirectory(goodbye_world)