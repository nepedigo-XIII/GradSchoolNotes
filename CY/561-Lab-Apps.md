# Cybersecurity Study Guide
## Applications & Concepts Overview

## Kleopatra
**Type:** Certificate Manager (GUI for GPG)  
**Purpose:** Encrypt, decrypt, manage keys, and digitally sign data.

**What it Does:**
- Generates public/private key pairs.
- Imports, exports, and revokes keys.
- Encrypts/decrypts files and email using OpenPGP or S/MIME.
- Manages certificate trust levels.

**Why It Matters:**
- Essential tool for learning asymmetric encryption workflows.
- Common in secure communication and file confidentiality.

## EFS (Encrypting File System)
**Type:** Windows file-level encryption  
**Purpose:** Protects individual files/folders on NTFS volumes.

**What it Does:**
- Encrypts files using a user-specific certificate.
- Automatically decrypts for the authorized user during access.
- Supports recovery agents for enterprise environments.

**Why It Matters:**
- Provides granular encryption (not whole-disk like BitLocker).
- Useful for protecting specific sensitive files on a shared system.

**Limitations:**
- Only works on NTFS.
- Not secure if attackers obtain the user password and log in normally.

## BitLocker
**Type:** Full-disk encryption (Microsoft)  
**Purpose:** Protects entire drives, including system drives, from offline access.

**What it Does:**
- Encrypts entire disks using AES (XTS or CBC depending on version).
- Uses TPM chips for secure key storage.
- Supports PINs, USB key unlocks, and network unlocks.

**Why It Matters:**
- Strong defense against device theft or physical compromise.
- Ensures data at rest stays confidential even if the machine is removed.

### BitLocker vs EFS
| Feature | BitLocker | EFS |
|--------|-----------|-----|
| Scope | Entire drive | Individual files |
| Uses TPM? | Yes | No |
| Protects at login? | No | Yes |

## OpenSSL
**Type:** Cryptography toolkit & command-line utility  
**Purpose:** Generates keys, creates CSRs, runs TLS tests, encrypts data.

**What it Does:**
- Generates RSA, ECC, and other key types.
- Creates, signs, and inspects X.509 certificates.
- Runs TLS server connection checks.
- Encrypts/decrypts strings and files.
- Converts certificate formats (PEM, DER, PFX).

**Why It Matters:**
- Industry standard for certificate operations.
- Used by web servers, security engineers, DevOps, and penetration testers.

## John the Ripper
**Type:** Password-cracking tool  
**Purpose:** Audits password strength by attempting to crack hashes.

**What it Does:**
- Cracks hashes using dictionary, brute force, and hybrid attacks.
- Supports NTLM, Linux shadow, ZIP, and many other formats.

**Why It Matters:**
- Critical for penetration testing and red teaming.
- Demonstrates weaknesses in poor password policies.

## ZenMap
**Type:** GUI for Nmap  
**Purpose:** Visual network mapping and port scanning.

**What it Does:**
- Runs Nmap scans with a GUI.
- Saves and compares scans.
- Includes preset scan profiles.
- Visualizes network topology.

**Why It Matters:**
- Useful for learning Nmap.
- Helps identify open ports, services, and attack surfaces.

## PKI Certificates
**Type:** Public Key Infrastructure  
**Purpose:** Authentication, encryption, and digital signatures.

**Key Components:**
- Certificate Authorities (CAs)
- Registration Authorities (RAs)
- Certificates (X.509)
- Revocation methods (CRL, OCSP)

**What PKI Enables:**
- HTTPS/TLS
- Code signing
- Email encryption
- VPN authentication
- Device and user authentication

**Why It Matters:**
- Backbone of secure communication online and in enterprises.
