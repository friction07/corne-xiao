# CORNE-XIAO

![corne-xiao](/rev2/docs/images/rev-2.jpg)

***

### Pcb 

[Here](/rev2/PCB/) you can find the Gerbers for the corne-xiao. 

***

### Case and Switch-plate

The pcb has the same dimensions and mounting points of the corne-cherry by foostan. So it will work with all the corne cases with the following constraint : **Since the controller is mounted facing up unlike the usual face-down style, make sure the case has clearance for the usb port**.

***

### Build Guide

While the build process is similar to most of the keyboards, the [build guide](/rev2/docs/buildguide.md) will be essential to solder jumpers and other stuff.

***

### Firmware

Firmware for both [5-col](/rev2/firmware/5-col/) and [6-col](/rev2/firmware/6-col/) has been shared which supports encoders on both half by default. 
If you are going for nice!view instead of encoder, you can find the firmware [here](https://github.com/sidx64/corne-zmk-enc-nview), courtesy of [sidx64](https://github.com/sidx64).
The uf2 folder contains ready to flash files for each half with an additional settings-reset file that might come in help if you are facing issues with bluetooth.
The default firmware and config uses a [zmk-rgbled-widget](https://github.com/caksoylar/zmk-rgbled-widget) made by the wonderful [caksoylar](https://github.com/caksoylar) to help with the bluetooth profile and battery status. In case you don't want to use the widget, you can remove `rgbled_adapter` from the build.yaml file in the zmk-config folder.
