
#ANDROID ADB + SCRCPY — COMPLETE GUIDE#
#Offline • Beginner-Friendly#



📦 1. WHAT'S INCLUDED

This repository contains everything required to run ADB and Scrcpy on
Windows — **completely offline**, no external downloads needed.

Included in /downloads:

    platform-tools-win.zip     → ADB + Fastboot (Windows)
    scrcpy-win64-v3.1.zip      → Scrcpy (Windows 64-bit)

This guide explains exactly how to extract, set up, and use both.


🛠️ 2. INSTALLATION (WINDOWS)

----------------------------
STEP 1 — Extract Platform Tools
----------------------------
1. Open:  /downloads/platform-tools-win.zip
2. Extract to a convenient location, e.g.:

       C:\Android\platform-tools\

3. Confirm the folder contains:
       adb.exe
       fastboot.exe

----------------------------
STEP 2 — Extract Scrcpy
----------------------------
1. Open:  /downloads/scrcpy-win64-v3.1.zip
2. Extract to:

       C:\Android\scrcpy\

3. Confirm you see:
       scrcpy.exe

Installation is complete. No setup required.


🔧 3. PREPARE YOUR ANDROID DEVICE

----------------------------
Enable Developer Options
----------------------------
1. Settings → About phone/tablet  
2. Tap "Build number" seven times  
3. Enter your PIN

----------------------------
Enable USB Debugging
----------------------------
Settings → System → Developer Options →  
✔ USB debugging

----------------------------
Connect Device
----------------------------
Use a good USB cable and approve the popup:

    “Allow USB debugging?”
    ✔ Always allow from this computer
    ✔ OK

🧪 4. TEST ADB CONNECTION

In Command Prompt:

cd C:\Android\platform-tools
adb devices

EXPECTED RESULT:
XXXXXXXXXXXX device

If you see “unauthorized”:
- Check the device for a popup  
- Toggle USB debugging off/on  

If you see nothing:
- Try a new cable  
- Try File Transfer (MTP) mode  
- Restart device  
- Restart ADB:  
adb kill-server
adb start-server

markdown
Copy code

⚙️ 5. ESSENTIAL ADB COMMANDS

List devices:
adb devices

makefile
Copy code

Reboot:
adb reboot

Open device shell:
adb shell
exit ← to leave

Install APK:
adb install app.apk

Push file → Downloads:
adb push file.txt /sdcard/Download/

Pull file ← Downloads:
adb pull /sdcard/Download/file.txt .

(The “.” means save to current folder.)

📺 6. USING SCRCPY (USB MIRRORING)

Run scrcpy:
cd C:\Android\scrcpy
scrcpy.exe

Fullscreen:
scrcpy -f

Turn device screen off (while mirroring):
scrcpy --turn-screen-off

Improve quality:
scrcpy --bit-rate 16M --max-size 1920

Show logs (if window closes instantly):
scrcpy

🚨 7. TROUBLESHOOTING

DEVICE NOT DETECTED:
- Try a different USB cable  
- Restart your phone/tablet  
- Run:
adb kill-server
adb start-server

UNAUTHORIZED:
- Toggle USB debugging  
- Reconnect cable  
- Clear authorization:
adb usb

SCRCPY INSTANTLY CLOSES:
- Run from CMD to see errors:
scrcpy

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

This guide and toolkit are part of **fireLabs_AI** — a personal collection
of curated tools, utilities, and experiments I organize to streamline
Android tinkering and AI-assisted development.

These tools are NOT created by me — they are publicly available.  
fireLabs_AI simply organizes them in a clean, offline, ready-to-use format
for convenience and learning.

More curated tools and experiments will be added as fireLabs_AI grows.

######################################################################
