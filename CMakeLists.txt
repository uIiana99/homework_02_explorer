cmake_minimum_required(VERSION 3.2.2)

project(explorer)

set(PRINT_VERSION_MAJOR 0)
set(PRINT_VERSION_MINOR 1)
set(PRINT_VERSION_PATCH 0)
set(PRINT_VERSION_TWEAK 0)
set(PRINT_VERSION ${PRINT_VERSION_MAJOR}.${PRINT_VERSION_MINOR}.${PRINT_VERSION_PATCH}.${PRINT_VERSION_TWEAK})
set(PRINT_VERSION_STRING "v${PRINT_VERSION}")

set(CMAKE_CXX_COMPILER "g++")
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


set(SOURCE_FILES main.cpp)
add_executable(explorer ${SOURCE_FILES})
target_link_libraries(${PROJECT_NAME} -lboost_system -lboost_filesystem -pthread)

include(CPackConfig.cmake)
