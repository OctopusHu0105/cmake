cmake_minimum_required(VERSION 3.5)

project(hello)

add_subdirectory(./func_lib)

aux_source_directory(./ source)

add_executable(hello ${source})

target_link_libraries(hello func_lib) 
