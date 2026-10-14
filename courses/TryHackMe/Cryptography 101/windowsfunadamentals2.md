# Windows Fundamentals Part 2 — TryHackMe  
Room: https://tryhackme.com/room/windowsfundamentals2  

---

## 1. Introduction

This module focuses on Windows utilities used for troubleshooting and system configuration.  
To follow along, the room provides a virtual machine accessible via browser or RDP.

---

## 2. System Configuration (MSConfig)

MSConfig is used for advanced troubleshooting, especially startup issues.

Open via:

```
Win + R → msconfig
```

MSConfig Tabs:

- **General** — Normal, Diagnostic, Selective startup  
- **Boot** — Boot options  
- **Services** — Background services  
- **Startup** — Startup items (redirects to Task Manager in Win10/11)  
- **Tools** — Launch diagnostic utilities  

### Q1: What service lists Systems Internals as the manufacturer?  
A: PsShutdown

### Q2: Whom is the Windows license registered to?  
A: Windows User

### Q3: What is the command for Windows Troubleshooting?  
A: `C:\Windows\System32\control.exe /name Microsoft.Troubleshooting`

### Q4: What command opens the Control Panel?  
A: `control.exe`

---

## 3. Change UAC Settings

User Account Control (UAC) prevents unauthorized system changes.  
The UAC Settings tool adjusts notification levels.

### Q1: What is the command to open UAC Settings?  
A: `UserAccountControlSettings.exe`

---

## 4. Computer Management (compmgmt.msc)

Computer Management consolidates administrative tools:

### System Tools
- Task Scheduler  
- Event Viewer  
- Shared Folders  

### Storage
- Disk Management  

### Services and Applications
- Services  
- WMI Control  

### Q5: What is the command to open Computer Management?  
A: `compmgmt.msc`

### Q6: At what time does GoogleUpdateTaskMachineUA run daily?  
A: 6:15 AM

### Q7: What is the name of the hidden shared folder?  
A: sh4r3dF0Ld3r

---

## 5. System Information (msinfo32)

System Information provides detailed hardware and software data.

Sections:

- System Summary  
- Hardware Resources  
- Components  
- Software Environment  

Environment Variables store OS paths such as `%windir%` and `%SystemRoot%`.

### Q8: What is the command to open System Information?  
A: `msinfo32.exe`

### Q9: What is listed under System Name?  
A: THM-WINFUN2

### Q10: What is the value for ComSpec?  
A: `%SystemRoot%\system32\cmd.exe`

---

## 6. Resource Monitor (resmon)

Resource Monitor provides real‑time monitoring of:

- CPU usage  
- Memory allocation  
- Disk activity  
- Network connections  

### Q11: What is the command to open Resource Monitor?  
A: `resmon.exe`

---

## 7. Command Prompt (cmd.exe)

Command Prompt is essential for Windows administration and cybersecurity.

Useful commands:

```
hostname
whoami
ipconfig
netstat
net help
```

### Q12: What is the full command for Internet Protocol Configuration in MSConfig Tools?  
A: `C:\Windows\System32\cmd.exe /k %windir%\system32\ipconfig.exe`

### Q13: How do you show detailed IP configuration?  
A: `ipconfig /all`

---

## 8. Registry Editor

The Windows Registry stores system and application configuration.

Root keys include:

- HKEY_CURRENT_USER  
- HKEY_LOCAL_MACHINE  

Editing the registry incorrectly can cause system instability.

### Q14: What is the command to open the Registry Editor?  
A: `regedt32.exe`

---

## Summary

Windows Fundamentals Part 2 introduces key administrative tools:

- MSConfig  
- Computer Management  
- System Information  
- Resource Monitor  
- Command Prompt  
- Registry Editor  
