# <div align="center"> Hackintosh-Thinkpad-T480s </div>

<p align="center">
<a href="https://github.com/felikafelix/Hackintosh-Thinkpad-T480s/tree/master/Ventura">
<img src="https://img.shields.io/badge/macOS-Ventura%2013.7.8-yellow?style=for-the-badge&logo=apple">
</a>
<a href="https://github.com/acidanthera/OpenCorePkg/releases/tag/1.0.5">
<img src="https://img.shields.io/badge/OpenCore-1.0.5-green?style=for-the-badge&logo=hackthebox">
</a>
<img src="https://img.shields.io/badge/Status-Stable-brightgreen?style=for-the-badge">
<a href="https://github.com/felikafelix/Hackintosh-Thinkpad-T480s/releases/tag/v3.0.1">
<img src="https://img.shields.io/github/downloads/felikafelix/Hackintosh-Thinkpad-T480s/total?style=for-the-badge">
</a>
</p>

## ⚠️ Attention
<p align="justify">I just upgraded my hacks to Sequoia, so v3 will be my last update for Ventura. <br>In case you want to upgrade from ventura to sequoia, im using the v3 release to upgrade from Ventura to Sequoia using <b>System Settings > General > Software Update</b>.</p>
The Adjustment i do on my EFI before upgrade

- Disable voltageshift script and its kext
- Cleaning the boot-args, add `-v` and `keepsyms=1`
-  Misc > Boot >
    - Show Picker = True
    - Timeout = 10
- Disable HiDPI
- After succesfully upgraded to sequoia, you can change the EFI to my sequoia release, and / or re-enable any kext & system patch disabled before upgrading.

<p align="justify">if you still want to stay on Ventura, maybe consider changing smbios to 16,3. From what i test on my Sequoia, the power and performance management is better.</p>

## 🚀 Usage

see [README](../README.md)

**Need help?** Open an [Issue](https://github.com/felikafelix/Hackintosh-Thinkpad-T480s/issues)

## 📌 Notes
i start adding HoRNDIS after installing Sequoia, so this Ventura EFI doesn't include the HoRNDIS yet (driver for android usb thetering), in case you need it:
1. Download [HoRNDIS](https://github.com/TomHeaven/HoRNDIS/releases) Kext
2. Add the kext to `EFI > OC > Kexts > here`,
3. Open config.plist with ProperTree, and do a snapshot `Command + R`, order the kext below airportltlwm or itlwm and save.
4. reboot

## 📸 Screenshot

- ### Desktop
<p align="center">
    <img src="Assets/Desktop.png">
</p>

- ### About This Mac
<p align="center">
    <img src="Assets/About This Mac.png">
</p>

- ### System & Graphic Info (VDA Decoder Fully Supported)
<p align="center">
    <img src="Assets/System Graphic Info.png">
</p>

- ### Display
<p align="center">
    <img src="Assets/Display.png">
</p>

- ### Apple Music Lossless Audio
<p align="center">
    <img src="Assets/Apple Music.png">
</p>

- ### Intel Power Gadget
    - Resource on Idle
    - Some light background apps running
<p align="center">
    <img src="Assets/Intel Power Gadget.png">
</p>

- ### Hardware Acceleration Check using ffmpeg
<p align="center">
    <img src="Assets/HW Acceleration.png">
</p>

- ### Undervolt Using Voltageshift
<p align="center">
    <img src="Assets/Voltageshift.png">
</p>

- ### Yoga SMC App
<p align="center">
    <img src="Assets/YogaSMC Pane.png">
</p>

- ### WiFi
<p align="center">
    <img src="Assets/WiFi.png">
</p>

- ### Bluetooth
<p align="center">
    <img src="Assets/Bluetooth.png">
</p>

- ### iMessage
<p align="center">
    <img src="Assets/iMessage.png">
</p>

- ### FaceTime
<p align="center">
    <img src="Assets/Facetime.png">
</p>

- ### App Store
<p align="center">
    <img src="Assets/App Store.png">
</p>

## 📜 License

This repo is licensed under the <a href="./LICENSE">MIT License</a>

OpenCore is licensed under the <a href="https://github.com/acidanthera/OpenCorePkg/blob/master/LICENSE.txt">BSD 3-Clause License</a>
