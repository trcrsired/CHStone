cmake_minimum_required(VERSION 3.15)

project(chstonec)

set(CMAKE_CXX_STANDARD 26)

if(FAST_IO_DIR)
include_directories(${FAST_IO_DIR}/include)
endif()

add_executable(adpcm adpcm/adpcm.cc)
