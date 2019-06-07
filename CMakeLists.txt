cmake_minimum_required(VERSION 3.14)
project(TGUITest)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

find_package(SFML 2 REQUIRED system window graphics audio)
find_package(TGUI REQUIRED)
set(EXECUTABLE_NAME "example")
include_directories(${SFML_INCLUDE_DIR})
add_executable(${EXECUTABLE_NAME} main.cpp)
target_link_libraries(${EXECUTABLE_NAME} ${CMAKE_THREAD_LIBS_INIT} ${CMAKE_DL_LIBS} sfml-graphics tgui)
