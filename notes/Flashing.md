# Flashing the Lenovo Smart Clock

## Fastboot

The device can easily be flashed through fastboot with an A->A USB Cable after removing the AVB lock with the keys provided in the XDA thread. 

To get the device to boot into fastboot mode you need to do the following:

1. Unplug all cables from the device
2. Plug the USB A->A Cable to the device and your computer.
3. Hold down the + Volume Button on the device
4. Plug in the power cable and continue holding the button for 10 seconds.

## SP Flash Tool

- The device seems to be affected by a [Mediatek BootROM exploit](https://github.com/MTK-bypass/bypass_utility) which would allow us to flash the device fully without the need for an SLA/DAA.
- The device has been successfully gotten to interact with SP Flash Tool after running the exploit but since we do not have an Scatter File for the device we couldn't try it any futher.
