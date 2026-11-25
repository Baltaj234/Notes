
# Comptia ++ Flashcard definitions

Plenum Cable - fire-rated cabling with low-smoke jacketing required in air-handling spaces (plenums) by fire code.

no power at all, first check - Verify the wall outlet, PSU power switch, and power cable. Confirm the PSU voltage switch and front panel button wiring.

Linux: cat, nano, vi - cat displays a file, nano and vi are text editors for config files.

malware: Spyware / keylogger - Secretly collects user activity/keystrokes and data.

PII, PHI, PCI handling - Protect personally Identifiable info, Health Info (HIPAA), and cardholder data (PCI DSS) with encryption and access control. Report breaches.

Standard vs adminstrator account - Standard users run with the least privilege. Admin accounts can change the core system. Use standard accounts for daily work.

printer: garbled output - Often the wrong/corrupt driver. Reinstall the correct driver and clear the print queue.

Intermiitent connectivity - Check for loose cables, interference, failing NIC/cable, duplex mismatch, or an overloaded AP.

on-demand self-service - A core cloud characteristic. Users provision resources instantly through a portal/API without human intervention.

Wifi: 2.4 GHz, 5 GHz, 6 GHz - 2.4 GHz is a longer range, more inference, slower. 5 GHz is faster, but shorter range. 6 GHz (Wi-Fi 6E) adds more clean spectrum.

DoS/DDoS - Flooding a service with traffic to make it unavailable. DDoS uses many distributed sources (A botnet).

Antivirus, anti-malware, EDR - Software that detects, quarantines, and remove malware. EDR adds behavioral detection and response.

Sandbox - An isolated environment for running or testing untrusted code/apps without affecting the host system.

Bitlocker - Windows full system encryption (Pro+) that uses TPM to protect data if a device is lost or stolen.

80 plus rating - A certification of PSU efficiency (Bronze, Silver, Gold Platinum, Titanium). Higher teirs waste less power as heat.

Physical Security Controls - Locks, badges, access cards, access control vestibules, bollards, fences, security guards and cameras.

touchpad and function keys - Fn key toggles laptop functions (brightness, volume, external display, wireless, keyboard backlight).

SMART Errors - Self monitoring data warning of impending drive failure. Back up and replace drive.

Self grounding, equipment grounding - Touch a grounded metal part before handling components when no strap is available. Ensure equipment is properly grounded.

ipconfig - Windows command to manage all IP configuration (/all, /release, /renew, /flushdns).

Replacing a laptop battery - Use a manufacturer approved Li-ion pack. A swelling battery is a safety hazard and must be replaced and recycled, not punctured.

TPM - Trusted platform module. A chip that stores cryptographic keys. Required for bitlocker and windows 11 (TPM 2.0).

Mobile connection: NFC - Near field communication. Very short range wireless tap to pay and pairing.

Biometrics - Authentication by physical traits. Fingerprint, face, retina/iris, voice.

USB-c and Thunderbolt - USB-C is a reversible connector. Thunderbolt 3/4 uses the USB-C connector to add very high bandwidth, PCIe tunneling, and DisplayPort for docks and external GPU's. 

Comptia troubleshooting step 6 - Documents findings, actions and outcomes. 

MacOS: Disk Utility - Repairs disks (first aid),formats and manages volumes/images. 

Multimeter use - Measures voltage, current and resistance continuity. Used to test PSU rails, cables, and fuses.

ECC RAM - Error correcting code memory defects and corrects single bit errors. Used in servers/workstations where data integrity is critical. Requires CPU/board support.

Zero-day - an attack exploiting a vulnerability before a patch exists.

System requirements check - Before install/upgrade, confirm CPU, RAM, storage, and (for windows 11) TPM 2.0 and Secure Boot.

Printer: ghosted/repeating images (laster) - A worn drum or fuser leaving a faint repeating image. Replace the affected component.

Continous reboots / no boot - Could be overheating, failing PSU, bad RAM, or corrupt OS. Test components and check temps and event logs.

What is BIOS/UEFI - Firmware on the motherboard that initializes hardware at power-on (POST) and starts the boot process. UEFI is the modern replacement with GUI, secure boot, and >2TB GPT disk support.

Raid not found / array failure - a drive dropped from the array. Replace the failed disk and rebuild. Never write to the degraded array carelessly. 

NVMe M.2 keying - M-key slots carry PCIe x4 (NVMe). B-key carries SATA/PCIe x2. B+M cards fit on both but at lower speed.

Cloud model: SaaS - Software as a Service. Ready to use applications over the internet. The provider manages everything.

Linux Sudo/su - Sudo runs a single command with elevated rights. su switches to another (often root) user.

Registory Editor (regedit) - Edits the Windows Registry. The hierarchical database of the OS/app settings. Back up before editing. 

Molex vs SATA power connectors - Molex is the older 4-pin DC connector for legacy drives/fans. SATA power is the flat 15-pin connector for modern drives.

Social Engineering: impersonation/pretexting - Pretending to be someone (IT, a vendor, an executive) with a fabricated story to gain access or info.

App won't open/crashes = Repair or reinstall app, update it/the OS, check compatability, clear cache, and review event logs.

Thermal printer - Uses heat to create images on heat-sensitive paper (receipts) or via a ribbon. Maintenance : replace paper/ribbon and clean the heating element.

NTFS vs FAT32 vs exFAT - NTFS is windows default with permissions, encryption and journaling. FAT32 is the max 4GB file size, broad compatability. exFAT has large files for flash/cross platform.

eSATA - external SATA. A port for connecting external drives at internal SATA speeds.

Cloud file synchronization - Services (OneDrive, iCloud, Google Drive) that keep files mirrored across devices and the cloud automatically. 

Cloud sync requirements - Sign in to the same account on each device and enable the sync service.

Sync conflicts - Review duplicate or conflicting copies instead of overwriting the wrong version.

Offline access - Changes made while offline are uploaded when the device reconnects.

Cloud sync security - Use strong authentication, MFA, encryption, and approved devices.

Selective sync - Download only needed folders to conserve storage, but remember that excluded folders may not be available offline.

Documentation: ticketing and KB - Track issues with clear, complete tickets. Document fixes in a knowledge base for reuse.

Change Management - A documented process to request, assess, approve, schedule, implement and review changes. Reduces risk and outages.

Change management components - Documented business reason, scope, risk analysis, rollback plan, end-user acceptance, change board approval, and a maintenance window.

What is a hypervisor host's storage controller (HBA) - A host bus adapter connects a server to storage (SAS/Fibre Channel) without RAID logic, passing drives to the OS or software RAID.

What is RAM - Random Access Memory. Fast, volatile system memory that holds running programs and data. Cleared when power is lost.

Comptia troubleshooting step 2 - Establish a theory of probable cause. Question the obvious. Consider multiple approaches (top-to-bottom / divide-and-conquer).

SODIMM - Small Outline DIMM. The compact RAM form factor used in laptops and small form factor PCs.

PCIe - Peripheral Component Interconnect Express. The high speed expansion bus for GPU's, NVMe, SSDs, and add-in cards. Slots come in x1, x4, x8, x16 lane widths.

Data at rest vs in transit - Encrypt stored data (Bitlocker/filevault) and data moving over networks (TLS/HTTPS, VPN).

Dual displays on a laptop - Extend or mirror to external monitors via HDMI/DisplayPort/USB-C. Toggle modes with display key or Win + P.

Social Engineering: Shoulder Surfing - Observing someone's screen/keypad to steal credentials and data.

Cloud model PaaS - Platform as a Service - a managed environment to build and deploy apps without managing servers or the OS.

Slow Performance - Check resource usage (Task Manager), startup apps, malware, disk space, overheating and pending updates.

thermal paste - A heat conductive compound applied between the CPU and heatsink to fill microscopic gaps and improve heat transfer.

Hard drive sanitization - Securely erase data before disposal/reuse. drive wipe (overwrite), secure erase, deguassing or physical destruction. 

Certificate warning in browser - an invalid/expired/untrusted certificate. Verify the site, check the system clock and don't bypass for sensitive sites.

ATX vs ITX form factors - ATX is the full size motherboard standard. MicroATX and mini-ITX are progressively smaller with fewer expansions slots for compact builds. 

Clean install - Wipes the drive and installs a fresh OS. Best for major issues. Requires backing up data first.

What is a switch - A layer-2 device that forwards frames between devices on the same LAN using MAC addresses. Each port is its own collision domain.

Ports 110/143 - 110 is for POP3 (downloads mail), 143 is for IMAP (syncs mail across devices).

Trusted vs untrusted software sources - Install sofware only from reputable vendors. Untrusted sources are a top malware vector.

Duplexing assembly - The printer component that automatically prints on both sides of the page.

printer: faded prints - For laser printers low toner or a failing transfer process. For inkjet printers low ink or clogged heads. Replace/clean as needed.

Remote support tools - RDP, SSH, VNC, MSRA (quick assist) and third party tolls provide remote access. Secure them and get consent.

Why educate the user last - User behaviour is the most common infection vector. Training prevents recurrence after the cleanup.

Difference between SATA and NVMe storage - SATA SSDs use the AHCI/SATA bus (=600 MB/s max). NVMe SSDs run over PCIe lanes (M.2 or add-in), giving multi-GB/s speeds and much lower latency. 

Cellular standards - Devices roam between LTE/4G and 5G. PRL/baseband updates keep the radio working with carrier networks.

Hot-swappable - Hardware (RAID drives, USB devices) that can be added or removed while the system is running.

Overheating symptoms - thermal shutdowns, throttling, loud fans, clean dust, reseat/replace heatsink, reapply thermal paste, check fan operation.

Windows in-place upgrade - Installs a new windows version while keeping apps, settings, and files.

Common PSU rails - +3.3V and +5V power logic and older peripherals. +12V power the CPU, GPU and drive motors and is the dominant rail in modern systems.

Fiber: single mode vs multimode - single mode means small core, laser, very long distance. Multimode means larger core, LED/VCSEL, shorter distance, cheaper.

macOS: Time Machine - Apple's built-in automatic backup to an external/network drive allowing point in time restores.

CIA triad - The core security goals. Confidentiality (keep data private), Integrity (keep it accurate/unaltered) and Availability (keep it accessible).

Hotspot/tethering - Sharing a phone's cellular data with other devices over Wi-fi (hotpost), USB, or bluetooth (tethering).

## General Notes

SSD's are faster than HDD's. An HDD is cheaper per GB. an SSD used flash memory faster.

Cloud uses are often billed by use. The consumption model makes it cost effective.

Disk management is important. Its a GUI tool to initialize, partition, format and resize disks and change drive letters. Drive letters are labels Windows assigns to drives or partitions. 

TCP and UDP protocols are important. TCP is connection-oriented and reliable. UDP is connectionless and fast with no guarantees. Typically UDP is used for streaming.

Every company has an AUP. It stands for Acceptable Use Policy. How company employees can use company software or data. Strict rules and regulations.

3 2 1 backup rule is important. Keep 3 copies of data, on 2 different media and 1 copy offsite. Protects against most problems and failures.

Whenever an incident happens document what happened and how it was resolved, who handled it and when? Report incidents with proper documentation and through proper communication channels.

Wireless Security has three main standards. WEP is broken and should never be used. WPA2 is acceptable. WPA 3 is the modern standard and strongest of them all.

MAC is related to everything in hardware. MAC filtering is an important technique where a service can allow/deny devices depending in their hardware (MAC) address.

Many common Linux commands should be studyed properly including file manipulation, finding files and information using only the terminal and common network commands.

Network Address translation lets many private IPs use the same public IP. Primarily done to hide internal addresses. Devices using private IP's cannot be routed directly on the public internet.

The Recovery partition is important. It is a hidden partition in Windows with a Windows recovery environment for repair, reset and startup repair.

Startup repair fixes windows boot problems. It can repair corrupted boot files, the boot configuration, and startup components. Used when Windows fails to start or gets stuck at startup. 

System restore uses an earlier restore point to restore system files, registry settings and installed updates/drivers. It does not normally affect personal files.

Reset this PC reinstalls Windows. Two ways it can be done. Keep my files which removes apps and settings up preserves personal files. Remove everything wipes apps, settings, and personal files for a factory reset.

IOT devices are devices that are segmented from the main devices. Many smart-home devices are good examples.

Many different boot methods for an operating system. Some examples include booting from a USB, optical, network or internal device.

If a mobile phone has battery drain and overheating it could be due to a variety of factors. Including rogue apps often dowloaded from 3rd party providers (not the official app store on that device), battery needing to get replaced or a poor signal meaning the device is constantly trying to find a connection.

POST beep codes are important patterns at computer startup which indicate which component of the computer failed.
Happens before video output is available.

Coaxial cable carries cable TV and cable internet signals using F-type connectors.

SSH is an important protocol. Widely used for starting remote connections with other machines. The process takes place on port 22.

Authentication and authorization are different things, remember this. Authentication proves who you are, while authorization determines what you are allowed to do.

Trojan is a powerful piece of malware used in today's world. It masks itself as legitimate software. Opens a backdoor when run and infects your machine.

Know the different Comptia troubleshooting steps in order

Standard formatting and secure erase are very different concepts. A standard format leaves data recoverable, while a secure erase removes any and all data. When dealing with sensitive data that must be fully wiped, secure erase is the best method.

HTTP is unencrypted web while HTTPS is  TLS encrypted web. Subtle difference.

TLS (Transport Layer Security) is the protocol that encrypts and secures communications between a web browser and a server, forming the foundation of HTTPS.

An Esim lets people switch phone carriers without a physical sim card. Embedded into the mobile device itself. Many modern phones have it now.

Many optical drive types including CD, Blue-Ray and DVD. Reading and writing optical disks is rare in modern PCs.

Integrated vs dedicated GPU is an important concept. An integrated GPU is part of the CPU and shares RAM with the rest of the computer. A dedicated GPU is seperate from teh CPU and has its own VRAM it uses. As a result dedicated GPUs have much higher performance.

Worm is an self-replicating malware that spreads on its own without any user action.

Multifactor authentication is becoming increasingly standard in the modern world. Requires two things to sign in to an account, a password and something you have (token/phone). More secure than just a single password.

GPS services today communicate with satellites to determine a user's exact location outdoors and indoors.

Event viewer should be the first tool to use to figure out what went wrong in a computer crashing. Shows logs of the system, security and application events.

Phishing is common today and shows users fake email/messages to trick them into giving up important credentials. 

Apt, yum and dnf are important package managers in Linux to install packages.

A firewall filters network traffic by a set of rules. Windows Defender is the built-in firewall for Windows hosts.

MDM is Mobile device management which enforces policies, encryption and remote wipe on company machines.

A digitizer is a touch-sensing layer on a screen which converts touch/stylus input into coordinates. Very important.

DHCP stands for Dynamic Host Configuration Protocol. It assigns IP addresses to clients. Uses port 67/68.

Airplane mode disables all radios (WIfI, bluetooth, cellular data) at once. They can be re-enabled.

Principal of least privilege is especially important. It states that you should only give users the minimum access to the system to complete their task, nothing more. Limits problems. 

Order of the Comptia troubleshooting steps (6):
Identify -> Theory -> Test -> plan & implement -> Verify -> Document. 
Documentation is especially important and educating the user afterwards so the same problem does not easily occurr again. Document the incident so that if someone has a similar problem they can refer back to your documentation to solve it, therefore making it more efficient for you and them.

64 bit machines and 32 bit machines have key important differences that should be remembered. 64 bit machines support more RAM, generally more than 4GB. 64 bit machines run 64 bit apps. 32 bit machines are limited to 4GB of RAM and legacy software.

Active Directory Security groups grant permissions to groups, rather than individuals to manage access at scale.

Add users to security groups based on their job roles, then grant those groups access to shared folders, printers, and other resources. When someone's role changes, update their group membership instead of changing permissions on every resource.

Use role-based groups and the principle of least privilege: give each group only the access its members need, and remove access when it is no longer required.

Nested groups let one group be a member of another, making it easier to manage access for teams and departments. Review nesting carefully so users do not receive unintended permissions.

Security groups can be used to assign permissions. Distribution groups are for email distribution lists and are not used to grant access to resources.

Active Directory group scopes include Global (organize users and groups from the same domain), Domain Local (assign permissions to resources in its domain), and Universal (organize membership across domains in a forest).

Redundant power supplies are important in servers. It involves a second PSU in a server that powers on if the first one fails.

Ping is an important command. Tests reachability and latency to a host using ICMP echo requests.

An on path attack is where an attacker alters traffic between two parties.

Brute force and dictionary are two very different types of password attacks. Bruteforce is slower and less reliable because is uses every single password available while dictionary tries likely passwords from a list.

Virtual desktop infrastructure hosts user desktops as VMs in a data center or cloud which can be accessed remotely.

Safe mode boots Windows with minimal drivers/services to troubleshoot driver and startup problems.

A DNS record CNAME is an alias pointing one hostname to another hostname.

Isolating malware helps other parts of the system not get infected so during cleanup there are no additional problems being created.

Full / incrimental / differential backup are important concepts when backing up a computer.

A full backup backs everything up on the computer. A incrimental means everything is backed up since the last backup. Differential means everything is backed up since only the last FULL backup. The differential backup type is the slowest, while incrimental is the fastest.

Cloud elasticity refers to being able to constantly scale up/ scale down resources depending on the demand. This is paired with a pay as you use model.


