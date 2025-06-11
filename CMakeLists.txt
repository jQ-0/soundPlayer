cmake_minimum_required(VERSION 4.0)
project(soundPlayer)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/$<CONFIGURATION>")
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/$<CONFIGURATION>")

add_subdirectory(vendored/SDL EXCLUDE_FROM_ALL)

set(CMAKE_CXX_STANDARD 20)


add_executable(soundPlayer main.cpp)

target_link_libraries(soundPlayer PRIVATE SDL3::SDL3)