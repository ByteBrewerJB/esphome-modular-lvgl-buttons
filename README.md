# Modular easy button screen for ESPHome + LVGL on cheap touchscreen devices

## Supported Devices
* Guition `ESP32-4848s040` 4.0" with capacitive touch 120v/220v relays and built in power supply + USB-C [AliExpress Link](https://www.aliexpress.com/item/3256806436431838.html).
* Guition `ESP32-JC8048W550` 5.0" with capacitive touch USB-C [AliExpress Link](https://www.aliexpress.com/item/3256806546911788.html).
* Guition `ESP32-jc4827w543C` 4.3" with capactivive touch and USB-C  [AliExpress Link](https://www.aliexpress.com/item/3256806543342794.html).
* Sunton `ESP32-8048S043` 4.3" with capactivive touch and USB-C [AliExpress Link](https://www.aliexpress.com/item/1005004788147691.html).
* Sunton `ESP32-8048S050` 5.0" with capactivive touch and USB-C [AliExpress Link](https://www.aliexpress.com/item/1005004952694042.html).
* Sunton `ESP32-8048s070` 7.0" with capactivive touch and USB-C [AliExpress Link](https://www.aliexpress.com/item/3256807882909237.html).
* Elecrow CrowPanel `DIS05035H` (v2.2) 3.5" with resistive touch and USB-C  [Manufacturer's Link](https://www.elecrow.com/esp32-display-3-5-inch-hmi-display-spi-tft-lcd-touch-screen.html).
* Waveshare `ESP32-S3-Touch-LCD-7` 7.0" with capactivive touch and USB-C [Manufacturer's Link](https://www.waveshare.com/esp32-s3-touch-lcd-7.htm).

## Install ESPHome on a build machine

I use a lot of svg vector graphics. The latest ESPHome does not install svg by default. Use pip to install cairosvg. If you have pre loaded Home Assistant hardware or images this should already be installed.

```
pip install esphome cairosvg
```

## Downloading the code in Home Assistant

I use the File Manager Add-on to download and edit code from Git repos and the ESPHome Device builder to build the code and install the resulting images onto my ESP32 devices.

[File Manager Add-on](https://github.com/home-assistant/addons/tree/master/configurator)
[ESPHome Device builder Add-on](https://esphome.io/)

# Supported screens

### SDL Display on host

The SDL display platform allows you to use create an ESPHome display on a desktop system running Linux or MacOS. This is particularly useful for designing display layouts, since compiling and running a host binary is much faster than compiling for and flashing a microcontroller target system.

### Guition `ESP32-4848s040` 4.0" 480px * 480px Smart Screen

This is a really great little screen. It has 120v/240v relays so it can control lights directly.  guition-esp32-s3-4848s040-display_modular.yaml has a boot screen, a system for dimming the backlight at night and some basic buttons for controlling local and Home Assistant devices.

### Guition `ESP32-4JC8048W550` 5.0" 480px * 800px Smart Screen

This is one of the best screens I have found so far. Bright IPS display, 16MB flash, Qwiic (i2c) port, speaker port and low cost

### Sunton `ESP32-8048s070` 7.0" 480px * 800px Smart Screen

This is the largest and higest resolution screen avalible for a low cost. It has a very good touch screen and good dimmining ability. Very good for info displays.

### Guition `ESP32-jc4827w543C` 4.3" 272px * 480px Smart Screen

Great screen with an very bright IPS display and dimming. You can get it on Ali for $20 USD. Only problem is it only has 4MB of flash. ESPhome only lets you use half the flash so you need to fit your code in 2MB. It even has a DAC + AMP and a connector for a speaker but try fitting the audio output code in 2MB!
