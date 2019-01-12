#最低版本
cmake_minimum_required(VERSION 3.11)

#项目信息
project(demo1)

#生成目标
#add_executable(demo2 1.cpp main.cpp)

# 查找当前目录下的所有源文件
# 并将名称保存到 DIR_SRCS 变量
aux_source_directory(. DIR_SRCS)
# 指定生成目标
#add_executable(Demo ${DIR_SRCS})

#添加子目录
add_subdirectory(complex)

add_executable(demo ${DIR_SRCS})

target_link_libraries(demo complexclass)