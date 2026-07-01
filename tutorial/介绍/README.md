### 战队基本情况介绍

### 机器人和软件的基本介绍
##### 硬件和软件的范围

##### 软件的架构
- 为什么使用上位机和下位机?
上位机面向程序员,下位机面向机器

##### 下位机
- 本质是什么
大量外设+CPU即有大量外设的代码执行器
- 什么是 CPU MCU 外设 芯片chip 板board
在stm32中MCU和chip基本等价
- 外设的分类
    - 片上外设
    - 片外外设
    - 板载外设
    - 外部外设
- 怎么使用
通过编写代码,控制外设,进而驱动外接设备

### 确认学习方式

### stm32 环境配置
- 教程
https://www.bilibili.com/video/BV1ren2zMEaS/?share_source=copy_web&vd_source=a80a0f20d4adc8210a2b7995021041d6
https://www.baud-dance.com/docs/stm32/CubeMX/install/
- CubeMX 配置stm32的芯片 https://www.st.com
- F1和F4的芯片支持包 提供对应的hal库和其他支持
- CLion
- 编译工具链
- st-link驱动