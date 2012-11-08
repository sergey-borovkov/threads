set (SOURCES main.cpp)

list (APPEND CMAKE_CXX_FLAGS "-std=c++0x ${CMAKE_CXX_FLAGS} -g -ftest-coverage -fprofile-arcs")

find_package (Threads)

add_executable(threads ${SOURCES})

target_link_libraries(threads ${CMAKE_THREAD_LIBS_INIT})
