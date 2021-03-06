# Acheron Elongate rev. Beta QMK firmware repository

![](https://i.imgur.com/G9LESkUh.jpg)

* Keyboard Maintainer: [Gondolindrim](https://github.com/Gondolindrim)
* Hardware Supported: [open-source PCB](https://github.com/AcheronProject/Elongate) powered by STM32F072 microcontroller
* Hardware Availability: the revision beta of Elongate was never publicly sold.

## Introduction

This is the QMK firmware repository for the Elongate PCB revision Beta and pre-revision Beta versions, which was the initial revision PCB for this keyboard; hence it was never sold publicly.

The Elongate PCB is an Open-Hardware-guideline-compliant PCB which files can be found at [this repository](https://github.com/AcheronProject/Elongate). Its designer and maintainer is [Gondolindrim](https://github.com/Gondolindrim).

## How to flash

### Enter bootloader

The DFU state in the bootloader can be accessed in 3 ways:

* **Bootmagic reset**: Hold down the key at (0,0) in the matrix (usually the top left key or Escape) and plug in the keyboard
* **Physical reset button**: press the button on the front of the PCB.
* **Keycode in layout**: Press the key mapped to `RESET` if it is available.

## Compile firmware

You can build the default layout firwmare for Elongate after setting up your build environment by using:

    make acheron/elongate/beta:default

After entering DFU state in your PCB, you can download the binary file generated through `dfu-util` or a GUI like QMK Toolbox.

To directly flash the PCB after it is put into a DFU state, use

    make acheron/elongate/beta:default:flash

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).

## PCB Documentation

See the [AcheronDocs](https://acheronproject.com/pcbs/elongate/) page for the ElongatePCB full documentation. You can also check the KiCad PCB files at the [Elongate GitHub repository](https://github.com/AcheronProject/Elongate).

Before using the files for personal or commercial use, please read the [Acheron Open-Hardware License V1.4](https://acheronproject.com/AOHL14/) under which the Elongate PCB is published.
