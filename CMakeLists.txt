cmake_minimum_required(VERSION 3.0)
project(MySQLConnectionPool)

# 设置C++标准
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# 如果MySQL Connector/C++安装在非标准路径，需要指定
# include_directories(/path/to/mysql-connector-cpp/include)
# link_directories(/path/to/mysql-connector-cpp/lib)

# 查找MySQL Connector/C++库
# find_package(MySQLConnectorCPP REQUIRED)

# 添加可执行文件
add_executable(${PROJECT_NAME} MySqlconnpool.cpp)

# 链接MySQL Connector/C++库
target_link_libraries(${PROJECT_NAME} mysqlcppconn)
