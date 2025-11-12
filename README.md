# 🧩 SamyGO Firmware Patcher (Python 3 Edition)

**Version:** 0.34       
**Original Author:** Erdem U. Altunyurt  
**Python 3 Port & Maintenance:** FrankSx  
**License:** GNU GPL v3  

---

## 📖 Overview

**SamyGO Firmware Patcher** is a cross-platform Python 3 tool that can **decrypt, patch, and repack Samsung Smart TV firmware images**.  
It was originally built for the SamyGO project and later updated by the community to support modern systems and Python 3 environments.

The patcher can enable advanced developer access (Telnet), apply display and subtitle fixes, and modify internal firmware behaviors on supported Samsung TVs.

---

## 🚀 Key Features

- 🔓 AES / XOR firmware decryption for `.img` and `.sec` images  
- 🧩 Automatic firmware detection via MD5 and model signatures  
- ⚙️ Patch options:
  - Enable Telnet / Advanced Mode  
  - Apply Video Aspect Ratio (AR) Fix  
  - Enable Big & Colorful Subtitles  
  - Wiselink Player Hack  
- 💾 Support for FAT16 and SquashFS v3.0 firmware images  
- 🧮 Built-in MD5 and CRC validation  
- 🖥️ Works on Windows, Linux, and macOS  

---

## 🧰 Requirements

- **Python 3.7 or newer**
- Python packages:
  ```bash
  pip install pycryptodome urllib3
  ```
- Standard library modules: `os`, `sys`, `binascii`, `hashlib`, `struct`, `stat`, `time`, `subprocess`, `tarfile`

---

## ⚙️ Installation

```bash
git clone https://github.com/FrankSx/samygo_firmware_patcher.git
cd samygo_firmware_patcher
chmod +x samygo_patcher.py   # optional on Linux/macOS
```

---

## ▶️ Usage

### Basic Command

```bash
python3 samygo_patcher.py <firmware_file.img>
```

### Example

```bash
python3 samygo_patcher.py T-CHL7DEUC_2004.1.exe.img
```

The patcher will:

1. Identify the firmware version  
2. Offer interactive options for Telnet / AR / Subtitle patches  
3. Decrypt, patch, and repack the firmware automatically  

---

## 🧩 Typical Tasks

| Task | Description |
|------|--------------|
| **Decrypt Firmware** | Automatically handles AES/XOR encryption. |
| **Patch exeDSP** | Adds AR Fix, Big Subtitles, and Wiselink hacks. |
| **Repack Image** | Rebuilds FAT16 or SquashFS after patching. |
| **Enable Telnet** | Injects `/etc/telnetd_start.sh` or `/mtd_rwarea/SamyGO.sh` for startup access. |

---

## 📁 Output Structure

```
samygo_patcher.py
├── info.txt               # firmware metadata
├── exeDSP-*               # extracted binary
└── squashfs-tools/        # auto-downloaded toolset
```

---

## ⚠️ Warnings & Disclaimer

- Use at your own risk — modifying firmware can void your warranty or brick your device.  
- Always **back up original firmware files** before patching.  
- Requires ≈ 1 GB of free disk space for temporary files.  
- Supports Samsung B-, C-, D-, and early E-series firmware only.  

---

## 🧠 Compatibility

| OS | Supported | Notes |
|----|------------|-------|
| **Windows** | ✅ | Includes Win32 SquashFS tools |
| **Linux** | ✅ | Auto-detects x86 / x64 builds |
| **macOS** | ✅ | Requires executable permission for tools |

---

## 🪪 License

This software is licensed under the **GNU General Public License v3.0**.  
You are free to use, modify, and redistribute under the same license.  
See [GNU GPL v3](https://www.gnu.org/licenses/gpl-3.0.txt) for details.

---

## 🙌 Credits

- **Original Author:** [Erdem U. Altunyurt](http://www.samygo.tv)  
- **Python 3 Port & Maintenance:** **FrankSx** (2025)  
- **Community Contributors:** SamyGO developers and testers  

---

### 💬 Project Links

- 🏠 Project Home: [SamyGO Community](http://www.samygo.tv)  
- 🐙 GitHub Mirror: [github.com/FrankSx/samygo_firmware_patcher](https://github.com/FrankSx/samygo_firmware_patcher)
