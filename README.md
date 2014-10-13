UltiboardV2-usbserial
=====================

This is frank26080115's fork of UltiboardV2-usbserial, it is meant to prevent the operating system from causing the main UM2 circuit to reset when a connection is estabilished with the virtual serial port.

For example, without this fork, if OctoPrint is launched and connected to the UM2 while it is printing, the UM2 will immediately reset and the print job is ruined.

The way it does this is that the reset line will be "locked" until a change to 300 baud will "unlock" it for a few minutes.

For Cura to update the UM2 firmware, the user will need to change the virtual serial port to use 300 baud first. Or the Cura code can be modified to do this automatically.
