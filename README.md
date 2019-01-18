# wmt_esp8266_study
My ESP8266 / ESP32 study  

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
	
## doc  
* esp32 ref  
https://docs.espressif.com/projects/esp-idf/en/latest/index.html  

* 安信可-NodeMCU 核心开发板, esp8266  
http://wiki.aithinker.com/esp8266/boards/nodemcu  

* 安信可-NodeMCU-32S 核心开发板, esp32    
http://wiki.aithinker.com/esp32/boards/nodemcu_32s  

* ESP8266 ESP32  
https://github.com/SmartArduino/SZDOITWiKi/wiki/ESP8266---ESP32  

* **ESP8266 on Arduino**  
https://github.com/esp8266/Arduino/blob/master/doc/libraries.rst  
**IMPORTANT**  
http://arduino.esp8266.com/stable/package_esp8266com_index.json  

* ESP8266 Arduino 2.2.0  
https://esp8266.github.io/Arduino/versions/2.2.0/doc/installing.html  

* ESP-IDF Programming Guide  
https://docs.espressif.com/projects/esp-idf/en/latest/index.html  

* ESP32 资源  
https://www.espressif.com/zh-hans/products/hardware/esp32/resources  

* ESP32 技术参考手册 (pdf)    
https://www.espressif.com/sites/default/files/documentation/esp32_technical_reference_manual_cn.pdf  

* ESP32 常见问题 (pdf)  
https://www.espressif.com/sites/default/files/documentation/ESP32_FAQs__CN.pdf  

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
* esp-idf (for esp32)    
for windows, need msys2 (from dl.espressif.com) and esp-idf two parts      
https://docs.espressif.com/projects/esp-idf/en/stable/get-started/windows-setup.html  
https://dl.espressif.com/dl/esp32_win32_msys2_environment_and_toolchain-20180110.zip  
https://docs.espressif.com/projects/esp-idf/en/stable/get-started/  
$ cd ~/esp  
$ git clone -b v3.1.2 --recursive https://github.com/espressif/esp-idf.git  

* arduino plugin (for esp32)    
https://dl.espressif.com/dl/package_esp32_index.json  

* cdt (for esp8266, esp32)    
http://wiki.aithinker.com/ai_ide_install  
cygwin\opt\xtensa-lx106-elf  
cygwin\opt\xtensa-esp32-elf  

* FLASH_DOWNLOAD_TOOLS  
<> for esp32  
(baidupan) FLASH_DOWNLOAD_TOOLS_V3.6.2.2_v1_good.rar  
<> for esp8266  
(baidupan) nodemcu_v2.rar  
(baidupan) ESP8266Flasher.exe  

* esplorer  
<> for esp32, esp8266    
(baidupan) esplorer_v1.rar  

## Download  
http://wiki.ai-thinker.com/esp_download  

## Ref  
* nodemcu：  
https://github.com/nodemcu/nodemcu-firmware/releases?after=1.5.1-master_20160603  

* micropython：  
http://micropython.org/download  

* Espruino：  
http://www.espruino.com/Download  

* mruby：  
https://github.com/mruby-esp32/mruby-esp32  

## luanode  
* https://github.com/Nicholas3388/LuaNode  

## NES  
* https://github.com/espressif/esp32-nesemu  

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

## oled  
https://github.com/squix78/esp8266-oled-ssd1306  

## esp32  
http://esp32.net  
https://github.com/G6EJD  

## esp32_mmd  
https://github.com/elect-gombe/esp32_mmd  
https://wifiboy.club/topic/59/3d-rendering-test-on-wifiboy32  

## wifiboy  
https://wifiboy.org  

## 乐鑫Esp32学习之旅  
https://blog.csdn.net/xh870189248/article/details/80208099  

## uGFX    
https://blog.csdn.net/qq_27114397/article/details/79027053  
https://github.com/InfiniteYuan1/esp32-ugfx-gui  

## esp32_gme  
https://github.com/lexus2k/esp32_gme  

## go-play  
https://github.com/OtherCrashOverride/go-play  

## esp32_ST7735_Tetris  
https://github.com/MhageGH/esp32_ST7735_Tetris  

## rtl / Ameba IoT    
https://www.amebaiot.com/cn/ameba-arduino-getting-started-rtl8710/  
https://www.amebaiot.com/cn/ameba-arduino-getting-started/  
https://blog.csdn.net/lvj_158/article/details/51234751  
https://www.amebaiot.com/cn/  
SWD模式下下载调试程序  
http://blog.sina.com.cn/s/blog_7ca994b801019ub1.html  
PADUINO Padi Stamp Photo Blog with SWD and CH340g  
https://forum.pine64.org/showthread.php?tid=5111  

## StudyInEsp32  
https://github.com/xuhongv/StudyInEsp32  
https://blog.csdn.net/xh870189248/article/details/80524714  

## esp32-iot-uno    
https://github.com/esp32vn/esp32-iot-uno  

## esp32-devkit  
https://www.sparkfun.com/news/2017  
https://github.com/CHERTS/esp32-devkit  

## PocketSprite Assembled    
OLED screen, 25 x 22 mm, 96 x 64 px, cropped to 5:4 ratio, 60+ FPS  
https://pocketsprite.com  
https://github.com/PocketSprite  

## odroid go  
2.4inch 320×240 TFT LCD (SPI interface)  
https://www.hardkernel.com/shop/odroid-go/  
https://wiki.odroid.com/odroid_go/odroid_go  

## m5stack  
https://docs.m5stack.com/  
https://github.com/m5stack/M5Stack  
