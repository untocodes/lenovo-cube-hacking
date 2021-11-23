# Lenovo Smart Clock USB Port

The clock features a USB 3.0 type A port but connected to USB 2.0 internally - the unused pairs are used for UART and OTG ID.

## Pinout
| Pin Number | Name | Colour | Function |
| ---------- | ---- | ------ | -------- |
| 1 | VBUS | Red | USB Power |
| 2 | D- | White | USB 2.0 Data - |
| 3 | D+ | Green | USB 2.0 Data + |
| 4 | GND | Black | Ground |
| 5 | StdA_SSRX− | Blue | UART RX |
| 6 | StdA_SSRX+ | Yellow | UART TX |
| 7 | GND_DRAIN | N/A | Ground |
| 8 | StdA_SSTX- | Purple | OTG ID Pin* |
| 9 | StdA_SSTX+ | Orange | NC(?) |

* OTG cables usually ground the ID pin to signify OTG and is pulled high internally when not connected. 
This device is the opposite, ID pin is pulled low internally and needs to be pulled high to disable host mode.

## UART

| Setting | Value |
| ------- | ----- |
| Level | **1.8v** |
| BAUD  | 921600* |
| Data Bits | 8 |
| Parity Bit | None |
| Stop Bits | 1 |
| Flow Control | No |

* Mac users will need a client that uses the IOSSIOSPEED IOCTL to set baud otherwise you will not achieve 921600.

On a standard build this will show the bootlog up until EL3 handover to the kernel and then no more.
On debug builds it will provide a shell.

## Serial console
You can access an serial console as root by enabling it with fastboot.
After enabling, open the serial connection and you should get a shell.
```sh
fastboot p2u on
```
## ADB

On the standard rom, ADB is only enabled when AVB is unlocked:

```java
            if (Util.isDeviceAvbUnlocked()) {
                Log.i(TAG, "Device unlocked, allowing ADB connection from host: " + fingerprints);
                service.allowUsbDebugging(false, key);
                return;
            }
```
But when AVB is unlocked, keys cannot be read from RPMB and so the device cannot complete setup.

On debug builds it provides shell access with the ability to su, remount and disable verity.

```Bus 020 Device 004: ID 0e8d:201c MediaTek Inc. iot_mt8167s_som  Serial: XXXXXXXX```



