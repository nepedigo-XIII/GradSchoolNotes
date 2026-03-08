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
