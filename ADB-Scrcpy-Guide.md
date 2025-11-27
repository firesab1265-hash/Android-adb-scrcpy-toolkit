# ADB & Scrcpy (Windows Only) — Beginner Guide

This guide explains how to set up ADB and scrcpy on Windows using the tools included in this repository. No external downloads are required.

Everything you need is already inside:

https://github.com/firesab1265-hash/Android-adb-scrcpy-toolkit/raw/main/downloads/platform-tools-win.zip

https://github.com/firesab1265-hash/Android-adb-scrcpy-toolkit/raw/main/downloads/scrcpy-win64-v3.1.zip



Copy code

---

# 📦 1. What’s Included

### **Platform Tools**
Contains:
- `adb.exe`
- `fastboot.exe`
- backend binaries

### **Scrcpy**
Allows you to:
- mirror the screen
- control the device with mouse/keyboard
- turn the tablet screen off while keeping scrcpy active
- adjust quality/performance

---

# 🛠️ 2. Install Instructions (Windows)

## **Step 1 — Extract Platform Tools**

1. Go to the `/downloads` folder in this repo.
2. Download **platform-tools-latest-windows.zip**.
3. Extract it somewhere easy, for example:

C:\Android\platform-tools\

yaml
Copy code

Inside that folder you should see `adb.exe`.

---

## **Step 2 — Extract Scrcpy**

1. Download **scrcpy-win64-v3.1.zip** from `/downloads`.
2. Extract it to:

C:\Android\scrcpy\

yaml
Copy code

Inside that folder you should see `scrcpy.exe`.

**That's it — installation is complete.**

---

# 🔧 3. Prepare Your Android Device

### Enable Developer Options
1. Settings → About phone / About tablet  
2. Tap **Build number** 7 times  
3. Enter your PIN when asked  

### Enable USB Debugging
Settings → System → Developer options →  
✔ **USB debugging**

### Connect Your Device
Use a good USB cable and approve the popup:

**Allow USB debugging?**  
✔ Always allow from this computer  
✔ OK

---

# 🧪 4. Test ADB

Open Command Prompt and navigate to platform-tools:

cd C:\Android\platform-tools
adb devices

lua
Copy code

Expected output:

XXXXXXXXXXXX device

yaml
Copy code

If it says `unauthorized`, check your device for a permission popup.

If nothing shows:
- try another cable  
- enable File Transfer (MTP) mode  
- close and reopen CMD  

---

# ⚙️ 5. Important ADB Commands

### ✔ List connected devices
adb devices

shell
Copy code

### ✔ Reboot device
adb reboot

shell
Copy code

### ✔ Open an interactive shell
adb shell

vbnet
Copy code
Exit with:
exit

shell
Copy code

### ✔ Install an APK
adb install app.apk

shell
Copy code

### ✔ Push a file to the Downloads folder
adb push file.txt /sdcard/Download/

shell
Copy code

### ✔ Pull a file *from* Downloads
adb pull /sdcard/Download/log.txt .

yaml
Copy code

The `.` means "save to the current folder".

---

# 📺 6. Scrcpy Basics (USB Only)

### Run scrcpy
cd C:\Android\scrcpy
scrcpy.exe

nginx
Copy code

Your device should immediately appear on your screen.

### Fullscreen mode
scrcpy.exe -f

shell
Copy code

### Turn device screen off while mirroring
scrcpy.exe --turn-screen-off

shell
Copy code

### Improve quality
scrcpy.exe --bit-rate 16M --max-size 1920

yaml
Copy code

---

# 🚨 7. Troubleshooting

### Device not detected?
- Try a different USB cable  
- Restart your device  
- Restart ADB:

adb kill-server
adb start-server

nginx
Copy code

### Unauthorized?
Toggle USB debugging off/on on the device.

### Scrcpy closes instantly?
Run from CMD to see errors:
scrcpy.exe

yaml
Copy code

---

# 🧾 8. Quick Cheat Sheet

adb devices
adb shell
adb reboot
adb install app.apk
adb push file /sdcard/Download/
adb pull /sdcard/Download/file .
scrcpy
scrcpy -f
scrcpy --turn-screen-off

yaml
Copy code
