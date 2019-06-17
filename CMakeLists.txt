cmake_minimum_required( VERSION 3.10 )
project ( template VERSION 0.0.1 )

if( ${CMAKE_BINARY_DIR} STREQUAL ${CMAKE_SOURCE_DIR})
    message(FATAL_ERROR "
    In-Source build is not allowed,
    You should create a seprated directory for build results")
endif()

if( CMAKE_BUILD_TYPE STREQUAL "")
    set( CMAKE_BUILD_TYPE "Debug")
    message( STATUS "
    Default build type : ${CMAKE_BUILD_TYPE}" )
endif()


add_subdirectory(src)