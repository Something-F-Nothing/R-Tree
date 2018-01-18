project(rtree)

set(HEADERS_FILES
    inc/rtreenode.hpp
    inc/rtree.hpp
    )

set(SOURCES_FILES
    src/rtreenode.cpp
    src/rtree.cpp
    )

add_library(rtree STATIC ${HEADERS_FILES} ${SOURCES_FILES})

target_include_directories(rtree
    PUBLIC $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/inc>
    PUBLIC $<INSTALL_INTERFACE:inc/rtree>
    )

add_subdirectory(test)
