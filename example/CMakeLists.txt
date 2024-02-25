

cmake_minimum_required(VERSION 3.5)

set(PROJECT DisplayImage)

project( ${PROJECT} )

set(CMAKE_CXX_STANDARD 14)

find_package(OpenCV REQUIRED)


message(STATUS "OpenCV_INCLUDE_DIRS = ${OpenCV_INCLUDE_DIRS}")
message(STATUS "OpenCV_LIBS = ${OpenCV_LIBS}")


include_directories(${OpenCV_INCLUDE_DIRS})

add_executable( ${PROJECT} DisplayImage.cpp )
target_link_libraries( ${PROJECT} ${OpenCV_LIBS} )


