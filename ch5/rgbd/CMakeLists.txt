cmake_minimum_required(VERSION 2.8)
project(jointMap)

find_package(Pangolin REQUIRED)
find_package(OpenCV REQUIRED)
find_package(Sophus REQUIRED)

include_directories(${Sophus_INCLUDE_DIRS})

add_executable(jointMap jointMap.cpp)
target_link_libraries(jointMap ${OpenCV_LIBS} ${Pangolin_LIBRARIES} Sophus::Sophus)