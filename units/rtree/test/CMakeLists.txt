project(rtreetest)

set(TEST_FILES
    rtreenodetest.cpp
    rtreetest.cpp
    )

enable_testing()
add_executable(rtreetest ${TEST_FILES})
target_link_libraries(rtreetest
    gtest
    gtest_main
    rtree
    )
add_test(rtreetest rtreetest)
