cmake_minimum_required(VERSION 3.3)
project(helloglfw)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

# Including GLFW
add_subdirectory(glfw)
include_directories(glfw/include)

set(SOURCE_FILES main.cpp)
add_executable(helloglfw ${SOURCE_FILES})

# Linking GLFW
target_link_libraries(helloglfw glfw ${GLFW_LIBRARIES})
