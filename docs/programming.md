# Programming your Agon computer

Whilst there is a lot of great software you can download and run on your Agon, you can write your own software too. And this is probably the reason you bought your Agon!

There are several programming languages available, something for everyone, from beginner to expert... or those just reliving their 1980's memories.

Some of the languages run directly on your Agon computer. Some run on your Windows, Mac or Linux PC for transfer to your Agon. Plus, there are some which your can run both on the Agon and your PC.

Most of the languages available allow you to code in traditional 16bit or 24bit _ADL mode_, where the full amount of memory is available, not limited to 64k.

In order to help speed up development, there is also an emulator so your can program and test _most_ code quickly on your PC, before transferring to the Agon.

It doesn't matter which model you own from the Agon platform range of computers, inside they are all the same and can run exactly the same software. The only thing which might make your software be less compatible is if you utilise features from the latest OS builds where another user may not have updated their system. If you intend on sharing your programs, make sure you specifiy the minimum system of MOS/VDP required.

All languages listed here come with examples to help you get started.

There are several getting started guides on the internet too, as well as YouTube videos, such as those from [https://www.youtube.com/@AgonBits] 



## The Languages

### Basic

This most popular language is installed by many Agon owners and is a great way to quickly start programming your Agon computer. 

The Agon port of BBC Basic provides a familiar yet powerful language used by beginners and experts alike. It runs directly on the Agon computer and is often started automaticaly by many users with a command in the `autoexec.txt` file.

Download from here (16bit mode): https://github.com/breakintoprogram/agon-bbc-basic

Download from here (ADL mode): https://github.com/breakintoprogram/agon-bbc-basic-adl


### Z80 Assembly

If you have ever written software in z80 Assembly for the Sinclair ZX81, ZX Spectrum, MSX, Amstrad CPC, TRS-80, Nintendo Game Boy, or even the Texas Instruments calulators, then this will be familliar territory for you.

You can write your code in whatever text editor you like, then assmble your source code with `ez80asm`, a z80 assembler which runs on the Agon itself, or on Mac, Windows, Linux, and even Raspberry Pi.

Download ez80asm assembler from here: https://github.com/AgonPlatform/agon-ez80asm


### C++

Many programmers enjoy coding in `C` or `C++`. This language is also available and there are a few options for coding on your desktop PC, then compiing and transferring onto your Agon to run.

A whole development toolchain is available for Windows called `AgDev`, and a Mac/Linux/Raspberry Pi toolchain called `Agondev`.

Download Windows (AgDev) from here: https://github.com/pcawte/AgDev

And Mac/Linux/Raspberry Pi (AgonDev) from here: https://github.com/AgonPlatform/agondev


### B Simple

_B_ was a language which, unsurpisingly, was around before _C_. This interpretation, `B Simple`, allows you to create programs that will be familliar to anyone who has used C, but without all the advanced features of C++. B Simple can be used on the Agon itslef, or on your desktop PC under Mac, Linux, Windows or Raspberry Pi. 

`B Simple`'s approach is to compile your code into z80 assembler, then use the power of `ez80asm` to assemble the compiled code into the final binary executable. It can eaasily be expanded by writing custom libraries in z80 assembler.

Download B Simple from here: https://github.com/nihirash/bsimple-ez80-compiler

### Forth

Some Agon users might reminisce on the days long gone of owning (or wishing they owned) a Jupiter Ace, with its more obscure _Forth_ programming language. 

`Agon Forth` runs on the Agon itself and provides a great way to learn the language.

Download Forth from here: https://github.com/lennart-benschop/agon-forth

## The Emulator

While you are here, you may as well download the latest version of the emulator: https://github.com/tomm/fab-agon-emulator



