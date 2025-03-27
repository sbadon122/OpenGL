cmake_minimum_required(VERSION 3.10.0)
project(OpenGLLearning VERSION 0.1.0 LANGUAGES C CXX)

# Ensure CMake is correctly installed and accessible
# You can specify the CMake executable path if needed:
# set(CMAKE_COMMAND /path/to/cmake)

# Set the C++ compiler to /usr/bin/clang++
#set(CMAKE_CXX_COMPILER /usr/bin/clang++)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)

add_subdirectory(glfw)
include_directories(glad/include)
find_package(OpenGL REQUIRED)


add_executable(OpenGLLearning 
                    main.cpp
                    glad/src/glad.c
                    glad/include/glad/glad.h
                    glad/include/KHR/khrplatform.h
                    )

target_link_libraries(OpenGLLearning glfw)
target_link_libraries(OpenGLLearning OpenGL::GL)

include(CTest)
enable_testing()

