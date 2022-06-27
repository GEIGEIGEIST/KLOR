# KLOR BUILD GUIDE (3DP CASE) [WIP]

## PART LIST

### REQUIRED PARTS

| Part name     | Count | Remarks | 
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

| Part name              | Count | Remarks | 
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

| Part name              | Count | Remarks | 
| ---                    | ---      | ---     |
| 3D printed case        | 02 | |
| acrylic parts          | 02 | Three parts and one ring per side |
| switch plate           | 02 | 1.5mm switch plate |
| 7mm M2 standoffs       | 16 | |
| 6mm M2 screws          | 16 | |
| 6mm M2 countersunk screws | 16 | The bottom only supports countersunk screws |


## INTRODUCTION

Here is an overview on which side each component needs to be soldered (you can click on the image to see a larger version).

![KLOR solder guide](/docs/images/solderguide_3DP.png)

Be aware that some components needs to be soldered on the opposite side for the stacked acrylic case.\
Some people like to mark top and bottom with masking tape to keep track of top and bottom, since the PCB is reversible.\
You should start with the lowest components and work your way to the higher components, ending with the OLEDs and the encoders.

***

## BREAK OFF PARTS (optional)

If you decided on [another layout](/README.md#layouts) than the Polydactyl you should remove the unnecessary parts. Use a flush cutter to snip through the support sections. You can also use a boxcutter to carve in grooves, which makes it easier to break on the right spot. 

> **Warning**
> Be very careful with this step, since there is a risk to break your PCB. Probably start with this step, since you won't loose all soldered parts if you really break the PCB.

![break off parts](/docs/images/buildguide/breakoff.jpg)


You can use a file to smooth out the edges, but you should wear a mask while doing this, since the FR4 dust is considered to be toxic.


***

## MICROCONTROLLER

> **Warning**
> First step should be to flash the microcontroller. This way you can make sure it works before soldering it in.

Unlike most boards the microcontroller needs to be mounted on the bottom, with the components facing upwards (to the PCB).\
You can choose the included header pins, but it's highly recommended to use MillMax low profile sockets.\
Place the sockets on the bottom side of the PCB in the marked spots.

![MCU sockets](/docs/images/buildguide/MCU_sockets.jpg)


You can keep them in place by using masking tape.

![sockets taped](/docs/images/buildguide/MCU_tape.jpg)


Then you can flip the board to solder in the sockets from the top.
Flip it again and insert the pins in the sockets.

> **Note**
> Use a plier to insert them. Don't use too much force, you will feel them snap in. After that you can carefully apply some pressure , using a flat object, to make sure they're fully seated. 

![MCU pins](/docs/images/buildguide/MCU_pins.jpg)


Now place your microcontroller on the pins (components facing the PCB) and solder it to the pins.\
You can use flush cutters to trim the header pins.

![MCU solder](/docs/images/buildguide/MCU_solder.jpg)


> **Warning**
> When trimming with flush cutters wear eye protection or hold your hand close above the pins. Otherwise the sharp metal pins will fly around and hurt you.


***

## DIODES

The diodes needs to be soldered on the bottomm of the PCB. Their orientation matters. They have a small line on one side, which should be on the side the arrow on the PCB is facing to.

<p align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/buildguide/diodes_dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/buildguide/diodes_bright.svg">
  <img alt="diode orientation" src="/docs/images/buildguide/diodes_dark.svg">
</picture>
</p>

Apply a small amount of solder on one pad.

![Solder on one pad](/docs/images/buildguide/diode_solder_pad.jpg)


Then use tweezers to place the diode on the pads and reheat the solder to secure the diode.

![Solder diode](/docs/images/buildguide/diode_in_place.jpg)


Now you can solder the second pad.

***

## LEDS (optional)

> **Note**
> If you use a layout with three thumbs, instead of four, you need to bridge the 'lost thumb?' jumper below the TRRS sockets, since the led chain lost its beginning. 

![Lost thumb jumper](/docs/images/buildguide/lostthumb.png)


LEDs are very heat sensitive. So it's a good idea to solder the pads on the PCB bottom first and then insert the LED.

![LED solder pads](/docs/images/buildguide/LED_solder_pads.jpg)


While the bottom of the PCB is facing you, insert the LEDs in the holes. The lens should face the table.

![LED in place](/docs/images/buildguide/LED_in_place.jpg)


Here you can see an image of the correct orientation.\
The L shaped pad on the LED needs to be connected to the square marked pad.

![LED orientation1](/docs/images/buildguide/LEDorientation.svg)


> **Note**
> While the orientation is the same on every half, it's different between both halves.

> **Warning**
> It's recommended to solder the LEDs in at 220º, since they're pretty sensitive to heat. Personally I had a hard time keeping it below 270º. So my advice would be to solder the first pad on every LED, while trying to be really quick. Then solder the second pad on every LED, starting with the first LED. This way they can cool down in the meantime.

Make sure the solder always builds a strong connection between the pad on the LED and the pad on the PCB.\
**IMAGE**

The advantage of soldering in the Microcontroller first is that you can occasionally check if all the LEDs work before continuing. 

![KLOR LED working](/docs/images/buildguide/LED_closeup.jpg)


This graphic shows in which order the LEDs are chained together.

![KLOR LED order](/docs/images/KLOR_LEDorder.png)


***

## SWITCH SOCKETS

Here you can use the same technique than the one used for the diodes: Apply some solder on one of the pads first.

![switch sockets pad](/docs/images/buildguide/switch_pad.jpg)


Than place the switch socket in the silk screen markings and reheat the solder. Make sure you apply some pressure with tweezers, so make sure the socket is fully seated.\
Now solder the second pad of the socket.

![switch socket soldered](/docs/images/buildguide/switchsocket.jpg)


***

## RESET SWITCHES

You soldered everything which goes on the bottom of the PCB. 
The reset switches are kinda fiddly to solder. 


***

## TRRS JACKS

Install the TRRS jack on the top side of the PCB. The place where you should insert it is marked with a white line.
You may want to use some masking tape to hold it in place, since you need to solder it on the bottom.

![TRRS jack taped](/docs/images/buildguide/TRRS_tape.jpg)

![TRRS jack soldered](/docs/images/buildguide/TRRS.jpg)


***

## HAPTIC FEEDBACK (optional)

> **Note**
> Currently haptic feedback only works on the primary side of your keyboard, which is a limitation of QMK.


Apply some solder to the jumpers on the top to bridge them.

![haptic feedback Jumper](/docs/images/buildguide/haptic_jumper.jpg)


Insert the module from below, with the motor facing upwards. Than insert the pin headers from below.\
**IMAGE**


Now you can solder the pins and use a flush cutter to snap of the excess. Again please hold your hand above them or wear eye protection while doing this.
You can also use a screw and a nut to stabilize the module further. But this step isn't necessary.

![haptic feedback solder](/docs/images/buildguide/haptic_solder.jpg)


***

## SPEAKER (optional)

> **Note**
> Currently haptic feedback only works on the primary side of your keyboard, which is a limitation of QMK. Unfortunately the audio feature of QMK doesn't work yet with the RP2040.

Soldering the speaker is pretty straight forwarded. Apply a tiny bit solder on one of the pads, use tweezers to hold the speaker in place and reheat the solder. Than apply solder to the other pad.

![speaker](/docs/images/buildguide/speaker.jpg)


***

## TRACKBALL (optional)
> **Note**
> While the hardware side should work fine, I still need to add the code for the trackball.

TBA

***

## ENCODERS

Mount the rotary encoder on the top side of the PCB. It should click into place and might require a firm press. If it's seated corretly solder the pins on the bottom.

![encoder](/docs/images/buildguide/encoder.jpg)


***

## OLEDs

> **Warning**
> Make sure the keyboard is fully functional before soldering the OLEDs, since they're the only components which covers pins, you can't access after the OLEDs are in place.


First step should be to bridge the jumpers on the top of the PCB, next to the OLED.

![OLED bridge jumpers](/docs/images/buildguide/OLED_bridge.jpg)


> **Note**
> The OLED needs to be as flush to the PCB as possible to fit under the switchplate.


You need to remove the plastic part from the headers, which is usually attached to the OLED, while keeping the pins. For me the easiest way is to use flush cutters to snap the plastic in half, which lets you remove the parts easily. You probably need to bend the pins back in place after doing this.

![OLED pin split](/docs/images/buildguide/OLED_split.jpg)


You also need to cover the back of the OLED with electrical tape, to prevent shorts with the microcontroller pins. Especially the top part with the copper traces is important.

![OLED tape on bottom](/docs/images/buildguide/OLED_tape_bottom.jpg)


Insert the OLED on the top of the PCB. Make sure it sits as flush to the PCB as possible. Maybe hold it in place with some masking tape.

> **Note**
> You could also temporarily install the switchplate over the OLED, using a few switches. This way you make sure it's exactly in the right spot and rotation.


Solder the OLED into place.

![OLED soldering](/docs/images/buildguide/OLED_solder.jpg)


Now use flush cutters to trim the top and bottom pins. Especially the top pins should be as short as possible to avoid interference with the switch plate.

![OLED flush cutter](/docs/images/buildguide/OLED_cutoff.jpg)


If you use a metal switch plate consider to cover them with electrical tape to prevent shorts.

![OLED tape on top](/docs/images/buildguide/OLED_tape_top.jpg)


> **Note**
> If you need to desolder the OLED or fix it's placement just apply a lot of solder to the four pins to connect them. This way you can heat all four pins at once and remove it by gently applying force to the bottom edge of the OLED module. Be really carefull not to apply to much pressure, since you could rip off a pad or destroy the OLED (which happens pretty fast).

![OLED desolder](/docs/images/buildguide/OLED_fix.jpg)


***

## CLEANING

This is how your finished PCB probably will look like. You can use an old toothbrush and some isopropanol to clean it from residues. 

![Finished PCB](/docs/images/buildguide/PCB_finished.jpg)


***

## FIRMWARE

### AVR based ProMicro 
**e.g. Pro Micro / Elite-C / Puchi-C**

If you not already flashed the firmware to the microcontroller you should do it know, to make sure everything works, before inserting it into the case.\
[Here](https://github.com/GEIGEIGEIST/qmk-config-klor) you can find the QMK firmware for the KLOR.\
Copy the **klor** folder into the **keyboards** directory of your qmk installation.\
Than use [QMK MSYS](https://msys.qmk.fm/) (or the command line tool of your choice) to compile it with this command.\

``qmk compile -kb klor -km default`` 

This will create a file called **klor_default.hex** in your **qmk_firmware** folder.\
Open [QMK Toolbox](https://github.com/qmk/qmk_toolbox) and locate the **klor_default.hex** file.\
Connect the ProMicro/keyboard and press the reset button (or connect the RST and GND pins on the ProMicro). QMK toolbox should show a connected device.\
Press **flash** in QMK toolbox to flash the firmware on your microcontroller.

![QMK toolbox](/docs/images/buildguide/qmk_toolbox.jpg)



### RP2040 ProMicro 
**e.g. Adafruit KB2040 / Sparkfun Pro Micro RP2040 / Boardsource Blok / Elite-Pi / Sea-Picro**

For now you can't use the official QMK version with the RP2040. Instead you should use [this PR](https://github.com/KarlK90/qmk_firmware/tree/feature/raspberry-pi-rp2040-support).\
Copy the **klor** folder into the **keyboards** directory of your qmk installation.\
Than use [QMK MSYS](https://msys.qmk.fm/) (or the command line tool of your choice) to compile it with this command.\

``qmk compile -kb klor/2040 -km default``

This will create a file called **klor_2040_default.uf2** in your **qmk_firmware** folder.\
The first time you need to keep boot pressed, than press reset and release boot. It will open the flash memory of your MicroController as device in your OS.\
Copy the **klor_2040_default.uf2** there to flash it. 

> **Note**
> After flashing the firmware the first time you can access the flash memory by double pressing the reset button on your keyboard or define a software reset key by using **QK_boot** as keycode.


***

## 3DP CASE

Here you can find the STL files for the case. I got them printed in PA12-HP Nylon (Multi Jet Fusion printing) by [JLCPCB](https://jlcpcb.com/3d-printing), which seemed pretty reasonably priced, for the level of detail.

![3DP case](/docs/images/buildguide/3DPcase.jpg)


Insert the PCB first. Starting with the inserting the microcontroller in the cutout at the top.

![3DP case insert MCU](/docs/images/buildguide/3DPcase_MCU.jpg)


Then lower it into the case. You probably need to bend the part of the case containing the holes for reset switch and TRRS jack a bit, to make it fit.

![3DP case bend](/docs/images/buildguide/3DPcase_finger.jpg)


The TRRS jack should snap in the provided hole.

![3DP case trrs](/docs/images/buildguide/3DPcase_trrs.jpg)


Insert the standoffs in the PCB and screw them into the bottom of the case using the countersunk screws.

![3DP case standoffs](/docs/images/buildguide/3DPcase_standoffs.jpg)


Now you can insert the plate and screw it to the case using the center standoff. 

![3DP case plate](/docs/images/buildguide/3DPcase_plate.jpg)


***

## ACRYLIC PARTS

Screw the acrylic parts on top of the plate.

 ![acrylic parts on top of plate](/docs/images/buildguide/3DPcase_acrylic.jpg)

***

## KNOBS

The design works best with 23mm (0.9") diameter encoder knobs. My recomendation would be a knob from kilo internationl which number starts with 90 (which means a 0.9" diameter) like the OEDNI-90-4-7 shown here.

![OEDNI-90-4-7](/docs/images/buildguide/knob.jpg)

***
