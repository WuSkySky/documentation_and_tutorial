#### CMakeList添加源文件和头文件的方法
在```CMakeList.txt```中添加
```
# Add sources to executable
target_sources(${CMAKE_PROJECT_NAME} PRIVATE
    # Add user sources here
    源文件路径
)
```
和
```
# Add include paths
target_include_directories(${CMAKE_PROJECT_NAME} PRIVATE
    # Add user defined include paths
    头文件的文件夹路径
)
```