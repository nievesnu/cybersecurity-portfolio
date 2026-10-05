# Windows Basics — TryHackMe

I just completed [Windows Basics room](https://tryhackme.com/room/windowsbasics?utm_campaign=social_share&utm_medium=social&utm_content=room&utm_source=linkedin&sharerId=687937a5488df707cc460ae1) on TryHackMe!

Windows Basics v6-badrrd
Pre Security → Operating Systems Basics → Windows Basics
Lab IP: 10.129.149.26

<details> <summary> Answers & Flag</summary>

Device name: TryHatMe
Installed RAM: 4.00 GB
Windows Server 2019 Datacenter Version: 1809
Flag in Welcome.txt: THM{welcome_to_tryhatme!}

</details>

**Finds**: keeping applications and the operating system updated helps maintain security and stability through security patches, performance improvements, and bug fixes.
The Time & Language section showed that the computer's country or region was set to United States.
The Task Manager showed that the currently logged-in account was Administrator.
A custom scan was performed on the TryHatMe Onboarding folder using Windows Security. The scan detected *Virus:DOS/EICAR_Test_File*
After selecting See details, the affected item was shown as: *tryhatmemaldoc.txt*

The TryHatMeWelcome installer was located inside: TryHatMe Onboarding
The application was installed and executed and the flag was given.

<details> <summary>🚩 Flag</summary>
THM{your_first_day!}
</details>


<details> <summary> Answers</summary>

TryHatMeWelcome flag: THM{your_first_day!}
Country/Region: United States
Logged-in account: Administrator
Affected item: tryhatmemaldoc.txt

</details>

This room covered the basics of the Windows operating system, including navigating the Windows interface, managing files and folders, installing applications, checking system information, using Task Manager, and working with Windows Security and Windows Defender Firewall.
