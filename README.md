# IITH AIMS Grade Notification System

A lightweight Windows app that monitors AIMS for newly released course grades and sends email notifications when grades become available.

The background worker checks AIMS every 15 minutes. When one or more courses are graded, an email is sent to your configured address.

---

## Quick Setup Guide

1. Download [`aims-notifs-win-x64.7z`](https://drive.google.com/uc?export=download&id=1WRwTagaKgkV9pvPVINLKwglmFrGliTqv).

2. Unblock the file by opening **Properties → General** and checking **Unblock**. This is important to ensure that the application can run.

3. Extract the contents into a directory of your choice.

4. For both `IITHAIMSGradeNotificationSystem.exe` and `IITHAIMSGradeNotificationSystem.Worker.exe`, open **Properties → Compatibility** and under **Settings**, check **Run this program as an administrator**, as both executables must always run as administrator.

5. *(Optional)* Create a desktop shortcut for `IITHAIMSGradeNotificationSystem.exe`.

6. Create a [Google App Password](https://support.google.com/mail/answer/185833) for the email address that will receive notifications when grades are released. Use this App Password during setup (**not** your normal Gmail password). Requires 2-Step Verification to be enabled on your Google account.

7. Connect to [IITH VPN](https://docs.google.com/document/u/0/d/e/2PACX-1vQxWGsv6dhwmvx4Efq17CPyCBTvMiKd9oTJecNDy51KXIPDfdjUQq822EpBExduoPtBTQbkvtNMudqh/pub) and stay connected, if applicable.

8. Launch `IITHAIMSGradeNotificationSystem.exe`. Enter your AIMS username, AIMS password, email address, and App Password when prompted, then use the app window to start monitoring. **Your passwords are encrypted and stored locally.**

**Note: the first run will take a few minutes to complete. This is normal. Do not close the application window until the first run is complete.**

---

## Features

* Automatic AIMS grade monitoring
* Email notifications when new grades are released
* Background checks every 15 minutes
* Manual on-demand checks
* Simple graphical setup and controls

---

## Requirements

* Windows 10 or newer
* Internet connection
* AIMS account credentials (encrypted and stored locally)
* Email account with an App Password configured (encrypted and stored locally)

---

## Usage

Everything is controlled from the app window:

* **Save and Continue**: enter your credentials (on first launch) or update them later
* **Check Now**: check for new grades immediately
* **Enable/Disable Background Worker**: start or stop automatic monitoring (checks every 15 minutes)
* **Change Credentials**: update your saved settings
* **Uninstall**: remove all application files and local data

---

## Reporting Issues

If you encounter a bug, have a feature request, or need help, please open an [issue on GitHub](https://github.com/Vardhan-R/IITH-AIMS-Grade-Notification-System-Win/issues).

When reporting a bug, please include your Windows version, VPN status, and relevant logs from the application window.

---

## Directory Layout

```text
<extracted-folder>\
├── IITHAIMSGradeNotificationSystem.exe
├── IITHAIMSGradeNotificationSystem.Worker.exe
└── data\
    ├── app.log
    ├── config.json
    ├── not_graded_courses.json
    └── state.json
```

There will be other files in the extracted folder, but you need not worry about them.

---

## Security Notes

Passwords are encrypted before being written to the configuration file.

Only install and run this software on machines you trust.

---

## Disclaimer

This project is an unofficial utility and is not directly affiliated with IIT Hyderabad or the AIMS platform.

Use at your own risk.
