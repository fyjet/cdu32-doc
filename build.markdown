---
layout: page
title: Build
permalink: /build/
---

# What you need to build CDU32
You'll have to assemble parts to build CDU32.

## List of parts
* 1 x ESP32 Wroom devkit
* 1 x ILI1394 3.5 inch display
* 1 x Double concentric rotary encoder and caps, with push button
* 2 x Momentary push button
* 1 x buzzer
* 1 x yellow LED
* Wiring cable

## Tools
* Soldering iron and tin

# Cabling

| ESP32 GPIO | TFT display ILI9341 |
|---|---|
| 15 (pin23) | TFT_CS |
| 4 (pin26) | TFT_RESET |
| 2 (pin24) | TFT_DC |
| 23 (pin37) | TFT_SDI/MOSI |
| 18 (pin30) | TFT_SCK |
| 3.3v | TFT_LED |
| 19 (pin31) | TFT_SDO/MISO |
| 18 (pin30) | T_CLK |
| 25 (pin 9) | T_CS |
| 23 (pin37) | T_DIN |
| 19 (pin31) | T_DO |
| 26 (pin10) | T_IRQ (used for fast TS readings) |

| ESP32 GPIO | twin rotary encoders |
|---|---|
| 13 (pin15) | ENC1 A |
| 12 (pin13) | ENC1 B |
| GND  |ENC1 COMMON |
| 14 (pin12) | ENC2 A |
| 27 (pin11) | ENC2 B |
| GND  |ENC2 COMMON |

| ESP32 GPIO | buttons |
|---|---|
| 32 (pin 7) | button1 |
| GND | button1 COMMON |
| 33 (pin 8) | button2 |
| GND | button2 COMMON |
| 5 (pin29) | button3 (auto pilot) |
| GND | button3 COMMON |

| ESP32 GPIO | lights |
|---|---|
| 17 (pin28) | LED + (autopilot) |
| GND | LED COMMON |

| ESP32 GPIO | buzzer |
|---|---|
| 16 (pin27) | buzzer + |
| GND | buzzer - |


# How to program CDU32

* Install [Visual Studio Code](https://code.visualstudio.com/Download) and then [platformio plugin](https://docs.platformio.org/en/latest/integration/ide/vscode.html#installation).
* Download [CDU32-ESP32 latest release](https://github.com/fyjet/cdu32-esp32/releases/latest)
* Uncompress it in your directory HOME/Documents/PlatformIO/Projects/

CDU32 configuration to adapt to your network settings is done by editing include/config.h file:
* Copy include/config_template.h to include/config.h
* Set Wifi network parameters: SSID and password
* Set MQTT server parameters: IP address

* Build program and upload it to ESP32
* You are readu to [run CDU32](../run/)
