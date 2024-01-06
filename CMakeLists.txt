cmake_minimum_required(VERSION 3.1)

project(lvgl_fb)

include_directories(.)

add_subdirectory(lvgl)
add_subdirectory(lv_drivers)
add_subdirectory(src)
