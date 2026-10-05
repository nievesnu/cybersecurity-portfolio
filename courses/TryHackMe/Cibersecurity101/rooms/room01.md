# Inside a Computer — TryHackMe
I just completed [Cold Boot room](https://tryhackme.com/room/insideacomputerQwe?utm_campaign=social_share&utm_medium=social&utm_content=room&utm_source=linkedin&sharerId=687937a5488df707cc460ae1
) on TryHackMe! 

**Case: Inside a Computer**

Briefing: A workstation was pulled from a breach scene. The suspect was gone before anyone arrived. All you have is the machine, in pieces, and a case file with notes from the scene.
Some of the recovered components aren't from this machine. To rebuild it, you'll need to know what each part does, how it connects to the motherboard, and read the evidence closely enough to tell what belongs.

Objective: Assemble the machine, boot it, find the evidence file, and email it to the senior analyst to close the case.

Instructions: 
> Hi! Welcome to TryHackMe Forensics Labs.
>
> This machine here came straight from a breach scene. The suspect was long gone by the time we showed up, but not before tearing the PC apart to slow us down. Our team collected everything they found at the scene and laid it out on that table. But here's the thing: some of those parts are impostors. Planted there just to confuse us.

<img width="260" height="155" alt="image" src="https://github.com/user-attachments/assets/a73d9e5a-a092-4720-a2ed-60bcea72917f" />
Image of the result of building the computer.

DIGITAL FORENSICS LAB
<details>
<summary>Parts & Function
What each component does, and where it belongs. — Click to expand</summary>
### Processor

**Central Processing Unit (CPU)**

- **Function:** Processes every program, click, and instruction, and tells the other components what to do.
- **Position:** CPU socket on the motherboard.

### Memory

**Random Access Memory (RAM)**

- **Function:** Temporarily stores the data the computer is currently using so it can be accessed quickly. Its contents are lost when the power is switched off.
- **Position:** DIMM slots on the motherboard.

### Power

**Power Supply Unit (PSU)**

- **Function:** Takes electricity from the wall and converts it into the correct voltage for the computer's internal components.
- **Position:** Mounted at the edge of the chassis.

### Laptop Power Charger

- **Function:** Converts electricity from a wall outlet into the DC power required by a laptop.
- **Position:** Outside the computer, connected to a wall outlet.

### Connectivity

**Network Adapter**

- **Function:** Sends and receives data over a network, allowing the computer to connect to other devices and the internet.
- **Position:** Inside the chassis near the rear.

**Wi-Fi Dongle**

- **Function:** Adds wireless network connectivity to a computer through an external USB connection.
- **Position:** USB port on the outside of the chassis.

### External Connections

**Input / Output Panel (I/O)**

- **Function:** Provides the external ports used to connect devices, including USB, HDMI, audio, and Ethernet.
- **Position:** Rear opening of the chassis.

### Storage

**Solid State Drive (SSD)**

- **Function:** Permanently stores files, applications, and the operating system. It is fast, silent, and has no moving parts.
- **Position:** Mounted directly on the motherboard.

**Hard Disk Drive (HDD)**

- **Function:** Permanently stores files using spinning magnetic disks and moving parts.
- **Position:** Drive bay inside the chassis.

### Visual Output

**Graphics Card (GPU)**

- **Function:** Creates the visuals shown on the screen and processes images, video, and 3D graphics.
- **Position:** PCIe x16 slot on the motherboard.

**Laptop Graphics Card (GPU)**

- **Function:** Creates visuals and processes images, video, and 3D graphics using smaller, lower-powered hardware.
- **Position:** Integrated into or mounted directly on a laptop motherboard.

</details>

<details>
<summary>🚩 Flag</summary>
`THM{c0ld_b00t_c0mpl3t3}`
</details>
