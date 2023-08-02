cmake_minimum_required(VERSION 3.23)
project(PROJECT_NAME)

set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)

find_package(SDL2 REQUIRED)

include_directories(${SDL2_INCLUDE_DIR})

set(CMAKE_CXX_STANDARD 14)

add_executable(PROJECT_NAME main.cpp)
target_link_libraries(PROJECT_NAME ${SDL2_LIBRARY} -lmingw32 -lSDL2main -lSDL2 -mwindows)
