cmake_minimum_required(VERSION 3.0)

project(eigen4rkt VERSION 3.3.90.4 LANGUAGES CXX)

include(ExternalProject)

ExternalProject_Add(eigen
    PREFIX etc
    GIT_REPOSITORY https://gitlab.com/libeigen/eigen.git
    GIT_TAG 9a4d04c05fbaad6e6de750b13cfeab9edeb71c90
    GIT_SHALLOW TRUE
    GIT_PROGRESS TRUE
    CMAKE_ARGS
        -DCMAKE_GENERATOR=${CMAKE_GENERATOR}
        -DCMAKE_PREFIX_PATH=${CMAKE_PREFIX_PATH}
        -DCMAKE_BUILD_TYPE=${CMAKE_BUILD_TYPE}
        -DCMAKE_INSTALL_PREFIX=${CMAKE_INSTALL_PREFIX}
        -DEIGEN_BUILD_PKGCONFIG=${EIGEN_BUILD_PKGCONFIG})
