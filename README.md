﻿# wmt_esp8266_study
My ESP8266 / ESP32 study  

## msys  
* search baidupan, msys_ESP8266_NONOS_SDK_v2.2.1_v3.rar  
* msys_ESP8266_NONOS_SDK_v2.2.1_v7_blink_success.rar  

## cygwin  
search baidupan, ESP8266机智云开发板 ESP12F  

## Arduino version flash and sram size:  
* esp8266, NodeMCU 1.0 (ESP-12E Module), Arduino:  
	Flash: 1044464=1019KB  
	SRAM: 81920=80KB  
 
* esp32, nodemcu-32s, Arduino:  
	Flash: 1310720=1280KB  
	SRAM: 327680=320KB (in fact about 80KB, for more use malloc)  
	
* MTK LinkIt 7697 for Arduino:  
	Flash: 2019328=1972KB  
	SRAM: 360448=354KB  

* RealTek Ameba RTL8710AF  
	Flash: 1048576=1024KB  
	SRAM: 397KB (Arduino global array var max size)      
	
* ESP8285, NodeMCU-M  
	like ESP8266, but with 1MB Flash  
	
## ESP-12f breakout board    
**esp8266 blink code: pinMode(13, OUTPUT);**    
RESET<->3.3V (can always 3.3V)    
CH_PC<->3.3V  
GPIO13<->LED<->200R<->GND (for blink code)    
VCC<->3.3V  
TXD<->RX  
RXD<->TX  
GPIO0<->GND (if not burning, connect 3.3V to run blink code)   
GPIO15<->GND  
GND<->GND  
(need some connected pins for common 3.3V and common GND)  

## doc  
* 安信可-NodeMCU 核心开发板, esp8266  
http://wiki.aithinker.com/esp8266/boards/nodemcu  

* ESP8266 ESP32  
https://github.com/SmartArduino/SZDOITWiKi/wiki/ESP8266---ESP32  

* **ESP8266 on Arduino**  
https://github.com/esp8266/Arduino/blob/master/doc/libraries.rst  
**IMPORTANT**  
http://arduino.esp8266.com/stable/package_esp8266com_index.json  

* ESP8266 Arduino 2.2.0  
https://esp8266.github.io/Arduino/versions/2.2.0/doc/installing.html  

## TFT Drivers  
http://www.lcdwiki.com/zh/【Application】1.44inch_SPI_Module_MSP1443_with_D1_mini  
http://www.lcdwiki.com/zh/【Application】1.6inch_SPI_Module_MSP1601_with_D1_mini  

## Soft WDT reset on ESP8266, Watch dog  
* Use ESP.wdtFeed() in while loop  
https://github.com/esp8266/Arduino/issues/34  
https://techtutorialsx.com/2017/01/21/esp8266-watchdog-functions/  
https://github.com/esp8266/Arduino/blob/master/doc/libraries.rst  

* Use ESP.getResetReason() to get reset reason    

* other reasons:  
https://blog.csdn.net/chen244798611/article/details/51636058  

## Tools  
* cdt (for esp8266, esp32)    
http://wiki.aithinker.com/ai_ide_install  
cygwin\opt\xtensa-lx106-elf  
cygwin\opt\xtensa-esp32-elf  

* FLASH_DOWNLOAD_TOOLS   
<> for esp8266  
(baidupan) nodemcu_v2.rar  
(baidupan) ESP8266Flasher.exe  

* esplorer  
<> for esp32, esp8266    
(baidupan) esplorer_v1.rar  



## Problem  
* bits/c++config.h: No such file or directory  
Create 'Portable' folder under exe folder  
https://www.esp8266.com/viewtopic.php?p=41432  
https://www.instructables.com/id/Portable-installation-guide-of-Arduino-IDE-v165-fo/  

* Run blink example  
Choose board 'NodeMCU 1.0 (ESP-12E Module)' in Arduino IDE for new nodemcu devkit bought from ai-thinker, don't use 'NodeMCU 0.9'   
https://github.com/nodemcu/nodemcu-devkit-v1.0  
https://github.com/nodemcu/nodemcu-devkit  
http://wiki.ai-thinker.com/esp8266/boards/nodemcu  
http://wiki.ai-thinker.com/esp32/boards/nodemcu_32s  

## doit  
http://bbs.doit.am/forum.php  
https://github.com/SmartArduino/SZDOITWiKi/wiki/ESP8266---NodeMCU  

## ESP8266-3种模式用法  
https://blog.csdn.net/weixin_40504976/article/details/84283320  
https://blog.csdn.net/txf1984/article/details/46654995  

## esp-12e折腾  
https://www.cnblogs.com/katachi/p/8468772.html  

## 菜鸟江涛带你学最小物联网系统之模块篇（01）—— WIFI模块ESP12F初次亲密接触  
https://blog.csdn.net/u010898329/article/details/82833893  

## ESP8266-12F WIFI转串口模块底板设计  
https://blog.csdn.net/xiaohupashu/article/details/53574859  

## ESP8266 常见问题, 安信可    
https://wiki.ai-thinker.com/esp8266/faq  

## esp8266 Summary Table  
https://www.esp8266.com/wiki/doku.php?id=esp8266-module-family  

## DSTIKE Deauther MINI ESP8266 WIFI 开发板 OLED NodeMCU     
硬件： https://github.com/lspoplove/Deauther-Project  
软件：  https://github.com/spacehuhn/esp8266_deauther  

## Arduino esp8266 IoT物联网示例代码（重要）  
* search baidupan : mini D1 PRO升级版_信泰微/D1-MINI资料.rar   
D1-MINI资料\ESP8266开发板连wifi点灯测试程序\sketch_jun07a.ino  
https://iot-playground.com/blog/2-uncategorised/40-esp8266-wifi-relay-switch-arduino-ide  
外国原版, see [WiFiWebServer.ino](WiFiWebServer.ino)  
信泰微提供资料中的修改版, see [sketch_jun07a.ino](sketch_jun07a.ino)  

* search baidupan : 信泰微_ESP8266套装, ESP8266物联网教程  
(TODO) 无法在真机上看到运行效果, 待考(基于安信可的IDE)  

* search baidupan : esp-12f_信泰微  
烧录方法   

## 信泰微, 技小新esp8266开发板烧录方法：  
ESP8266物联网开发板 sdk编程视频全套教程 wifi模块小系统板  
[jixin.txt](jixin.txt)  
search baidupan: readme_烧录方法.txt  

## What is ESP8266EX    
在espressif的英文官网上，esp8266被称为esp8266ex，那么esp8266ex是什么意思呢？  
https://www.espressif.com/en/products/hardware/esp8266ex/resources  
原来，我们平常所说的esp8266，用英文的准确说法是esp8266系列的其中一个型号esp8266ex，只不过习惯了不叫ex而已。另外esp8266还有一个型号叫esp8285，不过esp8285很少时候需要用到，只是flash的大小增加了  
http://esp8266.net  

## cesanta/ESP8266_RTOS_SDK  
https://github.com/cesanta/ESP8266_RTOS_SDK  
https://github.com/espressif/ESP8266_RTOS_SDK  
https://github.com/cesanta/esp-open-sdk  
https://github.com/pfalcon/esp-open-sdk  

## ESP8266_NONOS_SDK  
https://github.com/espressif/ESP8266_NONOS_SDK  

## samples  
https://github.com/espressif/esp8266-nonos-sample-code  
https://www.espressif.com/sites/default/files/documentation/2a-esp8266-sdk_getting_started_guide_cn.pdf  

## ESP8266 toolchain    
* see https://github.com/espressif/ESP8266_RTOS_SDK  
* https://dl.espressif.com/dl/xtensa-lx106-elf-gcc8_4_0-esp-2020r3-win32.zip  
* see https://www.cnblogs.com/dongxiaodong/p/12905967.html  
* https://dl.espressif.com/dl/xtensa-lx106-elf-win32-1.22.0-100-ge567ec7-5.2.0.zip  
* see https://github.com/espressif/ESP8266_RTOS_SDK/issues/843  
* see https://docs.espressif.com/projects/esp8266-rtos-sdk/en/latest/get-started/windows-setup.html  
* https://dl.espressif.com/dl/xtensa-lx106-elf-win32-1.22.0-88-gde0bdc1-4.8.5.tar.gz  

## ESP8266工具链4.8.5编译缺少libmesh.a跟libc.a跟libhal.a  
https://blog.csdn.net/weixin_42276326/article/details/108422865  
https://github.com/esp8266/esp8266-wiki/raw/master/libs/libhal.a  
https://github.com/esp8266/esp8266-wiki/raw/master/libs/libc.a  

## ESP8266 NONOS SDK开发初探各种报错解决方法（一）  
https://blog.csdn.net/weixin_43128823/article/details/108058537  
原来需要手动将demo，放到根目录才行  

## SPI_SIZE_MAP ?= 4  
32Mbits==4MB  
初学ESP8266所遇到的坑  
https://www.pianshen.com/article/892640775/  
ESP8266 烧写选项 Flash Size 32M和32M-c1的区别  
https://blog.csdn.net/toopoo/article/details/86415497  
esp8266 SDK3.0 spi_size_map设置 12f NORTOS问题解决方法  
https://blog.csdn.net/a1058191679/article/details/102644915  

## ESP8266 SDK开发基础入门  
3-ESP8266 SDK开发基础入门篇--点亮一个灯  
https://www.cnblogs.com/yangfengwu/p/11073055.html  
https://gitee.com/yang456/Learn8266SDKDevelop.git  

## Blynk  
使用ESP8266和Blynk制作物联网控制的机器小车  
https://www.yiboard.com/forum.php?mod=viewthread&tid=1258  
https://community.blynk.cc/t/new-blynk-library-release-v0-5-4/28463  
BlynkSimpleEsp8266  
https://github.com/blynkkk/blynk-library  
https://github.com/blynkkk/blynk-library/blob/master/src/BlynkSimpleEsp8266.h  
https://examples.blynk.cc  
https://blynk.io/  
