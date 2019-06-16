# Raspberry-Pi-Zero-Rubber-Ducky-Pi

Version alpha0
Rubber Ducky USB HID!


# Info:

## German Keyboard try supports actually all the key in the Result:

### expected: !"§$%&/()=?#@ _ . , ; : \ ` ´ ß { [ ] } + * ~ ' - < > | ^ °

### result:   !"§$%&/()=?#@ _ . , ; : \ ` ß { [ ] } + * ~ ' - # '   


## Introduction
```
      _      _      _      USB       _      _      _
   __(.)< __(.)> __(.)=   Rubber-  >(.)__ <(.)__ =(.)__
   \___)  \___)  \___)    Ducky!    (___/  (___/  (___/ 
```

The USB Rubber Ducky is a Human Interface Device programmable with a simple scripting language allowing penetration testers to quickly and easily craft and deploy security auditing payloads that mimic human keyboard input. Tools and payloads can be found at usbrubberducky.com. Quack!

RubberDucky Pi is a Raspberry Pi distro. based on Minibian which allows the Raspberry Pi Zero to behave similar to a [USB Rubber Ducky](https://hakshop.com/products/usb-rubber-ducky-deluxe): a small device USB device which emulates a keyboard and automates key entry.
Ducky scripts (uncompiled) which are made for the USB Rubber Ducky can be used with the Duckyberry Pi without modification. This can be useful for automating computer tasks, penetration testing machines, playing pranks, or just fun (by default plugging in an untouched Duckberry Pi image will open a Youtube video).
Since it is recognised as a standard keyboard, this tool is compatible with Windows, Mac OS, Linux, Android, PlayStation 4, and anything that supports a USB keyboard.

## Getting Started

These instructions will help you setup and install your own RubberDucky

### Installation

1) Download the latest ISO for [Rasbian Lite](https://www.raspberrypi.org/downloads/raspbian/).

2) Burn the ISO to the Micro SD Card - if you can't do this, [Google can help!](https://www.google.co.uk/search?q=burn+raspbian+lite+to+sd+card)

3) Version alpha0:
    ``` bash
    wget https://raw.githubusercontent.com/lucki1000/Raspberry-Pi-Zero-Rubber-Ducky-Duckberry-Pi/master/duckysetup.sh
    ```
   or for oneliners (skip 4 and 5):
    ``` bash
    wget https://raw.githubusercontent.com/lucki1000/Raspberry-Pi-Zero-Rubber-Ducky-Duckberry-Pi/master/duckysetup.sh && chmod +x duckysetup.sh && sudo ./duckysetup.sh
4) Make the script executable
    ``` bash
    chmod +x duckysetup.sh
    ```
   
5) Run the script
    ``` bash
    sudo ./duckysetup.sh
    ```
### Using RubberDucky
   
6) Turn off the PI, plug it into the target host machine via USB cable in the peripheral micro USB port, NOT THE POWER PORT.  A power cord is not required as the Pi Zero will take power directly from the host machine.
    
7) Watch the script execute on the host machine - You may have to plug it in twice, the first time installs drivers.

8) Once the default script runs you can unplug and take the SD card out of the PI, plug it into any machine with a USB SD card adaptor and then change /boot/payload.dd file to any DuckyScript Payload. This is what file the Pi will inject into the target device.

## Duckyscript

There are lots of [ready made ducky scripts here](https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Payloads) and you can make your own with your brain or an generator.

The .dd file is a standard .txt file who is only the extension changed. To clear up some confusion, the DuckToolKit will give you an option to download a compiled inject.bin file or a duckycode.txt file. You need to download the duckycode.txt file and change the name/extension to payload.dd and then put it in the /boot part of the SD card so that the Pi can load and run the script.

## Credits

Authors:
lucki1000
      
Credits to Original Authors:
DroidDucky by Andrej Budincevic (https://github.com/anbud/DroidDucky)
hardpass by girst (https://github.com/girst/hardpass)

## Summary

Follow step 1 -5.

Then edit /boot/payload.dd with your script.

Then reboot/shutdown your Zero and plug it into your target with the otg port. (Not the power port on the Pi)

Then wait.

Good Luck :)


## MIT License

Copyright (c) [2018] [Zac Henry Orehawa]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
