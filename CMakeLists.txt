cmake_minimum_required(VERSION 3.15)

project(chstonec)

set(CMAKE_CXX_STANDARD 26)

if(FAST_IO_DIR)
include_directories(${FAST_IO_DIR}/include)
endif()

if(CMAKE_SYSTEM_NAME STREQUAL "Windows" OR CMAKE_SYSTEM_NAME STREQUAL "Cygwin" OR CMAKE_SYSTEM_NAME STREQUAL "Msys")
link_libraries(ntdll)
endif()

add_executable(adpcm adpcm/adpcm.cc)
add_executable(aes aes/aes.cc)
add_executable(blowfish blowfish/bf.cc)
add_executable(dfadd dfadd/dfadd.cc)
add_executable(dfdiv dfdiv/dfdiv.cc)
add_executable(dfmul dfmul/dfmul.cc)
add_executable(dfsin dfsin/dfsin.cc)
add_executable(gsm gsm/gsm.cc)
add_executable(jpeg jpeg/main.cc)
add_executable(mips mips/mips.cc)
add_executable(motion motion/mpeg2.cc)
add_executable(sha sha/sha_driver.cc)