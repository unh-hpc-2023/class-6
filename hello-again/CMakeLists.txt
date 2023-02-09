cmake_minimum_required (VERSION 3.16)

project(HelloCpp)

add_library(stuff greeting.cxx factorial.cxx hello.h)

add_executable(hello hello.cxx)
target_link_libraries(hello PRIVATE stuff)

add_executable(test_factorial test_factorial.cxx)
target_link_libraries(test_factorial PRIVATE stuff)
