<picture>
  <source media="(prefers-color-scheme: dark)" srcset="/docs/images/klor-font-logo-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="/docs/images/klor-font-logo-bright.svg">
  <img alt="KLOR logo font" src="/docs/images/klor-font-logo-bright.svg">
</picture>

# KLOR SPLIT KEYBOARD

KLOR is 36-42 keys column-staggered split keyboard. It supports a per key RGB matrix, encoders, OLED displays, haptic feedback, speakers, a Pixart Paw3204 trackball, the [SplitKB tenting puck](https://splitkb.com/products/tenting-puck) and four different layouts, through brake off parts.


## LAYOUTS

![KLOR layouts](/docs/images/klor-layouts.svg)


## PCB 

[Here](/PCB/) you can find the KiCad files and Gerbers for the KLOR. 


## CASE

[Here](/case/) are the case files for the KLOR. There is an acrylic case and a 3D printed case (which uses acrylic too) for every layout.


## SWITCHPLATE

In every case directory you'll find the matching switchplates as **.dxf**, **.svg** and **.zip** containing gerber files for a FR4 plate.


## BUILD GUIDE

Here you can find the build guides for the KLOR.\
[KLOR build guide 3DP case](/docs/buildguide_3DP.md) (QMK)\
[KLOR build guide stacked acrylic case](/docs/buildguide_acrylic.md) (QMK)\
[KLOR BLE build guide 3DP case](/docs/buildguide_3DP_ble.md) (ZMK)\
[KLOR BLE build guide stacked acrylic case](/docs/buildguide_acrylic_ble.md) (ZMK)


## FIRMWARE

[QMK config](https://github.com/GEIGEIGEIST/qmk-config-klor) for the KLOR (supports OLED, encoders, LEDs, haptic feedback and speakers)\
[ZMK config](https://github.com/GEIGEIGEIST/zmk-config-klor) for the KLOR (supports OLED, encoders, LEDs and Bluetooth)\
Thaks to [Manna Harbour](https://github.com/manna-harbour) you can find KLOR in [Miryoku ZMK](https://github.com/manna-harbour/miryoku_zmk)


## CREDITS

The KLORs hardware is based on the [Sofle](https://github.com/josefadamcik/SofleKeyboard) by [Josef Adamcik](https://github.com/josefadamcik).\
Other inspirations are 
- [Kyria](https://splitkb.com/products/kyria-pcb-kit) by [Thomas Baart](https://github.com/splitkb)
- [Yacc46](https://github.com/1m38/keyboards/tree/main/yacc46) by [1m38](https://github.com/1m38)
- [Elephant42](https://github.com/illness072/elephant42) by [illness072](https://github.com/illness072)
- [Torn](https://github.com/rtitmuss/torn) by [Richard Titmuss](https://github.com/rtitmuss)

I used the Pimoroni Haptic Buzz Footprint from the [Buzzard](https://github.com/crehmann/Buzzard) by [Christoph Rehmann](https://github.com/crehmann).

***

People which helped me creating this board and fixing stuff
- [KarlK90](https://github.com/KarlK90)
- [MangoIV](https://github.com/MangoIV)
- [OxCB](https://github.com/0xCB-dev)
- [MicroFortnight](https://github.com/microfortnight)
- [dreipunkteinsvier](https://github.com/dreipunkteinsvier)