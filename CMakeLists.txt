cmake_minimum_required (VERSION 3.0)
project (abc)

# Compiler and linker flags
set(CMAKE_CXX_FLAGS                " ${CMAKE_CXX_FLAGS_INIT} -std=c++14 -fPIC")
set(CMAKE_CXX_FLAGS_DEBUG          "-g -DDEBUG")
set(CMAKE_CXX_FLAGS_MINSIZEREL     "-Os -DNDEBUG")
set(CMAKE_CXX_FLAGS_RELEASE        "-O4 -DNDEBUG")
set(CMAKE_CXX_FLAGS_RELWITHDEBINFO "-O2 -g -DDEBUG")

file(GLOB_RECURSE HEADER_FILES ./*.h)
file(GLOB_RECURSE SRC_FILES ./*.cpp)

add_library(abc STATIC ${HEADER_FILES} ${SRC_FILES} )
