# Hackintosh for Dell Precision 3240 Compact

## Specs

### Hardware

| Component | Tested                             |
| --------- | ---------------------------------- |
| CPU       | Core i5 10500 / 10600              |
| Chipset   | Intel W480                         |
| Graphics  | Intel UHD 630                      |
| Ethernet  | Intel I219-LM                      |
| SSD       | XPG SX8200 / WD SN750              |
| Memory    | G.SKILL 3200Mhz / SK Hynix 3200Mhz |
| Sound     | ALC3246 (ALC256)                   |
| Wireless  | BCM94360NG / BCM94360CS2           |
| Monitor   | LG 4K Ultra HD                     |

### Software

| Component     | Version |
| ------------- | ------- |
| Dell BIOS     | 1.1.1   |
| macOS         | 10.15.7 - 11.0 beta9 |
| SMBIOS        | iMac20,1|
| OpenCore      | 0.6.2   |
| Lilu          | 1.4.8   |
| VirtualSMC    | 1.1.7   |
| WhateverGreen | 1.4.3   |
| IntelMausi    | 1.0.4   |
| VoodooHDA     | 2.9.4   |

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

- 4K @ 60Hz for both DisplayPort
- All USB ports (2.0, 3.0 and Type C)
- Sleep, wake up and power nap
- Hardware acceleration
- Wi-Fi and bluetooth
- AirPlay, Sidecar, Airdrop and Handoff
- Internal SATA port


## Partial working
- Audio

## Not working
- DRM


