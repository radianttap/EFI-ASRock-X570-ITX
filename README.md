OpenCore ver 0.6.0 · Catalina 10.15.6

# ASRock X570 ITX/TB3 + Ryzen 5 3600 + RX 570 → iMacPro1,1

Current hardware:

- AMD [Ryzen 5 3600](https://www.amd.com/en/products/cpu/amd-ryzen-5-3600)
- [ASRock X570 Phantom Gaming-ITX/TB3](https://www.asrock.com/mb/AMD/X570%20Phantom%20Gaming-ITXTB3/) motherboard
- Sapphire [Nitro+ RX570 8GB](https://www.sapphiretech.com/en/consumer/nitro-rx-570-8g-g5-oc) graphics card
- Intel WiFi card (AX200) replaced with [Fenvi BCM94352Z](https://www.aliexpress.com/item/Dual-band-Wireless-Hackintosh-BCM94352Z-WIFI-Card-Broadcom-bcm94352-M-2-Bluetooth-4-0-Network-NGFF/32464748097.html)
- Corsair [Vengeance LPX](https://www.corsair.com/us/en/Categories/Products/Memory/VENGEANCE-LPX/p/CMK16GX4M2B3200C16) 16 GB (2 x 8 GB) DDR4 3200MHz CL16
- Nouvolo [Steck v1.1](https://www.nouvolo.com) SFF case
- Corsair [SF600 Platinum](https://www.corsair.com/us/en/Categories/Products/Power-Supply-Units/Power-Supply-Units-Advanced/SF-Series/p/CP-9020182-NA) SFX PSU
- Noctua [NH-L9x65](https://noctua.at/en/products/cpu-cooler-retail/nh-l9x65) CPU cooler
- Noctua [NF-A12x25](https://noctua.at/en/products/fan/nf-a12x25-pwm) case fan
- Noctua [NF-A9 PWM](https://noctua.at/en/products/fan/nf-a9-pwm) fan (used it to replace 9x14 on the CPU cooler).
- ADATA [XPG 8200 Pro](https://www.xpg.com/us/feature/583/) 1TB NVMe SSD

## Usage

In order to use this properly, you need to [update SMBIOS stuff](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html#generate-a-new-serial) with your own, inside `config.plist`

### What’s working

Almost everything.

- NVMe SSD works out of the box.
- Radeon GPU work out of the box.
- WiFi works with AirportBrcmFixup kext.
- Bluetooth works with additional 3 kexts.
- All media services (Plex, Netflix in Safari, iTunes, Apple TV+ etc). All are fully hardware-accelerated.
- 4K HDMI with HDR, Dolby.
- iMessage, iCloud, Keychain, all of it.
- System Integrity Protection (SIP) fully enabled.

### What’s not working

- Sleep / wake
- Xcode’s watchOS Simulator and even compiling some watchOS SDK projects
- Apple Watch unlock
- Thunderbolt 3 (gave up on this entirely)

## Notes

Use at your own risk. 

- All `.efi` drivers and `.kext` are `-DEBUG` builds from the respective packages. 
- Boot is verbose to simplify troubleshooting.
- OpenCanopy is up and running.
- I don’t boot Windows 10 using OC, thus I can’t guarantee it will work. I have Win 10 installed on separate SSD and switch using Boot Menu.

Don’t ask for help here; use appropriate [AMD-OSX](https://amd-osx.com) forums and Discord channels (both are linked there).

