cmake_minimum_required(VERSION 3.10)

project(main LANGUAGES CXX)


if (DEBUG)
    add_compile_options(-Wall -Werror -Wextra)
    add_compile_options(-g3 -ggdb -g)
endif()


set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

add_subdirectory(lib)
include_directories(lib)
add_subdirectory(src)