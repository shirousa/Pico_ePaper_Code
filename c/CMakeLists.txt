cmake_minimum_required(VERSION 3.12)
include(pico_sdk_import.cmake)
project(Pico_ePaper_Code)

# add a compilation subdirectory
add_subdirectory(lib/Config)
add_subdirectory(lib/e-Paper)
add_subdirectory(lib/Fonts)
add_subdirectory(lib/GUI)
add_subdirectory(examples)

# add a header directory
include_directories(examples)
include_directories(./lib/Config)
include_directories(./lib/GUI)
