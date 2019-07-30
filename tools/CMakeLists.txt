FILE(GLOB KlVancToolsCSources *.c)
add_executable (vanc ${KlVancToolsCSources})

target_compile_options(vanc PUBLIC "-pthread")
target_link_libraries (vanc LINK_PUBLIC libklvanc pthread)

install(TARGETS vanc DESTINATION bin)
