# 主控模块

## 简介

![](./images/render_controller.png)

主控模块是机器人的交互核心。

## 参数

尺寸：53 x 53 x 17.6 mm

主控芯片：ATmega1280

接口：4路舵机、2路电机、9路通用输入输出

板载资源：按键、LED指示灯、蜂鸣器、电子罗盘、加速度计

**外设和接口图：**

![](./images/pinout_controller.png)

## 使用示例

**主控LED和按键示例**

程序介绍：该程序是通过主控模块板载的2个可编程按键控制板载的2个RGB彩灯。

循环检测按键A和按键B的状态，当A被按下时LED1亮红色，当按键B被按下时LED2亮绿色，之后关闭LED。

![](./images/Mixly_example_controller_LEDbutton.png)

**主控蜂鸣器示例**