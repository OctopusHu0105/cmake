cmake_minimum_required(VERSION 3.5)
project(hello)
INCLUDE_DIRECTORIES(./../../components/func_libs/include)
add_subdirectory(./../../components/func_libs func_libs.out)
add_subdirectory(./main)

