# akeypad

8khz polling rate keypad, uses STM32F405 and USB3300, powered by QMK.

This project is just a prototype, cases, plates and other keyboard components are not included.

![akeypad](https://i.imgur.com/odIXScQ.jpg)

## PCB

![pcb_2](https://i.imgur.com/rlXCcCM.png)
![pcb_1](https://i.imgur.com/XtBSORx.png)
![pcb_2](https://i.imgur.com/3Kbza0o.png)

## Firmware

The code can be found on my [Fork](https://github.com/luantty2/qmk_firmware/tree/qmk_master_build_2022q4/keyboards/akeypad).

## Bootloader

STM32f405/7xx should comes with a built-in bootloader, but sadly it doesn't seem to work on USB HS interface, if someone uses the default bootloader, he has to manually switch to FS port to upload firmware, then switch back to HS port to use his keyboard.

To address the issue, we can use a mux chip with a customizable bootloader to automatically do the trick, then you don't bother switching port.

## How to test polling rate




