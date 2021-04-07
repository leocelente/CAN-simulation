cmake_minimum_required(VERSION 3.0.0)

add_library(can STATIC ${CMAKE_CURRENT_LIST_DIR}/can.c)
target_include_directories(can PUBLIC ${CMAKE_CURRENT_LIST_DIR})

add_custom_target(interface COMMAND echo -E 'sudo ${CMAKE_CURRENT_LIST_DIR}/../scripts/create_interface.sh')
set(can_INCLUDE_DIR ${CMAKE_CURRENT_LIST_DIR})
