# AVB Android Things eXtension
AVB-EXT is an extension to the AVB specification containing features used on Android Things devices.

## Terminology
| Name  | Explanation |
| ------------- | ------------- |
| AVB      | Android Verififed Boot, version 2.0 | 
| Permanent Attributes | Attributes containing the product ID and the PRK, hash of which is usually permanently fused into the hardware. |

## Keys
The keys listed here are in an hierarchical order (expect the GSK), the highest one can be used to generate all the ones below it.
### Product Root Key (PRK)
This key is provided in permanent attributes and is the root authority for all Android Things products.

### Product Intermediate Key (PIK)
This key is a rotated intermediary. It is certified by the PRK.

### Product Signing Key (PSK)
This key is a rotated authority for a specific Android Things product. It is certified by a PIK and must match the public key data.

### Google Signing Key (GSK)
This key is a rotated authority for system and boot partitions built by Google.


## Credits/Resources
- [Google AVB EXT/avbtool sourcecode](https://android.googlesource.com/platform/external/avb/+/147b08db62f068c4fa76c3629f83d4282b614039)
