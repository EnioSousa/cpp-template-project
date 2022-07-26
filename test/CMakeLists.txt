# Set project name
project(Test)

# Add the cmakes from google
add_subdirectory(lib/googletest)

# Set include directories, i.e. include the google stuff
include_directories(lib/googletest/googletest/include)
include_directories(lib/googletest/googlemock/include)

# Set the location of the sources of the tests
set(Sources example/test.cpp)

# Set target for the executable
add_executable(Test_run ${Sources})

# Add the target libraries to link
target_link_libraries(Test_run Example_lib)
target_link_libraries(Test_run gtest gtest_main)
target_link_libraries(Test_run gmock gmock_main)

