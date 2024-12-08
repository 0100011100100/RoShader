cmake_minimum_required(VERSION 3.10)
project(ShaderApp)

find_package(OpenGL REQUIRED)
find_package(GLFW3 REQUIRED)
find_package(GLEW REQUIRED)

include_directories(${OPENGL_INCLUDE_DIRS})
include_directories(${GLFW3_INCLUDE_DIRS})
include_directories(${GLEW_INCLUDE_DIRS})

add_executable(shader-app main.cpp)
target_link_libraries(shader-app ${OPENGL_LIBRARIES} ${GLFW3_LIBRARIES} ${GLEW_LIBRARIES})
