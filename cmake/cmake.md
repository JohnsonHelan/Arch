# Cmake
## Purpose
Cmake工具用来根据快速构建（生成）对应平台（工具链）的makefile.  
PS: makefile用来组织和管理代码  
  
  
快速构建项目（对应的工程文件和makefile)  
支持跨平台  
支持交叉编译  
可生成动态库，静态库  

## Roadmap
The roadmap can be found by the following web site:
```
https://github.com/SFUMECJF/cmake-examples-Chinese //改连接为下面连接的中文翻译版本
https://github.com/ttroy50/cmake-examples          //大量的例子

https://www.kitware.eu/cmake-training/             //systematic knowlege and can get a overview regarding which component you shoud study

```

## To Do List
To study systematiclly general or baisc knowlege regarding cmake.

## VAR
CMAKE_CURRENT_SOURCE_DIR: Cmakelists.txt 所在目录

## key word
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

## the arg of executting cmake
The arg -G used to point the type of generator, e.g if we would like to generate a prject compiled by MinGW tool chain, we can use the following command:
```
#cmake -G "MinGW Makefiles" ..
```

