# Project 42: Mouse In The House

* __Official repo for the "42" Digital System Design Final Project__ *

Contributers:
* [Andrew D'Angelo](https://sites.google.com/d/1RBr_eKZI24EjTWzsZB4v3GX3XFpaC1NY/p/18CrMngnyxBPsVCTbK__N-a7D6eivdq0i/edit)
* [Tahrim Imon](https://sites.google.com/stevens.edu/tahrim-imon-mobius-propage?pli=1&authuser=2)



## Overview

Since the project began, the team set out with a singular mission to develop an understanding of HID USB mouse integration using the Nexsys A7-100T FPGA board. Over the previous few months, we struggled with identifying the best way we could demonstrate successful mouse functionality. Initially, the team explored integrating mouse display and control functionality with a previous DSD project; however, we quickly came to realize the complexity of the task was too great for the limited time we had to work on the project. All in all, with the assistance of a fellow classmate (shoutout to Gupreet), the team successfully managed to strip the mouse code down to its very foundation and was able to develop an indepth understanding of the MouseDisplay and MouseCtl files developed by Xilinx.  

## Breaking down the HID Mouse

To integrate the HID USB mouse using VHDL and properly use it on the Nexsys A7 100-T board, a few key files must be added and an adjustment be made to the board. As may be observed below, to use the USB mouse you need to move the blue MODE jumper ( as was performed in lab #2 ) to the __USB/SD__ pin.


 
 
