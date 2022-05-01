cmake_minimum_required(VERSION 3.22)
project(Test)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
set(SOURCE_FILES src/main.cpp Depends/Sources/glad/glad.c)

include_directories(${PROJECT_SOURCE_DIR}/Depends/Include)
link_directories(${PROJECT_SOURCE_DIR}/Depends/Libraries/GLFW)

add_executable(Test ${SOURCE_FILES})

target_link_libraries(Test glfw3 opengl32)