cmake_minimum_required(VERSION 2.8)
project(PrMatrix)
set(LIBNAME "prmatrix")
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/..)
file(GLOB sources ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)
file(GLOB headers ${CMAKE_CURRENT_SOURCE_DIR}/*.h)

add_library(${LIBNAME} SHARED ${sources})
install(TARGETS ${LIBNAME} DESTINATION lib COMPONENT library)
install(FILES ${headers} DESTINATION include/${PROJECT_NAME})
