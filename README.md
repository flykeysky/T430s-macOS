# Lenovo T430s macOS Sierra

This repository contains latest Clover UEFI, macOS kernel extensions, DSDT patches and and support tools for using macOS Sierra on Lenovo T430s laptop.

**Current status**

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

**Installation**

1. Upgrade UEFI firmware to the latest available
2. Turn UEFI Boot on, Secure Boot off, CSM off in UEFI settings
3. Use another Mac or Hackintosh to install Sierra on drive via USB (or make an installation USB drive using EFI directory from the repository)
4. Mount EFI partition, replace EFI directory with one from the repository
5. ...
6. PROFIT!

**Directories**

**[DSDT]** - extracted vanilla DSDTs, patched DSDTs, MacIASL patch script

**[EFI]** - preconfigured Clover (this is the only one necessary)

**[OTHER]** - support tools and scripts

**Credits**

The Hackintosh Community. All the credits go to the respective authors. None of the code is written or compiled by me.

