# hackintosh-dell-precision-3640-comet-lake-opencore

## What works

* OpenCore (0.7.1)
* Supported OS
    * macOS Big Sur (up to 11.5)
* All USB Ports at full speed (USB 3.2) (via Custom USB Mapping)
* Intel UHD Graphics 630 - 4K UHD @ 60hz (Displayport)
* Full Metal hardware acceleration
* Sleep, wake and power nap
* Audio - Internal Speaker, Displayport/HDMI, and front audio port

## What's not working

Nothing!

## Installation

* Mount EFI Partition
* Copy `EFI` folder to EFI Partition root `(/)`
* Replace the following values in `EFI/OC/config.plist` with generated values from [GenSMBios](https://github.com/corpnewt/GenSMBIOS)
    * PlatformInfo --> Generic --> SystemSerialNumber
    * PlatformInfo --> Generic --> MLB
    * PlatformInfo --> Generic --> SystemUUID

## Bios Settings

Update the following settings in BIOS with [RU.exe](http://ruexe.blogspot.com/) or [bios-extraction-guide (Dell)](https://github.com/dreamwhite/bios-extraction-guide/tree/master/Dell)
Note: CFG Lock off you can use the opencore tools CFGLock.efi from the main menu.

| UEFI Variable | Offset | Value | Comment       |
| ------------- | ------ | ----- | ------------- |
| SaSetup       | 0xF5   | 0x2   | DVMT: 64M     |
| CpuSetup      | 0x3E   | 0x0   | CFG Lock: OFF |


Update the following settings in BIOS:

| Item              | Value             |
| ----------------- | ----------------- |
| Intergrated NIC   | Enabled           |
| SATA Operation    | AHCI              |
| Primary Display   | Intel HD Graphics |
| TPM               | Disabled          |
| Secure Boot       | Disabled          |
| Intel SGX         | Disabled          |
| VT for Direct I/O | Disabled          |


## Notes


## Tested Configuration

| Component | Tested                             |
| --------- | ---------------------------------- |
| Bios Ver  | 1.2.3                              |
| CPU       | Core i7 10700                      |
| Chipset   | Intel W480                         |
| Graphics  | Intel UHD 630                      |
| Ethernet  | Intel I219-LM                      |
| NVME      | WD SN550 (2)                       |
| Display   | Dell 2718qm 4K Monitor             |
| VideoCard | Radeon RX 460                      |
| Memory    | Crucial 32GBx1 DDR4 2600 MT/s      |
| Sound     | ALC3246 (ALC256)                   |



# Links
* [dell-precision-3240-compact-hackintosh](https://github.com/billzhong/dell-precision-3240-compact-hackintosh/)

* [hackintosh-dell-precision-3240-compact-comet-lake-opencore](https://github.com/weblogix/hackintosh-dell-precision-3240-compact-comet-lake-opencore)
