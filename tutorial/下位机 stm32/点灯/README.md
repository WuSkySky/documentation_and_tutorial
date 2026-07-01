#### 原理图

#### CubeMX介绍

#### 总是需要的配置
参考documentation/stm32.cd

#### GPIO

#### 项目结构

#### 引脚复用(可以了解)

#### 引脚重映射(可以了解)

#### GPIO的8种模式(可以了解)
参考```F1GPIO结构.jpg``` ```F4GPIO结构.jpg```
##### 8种模式
- 输入模式
    - 上拉输入 Pull-up input
    - 下拉输入 Pull-down input
    - 浮空输入 Floating input
    - 模拟输入 Analog input
- 输出模式
    - 推挽输出 Push-pull output
    - 开漏输出 Open-drain output
    - 复用推挽输出 Alternate function push-pull
    - 复用开漏输出 Alternate function open-drain

##### 引脚上下拉的含义
- 引脚上拉指引脚在不电平输出时通过上拉电阻将电平提升到高电平
- 引脚下拉指引脚在不电平输出时通过下拉电阻将电平降低到低电平
- 意义时在引脚不输出电平时,保证引脚电平可控与稳定
- 若不进行引脚上下拉,引脚不输出电平时,引脚处于浮空状态,引脚电平受环境影响(如静电),不可控,不稳定

##### 推挽输出和开漏输出的区别
- 推挽输出
    - 可以输出高电平或低电平
    - 对应PMOS激活NMOS不激活 PMOS不激活NMOS激活
    - 特点: 对高电平和低电平有驱动能力
- 开漏输出
    - 可以配置为输出高电平和高阻态
    - 对应PMOS不激活NMOS激活和PMOS不激活NMOS不激活
    - 特点: 只对低电平有驱动能力,对高电平没有驱动能力,高阻态时引脚电平取决于外部上下拉

##### 为什么输入没有复用
因为输入模式下,引脚电平信息可同时被CPU读取和被其他外设读取.而输出模式下,要保证引脚输出的控制源只有一个,引脚输出不能被CPU和被其他外设同时控制,所以输入模式不用配置复用,而输出模式需配置复用
#### QNA
- 点灯失败
    注意有些参数不能想当然,GPIO_PIN_x,不能直接填引脚编号对应的数字,而应该查看函数文档
    ```C
    HAL_GPIO_WritePin(GPIOC, GPIO_PIN_13, GPIO_PIN_SET); // 正确的
    HAL_GPIO_WritePin(GPIOC, 13, GPIO_PIN_SET); // 错误的
    ```
    函数文档写了怎么传参
    ```C
    /**
    * @param  GPIO_Pin: specifies the port bit to be written.
    *          This parameter can be one of GPIO_PIN_x where x can be (0..15).
    */
    ```
