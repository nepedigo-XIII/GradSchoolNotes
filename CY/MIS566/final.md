# Cybersecurity & Systems Study Guide (Ch. 8--14) --- Updated

------------------------------------------------------------------------

## `**Chapter 8: Windows OS Fundamentals**`

### Core

-   **Core of the OS:** Kernel The kernel is the central component of the operating system that operates at the highest privilege level. It manages hardware resources (CPU, memory, devices), handles process scheduling, enforces security boundaries, and provides an interface between software and hardware through system calls.

-   **Boot Security & Logon Policies:** LSASS (Local Security Authority
    Subsystem Service)  Responsible for enforcing security policies on the system. During boot and login, it:

    -   Authenticates users (verifies credentials)
    -   Generates access tokens that define user permissions
    -   Enforces password policies and account lockout rules
    -   Logs security-related events (e.g., login attempts)

### Virtual Memory

- **Swap/Page File (Windows):**
  - Extends RAM using disk space
  - Stores inactive memory pages
  - Improves multitasking but is slower than RAM

### Login Monitoring

- **Location:** Event Viewer → Windows Logs → Security

- **Key Event IDs:**
  - **4624** — Successful login:    Indicates a user or service has successfully authenticated
  - **4625** — Failed login:    Indicates an unsuccessful authentication attempt (e.g., wrong password, disabled account)



------------------------------------------------------------------------

## `**Chapter 9 - Linux Fundamentals**`

### Boot Process

Linux boot is a staged initialization sequence that transitions the system from firmware control to a fully operational user space environment:

1. **BIOS/UEFI**
   - Performs hardware initialization (POST: Power-On Self Test)
   - Detects bootable devices (SSD, HDD, USB)
   - Loads boot configuration from firmware settings

2. **Bootloader (GRUB)**
   - GRand Unified Bootloader (GRUB) is the most common Linux bootloader
   - Presents OS selection menu (if multiple kernels/OS installed)
   - Loads the selected Linux kernel into memory
   - Passes kernel parameters (e.g., recovery mode, quiet boot)

3. **Kernel Loads**
   - Linux kernel is decompressed and initialized
   - Hardware drivers are loaded (CPU, memory, storage, network)
   - Memory management and process scheduler are activated

4. **Init System (systemd)**
   - First user-space process (PID 1)
   - Responsible for system initialization and service orchestration
   - Mounts filesystems, configures hostname, time, and system state

5. **Services Start**
   - Background daemons and services are launched
   - Examples: networking, logging, SSH server, display manager
   - System reaches target state (multi-user or graphical mode)

---

### Key Concepts

#### Virtual Filesystems

- **`/proc` (Process Information Pseudo-Filesystem)**
  - Not stored on physical disk
  - Fully virtual; generated dynamically by the kernel
  - Provides real-time system and process information
  - Examples:
    - `/proc/cpuinfo` → CPU details
    - `/proc/meminfo` → memory usage
    - `/proc/[pid]/` → process-specific data

---

#### Privilege Escalation

- **`sudo` (SuperUser DO)**
  - Allows permitted users to execute commands with elevated privileges
  - Controlled via `/etc/sudoers` configuration file
  - Provides temporary root-level access without full root login
  - Enhances security by limiting persistent administrative access

---

### File Deletion (Linux & Windows)

File deletion in both Linux and Windows follows a similar logical model rather than immediate physical data removal:

- **Step 1: Reference Removal (Unlinking)**
  - File entry is removed from directory structure
  - Filename no longer points to inode (Linux) or file record (NTFS)

- **Step 2: Metadata Clearance**
  - File system marks inode / file record as free
  - Space is marked as available for reuse

- **Step 3: Data Persistence**
  - Actual data remains on disk temporarily
  - Data is only erased when overwritten by new files

**Implication:**
- Deleted files may be recoverable using forensic tools until overwritten

---

### Shell Types

The shell is the command-line interface used to interact with the Linux operating system:

- **Bash (Bourne Again Shell)**
  - Default shell on most Linux distributions
  - Supports scripting, variables, loops, and conditionals
  - Backward compatible with Bourne shell (sh)

- **Bourne Shell (`sh`)**
  - Original Unix shell
  - Minimal feature set
  - Foundation for many modern shells

- **Zsh (Z Shell)**
  - Advanced shell with enhanced auto-completion
  - Improved scripting features and customization
  - Popular in developer environments

- **Ksh (Korn Shell)**
  - Combines features of Bourne shell and C shell
  - Efficient scripting capabilities
  - Historically used in enterprise Unix systems

------------------------------------------------------------------------

## **Chapter 10 -- macOS & Unix Systems**

### Multiple File References

Unix-like systems (including macOS and Linux) support mechanisms that allow a single file to be referenced in more than one way. This improves flexibility in file organization without duplicating data.

#### Aliases (macOS)
- **Definition:** A macOS-specific file reference that points to another file or folder.
- **Behavior:**
  - Can survive file moves or renames (uses file metadata tracking).
  - Breaks if the original file is deleted and cannot be automatically resolved in all cases.
- **Use case:** Common in Finder for shortcuts to applications, documents, or directories.

#### Hard Links (Linux/macOS)
- **Definition:** A direct reference to the same inode (data structure) as the original file.
- **Behavior:**
  - Both the original file and hard link are identical at the filesystem level.
  - Deleting one does not remove the data as long as at least one hard link remains.
  - Cannot span different filesystems.
- **Limitation:** Typically cannot be used for directories (to prevent filesystem loops).

#### Symbolic Links (Symlinks)
- **Definition:** A special file that stores a path to another file or directory.
- **Behavior:**
  - Functions like a shortcut at the filesystem level.
  - Can cross filesystems.
  - Breaks if the target file is moved or deleted (“dangling link”).
- **Use case:** Common for linking libraries, configuration files, or shared resources.

---

### Log Storage

#### `/var/log` (Linux & macOS)
- **Definition:** Standard directory for system and application log files.
- **Purpose:**
  - Stores records of system events, errors, authentication attempts, and service activity.
- **Examples of logs:**
  - System logs (kernel and OS events)
  - Authentication logs (login attempts, sudo usage)
  - Application-specific logs (web servers, databases)
- **Importance:**
  - Critical for troubleshooting system issues.
  - Frequently used in security auditing and forensic analysis.

------------------------------------------------------------------------

## **Chapter 11 -- Email Forensics**

Email forensics focuses on analyzing email content, metadata, and transmission paths to identify fraud, impersonation, and malicious activity. It is commonly used in cybercrime investigations, incident response, and legal discovery.

---

### Email Spoofing Techniques

Email spoofing refers to falsifying email origin information so the message appears to come from a trusted source.

#### Forged Headers
- Email headers are manually altered or manipulated.
- Attackers change fields such as `From`, `Reply-To`, or `Return-Path`.
- Objective: make the email appear legitimate during casual inspection.

#### Fake Sender Addresses
- The visible sender address is falsified (e.g., display name spoofing).
- Example: “CEO <ceo@company.com>” when the real source is unrelated.
- Often used in phishing and business email compromise (BEC).

#### Domain Impersonation
- Attackers register or use lookalike domains:
  - Example: `micros0ft.com` instead of `microsoft.com`
- May rely on:
  - Character substitution (typosquatting)
  - Subdomain deception (e.g., `login.company.fake-site.com`)

#### Open Relay Abuse
- Exploits misconfigured mail servers that allow unauthenticated email forwarding.
- Allows attackers to:
  - Send spam anonymously
  - Obscure original source IP addresses
- Mostly mitigated in modern systems but still encountered in legacy infrastructure.

---

### Email Analysis

Email analysis involves examining both visible content and hidden metadata to determine authenticity and origin.

#### View Headers ("Show Original" / "View Source")
- Email clients provide full header access:
  - Gmail: *Show Original*
  - Outlook: *View Message Source*
- Headers reveal:
  - Transmission path (Received fields)
  - Sending IP address (in some cases)
  - Authentication results (SPF, DKIM, DMARC)

Key header elements:
- **Received:** chain of servers the email passed through
- **Message-ID:** unique identifier of the email
- **Authentication-Results:** validation of sender legitimacy

---

### Anonymization

Anonymization techniques aim to obscure sender identity and routing information.

#### Header Stripping
- Removal or alteration of identifying metadata.
- Can occur in:
  - Privacy-focused email services
  - Malicious tampering during transit
- Limits forensic traceability when critical headers are removed.

#### Remailers / VPN Usage
- **Remailers:**
  - Systems that forward email while removing sender identity.
  - Often used for privacy or anonymity networks.
- **VPNs:**
  - Mask originating IP address.
  - Makes geolocation and attribution more difficult.

---

### Evidence Collection

Email forensics relies on multiple data sources to reconstruct events.

#### Mail Server Logs
- Record all email transactions:
  - Sender/receiver IP addresses
  - Timestamps
  - Delivery status
- Often the most reliable source for tracing origin.

#### Backups
- Historical snapshots of mailboxes and servers.
- Useful when emails have been deleted or altered.
- Can provide chain-of-custody support in investigations.

#### Metadata Analysis
- Examination of non-visible email data:
  - Header structure
  - Encoding patterns
  - Attachment metadata (file origin, creation timestamps)
- Helps detect manipulation or inconsistencies.

---

### Remote Evidence Acquisition

When local access is insufficient, investigators rely on external data sources.

#### Subpoena ISP or Email Provider
- Legal request to obtain:
  - Account registration data
  - IP login history
  - Stored emails and metadata
- Common in criminal and civil investigations.

#### Retention Policies
- Data availability depends on provider policy:
  - Typically **30–90 days** for detailed logs
  - Some providers retain metadata longer
  - Content retention varies widely based on jurisdiction and service type

---

### Summary
Email forensics combines header analysis, server logs, and legal data acquisition to reconstruct message origin and detect manipulation. Its effectiveness depends heavily on log retention, provider cooperation, and the sophistication of anonymization techniques used.

------------------------------------------------------------------------

## **Chapter 12 -- Mobile Device Forensics**

Mobile device forensics focuses on the acquisition, preservation, and analysis of data from smartphones and tablets. These devices store a high density of personal, location, and application data, making them critical in digital investigations.

---

### Device Identification

Mobile devices can be uniquely identified using multiple hardware and network-based identifiers.

#### IMEI (International Mobile Equipment Identity)
- Unique identifier assigned to the physical device.
- Used by cellular networks to validate and track devices.
- Can be used to blacklist stolen phones.

#### MAC Address
- Hardware address assigned to network interfaces (Wi-Fi, Bluetooth).
- Used for local network identification.
- Can be randomized in modern devices to improve privacy.

#### Serial Number
- Manufacturer-assigned identifier.
- Used for warranty tracking and device inventory.
- Not typically exposed to networks.

#### Phone Number (MSISDN)
- Subscriber-assigned number linked to SIM card.
- Represents the user’s public-facing identity on the cellular network.

#### ICCID (Integrated Circuit Card Identifier)
- Unique identifier for the SIM card itself.
- Used to track SIM ownership and activation history.

---

### Mobile Databases

Mobile operating systems and applications rely heavily on embedded databases for storing structured data.

#### SQLite (Common Standard)
- Lightweight relational database engine.
- Widely used in:
  - Messaging apps
  - Browsers
  - System settings storage
- Stores data in `.db` files located within app directories.

#### App Databases
- Application-specific structured storage.
- May include:
  - Chat histories
  - User credentials (hashed/encrypted)
  - Cached content and metadata

#### System Logs
- Records of system events and app behavior.
- Includes:
  - Crash logs
  - Security events
  - Network activity logs

---

### Mobile Layers (Simplified Architecture)

Mobile systems are typically organized into layered abstractions:

#### 1. Application Layer
- User-facing applications (messaging, browsers, games).
- Handles user interaction and app logic.
- Most forensic evidence originates here.

#### 2. Media Layer
- Manages multimedia processing:
  - Audio
  - Video
  - Image rendering
- Supports APIs used by applications for media handling.

#### 3. Hardware / Touch Layer
- Direct interaction with physical device components:
  - Touchscreen input
  - Sensors (GPS, accelerometer, gyroscope)
  - Hardware drivers
- Bridges software commands with physical device behavior.

---

### Device States (NIST-style Classification)

Mobile device state affects data accessibility during forensic acquisition.

#### On (Active)
- Device fully powered and operational.
- Best state for volatile data acquisition.
- Risk: user interaction may alter evidence.

#### Sleep
- Low-power state preserving RAM.
- Some processes remain active (e.g., notifications, connectivity).

#### Locked / Unlocked
- Security state controlling access to user data.
- Locked devices may still be network-active.

#### Off
- Device powered down.
- Volatile memory lost, but persistent storage remains intact.

#### Hibernation-like States
- Hybrid low-power states used by some systems.
- RAM contents may be partially preserved to storage.
- Important for memory reconstruction efforts.

---

### SIM Card Concepts

SIM cards are critical for subscriber identity and network authentication in cellular systems.

#### Cloning
- Duplication of SIM credentials onto another card.
- Allows unauthorized access to subscriber identity.
- Often illegal and detectable via network anomalies.

#### Spoofing
- Impersonating SIM or device identifiers during network communication.
- May involve manipulation of IMSI/ICCID signals.
- Used in advanced fraud or interception scenarios.

#### Subscriber vs. Roamer Behavior
- **Subscriber:**
  - Registered on home network.
  - Uses standard authentication with home carrier.
- **Roamer:**
  - Connects via foreign networks.
  - Requires inter-carrier authentication and billing coordination.
- Cell tower interaction differs based on roaming status and network agreements.

------------------------------------------------------------------------

## **Chapter 13 -- Networks & Attacks**

This chapter covers how network communication is structured and how common attack types exploit weaknesses in that communication.

---

### Data Units

#### Packets
- Network data is transmitted in **packets**.
- A packet is a small, structured unit containing:
  - Payload (actual data)
  - Header (routing and control information)
- Reasons for packetization:
  - Efficient routing across networks
  - Error detection and retransmission
  - Load balancing across multiple paths

Packets are reassembled at the destination into the original message.

---

### Network Tools

#### Wireshark
- Packet capture and analysis tool.
- Functions:
  - Captures live network traffic
  - Decodes protocols (HTTP, TCP, DNS, etc.)
  - Filters traffic for forensic inspection
- Common use: identifying suspicious or unauthorized network activity.

#### Nmap (Network Mapper)
- Network scanning and discovery tool.
- Functions:
  - Identifies active hosts on a network
  - Detects open ports and services
  - Infers operating systems and service versions
- Common use: reconnaissance in both penetration testing and defense.

#### Netscan (Volatility Framework)
- Memory forensics plugin used to identify:
  - Active network connections
  - Open sockets
  - Associated processes in RAM
- Useful for detecting:
  - Hidden malware communication channels
  - Active connections not visible through standard OS tools

---

### Attack Types

#### SYN Flood
- Exploits the TCP handshake process.
- Mechanism:
  1. Attacker sends many SYN requests.
  2. Server responds with SYN-ACK.
  3. Attacker never completes handshake.
- Result:
  - Server resources are consumed by half-open connections.
  - Legitimate users are blocked.

---

#### Smurf Attack
- ICMP-based amplification attack.
- Mechanism:
  - Attacker sends ICMP echo requests to broadcast address.
  - Spoofs victim’s IP as the source.
  - All hosts respond to the victim.
- Result:
  - Victim is overwhelmed with traffic.

---

#### Fraggle Attack
- Similar to Smurf but uses UDP instead of ICMP.
- Targets UDP services (e.g., echo or chargen).
- Often results in amplified traffic directed at the victim.

---

#### Teardrop Attack
- Exploits IP packet fragmentation.
- Mechanism:
  - Sends overlapping or malformed packet fragments.
  - Target system fails during reassembly.
- Result:
  - System crash or instability (especially in older systems).

---

#### MITM (Man-in-the-Middle)
- Attacker intercepts communication between two parties.
- Capabilities:
  - Eavesdropping on data
  - Modifying transmitted data
  - Injecting malicious content
- Common in unsecured Wi-Fi or compromised routers.

---

#### DoS (Denial of Service)
- Attempts to make a system unavailable.
- Achieved by overwhelming resources (CPU, memory, bandwidth).
- Typically originates from a single source.

---

#### DDoS (Distributed Denial of Service)
- Same goal as DoS but uses multiple systems (botnets).
- Characteristics:
  - High traffic volume from many sources
  - Harder to block due to distributed nature
- Often used for large-scale disruption of services.


------------------------------------------------------------------------

## **Chapter 14 -- Memory & Exploitation (Expanded)**

---

## **Heap vs Stack**

| Feature      | Stack                              | Heap                                  |
|-------------|------------------------------------|----------------------------------------|
| Allocation  | Automatic (compiler-managed)       | Manual (programmer-controlled)        |
| Structure   | LIFO (Last In, First Out)         | Dynamic, unordered allocation         |
| Speed       | Very fast                         | Slower due to management overhead     |
| Size        | Limited (fixed per thread/process) | Large (limited by system memory)      |
| Lifetime    | Until function returns            | Until explicitly freed                |
| Risks       | Stack overflow                    | Memory leaks, fragmentation           |

### Stack Characteristics
- Stores:
  - Local variables
  - Function parameters
  - Return addresses
- Automatically cleaned up when scope ends
- Highly predictable memory behavior
- Common attack target:
  - **Buffer overflow exploits**

### Heap Characteristics
- Used for dynamic allocation (`malloc`, `new`)
- Managed by allocator (not automatic cleanup)
- More flexible but error-prone
- Common issues:
  - dangling pointers
  - double free
  - heap spraying (used in exploitation)

---

## **Memory Issues**

### Segmentation Fault
- Occurs when a program accesses invalid memory
- Typical causes:
  - null pointer dereference
  - buffer overflow
  - accessing freed memory
- OS response:
  - process termination

### Memory Leak
- Memory allocated but never freed
- Leads to:
  - gradual performance degradation
  - system instability over time
- Common in:
  - long-running services
  - poorly managed dynamic allocation

---

## **Tables (Memory & System Management)**

### Hardware-Level Management

#### Page Tables
- Translate **virtual memory → physical memory**
- Managed by the MMU (Memory Management Unit)
- Key concepts:
  - paging
  - page frames
  - address translation

#### Benefits
- Memory isolation between processes
- Enables virtual memory abstraction
- Prevents direct memory collisions

---

### Software-Level Management

#### Process Tables
- Tracks active processes
- Stores:
  - Process ID (PID)
  - state (running, waiting, etc.)
  - memory mappings
  - resource handles

#### File Tables
- Tracks open files per process
- Stores:
  - file descriptors
  - access modes (read/write)
  - file offsets

---

## **Volatility Commands (Memory Forensics)**

Used in memory analysis frameworks (e.g., Volatility)

- `pslist`
  - Lists active processes
  - Helps detect hidden or malicious processes

- `netscan`
  - Displays active network connections
  - Identifies suspicious outbound communication

- `dlllist`
  - Shows DLLs loaded by processes
  - Useful for detecting:
    - injected libraries
    - malicious modules

### Forensic Use Case
- Detect:
  - rootkits hiding processes
  - malware persistence
  - injection-based attacks

---

## **Malware Types**

### Trojan
- Disguised as legitimate software
- Requires user execution
- Common goal: credential theft or backdoor access

### Worm
- Self-replicating malware
- Spreads across networks automatically
- Does not require user interaction

### Logic Bomb
- Triggered by a condition (time/event)
- Dormant until activation
- Example: deletes files on a specific date

### Virus
- Attaches to legitimate files
- Requires execution of host file
- Spreads via file sharing or execution

### Rootkit
- Designed for stealth and persistence
- Hides processes, files, or system activity
- Often operates at kernel level

---

## **DLL Injection**

### Concept
- Technique where malicious code is inserted into a legitimate process

### Mechanism
1. Target process is opened
2. Memory is allocated inside process space
3. Malicious DLL is written into memory
4. Remote thread is created to execute it

### Objectives
- Privilege escalation
- Stealth execution
- Evading detection tools

### Common Targets
- system processes (e.g., explorer.exe)
- security software processes

---

## **Sockets**

### Definition
- A socket is a communication endpoint defined by:
  - IP address
  - Port number

### Structure
- Example:
  - `192.168.1.10:443`

### Types
- **TCP sockets**
  - connection-oriented
  - reliable transmission

- **UDP sockets**
  - connectionless
  - faster but less reliable

### Security Relevance
- Used in:
  - command-and-control (C2) channels
  - remote shells
  - data exfiltration


## **Process Directory**

-   `/proc` is virtual (not stored on disk)

