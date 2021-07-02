cmake_minimum_required(VERSION 3.0)

project(eigen4rkt VERSION 3.3.90 LANGUAGES CXX)

execute_process(COMMAND git submodule update --init --recursive
    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR})

add_subdirectory(eigen)
