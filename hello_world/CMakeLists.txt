# 0. Create Source and MakeFile
# 1. Create build directory
# 2. cd build
# 3. cmake ..
# 4. cmake --build .
# 5. ./Executable

cmake_minimum_required(VERSION 3.25)

project(
  HelloWorldTemplate
  VERSION 
  1.0.0 
  LANGUAGES 
  C
)

add_executable(
        helloWorldApp
        main.c
)
