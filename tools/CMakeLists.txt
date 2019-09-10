find_package(ZLIB REQUIRED)
FILE(GLOB KlVancToolsCSources *.c)
add_executable (vanc ${KlVancToolsCSources})

target_compile_options(vanc PUBLIC "-pthread")
target_link_libraries (vanc LINK_PUBLIC libklvanc pthread ${ZLIB_LIBS})
target_include_directories(vanc PRIVATE ${ZLIB_INCLUDE_DIRS})

install(TARGETS vanc DESTINATION bin)
