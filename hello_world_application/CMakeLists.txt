cmake_minimum_required(VERSION 3.4)
project(hello_world)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib ${CMAKE_CURRENT_BINARY_DIR}/formatter_ex_lib)

# Создаем исполняемый файл
add_executable(hello_world hello_world.cpp)
target_link_libraries(hello_world formatter_ex)
