## DC Servo board

![Image of DC servo board](https://github.com/ajharvie/OLIA/blob/main/doc/images/DCservo_LR.jpg)

For convenience we include designs for an optical DC servo board, whic allows for ambient light compensation. Details of the method of operation of the board are available [in this paper,](https://doi.org/10.1016/j.ohx.2021.e00228) but a short description of the use and function of the board is provided here.

# Parts list
To build this circuit, you will require:
* A PCB [gerbers available here](https://github.com/ajharvie/OLIA/blob/main/Boards/OpticalDCServoGerbers.zip)
* Through-hole resistors:
  * 3 x 3.3 kΩ
  * 1 x 1.8 kΩ
  * 2 x 1 MΩ
* 0805 capacitors:
  * 2 x 10 µF
  * 2 x 0.1 µF
* OPA827 op-amp
* TC7660 charge pump IC
* 2 x 3.5 mm terminal blocks
* OPT101 amplified photodiode
* (optional) DIP socket for OPT101
