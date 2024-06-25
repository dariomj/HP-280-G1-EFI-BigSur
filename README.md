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
- Android USB Tethering support

# Bugs

- Glitching video (could be me for using an adapter)

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
--- | ---
[AppleALC](https://github.com/acidanthera/AppleALC/releases) | Required for patching AppleHDA, without this the audio will not work.
[HoRNDIS](https://github.com/jwise/HoRNDIS/releases/tag/rel9.2) | Used for Android USB Tethering (Optional).
[IntelBluetoothFirmware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases/tag/v2.4.0) | Used to make Bluetooth work into macOS (Optional).
[IntelBluetoothInjector](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases/tag/v2.4.0) | Required for IntelBluetoothFirmware.
[IntelBTPatcher](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases/tag/v2.4.0) | Same as above.
[Lilu](https://github.com/acidanthera/Lilu/releases) | Needed to load kexts like AppleALC, WhateverGreen, VirtualSMC, etc.
[RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X/release) | Needed to make Ethernet work.
[VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases) | Emulates the Mac's SMC chip, required to boot the OS.
[SMCProcessor](https://github.com/acidanthera/VirtualSMC/releases) | Used to check the CPU temperatures.
[SMCSuperIO](https://github.com/acidanthera/VirtualSMC/releases) | Used to check the fans speeds.
[USBMap](https://github.com/corpnewt/USBMap) | Needed for USB ports to work.
[WhateverGreen](https://github.com/acidanthera/WhateverGreen/releases/tag/1.6.6) | Needed for GPUs patching and QE/CI support.


