# PiDP-11 I/O Expander

This repository contains the PCB design files for a 16-bit TTL compatible I/O
expander for the [PiDP-11][1] and [Raspberry Pi][2]. Design files are intended
to be viewed using [Altium Designer][3]. Releases may also be uploaded to the
standalone [Altium 365 Viewer][4] for free.

Project documentation is hosted on [Hackaday][5] and assembled boards are
available for purchase from [Tindie][6].

![PCB](PiDP11IOExpander.png)

## Details

The heart of the I/O Expander is a [Microchip MCP23016][7], which is similar in
function to the popular MCP23017 with the added benefit of TTL compatibility to
support both 3V3 and 5V logic levels. The I/O Expander provides GPIO access to
16 pins over I2C (up to 400kHz), which can be independently configured and
controlled by software. Interrupts are fully supported and routed to GPIO 19 on
the Raspberry Pi.

Up to 8 I/O Expander boards may be connected in series to increase the total
number of GPIO pins to 128. Rework may be needed to support multiple boards (eg.
adjusting pull-up resistor values) depending on installation method and overall
bus capacitance. Additional pin headers must be also be fitted and shunted to
configure I2C addresses to avoid bus conflicts.

For more details, see the latest release on [GitHub][8].

## Contributing

Pull requests are welcome! See [CONTRIBUTING.md] for more details.

## License

Source code in this repository is licensed under a Simplified BSD License. See
[LICENSE.txt] for more details.

[1]: https://obsolescence.wixsite.com/obsolescence/pidp-11
[2]: https://www.raspberrypi.org/
[3]: https://www.altium.com/altium-designer/
[4]: https://www.altium.com/viewer/
[5]: https://hackaday.io/project/181311
[6]: https://www.tindie.com/products/24781
[7]: https://www.microchip.com/en-us/product/MCP23016
[8]: https://github.com/sstallion/PCB-PiDP11IOExpander/releases/latest

[CONTRIBUTING.md]: CONTRIBUTING.md
[LICENSE.txt]: LICENSE.txt
