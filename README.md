# Hackintosh-EFI-X570I

Working EFI for dualboot with Bigsur 11.3 and Windows 10


Hardware:
---------
	.- Motherboard: ASUS ROG STRIX X570-I Gaming (BIOS version: 3801 Beta)
	.- Processor: RYZEN 7 3700 X
	.- GPU/Video Card: GIGABYTE RX 5700 XT OC Gaming - 8GB
	.- Storage: NVME M.2 SAMSUNN 970 EVO PLus 500GB
	.- Memory: 2 x Corsair Vengeance LPX DDR4 3600 16GB  - Total 32GB
	.- Wifi & Bluetooth : Originally motherboard comes with Intel AX200 (switched to BCM94360NG)
	.- Monitor: LG 49WL95C-W with integrated speakers (Display port with audio)

Booter & EFI Details
---------------------
	.- Opencore 0.6.8
	.- ACPI folder contents:
		.- SSDT-EC-USBX.aml
		.- SSDT-GPRW.aml
		.- SSDT-HPET.aml
		.- SSDT-SBUS-MCHC.aml
	.- Drivers:
		.- HfsPlus.efi
		.- OpenCanopy.efi
		.- OpenRuntime.efi
		.- OpenCore.efi (at OC folder)
	.- Kexts:
		.- AMDRyzenCPUPowerManagement.kext
		.- AppleMCEReporterDisabler.kext
		.- Lilu.kext
		.- NVMeFix.kext
		.- SmallTreeIntel82576.kext
		.- SMCAMDProcessor.kext
		.- USBPorts.kext
		.- VirtualSMC.kext
		.- WhateverGreen.kext
		.- NOTA: not using internal sound card so AppleALC.kext not present. Using display port audio to Monitor speakers.

OS versions
--------------
	.- Dual boot:
		.- Windows 10
		.- BigSur 11.3 (using iMacPro1,1 SMBIOS)


Motherboard BIOS Version & Settings
-----------------------------------
	.- BIOS version: 3801 Beta
	.- BIOS Settings:
		.- Fast Boot: Disabled
		.- Internal sound card: disabled (using audio from display port directly to monitor)
		.- CSM: disabled
		.- PCI mode: 3x
		.- Above 4G Decoding : Enabled
		.- Resize BAR: disabled
		.- TPM : enabled  (and bitlocker active in Windows partition)


What does work:
---------------
	.- Mostly everything
	.- USB Mapping
	.- Wifi
	.- Bluetooth (even after wake)
	.- Sleep / Wake
	.- Using MenuMeters and HWMonitor to gather different metrics from procesor, disk, network,temperatures, etc
	.- etc


What does not work
-------------------
	.- Microphone from internal sound card (but it is disabled)
	.- Sidecar (always report timeout from iPad when trying to connect)
