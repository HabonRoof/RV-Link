# RV-Link Introduction

RV-Link is a debugger which made up by RISC-V MCU GD32VF103CBT6

This repostory is a copy of <https://gitee.com/zoomdy/RV-LINK>.

If you want to download the code at the website, you'll need to register an account, so I copy the code and firmware to 
...the github to avoid that, and let everyone can use easily.

As the name "RV-Link" implied, this project is like "BlackMagic", which can turn MCUs into JTAG device, like the J-Link,
...and this project use GD32VF103CBT6 RISC-V architecture micro processor to do the job.

You can buy a GD32VF103CBT6 develop board at [GD32 RISC-V Nano Board](https://stage.mapleboard.org/gd32-risc-v-nano-product-page/)
Or you can also choose the smaller one at [GD32 RISC-V Pico Board](https://stage.mapleboard.org/gd32-risc-v-pico-product-page/)

# How to use
To use this reposity, you will need a GD32VF103 seires board.

..* First, buy a GD32 RISC-V Nano/Pico.

..* Second, follow the guide below to construce the environment to build the source code.

..* Third, upload the code through DFU mode, and ensure the on-board green LED flash.

..* Fourth, Now the board turned into RV-Link, so you can connect to another target (such as another GD32 RISC-V Board or any development board),
follow the JTAG pinout, and use debugger to start yout journy of embedded system.

# Environment Setup

## For Linux user:

We suggest you to use
VSCode
PlatformIO
platform = gd32v@1.1.1

dfu-util

risc-v tool chain

GDB

## For Windoes user:

dfu-util

## For Mac user:

Sorry we don't have Mac PC to test, you can reference the linux user guide to build the project:(

The enviorment setup guide
The dfu-util tool
