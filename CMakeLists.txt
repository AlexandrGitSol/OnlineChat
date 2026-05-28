cmake_minimum_required(VERSION 3.5)
project(OnlineChat)

set(SN "${PROJECT_NAME}server")
set(CN "${PROJECT_NAME}client")

add_executable(${CN} client/client.cpp)
target_include_directories(${CN} PRIVATE libs/asio-1.36.0/include)

add_executable(${SN} server/server.cpp)
target_include_directories(${SN} PRIVATE libs/asio-1.36.0/include)