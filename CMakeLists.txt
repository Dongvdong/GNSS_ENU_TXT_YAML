cmake_minimum_required(VERSION 3.10)
 
project(ReadTextFile)
 
# 设置 C++ 标准为 C++11
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)


# 包含GeographicLib的头文件路径
include_directories("/usr/include/GeographicLib")


# 添加可执行文件，并链接主程序文件和自定义类的头文件
add_executable(node main.cpp)

set(YAML_CPP_LIBRARIES ${CMAKE_SOURCE_DIR}/src/libyaml-cpp.a)
target_link_libraries(node ${YAML_CPP_LIBRARIES} Geographic)