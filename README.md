## EFI for MacOS Big Sur on Zephyrus G14 GA401QH

OpenCore version: v0.9.2  
MacOS version: 11.7.7

### Screenshot
![image](https://github.com/AlphaNecron/Zephyrus-G14-GA401QH-EFI/assets/57827456/b9ec2bc9-e8a7-4fac-bb26-197d48a60117)

### Hardware specification
| Component | Model |
| --- | --- |
| CPU | AMD Ryzen 7 5800HS |
| RAM | 24GB DDR4 SODIMM |
| iGPU | Radeon Vega 8 |
| Audio codec | Realtek ALC285 (layout 11) |
| Wifi | Mediatek MT7921 (requires replacement) |
| SSD | Intel 670p |

#### Working
- App Store and other apps
- USB ports
- USB tethering
- iGPU

#### Not working
- Wifi / Bluetooth - Requires compatible cards like Intel (non-native) and BCM.
- Internal microphone - AMD desktop is affected as well.
- Fn keys - requires SSDT patching.
- DRM - Waiting for fixes from `NootedRed`
- dGPU - 1650 is not supported btw.

### Notes
- Remember to use GenSMBIOS and change MASKED properties in `config.plist`.
- Only supports Big Sur, Monterey requires patches.
- Use [`UMAF`](https://github.com/DavidS95/Smokeless_UMAF) to enable `Above 4G decoding` and increase VRAM to at least 1GB (2GB is recommended)
