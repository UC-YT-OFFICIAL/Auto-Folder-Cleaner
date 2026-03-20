# Auto-Folder-Cleaner
Magisk module for automatic Directory Cleaning

# AFC Cleaner

A Magisk module that automatically deletes specified folders at custom intervals.

## Features
- ✅ Delete multiple folders automatically
- ✅ Custom time intervals (seconds, minutes, hours, days)
- ✅ Control from internal storage
- ✅ Logging support
- ✅ Lightweight & battery friendly

## Requirements
- Magisk 20.4+
- Android 8.0+
- compatible - Apatch - Sukisu - Ksu - magisk
- Ksu required - meta module - magic mount (recommend)
- 
## Installation
1. Download the ZIP file
2. Open Magisk Manager
3. Go to Modules → Install from storage
4. Select the ZIP file
5. Reboot

📱 AFC Ultra Cleaner - Easy Guide

---

🎯 What Does This Module Do?

This module automatically deletes the folders you choose - as often as you set.

---

📂 Where to Find After Installation?

A folder will be created in your phone's Internal Storage:

```
Internal Storage / AFC Ultra Cleaner /
```

This folder contains 2 files:

· config.conf - Settings file (THIS IS WHAT YOU EDIT)
· control.sh - Control file (ignore this, no need)

---

⚙️ How to Edit Config File?

Step 1: Open File Manager

Any file manager (MiXplorer, Solid Explorer, Files by Google)

Step 2: Go to Internal Storage

```
Internal Storage → AFC Ultra Cleaner → config.conf
```

Step 3: Open the File

Open with text editor

---

📝 What's Inside Config File?

```
DELETE_INTERVAL="1d"
DIRS_TO_DELETE="
/storage/emulated/0/Music/thumbnails/
/storage/emulated/0/Music/.thumbnails/
"
ENABLE_LOGGING="true"
LOG_FILE="/storage/emulated/0/AFC Ultra Cleaner/logs/cleaner.log"
```

---

⏰ How to Change Time?

Edit the DELETE_INTERVAL line:

You Want Write Example
Every 1 minute "1m" DELETE_INTERVAL="1m"
Every 5 minutes "5m" DELETE_INTERVAL="5m"
Every 1 hour "1h" DELETE_INTERVAL="1h"
Every 2 hours "2h" DELETE_INTERVAL="2h"
Every 12 hours "12h" DELETE_INTERVAL="12h"
Every 1 day "1d" DELETE_INTERVAL="1d"
Every 2 days "2d" DELETE_INTERVAL="2d"
Every 7 days "7d" DELETE_INTERVAL="7d"
Every 30 days "30d" DELETE_INTERVAL="30d"

---

📁 How to Add New Folders?

Step 1: Find the Folder Path

Open file manager, go to the folder you want to delete, copy its path

Common Paths:

· Internal Storage: /storage/emulated/0/
· WhatsApp Status: /storage/emulated/0/Android/media/com.whatsapp/WhatsApp/Media/.Statuses
· WhatsApp Cache: /storage/emulated/0/Android/data/com.whatsapp/cache
· Instagram Cache: /storage/emulated/0/Android/data/com.instagram.android/cache
· Download Folder: /storage/emulated/0/Download/temp/

Step 2: Edit Config File

Add new folder in the DIRS_TO_DELETE section

Before:

```
DIRS_TO_DELETE="
/storage/emulated/0/Music/thumbnails/
/storage/emulated/0/Music/.thumbnails/
"
```

After adding a new folder:

```
DIRS_TO_DELETE="
/storage/emulated/0/Music/thumbnails/
/storage/emulated/0/Music/.thumbnails/
/storage/emulated/0/Download/temp/
"
```

Step 3: Save File

Save and close the file

---

📝 Example Config File with Comments

```bash
# ====================================
# AFC ULTRA CLEANER - SETTINGS
# ====================================

# TIME INTERVAL
# m = minutes, h = hours, d = days
# Examples: 30m, 2h, 1d, 7d
DELETE_INTERVAL="2d"

# FOLDERS TO DELETE
# Add one folder per line
DIRS_TO_DELETE="
# Music thumbnails
/storage/emulated/0/Music/thumbnails/
/storage/emulated/0/Music/.thumbnails/

# WhatsApp cache
/storage/emulated/0/Android/data/com.whatsapp/cache

# WhatsApp Statuses
/storage/emulated/0/Android/media/com.whatsapp/WhatsApp/Media/.Statuses

# Instagram cache
/storage/emulated/0/Android/data/com.instagram.android/cache

# Download temp
/storage/emulated/0/Download/temp/

# Camera thumbnails
/storage/emulated/0/DCIM/.thumbnails/
"

# LOGGING (true = on, false = off)
ENABLE_LOGGING="true"
LOG_FILE="/storage/emulated/0/AFC Ultra Cleaner/logs/cleaner.log"
```

---

🎮 Simple Commands (Optional)

If you want to use terminal (not required):

```bash
su
sh "/storage/emulated/0/AFC Ultra Cleaner/control.sh" status   # Check status
sh "/storage/emulated/0/AFC Ultra Cleaner/control.sh" logs     # View logs
sh "/storage/emulated/0/AFC Ultra Cleaner/control.sh" run      # Manual cleanup
```

---

✅ How to Check If Working?

Method 1: Check Logs

Open file manager → Internal Storage/AFC Ultra Cleaner/logs/cleaner.log

Method 2: Create Test Folder

1. Create a folder in the list (like thumbnails)
2. Wait for the time you set
3. Check if folder is gone

---

🛠️ Troubleshooting

Folders Not Deleting?

1. Reboot your phone
2. Check logs if service is running
3. Make sure folder path is correct

Wrong Time Setting?

1. Open config.conf
2. Edit DELETE_INTERVAL line
3. Save file
4. Reboot phone

Want to Add Many Folders?

Just add them one per line in DIRS_TO_DELETE section

---

📋 Quick Reference

What You Want What to Edit
Change time DELETE_INTERVAL="2d"
Add folder Add new line in DIRS_TO_DELETE
Remove folder Delete that line from DIRS_TO_DELETE
Stop logging Change ENABLE_LOGGING="false"

---

📱 Common Folder Paths

```
📁 WhatsApp Statuses
/storage/emulated/0/Android/media/com.whatsapp/WhatsApp/Media/.Statuses

📁 WhatsApp Cache
/storage/emulated/0/Android/data/com.whatsapp/cache

📁 Instagram Cache
/storage/emulated/0/Android/data/com.instagram.android/cache

📁 Facebook Cache
/storage/emulated/0/Android/data/com.facebook.katana/cache

📁 Music Thumbnails
/storage/emulated/0/Music/thumbnails/
/storage/emulated/0/Music/.thumbnails/

📁 Camera Thumbnails
/storage/emulated/0/DCIM/.thumbnails/

📁 Download Temp
/storage/emulated/0/Download/temp/

📁 System Temp
/data/local/tmp
```

---

🙏 Credits

## 📢 Contact & Updates

**Stay connected for latest updates, support, and new features:**

### 📺 YouTube Channel
Subscribe for tutorials, updates, and more modules:
- **Channel:** [UC YT OFFICIAL](https://m.youtube.com/channel/UCiRljUMJMGQNarVHH2PjCYw)
- **Content:** Magisk modules, Android tips, rooting guides

### 📱 Telegram Group
Join for:
- Latest module updates
- Direct support
- Bug reports
- Feature requests
- Community help

**Telegram:** [Join UC Community](https://t.me/+SStU2a74TioyMWY1)

### 📧 Email
For business or direct contact:
- **Email:** [ucytofficial@gmail.com]

---

## 🙏 Credits

| Role | Name |
|------|------|
| **Developer** | UC YT OFFICIAL |
| **Testing** | AFC Community Members |
| **Thanks To** | Magisk Team, Android Community |

---

**Made with ❤️ by UC YT OFFICIAL**

*If you find this module helpful, please:*
- ⭐ Star this repository
- 📺 Subscribe to YouTube channel
- 🔔 Join Telegram group
- 📱 Share with friends
