cmake_minimum_required(VERSION 3.28)
project(OpenGL LANGUAGES C CXX)

# glfw
option(GLFW_BUILD_EXAMPLES off)
option(GLFW_BUILD_TESTS off)
option(GLFW_BUILD_DOCS off)
option(GLFW_INSTALL off)
add_subdirectory(libs/glfw)
list(APPEND LIBRARIES glfw)

# glad
add_subdirectory(libs/glad)
list(APPEND LIBRARIES glad)

# glm
add_subdirectory(libs/glm)
list(APPEND LIBRARIES glm::glm)

# main
add_executable(main src/main.cpp)
target_link_libraries(main PRIVATE ${LIBRARIES})
