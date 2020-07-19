# Hackintosh - Intel i7 7700k + Z270 Gaming K3
Clover EFI for a 100% stable 7700k + Z270 Hackintosh

**Latest working macOS**: 10.15.6

Complete hardware specs:
- i7 7700k OC to 4.8GHz
- Z270 Gaming K3
- Noctua NH-D15
- Radeon RX 5700 XT 8 GB
- Fenvi T919
- 64GB RAM - 3200 MHz DDR4

**SMBIOS**: iMacPro1,1

The system dual boots Windows 10

## Get it running
1. Create an macOS Catalina 10.15.x USB-Installer Stick
2. Install Clover bootloader to the same partition
3. Copy the EFI folder
4. Generate a new serial number, motherboard id and SMUUID (make sure serial number is invalid in order to iMessage/Facetime to work)
5. Boot the new macOS partition

## What works
- macOS Catalina and macOS Big Sur
- WiFi and Bluetooth + Airdrop + Sidecar
- Audio
- All USB ports
- 1Gbit Ethernet
- IGPU (must be enabled in BIOS and then in clover, i currently have it disabled but it works 100%)
- Temperature monitoring for everything except GPU (no 5700xt temp support in VirtualSMC)
- DRM content (Netflix, ATV+, Airplay 2 mirroring etc)
- Shutdown/Reboot/Update to newer macOS builds over time

## What doesn't work
- Sleep? Never got the chance to test it, my hackintosh is up 24/7

![alt text](https://i.imgur.com/TfIT7Nu.jpg "neofetch")
