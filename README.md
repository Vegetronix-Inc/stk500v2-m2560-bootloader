# stk500v2 Bootloader for VG3D Printer

This is a fork of the [Prusa version](https://github.com/prusa3d/stk500v2-prusa) of the stk500v2 bootloader for the ATMEGA2560 chip on the Einsy Rambo board. It has been modified to be used on the [VG3D](https://www.vegetronix.com/Products/3D-Printers) printer.

In order recompile this code into a .hex file after making changes, you will need to use the `make` command in Linux or in the Windows Subsystem for Linux.

The command used to flash this code to the ATMEGA2560 using avrdude is:

`avrdude -v -v -c usbasp -P usb -pm2560 -Uflash:w:stk500boot_v2_mega2560.hex:i -Uefuse:w:0xFD:m -Uhfuse:w:0xD0:m -Ulfuse:w:0xFF:m -Ulock:w:0x0F:m`

Modifications to the command should be made when using a programmer other than the USBasp.
