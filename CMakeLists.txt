cmake_minimum_required(VERSION 3.10.0)
project(OpenGL VERSION 0.1.0 LANGUAGES C CXX)

# Ensure CMake is correctly installed and accessible
# You can specify the CMake executable path if needed:
# set(CMAKE_COMMAND /path/to/cmake)

# Set the C++ compiler to /usr/bin/clang++
#set(CMAKE_CXX_COMPILER /usr/bin/clang++)

add_executable(OpenGL main.cpp)

include(CTest)
enable_testing()

