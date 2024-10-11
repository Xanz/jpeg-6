cmake_minimum_required(VERSION 3.13.0)
project(libjpeg VERSION 0.0.0.1)

file(GLOB_RECURSE JPGSRC src/*.cpp include/*.h)

set(JPGSource
    ${JPGSRC}
    )

# Set the C++ standard
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

include_directories(include/ PUBLIC)

set(LIBS)

add_library(${PROJECT_NAME} ${JPGSource})