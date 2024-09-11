cmake_minimum_required(VERSION 3.22)

project(UserLib)

# 创建一个静态库，名为UserLib
add_library(UserLib STATIC)

# 设置库的包含目录(头文件)
target_include_directories(UserLib PUBLIC 
    ./include
)

# 设置库的源文件
target_sources(UserLib PRIVATE 
    ./src/userlib.c
)

# 设置库需要链接的外部库（PUBLIC使得链接具有自动传播的特性）
target_link_libraries(UserLib PUBLIC stm32cubemx)