
# CompTIA A+ Master Cheat Sheet
## Core 1 (220-1201) & Core 2 (220-1202) — V15

---

# TABLE OF CONTENTS

1. Exam Overview
2. Computer Hardware
3. Storage & RAID
4. CPUs, RAM & Motherboards
5. Power Supplies & Connectors
6. Displays & Peripherals
7. Printers
8. Networking Fundamentals
9. Networking Ports & Protocols
10. Wireless Networking
11. IP Addressing & Network Services
12. Mobile Devices
13. Virtualization & Cloud Computing
14. Windows Operating Systems
15. Windows Commands & Utilities
16. Linux & macOS
17. Cybersecurity & Threats
18. Authentication & Access Control
19. Encryption & Security Technologies
20. Software Troubleshooting
21. Hardware & Network Troubleshooting
22. IT Operational Procedures
23. Important Acronyms
24. Common Exam Mistakes
25. Exam Strategies
26. Final Revision Checklist

---

# 1. EXAM OVERVIEW

CompTIA A+ requires passing TWO separate examinations.

| Exam | Main Focus | Passing Score |
|---|---|---|
| Core 1 (220-1201) | Hardware, networking, mobile devices, virtualization, troubleshooting | 675/900 |
| Core 2 (220-1202) | Operating systems, security, software troubleshooting, operational procedures | 700/900 |

Each exam:
- Maximum of 90 questions.
- 90 minutes.
- Multiple-choice questions.
- Performance-based questions (PBQs).
- Scored on a scale of 100–900.

## Core 1 Exam Weighting

| Domain | Weight |
|---|---:|
| Mobile Devices | 13% |
| Networking | 23% |
| Hardware | 25% |
| Virtualization and Cloud Computing | 11% |
| Hardware and Network Troubleshooting | 28% |

## Core 2 Exam Weighting

| Domain | Weight |
|---|---:|
| Operating Systems | 28% |
| Security | 28% |
| Software Troubleshooting | 23% |
| Operational Procedures | 21% |

**Study priority:** Pay particular attention to troubleshooting, networking, hardware, operating systems and security.

---

# 2. COMPUTER HARDWARE

## HDD vs SSD

| Feature | HDD | SSD |
|---|---|---|
| Technology | Magnetic spinning platters | Flash memory |
| Speed | Slower | Faster |
| Moving parts | Yes | No |
| Noise | Can produce noise | Silent |
| Durability | More vulnerable to physical shock | More resistant |
| Cost per GB | Usually cheaper | Usually more expensive |

Remember:
- HDD = Mechanical storage.
- SSD = Flash storage.
- NVMe SSDs generally outperform SATA SSDs.

## SATA vs NVMe

**SATA SSD**
- Uses the SATA interface.
- Maximum theoretical SATA III bandwidth: 6 Gbps.
- Commonly associated with 2.5-inch drives.

**NVMe SSD**
- Uses PCIe lanes.
- Much higher potential speeds.
- Lower latency.
- Commonly installed in M.2 slots.

Important:
- M.2 describes a physical form factor.
- NVMe describes a storage communication protocol.
- Not every M.2 drive is NVMe.
- M.2 drives can use SATA or PCIe/NVMe.

## Storage Interfaces

| Interface | Purpose |
|---|---|
| SATA | Common HDD and SSD connection |
| NVMe | High-speed SSD protocol |
| SAS | Enterprise storage interface |
| SCSI | Storage device communication |
| USB | External storage connection |
| eSATA | External SATA connection |

## Optical Storage

| Type | Description |
|---|---|
| CD | Compact Disc |
| DVD | Digital Versatile Disc |
| Blu-ray | Higher-capacity optical storage |

## RAID Configurations

RAID = Redundant Array of Independent Disks.

| RAID | Minimum Drives | Purpose | Fault Tolerance |
|---|---:|---|---|
| RAID 0 | 2 | Striping / performance | None |
| RAID 1 | 2 | Mirroring | 1 drive |
| RAID 5 | 3 | Striping with parity | 1 drive |
| RAID 6 | 4 | Striping with dual parity | 2 drives |
| RAID 10 | 4 | Mirroring + striping | Depends on failed drives |

Remember:
- RAID 0 = Speed, no redundancy.
- RAID 1 = Copies data to another drive.
- RAID 5 = Distributed parity, one drive can fail.
- RAID 6 = Two drives can fail.
- RAID 10 = Combines RAID 1 and RAID 0.

IMPORTANT:
RAID is NOT a backup. Accidental deletion, ransomware and corruption can affect an entire RAID array.

---

# 3. CPUs, RAM & MOTHERBOARDS

## CPU

CPU = Central Processing Unit.

Responsible for executing instructions and processing data.

Important components:
- ALU: Arithmetic Logic Unit.
- Control Unit: Directs CPU operations.
- Registers: Very fast temporary storage.
- Cache: High-speed memory close to the CPU.
- Cores: Independent processing units.
- Threads: Execution sequences handled by CPU cores.

## CPU Cache

| Level | Description |
|---|---|
| L1 | Smallest and fastest |
| L2 | Larger, generally slower than L1 |
| L3 | Larger shared cache, generally slower than L2 |

## RAM

RAM = Random Access Memory.

- Temporary working memory.
- Volatile: Data disappears when power is lost.
- Holds active programs and operating system data.

| RAM Type | Description |
|---|---|
| DDR4 | Older mainstream memory generation |
| DDR5 | Newer generation with higher bandwidth |
| DIMM | Desktop memory module |
| SODIMM | Laptop/small-form-factor memory |
| ECC | Detects and corrects certain memory errors |

Remember:
- RAM is volatile.
- SSD/HDD storage is non-volatile.
- DDR4 and DDR5 are physically incompatible.
- ECC is commonly used in servers and workstations.
- RAM must be compatible with the motherboard and CPU.

## Memory Channels

- Single-channel: One memory channel.
- Dual-channel: Two memory channels.
- Quad-channel: Four memory channels.

Matched RAM modules installed in the correct motherboard slots can enable multi-channel operation.

## Motherboard

The main circuit board connecting computer components.

Important components:

| Component | Purpose |
|---|---|
| CPU Socket | Holds the processor |
| RAM Slots | Hold memory modules |
| PCIe Slots | Expansion cards and GPUs |
| SATA Ports | Connect SATA storage |
| M.2 Slots | Connect compatible SSDs |
| Chipset | Manages communication and connectivity |
| CMOS Battery | Maintains clock and firmware settings |
| BIOS/UEFI | Initializes hardware and manages boot process |
| TPM | Hardware-based security functions |

## Motherboard Form Factors

| Form Factor | Description |
|---|---|
| ATX | Standard full-size desktop board |
| Micro-ATX | Smaller motherboard |
| Mini-ITX | Compact motherboard |

## BIOS vs UEFI

**BIOS**
- Older firmware interface.
- Performs POST.
- Initializes hardware.
- Starts the boot process.

**UEFI**
- Modern replacement for traditional BIOS.
- Supports Secure Boot.
- Supports GPT booting.
- Supports large boot drives.
- Can provide a graphical configuration interface.

## POST

POST = Power-On Self-Test.

Checks hardware during startup.

Common POST failures:
- Memory problems.
- CPU problems.
- GPU problems.
- Motherboard problems.
- Power supply issues.

Possible indicators:
- Beep codes.
- Diagnostic LEDs.
- Error messages.

## CMOS Battery

Usually a CR2032 coin-cell battery.

Maintains:
- Real-time clock.
- Certain firmware settings.

Symptoms of a failing battery:
- Incorrect system date/time.
- BIOS/UEFI settings resetting.
- Startup warnings.

---

# 4. POWER SUPPLIES & CONNECTORS

## PSU

PSU = Power Supply Unit.

Converts AC electricity from the wall into DC power required by computer components.

Common voltage rails:

| Voltage | Typical Use |
|---|---|
| +3.3V | Logic and motherboard components |
| +5V | Logic and certain peripherals |
| +12V | CPU, GPU and motors |

## Common Power Connectors

| Connector | Purpose |
|---|---|
| 24-pin ATX | Motherboard power |
| 4/8-pin EPS | CPU power |
| 6/8-pin PCIe | GPU power |
| 15-pin SATA | SATA drive power |
| 4-pin Molex | Older peripherals |

## 80 PLUS Certification

Measures PSU energy efficiency.

Common ratings:
- Bronze
- Silver
- Gold
- Platinum
- Titanium

Higher certification levels generally indicate greater efficiency under specified testing conditions.

## Important Concepts

- Redundant PSU: Secondary power supply for continued operation if one fails.
- UPS: Uninterruptible Power Supply.
- Surge Protector: Protects against voltage spikes.
- PDU: Power Distribution Unit.

Remember:
A UPS provides temporary battery power during an outage.

A surge protector primarily protects against voltage spikes.

---

# 5. DISPLAYS & PERIPHERALS

## Display Technologies

| Technology | Characteristics |
|---|---|
| LCD | Liquid crystal display technology |
| LED | LCD with LED backlighting |
| IPS | Better viewing angles and color reproduction |
| TN | Typically fast response times |
| OLED | Self-emissive pixels and excellent contrast |

## Display Connections

| Connector | Characteristics |
|---|---|
| HDMI | Digital audio and video |
| DisplayPort | Digital audio/video, common on PCs |
| VGA | Analog video |
| DVI | Primarily digital video, some variants support analog |
| USB-C | Reversible connector, supports various data/display capabilities |
| Thunderbolt | High-speed data, display and PCIe capabilities |

Important:
- VGA is analog.
- HDMI and DisplayPort are digital.
- USB-C describes the connector, not necessarily its capabilities.
- Thunderbolt 3 and 4 use the USB-C connector.

## USB Versions

| Standard | Theoretical Maximum Speed |
|---|---:|
| USB 2.0 | 480 Mbps |
| USB 3.2 Gen 1 | 5 Gbps |
| USB 3.2 Gen 2 | 10 Gbps |
| USB 3.2 Gen 2x2 | 20 Gbps |
| USB4 | Up to 40 Gbps or 80 Gbps depending on version |

Remember:
USB-C is a connector shape, not a speed specification.

## Common Peripherals

- Keyboard: Input.
- Mouse: Input.
- Monitor: Output.
- Printer: Output.
- Webcam: Input.
- Microphone: Input.
- Speakers: Output.
- Touchscreen: Input and output.
- Scanner: Input.

---

# 6. PRINTERS

## Printer Types

| Printer | How It Works | Common Use |
|---|---|---|
| Inkjet | Sprays liquid ink | Home printing, photographs |
| Laser | Uses toner and a laser imaging process | Offices, high-volume printing |
| Thermal | Uses heat | Receipts |
| Impact / Dot Matrix | Pins strike an ink ribbon | Multipart forms |

## Laser Printer Process

Memorize this sequence:

1. Processing
2. Charging
3. Exposing
4. Developing
5. Transferring
6. Fusing
7. Cleaning

Explanation:

- Processing: Printer processes the print job.
- Charging: Drum receives an electrical charge.
- Exposing: Laser writes the image onto the drum.
- Developing: Toner attaches to the image.
- Transferring: Toner transfers to paper.
- Fusing: Heat and pressure permanently bond toner to paper.
- Cleaning: Remaining toner is removed.

## Common Printer Problems

| Symptom | Possible Cause |
|---|---|
| Faded printing | Low toner or ink |
| Vertical lines | Dirty or damaged drum |
| Paper jams | Misaligned paper or damaged rollers |
| Ghosting | Drum or fuser issues |
| Smearing | Fuser or ink problem |
| Blank pages | Empty cartridge or imaging issue |
| Paper not feeding | Pickup roller problem |

## Printer Maintenance

**Inkjet**
- Clean printheads.
- Align cartridges.
- Replace ink cartridges.
- Prevent ink from drying.

**Laser**
- Replace toner.
- Inspect drum.
- Inspect fuser.
- Clean internal components.

**Thermal**
- Replace thermal paper.
- Clean printhead.

**Dot Matrix**
- Replace ribbon.
- Inspect printhead pins.

---

# 7. NETWORKING FUNDAMENTALS

## What Is a Network?

A network connects devices so they can communicate and share resources.

## Network Types

| Network | Meaning |
|---|---|
| PAN | Personal Area Network |
| LAN | Local Area Network |
| WLAN | Wireless Local Area Network |
| MAN | Metropolitan Area Network |
| WAN | Wide Area Network |
| SAN | Storage Area Network |
| VPN | Virtual Private Network |

## Network Devices

| Device | Purpose |
|---|---|
| Router | Connects different networks |
| Switch | Connects devices within a LAN |
| Hub | Broadcasts incoming traffic to all ports |
| Access Point | Provides wireless network access |
| Modem | Connects to an ISP service |
| Firewall | Filters network traffic |
| NIC | Connects a device to a network |
| Repeater | Regenerates or extends a signal |
| Patch Panel | Organizes network cabling |

## Router vs Switch

**Switch**
- Primarily operates at OSI Layer 2.
- Uses MAC addresses.
- Connects devices on a LAN.
- Can support VLANs.

**Router**
- Operates at OSI Layer 3.
- Uses IP addresses.
- Connects different networks.
- Uses routing tables.

## OSI Model

Memorize the seven layers from bottom to top.

| Layer | Name | Function |
|---|---|---|
| 7 | Application | User-facing network services |
| 6 | Presentation | Data formatting and encryption |
| 5 | Session | Establishes and manages sessions |
| 4 | Transport | TCP and UDP communication |
| 3 | Network | IP addressing and routing |
| 2 | Data Link | MAC addressing and frames |
| 1 | Physical | Cables, signals and connectors |

Memory trick:

**Please Do Not Throw Sausage Pizza Away**

Physical → Data Link → Network → Transport → Session → Presentation → Application.

Important:
- Layer 1 = Cables and signals.
- Layer 2 = MAC addresses and switches.
- Layer 3 = IP addresses and routers.
- Layer 4 = TCP and UDP.

## TCP vs UDP

| TCP | UDP |
|---|---|
| Connection-oriented | Connectionless |
| Reliable delivery | No delivery guarantee |
| Uses acknowledgements | No acknowledgements by default |
| Ordered delivery | No ordering guarantee |
| More overhead | Less overhead |

TCP examples:
- HTTPS.
- SSH.
- FTP.
- Email protocols.

UDP examples:
- DNS queries commonly use UDP.
- VoIP.
- Streaming.
- DHCP.

---

# 8. NETWORKING PORTS & PROTOCOLS

One of the most important memorization sections.

| Port | Protocol | Purpose |
|---:|---|---|
| 20/21 | FTP | File transfer |
| 22 | SSH | Secure remote access |
| 23 | Telnet | Unencrypted remote access |
| 25 | SMTP | Email transfer |
| 53 | DNS | Domain name resolution |
| 67/68 | DHCP | Automatic IP assignment |
| 69 | TFTP | Simple file transfer |
| 80 | HTTP | Unencrypted web traffic |
| 110 | POP3 | Email retrieval |
| 123 | NTP | Time synchronization |
| 143 | IMAP | Email synchronization |
| 161/162 | SNMP | Network monitoring |
| 389 | LDAP | Directory services |
| 443 | HTTPS | Secure web traffic |
| 445 | SMB | Windows file sharing |
| 465 | SMTPS | SMTP over implicit TLS |
| 514 | Syslog | System logging |
| 587 | SMTP Submission | Email submission |
| 636 | LDAPS | Secure LDAP |
| 993 | IMAPS | Secure IMAP |
| 995 | POP3S | Secure POP3 |
| 1433 | MS SQL | Microsoft SQL Server |
| 3389 | RDP | Remote Desktop Protocol |

## Important Comparisons

**SSH vs Telnet**
- SSH = Encrypted.
- Telnet = Unencrypted.
- Prefer SSH for secure remote administration.

**HTTP vs HTTPS**
- HTTP = Port 80.
- HTTPS = Port 443.
- HTTPS uses TLS encryption.

**POP3 vs IMAP**
- POP3 = Traditionally downloads email to a client.
- IMAP = Synchronizes email across multiple devices.

**SMTP**
- Used for sending email.

**DNS**
- Resolves domain names into IP addresses.

**DHCP**
- Automatically provides network configuration.

---

# 9. WIRELESS NETWORKING

## Wi-Fi Standards

| Standard | Wi-Fi Generation | Frequency |
|---|---|---|
| 802.11n | Wi-Fi 4 | 2.4 / 5 GHz |
| 802.11ac | Wi-Fi 5 | 5 GHz |
| 802.11ax | Wi-Fi 6 / 6E | 2.4 / 5 / 6 GHz |
| 802.11be | Wi-Fi 7 | 2.4 / 5 / 6 GHz |

## Wireless Frequencies

**2.4 GHz**
- Longer range.
- Better wall penetration.
- More interference.
- Usually lower speeds.

**5 GHz**
- Higher potential speeds.
- Shorter range than 2.4 GHz.
- Less interference in many environments.

**6 GHz**
- Additional wireless spectrum.
- Less congestion.
- Requires compatible devices.
- Generally shorter range and less wall penetration.

## Wireless Security

| Standard | Security |
|---|---|
| WEP | Insecure and outdated |
| WPA | Older security standard |
| WPA2 | Strong security when properly configured |
| WPA3 | Newer and stronger wireless security |

Remember:
WEP should never be considered secure.

## Wireless Technologies

- Bluetooth: Short-range wireless connections.
- NFC: Very short-range communication.
- RFID: Radio-frequency identification.
- GPS: Satellite-based positioning.
- Cellular: Mobile network communication.

## Common Wireless Problems

| Problem | Possible Cause |
|---|---|
| Weak signal | Distance or interference |
| Slow Wi-Fi | Congestion or interference |
| Cannot connect | Incorrect password or authentication |
| Intermittent connection | Signal interference |
| No internet | Router, ISP, DNS or gateway issue |

---

# 10. IP ADDRESSING & NETWORK SERVICES

## IPv4

IPv4 uses 32-bit addresses.

Example:
192.168.1.100

## IPv6

IPv6 uses 128-bit addresses.

Example:
2001:db8::1

IPv6 provides a significantly larger address space.

## Private IPv4 Ranges

Memorize these three ranges:

| Range | CIDR |
|---|---|
| 10.0.0.0 – 10.255.255.255 | 10.0.0.0/8 |
| 172.16.0.0 – 172.31.255.255 | 172.16.0.0/12 |
| 192.168.0.0 – 192.168.255.255 | 192.168.0.0/16 |

Private IP addresses are not directly routable over the public internet.

## APIPA

Automatic Private IP Addressing.

Range:
169.254.0.0/16

If a Windows computer receives an APIPA address, it often means the device could not contact a DHCP server.

Common causes:
- DHCP server unavailable.
- Network cable disconnected.
- Wireless connection issue.
- DHCP configuration problem.

## Important Network Concepts

**Subnet Mask**
Separates the network portion from the host portion of an IP address.

Example:
255.255.255.0 = /24

**Default Gateway**
The router address used to reach other networks.

**DNS**
Translates domain names into IP addresses.

**DHCP**
Automatically assigns:
- IP address.
- Subnet mask.
- Default gateway.
- DNS server.

**NAT**
Network Address Translation.

Allows private IP addresses to share public IP connectivity.

**VLAN**
Virtual LAN.

Logically separates devices into different network segments.

**VPN**
Virtual Private Network.

Creates an encrypted connection or tunnel over an existing network.

## DNS Record Types

| Record | Purpose |
|---|---|
| A | Maps hostname to IPv4 |
| AAAA | Maps hostname to IPv6 |
| CNAME | Alias to another hostname |
| MX | Mail server |
| TXT | Text information, including verification and email security records |
| NS | Authoritative name server |
| PTR | Reverse DNS lookup |

---

# 11. MOBILE DEVICES

## Mobile Device Components

Common components:
- Touchscreen.
- Battery.
- Camera.
- Microphone.
- Speakers.
- GPS.
- Accelerometer.
- Gyroscope.
- NFC.
- Bluetooth.
- Cellular modem.

## Mobile Connections

| Connection | Purpose |
|---|---|
| USB-C | Charging and data transfer |
| Lightning | Apple's older proprietary connector |
| Bluetooth | Wireless peripherals |
| NFC | Short-range communication |
| Wi-Fi | Wireless network access |
| Cellular | Mobile data and voice |
| Hotspot | Shares mobile internet access |

## Mobile Synchronization

Synchronization keeps data consistent across devices.

Examples:
- Contacts.
- Calendars.
- Photos.
- Emails.
- Documents.

Common synchronization problems:
- Incorrect account.
- Disabled synchronization.
- Insufficient storage.
- Network connectivity.
- Incorrect date/time.
- Authentication problems.

## Mobile Security

- Screen lock.
- Biometric authentication.
- Device encryption.
- Remote wipe.
- Mobile Device Management (MDM).
- Application permissions.
- Regular updates.

## MDM

Mobile Device Management.

Allows organizations to:
- Enforce security policies.
- Configure devices.
- Manage applications.
- Remotely lock devices.
- Remotely wipe devices.
- Monitor compliance.

---

# 12. VIRTUALIZATION & CLOUD COMPUTING

## Virtualization

Allows multiple virtual machines to run on one physical computer.

Benefits:
- Resource sharing.
- Isolation.
- Easier testing.
- Reduced hardware costs.
- Faster deployment.

## Hypervisor Types

**Type 1: Bare Metal**
Runs directly on physical hardware.

Examples:
- VMware ESXi.
- Microsoft Hyper-V.
- Xen.

**Type 2: Hosted**
Runs on top of an existing operating system.

Examples:
- Oracle VirtualBox.
- VMware Workstation.

Remember:
- Type 1 = Directly on hardware.
- Type 2 = Runs inside an existing OS.

## Virtual Machine Components

- Virtual CPU.
- Virtual RAM.
- Virtual storage.
- Virtual network adapter.
- Guest operating system.

Host = Physical machine.

Guest = Virtual machine operating system.

## Containers vs Virtual Machines

**Virtual Machines**
- Each VM runs its own guest operating system.
- More resource overhead.
- Strong isolation boundaries.

**Containers**
- Share the host operating system kernel.
- Lightweight.
- Faster deployment.
- Commonly used for application packaging.

Examples:
- Docker.
- Kubernetes.

## Cloud Computing

| Model | Meaning |
|---|---|
| IaaS | Infrastructure as a Service |
| PaaS | Platform as a Service |
| SaaS | Software as a Service |

**IaaS**
Provides virtual infrastructure.

Examples:
- Virtual machines.
- Virtual networks.
- Storage.

**PaaS**
Provides an application development and deployment platform.

Examples:
- Managed application hosting.
- Managed databases.

**SaaS**
Provides complete software applications over the internet.

Examples:
- Microsoft 365.
- Google Workspace.
- Salesforce.

## Cloud Deployment Models

| Model | Description |
|---|---|
| Public Cloud | Shared cloud infrastructure |
| Private Cloud | Dedicated cloud environment |
| Hybrid Cloud | Combination of public and private |
| Community Cloud | Shared by organizations with common requirements |

---

# 13. WINDOWS OPERATING SYSTEMS

## Windows Versions

Important versions:
- Windows 10.
- Windows 11.
- Windows Server.

Windows 11 has additional hardware security requirements, including TPM 2.0 and Secure Boot capability.

## Windows File Systems

| File System | Description |
|---|---|
| FAT32 | Older, broad compatibility, 4 GB maximum individual file size |
| exFAT | Suitable for external storage and large files |
| NTFS | Windows standard with permissions and journaling |
| ReFS | Resilient File System, used in supported Windows environments |

## NTFS Features

- File permissions.
- File compression.
- Encryption support through EFS.
- Journaling.
- Large file support.
- Disk quotas.

## Windows Editions

**Windows Home**
- Standard home-user features.

**Windows Pro**
- Business-oriented features.
- BitLocker support.
- Domain joining.
- Remote Desktop hosting.
- Group Policy.

**Windows Enterprise**
- Additional enterprise management and security features.

## Windows User Accounts

| Account | Purpose |
|---|---|
| Administrator | Full administrative permissions |
| Standard User | Limited permissions |
| Guest | Restricted guest access, where supported |
| Microsoft Account | Cloud-linked Windows account |
| Local Account | Account stored locally |

## Windows Tools

| Tool | Purpose |
|---|---|
| Task Manager | Processes and performance |
| Device Manager | Hardware drivers and devices |
| Disk Management | Partitions and disks |
| Event Viewer | System and application logs |
| Services | Manage Windows services |
| System Configuration | Startup and boot configuration |
| Resource Monitor | Detailed resource usage |
| Performance Monitor | System performance counters |
| Computer Management | Administrative tools |
| Windows Terminal | Command-line environment |

## Windows Recovery Options

**Safe Mode**
Starts Windows with minimal drivers and services.

Useful for:
- Driver issues.
- Software conflicts.
- Malware troubleshooting.

**System Restore**
Reverts system files and settings to a previous restore point.

**Startup Repair**
Attempts to repair boot-related problems.

**Reset This PC**
Reinstalls Windows with options to keep or remove personal files.

**Recovery Drive**
Provides recovery tools for Windows.

**System Image**
A complete image backup of a system.

---

# 14. WINDOWS COMMANDS & UTILITIES

Important commands to memorize.

## Networking Commands

| Command | Purpose |
|---|---|
| ipconfig | Displays IP configuration |
| ipconfig /all | Detailed network configuration |
| ipconfig /release | Releases DHCP address |
| ipconfig /renew | Requests new DHCP address |
| ipconfig /flushdns | Clears DNS resolver cache |
| ping | Tests network connectivity |
| tracert | Shows route to destination |
| nslookup | Queries DNS |
| netstat | Displays network connections |
| arp -a | Displays ARP cache |
| route print | Displays routing table |
| pathping | Combines route tracing and packet-loss analysis |

## Disk Commands

| Command | Purpose |
|---|---|
| chkdsk | Checks disk/file-system errors |
| sfc /scannow | Scans and repairs protected Windows system files |
| DISM | Repairs Windows image/component store |
| diskpart | Disk partition management |
| format | Formats a volume |

Important:
Run `DISM /Online /Cleanup-Image /RestoreHealth` to repair the Windows component store.

A common repair sequence is:

1. DISM /Online /Cleanup-Image /RestoreHealth
2. sfc /scannow

## System Commands

| Command | Purpose |
|---|---|
| tasklist | Lists running processes |
| taskkill | Terminates processes |
| systeminfo | Displays system information |
| hostname | Displays computer name |
| whoami | Displays current user |
| shutdown | Shuts down or restarts Windows |
| msconfig | System Configuration |
| services.msc | Opens Services |
| devmgmt.msc | Opens Device Manager |
| diskmgmt.msc | Opens Disk Management |
| eventvwr.msc | Opens Event Viewer |
| taskmgr | Opens Task Manager |
| gpedit.msc | Opens Local Group Policy Editor |
| regedit | Opens Registry Editor |
| perfmon | Opens Performance Monitor |
| msinfo32 | System Information |
| mstsc | Remote Desktop Connection |

## Windows Networking Troubleshooting Sequence

If a computer cannot access the internet:

1. Check physical connections.
2. Check Wi-Fi or Ethernet connectivity.
3. Run `ipconfig /all`.
4. Check the IP address.
5. Check the default gateway.
6. Ping the loopback address: `127.0.0.1`.
7. Ping the local gateway.
8. Ping a public IP address.
9. Test DNS with `nslookup`.
10. Check router, firewall and ISP connectivity.

Interpretation:

- Cannot ping 127.0.0.1: Possible local TCP/IP stack issue.
- Cannot ping gateway: Possible local network problem.
- Can ping public IP but not domain names: Possible DNS problem.
- APIPA address: Investigate DHCP.

---

# 15. LINUX & macOS

## Linux Basics

Linux is an open-source operating system commonly used in servers, networking and development environments.

Popular distributions:
- Ubuntu.
- Debian.
- Fedora.
- Red Hat Enterprise Linux.
- Linux Mint.

## Linux Commands

| Command | Purpose |
|---|---|
| pwd | Displays current directory |
| ls | Lists files |
| cd | Changes directory |
| mkdir | Creates directory |
| rmdir | Removes empty directory |
| touch | Creates an empty file |
| cp | Copies files |
| mv | Moves or renames files |
| rm | Removes files |
| cat | Displays file contents |
| less | Views files page by page |
| grep | Searches text |
| find | Searches for files |
| chmod | Changes permissions |
| chown | Changes ownership |
| sudo | Executes command with elevated privileges |
| ps | Displays processes |
| top | Monitors processes |
| kill | Terminates a process |
| df | Displays disk space |
| du | Displays directory/file space usage |
| ip addr | Displays network interfaces |
| ping | Tests connectivity |

## Linux Permissions

Three main permission types:

| Permission | Meaning |
|---|---|
| r | Read |
| w | Write |
| x | Execute |

Three permission categories:
- Owner.
- Group.
- Others.

Example:

`chmod 755 file.sh`

Meaning:
- Owner: Read, write, execute.
- Group: Read, execute.
- Others: Read, execute.

## macOS

Important macOS features:
- Finder: File management.
- Spotlight: Search.
- Activity Monitor: Process monitoring.
- Disk Utility: Disk management.
- Terminal: Command-line interface.
- Time Machine: Backup utility.
- Keychain Access: Credential management.

---

# 16. CYBERSECURITY & THREATS

## Common Security Threats

| Threat | Description |
|---|---|
| Virus | Malicious code that attaches to files/programs |
| Worm | Self-replicates across systems or networks |
| Trojan | Malware disguised as legitimate software |
| Ransomware | Encrypts or locks data for payment |
| Spyware | Secretly collects user information |
| Adware | Displays unwanted advertisements |
| Rootkit | Hides malicious activity and maintains privileged access |
| Keylogger | Records keyboard input |
| Botnet | Network of compromised devices |
| Logic Bomb | Activates when a condition is met |

## Social Engineering

Manipulating people into revealing information or performing actions.

| Attack | Description |
|---|---|
| Phishing | Fraudulent emails/messages |
| Spear Phishing | Targeted phishing |
| Whaling | Phishing targeting executives |
| Vishing | Voice-based phishing |
| Smishing | SMS-based phishing |
| Tailgating | Following someone into a restricted area |
| Shoulder Surfing | Observing someone entering sensitive information |
| Dumpster Diving | Searching discarded materials |
| Baiting | Offering something tempting to trick a victim |
| Pretexting | Creating a fabricated scenario to obtain information |

## Security Best Practices

- Use strong passwords.
- Enable MFA.
- Apply security updates.
- Use endpoint protection.
- Avoid suspicious attachments.
- Restrict administrative privileges.
- Encrypt sensitive information.
- Maintain backups.
- Use firewalls.
- Follow least privilege.

## Malware Removal Procedure

A typical safe malware-removal workflow:

1. Identify and research the symptoms.
2. Quarantine the infected system when appropriate.
3. Disable System Restore if required by the applicable removal procedure.
4. Remediate infected systems using approved tools.
5. Schedule and run scans.
6. Update anti-malware definitions.
7. Re-enable System Restore and create a clean restore point.
8. Educate the user.

Important:
Follow organizational procedures and preserve evidence when an incident requires investigation.

---

# 17. AUTHENTICATION & ACCESS CONTROL

## Authentication Factors

| Factor | Example |
|---|---|
| Something You Know | Password or PIN |
| Something You Have | Security key or phone |
| Something You Are | Fingerprint or face |
| Somewhere You Are | Geographic location |
| Something You Do | Behavioral patterns |

## MFA

Multi-Factor Authentication.

Requires two or more different authentication factors.

Example:
- Password + fingerprint.
- Password + hardware security key.

Important:
Password + PIN are both knowledge factors, so they are not necessarily MFA.

## Access Control Models

| Model | Description |
|---|---|
| DAC | Discretionary Access Control |
| MAC | Mandatory Access Control |
| RBAC | Role-Based Access Control |
| ABAC | Attribute-Based Access Control |

**DAC**
Resource owners determine access.

**MAC**
Access is determined by centrally enforced security labels and policies.

**RBAC**
Permissions are assigned based on job roles.

**ABAC**
Access depends on attributes such as user, device, resource and environment.

## Security Principles

**Least Privilege**
Users receive only the permissions required to perform their jobs.

**Need to Know**
Users access only information necessary for their responsibilities.

**Separation of Duties**
Critical tasks are divided among multiple people.

**Zero Trust**
Never automatically trust a user or device simply because it is inside the network.

---

# 18. ENCRYPTION & SECURITY TECHNOLOGIES

## Encryption Types

**Symmetric Encryption**
- Same key encrypts and decrypts data.
- Fast.
- Requires secure key distribution.

Examples:
- AES.

**Asymmetric Encryption**
- Uses public and private key pairs.
- Useful for key exchange and digital signatures.

Examples:
- RSA.
- ECC.

## Hashing

Converts data into a fixed-length digest.

Used for:
- Integrity verification.
- Password storage.
- Digital signatures.

Examples:
- SHA-256.
- SHA-512.

Important:
Hashing is one-way and is not encryption.

MD5 and SHA-1 are considered unsuitable for modern security-sensitive collision-resistant applications.

## Security Technologies

| Technology | Purpose |
|---|---|
| BitLocker | Windows full-volume encryption |
| EFS | NTFS file encryption |
| TPM | Hardware security module |
| Secure Boot | Prevents unauthorized boot components |
| TLS | Encrypts network communications |
| VPN | Encrypted network tunnel |
| Firewall | Filters network traffic |
| IDS | Detects suspicious activity |
| IPS | Detects and blocks suspicious activity |
| EDR | Endpoint detection and response |
| DLP | Data Loss Prevention |

## Certificates

Digital certificates help establish identity and support encrypted communication.

Important terms:
- CA: Certificate Authority.
- CSR: Certificate Signing Request.
- PKI: Public Key Infrastructure.
- CRL: Certificate Revocation List.

---

# 19. SOFTWARE TROUBLESHOOTING

## Common Windows Problems

| Symptom | Possible Cause |
|---|---|
| BSOD | Driver, hardware or OS problem |
| Slow performance | High CPU/RAM/disk usage |
| Application crashes | Software bug or compatibility |
| Boot failure | Bootloader, disk or OS problem |
| Random restarts | Overheating, PSU or system errors |
| Missing application | Uninstallation or corrupted installation |
| Driver failure | Incompatible or corrupted driver |
| No internet | Network configuration or connectivity |

## BSOD

Blue Screen of Death.

Possible causes:
- Faulty RAM.
- Driver conflicts.
- Hardware failure.
- Corrupted system files.
- Storage problems.
- Overheating.

Useful tools:
- Event Viewer.
- Device Manager.
- Windows Memory Diagnostic.
- SFC.
- DISM.
- Reliability Monitor.

## Application Troubleshooting

If an application crashes:

1. Identify when the crash occurs.
2. Check system requirements.
3. Restart the application.
4. Update the application.
5. Check for OS compatibility.
6. Check Event Viewer.
7. Repair or reinstall the application if necessary.

## Startup Problems

Possible causes:
- Corrupt boot files.
- Incorrect boot order.
- Failed storage drive.
- Driver problems.
- Corrupted operating system.

Useful tools:
- Startup Repair.
- Safe Mode.
- System Restore.
- Windows Recovery Environment.

---

# 20. HARDWARE & NETWORK TROUBLESHOOTING

## Troubleshooting Methodology

A structured troubleshooting process:

1. Identify the problem.
2. Establish a theory of probable cause.
3. Test the theory.
4. Establish a plan of action.
5. Implement the solution.
6. Verify full system functionality.
7. Document findings and actions.

## Common Hardware Symptoms

| Symptom | Likely Cause |
|---|---|
| No power | PSU, cable, outlet or motherboard |
| No display | GPU, monitor, cable or RAM |
| Random shutdowns | Overheating or power issues |
| Loud fans | Dust or high temperatures |
| Beep codes | POST hardware failure |
| Slow boot | Storage or startup issues |
| Clicking HDD | Possible mechanical failure |
| Memory errors | Faulty or incompatible RAM |
| USB not recognized | Port, driver or device issue |

## Networking Troubleshooting

| Symptom | Likely Cause |
|---|---|
| No network connection | Cable, NIC, switch or Wi-Fi |
| APIPA address | DHCP failure |
| Can access IP but not domain | DNS problem |
| Cannot reach external networks | Gateway or routing issue |
| Intermittent Wi-Fi | Interference or weak signal |
| Slow network | Congestion, duplex or bandwidth issue |
| Duplicate IP | IP address conflict |

## Common Network Tools

| Tool | Purpose |
|---|---|
| Cable Tester | Tests network cable wiring |
| Tone Generator | Sends signal through cable |
| Tone Probe | Locates cable |
| Crimper | Attaches connectors |
| Punchdown Tool | Terminates wires in patch panels |
| Loopback Plug | Tests network interface |
| Multimeter | Measures electrical values |
| Wi-Fi Analyzer | Identifies wireless channels and interference |
| Protocol Analyzer | Examines network traffic |

## Ethernet Cable Types

**Straight-Through**
Traditionally connects unlike devices.

Examples:
- PC to switch.
- Router to switch.

**Crossover**
Traditionally connects like devices.

Examples:
- PC to PC.
- Switch to switch.

Modern networking equipment commonly supports Auto-MDI-X, reducing the need for crossover cables.

## Cable Categories

| Category | Common Maximum Rated Frequency |
|---|---:|
| Cat 5e | 100 MHz |
| Cat 6 | 250 MHz |
| Cat 6a | 500 MHz |
| Cat 8 | 2000 MHz |

Remember:
Higher cable category does not automatically mean every connection operates at its maximum rated speed.

---

# 21. IT OPERATIONAL PROCEDURES

## Documentation

Good IT documentation should include:
- Problem description.
- Device information.
- Troubleshooting steps.
- Root cause.
- Resolution.
- Time and date.
- User communication.
- Escalation details.

## Change Management

A controlled process for making changes to IT systems.

Typical process:
1. Submit change request.
2. Assess risks and impact.
3. Obtain approval.
4. Schedule implementation.
5. Implement change.
6. Verify results.
7. Document the change.

## Backup Types

| Backup | Description |
|---|---|
| Full | Copies all selected data |
| Incremental | Copies changes since the last backup |
| Differential | Copies changes since the last full backup |

Important:

**Full**
- Most complete.
- Requires more storage.
- Simplest restore process.

**Incremental**
- Faster individual backups.
- Requires the last full backup and every subsequent incremental backup for restoration.

**Differential**
- Requires the last full backup and the latest differential backup for restoration.

## 3-2-1 Backup Rule

Maintain:
- 3 copies of important data.
- 2 different storage types.
- 1 offsite copy.

An offline or immutable copy also helps protect against ransomware.

## Disaster Recovery

Important terms:

**RTO**
Recovery Time Objective.

How quickly a system must be restored.

**RPO**
Recovery Point Objective.

How much data loss, measured in time, is acceptable.

Remember:
- RTO = Time to restore.
- RPO = Acceptable data loss.

## Safety

- Use an ESD wrist strap when appropriate.
- Ground yourself before handling components.
- Disconnect power before internal hardware work.
- Avoid working on energized components unless specifically required and trained.
- Maintain proper ventilation.
- Use appropriate PPE.
- Follow lockout/tagout procedures where applicable.

## ESD

Electrostatic Discharge.

A sudden transfer of static electricity that can damage sensitive electronic components.

Prevention:
- Anti-static wrist strap.
- Anti-static mat.
- Proper grounding.
- Appropriate component handling.

## Incident Response

Typical incident response stages:

1. Preparation.
2. Identification.
3. Containment.
4. Eradication.
5. Recovery.
6. Lessons Learned.

---

# 22. IMPORTANT ACRONYMS

| Acronym | Meaning |
|---|---|
| CPU | Central Processing Unit |
| GPU | Graphics Processing Unit |
| RAM | Random Access Memory |
| ROM | Read-Only Memory |
| PSU | Power Supply Unit |
| SSD | Solid State Drive |
| HDD | Hard Disk Drive |
| NVMe | Non-Volatile Memory Express |
| RAID | Redundant Array of Independent Disks |
| BIOS | Basic Input/Output System |
| UEFI | Unified Extensible Firmware Interface |
| POST | Power-On Self-Test |
| TPM | Trusted Platform Module |
| NIC | Network Interface Card |
| LAN | Local Area Network |
| WAN | Wide Area Network |
| WLAN | Wireless Local Area Network |
| VPN | Virtual Private Network |
| DNS | Domain Name System |
| DHCP | Dynamic Host Configuration Protocol |
| NAT | Network Address Translation |
| TCP | Transmission Control Protocol |
| UDP | User Datagram Protocol |
| IP | Internet Protocol |
| MAC | Media Access Control |
| VLAN | Virtual Local Area Network |
| APIPA | Automatic Private IP Addressing |
| OSI | Open Systems Interconnection |
| SSH | Secure Shell |
| RDP | Remote Desktop Protocol |
| HTTP | Hypertext Transfer Protocol |
| HTTPS | Hypertext Transfer Protocol Secure |
| FTP | File Transfer Protocol |
| SMTP | Simple Mail Transfer Protocol |
| SNMP | Simple Network Management Protocol |
| LDAP | Lightweight Directory Access Protocol |
| SMB | Server Message Block |
| MFA | Multi-Factor Authentication |
| EDR | Endpoint Detection and Response |
| IDS | Intrusion Detection System |
| IPS | Intrusion Prevention System |
| DLP | Data Loss Prevention |
| MDM | Mobile Device Management |
| PKI | Public Key Infrastructure |
| AES | Advanced Encryption Standard |
| ESD | Electrostatic Discharge |
| RTO | Recovery Time Objective |
| RPO | Recovery Point Objective |
| UPS | Uninterruptible Power Supply |
| SLA | Service Level Agreement |
| SOP | Standard Operating Procedure |

---

# 23. COMMON EXAM MISTAKES

These are important distinctions that are easy to confuse during the exam.

## Hardware

- M.2 does not automatically mean NVMe.
- RAM is volatile; SSD storage is non-volatile.
- RAID 0 has NO redundancy.
- RAID is not a backup.
- DDR4 and DDR5 are not interchangeable.
- A PSU converts AC to DC.
- A dead CMOS battery can reset the clock and firmware settings.
- UEFI is newer than traditional BIOS.
- USB-C does not automatically mean Thunderbolt.

## Networking

- Switches primarily use MAC addresses.
- Routers use IP addresses.
- DNS resolves names; DHCP assigns network configuration.
- APIPA usually indicates a DHCP problem.
- SSH is secure; Telnet is not.
- HTTPS uses port 443; HTTP uses port 80.
- SMTP sends email; IMAP and POP3 retrieve email.
- TCP is reliable; UDP does not guarantee delivery.
- A default gateway is needed to reach other networks.
- A private IP is not directly routable over the public internet.

## Operating Systems

- Task Manager monitors processes and performance.
- Device Manager manages hardware and drivers.
- Disk Management manages partitions and volumes.
- Event Viewer displays logs.
- `ipconfig /flushdns` clears DNS cache.
- `sfc /scannow` checks protected Windows system files.
- `chkdsk` checks file-system and disk-related errors.
- Safe Mode loads Windows with minimal drivers and services.
- System Restore is not the same as a full backup.

## Security

- Hashing is not encryption.
- MFA requires different authentication factors.
- Least privilege means minimum necessary permissions.
- Ransomware encrypts or locks data.
- Phishing uses deception to obtain information.
- A firewall filters traffic.
- IDS detects suspicious activity.
- IPS can actively block suspicious traffic.
- WPA3 is newer than WPA2.
- WEP is insecure.

## Cloud & Virtualization

- Type 1 hypervisor runs directly on hardware.
- Type 2 hypervisor runs on an existing operating system.
- SaaS provides complete software applications.
- PaaS provides an application platform.
- IaaS provides infrastructure.
- Containers share the host OS kernel.
- Virtual machines run their own guest operating systems.

## Troubleshooting

- Always gather information before replacing hardware.
- Do not assume the most expensive component is defective.
- Verify the fix after implementing it.
- Document changes and results.
- Do not perform destructive actions without considering data loss.
- Check simple causes before complex ones.

---

# 24. EXAM STRATEGIES

## 1. Read the Entire Question

CompTIA questions frequently contain important wording.

Watch for:
- FIRST.
- NEXT.
- BEST.
- MOST LIKELY.
- MOST SECURE.
- LEAST EXPENSIVE.
- MINIMUM DOWNTIME.

These words change the correct answer.

Example:

A user cannot access the internet. Their computer has an APIPA address.

The best initial direction is to investigate DHCP connectivity rather than immediately reinstalling Windows.

## 2. Identify the Actual Problem

Do not jump to a solution.

Ask yourself:
- Is this a hardware problem?
- Is this a software problem?
- Is this a network problem?
- Is this a security problem?
- Is this a user configuration problem?

Identify the category before choosing an answer.

## 3. Eliminate Incorrect Answers

For multiple-choice questions:

1. Identify what the question is asking.
2. Remove answers unrelated to the problem.
3. Compare the remaining options.
4. Choose the answer that best satisfies the scenario.

Sometimes multiple answers could work, but only one is the BEST answer.

## 4. Understand PBQs

Performance-Based Questions test practical knowledge.

You may be asked to:
- Configure network settings.
- Identify hardware components.
- Troubleshoot a system.
- Configure security settings.
- Match ports and protocols.
- Configure operating systems.

Practice doing tasks rather than only memorizing definitions.

## 5. Manage Your Time

Each exam is 90 minutes.

Recommended strategy:
- Answer straightforward questions first.
- Flag difficult questions.
- Avoid spending too long on one question.
- Return to flagged questions.
- Reserve time for PBQs and review.

## 6. Do Not Overthink

If the scenario describes a specific symptom, look for the technology directly associated with that symptom.

Examples:

| Scenario | Think About |
|---|---|
| 169.254.x.x | DHCP |
| Website names fail but IP connectivity works | DNS |
| No power | PSU / power connection |
| No display | Monitor / GPU / cable |
| Cannot connect to remote desktop | RDP / firewall / connectivity |
| Slow computer | CPU / RAM / storage |
| Laptop overheats | Cooling / ventilation |
| Files encrypted unexpectedly | Ransomware |

## 7. Learn Through Scenarios

Do not memorize only:

"What is DHCP?"

Also understand:

"A workstation cannot obtain an IP address automatically. What service should be investigated?"

Answer: DHCP.

The goal is to recognize the technology when presented with a real-world IT support problem.

---

# 25. FINAL REVISION CHECKLIST

Use this checklist before scheduling your exams.

## Core 1

### Hardware
- [ ] HDD vs SSD
- [ ] SATA vs NVMe
- [ ] RAID 0, 1, 5, 6 and 10
- [ ] CPU and motherboard components
- [ ] DDR4 vs DDR5
- [ ] DIMM vs SODIMM
- [ ] BIOS vs UEFI
- [ ] POST and CMOS battery
- [ ] PSU connectors and voltage rails
- [ ] Display connectors
- [ ] USB versions
- [ ] Printer technologies and laser printing sequence

### Networking
- [ ] OSI model
- [ ] TCP vs UDP
- [ ] Common ports and protocols
- [ ] Router vs switch
- [ ] DNS vs DHCP
- [ ] Private IP ranges
- [ ] APIPA
- [ ] Subnet masks
- [ ] Default gateway
- [ ] NAT and VLANs
- [ ] Wireless standards
- [ ] Wireless security
- [ ] Network troubleshooting commands
- [ ] Ethernet cable categories

### Mobile Devices
- [ ] Mobile device components
- [ ] Bluetooth and NFC
- [ ] Mobile synchronization
- [ ] Hotspots and tethering
- [ ] MDM
- [ ] Mobile security

### Virtualization & Cloud
- [ ] Type 1 vs Type 2 hypervisors
- [ ] Virtual machines vs containers
- [ ] IaaS vs PaaS vs SaaS
- [ ] Public vs private vs hybrid cloud

### Troubleshooting
- [ ] Hardware symptoms
- [ ] Network symptoms
- [ ] Printer troubleshooting
- [ ] Display troubleshooting
- [ ] Common diagnostic tools

## Core 2

### Operating Systems
- [ ] Windows editions
- [ ] Windows file systems
- [ ] NTFS permissions
- [ ] Windows administrative tools
- [ ] Windows command-line utilities
- [ ] Linux commands
- [ ] macOS utilities
- [ ] Windows recovery options

### Security
- [ ] Malware types
- [ ] Social engineering attacks
- [ ] Authentication factors
- [ ] MFA
- [ ] Access control models
- [ ] Least privilege
- [ ] Encryption vs hashing
- [ ] BitLocker and EFS
- [ ] TPM and Secure Boot
- [ ] Firewalls, IDS and IPS
- [ ] Malware removal

### Software Troubleshooting
- [ ] BSOD
- [ ] Application crashes
- [ ] Driver issues
- [ ] Boot problems
- [ ] Windows recovery
- [ ] System performance problems

### Operational Procedures
- [ ] Documentation
- [ ] Change management
- [ ] Backup types
- [ ] 3-2-1 backup rule
- [ ] RTO vs RPO
- [ ] Incident response
- [ ] ESD protection
- [ ] Workplace safety
- [ ] Professional communication
- [ ] Environmental and disposal procedures

---

# 26. HOW TO STUDY EFFECTIVELY

My recommended study routine:

### Step 1 — Learn
Study one topic at a time. Understand what the technology does and why it is used.

### Step 2 — Memorize
Use flashcards for:
- Ports.
- Protocols.
- Acronyms.
- Hardware components.
- Windows commands.
- RAID configurations.

### Step 3 — Apply
Use scenario-based questions and practical labs.

Examples:
- Diagnose a computer with no internet.
- Configure a static IP address.
- Identify a failing hardware component.
- Troubleshoot a Windows startup problem.
- Configure file permissions.

### Step 4 — Test
Complete practice exams without looking at your notes.

### Step 5 — Review Mistakes
For every incorrect answer:
1. Write down the question's topic.
2. Understand why your answer was incorrect.
3. Understand why the correct answer is correct.
4. Add the concept to your revision notes.

### Step 6 — Reassess
Repeat practice exams until your scores are consistently above the passing threshold, with a comfortable margin.

**Final advice:** Do not study just to recognize definitions. Study until you can explain what a technology does, identify when it is used, and troubleshoot a situation involving it.
