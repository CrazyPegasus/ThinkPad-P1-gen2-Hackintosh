# ThinkPad-P1-gen2-Hackintosh
# 中文版
# 联想ThinkPad P1&X1E GEN2上的macOS

此存储库包含10.14,10.15在Lenovo ThinkPad P1&X1E gen2上运行macOS（目前为Mojave，Catalina ）的示例配置
--------------------------------------------------------------------------
#相关设置

* SD卡读卡器走usb3.0通道，需要打开此USB端口即可使用，无此设备无法精确定制usb补丁。

* Thunderbolt 3【BIOS里需要设置“Thunderbolt BIOS Assist”：Disable，“Security level” :No Security(允许自动连接 Thunderbolt 设备)。这样即可使前端类型USB type-c端口在macOS中工作，连接扩展坞正常，雷电3设备工作正常（前提：冷启动前插入可以热插拔）】

* 机器自带独立的HDMI走独显，不正常，独显已屏蔽。

* 键盘Synaptics触摸板（PS / 2）使用ApplePS2SmartTouchPad.kext，EMlyDinEsH的v4.7b5，支持多点触控手势。
* 睡眠和唤醒正常

已禁用的设备和BIOS设置
-----------
* WWAN（无模块）
* TrackPad Synaptics指纹识别器无法驱动
* BIOS里设置Thunderbolt BIOS Assist为Disable(Enable雷电由BIOS控制决定，Disabled雷电由操作系统控制决定)，“Security level” :No Security(允许自动连接 Thunderbolt 设备和TYPEC)。
* BIOS里设置usb项Always on USB为enable，下面子项Charge in Battery Mode设置为enable（这样雷电口type-c就可以热插拔type-c外设）
* 关闭安全启动
