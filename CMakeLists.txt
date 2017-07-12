cmake_minimum_required(VERSION 2.8)
project(leveldb_example)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/Modules/")

find_package(Threads REQUIRED)
find_package(Snappy REQUIRED)
find_package(LevelDB REQUIRED)

add_executable(sample sample.cpp)
target_link_libraries(sample ${LEVELDB_LIBS})
target_link_libraries(sample ${SNAPPY_LIBS})
target_link_libraries(sample ${CMAKE_THREAD_LIBS_INIT})

