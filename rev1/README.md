# CORNE-XIAO

![corne-xiao](/rev1/docs/images/rev-1.jpg)

***

### Pcb 

[Here](/rev1/PCB) you can find the Gerbers for the corne-xiao. 

***

### Case and Switch-plate

The pcb has the same dimensions and mounting points of the corne-cherry by foostan. So it will work with all the corne cases with the following constraint : **Since the controller is mounted facing up and is different from pro micro, make sure the case has clearance for the usb port**.

_Corne v4 plates/cases will not fit as it has different spacing from the previous versions._

I have also shared files for a case that I personally use [here](/case).

***

### Build Guide

While the build process is similar to most of the keyboards, I have shared a guide with some images and details of the parts [here](/rev1/docs/buildguide.md).

***

### Firmware

You can find the zmk-config [here](https://github.com/friction07/zmk-config-corne-xiao). ZMK Studio support is enabled by default. Ensure you flash the v1 firmware for the Rev1 PCB and the v2 firmware for the Rev2 PCB.

By default, the firmware uses a [zmk-rgbled-widget](https://github.com/caksoylar/zmk-rgbled-widget) made by [caksoylar](https://github.com/caksoylar) to help with the bluetooth profile and battery status. In case you don't want to use the widget, you can remove the keyword `rgbled_adapter` from `build.yaml`.
