add_executable(MAIN main.cpp)
target_link_libraries(MAIN project_warnings CONAN_PKG::spdlog)

