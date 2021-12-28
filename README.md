# Xmas 2021

This is the repository that contains the xmas 2021 badge schematic and pcb.
The badge is equipped with an [STM8L101F2P3] MCU, a coin cell, a push button and
7 LEDs. There are various test point so you can play with it, if you want.

A jig programmer adapter is provided in [prog_adapter](prog_adapter). Since a
lot of PCBs where made, the adapter gave an huge help during the programming
phase: no extra pin header or soldering required.

## Hardware

The BoM has been kept as minimal as possible to reduce costs.

| Annotation | Part                  | Package | Q.ty | Note                                   |
|------------|-----------------------|---------|------|----------------------------------------|
| BT1        | BH57A-5               |         | 1    | CR1616/CR1620 battery holder           |
| C1, C3     | 100nF                 | 0603    | 2    |                                        |
| C2         | 10uF                  | 0603    | 1    |                                        |
| D1 - D7    | LED                   | 0603    | 7    | Red, Green, Blue, Orange SMD LEDs      |
| J1         | 00-9155-004-251-006   |         | 0    | Slide contact, receiver footprint only |
| R1, R2     | 4k7                   | 0603    | 2    | I2C optional pull-up                   |
| R3 - R9    | 100 - 150             | 0603    | 7    | LEDs resistor                          |
| SW1        | PTS526 SK15 SMTR2 LFS |         | 1    | User button                            |
| U1         | STM8L101F2P3          | TSSOP20 | 1    | MCU                                    |

The PCB cutout and top silk screen were traced from a PNG icon (see [credits](#credits) below) using
[svg2shenzhen], an Inkscape plugin. The source image in both PNG and SVG (traced from the PNG) can be found
in [res](res). The [svg2shenzhen] output is a KiCad library.

The resulting PCB:

![top](res/xmas_2021_top.png)

![bot](res/xmas_2021_bop.png)

## Firmware

The firmware can be found [here](https://github.com/SebastianoC94/XMAS_Tree_2021). Thanks [@SebastianoC94]!

The firmware can be flashed with any SWIM-capable probe (JLink, STLinkV2/V3).

## Credits

- [@SebastianoC94]
- KiCad
- [svg2shenzhen]
- PCB cutout traced from [this](https://www.flaticon.com/free-icon/christmas-tree_6118946) flaticon image. Artist: [Freepik](https://www.freepik.com)


[STM8L101F2P3]: https://www.st.com/en/microcontrollers-microprocessors/stm8l101f2.html
[svg2shenzhen]: https://github.com/badgeek/svg2shenzhen
[@SebastianoC94]: github.com/SebastianoC94
