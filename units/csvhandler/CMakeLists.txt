project(csvhandler)

set(HEADERS_FILES
    inc/csvhandler.hpp
    )

set(SOURCES_FILES
    src/csvhandler.cpp
    )

add_library(csvhandler STATIC ${HEADERS_FILES} ${SOURCES_FILES})

target_include_directories(csvhandler
    PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/inc>
    PUBLIC $<INSTALL_INTERFACE:inc/rtree>
    )

add_subdirectory(test)
