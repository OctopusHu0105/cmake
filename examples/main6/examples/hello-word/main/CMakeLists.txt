set(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/../)

aux_source_directory(./ source)

add_executable(hello ${source})

target_link_libraries(hello func_libs) 
