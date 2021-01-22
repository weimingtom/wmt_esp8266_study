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
