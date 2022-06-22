# KLOR BUILD GUIDE (3DP CASE) [WIP]

## PART LIST

### REQUIRED PARTS

| Part name     | Quantity | Remarks | 
| ---           | ---      | ---     |
| KLOR PCB      | 02 |         |
| ProMicro      | 02 | Alternatively you can use another controller, with a similar pinout like the Elite-C, Puchi-C, KB2040 dda. |
| MX Key switch | 42 | 40 switches for Konrad / 38 switches for Yubitsume / 36 switches for Saegewerk |
| switch socket | 42 | 40 sockets for Konrad / 38 sockets for Yubitsume / 36 sockets for Saegewerk |
| diodes 1N4148W| 44 | They are surface mount diodes in SOD123 package. 42 for Konrad / 40 for Yubitsum / 38 for Saegewerk |
| 1u MX keycaps | 42 | 40 keycaps for Konrad / 38 keycaps for Yubitsume / 36 keycaps for Saegewerk |
| OLED module   | 02 | SSD1306 128x64 pixel OLED Displays |
| reset button  | 02 | Alps SKRTLAE010 |
| TRRS jack     | 02 | |
| TRRS cable    | 01 | Alternatively you can use a TRS cable for [half-duplex](https://github.com/qmk/qmk_firmware/blob/master/docs/serial_driver.md#usart-half-duplex)|
| EC11 encoder  | 02 | You can use any EC11 encoder, but it will look better if you use a short one, like the EC11N1524402 |
| encoder knob  | 02 | The design works best with a 2,2cm encoder knob. I recommend kilo international knobs with a number starting with 90. 
| USB cable     | 01 | For connecting the keyboard with your PC |


### OPTIONAL PARTS

| Part name              | Quantity | Remarks | 
| ---                    | ---      | ---     |
| MCU sockets            | 04 | For socketing your MCU. Highly recommended |
| MCU pins               | 48 | In combinatin with the MCU sockets |
| SK6812 Mini LED        | 42 | 40 LEDs for Konrad / 38 LEDs for Yubitsume / 36 LEDs for Saegewerk |
| [Haptic Feedback Module](https://shop.pimoroni.com/products/drv2605l-linear-actuator-haptic-breakout) | 01 | Pimoroni Haptic Buzz |
| speaker                | 01 | Mallory AST1109MLTRQ or Keliking KLJ-1102 |
| [trackball](https://bit-trade-one.co.jp/selfmadekb/adtb7m/) | 01 | Pixart PAW3204OA. You can get it from [Yushakobo](https://shop.yushakobo.jp/products/adtb7m) |
| [level converter](https://github.com/sekigon-gonnoc/LevelConverterForTrackballModule) | 01 | Needed to use the trackball. You can get it from [Yushakobo](https://shop.yushakobo.jp/products/a0800tl-01-1/) |
| [tenting puck](https://splitkb.com/products/tenting-puck)| 02 | SplitKB Tenting Puck |


### 3DP CASE PARTS

| Part name              | Quantity | Remarks | 
| ---                    | ---      | ---     |
| 3D printed case        | 02 | |
| acrylic parts          | 02 | Three parts and one ring per side |
| switch plate           | 02 | 1.5mm switch plate |
| 7mm M2 standoffs       | 16 | |
| 6mm M2 screws          | 16 | |
| 6mm M2 countersunk screws | 16 | The bottom only supports countersunk screws |


## INTRODUCTION

Here you can see an overview on which side each component needs to be soldered. Be aware that some components needs to be soldered on the opposite side for the stacked acrylic case.\
Some people like to mark top and bottom with masking tape to keep track of top and bottom, since the PCB is reversible.

![KLOR solder guide](/docs/images/solderguide_3DP.png)

## BREAK OFF PARTS (optional)

If you decided on [another layout](/README.md#layouts) than the Polydactyl you should remove the unnecessary parts. 