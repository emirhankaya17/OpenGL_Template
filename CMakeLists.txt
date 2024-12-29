cmake_minimum_required(VERSION 3.10)
project(OpenGLTemplate)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Find required packages
find_package(OpenGL REQUIRED)

# Add external dependencies
add_subdirectory(external/glfw-3.4)
add_subdirectory(external/glad)
# Add source files
add_executable(${PROJECT_NAME}
    src/main.cpp
)

# Link libraries
target_link_libraries(${PROJECT_NAME}
    PRIVATE
    OpenGL::GL
    glfw
    glad
)

# Include directories
target_include_directories(${PROJECT_NAME}
    PRIVATE
    ${CMAKE_SOURCE_DIR}/external/glfw-3.4/include
    ${CMAKE_SOURCE_DIR}/external/glad/include
)

# Copy shaders to build directory
file(COPY ${CMAKE_SOURCE_DIR}/shaders DESTINATION ${CMAKE_BINARY_DIR}) 