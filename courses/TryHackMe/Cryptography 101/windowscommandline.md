# Windows Command Line — TryHackMe  
Room: https://tryhackme.com/room/windowscommandline  

---

## Task 1 — Introduction

Windows includes a built‑in command‑line interpreter used for administration, troubleshooting, and automation.

### Q1: What is the default command line interpreter in Windows?  
**A: cmd.exe**

---

## Task 2 — Basic System Information

Useful commands:

- `ver` — OS version  
- `systeminfo` — detailed system information  

### Q1: What is the OS version of the Windows VM?  
**A: 10.0.20348.2655**

### Q2: What is the hostname of the Windows VM?  
**A: WINSRV2022-CORE**

---

## Task 3 — Network Troubleshooting

Key commands:

- `ipconfig` — network configuration  
- `ipconfig /all` — full network details including MAC address  
- `netstat -a` — listening ports  
- `netstat -b` — associated processes  

### Q1: Which command shows the MAC address?  
**A: ipconfig /all**

### Q2: What process is listening on port 3389?  
**A: TermService**

### Q3: What is the subnet mask?  
**A: 255.255.0.0**

---

## Task 4 — File and Disk Management

Useful commands:

- `cd` — change directory  
- `dir` — list files  
- `type` — display file contents  

### Q1: What are the file contents in `C:\Treasure\Hunt`?  
**A: THM{CLI_POWER}**

---

## Task 5 — Task and Process Management

Useful commands:

- `tasklist` — list running processes  
- `tasklist /FI "imagename eq X"` — filter by process name  
- `taskkill /PID X` — terminate a process by PID  

### Q1: Command to find running processes related to notepad.exe?  
**A: tasklist /FI "imagename eq notepad.exe"**

### Q2: Command to kill the process with PID 1516?  
**A: taskkill /PID 1516**

---

## Task 6 — Conclusion (Shutdown Commands)

Useful commands:

- `shutdown /s` — shut down  
- `shutdown /r` — restart  
- `shutdown /a` — abort shutdown  

### Q1: Command to restart a system?  
**A: shutdown /r**

### Q2: Command to abort a scheduled shutdown?  
**A: shutdown /a**

---

## Summary
This room introduces essential Windows command‑line skills:

- System information (`ver`, `systeminfo`)  
- Network diagnostics (`ipconfig`, `netstat`)  
- File management (`cd`, `dir`, `type`)  
- Process control (`tasklist`, `taskkill`)  
- Shutdown operations (`shutdown /r`, `/a`)  

Mastering these commands is fundamental for Windows administration, troubleshooting, and cybersecurity operations.
