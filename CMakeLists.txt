cmake_minimum_required(VERSION 3.10.1)
project(RTree)

add_subdirectory(units/rtree)
add_subdirectory(units/csvhandler)

enable_testing()
add_subdirectory(units/googletest)
include_directories(${gtest_SOURCE_DIR}/include ${gtest_SOURCE_DIR})

add_executable(RTree main.cpp)

target_link_libraries(RTree rtree csvhandler)
