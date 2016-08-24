cmake_minimum_required(VERSION 2.8)
project(kazlog)

add_library(
    kazlog
    SHARED
    kazlog/kazlog.cpp
)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++1y -pthread")

install(TARGETS kazlog DESTINATION lib)
install(DIRECTORY kazlog DESTINATION include/kazlog FILES_MATCHING PATTERN *.h)
