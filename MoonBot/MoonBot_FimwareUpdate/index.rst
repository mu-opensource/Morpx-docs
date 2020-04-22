.. morpx documentation master file, created by
   sphinx-quickstart on Fri Jul 19 17:00:19 2019.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

MoonBot Kit 固件升级向导
========================

本文档旨在指导用户更新 MoonBot Kit :doc:`../MoonBot_Hardware/MoonBot_Hardware_controller`
及 :doc:`../MoonBot_Hardware/MoonBot_Hardware_MUVS3` 的相关固件。

查看视频教程：`固件更新视频教程 <https://v.qq.com/x/page/x095408v8a0.html>`_

准备工作
--------

硬件：

- MoonBot 开发者套件
- PC（Windows）

软件：

- `Arduino官方IDE <https://www.arduino.cc/en/Main/Software?setlang=cn>`_
- MoonBot Arduino 库
- `MU视觉传感器固件更新软件 <http://mai.morpx.com/images/page201904/flash_download_tools_v3.6.5.rar>`_
- `MU(for MoonBot) 最新版固件(.bin文件) <https://github.com/mu-opensource/MoonBot_RemoteController/releases/latest>`_

详细操作步骤
------------

步骤一：更新 MoonBot Kit 主控固件
+++++++++++++++++++++++++++++++++

主控固件升级可参考：:doc:`../MoonBot_App/MoonBot_ControllerRemoteUpdateGuide`

步骤二：更新 MU 视觉传感器3固件
++++++++++++++++++++++++++++++++++++

1.将 :doc:`../MoonBot_Hardware/MoonBot_Hardware_MUVS3` 连接至 MoonBot Kit
:doc:`../MoonBot_Hardware/MoonBot_Hardware_controller` 的端口P9，并将主控连接至电脑

2.按住 :doc:`../MoonBot_Hardware/MoonBot_Hardware_MUVS3`
左侧的 Function 键,再短按一次右侧 Reset 键重启,即可进入烧录模式，此时可以松开 Function 键

3.双击打开MU视觉传感器固件更新软件 ``flash_download_tools_vx.x.x.exe``

4.点击选择 ``ESP32 DownloadTool``

    .. image:: images/moonbot_upgrade_flash_loader.png

5.设置参数

    .. image:: images/moonbot_upgrade_setup.png

.. note::

    - SPI SPEED:40MHz
    - SPI MODE:DIO
    - FLASH SIZE:32Mbit
    - BAUD:115200
    - COM：连接模块的对应 COM 端口,可以通过 Windows 设备管理器查看主控模块所连接的 COM 端口

        .. image:: images/moonbot_upgrade_find_com.png

6.点击 ``...`` 按钮，选择所要更新的固件文件路径，并在前面方框内勾选 ``√``

7.在 ``@`` 符号后面输入地址：``0x10000``

.. Attention::

    **不要输入错误地址，也不要按ERASE擦除芯片所有内容，否则可能导致传感器芯片内置固件损坏。如有发生，请联系摩图科技售后技术支持进行解决**

    电话：(0571)8195 8588

    邮箱：support@morpx.com

8.点击左下角 ``START`` 按钮开始，电脑端显示“等待上电同步”，此时 **连续点击**
MoonBot Kit :doc:`../MoonBot_Hardware/MoonBot_Hardware_controller`
上按钮B直至软件开始烧录，烧录时主控右侧LED绿灯常亮

9.等待完成,当窗口最下方的绿色进度条至最右端，并显示 ``FINISH 完成`` 字样，则下载完成
