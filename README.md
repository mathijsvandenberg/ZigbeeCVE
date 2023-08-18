
# ZigbeeCVE


This project is about the CVE central ventilation unit by Itho Daalderrop, used widely in the Netherlands. It can be controlled by a mechanical switch and current units can be controlled by a remote control to set the intensity.

The remote is working on 868 MHz and is working fine, however my child threw one in the bathroom sink and the radio chip did not survive. Buying a new remote is rather expensive and that made me search for alternatives.

## Solder a new CC1150 chip
Yes, this would be the most easy and less expensive way, but I had some domotica plans for this fan for automating.

## Emulate a remote control
There are a handful projects about emulating a remote control, but this is convenient for me, as I would like to change settings in e.g. my bathroom to go full throttle while showering. I might connect this to Home Assistant with some wrappers and software but...no.

## Go for Arjen Hiemstra's solution

Arjen actually inspired me for working on this project. He found out that you can control the CVE fan by writing I2C messages on a I2C bus exposed on a pin header inside the CVE fan. He also made a PCB and software that can do all kind of things. I really like his solution, but it will require additional software on HA to make it work in a automated system.

## Go the Arjen way, but rather use the standard Zigbee Light Link, used for Hue, TRÅDFRI, and register as dimmable light that actually controls the CVE. Yes!
