cmake_minimum_required(VERSION 3.3)

project(BasicProject CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)


# Link this 'library' to use the warnings specified in CompilerWarnings.cmake
add_library(project_warnings INTERFACE)
# Compiler warnings
include(cmake/CompilerWarnings.cmake)
set_project_warnings(project_warnings)

# Static analyzers options
include(cmake/StaticAnalyzers.cmake)

include(cmake/Conan.cmake)
run_conan()

# Test code
enable_testing()
add_subdirectory(tests)

# Main code
add_subdirectory(src)
