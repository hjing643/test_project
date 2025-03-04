#Make 最低版本
cmake_minimum_required(VERSION 2.8)

#set project name
project(test_project)

# set c++ version
set(CMAKE_CXX_STANDARD 14)

#set debug
set(CMAKE_BUILD_TYPE Debug)

#set release + debug infor
#set(CMAKE_BUILD_TYPE RelWithDebInfo)
#add source file, cpp file add to parameter SOURCES
file(GLOB_RECURSE SOURCES "src/*.cpp")

# 添加库的头文件

#debug 
message(STATUS "Sources: ${SOURCES}")

# to static library .a(achive library)
# to share library .so(shared object)
#add_library(network_program SHARE ${SOURCES} ${HEADERS})

#cpp to exe file
add_executable(test_program ${SOURCES})
#install .a or .so to lib, .exe to bin

#install header file to include

