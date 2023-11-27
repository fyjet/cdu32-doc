---
layout: home
---

CDU32 is a small device based on cheap ESP32 microcontroller that allow to interract with Flight Simulator instruments. 3.5' touch display instrument with concentric rotary encoder.

It is inspired by Aibus A400M RTU (Radio Tunin Unit) and MCDU (Multifunctional Control and Display Unit).

![CDU32](assets/img/cdu32-home.jpg)

# Features

* Tunning of communication frequencies for entire radio stack (Radio Tuning Unit RTU)
* Audio Controle Panel (ACP)
* Tunning of navigation frequencies, VOR 1&2 curses
* Flight Control Unit (FCU) for autopilot parameters
* Trim axis
* Performances factors like OAT, TOW (display only)

# Architecture

CDU32 device connects to Flight Simulator using MQTT messaging protocol. On Flight Simulator computer, bridging to MQTT is done with fsbridge (python3.8 program). CDU32 device is programmed using C++.

# Project

CDU32 project is divided into two repositories:

* [CDU32-ESP32 source code](https://github.com/fyjet/cdu32-esp32)
* [CDU32-FSBridge (Flight Simulator bridge)](https://github.com/fyjet/cdu32-fsbridge)

# How to start

## Quick start

Read [build](build) and [run](run) pages

# Support

In order to get support, please use [github issue](https://github.com/fyjet/cdu32-doc/issues) on cdu32-doc project.
