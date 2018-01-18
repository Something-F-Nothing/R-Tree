project(csvhandlertest)

set(TEST_FILES
    csvhandlertest.cpp
    )

enable_testing()
add_executable(csvhandlertest ${TEST_FILES})
target_link_libraries(csvhandlertest
    gtest
    gtest_main
    csvhandler
    )
add_test(csvhandlertest csvhandlertest)
