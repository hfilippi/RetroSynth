cmake_minimum_required(VERSION 3.25)

project(RetroSynth
    VERSION 0.1.0
    DESCRIPTION "Retro-inspired hardware synthesizer platform"
    LANGUAGES CXX
)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_executable(retrosynth
    src/main.cpp
)

target_compile_options(retrosynth
    PRIVATE
        -Wall
        -Wextra
        -Wpedantic
)
