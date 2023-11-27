---
layout: page
title: Protocol
permalink: /protocol/
---

# Constant values
### Display layout
Display is divided with 4 columns and 8 lines. Position code contains 2 digits: first is column (from zero) and line (from 1), from left top corner.
01 11 21 31  
02 12 22 32   
03 13 23 33  
04 14 24 34  
05 15 25 35  
06 16 26 36  
07 17 27 37  
08 18 28 38  

### Encoders
INC1UP 50  
INC1DN 51  
INC2UP 52  
INC2DN 53  

### Buttons
BT1 57  
BT2 58  
BT3 59  

### Colors
WHITE 99  
YELLOW 98  
GREEN 97  
BLACK 96  

## device bridge (command mode)
### New screen
topic: j/[deviceName]/c/d  
content: N,[title]  
Clear screen, remove buttons and actions and write title on top in white color

### Create clickable button on screen
topic: j/[deviceName]/c/d  
content: B,[code Side Key on 2 chars],[bouton label]  
Create an outlined button with lable, LSK1-4, RSK1-4. This button returns position on key topic when pressed

### Print text, with or withoud clickable outlined
topic: j/[deviceName]/c/d  
content: T,XX,CC,B,Z,[string]  
Display string in position Side Key XX and color CC  
If B=0, no outline, if B=1 green outline (button reacts on click and returns posiiton on key topic)
Z is font size: 2 or 3

### Print slider
topic: j/[deviceName]/c/d  
content: S,XX,CC,value in percent
Print a slider at position XX (LSK1-4, RSK1-4) with color CC, value is in percent

### Autopilot led
topic: j/[deviceName]/c/d  
content: L,value (0 or 1)
Turn autopilot led On (value=1) or Off (value=0)

### beep
topic: j/[deviceName]/c/d  
content: X
Sounds a beep on cdu32


### request status (optionnal)
topic: j/[deviceName]/c/reqstatus  
content: 1  
Send a status request

## device to fsbridge (event mode)
### Pressed key (clickable, button or encorder)
topic: j/[deviceName]/e/k  
content: [pressed button button]  
Send position of pressed key

### status
topic: j/[deviceName]/e/s  
content: [code status]  
Send response to reqstatus, returns present status  
0 OK
other ERROR
