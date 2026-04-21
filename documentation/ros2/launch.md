##### 最小实现
- 框架
```py
from launch import LaunchDescription

def generate_launch_description():
    ld = LaunchDescription()

    return ld
```

- 添加node
```py
node = Node(
    package='PKG_NAMW',
    executable='EXE_NAME',
    name='NODE_NAME',
    remappings=[
        (FROM, TO)
    ]
)
ld.add_action(node)
```

- 添加launch
```py
launch_file = os.path.join(
    get_package_share_directory('PKG_NAME'), 
    'launch',                      
    'LAUNCH_NAME'                
)

launch = IncludeLaunchDescription(
    PythonLaunchDescriptionSource(launch_file)
)

ld.add_action(launch)
```

- 添加命令行命令
```py
cmd = ExecuteProcess(
    cmd=[CMD1, CMD2],
    name=NAME,
)
ld.add_action(find_can_cmd)
```

##### 命令
使用launch启动
```bash
ros2 launch 功能包名 xxx.py
```
