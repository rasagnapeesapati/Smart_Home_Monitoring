firstly download AURDINO IDE 
https://downloads.arduino.cc/arduino-1.8.18-windows.zip

Then open it securely and download requrire libraires from aurdino
like
1.ESP32 by Espressif Systems

Install via Arduino IDE Board Manager.

Add board URL:
https://raw.githubusercontent.com/espressif/arduino-esp32/gh-pages/package_esp32_index.json


Required Libraries
2.esp_camera.h

For ESP32-CAM camera configuration and image capture.

3.Arduino.h

Core Arduino library for digital I/O, delays, etc.

4.FS.h

Filesystem interface used to handle SD card operations.

5.SD_MMC.h

For using the microSD card slot on ESP32-CAM via SDMMC (1-bit mode supported).

6.SPI.h

SPI library (optional, included for completeness).

7.EEPROM.h

To read/write values (like image count) in non-volatile memory.

8.soc/soc.h

Used to disable the brownout detector on ESP32.

9.soc/rtc_cntl_reg.h

Required to access the brownout control register.

10.driver/rtc_io.h

For using RTC GPIOs and deep sleep functionality.

After installing the required libraries then connect the jumping wires as per the images in the connections folder.
the connect it to the FTID sensor to esp 32 cam and connect it to the aurdino through usb connecter and the dump the code using aurdino in esp 32 cam.
Then  fix out the PIR sensor according to the image in connections folder to the esp 32 cam.

Furtherly place the sd card in the driver in esp 32 cam ,which helps to store the images which are being captured while motion being taking place before the sensor.
