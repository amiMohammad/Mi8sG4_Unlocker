# Mi8sG4-Unlocker — Fully Automatic Edition

<p align="center">
  <b>Windows one-click bootloader (BL) unlock assistant for Xiaomi devices with Snapdragon 8s Gen 4</b>
</p>

<p align="center">
  <a href="https://t.me/Kernix_dev">
    <img src="https://img.shields.io/badge/Telegram-Kernix_dev-26A5E4?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>
  <img src="https://img.shields.io/badge/Platform-Windows-blue?style=for-the-badge&logo=windows&logoColor=white" alt="Windows">
  <img src="https://img.shields.io/badge/SoC-Snapdragon%208s%20Gen%204-red?style=for-the-badge" alt="Snapdragon 8s Gen 4">
  <img src="https://img.shields.io/badge/System-HyperOS%202%2B-orange?style=for-the-badge" alt="HyperOS 2+">
  <img src="https://img.shields.io/badge/Status-Active-success?style=for-the-badge" alt="Status">
</p>

---

## 📌 Project Overview

**Mi8sG4-Unlocker** is a **Windows fully-automatic bootloader (BL) unlock assistant** for Xiaomi devices based on the **Snapdragon 8s Gen 4** platform.

This project provides an automated workflow via the `toUnlock.bat` script. It bundles an ADB / Fastboot environment, device-specific resources, status-checking tools, and debug entry points to complete the BL unlock process under HyperOS.

Users only need to fully extract the package on Windows, connect their device, and run `toUnlock.bat`; follow the script prompts to complete the automated flow.

> For help or discussion, join the channel:  
> **https://t.me/Kernix_dev**

---

## ✨ Key Features

- **One-click Windows run**  
  Run `toUnlock.bat` to start the automated workflow.

- **Targeting Snapdragon 8s Gen 4 platform**  
  Adapted specifically for Xiaomi devices on the new 8s Gen 4 platform.

- **Multi-model precise matching**  
  The script selects model-specific resources from the corresponding directories.

- **Built-in ADB / Fastboot**  
  No need to separately install Android Platform Tools — just extract and use.

- **BL status detection**  
  Includes `check-unlock.bat` to check bootloader lock and engineering ABL status.

- **Integrated debug tools**  
  Includes `adb-tool.bat` for convenient ADB / Fastboot debugging commands.

- **Lightweight resource package**  
  Bundles only necessary ABL / GPT resources to reduce unnecessary file size.

---

## 📱 Supported Models

The following three Snapdragon 8s Gen 4 devices are currently supported:

### Redmi series

- **Redmi Turbo 4 Pro**

### Xiaomi series

- **Xiaomi Civi 5 Pro**

### Tablet series

- **Xiaomi Pad 8**

---

## 🧩 System Requirements

Please confirm your device meets the following requirements before use.

| Item | Requirement |
|---|---|
| PC OS | Windows 10 / Windows 11 |
| Phone OS | HyperOS 2.0 or later |
| Device platform | Snapdragon 8s Gen 4 |
| Connection | USB data cable |
| Debug status | USB debugging enabled |

---

## ⚠️ Compatibility Notes

### System Version

Supported:

```text
HyperOS 2.0 and above
```

Not supported:

```text
HyperOS 1.0 and earlier
```

HyperOS 1.0 and earlier lack necessary low-level system components, so this tool's flow will not work correctly on those older versions.

---

## 📦 Release Package Structure

```text
Mi8sg4-unlock-windows-auto.zip
├── 8735-Ennea.img
├── 8sg4-unlock.bat
├── toUnlock.bat
├── check-unlock.bat
├── adb-tool.bat
├── adb.exe
├── fastboot.exe
├── AdbWinApi.dll
├── AdbWinUsbApi.dll
└── unlockFolder/
    ├── factoryImages/
    │   ├── Redmiturbo4pro/
    │   │   └── images/
    │   │       ├── abl.elf
    │   │       └── gpt_both4.bin
    │   ├── Xiaomicivi5pro/
    │   │   └── images/
    │   │       ├── abl.elf
    │   │       └── gpt_both4.bin
    │   └── Xiaomipad8/
    │       └── images/
    │           ├── abl.elf
    │           └── gpt_both4.bin
    └── unlockGPT/
        ├── Redmiturbo4pro/
        │   └── unlockgpt_both4.bin
        ├── Xiaomicivi5pro/
        │   └── unlockgpt_both4.bin
        └── Xiaomipad8/
            └── unlockgpt_both4.bin
```

---

## 📁 Main File Descriptions

| File / Directory | Description |
|---|---|
| `toUnlock.bat` | One-click entry script |
| `8sg4-unlock.bat` | Main unlock process script |
| `check-unlock.bat` | Script to check BL lock / engineering ABL status |
| `adb-tool.bat` | ADB / Fastboot debugging tool |
| `8735-Ennea.img` | Image used in the unlock flow |
| `adb.exe` | ADB tool |
| `fastboot.exe` | Fastboot tool |
| `AdbWinApi.dll` | Windows ADB runtime library |
| `AdbWinUsbApi.dll` | Windows ADB USB runtime library |
| `unlockFolder/factoryImages/` | ABL / GPT resources per model |
| `unlockFolder/unlockGPT/` | GPT unlock resources |

---

## 🚀 How to Use

### 1. Download the package

Download the latest version from the Releases page:

```text
Mi8sg4_Unlocker.zip
```

### 2. Extract the files

Fully extract to a local directory.

It is recommended to use an English path, for example:

```text
C:\Mi8sG4-Unlocker\
```

Do not run scripts directly from inside the ZIP archive.

### 3. Enable USB debugging

On the phone:

```text
Settings → About phone → tap the build number repeatedly to enable Developer options
Settings → More settings → Developer options → USB debugging
```

After connecting to the PC, allow the USB debugging authorization prompt on the phone.

### 4. Start the unlock process

Double-click to run:

```text
toUnlock.bat
```

Choose the corresponding model when prompted by the script and continue.

### 5. Check unlock status

After the unlock process completes, you can run:

```text
check-unlock.bat
```

This script checks:

- Bootloader (BL) lock status
- Engineering ABL status
- Current device connection status
- Possible exceptions or errors

### 6. Debugging / Manual commands

If you need to run ADB / Fastboot commands manually, run:

```text
adb-tool.bat
```

---

## ⚠️ Important Notes

- Unlocking the bootloader will erase all user data — be sure to back up beforehand.
- Use the original or a reliable quality data cable.
- It is recommended to connect to a USB 2.0 port on the computer.
- Fully extract the package before running scripts.
- Do not delete, move, or rename files inside the package.
- Not recommended to run in virtual machines, remote desktop, or unstable USB environments.
- If the device is not recognized, check USB debugging authorization, drivers, and the data cable.
- There is no guarantee the tool will work for all system versions, region variants, or device states.

---

## ❓ Frequently Asked Questions

### Q: What if the device is not recognized after running the script?

Check:

- Whether USB debugging is enabled
- Whether the phone showed a USB debugging authorization prompt
- Whether you tapped Allow for debugging
- Whether the data cable supports data transfer
- Whether Windows drivers are installed correctly
- Whether another phone management tool is occupying ADB
- Whether the package was fully extracted

### Q: Can HyperOS 1.0 be used?

No.  
This tool requires HyperOS 2.0 or later.

### Q: Will unlocking wipe data?

Yes.  
BL unlock will erase user data — please back up first.

### Q: Why is an English path recommended?

Some batch scripts and ADB / Fastboot tools may behave unexpectedly when run from Chinese or special-character paths.

Recommended path:

```text
C:\Mi8sG4-Unlocker\
```

---

## 💬 Feedback & Discussion

If you encounter any of the following issues on supported models:

- Device not recognized
- Script errors
- Status check abnormal
- Model matching errors
- ADB / Fastboot communication issues
- Process interrupted or failed

Please open an **Issue** and include as much of the following as possible:

- Device model
- System version
- Screenshot of the script
- Error messages
- Which step failed
- Current device mode: System / Fastboot

You can also discuss in the channel:

> **https://t.me/Kernix_dev**

---

## 👥 Contributors

Thanks to [@Littlenine](https://github.com/LittlenineEnnea) for core technical support.

<table>
  <tr>
    <td align="center">
      <a href="https://github.com/LittlenineEnnea">
        <img src="https://github.com/LittlenineEnnea.png" width="100px;" alt="LittlenineEnnea"/><br />
        <sub><b>Littlenine</b></sub>
      </a><br />
      <sub>💡 Core technology / 💻 Unlocking boot.img</sub>
    </td>
  </tr>
</table>

---

## ⚖️ Disclaimer

This project is provided for technical exchange, maintenance of personal devices, and authorized testing only.

Using this tool may result in:

- User data deletion
- Device malfunction
- System failure to boot
- Warranty status changes
- Need for reflashing to recover
- Other unforeseen issues

Users must ensure they own the device or have authorization to use it and accept full responsibility for any risks.

The developer is not liable for device failures, data loss, warranty voiding, or other direct/indirect losses resulting from use of this project.

Do not use this project on unauthorized devices, for illegal activities, or to infringe others' rights.
