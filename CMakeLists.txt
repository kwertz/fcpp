cmake_minimum_required(VERSION 2.8)
project(fcpp)

if (MSVC)
	add_definitions(-D_CRT_SECURE_NO_WARNINGS)
endif()

add_library(fcpp STATIC cpp1.c cpp2.c cpp3.c cpp4.c cpp5.c cpp6.c)

add_executable(usecpp usecpp.c)
target_link_libraries(usecpp fcpp)
