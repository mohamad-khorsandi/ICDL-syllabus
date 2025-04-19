### 🧪 1. **System Cleanup Script**

**Goal**: Free up space by cleaning temporary files.

```
batCopy code@echo off
echo Cleaning temporary files...
del /s /q "%temp%\*.*"
del /s /q "C:\Windows\Temp\*.*"
echo Done!
pause
```

✅ Add: Launch Disk Cleanup with `cleanmgr`

------

### 💻 2. **Create a Daily Backup Script**

**Goal**: Copy important files from one folder to a backup folder (e.g. from `Documents` to `D:\Backup`)

```
batCopy code@echo off
xcopy "%USERPROFILE%\Documents" "D:\Backup\Documents" /s /i /y
echo Backup complete!
pause
```

✅ Tip: Use `Task Scheduler` to run this daily.

------

### 📦 3. **Auto-Installer Script**

**Goal**: Install several `.exe` apps silently (when supported)

```
batCopy code@echo off
start /wait NotepadPlusPlusInstaller.exe /S
start /wait ChromeSetup.exe /silent /install
echo All apps installed!
pause
```

✅ Works well in lab setups or bootstrapping your own PC.

------

### 🧭 4. **Open Favorite Websites with One Click**

**Goal**: Launch multiple websites in your default browser.

```
batCopy code@echo off
start https://www.google.com
start https://www.github.com
start https://mail.google.com
```

✅ Combine with `Shell:startup` to launch at login.

------

### 📂 5. **Create a Folder Structure for a Project**

**Goal**: Quickly create a set of folders for a new work or school project.

```
batCopy code@echo off
set /p projectName=Enter Project Name:
mkdir %projectName%
cd %projectName%
mkdir Docs Images Code Backup
echo Folder structure created for %projectName%
pause
```

------

### 🔐 6. **Lock Folder with a Password**

This one's a cool trick (not very secure but fun for learning):

```
batCopy code@echo off
title Folder Locker
if EXIST "Private" (
  echo Folder already locked or exists!
  pause
  exit
)
md Private
echo Private folder created.
pause
```

Then create another file to rename/hide the folder and another to unlock. Let me know if you want the full version of the "locker" setup.

------

### 🧠 7. **System Info Exporter**

**Goal**: Save a detailed report of the system to a text file.

```
batCopy code@echo off
systeminfo > "%USERPROFILE%\Desktop\SystemInfo.txt"
echo System info saved to Desktop!
pause
```

------

### ⚙️ 8. **Toggle Wi-Fi Adapter**

**Goal**: Enable or disable Wi-Fi with a batch file (requires elevated permissions).

```
batCopy code@echo off
netsh interface set interface "Wi-Fi" admin=disabled
pause
```

Change to `enabled` to re-enable.