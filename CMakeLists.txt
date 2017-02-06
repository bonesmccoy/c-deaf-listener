cmake_minimum_required(VERSION 3.6)
project(listener)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES
        main.cpp
        utils.c
        utils.h
        include/amqp.h
        include/amqp_framing.h
        include/amqp_tcp_socket.h
        )

add_executable(listener ${SOURCE_FILES})
target_link_libraries(listener ${PROJECT_SOURCE_DIR}/librabbitmq.4.2.0.dylib)
