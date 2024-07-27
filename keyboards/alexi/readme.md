# LXIII @ Alexi

![Alexi](https://i.imgur.com/16LtZKQ.jpg)
![Alexi_Bottom](https://i.imgur.com/8mbWkhO.jpg)
![Alexi_Colors](https://i.imgur.com/o0SzCWA.jpg)

*LXIII @ Alexi is an ergonomic split layout 5X/6X% keyboard. Solder only. Several liberties such as removing several keys to achieve the maximum symmetricity. Users are expected to map the missing keys into additional layers. The keys are laid out based on having both homing keys F&J to be placed on mirrored identical position on either left and right side of the keyboard. Currently only 2 major layouts is available in the qmk build folder - stock 63 (lxiii) keys and VIA. All possible layouts are customizable through VIA. Note - Currently VIA only works by self uploading the keyboard definition into the design tab* *pending pull request* *VIA keyboard definition is available through maintainer's github*
*Alexi is equipped with an OLED display on the left side of the keyboard, an optional pinout for a pushbutton rotary encoder (matrix: 1,12)

LAYOUTS
this keyboard supports the following layouts as per baked in into the VIA specific firmware.

BASE LAYOUT
![Base_Layout](https://i.imgur.com/7YPRcfj.jpg)
A1+B1+C1+D1+E1+F1+G1

[Layouts](https://i.imgur.com/j8SfRmf.mp4)

        A. BackSpace Cluster
        1. 1U + Push Button Rotary Encoder
        2. Split 1U + 1U Backspace
        3. 2U Backspace

        B. Left Shift Cluster
        4. 1.5U + 1.25u Split Left Shift
        5. 1.75U+1U Split Left Shift
        6. 2.75u Left Shift (not supported with supplied switch plate)
        
        C. Right Shift Cluster
        7. 1U Up Key + 1.75U Right Shift
        8. 2.75U Right Shift (not supported with supplied switch plate)
        
        D. Bottom Left Modifiers
        9. 3 x 1U Bottom Left Modifiers
        10. 2 x 1.5U Bottom Left Modifiers

        E. Bottom Right Modifiers
        11. 3 x 1U Bottom Right Modifiers
        12. 2 x 1.5U Bottom Right Modifiers

        F. Left Spacebar Cluster
        13. 2.75U Spacebar + 1U Spacebar
        14. 1U Spacebar + 2.75U Spacebar

        G. Right Spacebar Cluster
        15. 2U Spacebar + 1.25U Spacebar
        16. 1.25U Spacebar + 2U Spacebar

layouts B6 and C8 (2.75U Shift)is not supported with the supplied switchplate 

Additional features

        A. 1306 vertical oled display. limited customization via coding due to the available memory on the at32u4. learn more on customizing oled display at https://docs.qmk.fm/features/oled_driver
        B. Optional rotary encoder (refer to A. BackSpace Cluster) rotary encoder mapping will be activated on both stock base qmk and VIA firmware.
        C. 18x RGB led underglow with reduced animations to adhere to EEEPROM size limit. Users can make more space by removing any graphics displayed on the oled display as well as only using basic fonts.

* Keyboard Maintainer: [dumb_dumb](https://github.com/hxy)
* Hardware Supported: alexi v3.17 pcb with oled, rotary encoder and rgb underglow.
* Hardware Availability: *currently not available for purchase - switchplate dxf for 2.75u shift available upon request*

Make example for this keyboard (after setting up your build environment):

    make alexi:default
    make alexi:via

Flashing example for this keyboard:
    directly flashing post compiled is not advisable. please compile and flash using qmk toolbox

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).

## Bootloader

Enter the bootloader in 3 ways:

* **Bootmagic reset**: Hold down the key at (0,0) or 6
* **Physical reset terminals**: Use twizers to short the reset terminal labelled (bottom side pcb left of the usb port array)
* **Keycode in layout**: Press the key mapped to `QK_BOOT` (refer to default keymap for both base qmk and VIA)
