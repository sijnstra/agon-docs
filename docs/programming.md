# Programming your Agon Light computer

Whilst there is a lot of great software you can download and run on your Agon, you can write your own software too. And this is probably the reason you bought your Agon!

There are several programming languages available, something for everyone, from beginner to expert... or those just reliving their 1980's memories.

Some of the languages run directly on your Agon computer. Some run on your Windows, Mac or Linux PC for transfer to your Agon. Plus, there are some which your can run both on the Agon and your PC.

In order to help speed up development, there is also an emulator so your can program and test _most_ code quickly on your PC, before transferring to the Agon.



## Languages

### Basic

The most popular language is instaled by many Agon owners and is a great way to quickly start programming your Agon computer. 

The Agon port of BBC Basic provides a familiar yet powerful language used by beginners and experts alike. It runs directly on the Agon computer and is often started automaticaly by many users with a command in the `autoexec.txt` file.

Alternative operating systems such as CP/M can be used on the Agon Light, but MOS is the default operating system.

### The video display processor, or VDP

Whilst the eZ80 is manufactured today, none of the video chips that were used in computers of the 1970s and 1980s are still manufactured, so for video output a different solution is needed.  To solve this problem the Agon Light uses a separate video processor, which we call the VDP, the Video Display Processor.  This chip is responsible for sound and video output, and also keyboard and mouse input.  Technically, this is an ESP32-Pico-D4 chip, which has attached to it an 8MB RAM chip which is used for storing bitmaps, sound samples, fonts, and other data.

The exact technical details of the VDP however for most programmers is not important - in the Agon platform, from a software perspective, the VDP is designed to be used via a [simple API](VDP.md), with the details of how it works abstracted away.  Indeed, when using an emulator of the Agon Light, the VDP chip is not emulated at all; the emulator instead runs a compiled version of the VDP firmware using the host computer's video and audio hardware.


Effectively, the design of the Agon Light is that of two computers in one.  The eZ80 is the computer that is used to run programs, and the VDP is a smart terminal computer that draws the screen, plays sound, and handles the keyboard and mouse[^1] interfaces.  The eZ80 and the VDP communicate with each other using a high speed serial interface.


Some other retro-inspired computers take a different approach to solving the video output problem.  Often this involves making use of an FPGA chip, which is a chip that can be programmed to behave like any other chip.  This is a very flexible solution, but it is also very expensive.  The Agon Light takes a different approach, using a separate video processor chip, which is much cheaper than an FPGA.


The use of what is effectively a separate computer for the VDP in the Agon platform creates a significant architectural difference to many classic home computers of the 8-bit, 16-bit and early 32-bit era.  Those classic computers would usually use a shared area of memory that the main processor and the video processor would both have access to.  This shared memory would be used to store the screen memory, and the main processor would write to this memory to update the screen.  This is not the case with the Agon platform.  The eZ80 and the VDP have no shared memory, and the VDP has no access to the eZ80's RAM.  This means that the VDP cannot read the screen memory directly, and the eZ80 cannot write directly to the screen memory.  Instead, the VDP has to be sent commands to draw things to the screen, and the eZ80 has to be sent commands to read things from the screen.  This is a significant difference to many classic computers, and is something that programmers need to be aware of when writing programs for the Agon platform.


## The Agon software platform

From a software perspective, a significant inspiration for the Agon Light was the BBC Micro, a popular computer in the UK from the 1980s designed and built by Acorn Computers Ltd..  (Acorn went on to design the 
