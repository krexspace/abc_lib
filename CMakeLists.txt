cmake_minimum_required (VERSION 3.0)
project (abc)

file(GLOB_RECURSE HEADER_FILES ./*.h)
file(GLOB_RECURSE SRC_FILES ./*.cpp)

add_library(abc STATIC ${HEADER_FILES} ${SRC_FILES} )