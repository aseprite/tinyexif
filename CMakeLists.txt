cmake_minimum_required(VERSION 3.1)

project(tinyexif)
include(GNUInstallDirs)

find_package(tinyxml2 REQUIRED)

#CMAKE_BUILD_TOOL

################################
# set lib version here

set(GENERIC_LIB_VERSION "1.0.1")
set(GENERIC_LIB_SOVERSION "1")

################################
# Add definitions

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -DDEBUG")

add_library(tinyexif STATIC
  tinyexif.cpp
  tinyexif.h)

target_link_libraries(tinyexif)