# Project 42: Mouse In The House

* __Official repo for the "42" Digital System Design Final Project__ *

Contributers:
* [Andrew D'Angelo](https://sites.google.com/d/1RBr_eKZI24EjTWzsZB4v3GX3XFpaC1NY/p/18CrMngnyxBPsVCTbK__N-a7D6eivdq0i/edit)
* [Tahrim Imon](https://sites.google.com/stevens.edu/tahrim-imon-mobius-propage?pli=1&authuser=2)



## Overview

Since the project began, the team set out with a singular mission to develop an understanding of HID USB mouse integration using the Nexsys A7-100T FPGA board. Over the previous few months, we struggled with identifying the best way we could demonstrate successful mouse functionality. Initially, the team explored integrating mouse display and control functionality with a previous DSD project; however, we quickly came to realize the complexity of the task was too great for the limited time we had to work on the project. All in all, with the assistance of a fellow classmate (shoutout to Gupreet), the team successfully managed to strip the mouse code down to its very foundation and was able to develop an indepth understanding of the MouseDisplay and MouseCtl files developed by Xilinx.  

## Breaking down the HID Mouse

To integrate the HID USB mouse using VHDL and properly use it on the Nexsys A7 100-T board, a few key files must be added and an adjustment be made to the board. 

#### Adjusting the jumper
As may be observed below, to use the USB mouse you need to move the blue MODE jumper ( as was performed in lab #2 ) to the __USB/SD__ pin.

![FPGA board image](/fpga_mode_image.jpg)
 
 
 #### Displaying the Mouse Cursor
 
 To display the mouse cursor in your VHDL project, you need to include the _MouseDisplay.vhdl_ file that is found in this repo. 
 
 __The _MouseDisplay.vhdl_ provides the following ports:__
 * _xpos_: ( input pin ) the x position of the mouse realitive to the top, left-hand corner of the screen.
 * _ypos_: ( input pin ) the y position of the mouse realitive to the top, left-hand corner of the screen.
 * *pixel_clk*: ( input pin ) clock used to read pixels from internal memory and then outputs data on the vga color outputs. Different screen resolutions can be achieved by changing the speed of the clock: 25MHz --> 640x480, 40MHz --> 800x600, 108MHz --> 1280x1024.
 * _hcount_: ( input pin ) recounts the horizontal position of the current pixel from left to right on the screen.
 * _vcount_: ( input pin ) recounts the vertical position of the current pixel from left to right on the screen.
 * *red_out*: ( output pin ) 4 bit color output to the red vga pins.
 * *green_out*: ( output pin ) 4 bit color output to the green vga pins.
 * *blue_out*: ( output pin ) 4 bit color output to the blue vga pins.
 
 
 
 
 
