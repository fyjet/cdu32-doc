---
layout: page
title: Run
permalink: /run/
---

# Prerequisites
## On computer running Flight simulator

### Download
* [FSUIPC4](https://fsuipc.simflight.com/beta/FSUIPC4.zip)
* [FSUIPCSDK](https://fsuipc.simflight.com/beta/FSUIPC_SDK.zip)
* [Mosquitto MQTT Server](https://mosquitto.org/download/)
* [Python 3.8.10 32bits](https://www.python.org/ftp/python/3.8.10/python-3.8.10.exe)
* [CDU32-FSBridge latest release](https://github.com/fyjet/cdu32-fsbridge/releases/latest)

### Components installation
* Install Python 3.8.10 for 32 bits architecture (even if you are on 64bits) in c:\Python38-12 directory
* Install paho-mqtt python library
```
pip install paho-mqtt
```
* Install FSUIPCSDK for python 3.8 (supports 32 bits only)
* Install FSUIPC4 (latest version runs on FS2002 to FSX, just force installation on FS2002)
* Install Mosquitto MQTT and run it as service
* Deploy latest FSBRIDGE release to c:\devfs directory

Note: if you dont' want to overload your Flight Simulator computer, you can use [WideFS](https://fsuipc.simflight.com/beta/WideFS7.zip) on a remote computer, where CDU32 is plugged.

Note: it's possible to install an infrastructure MQTT server on a Raspberry Pi 2,3,4 or cheap Orange Pi/Banana Pi device.

## On CDU32 device

* First build, configure and upload [CDU32-ESP32 source code](https://github.com/fyjet/cdu32-esp32/releases/latest) on CDU32
* Connect CDU32 device to Wifi network
* Start Flight Simulator
* Start FSBRIDGE
```
fsbridge.bat
```
* Plug CDU32 device: it will first connect to Wifi network, then connects to fsbrige via MQTT