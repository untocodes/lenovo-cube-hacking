# AVB on the Lenovo Smart Clock

## Resources
- [Explanation on how the AVB works on an Android Things device](https://github.com/untocodes/lenovo-cube-hacking/blob/main/notes/avb/EXT.md)
## Unlocking and locking the AVB

### Unlocking
The AVB of the device can be unlocked by running the following command after booting the device into fastboot mode:
```sh
python at_auth_unlock.py cube_unlock_credentials_v2.zip
```
at_auth_unlock is a part of the google AVB tools and can be found [here](https://android.googlesource.com/platform/external/avb/+/master/tools/at_auth_unlock.py).

### Locking
The AVB of the device can be relocked by running the following command after booting the device into fastboot mode:
```sh
fastboot oem at-lock-vboot!
```
## Resources
- [Google's AVB 2.0 Docs](https://android.googlesource.com/platform/external/avb/+/master/README.md)
- [General reference into Android Security](https://github.com/doridori/Android-Security-Reference)
- [AVB EXT (eXtension) for Android Things](https://android.googlesource.com/platform/external/avb/+/147b08db62f068c4fa76c3629f83d4282b614039)
