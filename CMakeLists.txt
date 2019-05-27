cmake_minimum_required(VERSION 3.7)

project(sphinx-stats)

find_library(MYSQL_LIB libmysqlclient.a)
message(STATUS "Found libmysqlclient library: ${MYSQL_LIB}")

add_executable(
    sphinx-stats
    "src/main.cpp"
)

target_link_libraries(sphinx-stats
    ${MYSQL_LIB}
)
