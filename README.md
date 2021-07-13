# Lenovo Smart Clock Hacking

## Progress
| Name  | Status |
| ------------- | ------------- |
| AVB Keys  | ☑️ Leaked/Obtained  |
| Firmware  | ☑️ Leaked/Obtained  |
| Kernel source  | ☑️ Available on Lenovo's Site  |
| Debug output  | ❓ Lenovo has an special debug cable for sale, most likely using usb 3 pins  |
| Boot  | ❓ Device won't boot custom/modified firmware, possibly AVB related  |
| ADB | 🛑 Blocked in device firmware |
| Fastboot | ☑️ Available with an USB A->A Cable |
| SP Flash Tool | ☑️ Working with BootROM exploit! | 
## Notes
- [Basic information about the Smart Clock and related devices](https://github.com/untocodes/lenovo-cube-hacking/blob/main/notes/Basics.md)
- [Flashing the device](https://github.com/untocodes/lenovo-cube-hacking/blob/main/notes/Flashing.md)
- [AVB and unlocking](https://github.com/untocodes/lenovo-cube-hacking/blob/main/notes/AVB.md)
## Resources

- [deadman96385's XDA Thread](https://forum.xda-developers.com/t/lenovo-smart-clock-bootloader-avb-unlock-firmware-region-changer-kernel-source.4130295/)
- [System partition files](https://github.com/deadman96385/things_mt8167s_som_dump)
- [Kernel Source provided by Lenovo](https://smartsupport.lenovo.com/uk/en/products/smart/smart-home/smart-clock/za4r/downloads/driver-list/component?name=Software%20and%20Utilities) 
- [Fuschia Board Drivers](https://fuchsia.googlesource.com/fuchsia/+/3a593fc8b3a7/src/devices/board/drivers/mt8167s_ref)
- [Fuschia Board Ref](https://fuchsia.googlesource.com/fuchsia/+/refs/heads/releases/f2/boards/mt8167s_ref.gni)

## Credits

- [@Wh1terat](https://github.com/Wh1terat) for helping with figuring most of this stuff out.
