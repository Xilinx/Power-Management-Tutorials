===============================
Using the Power Advantage Tool
===============================

**************
Overview
**************

The purpose of this project is to demonstrate the use of the Power Advantage Tool on the Ultra96v2 board. The Power Advantage tool connects to the Infineon measurement chip on-board this device via wired I2C connections. Connecting to this on-board chip enables you to not only extract important measurements regarding power from the board, but you can also begin your dive into power management and gain some meaningful experience working with the tools that enable you to monitor power. Throughout this tutorial, you as an engineer will learn about the process of setting up the Power Advantage Tool, as well as hopefully learn some transferable knowledge to your own projects. Just like the engineers in our Power Advantage Tool Video, let's get to work!

****************************
Hardware Requirements
****************************

To successfully perform this tutorial, ensure that you have the following hardware available:

- Ultra96v2 board

  .. image:: ./media/image1.jpeg

- Bus Pirate

  .. image:: ./media/image2.jpeg

- Three wires, where one side is a male header and the other side is a female header

  .. image:: ./media/image3.jpeg
     :alt: Jumper Wires Premium 6&quot; M/F Pack of 10 - PRT-09140 -
      SparkFun Electronics

- USB to USB MINI-B cord

  .. image:: ./media/image4.jpeg

********************************
Step-by-step Walkthrough
********************************

1. Solder the three male headers of the separate wires to the I2C interface on the Ultra96v2 board. The soldering job is shown in the following figure. 
   
   The left black wire is SCL, the middle white wire is SDA, and the right grey wire is GND.

   .. image:: ./media/image5.jpeg
     :alt: Machine generated alternative text; -—rpst rpso R4S vps T'P4
      cct RISO -RI-st RVCQ ors rpt.
      

2. Next, connect the female headers of these wires to the bus pirate.
   
   The SCL wire connects to the ``CLK`` pin, the SDA wire connects to the ``MOSI`` pin, and the GND wire connects to the ``GND`` pin. This wiring is shown below. Once the wires are connected, connect the USB MINI-B port of the bus pirate to the USB port on the host computer using the USB MINI-B to USB cord. Do not forget to turn on your device!

   .. image:: ./media/image2.jpeg

3. Now that you have successfully completed the hardware setup of the project, you can start on getting the Power Advantage Tool set up! Download the .zip file for the board you would like to use. You can find a list of files `here <https://xilinx-wi                                                     |
| ki.atlassian.net/wiki/spaces/A/pages/18841681/Zynq+UltraScale+MPSoC+P |
| ower+Advantage+Tool+part+1+-+Introduction+to+the+Power+Advantage+Tool>`__. Make sure to download the most updated version.

4. After downloading the zip file, unzip it to the file path you choose.

   .. image:: ./media/image6.png

5. Inside this folder, navigate to the following path:

   .. image:: ./media/image7.png

6. Once in this folder, click on the ``CP210xVCPInstaller_x64.exe`` file to download a necessary USB to UART driver for the Power Advantage Tool. If you are using a 32-bit machine, make sure to download the x86 version instead.

   .. image:: ./media/image8.png
     :alt: Machine generated alternative text; Name x64 x86
      CP210xVCPlnstaller x64.exe CP210xVCPlnstaller x86.exe dpinst.xml
      SLAB License Agreement VCP Windows.t.xt slabvcp.cat slabvcp.inf
      Date modified 9/20/2020 9:18 AM 9/20/2020 9:18 AM 5/16/2016 8:30
      PM 5/16/2016 8:30 PM 5/16/2016 8:30 PM 5/16/2016 8:30 PM 5/16/2016
      8:30 PM 5/16/2016 8:30 PM Type File folder File folder Application
      Application XML Document Text Document Security Catalog Setup
      Information Size 1,034 KB 911 KB 12 KB 11 KB 12 KB

7. Also install the following tools which are available in the ``tools/`` folder within the Power Advantage Tool directory.

   .. image:: ./media/image9.png
     :alt: Machine generated alternative text: AutoHotkey1122D3
      Install.exe Z] • WHQL Certlfied.exe 7/17/2015258 AM 11/30/2015
      11:18 AM Application Application 2802 KB 2032 KB

8. Once all of the necessary drivers are installed, move the ``ZynqUS_Demos`` folder to your ``C:/`` drive. This is necessary to allow the proper shortcut when opening the Power Advantage Tool. The necessary path is shown below.

   .. image:: ./media/image10.png

9. Now connect your Ultra96v2 board to power and turn on your board. Booting by JTAG or by SD card is not necessary since you are only extracting data from the INA226 chip on the board.

10. With the board powered on, navigate through your ``ZynqUS_Demos`` folder to the following path.

   .. image:: ./media/image11.png

11. Within this folder is a shortcut titled ``ZynqusPowerTool.exe Ultra96 - Shortcut``. Double-click to open this shortcut. Once the shortcut executes, you should see the Power Advantage Tool at work! 

   .. image:: ./media/image12.png
     :alt: Machine generated alternative text: ZynqusPowerTool ZYNQ%
      ultra-SCALÉ+ x Zynq UltraScale+ MPSoC Power Management Socct Low
      Power R5/O R511 09MUl CSU Periph I ±Full Power Domain A53/O A5311
      •103% 9103% A5312 - A53/3 •103% 9103% Periph Batt Power Domain PS
      Temperature 0.00 Full Power Domain VCCO HP Low Power Domain Prog
      Logic Domain Total 1023.4 mW 443.2 mW 1231.6mW 2698.2 mW
      Programmable Logic Domain 0103% • Hard Ecc 25%, am', 2_5v


Congratulations on completing this project! Hope you had some fun along the way.