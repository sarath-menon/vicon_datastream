cmake_minimum_required(VERSION 3.0.0)
project(vicon_test VERSION 0.1.0)
set(CMAKE_CXX_STANDARD 17)

# include folders src,include
# include_directories(include src)

add_executable(${PROJECT_NAME} 
# src/ViconDataStreamSDK_CPPTest.cpp
# src/vicon_simple.cpp
 src/vicon_simple_clean.cpp
)

target_include_directories(${PROJECT_NAME}  PUBLIC include)
target_include_directories(${PROJECT_NAME}  PRIVATE src)
target_include_directories(${PROJECT_NAME}  PRIVATE lib)


target_link_libraries(${PROJECT_NAME} "${CMAKE_CURRENT_LIST_DIR}/lib/libViconDataStreamSDK_CPP.dylib")

