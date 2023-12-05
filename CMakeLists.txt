cmake_minimum_required(VERSION 3.1)
project(xx3dsfml)

find_package(SFML COMPONENTS graphics audio REQUIRED)

add_executable( xx3dsfml 
                xx3dsfml.cpp)
target_link_libraries(xx3dsfml sfml-graphics sfml-audio ftd3xx)

