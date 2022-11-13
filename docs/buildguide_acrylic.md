# KLOR BUILD GUIDE (STACKED ACRYLIC CASE) [WIP]

## PART LIST

### REQUIRED PARTS

| Part name     | Count | Remarks | 
| :------------ | :---: | :------ |
| KLOR PCB      | 02 | You can find the files for it [here](/PCB/) |
| ProMicro      | 02 | Alternatively, you can use another controller with a similar pinout like the Elite-C, Puchi-C, KB2040 dda. |
| MX Key switch | 42 | 40 switches for Konrad / 38 switches for Yubitsume / 36 switches for Saegewerk |
| switch socket | 42 | 40 sockets for Konrad / 38 sockets for Yubitsume / 36 sockets for Saegewerk |
| diodes 1N4148W| 44 | These are surface mount diodes in SOD123 package. 42 for Konrad / 40 for Yubitsume / 38 for Saegewerk |
| 1u MX keycaps | 42 | 40 keycaps for Konrad / 38 keycaps for Yubitsume / 36 keycaps for Saegewerk |
| OLED module   | 02 | SSD1306 128x64 pixel OLED Displays |
| reset button  | 02 | Alps SKRTLAE010 |
| TRRS jack     | 02 | MJ-4PP-9 or PJ320A |
| TRRS cable    | 01 | Alternatively, you can use a TRS cable for [half-duplex](https://github.com/qmk/qmk_firmware/blob/master/docs/serial_driver.md#usart-half-duplex)|
| EC11 encoder  | 02 | You can use any EC11 encoder, but it will look better if you use a short one, like the EC11N1524402 |
| encoder knob  | 02 | The design works best with a 2,2cm encoder knob. I'd recommend kilo international knobs with a number starting with 90. You could also use the [knob](/knob/) I designed for the KLOR, based on the kilo knob. 
| USB cable     | 01 | For connecting the keyboard with your PC |


### OPTIONAL PARTS

| Part name              | Count | Remarks | 
| :--------------------- | :---: | :------ |
| MCU sockets            | 04 | For socketing your MCU. Highly recommended |
| MCU pins               | 48 | In combinatin with the MCU sockets |
| SK6812 Mini LED (not Mini-E)        | 42 | 40 LEDs for Konrad / 38 LEDs for Yubitsume / 36 LEDs for Saegewerk |
| [Haptic Feedback Module](https://shop.pimoroni.com/products/drv2605l-linear-actuator-haptic-breakout) | 01 | Pimoroni Haptic Buzz |
| speaker                | 01 | Mallory AST1109MLTRQ or Keliking KLJ-1102 |
| [trackball](https://bit-trade-one.co.jp/selfmadekb/adtb7m/) | 01 | Pixart PAW3204OA. Available at [Yushakobo](https://shop.yushakobo.jp/products/adtb7m) |
| [level converter](https://github.com/sekigon-gonnoc/LevelConverterForTrackballModule) | 01 | Needed to use the trackball. You can get it from [Yushakobo](https://shop.yushakobo.jp/products/a0800tl-01-1/) |
| [tenting puck](https://splitkb.com/products/tenting-puck)| 02 | SplitKB Tenting Puck |


### ACRYLIC CASE PARTS

| Part name              | Count | Remarks | 
| :--------------------- | :---: | :------ |
| acrylic parts          | 02 | Find the case files [here](/case/acrylic/) |
| switch plate           | 02 | 1.5mm switch plate |
| 9mm M2 standoffs       | 22 | Up to 22 9mm round standoffs for the actual case (check the appropiate puzzleguide) |
| 7mm M2 standoffs       | 12 | 7mm round standoffs for holding the PCB in place |
| 6mm M2 screws          | 56 | Up to 56 regular 6mm M2 screws (check the appropiate puzzleguide) |
| 5mm M2 wafer head screws | 12 | These screws need a flat head to fit under the acrylic top layer |


## INTRODUCTION

Here is an overview of where and on which side each component needs to be soldered (click on the image to see a larger version).

![KLOR solder guide](/docs/images/solderguide_acrylic.png)

To see what component needs to sit where you can take a look at the [interactive HTML BOM](https://htmlpreview.github.io/?https://github.com/GEIGEIGEIST/KLOR/blob/main/docs/klor_rev1-3_ibom.html).

> **Warning**
> This interactive HTML BOM does show where each component is located, but please still refer to the solder guide above to see if a component needs to go on the top or bottom of the PCB.

Be aware that for the 3D printed case some components need to be soldered on the opposite side.\
Some people mark the top and bottom with tape to keep track of which side is which, as the PCB is reversible.\
Beginn with the flat components and progress to the higher ones, ending with the OLEDs and the encoders.

***

## BREAK OFF PARTS (optional)

If you choose a layout [other than](/README.md#layouts) Polydactyl you should remove the unnecessary parts. Use a flush cutter to snip through the support sections. You can also use a boxcutter to carve in grooves, which makes it easier to break on the right spot. 

> **Warning**
> Be very careful with this step, since there is a risk to break the PCB. Probably it would be best to beginn with this step, to avoid loosing already soldered parts.

![break off parts](/docs/images/buildguide/breakoff.jpg)


You can use a file to smooth out the edges, but you should wear a mask while doing this, since the FR4 dust is considered to be toxic.

***

## MICROCONTROLLER

> **Warning**
> First flash the microcontroller to make sure it works, before soldering it in.

Unlike most other boards here the microcontroller needs to be mounted on the bottom, with the components facing upwards (to the PCB).\
Feel free to use the included header pins, but it's highly recommended to use MillMax low profile sockets.\
Place the sockets in the marked spots on the bottom side of the PCB.

![MCU sockets](/docs/images/buildguide/MCU_sockets.jpg)


You can keep them in place by using masking tape.

![sockets taped](/docs/images/buildguide/MCU_tape.jpg)


Then you can flip the board to solder in the sockets from the top.
Flip it again and insert the pins into the sockets.

> **Note**
> Use tweezers to insert them. Don't apply too much force, you will feel them snap in. After that, you can carefully apply some pressure, using a flat object to make sure they're fully seated. 

![MCU pins](/docs/images/buildguide/MCU_pins.jpg)


Now place your microcontroller on the pins (components facing the PCB) and solder it to them.\
You can use flush cutters to trim the header pins.

![MCU solder](/docs/images/buildguide/MCU_solder.jpg)


> **Warning**
> When trimming with flush cutters wear eye protection or hold your hand close above the pins. Otherwise sharp metal pins flying around might hurt you.

***

## LEDS (optional)

> **Note**
> If you use a layout with three thumbs, instead of four, you need to bridge the 'lost thumb?' jumper below the TRRS sockets on the primary and secondary PCB, since the led chain lost its beginning. 

![Lost thumb jumper](/docs/images/buildguide/lostthumb.png)


LEDs are very heat sensitive. So it's a good idea to solder the pads on the PCB bottom first and then insert the LED.

![LED solder pads](/docs/images/buildguide/LED_solder_pads.jpg)


While the bottom of the PCB is facing you, insert the LEDs in the holes. The lens should face the table.

![LED in place](/docs/images/buildguide/LED_in_place.jpg)


This image depicts the correct orientation.\
The L shaped pad on the LED need to be connected to the square marked pad.

![LED orientation1](/docs/images/buildguide/LEDorientation.svg)


> **Note**
> While the orientation is uniform within a half, it differs between left and right.

> **Warning**
> It's recommended to solder the LEDs in at 220º, since they're pretty heat sensitive. Personally, I had a hard time keeping it below 270º. So my advice would be while soldering the first pad on every LED, try to be really quick. Then solder the second pad on every LED, starting with the first LED. This way they can cool down in the meantime.

Make sure the solder always builds a strong connection between the pad on the LED and the pad on the PCB. 

![LED connection](/docs/images/buildguide/LED_soldered.jpg)


The advantage of soldering in the microcontroller first is that you can occasionally check if all the LEDs work before continuing. 

![KLOR LED working](/docs/images/buildguide/LED_closeup.jpg)


This graphic shows the order in which the LEDs are chained together.

![KLOR LED order](/docs/images/KLOR_LEDorder.png)

***

## DIODES

The diodes needs to be soldered on the bottomm of the PCB. Pay attention to their orientation:  They have a small line on one side, which should be on the side the arrow on the PCB is facing to.

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

## SWITCH SOCKETS

Here you can apply the same technique as used for the diodes: Apply some solder on one of the pads first.

![switch sockets pad](/docs/images/buildguide/switch_pad.jpg)


Then place the switch socket in the silk screen markings and reheat the solder. Apply some pressure with a pair of tweezers to make sure the socket is fully seated.\
Now solder the second pad.

![switch socket soldered](/docs/images/buildguide/switchsocket.jpg)

***

## RESET SWITCHES

The reset switches are a bit fiddly to solder. It helps to apply a really thin film of solder to the pads first. Then hold the switch in place with tweezers and solder the big pads on the left and right of the switch (they do not fulfill any electrical purpose, but serve to hold the switches in place). If the switch is seated corretly reheat the solder pads under the switch to connect it. 

![reset switch](/docs/images/buildguide/reset_switch.jpg)

***

## TRRS JACKS

Install the TRRS jack on the bottom side of the PCB. The place where you should insert it is marked with a white line.
You may want to use some masking tape to hold it in place, since you need to solder it on the bottom.

![TRRS jack taped](/docs/images/buildguide/TRRS_tape.jpg)

![TRRS jack soldered](/docs/images/buildguide/TRRS.jpg)


***

## HAPTIC FEEDBACK (optional)

> **Note**
> Currently, haptic feedback only works on the primary side of your keyboard, which is a limitation of QMK.


Apply some solder to the jumpers on the top to bridge them.

![haptic feedback Jumper](/docs/images/buildguide/haptic_jumper.jpg)


Insert the module from below with the motor facing upwards. Then insert the pin headers from below.

![haptic feedback pins](/docs/images/buildguide/haptic_pins.jpg)


Now you can solder the pins and use a flush cutter to snap of the excess. Remember to hold your hand above them or wear eye protection while doing so.

![haptic feedback snap of pins](/docs/images/buildguide/haptic_snap.jpg)


You can also use a screw and a nut to stabilize the module further. But this step is optional.

![haptic feedback solder](/docs/images/buildguide/haptic_solder.jpg)


***

## SPEAKER (optional)

> **Note**
> Currently haptic feedback only works on the primary side of your keyboard, which is a limitation of QMK. Unfortunately, the audio feature of QMK doesn't work yet with the RP2040.

Soldering the speaker is pretty simple. Apply a tiny bit solder on one of the pads, use tweezers to hold the speaker in place and reheat the solder. After that apply solder to the other pad.

![speaker](/docs/images/buildguide/speaker.jpg)


***

## TRACKBALL (optional)
> **Note**
> While the hardware side should already work fine, I still need to add the code for the trackball.

TBA

***

## ENCODERS

Mount the rotary encoder on the top side of the PCB. It should click into place maybe requiring a firm press. If it's seated correctly solder the pins on the bottom.

![encoder](/docs/images/buildguide/encoder.jpg)


***

## OLEDs

> **Warning**
> Make sure the keyboard is fully functional before soldering the OLEDs, since they're the only components which cover pins, you won't be able to access once they are in place.


First step should be to bridge the jumpers on the top of the PCB next to the OLED.

![OLED bridge jumpers](/docs/images/buildguide/OLED_bridge.jpg)


> **Note**
> The OLED needs to be as flush to the PCB as possible to fit under the switchplate.


You need to remove the plastic part, which is usually attached to the OLED, from the headers, while keeping the pins. For me the easiest way is to use flush cutters to snap the plastic in half, which allows you to remove the parts easily. You probably need to bend the pins back in place after doing this.

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
> If you need to desolder the OLED or fix its placement just apply a lot of solder to the four pins to connect them. This way you can heat all four pins at once and remove it by gently applying force to the bottom edge of the OLED module. Be really carefull not to use too much pressure, since you could rip off a pad or destroy the OLED (which happens pretty fast).

![OLED desolder](/docs/images/buildguide/OLED_fix.jpg)


***

## CLEANING

This is how your finished PCB probably will look like. You can use an old toothbrush and some isopropanol to clean it from residues. 

![Finished PCB](/docs/images/buildguide/PCB_finished.jpg)
***IMAGE***

***

## FIRMWARE

### AVR based ProMicro 
**e.g. Pro Micro / Elite-C / Puchi-C**

If you have not already flashed the firmware to the microcontroller you should do it now, to make sure everything works, before inserting it into the case.\
[Here](https://github.com/GEIGEIGEIST/qmk-config-klor) you can find the QMK firmware for the KLOR.\
Copy the **klor** folder into the **keyboards** directory of your qmk installation.\
Then use [QMK MSYS](https://msys.qmk.fm/) (or the command line tool of your choice) to compile it with this command:

``qmk compile -kb klor -km default`` 

This will create a file called **klor_default.hex** in your **qmk_firmware** folder.\
Open [QMK Toolbox](https://github.com/qmk/qmk_toolbox) and locate the **klor_default.hex** file.\
Connect the ProMicro/keyboard and press the reset button (or connect the RST and GND pins on the ProMicro). QMK toolbox should show a connected device.\
Press **flash** in QMK toolbox to flash the firmware on your microcontroller.

![QMK toolbox](/docs/images/buildguide/qmk_toolbox.jpg)



### RP2040 ProMicro 
**e.g. Adafruit KB2040 / Sparkfun Pro Micro RP2040 / Boardsource Blok / Elite-Pi / Sea-Picro**

Copy the **klor** folder into the **keyboards** directory of your qmk installation.\
Then use [QMK MSYS](https://msys.qmk.fm/) (or the command line tool of your choice) to compile it with this command:

``qmk compile -kb klor/rp2040 -km default``

This will create a file called **klor_rp2040_default.uf2** in your **qmk_firmware** folder.\
The first time you need to keep boot pressed, then press reset and release boot. This will open the flash memory of your MicroController as device in your OS.\
Copy the **klor_rp2040_default.uf2** there to flash it. 

> **Note**
> After flashing the firmware the first time you can access the flash memory by double pressing the reset button on your keyboard or define a software reset key by using **QK_boot** as keycode.


***

## STACKED ACRYLIC CASE

> **Note**
> Since there are a lot of different parts please check the 'puzzle guide' which you can find in the same folder than the case files of your layout. 

Screw the standoffs onto the bottom plate. You can find the locastion of the 7mm standoffs and 9mm standoffs in the 'puzzle guide', but as a rule of thumb the 9mm standoffs should be on the outside, holding the case parts, while the 7mm standoffs will hold the PCB and switchplate.\
(The dark shapes on the bottom are pieces of deskmat, I use as bumpers.) 

![acrylic bottom](/docs/images/buildguide/acrylic_bottom.jpg)


Next you should align the parts of the first layer to the outer standoffs. The parts for the left and right case are interchangeable.

![acrylic first layer](/docs/images/buildguide/acrylic_first_layer.jpg)


Now you can insert the PCB and add the other layers.

![acrylic all layers](/docs/images/buildguide/acylic_all_layers.jpg)


 Align the plate and screw them to the center standoffs.

 ![acrylic switchplate](/docs/images/buildguide/acrylic_plate.jpg)


For this step you need the 5mm wafer head screws, since other screwheads would intersect with the top layer.

![wafer head screws](/docs/images/buildguide/flat_screws.jpg)


Finally attach the top plate and insert the switches into the plate.

![acrylic top plate](/docs/images/buildguide/acrylic_topplate.jpg)


***

## KNOBS

The design works best with 23mm (0.9") diameter encoder knobs. My recomendation would be a knob from kilo internationl with a number beginning with 90 (which means a 0.9" diameter) like the OEDNI-90-4-7 shown here.

![OEDNI-90-4-7](/docs/images/buildguide/knob.jpg)

***

## FINAL BUILD

This is how the final keyboard will look like. In this picture you see the KLOR saegewerk, with RAMA Grid keycaps in NOCT.

![KLOR acrylic case](/docs/images/buildguide/acrylic_case.jpg)
