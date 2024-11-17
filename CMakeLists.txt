cmake_minimum_required(VERSION 3.13)

# Project name and version
project(simple VERSION 1.0)

# Set C++ standard (optional, adjust as needed)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add the executable
add_executable(simp source/main.cpp)  # Replace main.cpp with your source file(s)

# Find and link GLFW
find_package(glfw3 REQUIRED)
target_link_libraries(simp PRIVATE glfw)

# linking with glad
target_link_libraries(simp PRIVATE glad)

# Find and link OpenGL
find_package(OpenGL REQUIRED)
target_link_libraries(simp PRIVATE OpenGL::GL)

nx_create_nro(simp)
