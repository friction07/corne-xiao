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
| Battery & Battery Connector | 02 | 3.7v lipo battery and S2B-PH-K-S connector |

Note: 
 - Use a battery with a built-in protection circuit.
 - You can always solder the battery directly and skip the connector. If opting for the connector, you'll need to use longer spacers to accommodate them below the pcb.
 - Only an encoder or an oled can be used due to limited space.
 - You can solder the power switch on either side of the pcb.

***

> **Warning**
> This guide assumes you are capable of soldering the diodes, hotswap sockets, power button, encoder and mcu sockets yourself. You can find videos/guides about these stuff very easily. I have only shared some of the extra things you need to take care of.

***

#### Pads at the back

We have to solder 3 diode legs to the 3 pads at the back of the xiao. The pads being *BAT+* and the two *NFC* pads at the corner. The other battery pad is ignored as it is internally connected to *GND* pin.
**_You can skip soldering one of the NFC pads if you are not going to use nice!views. Check the "CS" label on the pcb to know which._**

- **Tin the pads**

![tin the pads](/rev1/docs/images/mcu1.jpg)

- **Solder the diode legs**

![solder the legs](/rev1/docs/images/mcu2.jpg)

> **Warning**
> Use low temperature for this (I used 260 C). Hold the legs with help of tweezers. Flux will help a lot. Try to make the legs straight which shouldn't be difficult as they are easy to bend. **Do not overheat or use excess force or you may end up lifting the pads**.
I soldered multiple xiao like this. It looks scary at first but it just needs patience.

- **Push the controller carefully in the pcb**

![push it in](/rev1/docs/images/mcu3.jpg)

- **Solder these legs to the pcb**

![solder the three legs](/rev1/docs/images/mcu4.jpg)

Yes, this will make the controller non-removable. You can use pogo pins instead but I wasn't able to find them locally, so I went this route.

### Encoder

Before soldering the encoder, make sure the bottom is non-conductive. Since my encoders had a metallic bottom, I used a piece of kapton tape over the oled header.

![encoder](/rev1/docs/images/enc.jpg)

***

### FINAL LOOK

Congrats! You did it.

![final look](/rev1/docs/images/final.jpg)
