## MacOS Sonoma on Zephyrus G14 GA401QH

OpenCore version: v1.0.1
MacOS version: 14.5.1

### Hardware
| Component | Model |
| --- | --- |
| CPU | AMD Ryzen 7 5800HS |
| RAM | 24GB DDR4 SODIMM |
| iGPU | Radeon Vega 8 |
| Audio codec | Realtek ALC285 (layout 11) |
| WLAN | Intel AX210 |
| SSD | Intel 670p |

#### Working
- WiFi and Bluetooth
- USB ports
- USB tethering
- Internal microphone
- iGPU

#### Not working
- DRM
- dGPU (of course)
- OpenGL (broken most of the time, should be mitigated with `BFixup`)
- iServices with WLAN (LAN works out of the box)

### Caveats
- `ForgedInvariant` and `NootedRed` are not bundled, manually download them from `ChefKissInc`.
- Fill redacted fields like MLB and serial number in `config.plist` before installing.
- Use [`UMAF`](https://github.com/DavidS95/Smokeless_UMAF) to enable `Above 4G decoding` and set VRAM to at least 1GB.
