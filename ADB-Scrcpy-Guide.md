# ADB & SCRCPY (WINDOWS ONLY) — COMPLETE GUIDE
### Clean • Beginner-Friendly • Self-Contained

---------------------------------------------------------------------

# 📦 1. WHAT’S INCLUDED

This repository contains everything needed to run ADB and Scrcpy on Windows  
without installing Android Studio or downloading anything externally.

Included inside `downloads`:

• `platform-tools-win.zip` → ADB + Fastboot (Windows)  
• `scrcpy-win64-v3.1.zip` → Scrcpy (Windows 64-bit)

---------------------------------------------------------------------

# 🛠️ 2. INSTALLATION (WINDOWS)

## STEP 1 — Extract Platform Tools
Open: `downloads/platform-tools-win.zip`  
Extract to a simple location, such as:  
C:\Android\platform-tools\  
Confirm you see: `adb.exe` and `fastboot.exe`

## STEP 2 — Extract Scrcpy
Open: `downloads/scrcpy-win64-v3.1.zip`  
Extract to:  
C:\Android\scrcpy\  
Confirm you see: `scrcpy.exe`

Installation is complete.

---------------------------------------------------------------------

# 🔧 3. PREPARE YOUR ANDROID DEVICE

## Enable Developer Options
Settings → About phone/tablet  
Tap “Build number” seven times    

## Enable USB Debugging
Settings → System → Developer options → USB debugging    

## Connect Your Device
Use a good USB cable and approve the popup:  
“Allow USB debugging?”  
✔ Always allow from this   computer  
✔ OK  

---------------------------------------------------------------------

# 🧪 4. TEST ADB CONNECTION

Run the following in Command Prompt:  
cd C:\Android\platform-tools  
adb devices  

Expected result:  
XXXXXXXXXXXX    device  

If it shows “unauthorized”:  
• Check your device for a popup  
• Toggle USB debugging  

If nothing appears:  
• Try a new cable  
• Enable File Transfer (MTP)  
• Restart your device  
• Restart ADB:  
  adb kill-server  
  adb start-server  

---------------------------------------------------------------------

# ⚙️ 5. ESSENTIAL ADB COMMANDS

List devices:  
adb devices  

Reboot device:  
adb reboot  

Open shell:  
adb shell  
(exit with: exit)  

Install APK:  
adb install app.apk  

Push file → Downloads:  
adb push file.txt /sdcard/Download/  

Pull file ← Downloads:  
adb pull /sdcard/Download/file.txt .  
(The “.” means “save to current folder”.)

---------------------------------------------------------------------

# 📺 6. SCRCPY BASICS (USB MIRRORING)

Run scrcpy:  
cd C:\Android\scrcpy  
scrcpy.exe  

---------------------------------------------------------------------

# 🚨 7. TROUBLESHOOTING

## Device not detected
• Change USB cable  
• Restart device  
• Restart ADB:  
  adb kill-server  
  adb start-server  

## Unauthorized
• Toggle USB debugging  
• Reconnect USB  
• Clear authorization and try again  

## Scrcpy closes instantly
• Run “scrcpy” from CMD to view error output  

---------------------------------------------------------------------

# 🧾 8. QUICK CHEAT SHEET

adb devices  
adb shell  
adb reboot  
adb install app.apk  
adb push file /sdcard/Download/  
adb pull /sdcard/Download/file .  
scrcpy  
scrcpy -f  
scrcpy --turn-screen-off  

---------------------------------------------------------------------

# 🔥fireLabs_AI

This toolkit is part of **fireLabs_AI** — a personal collection of tools  
and experiments I organize as an IT hobby developer using AI-assisted  
development.

The tools in this repo are **not created by me** — they are publicly  
available utilities bundled here for convenience and ease of use.

More curated tools and experiments will be added as fireLabs_AI grows.

---------------------------------------------------------------------
