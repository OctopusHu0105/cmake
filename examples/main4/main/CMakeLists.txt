include_directories(${project_source_dir}/func_lib)

aux_source_directory(./ source)

add_executable(hello ${source})
target_link_libraries(hello func_lib) 
