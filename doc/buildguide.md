**Parts list**

You will need:
* PCB
* Teensy 4.0
* 2 MCP602 op-amp ICs
* 1 LTC6910-2 programmable gain amplifier
* 1 TC7660 charge pump IC
* 1 74HC4060D binary counter IC
* 1 74HC4046AD phase-locked loop IC
* 1 200k potentiometer (Bourns 3310Y-001-204L or similar) and corresponding knob
* Through-hole resistors:
  * 4x 100k
  * 3x 10k
  * 2x 12k
  * 1x 2.2k
  * 1x 3.3k
  * 1x 4.7k
  * 1x 220k
* 0805 capacitors:
  * 3x 10 uF
  * 3x 100 pF
  * 1x 1.5 uF
  * 1x 820 pF
* 3.5 mm terminal blocks
  * 1x 2-terminal
  * 2x 4-terminal

**Assembly tips**

The PCB is designed with wide traces and vias to make it easy to manufacture using a desktop milling machine, but a cleaner option is to use an on-demand PCB manufacturing service (such as PCBWay or JLCPCB).

Before beginning soldering, the Teensy 4.0 should be flashed with the [correct firmware](https://github.com/ajharvie/OLIA/blob/main/Firmware/OLIAFirmware.ino). To do this, you will first need to download the [Arduino IDE](https://www.arduino.cc/en/software) and [Teensyduino](https://www.pjrc.com/teensy/teensyduino.html) (other solutions such as platformIO can also be used). For correct operation, the teensy must be run at a slight overclock - select "816 MHz - Overclock" in the CPU speed menu before flashing.

<img src="https://github.com/ajharvie/OLIA/blob/main/doc/images/boardImage.PNG" width=50% height=50%>

The image above shows the location where each component is soldered onto the PCB (locations are also marked on the PCB's silkscreen) All components are soldered onto the top side of the PCB. This can be achieved using only an iron, if you're careful, but those less experienced at soldering may wish to use a hot air gun when soldering on the LTC6910-2 as it is a very small package. The Teensy 4.0 is soldered to the board using pin headers. Once assembled, the board should be inspected for any bridges before applying power. The finished PCB is shown below:

 <img src="https://github.com/ajharvie/OLIA/blob/main/doc/images/completeboard.png" width=60% height=60%>


