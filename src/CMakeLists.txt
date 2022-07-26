# Set include directories
include_directories(../include/)

# Set variables values, that will be used to aggregate source and header files
set(Example_Headers ../include/example/example.hpp)
set(Example_Sources example/example.cpp)

# Set target to build library.
add_library(Example_lib ${Example_Sources} ${Example_Headers})