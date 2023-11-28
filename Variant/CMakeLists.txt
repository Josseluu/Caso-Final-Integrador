cmake_minimum_required(VERSION 3.12)
project(MiProyecto)

set(CMAKE_CXX_STANDARD 11)


add_library(jsonlib
        src/jsonlib.cpp
)

target_include_directories(jsonlib
        PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)



add_executable(MiPrograma main.cpp)


target_link_libraries(MiPrograma PRIVATE jsonlib)
