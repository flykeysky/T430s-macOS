# Lenovo T430s macOS High Sierra

![About](https://raw.githubusercontent.com/dmitriypavlov/T430s-macOS/master/about.png)

This repository contains latest Clover UEFI, macOS kernel extensions, DSDT patches and support tools for using macOS High Sierra on **Lenovo T430s** (1600 х 900) laptop. 

None of another models are currently supported (while adding **X220**/**X230** support is possible in future).

### Warning
APFS is supported by this install (apfs.efi) but strongly discouraged as it causes malfunctions and long boot times with TRIM enabled on non-Apple SSD.

Use `sudo trimforce disable` with APFS startup volume as a workaround or consider switching back to HFS+.

Alternatively it is possible to do in-place upgrade from macOS Sierra (10.12) without APFS conversion with `/Applications/Install\ macOS\ High\ Sierra.app/Contents/Resources/startosinstall --converttoapfs NO`

### Current status

* macOS 10.13: **OK**
* UEFI boot: **OK**
* Battery: **OK** (minor % issues)
* CPU Speedstep: **OK**
* Sleep: **OK** (KP on wakeup with BT enabled)
* LID (sleep, wake): **OK**
* Hibernation: **NO**
* Intel GPU: **OK**
* Display Port: **OK**
* VGA: **NO**
* Brightness control: **OK**
* Status LED: **OK**
* Ethernet: **OK**
* WLAN: **NO** (use USB dongle)
* Bluetooth: **OK** (KP on wakeup with BT enabled)
* Keyboard: **OK**
* Touchpad: **OK**
* Trackpoint: **OK** (tracking issues)
* Camera: **OK**
* Sound (speakers): **OK**
* Sound (jack): **OK**
* Sound (DP/HDMI): **not tested**
* Microphone (built-in): **OK**
* Microphone (jack): **OK**
* USB2: **OK**
* USB3: **OK**
* Fingerprint: **NO**
* Lenovo Dock Station: **OK**
* DVD: **OK**

### Installation

1. Upgrade UEFI firmware to the latest available
2. Turn **SATA AHCI mode ON**, **UEFI Only Boot ON**, **Secure Boot OFF**, **CSM support OFF** in UEFI settings
3. Partition and format target drive as MacOS Extended (Journaled) using GUID Partition Map in Disk Utility
4. Use another Mac or Hackintosh to install Sierra on that partition via USB external enclosure (or make an installation USB drive using EFI directory from the repository)
5. Mount EFI partition in Terminal (**diskutil mount /dev/diskXs1** where **diskX** is target drive BSD device node which can be checked in Disk Utility), replace any existing **EFI** directory with one from the repository (the actual macOS partition stays untouched)
6. ...
7. PROFIT!

### Directories

* **[DSDT]** - extracted vanilla DSDTs, patched DSDTs, MacIASL patch script
* **[EFI]** - preconfigured Clover (this is the only one necessary)
* **[OTHER]** - support tools and scripts

### Software

* Clover [**r4233**](https://sourceforge.net/projects/cloverefiboot)
* Clover Configurator [**4.53.0.0**](http://mackie100projects.altervista.org)
* MaciASL [**RM-1.31**](https://bitbucket.org/RehabMan/os-x-maciasl-patchmatic/downloads)
* FakeSMC.kext [**6.25-333**](https://bitbucket.org/RehabMan/os-x-fakesmc-kozlek/downloads)
* ACPIBatteryManager.kext [**1.81.4**](https://bitbucket.org/RehabMan/os-x-acpi-battery-driver/downloads)
* AppleBacklightInjector.kext [**0.9.0**](https://github.com/RehabMan/HP-ProBook-4x30s-DSDT-Patch/tree/master/kexts/AppleBacklightInjector.kext)
* IntelMausiEthernet.kext [**2.3.0**](https://bitbucket.org/RehabMan/os-x-intel-network/downloads)
* VoodooPS2Controller.kext [**1.8.28**](https://bitbucket.org/RehabMan/os-x-voodoo-ps2-controller/downloads)
* BrcmBluetoothInjector.kext [**2.2.7**](https://bitbucket.org/RehabMan/os-x-brcmpatchram/downloads)
* AppleALC.kext [**1.1.4**](https://github.com/vit9696/AppleALC/releases)
* Lilu.kext [**1.1.7**](https://github.com/vit9696/Lilu/releases)
* IntelGraphicsFixup.kext [**1.1.6**](https://bitbucket.org/RehabMan/intelgraphicsfixup/downloads)
* CodecCommander.kext [**2.6.3**](https://bitbucket.org/RehabMan/os-x-eapd-codec-commander/downloads)

### Credits

The Hackintosh Community. All the credits go to the respective authors. None of the code is written or compiled by me.