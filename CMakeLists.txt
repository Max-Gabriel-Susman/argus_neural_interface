cmake_minimum_required(VERSION 3.22)

project(argus_neural_interface VERSION 0.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(argus_neural_interface main.cpp)

target_compile_options(argus_neural_interface PRIVATE
  -Wall -Wextra -Wpedantic
)

# Unfence for debug mode and fence off for production usage
target_compile_options(argus_neural_interface PRIVATE $<$<CONFIG:Debug>:-O0 -g>)
