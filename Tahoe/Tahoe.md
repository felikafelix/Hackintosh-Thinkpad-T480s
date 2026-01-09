# <div align="center"> Hackintosh-Thinkpad-T480s </div>

<p align="center">
<a href="https://github.com/felikafelix/Hackintosh-Thinkpad-T480s/tree/master/Tahoe">
<img src="https://img.shields.io/badge/macOS-Tahoe%2026.0-lightblue?style=for-the-badge&logo=apple">
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

### V9 EFI for Tahoe
finally i have replaced my current display with the one that have touchscreen, so V9 will start adding touchscreen support again. 

Also i have added some change to thunderbolt controller, thanks to [@aerhazu](https://github.com/aerhazu) at least it now detected on IORegistryExplorer. I still can't test it, because i don't have the thunderbolt device. so it will helpful if you can test it and let me know if it works.

<p align="center">
    <img src="./Assets/ThunderboltIOREG.png">
</p>

What did i test on thunderbolt port and works:
- Flashdisk using USB to Type C
- External SSD using USB to Type C
- Connect iPhone using Type C to Lightning (sync iphone and personal hotspot)

Btw, my Thunderbolt Path is Located at `RP05`, if you have difference path, you can edit the path on TB3 SSDT and ACPI PATCH to match your own.

### V6 EFI for Tahoe
My laptop screen is break, and i replace it with the one that haven't touchscreen. So starting from Tahoe, my EFI will not including the kext for touchscreen.
If you want to use the touchscreen, you can use the lates Sequoia EFI's kext for touchscreen references.

## Installation

1. Download the Tahoe Install EFI from [Tahoe Install EFI](https://github.com/felikafelix/Hackintosh-Thinkpad-T480s/releases/tag/v6.0.1). or you can setup your own EFI using [OpCore-Simplify](https://github.com/lzhoang2801/OpCore-Simplify).
2. Download the MacOS Tahoe Recovery Image using macrecovery.py and place the recover folder to the USB same as the EFI folder.
```python3 ./macrecovery.py -b Mac-CFF7D910A743CAAF -m 00000000000000000 -os latest download```.    
3. Installation (on my case) take around 2 hours to finish and get to the desktop. Just be patient.
4. After installation, switch to [Latest EFI for Tahoe](https://github.com/felikafelix/Hackintosh-Thinkpad-T480s/releases/tag/v7.0.1) and than you can setup the post install, see [Post Installation](../README.md#postinstall).
5. Don't forget to set your own SMBIOS, see [SMBIOS](../README.md#smbios), use MacBookPro16,4.
6. Setup your own CPUFriendDataProvider, see [CPUFriendDataProvider](../README.md#cpufrienddataprovider).
7. Setup your USB Mapping, see [USB Mapping](../README.md#usb-mapping).
8. To make the audio works, use [MyKextInstaller](https://github.com/Mirone/MyKextInstaller) to install AppleHDA.

## Updates
1. Since v8, i change my SMBios from MacBookPro16,1 to MacBookPro16,4, because i found that the performance and thermal management is better.
2. if you using SMBIOS MacBookPro16,1 and want to change to MacBookPro16,4, please disable filevault first for safety.
3. **My Personal Case**
    - i can't turn off the filevault, because the encrypting process is stuck.
    - Using command ```fdesetup status``` it shows that the encrypting process isn't changed.
    - Using command ```diskutil apfs list``` it shows that the encrypting process is paused.
    - If you facing the same issue, follow this method
        - run ```sudo fdesetup list``` to get the uuid of your mac user, it will be something like ```youruser, 12345678-1234-1234-1234-123456789012```.
        - reboot to recovery mode, you can enter recovery mode by selecting it on opencore picker, or hold commmand/windows + r.
        - On Disk Utility, select your data disk that locked (usually greyyed out), and mount it. Close the Disk Utility.
        - On the Menubar, Click on Utilities > Terminal.
        - Run ```diskutil apfs list```, see there will be a partition that have like ```Encrypted``` or ```Encryption Progress``` something like that. look for the one that has Data disk name, not system disk name.
        - In my case, the name of Data partition is ```disk3s1```.
        - for APFS file system, run ```/usr/libexec/apfsd```. For others, run ```/usr/libexec/corestoraged```.
        - in my case, im using APFS file system, so i run ```/usr/libexec/apfsd```. While the command running, open new terminal window.
        - In the new terminal window, run ```diskutil apfs list``` (For APFS file system) or ```diskutil cs list``` (for others).
        - now, run again ```diskutil apfs list```, you would see that the encrypting process is now running. the ```paused``` status is gone. Just let the encrypting process finish.
        - after the encrypting process finish, you can decrypt / disable filevault by running ```diskutil apfs decryptVolume {yourdiskname} -user {youruseruuid}```
        - for example ```diskutil apfs decryptVolume disk3s1 -user 12345678-1234-1234-1234-123456789012```.
        - after the decrypt process finish, you can reboot to normal mode, now the filevault should be disabled, and you can change the SMBIOS to MacBookPro16,4.
        

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
