# BUILD GUIDE

### List of parts

| Part name     | Count | Remarks | 
| :------------ | :---: | :------ |
| Seeed Studio XIAO nRF52840  | 02 | https://www.seeedstudio.com/Seeed-XIAO-BLE-nRF52840-p-5201.html |
| Hotswap socket              | 42 | Hotswap sockets for MX-style |
| Diodes 1N4148W              | 44 | Surface mount diodes in SOD123 package |
| EC11 encoder                | 02 | 20 steps, 20 detent Bourns encoder are recommended. You can read more about it here [(Quadrature) Encoders](https://kbd.news/Designing-for-Wireless-1784.html)|
| OLED                        | 02 | [Nice!view](https://nicekeyboards.com/nice-view) is recommended |
| MCU sockets                 | 04 | For socketing your MCU |
| MCU pins and/or diodes      |    | For the pins and the pads at the back, I used diode legs. More on this later |
| Power Button                | 02 | MSK12C02 SMD Toggle Slide Switch |
| Battery & Battery Connector | 02 | 3.7v lipo battery and S2B-PH-K-S |

Note: 
 - Use a battery with a built-in protection circuit.
 - You can directly solder the battery to the large BAT pad(just below the oled connector). If opting for the connector, you may need to use longer spacers to accommodate them below the pcb.
 - Only an encoder or an oled can be used due to limited space.
 - You can solder the power switch on either side of the pcb but I have tested it only on the back side.
 - **Shared below are the steps to build the LEFT HALF. Since the pcb is reversible, you can just repeat these but on the opposite side to make a right half.**

### PCB Layout
**Back / Left Side of PCB**

![Left](/rev2/docs/images/pcbl.png)

**Front / Right Side of PCB**

![Right](/rev2/docs/images/pcbr.png)

***

> **Warning**
> This guide assumes you are capable of soldering the diodes, hotswap sockets, power button, encoder and mcu sockets yourself. You can find videos/guides about these stuff very easily. I have only shared some of the extra things you need to take care of.

***

### Preparing the controller

We have to solder 3 diode legs to the 3 pads at the back of the xiao. The pads being *BAT+* and the two *NFC* pads at the corner. The other battery pad is ignored as it is internally connected to *GND* pin.
> **Note**
> You can skip soldering both NFC pads if you are building a 5 column corne with encoders, since one of the pad is used for 6th col and one for CS pin of nice!view oled. These pins have been marked as "6" and "CS" on the PCB for reference.

- **Tin the pads**

![tin the pads](/rev1/docs/images/mcu1.jpg)

- **Solder the diode legs**

![solder the legs](/rev1/docs/images/mcu2.jpg)

> **Warning**
> Use low temperature for this (I used 260 C). Hold the legs with help of tweezers. Flux will help a lot. Try to make the legs straight which shouldn't be difficult as they are easy to bend. **Do not overheat or use excess force or you may end up lifting the pads**.
I soldered multiple xiao like this. It looks scary at first but it just needs patience.

### Jumpers

- Bridge jumpers on the opposite side for the xiao-ble that is if the xiao is mounted on the front, bridge the jumpers on the back.
- Bridge jumpers on the same side for battery connector.
- Bridge Jumpers on the same side for oled connector (only if you are using oled instead of encoder).

|     Backside of the left half     | Bridge the two jumpers for battery connector | Bridge the 10 jumpers for controller(xiao-ble) | Final look after soldering the battery connector and mcu sockets |
| :-------------------------------: | :------------------------------------------: | :--------------------------------------------: | :--------------------------------------------------------------: |
| ![](rev2/docs/images/Jumper1.jpg) |       ![](rev2/docs/images/Jumper2.jpg)      |       ![](rev2/docs/images/Jumper3.jpg)        |              ![](rev2/docs/images/Jumper4.jpg)                   |

### Solder the controller

- **Push the controller carefully in the pcb**
The image is from rev1 but the process is same for rev2

![push it in](/rev1/docs/images/mcu3.jpg)

- **Solder these legs to the pcb**

![solder the three legs](/rev2/docs/images/solder-xiao.jpg)

Yes, this will make the controller non-removable. You can use pogo pins instead but I wasn't able to find them locally, so I went this route.

### Encoder

Before soldering the encoder, make sure the bottom is non-conductive. Since my encoders had a metallic bottom, I used a piece of kapton tape over the jumpers for oled.

![encoder](/rev2/docs/images/encoder.jpg)

***

### Final look of the left half

Front
![left-half front side](/rev2/docs/images/final-front.jpg)
Back
![left-half back side](/rev2/docs/images/final-back.jpg)

### Both halves together 

Here's how both the halves should look once you are done:

|                 Front                 |                 Back                 |
| :-----------------------------------: | :----------------------------------: |
| ![](/rev2/docs/images/both-front.jpg) | ![](/rev2/docs/images/both-back.jpg) |
