cmake_minimum_required( VERSION 2.8 )

project( helloSLAM )

add_executable( helloSLAM helloSLAM.cpp )
# add_library( hello libHelloSLAM.cpp ) #静态库
add_library( hello_shared SHARED libHelloSLAM.cpp )#共享库
add_executable( useHello useHello.cpp )
target_link_libraries( useHello hello_shared )