# LabVIEW wrapper for WiringPi

A ligth wrapper that allow using wiringPi library (https://github.com/WiringPi/WiringPi) with LabVIEW-LINX. 

**Key Features:**  

- **Compatibility:** Valid with all versions of Raspberry Pi compatible with LabVIEW-LINX: Pi2, Pi3, Zero 2w, Pi4, and Pi5..
- **GPIO:** All pins can be configured as inputs or outputs, and an internal pull-up/pull-down resistor can be set. Edge detection functions are also available.
- **PWM:** The two hardware PWM channels can be configured and used with the corresponding pins (PWM0 on GPIO12 and GPIO18, and PWM1 on GPIO13 and GPIO19). The remaining pins can be configured for software PWM.
- **SPI:** Both channels, SPI0 and SPI1, can be used (if properly enabled in config.txt) and any of the corresponding chip select pins (CE0, CE1, or CE2) can be chosen.
- **I2C:** Standard access to the I2C port with data and register read/write functions.
- **Timming:** Funciones para implementar retardos en milisegundos y microsegundos 

Whether you’re working on a simple LED blink project or a complex automation system, WiringPi provides the tools you need to get the job done efficiently.

## Instalation

**On your PC:**  

Use the JKI VIPM tool to open and install the witingPI-1.0.X.XXX.vipm library.
The Funcitons menu will be updated to include the new blocks. 

**On your Raspberry:**

libLVwiringPi.so (*) and libcrypt.so.1 libraries (available in <vi.lib>\wiringPi) must be copied to the Raspberry where the code will be executed in the /usr/lib folder of the LabVIEW chroot environment (/srv/chroot/labview/usr/lib on the main file system).
This can be done manually, but a program for automatic installation is included: "Install Libraries.vi" in <vi.lib>\wiringPi. Run the program, enter the device details (Host, user, and password), and click Install.

(*) LibLVwiringPi.so is a version of wiringPi compiled within the LINX LabVIEW environment with some minor additions to support the LabVIEW's Call Library Funcition Node.