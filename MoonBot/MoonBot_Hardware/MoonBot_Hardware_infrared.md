# 红外模块

## 简介

![](./images/render_infrared.png)

红外模块含有两个红外开关，可检测一定距离内的障碍。

模块有远近两种模式，用于巡线或避障等不同安装方式。

## 参数

尺寸：34 x 32 x 12 mm

红外形式：2路反射式红外开关

检测距离：

近距离模式约10mm

远距离模式约110mm

### 接口图

![](./images/pinout_infrared.png)

## 使用示例

程序介绍：将红外模块连接至主控口，循环检测红外传感器两路状态。
当红外传感器两路同时被检测到有障碍时，主控LED两个灯亮红色，检测到一路障碍时，主控LED亮程序中对应的红灯。

![](./images/Mixly_example_infrared.png)

实物图：

![](./images/photo_infrared.png)
