add_executable(MAIN main.cpp)
target_link_libraries(MAIN PRIVATE 
	project_warnings 
	CONAN_PKG::fmt
	CONAN_PKG::spdlog)
