include_directories(${project_source_dir}/func_lib)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/bin)

aux_source_directory(./ source)

add_executable(hello ${source})

target_link_libraries(hello func_lib) 
