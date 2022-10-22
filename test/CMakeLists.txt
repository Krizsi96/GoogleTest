cmake_minimum_required(VERSION 3.0)

set(This GoogleTestTests)

set(Sources 
    ExampleTests.cpp
)

add_executable(${This} ${Sources})
target_link_libraries(${This} PUBLIC
    gtest_main
    Example
)

add_test(
    NAME ${This}
    COMMAND ${This}
)