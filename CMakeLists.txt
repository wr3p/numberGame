cmake_minimum_required(VERSION 3.5)
project(numberGame)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(numberGame main.cpp)

if(WIN32)
    message(STATUS "Configuring for Windows")
    target_compile_definitions(numberGame PRIVATE _CRT_SECURE_NO_WARNINGS)
elseif(UNIX)
    message(STATUS "Configuring for Linux / macOS")
    target_compile_options(numberGame PRIVATE -Wall -Wextra -pedantic)
endif()
