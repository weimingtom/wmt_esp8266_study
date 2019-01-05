# wmt_esp8266_study
My ESP8266 / ESP32 study  

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

## Soft WDT reset on ESP8266, Watch dog  
Use ESP.wdtFeed() in while loop, use ESP.
https://github.com/esp8266/Arduino/issues/34  
https://techtutorialsx.com/2017/01/21/esp8266-watchdog-functions/  
https://github.com/esp8266/Arduino/blob/master/doc/libraries.rst  
other reasons:  
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
