# X.Tips X7S QMK Firmware

QMK firmware files for the X.Tips X7S 36-key split keyboard.

<p align="center">
  <img src="images/keyboard.png" width="80%" alt="X.Tips X7S Keyboard">
</p>

## Overview

- Works out of the box with [Vial 0.7.1](https://get.vial.today/download/)
- Full QMK support with 9 layers via VIA/Vial
- RGB LED indicators for each layer
- Split keyboard with 3x5 + 3 thumb keys per half
- USB-C connection
- TRRS/audio jack connection between halves


## Hardware Features

- STM32F103 MCU
- Split keyboard communication via USART
- WS2812 RGB LEDs (1 per half)
- Direct pin matrix

## RGB LED Layer Indicators

The RGB LEDs show different colors for each layer as defined in leds.c

## Folder Structure

```
x7s/
├── 

config.h

               # Core QMK configuration
├── 

halconf.h

             # ChibiOS HAL config
├── info.json             # QMK keyboard info
├── 

keyboard.json

         # VIA/Vial layout definition
├── 

mcuconf.h

            # MCU settings for STM32F103
├── readme.md            # This documentation
├── 

rules.mk

             # QMK build rules
├── 

x7s.c

                # Keyboard initialization
├── x7s.h                # Matrix definitions
└── keymaps/
    ├── default/         # Default keymap
    │   ├── keymap.c     # Base layer definitions
    │   └── 

rules.mk

     # Keymap build rules  
    └── via/            # VIA-enabled keymap
        ├── keymap.c     # VIA keymap with 9 layers
        ├── leds.c       # RGB LED indicators
        ├── 

config.h

     # VIA-specific config
        └── 

rules.mk

     # VIA build settings
```

## License

This firmware is released under [GPL-2.0-or-later](https://www.gnu.org/licenses/gpl-2.0.html).

## Credits

- Original firmware by zvecr
- VIA compatibility and RGB layer indicators by X.Tips
