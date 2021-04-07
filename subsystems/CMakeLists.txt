cmake_minimum_required(VERSION 3.10)

set(SUBSYSTEM_LIST acs;ads;cdh;cth;eps)

foreach(SUBSYSTEM IN LISTS SUBSYSTEM_LIST)
    include(${CMAKE_CURRENT_LIST_DIR}/${SUBSYSTEM}/CMakeLists.txt )
endforeach()

