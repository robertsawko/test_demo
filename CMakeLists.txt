cmake_minimum_required(VERSION 2.6)

project (TestDemo CXX)

enable_testing()

add_subdirectory(tests/googletest/googletest)

find_package (Threads)
add_subdirectory(tests)
