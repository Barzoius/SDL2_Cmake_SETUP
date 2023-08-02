cmake_minimum_required(VERSION 3.23)
project(AUTOMATA_THEORY_101)

set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)

find_package(SDL2 REQUIRED)

include_directories(${SDL2_INCLUDE_DIR})

set(CMAKE_CXX_STANDARD 14)

add_executable(AUTOMATA_THEORY_101 CPPS/main.cpp HEADERS/Game.hpp CPPS/Loop.cpp)
target_link_libraries(AUTOMATA_THEORY_101 ${SDL2_LIBRARY} -lmingw32 -lSDL2main -lSDL2 -mwindows)
