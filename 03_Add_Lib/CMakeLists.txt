cmake_minimum_required(VERSION 2.6)
file(GLOB CPP_FILES *.cpp *.c)
file(GLOB HEADER_FILES *.h *.hpp)
add_library(LibTest_Dynamic SHARED ${CPP_FILES} ${HEADER_FILES})
add_library(LibTest_Static STATIC ${CPP_FILES} ${HEADER_FILES})
set_target_properties(LibTest_Dynamic PROPERTIES OUTPUT_NAME "LibTest")
set_target_properties(LibTest_Static PROPERTIES OUTPUT_NAME "LibTest")