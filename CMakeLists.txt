# https://stackoverflow.com/questions/34418357/cmake-scoping-rules

cmake_minimum_required(VERSION 3.15)
project( fernpedro)

cmake_minimum_required(VERSION 3.15)
project(fernpedro)
#set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_SOURCE_DIR}/cmake)
#set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH})

include(cmake/MyCMake)
add_subdirectory(child)  # add_subdirectory() establish a new scope
message("Parent1: " ${MY_NAME} " " ${YOUR_NAME} " " ${HIS_NAME})
include(cmake/MyCMake2)
message("Parent2: " ${MY_NAME} " " ${YOUR_NAME} " " ${HIS_NAME})