# Lenovo T430s macOS Sierra

![alt text](http://url/to/img.png)

This repository contains latest Clover UEFI, macOS kernel extensions, DSDT patches and support tools for using macOS Sierra on **Lenovo T430s** (1600 х 900) laptop. 

None of another models are currently supported (while adding **X220**/**X230** support is possible in future).

### Current status

* macOS 10.12.6: **OK**
* UEFI boot: **OK**
* Battery: **OK** (minor % issues)
* CPU Speedstep: **OK**
* Sleep: **OK**
* LID (sleep, wake): **OK**
* Hibernation: **NO**
* Intel GPU: **OK**
* Display Port: **OK**
* VGA: **NO**
* Brightness control: **OK**
* Status LED: **OK**
* Ethernet: **OK**
* WLAN: **NO** (use USB dongle)
* Bluetooth: **OK**
* Keyboard: **OK**
* Touchpad: **OK**
* Trackpoint: **OK** (tracking issues)
* Camera: **OK**
* Sound (speakers): **OK**
* Sound (jack): **OK**
* Sound (DP/HDMI): **not tested**
* Microphone (built-in): **OK**
* Microphone (jack): **not tested**
* USB2: **OK**
* USB3: **OK**
* Fingerprint: **NO**
* Dock Station: **not tested**
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

**[DSDT]** - extracted vanilla DSDTs, patched DSDTs, MacIASL patch script

**[EFI]** - preconfigured Clover (this is the only one necessary)

**[OTHER]** - support tools and scripts

### Credits

The Hackintosh Community. All the credits go to the respective authors. None of the code is written or compiled by me.

****