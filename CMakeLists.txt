# Set minimum cmake required version
cmake_minimum_required(VERSION 3.22)

# Set project name
project(cppCoding)

# Set c++ version
set(CMAKE_CXX_STANDARD 14)

# Add target executable
add_executable(${CMAKE_PROJECT_NAME}_run src/main.cpp)

# Set include directories
include_directories(include)

# Define where other cmake lists are
add_subdirectory(src)
add_subdirectory(test)

# Add libraries to link, to build executable in the previous line
# Note include "m" to link with the math library
target_link_libraries(${CMAKE_PROJECT_NAME}_run Example_lib)