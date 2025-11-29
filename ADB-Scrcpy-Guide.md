ADB & SCRCPY (Windows Only) — Complete Offline Guide

Clean • Beginner-Friendly • Self-Contained

📦 1. What’s Included

This repository contains everything needed to run ADB and Scrcpy on Windows without installing Android Studio or downloading anything externally.

Included inside downloads:

platform-tools-win.zip → ADB + Fastboot (Windows)

scrcpy-win64-v3.1.zip → Scrcpy (Windows 64-bit)

🛠️ 2. Installation (Windows)
Step 1 — Extract Platform Tools

Open: downloads/platform-tools-win.zip

Extract to a simple location such as:
C:\Android\platform-tools\

Confirm you see: adb.exe and fastboot.exe

Step 2 — Extract Scrcpy

Open: downloads/scrcpy-win64-v3.1.zip

Extract to:
C:\Android\scrcpy\

Confirm you see: scrcpy.exe

Installation is complete.

🔧 3. Prepare Your Android Device
Enable Developer Options

Settings → About phone/tablet

Tap Build number 7 times

Enter your PIN

Enable USB Debugging

Settings → System → Developer options

Enable USB debugging

Connect Your Device

Use a good USB cable and accept the popup:

Allow USB debugging?

✔ Always allow from this computer

✔ OK

🧪 4. Test ADB Connection

Run in Command Prompt:

cd C:\Android\platform-tools
adb devices


Expected output:

XXXXXXXXXXXX    device


If it shows unauthorized:

Check device for a popup

Toggle USB debugging

If nothing appears:

Try a new cable

Enable File Transfer (MTP)

Restart your device

Restart ADB:

adb kill-server
adb start-server

⚙️ 5. Essential ADB Commands

List devices
adb devices

Reboot device
adb reboot

Open shell
adb shell
Exit with: exit

Install APK
adb install app.apk

Push file → Downloads
adb push file.txt /sdcard/Download/

Pull file ← Downloads
adb pull /sdcard/Download/file.txt .
(The . means “save to current folder”)

📺 6. Scrcpy Basics (USB Mirroring)

Run scrcpy

cd C:\Android\scrcpy
scrcpy.exe


Fullscreen mode
scrcpy -f

Turn device screen off while mirroring
scrcpy --turn-screen-off

Improve quality
scrcpy --bit-rate 16M --max-size 1920

Show errors
scrcpy

🚨 7. Troubleshooting
Device Not Detected

Change USB cable

Restart device

Restart ADB:

adb kill-server
adb start-server

Unauthorized

Toggle USB debugging

Reconnect USB

Clear authorization and retry

Scrcpy Closes Instantly

Run scrcpy from CMD to view errors:
scrcpy

🧾 8. Quick Cheat Sheet
adb devices
adb shell
adb reboot
adb install app.apk
adb push file /sdcard/Download/
adb pull /sdcard/Download/file .
scrcpy
scrcpy -f
scrcpy --turn-screen-off

🔥 9. fireLabs_AI

This toolkit is part of fireLabs_AI — a personal collection of tools and experiments I organize as an IT hobby developer using AI-assisted development.

The tools in this repo are not created by me — they are publicly available utilities bundled here for convenience.

More curated tools and experiments will be added as fireLabs_AI grows.
