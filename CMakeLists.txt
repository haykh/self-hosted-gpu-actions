cmake_minimum_required(VERSION 3.16)

set(PROJECT_NAME main-cpu)

project(${PROJECT_NAME}
  LANGUAGES CXX C
)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# ---------------------------------- Tests --------------------------------- #
set(BUILD_TESTING OFF CACHE BOOL "Build tests")

# ------------------------------- Main source ------------------------------ #
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/src src)
