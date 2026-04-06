# Lesson: Computer Hardware Components

## Introduction
To secure a system, you must first understand the physical layer. Cybersecurity isn't just about code; it's about the hardware that executes that code. If an attacker has physical access to hardware, the software security often becomes irrelevant.

## Core Hardware Components

### 1. The Central Processing Unit (CPU)
- **What it is:** The "brain" of the computer.
- **Function:** Executes instructions (Fetch-Decode-Execute cycle).
- **Cybersecurity Relevance:** 
    - **Side-Channel Attacks:** Attackers can sometimes infer data by measuring CPU power consumption or timing (e.g., Spectre and Meltdown vulnerabilities).
    - **Overclocking:** Can lead to system instability or overheating, potentially causing a Denial of Service (DoS) at a physical level.

### 2. Random Access Memory (RAM)
- **What it is:** Volatile short-term memory.
- **Function:** Stores data that the CPU needs immediately.
- **Cybersecurity Relevance:** 
    - **Cold Boot Attacks:** Data remains in RAM for a short period after power-off; attackers can freeze the RAM to extract encryption keys.
    - **Buffer Overflows:** A classic software vulnerability where data overflows its allocated space in RAM, allowing attackers to execute malicious code.

### 3. Storage (HDD, SSD, NVMe)
- **What it is:** Non-volatile long-term memory.
- **Function:** Persistently stores the OS, applications, and user data.
- **Cybersecurity Relevance:** 
    - **Data Remanence:** Deleted files aren't "gone"; they are marked as available space. Forensics tools can recover this data.
    - **Encryption:** Full Disk Encryption (FDE) is critical to protect data if the physical drive is stolen.

### 4. The Motherboard
- **What it is:** The main circuit board that connects all components.
- **Function:** Provides communication paths (Buses) between the CPU, RAM, and peripherals.
- **Cybersecurity Relevance:** 
    - **BIOS/UEFI:** The firmware that starts the computer. If an attacker infects the UEFI (Bootkits), they can control the system before the OS even loads.

### 5. Network Interface Card (NIC)
- **What it is:** The hardware that allows the computer to connect to a network.
- **Function:** Converts digital data into electrical, optical, or radio signals.
- **Cybersecurity Relevance:** 
    - **MAC Spoofing:** Attackers can change the hardware address of their NIC to impersonate another device.
    - **Promiscuous Mode:** Allows a NIC to "listen" to all traffic on a network segment, enabling packet sniffing.

## Summary Table
| Component | Role | Key Security Risk |
| :--- | :--- | :--- |
| CPU | Processing | Side-channel attacks / Firmware exploits |
| RAM | Temporary Storage | Buffer overflows / Cold boot attacks |
| Disk | Permanent Storage | Data theft / Unencrypted data |
| Motherboard | Connectivity | UEFI Bootkits |
| NIC | Network Comms | MAC spoofing / Eavesdropping |
