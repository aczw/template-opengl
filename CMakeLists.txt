cmake_minimum_required(VERSION 3.28)
project(template_opengl)

set(CMAKE_CXX_STANDARD 17)

add_executable(${PROJECT_NAME} src/main.cpp)

# Statically links libstdc++-6.dll so that we can launch the .exe by itself (e.g. through RenderDoc)
# target_link_options(${PROJECT_NAME} PUBLIC -static)

add_subdirectory(lib/glad)
add_subdirectory(lib/glfw)
add_subdirectory(lib/glm/glm)

target_include_directories(${PROJECT_NAME} PRIVATE lib/glm)
target_link_libraries(${PROJECT_NAME} glad glfw)