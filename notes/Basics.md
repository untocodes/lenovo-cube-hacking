# Basic information about the Lenovo Smart Clock

## Specifications
| Type | Detail |
| ---- | ------ |
| CPU  | MediaTek MT8167S 1.5GHz * |
| RAM  | 1GB |
| STORAGE | 8GB eMMC |
| SCREEN | 480 x 800 IPS Touch Screen |

* This CPU is also known as the MT8516

## Related devices
- [Xiaomi Mi Smart Clock](https://www.mi.com/global/product/mi-smart-clock/overview) (Runs the same software and probably uses the same IC)
- [Lenovo Smart Frame](https://www.lenovo.com/ca/en/virtual-reality-and-smart-devices/smart-home/smart-home-series/Lenovo-CD-3L501/p/ZZISZSDCD04) (has same IC, runs AOSP)
- [Lenovo Smart Display 7](https://www.lenovo.com/us/en/virtual-reality-and-smart-devices/smart-home/smart-home-series/Lenovo-CD-17302/p/ZZISZSDCD02) (same IC, runs Things)
- [Google Coral Dev Board Mini](https://www.mediatek.com/blog/google-coral-dev-board-mini-pairing-tpu-to-mt8167-soc) (same IC with TPU, Runs Mendel Linux)
## Hidden Menus
A debug menu can be enabled by modifying the factory props included in the factory.img file and adding the line below to the end of the file.
```sh
ro.debuggable=1
```
![About Device Menu](https://raw.githubusercontent.com/untocodes/lenovo-cube-hacking/main/notes/images/debug_settings1.jpg)
![Debug Settings Menu](https://raw.githubusercontent.com/untocodes/lenovo-cube-hacking/main/notes/images/debug_settings2.jpg)
