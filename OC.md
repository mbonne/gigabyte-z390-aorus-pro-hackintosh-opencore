# OpenCore EFI

Compile latest OC from [here](https://github.com/acidanthera/OpenCorePkg)

## ACPI 
- SSDT-EC-USBX.aml
- SSDT-PLUG.aml
- SSDT-HPET.aml
- SSDT-PMC.aml

## Driver
- [HfsPlus.efi](https://github.com/acidanthera/OcBinaryData/raw/master/Drivers/HfsPlus.efi)
- OpenRuntime.efi - Included in OpenCore package
- OpenCanopy.efi - Included in OpenCore package
- AudioDxe.efi - Included in OpenCore package

## Kext - Compile on your own
- [Lilu.kext](https://github.com/acidanthera/Lilu)
- [VirtualSMC.kext](https://github.com/acidanthera)
- [WhateverGreen.kext](https://github.com/acidanthera)
- [AppleALC.kext](https://github.com/acidanthera)
- [IntelMausi.kext](https://github.com/acidanthera)
- USBPorts.kext - Grab from your current machine
- SMCProcessor.kext - Included in VirtualSMC package
- SMCSuperIO.kext - Included in VirtualSMC package

## Tools
- [modGRUBShell.efi](https://github.com/datasone/grub-mod-setup_var/releases/download/1.1/modGRUBShell.efi)
- OpenShell.efi - Included in OpenCore package
- ResetSystem.efi - Included in OpenCore package
- CleanNvram - Included in OpenCore package

## config.plist

- Use `config_usb.plist` for installation media(USB).
- Use `config.plist` for internal boot disk.

## EFI Folder Structure


### SSD/NVME/HDD
```
EFI
├── BOOT
│   └── BOOTx64.efi
└── OC
    ├── ACPI
    │   ├── SSDT-EC-USBX.aml
    │   ├── SSDT-HPET.aml
    │   ├── SSDT-PLUG.aml
    │   └── SSDT-PMC.aml
    ├── Bootstrap
    │   └── Bootstrap.efi
    ├── Drivers
    │   ├── AudioDxe.efi
    │   ├── HfsPlus.efi
    │   ├── OpenCanopy.efi
    │   └── OpenRuntime.efi
    ├── Kexts
    │   ├── AppleALC.kext
    │   ├── IntelMausi.kext
    │   ├── Lilu.kext
    │   ├── SMCProcessor.kext
    │   ├── SMCSuperIO.kext
    │   ├── USBPorts.kext
    │   ├── VirtualSMC.kext
    │   └── WhateverGreen.kext
    ├── OpenCore.efi
    ├── Tools
    │   ├── CleanNvram.efi
    │   ├── OpenShell.efi
    │   ├── ResetSystem.efi
    │   └── modGRUBShell.efi
    └── config.plist

```
