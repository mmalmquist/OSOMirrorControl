# OSOMirrorControl
The code that is used to control the motion of ozon and water mirrors at Onsala Space Observatory.

# Setup communication
The RS232 port is prefered when serviceing the controllers as they have the ethernet port configured for normal operation.

The serial port on the servicing machine can be configured by issuing:

`stty -F /dev/ttyS0 <baud-rate> cs8 -cstopb -parenb`
## Vattenspegel
The DMC-2112 is set up to use a baud rate of 19200.

## OzonMirror and Kinaradiometer
The DMC-30011 are set up to use a baud rate of 115200.

# Upgrading control code
The command reference is located in the `doc` directory.
The updated code can be burned into the DMC unit using the development environmend using the folowing procedure.

+ In the terminal window, run the command `RS` to reset the device to a power-on state.
+ Select the program that is to be burned onto the device and click "Download".
+ In the terminal window, run the command `BP` to burn the program into the device's memory.

Optional:
+ Run the command `RS` once again.
+ Upload the program from the devices memory into the development environment.
+ Verify that it is the program you just downloaded onto the device.