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

Advantages: - easiest to restore

Disadvantages: - time consuming - large storage requirements

### Differential Backup

Copies all data changed **since the last full backup**.

Restoration requires: - last full backup - most recent differential
backup

### Incremental Backup

Copies all data changed **since the last backup of any type**.

Advantages: - smaller and faster backups

Disadvantages: - restoration requires multiple backup sets.

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

Examples: - disconnect compromised machines - disable compromised
accounts

### 3. Eradication

Remove the root cause of the incident.

Examples: - deleting malware - patching vulnerabilities

### 4. Recovery

Restore systems and return operations to normal.

Activities include: - restoring from backups - validating system
integrity

### 5. Follow‑Up

After the incident:

-   document lessons learned
-   improve defenses
-   update security policies

This final stage strengthens the organization's future security posture.

