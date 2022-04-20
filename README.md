# OLIA
## The Open Lock-In Amplifier

![Image of completed board](https://github.com/ajharvie/OLIA/blob/main/doc/images/completeboard.png)

A pocket-sized, USB-powered, open digital lock-in amplifier, based around the Teensy 4.0. Features include:
- Internal or external referencing
- 10 Hz - 15 kHz frequency range
- Dynamic range of ~10<sup>6</sup> (using input preamp)
- -1.6 V to +1.6 V bipolar input
- Variable input gain (from 0 to 64)
- Configurable analogue output
- Both exponential and synchronous filtering, with adjustable filter time constant
- Parallel calculation of higher harmonics
- 5 V power passthrough
- Simple, powerful frontend
- Ultra low unit cost (~£30)
- Simple construction (all hand-solderable)

More details coming soon, but in the short term we include a [parts list and build guide](https://github.com/ajharvie/OLIA/blob/main/doc/buildguide.md) alongside some simple [usage instructions.](https://github.com/ajharvie/OLIA/blob/main/doc/usageGuide.md) CAD and CAM files for the device's PCB are available in the [boards](https://github.com/ajharvie/OLIA/tree/main/Boards) directory, and source code for the device's firmware is available [here](https://github.com/ajharvie/OLIA/tree/main/Firmware). A simple python frontend is provided [here](https://github.com/ajharvie/OLIA/tree/main/GUI), but those who wish to build their own interface can refer to the [serial reference](https://github.com/ajharvie/OLIA/blob/main/doc/SerialRef.md).
