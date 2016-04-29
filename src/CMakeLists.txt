#according to cmake doc not recommend - just don't forget to run cmake
file(GLOB ARMAKE_SOURCES *.c)

add_executable(armake ${ARMAKE_SOURCES})

target_link_libraries(armake minilzo sha1 m)
