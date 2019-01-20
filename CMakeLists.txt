cmake_minimum_required(VERSION 3.0)

set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_FLAGS "-std=c++14 -O3 -fopenmp")
set(CMAKE_LDFLAGS "-fopenmp")

project(stockast)

add_executable(
	stockast
	stockast.cpp
)
