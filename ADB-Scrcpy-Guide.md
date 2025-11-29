ADB & Scrcpy (Windows Only) — Complete Offline Guide

Clean • Beginner-Friendly • Self-Contained

📦 1. What’s Included

This repository contains everything required to run ADB and Scrcpy on Windows without installing Android Studio or downloading anything from the internet.

Included (inside /downloads):

platform-tools-win.zip → ADB + Fastboot (Windows)

scrcpy-win64-v3.1.zip → Scrcpy (Windows 64-bit)

Direct links for reference:

Platform Tools:
https://github.com/firesab1265-hash/Android-adb-scrcpy-toolkit/raw/main/downloads/platform-tools-win.zip

Scrcpy:
https://github.com/firesab1265-hash/Android-adb-scrcpy-toolkit/raw/main/downloads/scrcpy-win64-v3.1.zip

🛠️ 2. Installation (Windows)
Step 1 — Extract Platform Tools

Open /downloads/platform-tools-win.zip.

Extract to a simple location such as:
C:\Android\platform-tools\

Make sure the folder contains:

adb.exe

fastboot.exe

Step 2 — Extract Scrcpy

Open /downloads/scrcpy-win64-v3.1.zip.

Extract to:
C:\Android\scrcpy\

Confirm that scrcpy.exe is inside the folder.

Installation is complete.

🔧 3. Prepare Your Android Device
Enable Developer Options

Settings → About phone/tablet

Tap “Build number” seven times

Enter your PIN

Enable USB Debugging

Settings → System → Developer Options

Turn on USB debugging

Connect Device via USB

Use a good cable and accept the popup:

“Allow USB debugging?”

✔ Always allow from this computer

✔ OK

🧪 4. Test ADB Connection

Run these commands in Command Prompt after extracting the tools:

cd C:\Android\platform-tools
adb devices


Expected output:
XXXXXXXXXXXX device

If it shows unauthorized, approve the popup on your device.

If nothing appears:

Try another cable

Enable File Transfer (MTP)

Close and reopen CMD

Restart ADB using:

adb kill-server

adb start-server

⚙️ 5. Essential ADB Commands

List devices
adb devices

Reboot device
adb reboot

Open shell
adb shell
Exit with exit

Install APK
adb install app.apk

Push file → Downloads
adb push file.txt /sdcard/Download/

Pull file ← Downloads
adb pull /sdcard/Download/file.txt .
(“.” means save in current folder)

📺 6. Scrcpy Basics (USB Mirroring)

Run Scrcpy

cd C:\Android\scrcpy
scrcpy.exe


Fullscreen
scrcpy -f

Turn device screen off while mirroring
scrcpy --turn-screen-off

Improve quality
scrcpy --bit-rate 16M --max-size 1920

Show errors
scrcpy

🚨 7. Troubleshooting

Device not detected

Try different USB cables

Restart device

Restart ADB:

adb kill-server

adb start-server

Unauthorized

Toggle USB debugging off/on

Reconnect cable

Scrcpy closes instantly

Run scrcpy from CMD to see logged errors

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

🔥 fireLabs_AI

This toolkit is part of fireLabs_AI — a personal collection of curated tools, utilities, and experiments I organize as an IT hobby developer using AI-assisted development.

The tools in this repo are not created by me; they are publicly available.
fireLabs_AI simply organizes them into a clean, offline, easy-to-use format for convenience and learning.

More curated tools and experiments will be added as the project grows.
