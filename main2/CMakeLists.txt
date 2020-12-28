cmake_minimum_required(VERSION 3.5)

project(hello)

aux_source_directory(./ source)

#add_executable(hello main.c func.c)

add_executable(hello ${source})
