Ethernet Bootloader
==================

Dual bootloader
===============
This bootloader was written originally by https://github.com/thseiler and adapted for Arduino Ethernet by David Cuartielles



Arduino Ethernet board and TFTP Bootloader
==========================================

The Arduino Ethernet board is built by merging a regular Arduino board with the Arduino Ethernet Shield. Therefore, codewise, anything that works on your Arduino plus Ethernet Shield works on this board.

There are some small hardware improvements from the Ethernet shield, namely we have replaced the resistors used to adapt the 3.3v parts to 5v coming from the processor with new high speed buffer. This will allow faster transfer rate when accessing the SD Card.

How to get code into your board: The boards that you have received don't have any bootloader installed on it, they have run a small test program in the factory. In order to upload code to the board you will need either an ISP programmer or an Arduino 2009 running the AVR ISP sketch (Arduino Uno's have some issues with the ISP sketch due to new bootloader)

If you burn the normal Arduino bootloader on this board you can hook up an usb-serial converter (or an unchipped Arduino) to pins 0,1,GND and Reset to program it like any 2009 board.

We have been developing an ethernet bootloader that will allow you to upload code to the board using a TFTP client. It's currently alpha quality code and we would immensely appreciate if you could help us test it and debug it.

The boards that you have received should be fitted with a Power-Over-Ethernet (PoE) module, this allows you to power your board through its ethernet cable. 
These modules are compliant with current PoE standards and require a proper PoE enabled hub delivering 48 Volts.

BE CAREFUL, when the Arduino Ethernet is connected to a PoE enabled hub, the bottom of the board has pins connected to 48V, be very very careful not to place the board on metallic surfaces. We recommend you place your Arduino in a plastic enclosure.






