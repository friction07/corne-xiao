# CORNE-XIAO

![corne-xiao](/rev1/docs/images/corne_wireless.jpg)

***

### Pcb 

[Here](/PCB/) you can find the Gerbers for the corne-xiao. 

***

### Case and Switch-plate

The pcb has the same dimensions and mounting points of the corne-cherry by foostan. So it will work with all the corne cases with the following constraint : **Since the controller is mounted facing up unlike the usual face-down style, make sure the case has clearance for the usb port**.

***

### Build Guide

While the build process is similar to most of the keyboards, I have shared a guide with some images and details of parts [here](/rev1/docs/buildguide.md).

***

### Firmware

You can find [zmk-config](/firmware/zmk-config) which supports encoders on both half by default. If you are planning to put an oled instead, you can look at [Jon's config](https://github.com/JonMuller/gerbers/tree/main/corne-choc-xiao/zmk_starter).
The [uf2](/firmware/uf2/) folder contains ready to flash files for each half with an additional settings-reset file that might come in help if you are facing issues with bluetooth.
The default firmware and config uses a [rgb-led-widget](https://github.com/caksoylar/zmk-config/tree/main/config/boards/shields/rgbled_widget) made by the wonderful [caksoylar](https://github.com/caksoylar) to help with the bluetooth profile and battery status. In case you don't want to use the widget, you can remove `rgbled_widget` from the [build.yaml](/firmware/zmk-config/build.yaml) for each half.

***

### Choc Version

Jon Muller's [corne-choc-xiao](https://github.com/JonMuller/gerbers/tree/main/corne-choc-xiao) inspired me to make this. He did an amazing job with it and I just took it a step further to make an mx variant with encoders.
