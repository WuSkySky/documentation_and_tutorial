#### 要做什么
- 推荐下面的顺序进行,有问题可以看看QNA
- 完成了某个功能可以反馈一下进度
- 注意问问题可以随便问我**但是每次反馈进度只能由一个人反馈**

#### CubeMX
1. CubeMX是干什么的(了解)
2. CubeMX怎么使用(简单了解,然后用到什么再对应的配置方法)
3. 在CubeMX配置一个PC13的LED常量,生成代码

#### 编译和烧录
4. 在Clion中编译LED常量的代码
5. 在Clion中烧录LED常量的代码(实现之后可以录视频给我看)

#### 配置GPIO与添加LED闪烁功能
6. 什么是GPIO(了解)
7. 使用延时函数实现LED亮0.5s,灭0.5s
8. 编译烧录(实现之后可以录视频给我看)

#### 添加按钮控制LED功能
9. 使用GPIO外设读取按钮状态
10. 实现按钮按下LED亮,松开LED灭(实现之后可以录视频给我看)
11. 什么是按键抖动,有什么解决方法(了解)
12. 实现按键消抖
13. 实现按按钮一次LED亮,再按一次LED灭,要每一次都能正确响应,也就是功能稳定(实现之后可以录视频给我看)

#### 中断,EXTI与更优雅实现的按钮控制LED功能
14. 什么是中断(了解)
15. 什么是EXTI(了解)
16. 使用中断实现编号13的功能,不过不能阻塞主循环(实现之后可以录视频给我看,以及中断回调函数也可以截图给我看)

#### QNA
##### 遇到问题怎么办
- 问组员
- 用AI帮助你,不过要尽量多了解为什么某一步要这么做
- AI解决不了可以浏览器找找,说不准有惊喜
- 搞不定也可以找我

##### 想要视频教程
- 新手友好
https://space.bilibili.com/6100925?spm_id_from=333.788.upinfo.head.click

##### 环境配置问题
- CubeMX环境配置教程(这个还包含了CubeIDE的教程,但是不推荐使用,只用关心CubeMX的配置) 
https://www.bilibili.com/video/BV1AsZGYtEA2?spm_id_from=333.788.videopod.sections&vd_source=9016c4056f9cb6808524aac0e7946d21
- Clion配置stm32的视频链接
https://www.bilibili.com/video/BV1ren2zMEaS/?spm_id_from=333.337.search-card.all.click&vd_source=9016c4056f9cb6808524aac0e7946d21
- Clion配置常见问题(这个网站还有其他常见问题的解决方案)
https://www.baud-dance.com/docs/stm32/CLion/error
- 无法用Clion下载,可以试试CubeProgrammer https://www.st.com.cn/zh/development-tools/stm32cubeprog.html

##### 开发问题
- 锁芯片了,也就是突然不能下载程序了 https://www.baud-dance.com/docs/stm32/FAQ/CompilationFailed
- 插拔stlink导致无法烧录 **在Clion的调试服务器中关闭持久会话**,可能还要重启一次电脑

