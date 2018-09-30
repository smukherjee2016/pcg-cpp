cmake_minimum_required(VERSION 3.1)

if(${CMAKE_VERSION} VERSION_LESS 3.12)
    cmake_policy(VERSION ${CMAKE_MAJOR_VERSION}.${CMAKE_MINOR_VERSION})
else()
    cmake_policy(VERSION 3.12)
endif()

project(pcg-cpp VERSION 0.98.0)

add_library(pcg_lib INTERFACE)
target_sources(pcg_lib INTERFACE
        "${CMAKE_CURRENT_LIST_DIR}/include/"
        )
target_include_directories(pcg_lib INTERFACE "${CMAKE_CURRENT_LIST_DIR}/include/")
