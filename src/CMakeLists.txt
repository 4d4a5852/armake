#according to cmake doc not recommend - just don't forget to run cmake
file(GLOB ARMAKE_SOURCES *.c)
list(SORT ARMAKE_SOURCES)

add_definitions(-DVERSION="vTODO")
add_executable(armake ${ARMAKE_SOURCES})

find_package(OpenSSL REQUIRED)

include_directories(${OPENSSL_INCLUDE_DIR})
target_link_libraries(armake minilzo sha1 m ${OPENSSL_LIBRARIES})
