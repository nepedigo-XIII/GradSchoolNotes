# Digital Forensics Study Guide

------------------------------------------------------------------------

# Ch1 -- Foundations of Digital Forensics

## What is Digital Forensics?

Digital forensics is the application of scientific methods to identify,
collect, preserve, analyze, and present digital evidence in a legally
acceptable manner.

Digital forensics differs from traditional forensic science because:

-   Evidence exists in electronic form
-   Evidence is volatile and easily altered
-   Investigators must maintain strict evidence integrity
-   Analysis requires understanding of computing systems

Investigators must also be familiar with:

-   Computer hardware (CPU, RAM, storage devices)
-   Software and operating systems
-   Networking fundamentals

### Operating Systems (OS)

An Operating System is the software that manages hardware resources and
provides services for applications.

Common responsibilities include:

-   Memory management
-   Process scheduling
-   File system management
-   Device control

### Core Hardware Components

  Component           Function
  ------------------- ----------------------------------------
  CPU                 Executes instructions
  RAM (Memory)        Temporary storage for running programs
  Storage             Long-term data storage
  Network Interface   Enables communication across networks

------------------------------------------------------------------------

## Scientific Approach to Digital Evidence

Digital forensic investigations follow a scientific methodology:

1.  Identification -- locating potential evidence
2.  Collection -- acquiring data without altering it
3.  Preservation -- maintaining integrity of evidence
4.  Analysis -- examining the data
5.  Presentation -- reporting findings in court

### Expert Witness Credibility

Forensic investigators presenting evidence must establish credibility
through:

-   Curriculum Vitae (CV)
-   Professional certifications
-   Education and training
-   Experience
-   Published work

------------------------------------------------------------------------

## The Daubert Standard

The Daubert Standard determines whether scientific evidence is
admissible in U.S. courts.

Courts evaluate:

-   Empirical testing
-   Peer review
-   Known error rates
-   Standards controlling the method
-   General acceptance in the scientific community

------------------------------------------------------------------------

## Types of Evidence

### Real Evidence

Physical evidence directly involved in the case.

Example: - Hard drives - USB devices - Smartphones

### Documentary Evidence

Recorded information.

Example: - Emails - Log files - Documents

### Testimonial Evidence

Statements made by witnesses or experts.

Example: - Expert testimony explaining forensic findings

### Demonstrative Evidence

Materials used to help explain evidence.

Example: - Charts - Diagrams - Data visualizations

------------------------------------------------------------------------

## Scope-Related Challenges

Digital investigations must often operate under constraints such as:

-   Limited time
-   Massive data volumes
-   Legal restrictions

Investigators must narrow the scope of analysis to what is relevant to
the case.

Example: - Focusing only on communications during a specific time
period.

------------------------------------------------------------------------

## Networking Fundamentals

### Ports

A port is a logical communication endpoint used by network services.

Examples:

  Port   Protocol   Service
  ------ ---------- ---------
  80     TCP        HTTP
  443    TCP        HTTPS
  21     TCP        FTP

### MAC Address

A MAC address is a unique hardware identifier assigned to a network
interface card (NIC).

Example format:

00:1A:2B:3C:4D:5E

------------------------------------------------------------------------

## Network Diagnostic Commands

### ipconfig

Displays network configuration including IP address, subnet mask, and
gateway.

### ping

Tests connectivity between systems using ICMP packets.

### tracert

Shows the path packets take to reach a destination.

------------------------------------------------------------------------

## Obscured Data vs Antiforensics

### Obscured Data

Data intentionally hidden but still recoverable.

Examples: - Encryption - Steganography - Hidden partitions

### Antiforensics

Techniques designed to prevent forensic analysis.

Examples: - Secure deletion - Log tampering - Metadata manipulation

------------------------------------------------------------------------

## Relevant Laws

### Patriot Act

Expanded surveillance authority for U.S. investigators after the
September 11 attacks.

### Telecommunications Act (1987)

Regulated telecommunications services and infrastructure.

------------------------------------------------------------------------

## Fourth Amendment (4A)

Protects against unreasonable searches and seizures.

Investigators usually need a search warrant.

### Plain Sight Doctrine

Evidence visible during lawful access may be seized without a warrant.

------------------------------------------------------------------------

# Ch2 -- Cybercrime Techniques

## Identity Theft

Identity theft involves stealing personal data to impersonate another
person.

Uses include:

-   Financial fraud
-   Credit card abuse
-   Tax fraud
-   Account takeover

------------------------------------------------------------------------

## Phishing

A social engineering attack designed to trick victims into revealing
credentials or financial data.

Often uses fake websites or emails.

------------------------------------------------------------------------

## Spyware

Malicious software designed to secretly monitor user activity.

Examples include:

-   Keyloggers
-   Credential harvesters

------------------------------------------------------------------------

## Dumpster Diving

Searching discarded materials for useful information such as:

-   Passwords
-   Printed documents
-   Network diagrams

------------------------------------------------------------------------

## Remote vs Physical Attacks

Most attacks occur remotely.

However, physical access can bypass protections through:

-   Booting from external media
-   Removing storage drives

------------------------------------------------------------------------

## SQL Injection

An attack inserting malicious SQL commands into database queries.

Example:

' OR '1'='1

This may allow attackers to read or modify database data.

------------------------------------------------------------------------

## Cross Site Scripting (XSS)

Injecting malicious scripts into websites viewed by other users.

Possible effects:

-   Cookie theft
-   Session hijacking
-   Malware delivery

------------------------------------------------------------------------

## Windows Password Storage

Windows stores password hashes in the Security Accounts Manager (SAM)
database in the registry.

------------------------------------------------------------------------

## Non‑Access Computer Crimes

Crimes involving computers without unauthorized system entry.

Examples:

-   Software piracy
-   Digital fraud
-   Harassment

------------------------------------------------------------------------

## Logic Bombs

Malicious code that triggers when specific conditions are met.

Triggers may include:

-   Dates
-   Events
-   System states

------------------------------------------------------------------------

# Ch3 -- Evidence Collection

## Order of Volatility

Investigators collect the most volatile data first.

Typical order:

1.  CPU registers and cache
2.  RAM
3.  Network connections
4.  Running processes
5.  Disk storage
6.  Backups and archives

------------------------------------------------------------------------

## Bit‑Level Evidence Collection

A bit‑by‑bit image copies every bit on a disk including:

-   Deleted files
-   Unallocated space
-   File slack

------------------------------------------------------------------------

## File Slack

Unused space between the end of file data and the end of the disk
cluster.

It may contain fragments of previous data.

------------------------------------------------------------------------

## Evidence Handling Tasks

Find -- locate potential evidence\
Preserve -- maintain integrity\
Prepare -- document and organize evidence

------------------------------------------------------------------------

## RAID Storage

  RAID      Purpose
  --------- ----------------------
  RAID 0    Performance
  RAID 1    Mirroring
  RAID 5    Parity
  RAID 10   Mirroring + striping

------------------------------------------------------------------------

## Common Forensic Certifications

Examples:

-   EnCE -- EnCase Certified Examiner
-   GCFA -- GIAC Certified Forensic Analyst
-   CFCE -- Certified Forensic Computer Examiner
-   CHFI -- Computer Hacking Forensic Investigator

------------------------------------------------------------------------

# Ch4 -- Evidence Capture

## Initial System Assessment

Before shutting down a system investigators should:

-   Document running processes
-   Record logged‑in users
-   Identify network connections

------------------------------------------------------------------------

## Network Commands

### netstat

Displays active connections and listening ports.

### net sessions

Displays active sessions connected to the system.

------------------------------------------------------------------------

## BIOS vs UEFI

  BIOS                 UEFI
  -------------------- ----------------------
  Legacy firmware      Modern firmware
  Limited features     Advanced interface
  Small disk support   Supports large disks

------------------------------------------------------------------------

## Storage Media Types

Common digital storage media:

-   Hard Disk Drives (HDD)
-   Solid State Drives (SSD)
-   DAT tapes
-   DLT tapes
-   Optical discs
-   USB drives

------------------------------------------------------------------------

## Acquisition Types

Logical acquisition copies visible files.

Bit‑by‑bit acquisition copies the entire disk including hidden data.

------------------------------------------------------------------------

## dd Imaging Tool

Common Linux forensic imaging tool.

Example:

dd if=/dev/sda of=image.dd bs=4M

------------------------------------------------------------------------

# Ch5 -- Cryptography and Steganography

## Steganography vs Encryption

Encryption hides the meaning of data.

Steganography hides the existence of data.

------------------------------------------------------------------------

## Steganography Elements

Payload -- hidden data\
Carrier -- file containing hidden data\
Channel -- transmission medium

------------------------------------------------------------------------

## LSB Steganography

Least Significant Bit method hides data in the smallest bits of media
files.

Common carriers:

-   Images
-   Audio
-   Video

------------------------------------------------------------------------

## Classical Cryptography

### Substitution Cipher

Characters replaced with others.

### Transposition Cipher

Characters rearranged.

------------------------------------------------------------------------

## Playfair Cipher

Uses a 5×5 letter matrix to encrypt letter pairs.

------------------------------------------------------------------------

## Vigenère Cipher

Polyalphabetic cipher using multiple substitution alphabets.

------------------------------------------------------------------------

## Poly vs. Mono Alphabetic

Mono Alphabetic cyphers make use of a singular set of characters, meaning there is a one to one translation of characters.

Poly Alphabetic cyphers use multiple sets, meaning one character can be translated to plural different characters.


------------------------------------------------------------------------

## Symmetric vs Asymmetric Encryption

  Type         Description
  ------------ --------------------------------
  Symmetric    Same key encrypts and decrypts
  Asymmetric   Uses public/private key pair

------------------------------------------------------------------------

## XOR Encryption

XOR encryption is reversible:

A XOR B XOR B = A

------------------------------------------------------------------------

## Hashing

Hashing converts data into fixed‑length values.

Uses:

-   Password storage
-   Data integrity verification

### Salting

Adding random data before hashing to prevent rainbow table attacks.

------------------------------------------------------------------------

## Cryptanalysis

### Frequency Analysis

Examines letter frequency in ciphertext.

### Kasiski Examination

Used to break Vigenère cipher keys.

------------------------------------------------------------------------

# Ch6 -- File Systems and Data Recovery

## Clusters vs Sectors

  Term      Meaning
  --------- --------------------------------------
  Sector    Smallest physical disk unit
  Cluster   Group of sectors used by file system

------------------------------------------------------------------------

## File Systems

Common systems:

-   FAT32
-   NTFS
-   EXT3
-   EXT4

------------------------------------------------------------------------

## Journaling

Journaling file systems record pending changes to prevent corruption
during crashes.

------------------------------------------------------------------------

## File Tables

File tables track:

-   File locations
-   Metadata
-   Permissions

Example: NTFS Master File Table (MFT).

------------------------------------------------------------------------

## Windows File Deletion

Deleted files often involve:

$R – file contents$I -- metadata about deletion

------------------------------------------------------------------------

## Linux Inodes

EXT3/EXT4 use inodes containing:

-   Metadata
-   Block pointers

If an inode has 0 references the file is considered deleted.

------------------------------------------------------------------------

## Scalpel

Scalpel is a file carving tool used to recover files from raw disk data.

------------------------------------------------------------------------

## Logical Damage Recovery

Tools for repair:

Windows: - chkdsk

Linux: - fsck

------------------------------------------------------------------------

## hiberfil.sys

Stores memory contents when Windows enters hibernation.

------------------------------------------------------------------------

## Zero Knowledge Analysis

Forensic analysis performed without assuming the file system structure.

------------------------------------------------------------------------

## File Carving

Recovery of files by scanning raw disk data for known file signatures.

Also called disk scraping.

------------------------------------------------------------------------

# Ch7 -- Disaster Recovery

## Business Impact Analysis (BIA)

Identifies:

-   Critical systems
-   Maximum tolerable downtime
-   Recovery priorities

Used for disaster recovery planning.

------------------------------------------------------------------------

# Ch8 -- Windows Internals

## Boot Process

POST -- hardware diagnostics during startup.

MBR -- first sector containing boot loader code.

ntoskrnl.exe -- Windows NT kernel managing memory, processes, and
hardware.

------------------------------------------------------------------------

## Windows Registry

Hierarchical database storing configuration information including:

-   User settings
-   Installed software
-   Hardware configuration
-   System policies

------------------------------------------------------------------------

## Registry Hives

  Hive   Description
  ------ -----------------------------
  HKCR   File associations
  HKCU   Current user settings
  HKLM   Local machine configuration
  HKU    User profiles

------------------------------------------------------------------------

## Swap File

pagefile.sys stores memory pages moved from RAM when memory usage is
high.

------------------------------------------------------------------------

## Windows Event Logs

  Log           Purpose
  ------------- ----------------------------------
  System        OS events
  Application   Program events
  Security      Authentication and access events

------------------------------------------------------------------------

## Windows Log Location

C:`\Windows`{=tex}`\System32`{=tex}`\winevt`{=tex}`\Logs`{=tex}

------------------------------------------------------------------------

## index.dat

Legacy file storing Internet browsing history and cache data in older
Windows systems.

------------------------------------------------------------------------

## Copy vs Cut

Copy creates a duplicate file, with the permissions of the target folder.

Cutting a file, if it stayings on the same volume, does not change the permissions to that of the target folder.

---

# Expanded Explanations

The following sections provide additional clarification and context for the concepts outlined in the study guide.

## Digital Forensics
Digital forensics is a specialized discipline within forensic science that focuses on evidence stored or transmitted in digital form. Unlike traditional evidence, digital evidence is highly volatile and can be altered simply by powering a device on or connecting it to a network. Because of this, forensic investigators must follow strict procedures to maintain **evidence integrity** and **chain of custody**. Digital forensics is used in criminal investigations, corporate incident response, civil litigation, and national security cases.

## Operating Systems
Operating systems act as an intermediary layer between hardware and software. They allocate computing resources such as processor time, memory, and storage while providing services that allow applications to function correctly. Examples include Windows, Linux, and macOS. Understanding the OS is critical in forensic investigations because artifacts such as logs, configuration files, and system registries are managed by the OS.

## Scientific Method in Forensics
Digital forensic investigations mirror the traditional scientific method. Hypotheses are formed about what occurred on a system, evidence is collected to test those hypotheses, and conclusions are formed based on verifiable data. Repeatability and documentation are essential so that other investigators or courts can reproduce the findings.

## The Daubert Standard
The Daubert Standard emerged from the U.S. Supreme Court case *Daubert v. Merrell Dow Pharmaceuticals (1993)*. It requires judges to act as “gatekeepers” who evaluate whether scientific testimony is reliable and relevant before allowing it in court. Digital forensic tools and methodologies may be challenged under this standard, making documentation and validation of tools extremely important.

## Networking Fundamentals
Networking knowledge helps investigators understand how systems communicate and how attackers may have accessed a system. Logs often contain IP addresses, port numbers, and timestamps that help reconstruct events across networks.

## Antiforensics
Antiforensic techniques are methods used by attackers to hide their activities or destroy potential evidence. Examples include wiping utilities, log manipulation, timestomping (changing file timestamps), and encryption. Investigators must recognize these techniques to identify when evidence may have been intentionally concealed.

## Identity Theft
Identity theft commonly occurs when attackers gain access to personally identifiable information (PII) such as Social Security numbers, bank credentials, or authentication tokens. These attacks may occur through phishing campaigns, database breaches, or malware infections.

## SQL Injection
SQL injection exploits poorly sanitized input fields in web applications. Attackers insert database commands into user input fields to manipulate backend queries. This can lead to unauthorized data retrieval, modification, or deletion of entire databases.

## Order of Volatility
The order of volatility principle states that investigators should collect the most fragile data first. Data stored in CPU registers and memory disappears once power is lost, while data stored on disks or backups remains available longer.

## Disk Imaging
Bit‑level imaging is critical in forensic analysis because it ensures that investigators obtain an exact duplicate of the original storage device. Imaging tools also compute cryptographic hashes before and after acquisition to verify that the image has not been altered.

## RAID
Redundant Array of Independent Disks (RAID) combines multiple disks into a single logical storage system. RAID configurations improve performance, reliability, or both. Investigators must understand RAID because data may be distributed across multiple disks.

## Steganography
Steganography embeds hidden information within digital files so that the existence of the message is concealed. Images are common carriers because slight pixel modifications are difficult for humans to detect.

## Hashing
Hash functions convert data into fixed‑length values called hashes or digests. Even a small change in input data results in a completely different hash value. Forensic investigators use hashing to verify that evidence has not changed during analysis.

## File Systems
File systems organize how data is stored and retrieved on disks. They define how files are named, how metadata is stored, and how disk space is allocated. Understanding file systems allows investigators to recover deleted files and interpret raw disk structures.

## File Carving
File carving is used when file system metadata is damaged or missing. The technique scans raw disk data for recognizable file headers and footers (known as signatures) to reconstruct files.

## Windows Registry
The Windows Registry is one of the most important forensic artifacts in Windows systems. It stores configuration settings, installed software information, startup programs, and user activity traces.

## Event Logs
Windows event logs record system activity such as login attempts, service failures, and security events. These logs often provide a timeline of events that investigators use to reconstruct incidents.

## Copy vs Cut
Understanding file operations is important in investigations. Copying a file creates a new instance of the file in the destination directory. Cutting (moving) a file within the same filesystem typically only updates directory references rather than duplicating the file's data blocks. This difference can affect timestamps, permissions, and forensic interpretation of file activity.


------------------------------------------------------------------------

## What was the kitty hiding in Lab 3

I'm pretty sure it was a document guide on Tor browser