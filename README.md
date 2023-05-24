## EFI for MacOS Big Sur on Zephyrus G14 GA401QH

OpenCore version: v0.9.2  
MacOS version: 11.7.7

![image](https://github.com/AlphaNecron/Zephyrus-G14-GA401QH-EFI/assets/57827456/b9ec2bc9-e8a7-4fac-bb26-197d48a60117)

### Specifications
| Component | Model |
| --- | --- |
| CPU | AMD Ryzen 7 5800HS |
| iGPU | Radeon Vega 8 |
| Audio Codec | Realtek ALC285 |
| Wifi | Mediatek MT7921 (needs replacement) |
| SSD | Intel 670p |

#### Working
- App Store and other apps
- USB ports
- USB tethering
- iGPU

#### Not working
- Wifi / Bluetooth
- AirDrop - Requires compatible WLAN/Bluetooth card
- Internal microphone - AMD desktop is affected as well
- DRM - Waiting for fixes from `NootedRed`
- dGPU - 1650 is not supported btw.

### Notes
- Remember to use GenSMBIOS and change MASKED properties in `config.plist`.
- Only supports Big Sur, Monterey requires patches.
