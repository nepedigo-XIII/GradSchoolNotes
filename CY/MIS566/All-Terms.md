# Digital Forensics Study Guide

------------------------------------------------------------------------

# Chapter 1 -- Foundations of Digital Forensics

## What is Digital / Computer Forensics?

Digital forensics (also called computer forensics) is the application of
scientific investigative techniques to identify, preserve, analyze, and
present digital evidence. The goal is to determine what occurred on a
digital system while ensuring the evidence remains legally admissible in
court.

Digital forensics involves the systematic examination of computers,
storage devices, networks, and other digital systems in order to uncover
evidence related to criminal activity, policy violations, or civil
disputes.

Key objectives include:

-   Preserving digital evidence without altering it
-   Recovering deleted, hidden, or encrypted data
-   Analyzing system artifacts to reconstruct events
-   Presenting findings clearly for investigators, attorneys, or courts

Digital forensics is used in cases such as fraud, cybercrime,
intellectual property theft, insider threats, harassment, and data
breaches.

------------------------------------------------------------------------

## Seven Domains of Typical IT Infrastructure

A typical enterprise IT environment can be divided into seven major
domains. Understanding these domains helps investigators identify
potential evidence locations.

1.  **User Domain**
    -   Individuals who interact with systems and data.
    -   Users often create artifacts such as documents, browsing
        history, and login records.
2.  **Workstation Domain**
    -   Desktop and laptop computers used by individuals.
    -   Common forensic artifacts include local files, logs, browser
        history, and installed software.
3.  **LAN Domain**
    -   Internal local area networks connecting systems within an
        organization.
    -   Switch logs, network monitoring tools, and internal traffic may
        provide evidence.
4.  **LAN-to-WAN Domain**
    -   Boundary between internal networks and external networks.
    -   Includes firewalls, gateways, and intrusion detection systems.
5.  **WAN Domain**
    -   Wide Area Network connections, typically the internet.
    -   Investigations may involve ISPs, routing data, and external
        communications.
6.  **Remote Access Domain**
    -   Systems that allow remote connections such as VPN services.
    -   Logs may show remote access attempts or unauthorized
        connections.
7.  **System/Application Domain**
    -   Servers and applications used to store and process
        organizational data.
    -   Includes databases, authentication servers, and application
        logs.

------------------------------------------------------------------------

## Scientific Knowledge in Digital Forensics

Digital forensics relies heavily on scientific methodology.

Investigators must follow structured processes for:

-   **Collecting evidence**
-   **Analyzing data**
-   **Documenting procedures**
-   **Presenting findings**

This ensures results are reproducible, reliable, and admissible in
court. Investigators must demonstrate that their methods follow accepted
forensic standards.

------------------------------------------------------------------------

## Forensic Expert Reports and Testimony

Digital forensic investigators often serve as expert witnesses.

Responsibilities include:

-   Preparing **technical forensic reports**
-   Explaining investigative methods
-   Presenting evidence clearly for judges and juries
-   Providing expert testimony during trials

Reports must be:

-   Objective
-   Clearly documented
-   Technically accurate
-   Understandable to non-technical audiences

------------------------------------------------------------------------

## Types of Evidence

Courts recognize several types of evidence used during investigations.

### Real Evidence

Physical objects that directly prove a fact.

Examples:

-   Hard drives
-   USB devices
-   Smartphones
-   Servers

### Documentary Evidence

Written or recorded information.

Examples:

-   Log files
-   Emails
-   Documents
-   Chat transcripts

### Testimonial Evidence

Statements made by witnesses under oath.

Examples:

-   Investigator testimony
-   User statements
-   Expert witness explanations

### Demonstrative Evidence

Visual aids used to explain evidence.

Examples:

-   Diagrams
-   Charts
-   Timeline reconstructions
-   Digital recreations

------------------------------------------------------------------------

## Scope-Related Challenges to System Forensics

Digital investigations face several challenges.

### Volume of Data

Modern storage devices can contain terabytes of information.
Investigators must use tools to filter and identify relevant evidence
efficiently.

### Complexity of Computer Systems

Modern systems involve:

-   Multiple operating systems
-   Virtual machines
-   Cloud services
-   Encrypted data

This complexity makes investigations more difficult.

### Size and Character of the Crime Scene

Digital evidence may be distributed across:

-   Multiple computers
-   Networks
-   Cloud environments
-   Mobile devices

### Caseload and Resource Limitations

Investigative teams often face limited:

-   Personnel
-   Storage capacity
-   Time

These constraints require prioritization and efficient workflows.

------------------------------------------------------------------------

## Types of Digital System Forensics Analysis

Digital investigations may focus on several types of data sources.

### Physical Storage Media

Includes:

-   Hard drives
-   Solid-state drives
-   External storage
-   Backup media

Investigators analyze file systems, deleted files, and hidden data.

### Email Forensics

Examines email messages, attachments, and metadata to determine:

-   Sender identity
-   Message authenticity
-   Communication timelines

### Network Forensics

Focuses on network traffic and logs to identify:

-   Intrusions
-   Unauthorized access
-   Data exfiltration

### Internet Forensics

Investigates web-related artifacts such as:

-   Browser history
-   Cached files
-   Cookies
-   Download logs

### Software Forensics

Analyzes installed applications and program behavior.

### Live System Analysis

Involves examining a running system before shutdown in order to capture
volatile data.

### Mobile Device Forensics

Investigates smartphones and tablets to recover:

-   Messages
-   Contacts
-   Photos
-   Application data
-   Location information

------------------------------------------------------------------------

## General Guidelines for Digital Investigations

Investigators must follow strict procedures to preserve evidence.

### Maintain Chain of Custody

Chain of custody documents every person who handled evidence and every
transfer that occurred.

### Do Not Touch the Suspect Drive

Investigators should not directly examine original evidence. Instead
they create forensic images and analyze the copies.

### Create a Document Trail

Every step must be documented including:

-   Tools used
-   Procedures followed
-   Observations made

### Secure Evidence

Evidence must be protected from:

-   Unauthorized access
-   Environmental damage
-   Tampering

------------------------------------------------------------------------

## Obscured Information vs. Anti-Forensics

### Obscured Information

Data that is hidden but not intentionally concealed to defeat
investigators.

Examples:

-   File compression
-   Encryption used for legitimate purposes

### Anti-Forensics

Techniques intentionally designed to obstruct investigations.

Examples:

-   Data wiping
-   Log manipulation
-   Steganography
-   Encryption used specifically to conceal criminal activity

------------------------------------------------------------------------

## The Daubert Standard

The Daubert Standard is a rule used by U.S. courts to determine whether
expert testimony is scientifically valid.

Judges evaluate whether:

1.  The theory or technique has been tested
2.  It has been peer reviewed
3.  The error rate is known
4.  Standards exist for its use
5.  It is widely accepted within the scientific community

Digital forensic methods must satisfy these criteria to be accepted in
court.

------------------------------------------------------------------------

## Relevant U.S. Laws Affecting Digital Forensics

Several laws govern how investigators collect digital evidence.

Examples include:

-   Computer Fraud and Abuse Act (CFAA)
-   Electronic Communications Privacy Act (ECPA)
-   Stored Communications Act
-   USA PATRIOT Act
-   Digital Millennium Copyright Act (DMCA)

Investigators must ensure evidence collection complies with legal
requirements such as search warrants and privacy protections.

------------------------------------------------------------------------

# Chapter 2 -- Computer Crime and Password Recovery

## Ophcrack and Linux Bootable CD

Ophcrack is a password recovery tool used to crack Windows passwords
using rainbow tables.

Investigators commonly run Ophcrack from a **bootable Linux CD or USB
drive** to avoid modifying the suspect system. Booting from external
media allows the examiner to access password hashes stored in the
Windows Security Account Manager (SAM) database.

Advantages include:

-   No installation required on the suspect system
-   Reduced risk of altering evidence
-   Ability to bypass system login

------------------------------------------------------------------------

## Types of Common Computer Crimes

Computer crimes can involve systems as the target or as the tool used to
commit the crime.

Common categories include:

-   Hacking and unauthorized access
-   Identity theft
-   Online fraud and financial scams
-   Intellectual property theft
-   Distribution of illegal content
-   Cyberstalking and harassment
-   Malware distribution

Digital forensic investigators analyze systems to identify evidence
supporting these crimes.

------------------------------------------------------------------------

## Non-Access Crimes

Non-access crimes involve computers but do not necessarily require
unauthorized system entry.

Examples include:

-   Software piracy
-   Intellectual property violations
-   Online harassment
-   Cyberbullying
-   Fraud conducted using legitimate access

Even though systems are accessed legally, digital evidence is still
required to demonstrate criminal activity.

------------------------------------------------------------------------

# Chapter 3 -- Digital Forensic Methodology

## Digital Forensics Methodology

Digital forensic methodology is the structured process used to conduct
investigations.

Typical phases include:

1.  Identification of potential evidence
2.  Preservation of evidence
3.  Collection and imaging of storage media
4.  Examination and analysis
5.  Documentation and reporting
6.  Presentation of findings

Following a structured methodology ensures reliability and legal
admissibility.

------------------------------------------------------------------------

## Assessing Order of Information Volatility

Digital evidence must be collected based on how quickly it may
disappear.

The order of volatility prioritizes the collection of the most fragile
data first.

Typical order:

1.  CPU registers and cache
2.  RAM memory
3.  Network connections
4.  Running processes
5.  Temporary files
6.  Disk storage
7.  Archival backups

Failure to collect volatile data quickly may result in permanent loss.

------------------------------------------------------------------------

## Formal Forensic Approaches

Several organizations have developed standardized frameworks for digital
investigations.

### DoD Cyber Crime Center (DC3)

Provides forensic standards and training for U.S. Department of Defense
investigations.

### Digital Forensic Research Workshop (DFRWS)

Developed one of the earliest structured forensic frameworks
emphasizing:

-   Identification
-   Preservation
-   Collection
-   Examination
-   Analysis
-   Presentation

### Scientific Working Group on Digital Evidence (SWGDE)

Creates guidelines and best practices used by law enforcement agencies.

### Purdue Event-Based Digital Forensic Investigation Framework

Focuses on reconstructing incidents based on event timelines and system
activity.

------------------------------------------------------------------------

## Evidence-Gathering Measures

Effective evidence collection requires adherence to strict principles.

Key guidelines:

-   Avoid altering the evidence
-   Determine when evidence was created or modified
-   Trust physical evidence over assumptions
-   Search entire devices for hidden artifacts
-   Present evidence clearly and professionally

------------------------------------------------------------------------

## How to Set Up a Forensic Lab

### Equipment

A digital forensic lab must include:

-   Adequate forensic workstations
-   Large storage capacity for disk images
-   Redundant storage systems such as RAID 5
-   Systems capable of connecting to many drive types
-   Power connectors and adapters for smartphones, laptops, and other
    devices

### Security

Forensic labs must maintain strict security controls.

Requirements include:

-   No internet access on examination machines
-   Separate network for investigative systems
-   Shielding from electromagnetic interference
-   Controlled physical access to the lab
-   Secured windows and doors

These precautions prevent evidence contamination and unauthorized
access.

------------------------------------------------------------------------

## Common Forensic Software Programs

Several tools are widely used in digital investigations.

-   **EnCase** -- commercial forensic analysis platform
-   **Forensic Toolkit (FTK)** -- powerful indexing and analysis
    software
-   **OSForensics** -- investigative software for analyzing disk images
-   **Helix** -- forensic Linux distribution
-   **Kali Linux** -- penetration testing and forensic toolkit
-   **AnaDisk** -- disk analysis utility
-   **CopyQM Plus** -- disk duplication tool
-   **The Sleuth Kit** -- open-source forensic toolkit
-   **Disk Investigator** -- tool for examining disk contents

These tools assist investigators with imaging, file recovery, artifact
analysis, and reporting.

------------------------------------------------------------------------

# Chapter 4 -- Evidence Collection and System Imaging

## Steps Before Shutting Down a Computer

When encountering a running system, investigators should collect
volatile information before shutting it down.

Important actions:

-   Check running processes using Task Manager (Windows)
-   Photograph the screen to document system activity
-   Capture network connections
-   Document logged-in users and open files

These steps preserve evidence that would disappear after shutdown.

------------------------------------------------------------------------

## Network and System Commands

Several command-line utilities help capture live system data.

### netstat

Displays active network connections and listening ports.

### net sessions

Shows active sessions connected to the system.

### openfiles

Displays files currently opened by users or applications.

These commands help identify unauthorized access or suspicious activity.

------------------------------------------------------------------------

## Preparing the System for Evidence Collection

### For Suspect Computers

-   Remove internal drives
-   Label each drive carefully
-   Prepare evidence documentation

### For Mobile Devices

-   Remove the SIM card if necessary
-   Use docking systems or forensic extraction tools when possible

### For All Seized Devices

Investigators must:

-   Create evidence forms
-   Maintain chain of custody documentation

------------------------------------------------------------------------

## Documenting Hardware Before Dismantling

Before disassembling a computer:

-   Photograph the system from multiple angles
-   Label cables and connections
-   Record BIOS or UEFI settings
-   Document system date and time

These records help reconstruct the system configuration later.

------------------------------------------------------------------------

## Mathematically Authenticating Data

Forensic imaging requires verification that copies are identical to the
original data.

Process:

1.  Create a forensic image of the storage device
2.  Generate a cryptographic hash of the original drive
3.  Generate a hash of the image copy
4.  Compare both values

If the hashes match exactly, the data is verified as unchanged.

Common hashing algorithms include:

-   MD5
-   SHA‑1
-   SHA‑256

------------------------------------------------------------------------

## Examples of Volatile Data

Volatile data is temporary information stored in memory or active
processes.

Examples include:

-   RAM contents
-   Swap files
-   Active network connections
-   Running processes
-   Open files
-   Clipboard contents
-   System logs

This information disappears once the system is powered down.

------------------------------------------------------------------------

## Storage Formats

Digital evidence may be stored on many types of media.

### Magnetic Media

Traditional spinning hard drives that store data using magnetic
patterns.

### Solid-State Drives (SSD)

Use flash memory instead of moving parts. Data recovery can be more
difficult due to wear-leveling and TRIM operations.

### Digital Audio Tape (DAT)

Tape-based backup storage previously used in enterprise environments.

### Digital Linear Tape (DLT) and Super DLT

High-capacity tape storage used for large-scale backups.

### Optical Media

Includes CDs, DVDs, and Blu-ray discs.

### USB Storage

Portable flash drives commonly used for data transfer.

------------------------------------------------------------------------

## RAID Storage Types

RAID (Redundant Array of Independent Disks) combines multiple drives to
improve performance or reliability.

Common RAID configurations:

-   **RAID 0**: striping for performance but no redundancy
-   **RAID 1**: mirroring for redundancy
-   **RAID 5**: striping with distributed parity
-   **RAID 6**: similar to RAID 5 but with additional parity
    protection
-   **RAID 10**: combination of mirroring and striping

Investigators must understand RAID configurations to reconstruct data
properly during forensic imaging.

------------------------------------------------------------------------
# Chapter 5: Steganography, Cryptography, Encryption, Hashing, and Digital Signatures

## Steganography

Steganography is the practice of hiding information inside other data so
that the existence of the hidden information is concealed. Unlike
encryption, which obscures the content of a message, steganography hides
the presence of the message itself.

Common steganography mediums include:

### Image Steganography

Data is hidden within image files by modifying pixel values in a way
that is imperceptible to the human eye. A common technique is **Least
Significant Bit (LSB) substitution**, where the smallest bit of a pixel
value is altered to encode data.

### Audio Steganography

Hidden information is embedded within audio files. Methods include: -
LSB encoding in sound samples - Phase coding - Spread spectrum encoding

### Video Steganography

Video combines image frames and audio tracks, offering multiple
locations for hidden data. Investigators may analyze frame anomalies or
embedded metadata.

### Text Steganography

Text steganography hides messages using formatting changes or linguistic
tricks such as: - Extra spaces - Hidden characters - Word pattern
manipulation

Forensic investigators search for statistical anomalies, unusual file
sizes, or modified metadata to detect steganography.

------------------------------------------------------------------------

## Cryptography

Cryptography is the science of securing communication by converting
readable information (**plaintext**) into an unreadable format
(**ciphertext**). It ensures:

-   Confidentiality
-   Integrity
-   Authentication
-   Non‑repudiation

------------------------------------------------------------------------

## Encryption

Encryption is the process of transforming plaintext into ciphertext
using an algorithm and a key. Decryption reverses this process.

Two major categories exist.

### Symmetric Encryption

-   Uses **one shared key** for both encryption and decryption.
-   Faster and computationally efficient.
-   Requires secure key exchange.

Examples: - DES - AES - 3DES

### Asymmetric Encryption

Uses **two mathematically related keys**:

-   Public key (shared openly)
-   Private key (kept secret)

Used for: - Secure key exchange - Digital signatures - Authentication

Examples: - RSA - Diffie‑Hellman

------------------------------------------------------------------------

## Data Encryption Standard (DES)

DES is a symmetric encryption algorithm developed in the 1970s.

Characteristics: - 56‑bit key - Block cipher - Processes 64‑bit blocks

Due to its short key length, DES is now considered insecure because
modern hardware can brute‑force the key.

------------------------------------------------------------------------

## Advanced Encryption Standard (AES)

AES replaced DES as the modern encryption standard.

Key features:

-   Block size: 128 bits
-   Key sizes: 128, 192, or 256 bits
-   Extremely resistant to brute‑force attacks
-   Widely used for government and commercial encryption

AES is currently the dominant encryption standard in most security
systems.

------------------------------------------------------------------------

## Triple DES (3DES)

3DES strengthens DES by applying the algorithm three times.

Process: 1. Encrypt with key 1 2. Decrypt with key 2 3. Encrypt with key
3

Although more secure than DES, it is slower than AES and is gradually
being phased out.

------------------------------------------------------------------------

## RSA Encryption

RSA is a widely used asymmetric encryption algorithm.

It is based on the mathematical difficulty of **factoring large prime
numbers**.

Applications include:

-   Secure communications
-   Digital signatures
-   Key exchange protocols

------------------------------------------------------------------------

## Diffie‑Hellman Key Exchange

Diffie‑Hellman is not an encryption method but a **secure key exchange
protocol**.

It allows two parties to establish a shared secret key over an insecure
channel without transmitting the key itself.

This method is widely used in:

-   HTTPS
-   VPN connections
-   Secure messaging systems

------------------------------------------------------------------------

## Kasiski Examination

The Kasiski Examination is a classical cryptanalysis technique used to
break **polyalphabetic substitution ciphers**, such as the Vigenère
cipher.

It works by: 1. Finding repeated character sequences 2. Measuring
distances between repetitions 3. Inferring likely key lengths

This method was historically important in breaking classical encryption
systems.

------------------------------------------------------------------------

## Cracking Modern Cryptographic Methods

Cryptanalysis attempts to defeat encryption without knowing the key.

Common attack models include:

### Known Plaintext Attack

The attacker has access to both: - plaintext - corresponding ciphertext

This information is used to deduce the encryption key.

### Chosen Plaintext Attack

The attacker can choose plaintext messages and observe their encrypted
versions. This allows deeper analysis of the encryption system.

### Ciphertext‑Only Attack

The attacker has only encrypted messages. Statistical analysis and brute
force methods may be used to attempt decryption.

### Related‑Key Attack

The attacker observes encryptions performed with **different but
mathematically related keys**, allowing weaknesses in the algorithm to
be exploited.

------------------------------------------------------------------------

# Chapter 6: File Systems and Data Recovery

## File Systems Used by Different Operating Systems

### Windows File Systems

Common Windows file systems include:

-   **FAT32** -- older system used in legacy devices
-   **exFAT** -- optimized for flash storage
-   **NTFS** -- modern Windows file system supporting permissions,
    journaling, and large file sizes

NTFS is the most common file system encountered in digital forensics for
modern Windows systems.

### Linux File Systems

Linux commonly uses:

-   **ext2** -- early Linux filesystem
-   **ext3** -- journaling version of ext2
-   **ext4** -- modern Linux filesystem with improved reliability and
    scalability

### macOS File Systems

Apple systems historically used:

-   **HFS+ (Hierarchical File System Plus)**

Modern macOS uses:

-   **APFS (Apple File System)**

APFS supports encryption, snapshots, and fast directory sizing.

------------------------------------------------------------------------

## Common Data Recovery Utilities

Forensic investigators often use specialized tools to recover deleted or
damaged data.

Examples include:

-   Autopsy / Sleuth Kit
-   EnCase
-   FTK (Forensic Toolkit)
-   Recuva
-   TestDisk

These tools allow recovery of deleted files, analysis of disk images,
and reconstruction of file systems.

------------------------------------------------------------------------

## Recovering Files from a Suspect Drive

A typical forensic recovery process may include:

1.  Remove the drive from the suspect system.
2.  Connect the drive to a trusted forensic workstation.
3.  Boot the workstation using a forensic operating environment.
4.  Use write blockers to prevent modification of evidence.
5.  Copy or image the drive contents.

------------------------------------------------------------------------

## If the Drive is Not Recognized

If the system does not recognize the drive:

-   Attempt hardware repair or controller replacement
-   Use specialized forensic recovery hardware
-   Access the raw sectors directly

------------------------------------------------------------------------

## Imaging Drive Content

Forensic imaging creates an **exact bit‑for‑bit copy** of a storage
device.

Benefits:

-   Preserves evidence integrity
-   Allows investigators to analyze copies instead of original media
-   Supports verification using hash values

Common image formats include:

-   RAW
-   E01 (EnCase format)
-   AFF

------------------------------------------------------------------------

## Recovering Data After Logical Damage

Logical damage refers to file system corruption rather than physical
damage.

Recovery methods include:

-   Rebuilding file allocation tables
-   Recovering partition structures
-   Using disk repair utilities

------------------------------------------------------------------------

## File Carving

File carving recovers files by examining raw disk data rather than
relying on the file system.

It identifies file signatures (headers and footers) to reconstruct
files.

Examples:

-   JPEG header: `FFD8`
-   PDF header: `%PDF`

File carving is useful when file system structures are destroyed.

------------------------------------------------------------------------

# Chapter 7: Disaster Recovery and Incident Response

## Disaster Recovery Plans (DRP)

A **Disaster Recovery Plan** outlines procedures to restore IT
infrastructure after catastrophic events such as:

-   cyberattacks
-   natural disasters
-   hardware failures
-   data corruption

The plan focuses primarily on restoring **technology systems and data**.

------------------------------------------------------------------------

## Business Continuity Plan (BCP) vs Disaster Recovery Plan (DRP)

**Business Continuity Plan** Ensures that critical business operations
continue during disruptions.

**Disaster Recovery Plan** Focuses specifically on restoring IT systems
and data after an incident.

In short:

BCP = keeping the business running\
DRP = restoring technical infrastructure

------------------------------------------------------------------------

## Business Impact Analysis (BIA)

A Business Impact Analysis identifies:

-   critical systems
-   operational dependencies
-   financial losses caused by downtime

It helps organizations prioritize recovery strategies.

------------------------------------------------------------------------

## Risk and Loss Metrics

### Recovery Point Objective (RPO)

Maximum acceptable amount of data loss measured in time.

Example: backups every 4 hours → RPO = 4 hours.

### Recovery Time Objective (RTO)

Maximum acceptable downtime before services must be restored.

### Single Loss Expectancy (SLE)

Formula:

SLE = Asset Value × Exposure Factor

### Annualized Loss Expectancy (ALE)

Formula:

ALE = SLE × Annual Rate of Occurrence

These metrics help quantify financial risk.

------------------------------------------------------------------------

## Common Vulnerability Scoring System (CVSS)

CVSS is an industry standard used to rate the severity of security
vulnerabilities.

Scores range from **0 to 10** based on factors including:

-   attack complexity
-   exploitability
-   impact on confidentiality, integrity, and availability

------------------------------------------------------------------------

## DREAD Risk Model

DREAD is another vulnerability rating framework.

It evaluates risk based on five factors:

1.  **Damage Potential** -- severity of impact
2.  **Reproducibility** -- ease of repeating the attack
3.  **Exploitability** -- effort required to launch attack
4.  **Affected Users** -- number of users impacted
5.  **Discoverability** -- likelihood vulnerability will be found

Each factor is rated to determine an overall risk score.

------------------------------------------------------------------------

## Types of Backups

### Full Backup

A full backup copies **all data**.

Advantages: 
- easiest to restore

Disadvantages: 
- time consuming 
- large storage requirements

### Differential Backup

Copies all data changed **since the last full backup**.

Restoration requires: 
- last full backup 
- most recent differential backup

### Incremental Backup

Copies all data changed **since the last backup of any type**.

Advantages: 
- smaller and faster backups

Disadvantages: 
- restoration requires multiple backup sets.

### Hierarchical Storage Management (HSM)

HSM automatically moves older or less frequently accessed data to
cheaper storage tiers.

It effectively creates **continuous backup and archival storage**.

------------------------------------------------------------------------

## Incident Response Process

A structured response process ensures incidents are handled effectively.

### 1. Detection

Identify potential security incidents through:

-   monitoring systems
-   intrusion detection systems
-   user reports

### 2. Containment

Limit the damage by isolating affected systems or networks.

Examples: 
- disconnect compromised machines 
- disable compromised accounts

### 3. Eradication

Remove the root cause of the incident.

Examples: 
- deleting malware 
- patching vulnerabilities

### 4. Recovery

Restore systems and return operations to normal.

Activities include: 
- restoring from backups 
- validating system integrity

### 5. Follow‑Up

After the incident:

-   document lessons learned
-   improve defenses
-   update security policies

This final stage strengthens the organization's future security posture.

---

# Chapter 8: Windows Forensics

## Brief History of Windows

[Windows Development History]('Windows Development History.jpg')

## Questions About Target Windows Version

- Does the Windows version in question support 64-bit processing?
- Does it have a firewall? If so, is the firewall automatically on?
- Does the version of Windows support the Encrypted File System (EFS), which allows the user to encrypt specific files and folders?

## Windows Boot Process

### 1. Power-On Self-Test (POST)
- System firmware (**BIOS** or **UEFI**) initializes hardware.
- Performs diagnostic checks on CPU, RAM, storage, and peripherals.
- If successful, firmware locates a bootable device using the configured boot order.

**BIOS systems**
- Reads the **Master Boot Record (MBR)** from the disk.
- Transfers execution to the bootloader.

### 2. Windows Boot Manager / Loader
- **Windows Boot Manager (`bootmgr`)** loads.
- Loads NTLDR
- Determines which operating system to start, 32 or 64 bit.

### 3. Boot Files

- Min. Drivers
- boot.ini
- NTOSKRNL (Windows kernel)
- hal.dll (hardware abstraction layer)
- Windows Registry

### 4. Kernel Initialization
- Windows kernel initializes memory management, process scheduling, and device drivers.
- Core system components are started.

### 5. Win32 Subsystems
- **`smss.exe`** starts system sessions.
- Initializes paging files and system environment.

Processes launched:
- **`csrss.exe`** – Client/Server Runtime Subsystem  
- **`wininit.exe`** – Windows initialization process  
- **`services.exe`** – Service Control Manager  
- **`lsass.exe`** – Local Security Authority  
- **`winlogon.exe`** starts.
- Displays the Windows login screen.
- User authentication occurs.

------------------------------------------------------------------------

## Important Files

- **ntdetect.com**  
  Legacy component used in older Windows versions (NT-based systems). Detects basic hardware during early boot and passes this information to the Windows loader.

- **ntbootdd.sys**  
  A boot-time device driver used when Windows must access storage controllers that are not directly supported by the system firmware (commonly seen with certain SCSI controllers).

- **ntoskrnl.exe**  
  The Windows **kernel**. Responsible for core operating system functions including memory management, process scheduling, hardware interaction, and system security enforcement.

- **hal.dll**  
  The **Hardware Abstraction Layer (HAL)**. Provides a standardized interface between the Windows kernel and underlying hardware so the OS can run on different hardware architectures without modification.

- **smss.exe**  
  The **Session Manager Subsystem**. First user-mode process started by the kernel. Initializes system sessions, creates environment variables, and launches essential system processes.

- **winlogon.exe**  
  Manages the **Windows logon process**. Handles user authentication, secure attention sequence (Ctrl+Alt+Delete), and starts the user shell after successful login.

- **lsass.exe**  
  The **Local Security Authority Subsystem Service**. Enforces security policies, manages user authentication, and handles password verification and security tokens.

- **explorer.exe**  
  The **Windows shell**. Provides the graphical user interface including the desktop, taskbar, Start menu, and file browsing functionality.

- **csrss.exe**  
  The **Client/Server Runtime Subsystem**. Handles essential Windows subsystem operations such as console windows, thread creation, and portions of the Win32 environment.

------------------------------------------------------------------------

## Important Functions and Utils

- **pslist**  
  Command-line utility from the Sysinternals suite used to display information about running processes, including process ID (PID), memory usage, CPU time, and thread counts.

- **psinfo**  
  Sysinternals tool that provides detailed system information such as installed Windows version, system uptime, processor type, memory configuration, and installed hotfixes.

- **listdlls**  
  Utility that lists all **DLL files loaded by running processes**. Often used in troubleshooting or digital forensics to identify injected libraries or suspicious modules.

- **psloggedon**  
  Sysinternals tool that identifies **which users are currently logged onto a system**, both locally and through network sessions.

- **netstat**  
  Built-in Windows command-line tool that displays **active network connections, listening ports, routing tables, and associated processes**, commonly used for network diagnostics and security analysis.

------------------------------------------------------------------------

## Windows Swap File

The swap file in Windows is officially known as the page file, and its default file name is `pagefile.sys`.  It is a hidden system file used as virtual memory, allowing Windows to extend physical RAM by temporarily storing inactive data on the hard drive or SSD

------------------------------------------------------------------------

## Volume Shadow Copy

Point in time copy / image of files or entire volumes on the storage media. 

------------------------------------------------------------------------

## Forensicaly Relevant Windows Directories

C:\Windows documents and settings
• Default location to save documents
C:\Users
• User profile information, documents, pictures, and more for all users, not just the one
currently logged on
C:\Program Files
• Programs are installed in subdirectories of this directory
C:\Program Files (x86)
• In 64-bit systems, 32-bit programs are installed here
C:\Users\username\Documents
• Current user’s Documents folder

------------------------------------------------------------------------

## Guide to Windows Registry 

### Index.dat
Index.dat is a hidden database file used by older versions of Microsoft Internet Explorer (up to IE 9) to store browsing history, cache, cookies, and other user activity data.

### Relevant Artifacts

- **USB Info**  
  Registry and system artifacts that record information about **USB devices connected to a system**, including device IDs, manufacturer details, and first/last connection timestamps.

- **Wireless Networks**  
  Artifacts that store **previously connected Wi-Fi networks**, including SSIDs, connection history, and security settings.

- **Tracking Documents**  
  Metadata and system records that reveal **files recently opened or accessed**, often through shortcuts, recent file lists, or application logs.

- **Malware**  
  Evidence of **malicious software execution or persistence**, typically identified through unusual processes, suspicious files, registry changes, or abnormal network activity.

- **Uninstalled Software**  
  Residual registry entries, configuration files, or logs that indicate **programs previously installed but later removed** from the system.

- **Passwords**  
  Stored authentication data found in system components, browsers, credential managers, or memory artifacts that may reveal **saved login credentials**.

- **ShellBag**  
  Windows Registry artifacts that record **folder view settings and directory access history**, allowing investigators to determine which folders a user has browsed.

- **Shimcache (AppCompatCache)**  
  A registry-based cache used by Windows for **application compatibility tracking**. It records executables that have been run or accessed on the system.

- **Amcache**  
  Windows artifact that stores **detailed metadata about executed programs**, including file paths, hashes, and timestamps.

- **Prefetch**  
  Windows performance feature that logs **recently executed programs** to improve startup speed. Useful in forensics for confirming program execution.

- **SRUM (System Resource Usage Monitor)**  
  Database that records **system resource usage**, including application network activity, energy usage, and execution patterns.

- **BAM and DAM**  
  **Background Activity Moderator (BAM)** and **Desktop Activity Moderator (DAM)** track **application execution history and background process activity** for power and resource management.

---

# CH9 + 10 Linux + MacOS Forensics

## Brief Linux History

[Brief History of Linux]('Linux Development History.jpg')

## Important Linux Commands
- **ls**  
  Lists files and directories within the current or specified directory.

- **cp**  
  Copies files or directories from one location to another.

- **mkdir**  
  Creates a new directory.

- **cd**  
  Changes the current working directory.

- **rm**  
  Deletes files or directories.

- **rmdir**  
  Removes an empty directory.

- **mv**  
  Moves or renames files and directories.

- **ps**  
  Displays information about currently running processes.

- **pstree**  
  Shows running processes in a **tree structure**, illustrating parent-child relationships.

- **top**  
  Displays real-time system resource usage, including CPU, memory, and active processes.

- **fsck**  
  Checks and repairs file system errors.

- **fdisk**  
  Utility used to create, delete, and manage disk partitions.

- **mount**  
  Attaches a file system or storage device to the directory tree so it can be accessed.

- **lsof**  
  Lists **open files** and the processes that are using them.

- **lsattr**  
  Displays special file attributes (such as immutable or append-only flags) on Linux file systems.

- **dmesg**  
  Displays messages from the Linux kernel ring buffer. These messages typically include hardware detection, driver initialization, and system boot events. It is commonly used to troubleshoot hardware issues or view kernel-level system logs.

- **grep**  
  Searches for specific patterns of text within files or command output. It supports regular expressions and is commonly used in pipelines to filter results from other commands.

- **history**  
  Displays a list of previously executed commands in the current shell session. This allows users to review, reuse, or rerun earlier commands.

- **pgrep**  
  Searches for running processes by name and returns their process IDs (PIDs). It simplifies locating processes compared to manually searching through full process listings.

- **kill**  
  Sends a signal to a process, usually to terminate it. The most common signal is `SIGTERM`, which requests a graceful shutdown, though stronger signals such as `SIGKILL` can force termination.

- **file**  
  Determines the type of a file by examining its contents rather than relying solely on the file extension. It can identify file formats such as text files, executables, images, and archives.

- **su**  
  Allows a user to switch to another user account within the current terminal session. It is commonly used to temporarily obtain superuser (root) privileges.

- **who**  
  Displays a list of users currently logged into the system, including their login terminals and login times.

- **finger**  
  Provides information about system users, such as their login name, real name, last login time, and sometimes additional profile information if configured.

- **dd**  
  A low-level data copying utility used to copy and convert raw data between files, devices, or partitions. It is frequently used for disk imaging, creating backups, or performing forensic disk acquisition.


## Linux Boot Process

1. **BIOS performs POST**  
The system firmware (**BIOS/UEFI**) performs the **Power-On Self-Test (POST)** to verify that hardware such as the CPU, RAM, and storage devices are functioning. After POST, it searches for a bootable device.

2. **MBR (Master Boot Record)**  
The firmware loads the **bootloader** from the MBR of the selected disk. The bootloader is responsible for loading the Linux kernel.

- **GRUB (Grand Unified Bootloader)** – The most common Linux bootloader; allows selecting between operating systems or kernel versions.  
- **LILO (Linux Loader)** – An older Linux bootloader that loads the kernel directly but lacks the interactive features of GRUB.

3. **Kernel**  
The **Linux kernel** is loaded into memory and begins system initialization.

- **Initializes devices** – Detects and initializes hardware drivers needed for operation.  
- **Real mode to protected mode** – Switches the CPU from basic firmware execution mode to protected mode so the operating system can access full system memory and capabilities.

4. **INIT**  
The first user-space process started by the kernel (**PID 1**). It initializes the system environment and starts background services and system processes. Modern systems often use **systemd** as a replacement for the traditional init system.

5. **Runlevels**  
Define the **operational state of the system**, determining which services start.

Common traditional runlevels:

- **0** – Halt (shutdown)  
- **1** – Single-user mode (maintenance)  
- **3** – Multi-user mode without GUI  
- **5** – Multi-user mode with graphical interface  
- **6** – Reboot

## Common Distros

- Ubuntu
- Red Hat Enterprise Linux (Paid)
- OpenSUSE
- Debian
- Mint
- Fedora
- CentOS

## Linux Log Types

- `/var/log/fail.log`: Failed user logins
- `/var/log/kern.log`: Messages from the operating system’s kernel
- `/var/log/lpr.log`:- Items that have been printed
- `/var/log/mail.*`: Email activity
- `/var/log/mysql.*`: MySQL database server activity
- `/var/log/apache2/*`: Apache web server activity
- `/var/log/lighttpd/*`: Lighttpd web server activity
- `/var/log/apport.log`: Application crashes
- Intrusion detection system logs Suspicious traffic

## Key Linux Directories

- `/root`: Home directory for root user / admin
- `/bin`: Contains program binaries
- `/sbin`: Contains special binaries, not intended for average user(s)
- `/etc`: Contains config files, attractive to hackers
- `/dev`: Contains device files, interfaces for devices. Naming conventions are as follows:
    - `/hd`: Hard Drive
    - `/fd`: Floppy Drive
    - `/cd`: CD
- `/mnt`: Mounted devices, need to mount drives before use. Checking what is here shows whats currently mounted.
- `/boot`: COntains files critical for boot. GRUB looks here, Kernel images often here. 
- `/usr`: Contains subdirectories for each user acount
- `/tmp`: Contains files that are only temporary, can find data on recent activity here. Will be removed on reboot.
- `/var/tmp`: Made available for programs that need temp file space, remains for 30 days.
- `/var/backups`: Contains backup of system files and shadow copies.
- `/var/spool`: Contains print queue, Seth's mortal enemy.
- `/proc`: The /proc directory in Linux is a pseudo-filesystem that provides a dynamic interface to kernel data structures, exposing real-time system and process information.
- `/run`: Volatile runtime data

## tmpfs

Linux file system that only resides in memory, never written to local disk. When unmounted, entire system is wiped. Data here must be captured before shutdow:

`volatility –profile=Linuxthisx86 –f /root/lime-tmpfs linux_tmpfs`
    
## Undeleting Files in Linux

1. **Move the system to single-user mode**  
   Boot or switch the system into single-user (maintenance) mode to minimize disk activity. This reduces the risk of overwritten data on the partition where the deleted file existed.

2. **Search the raw partition for known text**  
   If the deleted file contained known strings or identifiable text, the raw disk device can be searched directly for those patterns.

3. **Use `grep` to scan the partition**  
   The `grep` command can search a raw device for matching text and return the byte offset of matches.

   Example:
   ```bash
   grep -b 'search-text' /dev/partition > file.txt
   ```

------------------------------------------------------------------------

## Brief History of MacOS

[History of MacOS]('MacOS Development History.jpg')

## File Systems

- **Macintosh** : Legacy
- **Hierarchical File System (HFS)**: Macintosh Plus and above
- **HFS +**: Current Mac OS X system after MacOS 8.1

## HFS+ Partition Types
- GUID Partition Table
- Apple Partition Map
- Master Boot Record (MBR)

## Boot Camp Assistant
Supports 1 additional operating system, supports Windows 10. Important to assess in forensics.

## Mac OS Log types

- `var/log/`: General log repo, data on removable media and devices such as serial numbers
- `var/spool/`: Information on printed documents like name and who printed
- `private/var/audit/`: Logs of system audits
- `private/var/VM/`: Contains swap and sleep image files, and important to assess.
- `Library/Receipts/`: Software and system updates 
- `Library/Mobile/`: iCloud sync information
- `/Users/<user>/.bash_history`: Bash shell activities
- `/var/vm/`: Lists of recently opened applications and temporary application data
- `/Users/`: User specific files and preferences
- `/Users/<user>/Library/Preferences`: Maintains preferences of deleted programs

## Important Mac Directories

- The `/Volumes` Directory
The `/Volumes` directory is the mount point where macOS attaches external and additional storage devices. When a disk, USB drive, or network share is mounted, it typically appears as a subdirectory within `/Volumes`. Each mounted volume is represented as its own folder, allowing the system and users to access the contents through the standard file system hierarchy.

- The `/Users` Directory
The `/Users` directory stores the home folders for all user accounts on the system. Each user has a dedicated subdirectory that contains personal files, application settings, documents, downloads, and desktop items. It also includes a `Shared` directory, which allows files to be accessed by multiple user accounts on the same machine.

- The `/Applications` Directory
The `/Applications` directory contains application bundles installed for all users of the system. Most macOS software is installed here and can be launched directly from this location or through Finder and Launchpad. Applications stored here are accessible system-wide, unlike applications placed in a user’s personal `~/Applications` directory.

- The `/Network` Directory
The `/Network` directory provides access to network resources that are available through directory services or network file systems. It can display shared servers, network volumes, or resources discovered through protocols such as NFS or SMB. In many modern macOS setups it is not heavily used by default, but it still serves as a standardized mount location for network-based resources.

- The `/etc` Directory
The `/etc` directory contains important system configuration files used by the operating system and installed services. In macOS, `/etc` is largely a compatibility layer that points to configuration data stored elsewhere (often within `/private/etc`). Files located here may control network settings, hostnames, service configurations, and other low-level system parameters.

- The `/Library/Preferences/SystemConfiguration/com.apple.preferences.plist` File
The `com.apple.preferences.plist` file located within `/Library/Preferences/SystemConfiguration/` stores system-level configuration settings used by macOS. Property list (`.plist`) files are structured data files that store application or system preferences in key-value format. This particular file may contain configuration data that influences system behavior, network settings, or global preference values used by macOS services.

## Analysis Steps and Target Disk Mode
Create a sound copy of disk contents,  `dd` and `netcat`. Be sure to begin in Target Disk Mode.

## Undeleting in Mac OS

- Similar to Windows, when file is deleted, references to file are gone and clusters might be used and overwritten
- Even if data is overwritten, data might exist in unallocated space and in index nodes
- Deleted files moved to the Trash folder, similar to Recycle Bin in Windows
- Mac OS Trash folder is .Trash, a hidden folder on the root directory of file system

---

# CH 11 Email Forensics

## Email Process Overview

1. Sender uses a mail client to send a message
2. Message travels to multiple mail servers
    - Each mail server sends the message closer to its destination
3. Destination mail server stores the message
4. Receiver uses a mail client to retreive the message from mail server

## Email Contents

Emails can reveal:

- Messages relevant to the investigation
- Email addresses related to the investigation
- Sender and recipient info
- Data on anyone copied on the email
- Email content
- IPs
- Dates and times
- User info
- Attachments
- Passwords
- Application logs


## Email Protocols

-SMTP
-POP3
-IMAP

## Potentially Hazardous Emails

- Spoofing: Email appears to come from someone or someplace other than the real sender or location. First machine to receive spoofed message records machine’s real IP address. Header contains both the faked IP and the real IP address

- Anon. Remail: Anonymizer strips identifying information before forwarding it with the
anonymous computer’s IP address. To find out who sent remailed email, examine logs maintained by remailer or anonymizer companies. Many websites let someone send an email and choose any “From” address

- `Valid` Email:  May appear legitimate, contains suspicious content and potentially dangerous URLs.

## RFC 2822
Standardized format for emails and headers, uniform regardless of OS. Header records journey of email through each server. 

Header must include:
- `FROM` email address, optionally name field 
- `DATE` field

Header should include:
- `Message-ID` auto generated field
- `In-Reply-TO` id field

## RFC 3864

RFC 3864 defines standard email header fields and conventions for Internet messages, specifying how mail clients and servers handle routing, threading, and metadata. Key headers include:

- **To**  
  The primary recipient(s) of the email. This field contains one or more email addresses to which the message is directed.

- **Subject**  
  A brief summary or title of the email’s content. It helps recipients quickly identify the purpose or topic of the message.

- **Cc / Bcc**  
  - **Cc (Carbon Copy):** Recipients who receive a copy of the email, visible to all other recipients.  
  - **Bcc (Blind Carbon Copy):** Recipients who receive a copy without other recipients seeing their addresses.

- **Content-Type**  
  Specifies the media type of the email body (e.g., `text/plain`, `text/html`, `multipart/alternative`) and character encoding, allowing clients to render messages correctly.

- **Precedence**  
  Used to indicate the importance or handling of the message, often set to values like `bulk`, `list`, or `normal` to guide automated processing.

- **Received**  
  Contains trace information of the message as it passes through mail servers. Each mail server adds a new `Received` line, creating a path for debugging or auditing message delivery.

- **References**  
  Lists message IDs of previous emails in a thread, enabling proper conversation threading in email clients.

- **Reply-To**  
  Specifies an alternate email address for responses, overriding the `From` field if present.

- **Sender**  
  Indicates the actual sender of the message, which may differ from the `From` field if the message is sent on behalf of someone else.


## Viewing Headers

1. Select `inbox` from left menu
2. Right click the message you wish to view and select `View Message Source`

On Mac
2. `View` of selected message
3. Select `Message`
4. Select `Long Headers`


## Important Email Files

- **`.pst` (Personal Storage Table)**  
  A file format used by Microsoft Outlook to store copies of emails, calendar events, contacts, and other mailbox items locally. `.pst` files are typically used for personal email accounts and can be archived or backed up.

- **`.ost` (Offline Storage Table)**  
  An Outlook file that allows users to work offline with an Exchange or Microsoft 365 mailbox. Changes made offline are synchronized with the server when a connection is re-established.

- **`.mbx / .dbx`**  
  - **`.mbx`**: A mailbox file format used by older Unix-based or legacy email clients (e.g., early versions of macOS Mail) to store emails in a single text-based file.  
  - **`.dbx`**: Used by Microsoft Outlook Express to store email folders. Each `.dbx` file represents a single folder such as Inbox, Sent Items, or Drafts.

- **`.emi` (Eudora Mail Index)**  
  A file format used by the Eudora email client to index and manage messages stored on disk. It works alongside message storage files to enable fast searching and retrieval.


## Relevant Email Laws

- **4A**  
  Refers to the Fourth Amendment of the U.S. Constitution, which protects against unreasonable searches and seizures. In the context of email, it establishes legal boundaries for government access to private electronic communications without a warrant.

- **ECPA (Electronic Communications Privacy Act, 1986)**  
  Protects electronic communications while in transit and in storage. It regulates government access to emails, phone calls, and other digital communications, requiring warrants or court orders for certain types of interception.

- **CAN-SPAM Act (Controlling the Assault of Non-Solicited Pornography And Marketing, 2003)**  
  Regulates commercial email messages in the U.S., establishing requirements for sender identification, opt-out mechanisms, and prohibitions against deceptive subject lines or headers.

- **18 USC 2252B**  
  U.S. federal law criminalizing the distribution, receipt, or possession of child pornography via electronic means, including email. It provides specific provisions for investigating digital communications in such cases.

- **CALEA (Communications Assistance for Law Enforcement Act, 1994)**  
  Requires telecommunications providers to design systems that allow law enforcement to conduct authorized electronic surveillance, including access to email transmissions, while maintaining network integrity.

- **FISA (Foreign Intelligence Surveillance Act, 1978)**  
  Governs surveillance of foreign intelligence targets in the U.S., including email and electronic communications. Provides a legal framework for monitoring non-U.S. persons while protecting U.S. citizens’ rights.

- **Patriot Act (Uniting and Strengthening America by Providing Appropriate Tools Required to Intercept and Obstruct Terrorism, 2001)**  
  Expanded the government’s ability to access electronic communications, including emails, for counterterrorism purposes. Includes provisions for wiretaps, records access, and enhanced investigative powers.