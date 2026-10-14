# Windows Fundamentals Part 1 — TryHackMe  
Room: https://tryhackme.com/room/windowsfundamentals1  

---

## 1. Introduction to Windows

Windows is the most widely used desktop operating system in corporate and home environments.  
This room introduces:

- The Windows interface  
- File system basics  
- User accounts and permissions  
- System utilities and configuration tools  

---

## 2. Windows Editions

Windows has evolved since 1985, with major versions including XP, Vista, 7, 8, 10, and 11.  
Windows 10/11 typically come in **Home** and **Pro** editions.

Key difference relevant to cybersecurity:

**Q1: What encryption can you enable on Pro that you can’t enable in Home?**  
**A: BitLocker**

BitLocker provides full‑disk encryption to protect data on lost or stolen devices.

---

## 3. Desktop GUI

Windows uses a Graphical User Interface (GUI) composed of:

- Desktop  
- Start Menu  
- Taskbar  
- Notification Area  

### Q1: Which selection hides the Search box?  
A: Hidden

### Q2: Which selection hides the Task View button?  
A: Show Task View button (toggle off)

### Q3: Besides Clock and Network, what other icon appears in the Notification Area?  
A: Action Center

---

## 4. The File System

Modern Windows systems use **NTFS (New Technology File System)**.

NTFS supports:

- Journaling  
- File permissions  
- Compression  
- Encryption  

### Q1: What is the meaning of NTFS?  
A: New Technology File System

---

## 5. The Windows\System32 Folder

The Windows directory contains core OS files.  
Windows uses environment variables to reference system paths.

### Q1: What is the system variable for the Windows folder?  
A: %windir%

System32 contains essential executables and libraries required for Windows operation.

---

## 6. User Accounts, Profiles, and Permissions

Windows supports two main local account types:

- **Administrator** — full system control  
- **Standard User** — limited permissions  

User profiles are stored in `C:\Users`.  
User and group management is done via `lusrmgr.msc`.

### Q1: What is the name of the other user account?  
A: tryhackmebilly

### Q2: What groups is this user a member of?  
A: Remote Desktop Users, Users

### Q3: What built‑in account is for guest access?  
A: Guest

### Q4: What is the account description?  
A: Built‑in account for guest access to the computer/domain

---

## 7. User Account Control (UAC)

UAC prevents unauthorized system changes by requiring elevation for administrative tasks.

### Q1: What does UAC mean?  
A: User Account Control

---

## 8. Settings and Control Panel

Windows provides two configuration interfaces:

- **Settings** — modern UI  
- **Control Panel** — traditional, detailed configuration  

### Q1: In Small icons view, what is the last setting listed?  
A: Windows Defender Firewall

---

## 9. Task Manager

Task Manager monitors system performance and manages processes.  
It displays CPU, RAM, disk, and network usage.

### Q1: What is the keyboard shortcut to open Task Manager?  
A: Ctrl+Shift+Esc

---

## Summary

This room introduces essential Windows concepts:

- Navigating the GUI  
- Understanding Windows editions  
- NTFS file system  
- User accounts and permissions  
- System utilities (Control Panel, Task Manager)  
- Security features like UAC and BitLocker  

These fundamentals are crucial for cybersecurity professionals, as Windows environments are a major focus in defensive security.
