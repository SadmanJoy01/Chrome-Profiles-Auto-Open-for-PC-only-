# 🚀 Chrome Profiles Auto-Open at Startup

This guide shows you how to automatically open multiple Google Chrome profiles **5 seconds (or user input time) after your PC starts**, using a simple batch script.

---

## 📌 Step 1 — Find Your Chrome Profile Paths

Open **Google Chrome**  >  Go to: **chrome://version**  >  Look for the line **Profile Path**  
   It will look like - 
   C:\Users\John\AppData\Local\Google\Chrome\User Data\Profile 2


This tells you the exact folder name of each Chrome profile (e.g., `Default`, `Profile 1`, `Profile 2`).

---

## 📌 Step 2 — Create a Batch File

Open **Notepad**  >  Paste the script below:

```
@echo off
timeout /t 5 /nobreak >nul

start "" "C:\Program Files\Google\Chrome\Application\chrome.exe" --profile-directory="Default"
start "" "C:\Program Files\Google\Chrome\Application\chrome.exe" --profile-directory="Profile 1"
start "" "C:\Program Files\Google\Chrome\Application\chrome.exe" --profile-directory="Profile 2"
```

## Important:

Replace - C:\Program Files\Google\Chrome\Application\chrome.exe  with the Chrome path from your system.
To find your exact path:
Go to **chrome://version**  >  Look at the **Command Line**. 

Change the time **t** if needed

---

## 📌 Step 3 — Save the Script

Save the file as : open_profiles.bat 

**Make sure the file extension is .bat, not .txt.**

---

## 📌 Step 4 — Add to Startup Folder

Press **Win + R**  >  type **shell:startup**  >  Place your open_profiles.bat file inside this folder.


