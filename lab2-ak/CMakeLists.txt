cmake_minimum_required(VERSION 3.10)
set(CMAKE_CXX_STANDARD 14)

project(lab2-ak)

add_library(Calculator
	src/Calculator.h
	src/Calculator.cpp
)


target_include_directories(
	Calculator
	PUBLIC
		"src"
)

add_executable(program
  src/main.cpp
)

target_link_libraries(program Calculator)