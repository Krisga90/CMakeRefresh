cmake_minimum_required(VERSION 3.22)

project(
    CppProjectTemplate 
    VERSION 1.0.0 
    LANGUAGES C CXX)

#inside cmake variables
set(CMAKE_CXX_STANDARD          17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS        OFF)

# set variables used in CMakeLists.txt in this and all children files
set(LIBRARY_NAME Library)
set(EXECUTABLE_NAME Exec)

option(COMPILE_EXECUTABLE "Whether to compile the executable" ON)

add_subdirectory(src)
add_subdirectory(configured)
if(COMPILE_EXECUTABLE)
    add_subdirectory(app)
endif()
