<picture><img align="left" src="/Img/Logo.png" width="20%"/></picture>
<h1>UXTU4Unix (WIP)</h1>
<h3>Based on RyzenAdj and Python</h3>

![GitHub Downloads (all assets, latest release)](https://img.shields.io/github/downloads/AppleOSX/UXTU4Mac/total)

---

### 13/4/2024: `UXTU4Mac` has been renamed to `UXTU4Unix` to support with Linux 

> [!CAUTION]
> - **Do not** use `UXTU4Unix` with [SMCAMDProcessor](https://github.com/trulyspinach/SMCAMDProcessor) as they may conflict with each other.
> - This is not an **alternative solution** to [SMCAMDProcessor](https://github.com/trulyspinach/SMCAMDProcessor) and [NootedRed](https://github.com/ChefKissInc/NootedRed) for their CPU/APU power management itself.


## Supported APU & OS
> [!NOTE]
> - AMD Zen-based processors that are supported [NootedRed](https://github.com/ChefKissInc/NootedRed) **or** [UXTU](https://github.com/JamesCJ60/Universal-x86-Tuning-Utility) **Premade Preset** section (or just simply support RyzenAdj)
> - Support from macOS 10.4 to the latest version (14)
> - Support Linux (tested on Debian-based distros, Fedora)

## Usage
- Download the official build from Releases.
- Run `UXTU4Unix.command` (only for macOS) or run `UXTU4Unix.py` by using `python3` command ( `python3 /path/to/UXTU4Unix.py` )
- Follow the instructions.
- [macOS only] Disable `Core Performance Boost` in BIOS using [Smokeless_UMAF](https://github.com/DavidS95/Smokeless_UMAF) to achieve better temperature but sacrifice a lot of CPU performance/better control with `UXTU4Unix`

## FAQ
### 1. Why do we have to disable SIP in macOS?
- Honestly, the binary file (ryzenAdj and DirectHW) is recognized in macOS as untrusted kexts. So, in order to get it working, we have to disable SIP including the flag `ALLOW_UNTRUSTED_KEXTS` (0x1).
### 2. Why does `UXTU4Unix` lack CPU support?
- When I ported a bunch of AMD APU presets from `UXTU` to `UXTU4Unix`, some commands were not compatible with ryzenAdj (because `UXTU` uses lots of methods to change CPU/APU settings besides ryzenAdj), especially the CPU presets. So, I could only keep some commands as a `work-around`.
### 3. GUI wen eta?
- `idk` - NotchApple1703 said to me, but we will release it soon.

## For advanced users, please visit [Custom.md](Custom.md).
## Comparison 

|  | UXTU | UXTU4Unix |  
|    :---:     |    :---:   |    :---:   |
| GUI | ✅ | ❌ No, currently only for CLI |
| Adjust power management settings | ✅ | ✅ |
| Premade presets | ✅ | ✅ |
| Custom presets | ✅ | ❓ |
| Adaptive mode tracking | ✅ | ❓ |
| Game mode tracking | ✅ | ❓ |
| Support for many hardware | ✅ | ❌ Only for some AMD Ryzen APU/CPU models |

# Preview

<p align="left">
  <img src="/Img/main_menu.png">
  <img src="/Img/apply_preset.png">
  <img src="/Img/preset.png">
  <img src="/Img/preset_setting.png">
  <img src="/Img/settings.png">
</p>

### Extreme Preset
![Screenshot 2024-02-12 at 15 52 16](https://github.com/AppleOSX/UXTU4Mac/assets/98001973/19e1481a-07ae-4efb-9b50-fac0cf137e0a)

> [!CAUTION]
> - We **think** the members and owners of ChefKiss Inc shouldn't use this tool. Why? Because Visual **will** say `Do not use this tool because it will break our NootedRed/AMDPlatformPlugin power management, etc...`. So, is that true? We still don't know because I've been banned from both Telegram and GitHub by ChefKiss (Visual)
> - PR is welcome btw

### Special thanks to
- [corpnewt](https://github.com/corpnewt) for command file
- [NotchApple1703](https://github.com/NotchApple1703) for the GUI (starting from version `0.3.x` or `0.4.x`)
- [b00t0x](https://github.com/b00t0x) for the guide to build ryzenAdj based on DirectHW and pciutils-osx
- [JamesCJ60](https://github.com/JamesCJ60) for [UXTU](https://github.com/JamesCJ60/Universal-x86-Tuning-Utility)
