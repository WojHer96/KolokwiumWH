cmake_minimum_required(VERSION 3.0)
project(test)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

include_directories(include)

file(GLOB SOURCES "src/*.cpp")

add_executable(myProgram.exe ${SOURCES})
add_library(Library SHARED ${SOURCES})
install(TARGETS Library DESTINATION ${CMAKE_BINARY_DIR}/lib)
