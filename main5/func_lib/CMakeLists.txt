aux_source_directory(./ source)

set(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib)

add_library(func_lib  ${source})
