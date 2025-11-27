![Platform: Windows](https://img.shields.io/badge/Platform-Windows-blue)
![ADB Included](https://img.shields.io/badge/ADB-Platform--Tools-green)
![Scrcpy Included](https://img.shields.io/badge/Scrcpy-v3.1-orange)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow)

# Android ADB + Scrcpy Toolkit (Windows Only)

A clean, offline-ready toolkit for using **ADB** and **Scrcpy** on Windows.  
Everything you need is stored **inside this repo** — no external downloads required.

This toolkit is designed for:
- Samsung tablets  
- Pixel tablets  
- Lenovo tablets  
- Any Android device with USB debugging enabled  

Perfect for IT helpdesk, wall panels, kiosk devices, development, automation, and general Android management.

---

# 📦 Included Tools (Offline)

All required tools are located in the `/downloads` folder:

/downloads/platform-tools-win.zip ← ADB & Fastboot (Windows)
/downloads/scrcpy-win64-v3.1.zip ← Scrcpy (Windows 64-bit)


You do **not** need any other downloads.  
These are the exact files used for all instructions in this toolkit.

---

# 📘 Main Guide

Start here:

👉 **[ADB-Scrcpy-Guide.md](ADB-Scrcpy-Guide.md)**

The guide covers:

- Extracting the offline tools  
- Enabling Developer Options  
- Enabling USB debugging  
- Connecting the device  
- Running ADB commands  
- Installing APKs  
- Pushing/Pulling files safely  
- Running scrcpy over USB  
- Basic troubleshooting  
- A clean ADB + Scrcpy cheat sheet  

Everything is written to be beginner-friendly and Windows-only so there's no confusion.

---

# 🗂 Repository Structure

Android-adb-scrcpy-toolkit/
├── ADB-Scrcpy-Guide.md ← Main setup guide
├── downloads/ ← Offline tools included here
│ ├── platform-tools-win.zip
│ └── scrcpy-win64-v3.1.zip
├── scrcpy/ ← (reserved for advanced scrcpy docs)
├── tools/ ← (reserved for batch files/scripts)
└── README.md ← You are here


This structure keeps everything tidy, expandable, and future-proof.

---

# 🤖 AI-Powered ADB & Scrcpy Help

This toolkit intentionally keeps documentation **lean and essential**.

For anything advanced, you can use **AI to generate commands on the fly**.

## How to use AI with this toolkit:

1. Download this entire GitHub repository as a ZIP  
2. Upload it into ChatGPT (or your preferred AI assistant)  
3. Ask:

Give me the exact ADB command for ______ using this toolkit.


### Example prompts:

Give me ADB commands to remove system apps.
Give me the command to disable all vibration.
Give me ADB commands to extract an APK.
Give me debugging commands for scrcpy freezing.
Give me ADB commands to list all installed packages.
Give me ADB commands to read logs or battery stats.


The AI will automatically:
- detect that you're on **Windows**
- use the correct folder structure (`downloads/platform-tools-win/`)
- generate accurate commands
- warn you before dangerous operations
- provide full explanations

This makes the toolkit **infinite**, without storing hundreds of command reference files.

---

Made for fast Android setup, scrcpy management, kiosk devices, and streamlined IT work.
