cmake_minimum_required(VERSION 2.8)
project(gaussNewton)

find_package(OpenCV REQUIRED)

include_directories("/usr/include/eigen3")

add_executable(gaussNewton gaussNewton.cpp)
target_link_libraries(gaussNewton ${OpenCV_LIBS})