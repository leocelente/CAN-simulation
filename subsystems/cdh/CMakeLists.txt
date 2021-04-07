cmake_minimum_required(VERSION 3.10)
set(SUBSYSTEM "cdh")

add_executable(${SUBSYSTEM} ${CMAKE_CURRENT_LIST_DIR}/${SUBSYSTEM}.c)
target_link_libraries(${SUBSYSTEM} PRIVATE can)
target_compile_options(${SUBSYSTEM} PRIVATE -pthread)
target_link_options(${SUBSYSTEM} PRIVATE -pthread)

target_include_directories(${SUBSYSTEM} PRIVATE ${can_INCLUDE_DIR})

unset(SUBSYSTEM)
