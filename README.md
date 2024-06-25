# [OpenCore](https://github.com/acidanthera/OpenCorePkg) EFI
A prebuilt EFI for installing macOS Big Sur on the HP 280 G1.

Special thanks to sonic89 and Krazy-Killa from the /r/Hackintosh Paradise server!

**OpenCore Version:** 1.0.0 from May 9, 2024.

# IMPORTANT WARNING
To avoid problems i removed the SMBIOS Serials, you can generate yours by following [this](https://dortania.github.io/OpenCore-Install-Guide/config.plist/haswell.html#platforminfo) guide.

It's really easy and it doesn't take long.

# Working features:

- QE/CI of Intel HD 4400
- Audio
- Ethernet
- Mapped USBs
- Android USB Tethering (idk if it works with iOS)

# Bugs

- It's probably only for me because i use an adapter but the video glitches sometimes.

# Specifications of the PC

Component | Model
--- | --- 
Desktop | HP 280 G1
CPU | Intel i3 4160 Quad Core
iGPU | Intel HD Graphics 4400
Audio Codec | RealTek ALC221
Ethernet Chipset | RealTek RTL8168/8111 PCI-E Gigabit Ethernet NIC

# Included Drivers:

Drivers | Description
--- | ---
HfsPlus | Needed to show HFS drives.
OpenRuntime | Required to boot the EFI.
ResetNvramEntry | Needed to reset the system's NVRAM. (Optional) 
FirmwareSettingsEntry | Used to reboot into the system's UEFI settings (Optional)

# Installed Kexts

Kext | Description
