cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

project(view)

find_package(PCL 1.7 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (view view.cpp)
set(CMAKE_CXX_FLAGS "-w")
target_link_libraries (view ${PCL_LIBRARIES})
