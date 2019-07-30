FILE(GLOB LibKlVancCSources *.c)
add_library(libklvanc STATIC ${LibKlVancCSources})

target_include_directories (libklvanc PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
#install(TARGETS libklvanc DESTINATION lib)
#install(FILES libklvanc/vanc.h DESTINATION include)
