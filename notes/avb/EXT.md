# AVB Android Things eXtension
AVB-EXT is an extension to the AVB specification containing features used on Android Things devices.

## Terminology
| Name  | Explanation |
| ------------- | ------------- |
| AVB      | Android Verififed Boot, version 2.0 | 
| Permanent Attributes | Attributes containing the product ID and the PRK, hash of which is usually permanently fused into the hardware. |
| vbmeta | Partition containing checksums of the most important partitions to verify them. |
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

## Commands
The avbtool utility has several Android Things specific commands. 
### make_atx_certificate
| Name | Function |
| ---  | -------- |

### make_atx_permanent_attributes
Generates the permanent attributes from the keys and device ID provided.
| Name | Function |
| ---  | -------- |
| output | Output file |
| authority_key_path | Path to authority (PRK) PEM |
| subject_key | A PEM or DER subject (PIK) public key. |
| subject_key_version | 64bit version value |
| subject | Product ID | 
| is_intermediate_authority | True if subject key is an PIK. |
| signing_helper | Program to hash the signature (NOT REQUIRED) | 
### make_atx_metadata
Generates AVB metadata for the vbmeta image.
| Name | Function |
| ---  | -------- |
| output | Location for the file to be written on success |
| intermediate_key_certificate | PIK Certificate file |
| product_key_certificate | A certificate file as output by make_atx_certificate with is_intermediate_authority set to false. |
| google_key_version | The version of the Google Signing Key used in the associated vbmeta image. |

## Credits/Resources
- [Google AVB EXT/avbtool sourcecode](https://android.googlesource.com/platform/external/avb/+/147b08db62f068c4fa76c3629f83d4282b614039)
