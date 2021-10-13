cmake_minimum_required(VERSION 3.14...3.18)

project(MyProject
  VERSION
    1.0
  DESCRIPTION
    "Very nice project"
  LANGUAGES
    CXX
)

add_library(simple_lib ./src/simple_lib.cpp ./src/simple_lib.hpp)

target_include_directories(simple_lib PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}"/src/)
# Adding definitions
target_compile_definitions(simple_lib PUBLIC MYLIB_PUBLIC)
target_compile_definitions(simple_lib PRIVATE MYLIB_PRIVATE)

# Require a C++ feature (here: at least C++11)
target_compile_features(simple_lib PUBLIC cxx_std_11)

# Now add the executable
add_executable(simple_example ./src/simple_example.cpp)

# Adding the all-important link to simple-lib
target_link_libraries(simple_example PUBLIC simple_lib)
