# Hackintosh for Dell Precision 3240 Compact

Also tested on Dell Precision 3440 Small Form Factor Workstation. Assuming it will work for Dell Precision 3640 Tower Workstation.

## Specs

### Hardware

| Component | Tested                                                                                                           |
| --------- | ---------------------------------------------------------------------------------------------------------------- |
| CPU       | Intel Core i3 / i5 / i7 10x00 (10th Gen)                                                                         |
| Chipset   | Intel W480                                                                                                       |
| Graphics  | Intel UHD 630                                                                                                    |
| Ethernet  | Intel I219-LM                                                                                                    |
| Memory    | SK Hynix / G.SKILL / Crucial                                                                                     |
| NVMe      | XPG SX8200 / WD SN750 / Samsung 970 Evo Plus                                                                     |
| Sound     | ALC3246 (ALC256)                                                                                                 |
| Wireless  | [BCM94360NG](https://s.click.aliexpress.com/e/_9zltft) / [BCM94360CS2](https://s.click.aliexpress.com/e/_ALfsCV) |

### Software

| Component     | Version          |
| ------------- | ---------------- |
| Dell BIOS     | 1.2.0            |
| macOS         | 10.15.7 - 11.3   |
| SMBIOS        | iMac20,1         |
| OpenCore      | 0.6.5            |
| Lilu          | 1.5.2            |
| VirtualSMC    | 1.2.2            |
| WhateverGreen | 1.4.9            |
| IntelMausi    | 1.0.5            |
| AppleALC      | 1.5.9            |

### BIOS

You need to use [RU](http://ruexe.blogspot.com) to change following offsets:

| UEFI Variable | Offset | Value | Comment       |
| ------------- | ------ | ----- | ------------- |
| SaSetup       | 0xF5   | 0x2   | DVMT: 64M     |
| CpuSetup      | 0x3E   | 0x0   | CFG Lock: OFF |

And change following settings in BIOS:

| Item              | Value             |
| ----------------- | ----------------- |
| Intergrated NIC   | Enabled           |
| SATA Operation    | AHCI              |
| Primary Display   | Intel HD Graphics |
| TPM               | Disabled          |
| Secure Boot       | Disabled          |
| Intel SGX         | Disabled          |
| VT for Direct I/O | Disabled          |

## Working

- 4K UHD @ 60Hz for both DisplayPort
- All USB ports (2.0, 3.0 and Type C)
- Sleep, wake up and power nap
- Hardware acceleration
- Wi-Fi and Bluetooth
- AirPlay, Sidecar, Airdrop and Handoff
- Internal SATA ports

## Not working
- DRM

---

#### Similar projects
[weblogix/hackintosh-dell-precision-3240-compact](https://github.com/weblogix/hackintosh-dell-precision-3240-compact)
