file(GLOB_RECURSE SRC_FILES ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)

add_executable(${PROJECT_NAME}-cpu main.cpp)
target_include_directories(${PROJECT_NAME}-cpu PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})

configure_file(${CMAKE_CURRENT_SOURCE_DIR}/warandpeace.txt ${CMAKE_BINARY_DIR}/warandpeace.txt COPYONLY)
add_executable(${PROJECT_NAME}-gpu main.cu)
target_include_directories(${PROJECT_NAME}-gpu PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})
