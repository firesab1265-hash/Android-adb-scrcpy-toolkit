ADB & SCRCPY (WINDOWS ONLY) — COMPLETE OFFLINE GUIDE
Clean • Beginner-Friendly • Self-Contained

📦 1. WHAT’S INCLUDED

This repository contains everything needed to run ADB and Scrcpy on Windows
WITHOUT installing Android Studio or downloading anything externally.

Included (inside downloads):

• platform-tools-win.zip → ADB + Fastboot (Windows)
• scrcpy-win64-v3.1.zip → Scrcpy (Windows 64-bit)

🛠️ 2. INSTALLATION (WINDOWS)

STEP 1 — Extract Platform Tools

Open: downloads/platform-tools-win.zip

Extract to a simple location such as:
C:\Android\platform-tools\

Confirm you see: adb.exe and fastboot.exe

STEP 2 — Extract Scrcpy

Open: downloads/scrcpy-win64-v3.1.zip

Extract to:
C:\Android\scrcpy\

Confirm you see: scrcpy.exe

Installation is complete.

🔧 3. PREPARE YOUR ANDROID DEVICE

Enable Developer Options
Settings → About phone/tablet
Tap “Build number” seven times
Enter your PIN

Enable USB Debugging
Settings → System → Developer options → USB debugging
✔ Turn it on

Connect Your Device
Use a good USB cable and approve the popup:

“Allow USB debugging?”
✔ Always allow from this computer
✔ OK

🧪 4. TEST ADB CONNECTION

Open Command Prompt and run:

cd C:\Android\platform-tools
adb devices

Expected result:
XXXXXXXXXXXX device

If it shows “unauthorized”:
• Check your device for a popup
• Toggle USB debugging

If no devices appear:
• Try a different cable
• Enable File Transfer (MTP)
• Restart the device
• Restart ADB:
adb kill-server
adb start-server

⚙️ 5. ESSENTIAL ADB COMMANDS

List devices:
adb devices

Reboot device:
adb reboot

Open shell:
adb shell

Exit shell:
exit

Install APK:
adb install app.apk

Push file → Downloads:
adb push file.txt /sdcard/Download/

Pull file ← Downloads:
adb pull /sdcard/Download/file.txt .

(The . means “save to current folder”.)

📺 6. SCRCPY BASICS (USB MIRRORING)

Run scrcpy:
cd C:\Android\scrcpy
scrcpy.exe

Fullscreen:
scrcpy -f

Turn device screen off while mirroring:
scrcpy --turn-screen-off

Improve quality:
scrcpy --bit-rate 16M --max-size 1920

Show debug logs (if it closes instantly):
scrcpy

🚨 7. TROUBLESHOOTING

Device not detected:
• Change USB cable
• Restart device
• Restart ADB:
adb kill-server
adb start-server

Unauthorized:
• Toggle USB debugging
• Reconnect USB
• Clear authorization

Scrcpy closes instantly:
• Run scrcpy from CMD to view errors

🧾 8. QUICK CHEAT SHEET

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

This toolkit is part of fireLabs_AI — a personal collection of tools
and experiments I organize as an IT hobby developer using AI-assisted
development.

The tools in this repo are not created by me — they are publicly
available utilities bundled here for convenience.

More curated tools and experiments will be added as fireLabs_AI grows.
