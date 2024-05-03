cmake_minimum_required(VERSION 3.22.0)

project(Dynamic_Library)

add_executable(DynamicLibrary DynLibClient.cpp)

set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)

add_library(DynamicLib SHARED DynLib.h DynLib.cpp)

target_link_libraries(DynamicLibrary DynLibClient.cpp)