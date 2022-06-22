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

Here you can see an overview on which side each component needs to be soldered (you can click on the image so see a larger version of it).

![KLOR solder guide](/docs/images/solderguide_3DP.png)

Be aware that some components needs to be soldered on the opposite side for the stacked acrylic case.\
Some people like to mark top and bottom with masking tape to keep track of top and bottom, since the PCB is reversible.\
Generally speaking you should start with the lowest components and work your way to the higher components, ending with the OLEDs and the encoders.

## BREAK OFF PARTS (optional)

If you decided on [another layout](/README.md#layouts) than the Polydactyl you should remove the unnecessary parts. Use a flush cutter to snip through the support sections. Alternatively you can use a boxcutter to carve in grooves, which makes it easier to break on the right spot. 

> **Warning**
> Be very careful with this step, since there is a risk to break your PCB. You should consider to do this first, since you won't loose all soldered parts if you really break the PCB.

**IMAGE**


## MICROCONTROLLER

> **Warning**
> First step should be to flash the microcontroller. This way you can make sure it works before soldering it in. Another advantage is that you can confirm the LEDs work, while soldering them.

Unlike most boards the microcontroller needs to be mounted on the bottom, with the components facing upwards (to the PCB).\
You can choose the included header pins, but it's highly recommended to use MillMax low profile sockets.\
Place the sockets on the bottom side of the PCB in the marked spots.\
**IMAGE**

You can keep them in place by using masking tape.\
**IMAGE**

Than you can flip the board to solder in the sockets from the top.
Than flip it again and insert the pins in the sockets.

> **Note**
> Use a plier to insert them. Don't apply to much force, you'll will feel if they're snap in. After snapped in you can carefully apply some pressure from above, using a flat object, to make sure they're fully seated. 

**IMAGE**

Now place your microcontroller on the pins (components facing the PCB) and solder it to the pins.\
**IMAGE**



## LEDS (optional)

While the bottom of the PCB is facing you insert the LEDs in the holes with the glass part away from you.\
**IMAGE**

Here you can see an image of how the LEDs needs to be rotated.\
**IMAGE**\
The L shaped pad on the LED needs to be connected to the pad on the PCB marked with a square. 
> **Note**
> Note that while the orientation is the same on every half it's different between both halves.

> **Warning**
> It's recommended to solder the LEDs in at 220º, since they can't handle heat very good. Personally I had a hard time keeping it below 270º. So my advice would be to solder the first pad on every LED, while trying to be really quick. Than do the second pad, starting at the first LED. This way they can cool down in the meantime.

**IMAGE**

The advantage of soldering in the Microcontroller first is that you can occasionally check if all the LEDs work before continuing. Here you can find the order in which the LEDs are chained together.

![KLOR LED order](/docs/images/KLOR_LEDorder.png)

> **Note**
> If you use a layout with three thumbs instead of four you need to bridge the 'lost thumb?' jumper below the TRRS sockets, since the led chain lost its beginning. 
![Lost thumb jumper](/docs/images/buildguide/lostthumb.png)


## DIODES

## SWITCH SOCKETS

## RESET SWITCHES

## TRRS SOCKETS

## HAPTIC FEEDBACK (optional)

## SPEAKER (optional)

## TRACKBALL (optional)

## OLEDs

> **Warning**
> Be sure you make sure the keyboard is fully functional before soldering the OLEDs, since they are the only components which covers pins, you can't access after the OLEDs are in place.

## ENCODERS

## 3DP CASE

## ACRYLIC PARTS

## FIRMWARE







> **Note**
> This is a note

> **Warning**
> This is a warning