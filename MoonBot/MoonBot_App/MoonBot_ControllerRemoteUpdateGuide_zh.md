MoonBot遥控器固件升级向导
======================

使用MoonBot手机编程需要在主控内烧录

## 通过烧录HEX文件进行升级

- 1.下载[MoonBot 主控遥控器固件](https://github.com/mu-opensource/MoonBot_RemoteController/releases/latest)(.hex 文件)
- 2.烧录 .hex 固件
    - Windows
        ```
        1）下载 Arduino Hex 烧录工具
        2）选择 MoonBot 端口，硬件选择 `Genuino ATmega1280`
        3）点击下载，等待下载完成
        ```

## 通过Arduino IDE编译Arduino源码进行升级

- 1.下载[MoonBot 主控遥控器源码](https://github.com/mu-opensource/MoonBot_RemoteController/releases/latest)(Source.zip 文件)
- 2.下载[MuVisionSensorIII Arduino 库](https://github.com/mu-opensource/MuVisionSensorIII/releases/latest)(Source.zip 文件)
- 3.下载[MoonBot Arduino 库](https://github.com/mu-opensource/MoonBot/releases/latest)(Source.zip 文件)
- 4.打开 Arduino IDE，点击`项目->加载库->添加.ZIP库`，选择第1,2步下载的.zip文件文件
- 5.点击确定，完成源码的加载
- 6.点击`项目->加载库->管理库`，打开`库管理器`
- 7.搜索库`AsyncDelay`，若没有安装则安装相关库，若库有更新，则进行更新
- 8.按照第三步的安装方法安装库`SoftwareWire` `Adafruit_NeoPixel` `Servo`，保证相关库安装到最新版
- 9.关闭Arduino，完成外部依赖库安装
- 10.点击`文件->示例->MoonBotRemote->RemoteWithDemo`，打开源码
- 11.点击`工具->开发板`选择`Arduino/Genuino Mega or Mega 2569`
- 12.点击`工具->处理器`选择`ATmega1280`
- 13.连接 MoonBot 主控至电脑，点击`工具->端口`，选择对应的 MoonBot 端口
- 14.点击下载按钮，等待下载完成

## 测试

- 1.开机重启后按下主控上按钮A，靠近A键LED亮青色灯光并发出提示音
- 2.开机重启后按下主控上按钮B，靠近B键LED亮绿色灯光并发出提示音
