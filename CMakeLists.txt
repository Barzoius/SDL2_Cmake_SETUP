cmake_minimum_required(VERSION 3.23)
project(PROJECT_NAME)

set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)

find_package(SDL2 REQUIRED)
find_package(SDL2_image REQUIRED)

include_directories(${SDL2_INCLUDE_DIR})
include_directories(${SDL2_IMAGE_INCLUDE_DIRS})

set(CMAKE_CXX_STANDARD 14)

add_executable(PROJECT_NAME main.cpp)
target_link_libraries(PROJECT_NAME ${SDL2_LIBRARY} -lmingw32 -lSDL2main -lSDL2 -lSDL2_Image -mwindows)

#PROJECT_NAME means your project's name :))
#Need to add find_package, include_directories lines for every other SDL2 sublibrary you add + target in target_link_libraries().
