cmake_minimum_required(VERSION 3.16)
project(xx3dsfml)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
option(BUILD_SHARED_LIBS "Build shared libraries" OFF)

include(FetchContent)
FetchContent_Declare(SFML
    GIT_REPOSITORY https://github.com/SFML/SFML.git
    GIT_TAG 2.6.1)
FetchContent_MakeAvailable(SFML)

add_executable( xx3dsfml 
                xx3dsfml.cpp)
target_link_libraries(xx3dsfml PRIVATE sfml-graphics sfml-audio ftd3xx-static)
target_compile_features(xx3dsfml PRIVATE cxx_std_17)

install(TARGETS xx3dsfml)

