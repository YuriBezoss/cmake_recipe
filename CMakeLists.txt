cmake_minimum_required(VERSION 3.14...3.18)

project(MyProject
  VERSION
    1.0
  DESCRIPTION
    "Very nice project"
  LANGUAGES
    CXX
)

add_executable(myexample ./src/Test.cpp)
