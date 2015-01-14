nodemcu_file_util
=================

File manipulation utility for NodeMCU firmware for ESP8266 WiFi modules

This utility can transfer files to the flash memory connected to ESP8266 running
the NodeMCU firmware (developed using 'NodeMcu 0.9.5 build 20150108'). Currently
the following functions available:

 - list the names and sizes of the files stored in the flash
 - delete files from the flash
 - transfer files to flash
 - transfer files from flash
 - execute stored files

For transferring files it converts all bytes of the source file into escape
sequences, for example the new line character becomes '\10', letter 'A' becomes
'\65', and so on. This obviously causes a relatively big overhead when sending
the data over the serial line but it makes possible to send binary files without
limitation.
