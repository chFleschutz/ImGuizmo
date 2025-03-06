cmake_minimum_required(VERSION 3.28)

project(imguizmo)

set(CMAKE_CXX_STANDARD 20)

add_library(imguizmo)

target_link_libraries(imguizmo 
    PUBLIC 
        imgui
)

target_include_directories(imguizmo 
    PUBLIC
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
)

target_sources(imguizmo PRIVATE
    ImCurveEdit.cpp
    ImGradient.cpp
    ImGuizmo.cpp
    ImSequencer.cpp
)
