# 目录结构
```
D:.
│  Cmakelists.txt
│
├─include
│      hello.h
│
└─src
        hello.cpp
        main.cpp
```


# CmamkeLists.txt
工具链：MinGW  
命令：Cmake -G "MinGW Makefiles" ..  
PS: 采用外部构建的方案，这样做的目的是资料和产出分离

```
#最低CMake版本
cmake_minimum_required (VERSION 3.5)

message (STATUS "CMAKE_CURRENT_SOURCE_DIR: ${CMAKE_CURRENT_SOURCE_DIR}" )


# 工程名
project (HELLO_WORLD)

# 设置变量
set (SRC 
    ${CMAKE_CURRENT_SOURCE_DIR}/src/hello.cpp
    ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp
)

# 指定target和对应的源码
# 引用变量 ${VAR}
add_executable (hello ${SRC})

# 设置本地库变量
set (LOCAL_LIB ${CMAKE_CURRENT_SOURCE_DIR}/include
)

message (STATUS "LOCAL_LIB: ${LOCAL_LIB}" )


# 指定包含的头文件路径
# CMAKE_CURRENT_SOURCE_DIR: Cmakelists.txt 所在目录
target_include_directories ( hello PRIVATE ${LOCAL_LIB}
)

```
