cmake_minimum_required(VERSION 3.24)
project(
        cmake_template
        LANGUAGES CXX
        VERSION 1.0.0
        DESCRIPTION "Template project for code implemented in C++."
)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(cmake_template main.cpp)
add_subdirectory(template_dir)

cmake_policy(SET CMP0054 NEW)
cmake_policy(SET CMP0057 NEW)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
