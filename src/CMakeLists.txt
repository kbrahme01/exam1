cmake_minimum_required(VERSION 3.10.0)
project (main LANGUAGES CXX)
set(CMAKE_SUPPRESS_REGENERATION true)
set(CMAKE_CXX_STANDARD 17)
#IF(${CMAKE_SYSTEM_NAME} MATCHES "Windows")
#SET(CMAKE_INCLUDE_PATH ${CMAKE_INCLUDE_PATH} "C:/Program Files/Boost/boost_1_74_0/boost_1_74_0")
#ELSE()

#SET(CMAKE_INCLUDE_PATH ${CMAKE_INCLUDE_PATH} "/mnt/c/Program Files/Boost/boost_1_74_0/boost_1_74_0")
#ENDIF()
find_package(Boost 1.72.0) 

add_executable(main main.cpp readFA.cpp  )
target_include_directories(main PUBLIC "${PROJECT_SOURCE_DIR}")
include_directories(${Boost_INCLUDE_DIR}) 
#message(${Boost_INCLUDE_DIR})
