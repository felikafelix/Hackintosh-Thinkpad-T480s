# macOS Ventura Notes

<p align="center">
<img src="https://img.shields.io/badge/macOS-Ventura%2013.7-f39f21?style=for-the-badge&logo=apple">
<img src="https://img.shields.io/badge/OpenCore-1.0.5-04a0fc?style=for-the-badge&logo=hackthebox">
<img src="https://img.shields.io/badge/Status-Stable-brightgreen?style=for-the-badge">
</p>

---

## ⚠️ Notice

I've upgraded to Sequoia so **v3 is my last Ventura release**.

If you want to stay on Ventura, consider changing SMBIOS to `MacBookPro16,3` for better power/performance management.

---

## 🔄 Upgrading to Sequoia

Before upgrading from Ventura to Sequoia:

1. **Disable VoltageShift** - Remove script and kext
2. **Clean boot-args** - Add `-v` and `keepsyms=1`
3. **BIOS settings**:
   - `Misc > Boot > Show Picker` = True
   - `Misc > Boot > Timeout` = 10
4. **Disable HiDPI** if using one-key-hidpi
5. **Upgrade** via System Settings > General > Software Update
6. After upgrade, switch to Sequoia EFI and re-enable kexts/patches

---

## 📝 Additional Notes

### HoRNDIS (Android USB Tethering)

Ventura EFI doesn't include HoRNDIS. To add it:

1. Download [HoRNDIS](https://github.com/TomHeaven/HoRNDIS/releases)
2. Add kext to `EFI/OC/Kexts`
3. Open config.plist with ProperTree, run snapshot (`⌘+R`)
4. Order kext below AirportItlwm or itlwm
5. Reboot

---

## 📸 Screenshots

<details>
<summary>Click to expand</summary>

### Desktop
<p align="center"><img src="../../assets/screenshots/ventura/Desktop.png"></p>

### About This Mac
<p align="center"><img src="../../assets/screenshots/ventura/About This Mac.png"></p>

### System & Graphics Info
<p align="center"><img src="../../assets/screenshots/ventura/System Graphic Info.png"></p>

### Display
<p align="center"><img src="../../assets/screenshots/ventura/Display.png"></p>

</details>

---

[← Back to README](../../README.md)
