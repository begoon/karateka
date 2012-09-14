The vintage game Karateka
=========================

If you install the AppleWin emulator and google for `karateka.dsk.gz`, you can experience
the original gameplay from the Apple version of Karateka.

![](https://github.com/begoon/karateka/raw/master/karateka-screenshot-apple.png)

A snapshot from the DOS version.

![](https://github.com/begoon/karateka/raw/master/karateka-screenshot.png)

For lazy players
================

The patch below allows to quickly win the game, for example: http://www.youtube.com/watch?v=HjeuB6pxMzI (don't miss the funny episode at the end of the video).

    Immortality
    KARATEKA.EXE
    00003066: 48 90
    00003D7E: 48 90

    Steel breast
    KARATEKA.EXE
    0000306E: 83 C6
    0000306F: 3E 06
    00003072: 3F 01
    00003073: 7E 75

    Flying kick for humans
    KARATEKA.EXE
    00002F30: 7E 00

    Flying kick for bird
    KARATEKA.EXE
    00002E2F: 7F 00
    00002E30: 01 00
    00002E34: 3D 25
    00002E35: 04 00
    00002E44: 06 00

    Kill bird by first kick
    KARATEKA.EXE
    000031BA: 85 33

    Kill humans by first kick
    KARATEKA.EXE
    00002F3A: 85 33


Applying the patch
------------------

    cd patch
    cp ../KARATEKA.EXE .
    ruby patch-xck.rb KARATEKA.XCK

Answer YES to the questions and it procudes the `KARATEKA_patched.EXE` file.
