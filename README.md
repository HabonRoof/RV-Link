# RV-Link Introduction/RV-Link簡介

RV-Link is a debugger which made up by RISC-V MCU GD32VF103CBT6

This repostory is a copy of <https://gitee.com/zoomdy/RV-LINK>.

If you want to download the code at the website, you'll need to register an account, so I copy the code and firmware to the github to avoid that, and let everyone can use easily.

As the name "RV-Link" implied, this project is like "BlackMagic", which can turn MCUs into JTAG device, like the J-Link, and this project use GD32VF103CBT6 RISC-V architecture micro processor to do the job.

You can buy a GD32VF103CBT6 develop board at [GD32 RISC-V Nano Board](https://stage.mapleboard.org/gd32-risc-v-nano-product-page/)  

Or you can also choose the smaller one at [GD32 RISC-V Pico Board](https://stage.mapleboard.org/gd32-risc-v-pico-product-page/)

RV-Link是一個使用GD32VF103 RISC-V架構微處理器的除錯計專案
如同RV-Link這個名子暗示的，它是一個有如"BlackMagic"一樣，能夠將特定微處理器變成符合JTAG規範的除錯器（Debugger），而這個專案使用GD32VF103CBT6作為核心來完成這個任務。  

你可以前往 [GD32 RISC-V Nano Board](https://stage.mapleboard.org/gd32-risc-v-nano-product-page/) 來購買GD32VF103CBT6開發板，  

或者也可以買到更小更便宜的[GD32 RISC-V Pico Board](https://stage.mapleboard.org/gd32-risc-v-pico-product-page/)

# How to use/如何使用
To use this reposity, you will need a GD32VF103 seires board.

* First, buy a GD32 RISC-V Nano/Pico. 

* Second, follow the guide below to construce the environment to build the source code. 

* Third, upload the code through DFU mode, and ensure the on-board green LED flash. 

* Fourth, Now the board turned into RV-Link, so you can connect to another target (such as another GD32 RISC-V Board or any development board), follow the JTAG pinout, and use debugger to start yout journy of embedded system!   

要使用這個資料庫，你會需要DS32VF103系列的開發板  

* 首先購買一塊GD32 RISC-V Nano/Pico板。  

* 第二，依照下方指南來建立開發環境以便建置RV-Link的韌體。  

* 第三，利用DFU上傳韌體，並且確認板載的綠色LED會閃爍。  

* 第四，現在開發板已經化身為RV-Link，你可以將任意板子透過JTAG的腳位規範連接到RV-Link，利用這個除錯器開起嵌入式系統的開發之旅吧！  

# References/參考資料
* [GD32VF103CBT6 Datasheet]()
* [PlatformIO official website]()

# Environment Setup/環境建置

## For Linux user:
Benefit from the spirit of open source of Linux, there are many wayes to build the RV-Link firmware, we have two recommend method:
* [PlatformIO](https://platformio.org/?utm_source=github&utm_medium=core) 
* [RISC-V GNU toolchain](https://github.com/riscv/riscv-gnu-toolchain)

### PlatformIO
[PlatformIO environment setup](https://docs.platformio.org/en/latest/integration/ide/pioide.html)  

繁體中文版教學連結：[GD32 RISC-V 開發板的PlatformIO開發環境建置](https://stage.mapleboard.org/platformio-environment-setup/)  

99dfu-rule

platform = gd32v@1.1.1  

dfu-util  

risc-v tool chain  

GDB  

## For Windows user:

1.  You need "libusb" driver for Windows (Not GD32 official driver), the download link is [HERE](https://github.com/pbatard/libwdi/releases/download/b721/zadig-2.4.exe)  

2. After download, launch "Zadig", and choose "GD32 Devices in DFU Mode", replace the driver into "WinUSB"  
圖片  

3. Download DFU Tool for Windows
Download a DFU Tool for windows [HERE](http://dl.sipeed.com/LONGAN/Nano/Tools/GD32_MCU_Dfu_Tool_V3.8.1.5784_1.rar) and decompress it.  
You will get two directeries that is "GD32 MCU Dfu Drivers_v1.0.1.2316" and "GD32 MCU Dfu Tool_v3.8.1.5784"  
* Get into the driver directory, install the GD32 MCU Dfu Driver
圖片
* Run the "GD32 MCU DFU Tool.exe", plug in the GD32 RISC-V Nano/Pico Board, and press down the "BOOT" button on the board, and single press "RST" button, then release the "BOOT" button. Now the program can identify the GD32V chip.
圖片

4. Upload the firmware (which file name extension is .bin), and setup the download address as 0x08000000, select "Verify after download" and click "OK" to download the formware file into GD32 RISC-V Nano/Pico.

You can download the latest GD32VF103 DFU Tool at 
dfu-util  

## For Mac user:
Follow the PlatformIO tutorial [HERE](https://platformio.org/platformio-ide)  

And the other step is like as Linux tutorial.


The enviorment setup guide
The dfu-util tool
