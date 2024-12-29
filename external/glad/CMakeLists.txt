# Create GLAD library
add_library(glad 
    src/glad.c
)

# Set include directories
target_include_directories(glad
    PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
)

# If you're on a Unix-like system, you might need to link against dl
if(UNIX)
    target_link_libraries(glad PUBLIC dl)
endif()
