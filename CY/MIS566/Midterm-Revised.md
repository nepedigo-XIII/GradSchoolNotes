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
