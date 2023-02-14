#Cantor Choc V2
This is a Cantor variant adjusted for chocV2 switches, which use MX keycaps. Choc V2's are slighlty larger than Choc V1, so the layout has been adjusted accordingly. None of the routing has changed, so any V1 firmware will work on V2. This design has not been produced/validated yet. Proceed at your own risk.
Todo:
* Validate the double-sided footprint is correct.
* Verify the routing sans diodes.
* Update branding/versioning. (Try out fonts with KiCad v7).
* What's the deal with the licensing?
* Should this be updated for the pi2040 (Currently uses blackpill).
* Can the footprint be modified to accomidate Cherry low-profile?

# Cantor Keyboard
The Cantor keyboard is a 42 key diodeless split keyboard, designed with simplicity in mind. It is inspired on the popular [corne](https://github.com/foostan/crkbd), [ferris](https://github.com/pierrechevalier83/ferris) and [sweep](https://github.com/davidphilipbarr/Sweep) keyboards, aiming to provide a more ergonomic (stronger column stagger) corne-like layout with a simple, easy to assemble and cheap design.

![Cantor Keyboard](assets/cantor_keyboard.jpg)

The keyboard uses choc switches with choc spacing. Therefore, only MBK keycaps can be used.

### Why diodeless?

A diodeless design reduces the keyboard assembly time, as the amount of components to solder is significantly reduced.
Moreover, soldering diodes can cause trouble during the keyboard build. Diodes need to be placed in the correct direction, if not, the keys won't work well!
Eliminating diodes will prevent many errors during the assembly process.

## Disclaimers

All the designs and files are provided "AS IS" without any warranty or support.

## Design philosophy

The Cantor is designed with the following goals:

- Comfort
- Powerful
- Low cost
- Simplicity
- Ease of build
- USB-C
- No diodes

The PCB is reversible to reduce manufacturing costs.

## Getting started

Would you like to build this keyboard? Then continue reading!

You can also buy a kit to build the Cantor keyboard from one of the **honorable sponsors**:

<a href="https://shop.beekeeb.com" target="_blank"><img src="https://beekeeb.com/beekeeb-logo.png" align="left" width="200" ></a>
<a href="https://42keebs.eu" target="_blank"><img src="https://user-images.githubusercontent.com/25749629/194108923-33d79eb9-c6da-495b-a60e-fd3f4cd073f4.png" align="left" width="200" ></a>
<br><br><br><br>
  
### Bill of Materials

To build the keyboard, you will need the following materials:

- 2x PCB boards (both are equal since they are reversible)
- 2x STM32F401CC blackpill microcontrollers (they are cheap on aliexpress)
- Pins and sockets for the microcontrollers (blackpill needs 20 pin stripes)
- 42 Choc v1 switches
- 42 MBK keycaps
- Some little rubber feet/bumpers (recommended 6 mm of diameter)
- 2x TRRS jacks (PJ-320A)
- 1x TRRS cable
- 1x USB cable compatible with your computer and the blackpill

### Order the PCB

Download the gerber file from realeses, and submit it to your favorite PCB manufacturer. The keyboard designs have been tested with JLCPCB.

Note: if you don't want a random tracking number to be printed in the PCB, make sure to select the option 'Remove Order Number' in JLCPCB.

### How to Build

To build the keyboard, you'll also need a soldering iron and some tin. Follow the [build guide](doc/build_guide.md).

### Firmware

The Cantor keyboard uses the QMK firmware. Firmware for this keyboard is coming soon to the main QMK repository with [this PR](https://github.com/qmk/qmk_firmware/pull/16552).

To flash the firmware to the microcontroller connect the blackpill to your computer and set it to bootloader mode. To do this the first time:

1. Press and hold the BOOT0 button.
2. Press and release the NRST button.
3. Release the BOOT0 button.

The following times you want to flash the keyboard, it is much simpler thanks to bootmagic. Hold the top left key of the keyboard and plug the microcontroller. If flashing the right part, hold the top right key.

## Feedback

If you have build this keyboard, please fill [this form](https://forms.gle/nfJCsei5hyHbjaHn9) to provide feedback. This will help to improve the keyboard design in future revisions.

Also, you can open an issue reporting any problem or feature request.

## Support

The development of a keyboard takes time and money. If you like this keyboard a want to support me for the work and to develop future revisions of the keyboard, consider donating:

PayPal: [![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donate_SM.gif)](https://www.paypal.com/donate/?hosted_button_id=ZKKE68MCBQ9P6)
GitHub: [Here](https://github.com/sponsors/diepala)

### Honorable sponsors


Thank you very much to everyone contributing and/or sonponsoring this project. Special thanks to the honorable sponsors:

<a href="https://shop.beekeeb.com" target="_blank"><img src="https://beekeeb.com/beekeeb-logo.png" align="left" width="200" ></a>
<a href="https://42keebs.eu" target="_blank"><img src="https://user-images.githubusercontent.com/25749629/194108923-33d79eb9-c6da-495b-a60e-fd3f4cd073f4.png" align="left" width="200" ></a>
