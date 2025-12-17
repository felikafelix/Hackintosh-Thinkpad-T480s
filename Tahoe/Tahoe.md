# <div align="center"> Hackintosh-Thinkpad-T480s </div>

<p align="center">
<a href="https://github.com/felikafelix/Hackintosh-Thinkpad-T480s/tree/master/Tahoe">
<img src="https://img.shields.io/badge/macOS-Tahoe%2016.0-lightblue?style=for-the-badge&logo=apple">
</a>
<a href="https://github.com/acidanthera/OpenCorePkg/releases/tag/1.0.5">
<img src="https://img.shields.io/badge/OpenCore-1.0.6-green?style=for-the-badge&logo=hackthebox">
</a>
<img src="https://img.shields.io/badge/Status-Stable-brightgreen?style=for-the-badge">
<a href="https://github.com/felikafelix/Hackintosh-Thinkpad-T480s/releases?q=MacOS+Tahoe&expanded=true">
<img src="https://img.shields.io/github/downloads/felikafelix/Hackintosh-Thinkpad-T480s/total?style=for-the-badge">
</a>
</p>

## Notes
My laptop screen is break, and i replace it with the one that haven't touchscreen. So starting from Tahoe, my EFI will not including the kext for touchscreen.
If you want to use the touchscreen, you can use the lates Sequoia EFI's kext for touchscreen references.

## Installation
1. Download the Tahoe Install EFI from [Tahoe Install EFI](https://github.com/felikafelix/Hackintosh-Thinkpad-T480s/releases/tag/v6.0.1). or you can setup your own EFI using [OpCore-Simplify](https://github.com/lzhoang2801/OpCore-Simplify)
2. Download the MacOS Tahoe Recovery Image using macrecovery.py and place the recover folder to the USB same as the EFI folder.
```python3 ./macrecovery.py -b Mac-CFF7D910A743CAAF -m 00000000000000000 -os latest download```
3. Installation (on my case) take around 2 hours to finish and get to the desktop. Just be patient.
4. After installation, switch to [Latest EFI for Tahoe](https://github.com/felikafelix/Hackintosh-Thinkpad-T480s/releases/tag/v7.0.1) and than you can setup the post install, see [Post Installation](../README.md#postinstall).
5. Don't forget to set your own SMBIOS, see [SMBIOS](../README.md#smbios)
6. Setup your own CPUFriendDataProvider, see [CPUFriendDataProvider](../README.md#cpufrienddataprovider)
7. Setup your USB Mapping, see [USB Mapping](../README.md#usb-mapping)

## 📸 Screenshot

- ### Desktop
<p align="center">
    <img src="./Assets/Desktop.png">
</p>

- ### About This Mac
<p align="center">
    <img src="./Assets/About This Mac.png">
</p>

- ### System & Graphic Info (VDA Decoder Fully Supported)
<p align="center">
    <img src="./Assets/System Graphic Info.png">
</p>

- ### Display (Better Display)
<p align="center">
    <img src="./Assets/Display.png">
</p>

- ### Apple Music Lossless Audio
<p align="center">
    <img src="./Assets/Apple Music.png">
</p>

- ### Screen Mirroring
<p align="center">
    <img src="./Assets/Screen Mirroring.png">
</p>

- ### AirPlay
<p align="center">
    <img src="./Assets/AirPlay.png">
</p>

- ### Intel Power Gadget
    - Resource and Temperature
    - Some background apps running
<p align="center">
    <img src="./Assets/Intel Power Gadget.png">
</p>

- ### Hardware Acceleration Check using ffmpeg
<p align="center">
    <img src="./Assets/HW Acceleration.png">
</p>

- ### Undervolt Using Voltageshift
<p align="center">
    <img src="./Assets/Voltageshift.png">
</p>

- ### Yoga SMC App
<p align="center">
    <img src="./Assets/YogaSMC Pane.png">
</p>

- ### WiFi
<p align="center">
    <img src="./Assets/WiFi.png">
</p>

- ### Bluetooth
<p align="center">
    <img src="./Assets/Bluetooth.png">
</p>

- ### iMessage
<p align="center">
    <img src="./Assets/iMessage.png">
</p>

- ### FaceTime
<p align="center">
    <img src="./Assets/Facetime.png">
</p>

- ### App Store
<p align="center">
    <img src="./Assets/App Store.png">
</p>