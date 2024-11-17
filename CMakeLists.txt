cmake_minimum_required(VERSION 3.20)

project(gui VERSION 1.0
            DESCRIPTION "GUI librairie for Indoor Weather Station"
            LANGUAGES CXX C)


# ADD .cpp & .h
set(SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)

set(SRC
    ${SRC_DIR}/gui.cpp
)


# LINK
add_library(gui STATIC ${SRC})
target_include_directories(gui PUBLIC ${SRC_DIR})
target_link_libraries(gui PUBLIC lvgl)
