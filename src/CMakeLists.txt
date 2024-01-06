file(GLOB APP_SRC ./*.c)
add_executable(${PROJECT_NAME} ${APP_SRC})
target_link_libraries(${PROJECT_NAME} PRIVATE lvgl lvgl::drivers lvgl::demos)