cmake_minimum_required(VERSION 3.5)
project(myproject)

# Build foo library
add_library(foo STATIC foo.cpp)

# Add include directory for foo.hpp
target_include_directories(foo PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

# Build main executable
add_executable(main main.cpp)

# Link main executable with foo library
target_link_libraries(main PUBLIC foo)