<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/klor-font-logo-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/klor-font-logo-bright.svg">
  <img alt="KLOR logo font" src="/docs/images/klor-font-logo-bright.svg">
</picture>

# KLOR SPLIT KEYBOARD

KLOR is a 36-42 key column-staggered split keyboard. It supports a per-key RGB matrix, encoders, OLED displays, haptic feedback, speakers, a Pixart Paw3204 trackball, the [SplitKB tenting puck](https://splitkb.com/products/tenting-puck), and four different layouts, through break-off parts.

***

## LAYOUTS

![KLOR layouts](/docs/images/klor-layouts.svg)

***

## IMAGES

![KLOR polydactyl](/docs/images/KLOR_polydactyl_DES01.jpg)

![KLOR polydactyl](/docs/images/KLOR_polydactyl_DES02.jpg)

▲ KLOR polydactyl with 3DP case and DES keycaps.

***

![KLOR saegewerk](/docs/images/KLOR_saegewerk_GRID01.jpg)

![KLOR saegewerk](/docs/images/KLOR_saegewerk_GRID02.jpg)

▲ KLOR saegewerk with stacked acrylic case and GRID keycaps.

***

## PCB 

[Here](/PCB/) you can find the KiCad files and Gerbers for the KLOR. 

***

## CASE

[Here](/case/) are the case files for the KLOR. There is an acrylic case and a 3D printed case (which uses acrylic too) for every layout.

***

## SWITCHPLATE

In every case directory you'll find the matching switchplates as **.dxf**, **.svg**, **.stl**, and a **.zip**-file, containing gerber files for a FR4 plate.

***

## KNOB

You can use pretty much any knob, which works with the EC11 encoder, but [here](/knob/) you can find one, I designed for the KLOR.

***

## BUILD GUIDE

Here you can find the build guides for the KLOR.\
[KLOR build guide 3DP case](/docs/buildguide_3DP.md) (QMK)\
[KLOR build guide stacked acrylic case](/docs/buildguide_acrylic.md) (QMK)\
[KLOR BLE build guide 3DP case](/docs/buildguide_3DP_ble.md) (ZMK)\
[KLOR BLE build guide stacked acrylic case](/docs/buildguide_acrylic_ble.md) (ZMK)

***

## FIRMWARE

[QMK config](https://github.com/GEIGEIGEIST/qmk-config-klor) (supports OLED, encoders, LEDs, haptic feedback and speakers)\
[ZMK config](https://github.com/GEIGEIGEIST/zmk-config-klor) (supports OLED, encoder, LEDs and Bluetooth)\
[KMK config](https://github.com/moritz-john/kmk-config-klor) (supports OLED, encoders, LEDs and speakers) made by [Moritz John](https://github.com/moritz-john)\
Thanks to [Manna Harbour](https://github.com/manna-harbour) you can find KLOR in [Miryoku ZMK](https://github.com/manna-harbour/miryoku_zmk)

***

## CHOC/KS27 VERSION

[Sadek Baroudi](https://github.com/sadekbaroudi) did an amazing job in creating a version of the KLOR which supports KS-27 and Choc V1 switches. Including a special case for it.\
[KLOR Sadek KS-27 and Choc V1 mod](https://github.com/sadekbaroudi/KLOR)

***

## CREDITS

The KLORs hardware is based on the [Sofle](https://github.com/josefadamcik/SofleKeyboard) by [Josef Adamcik](https://github.com/josefadamcik).\
Other inspirations are 
- [Kyria](https://splitkb.com/products/kyria-pcb-kit) by [Thomas Baart](https://github.com/splitkb)
- [Yacc46](https://github.com/1m38/keyboards/tree/main/yacc46) by [1m38](https://github.com/1m38)
- [Elephant42](https://github.com/illness072/elephant42) by [illness072](https://github.com/illness072)
- [Torn](https://github.com/rtitmuss/torn) by [Richard Titmuss](https://github.com/rtitmuss)
- [Claw44](https://github.com/yfuku/claw44) by [yfuku](https://github.com/yfuku)

I used the Pimoroni Haptic Buzz Footprint from the [Buzzard](https://github.com/crehmann/Buzzard) by [Christoph Rehmann](https://github.com/crehmann).

***

People who helped me create this board and fix stuff
- [KarlK90](https://github.com/KarlK90)
- [MangoIV](https://github.com/MangoIV)
- [OxCB](https://github.com/0xCB-dev)
- [MicroFortnight](https://github.com/microfortnight)
- [dreipunkteinsvier](https://github.com/dreipunkteinsvier)


If you build a KLOR I would be pretty happy to see some pictures. And if you want to leave me a tip you can do this [here](https://ko-fi.com/geigeigeist) (but please don't feel pressured)
