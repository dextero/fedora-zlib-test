cmake_minimum_required(VERSION 3.15)

project(zlib-test VERSION 0.1
        DESCRIPTION "zlib dependency test"
        LANGUAGES CXX)

set(CMAKE_FIND_PACKAGE_PREFER_CONFIG ON CACHE BOOL "set to OFF, wipe generated CMake files and rebuild to fix Fedora build")

# note: using lowercase zlib fails regardless of CMAKE_FIND_PACKAGE_PREFER_CONFIG
find_package(ZLIB REQUIRED)

add_executable(${PROJECT_NAME} main.cpp)
target_link_libraries(${PROJECT_NAME} ZLIB::ZLIB)
