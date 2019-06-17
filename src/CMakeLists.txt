
add_executable( main.out 
    main.c )

target_include_directories( main.out
    PUBLIC ${CMAKE_SOURCE_DIR}/include
)

if(CMAKE_COMPILER_IS_GNUCC OR CMAKE_COMPILER_IS_GNUCXX)
    set( DEBUG_COMPILE_OPTIONS -g -W -Wall)
endif()

target_compile_options( main.out
    PUBLIC ${DEBUG_COMPILE_OPTIONS} )

    