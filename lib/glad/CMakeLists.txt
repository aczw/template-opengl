# modeled after https://github.com/Dav1dde/glad/issues/186#issuecomment-436713397

cmake_minimum_required(VERSION 3.28)
project(glad)

add_library(${PROJECT_NAME} include/glad/glad.h src/glad.c)
target_include_directories(${PROJECT_NAME} PUBLIC include/)