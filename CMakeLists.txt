cmake_minimum_required(VERSION 3.10.1)
project(RTree)

add_subdirectory(rtree)

add_executable(RTree main.cpp)

target_link_libraries(RTree rtree)
