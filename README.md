# Hackintosh - Intel i7 7700k + Z270 Gaming K3
Clover EFI for a 100% stable 7700k + Z270 Hackintosh

**Latest working macOS**: 10.15.6

Complete hardware specs:
- i7 7700k OC to 4.8GHz
- Gigabyte Z270 Gaming K3
- Noctua NH-D15
- Radeon RX 5700 XT 8 GB
- Fenvi T919
- 64GB RAM - 3200 MHz DDR4
- 500GB Kingston A2000 NVMe PCIe SSD (macOS Partition) + other HDDs for storage (shared with Windows)

**SMBIOS**: iMacPro1,1

The system dual boots Windows 10

## Get it running
1. Create an macOS Catalina 10.15.x USB-Installer Stick ([how?](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/building-the-usb-installer))
2. Install Clover bootloader to the same partition ([how?](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/clover-setup))
3. Copy the EFI folder ([how?](https://www.youtube.com/watch?v=arebuadFSuw))
4. Generate a new serial number, motherboard id and SMUUID (make sure serial number is **invalid** in order to iMessage/Facetime to work) ([how?](https://hackintosh.gitbook.io/-r-hackintosh-vanilla-desktop-guide/config.plist-per-hardware/skylake#explanation-5) + [this tool](http://mackie100projects.altervista.org/download-clover-configurator/))
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

## Kexts used:
- AppleALC (audio)
- AtherosE2200Ethernet (ethernet)
- Lilu + Whatevergreen (Audio helper, DRM support, GPU helper)
- VirtualSMC + addons (you cannot boot without this + temperature support)
- USBInjectAll (make USB ports work)

## Drivers used:
- ApfsDriverLoader (make APFS drives discoverable in Clover bootloader)
- FSInject (required driver to inject kexts)
- HFSPlus (optional, make HFS drives discoverable in Clover bootloader if you want to use Mojave or older macOS versions)
- NvmExpressDxe (required to boot and use a "non-Apple" NVM SSD)
- OsxAptioFix3Drv (required to patch some motherboard stuff in order to boot and not kernel panic)
- PartitionDxe (optional, support for custom partition types)
- Ps2MouseDxe (optional, support for non-bluetooth mouse and keyboard)
- VirtualSmc (required, works with the kext)

## Thanks/Credits
- tonymacx86
- insanelymac


**Fuck /r/Hackintosh for not allowing EFI sharing**
