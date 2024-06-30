<img src="/Docs/Logo1.jpg" width="875" height="180"/>

# [OpenCore](https://github.com/acidanthera/OpenCorePkg) EFI

**A prebuilt EFI for installing macOS Big Sur on the HP 280 G1.**

(If you need to make any changes to the EFI, follow this guide [here](https://dortania.github.io/OpenCore-Install-Guide/).)

**OpenCore Version:** 1.0.0 from May 9, 2024.

# IMPORTANT WARNING

To avoid problems i removed the SMBIOS Serials, you can generate yours by following [this](https://dortania.github.io/OpenCore-Install-Guide/config.plist/haswell.html#platforminfo) guide.

It's really easy and it doesn't take long.

# Working features:

- Power Management
- QE/CI of Intel HD 4400
- Audio
- Ethernet
- Mapped USBs
- Android USB Tethering support

# Bugs

- Sleep causes screen flickering.
- Glitching video with trasparency effects, photos and Siri.

# Specifications of the PC

Component | Model
--- | --- 
Desktop | HP 280 G1 MT
Chipset | Intel H81
CPU |  Intel(R) Core i3-4160 3.60GHz - **Haswell**
iGPU | Intel HD Graphics 4400 - 1GB
USB Ports | Front: 2x USB 2.0 - Back: 4x USB 2.0 + 2x USB 3.0
Audio Codec | RealTek HD Audio - ALC221
Ethernet Controller | RealTek RTL8168/8111 PCI-E Gigabit Ethernet NIC

# ACPI Tables

Name | Description
--- | ---
SSDT-PLUG | For fixing Power Management
SSDT-EC | For faking the Embedded Controller
SSDT-EHCx_OFF | Needed to remove the extra USBs from the mapping

# Included Drivers:

Drivers | Description
--- | ---
HfsPlus | Needed to show HFS drives.
OpenRuntime | Required to boot the EFI.
OpenCanopy | Used to load the boot GUI.
ResetNvramEntry | Needed to reset the system's NVRAM. (Optional) 
FirmwareSettingsEntry | Used to reboot into the system's UEFI settings. (Optional)

These drivers are included with the OpenCore package, you can update them by downloading it [here](https://github.com/acidanthera/OpenCorePkg/releases/).

# Installed Kexts

Kext | Description
--- | ---
[AppleALC](https://github.com/acidanthera/AppleALC/releases) | Required for patching AppleHDA, without this the audio will not work.
[HoRNDIS](https://github.com/jwise/HoRNDIS/releases/) | Used for Android USB Tethering (Optional).
[Lilu](https://github.com/acidanthera/Lilu/releases) | Needed to load kexts like AppleALC, WhateverGreen, VirtualSMC, etc.
[RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X/release) | Needed to make Ethernet work.
[VirtualSMC](https://github.com/acidanthera/VirtualSMC/releases) | Emulates the Mac's SMC chip, required to boot the OS.
[SMCProcessor](https://github.com/acidanthera/VirtualSMC/releases) | Used to check the CPU temperatures. (Optional)
[SMCSuperIO](https://github.com/acidanthera/VirtualSMC/releases) | Used to check the fans speeds. (Optional)
[USBMap](https://github.com/corpnewt/USBMap) | Needed for USB ports to work.
[WhateverGreen](https://github.com/acidanthera/WhateverGreen/releases/) | Needed for GPUs patching and QE/CI support.

# Credits
- [Dortania](https://dortania.github.io/) - For the amazing OpenCore guides.
- sonic89 - For helping me a lot building this EFI, without him this wouldn't exist.
- Krazy-Killa from /r/Hackintosh Paradise - For helping me with the QE/CI


