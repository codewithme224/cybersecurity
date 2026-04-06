# Lesson: Connection Types and Their Functions

## Introduction
In cybersecurity, "connectivity" is the primary attack vector. Whether it's a physical cable or a wireless signal, any point where data enters or leaves a system is a potential gateway for an attacker. Understanding not just *what* a connection does, but *how* it can be abused, is critical for hardware hardening.

---

## 1. Peripheral & Data Connections

### USB (Universal Serial Bus)
- **Function:** The standard for connecting peripherals (keyboards, mice, drives, webcams).
- **Technical Detail:** USB uses a bus architecture allowing multiple devices to connect to a single host. Modern standards (USB 3.0, 3.1, USB-C) focus on higher data throughput and power delivery.
- **Cybersecurity Risks:**
    - **HID Payload Attacks (BadUSB):** A device that looks like a USB thumb drive but registers as a keyboard (Human Interface Device). Once plugged in, it "types" malicious commands at superhuman speed to steal data or install backdoors.
    - **USB Killer:** A device designed to send high-voltage power surges into the motherboard, physically destroying the hardware.
    - **Juice Jacking:** Malicious charging stations that use the USB data pins to steal data or install malware while the user thinks they are only charging their phone.
- **Mitigation:** Disable unused USB ports in BIOS, use "USB Condoms" (data blockers), and implement endpoint security to block unauthorized HID devices.

### Thunderbolt & USB-C
- **Function:** High-speed data transfer and video output. Thunderbolt is essentially PCIe (Peripheral Component Interconnect Express) extended over a cable.
- **Technical Detail:** Because Thunderbolt provides direct access to the system's memory (DMA - Direct Memory Access) for speed, it is incredibly powerful.
- **Cybersecurity Risks:**
    - **DMA Attacks (Thunderclap):** Because Thunderbolt can bypass the CPU to read/write directly to RAM, an attacker with a malicious Thunderbolt device can read sensitive data (like encryption keys) directly from memory without the OS ever knowing.
- **Mitigation:** Use "Kernel DMA Protection" (enabled in modern Windows/macOS) to isolate memory regions.

---

## 2. Display & Video Connections

### HDMI (High-Definition Multimedia Interface) & DisplayPort
- **Function:** Transmit uncompressed video and audio data from a source to a display.
- **Technical Detail:** HDMI includes **CEC (Consumer Electronics Control)**, which allows devices to control each other (e.g., your TV turning on your Soundbar).
- **Cybersecurity Risks:**
    - **CEC Exploitation:** Attackers can use the CEC protocol to send commands to other devices on the HDMI network, potentially gaining control over a home theater system or projecting unauthorized content.
    - **HDMI "Sniffing":** Specialized hardware can capture the unencrypted video/audio stream from an HDMI cable to steal visual information (like passwords being typed on a screen).
- **Mitigation:** Use trusted cables and avoid plugging laptops into "public" projectors/displays without verifying the hardware.

### VGA & DVI (Legacy)
- **Function:** Analog (VGA) and Digital (DVI) video transmission.
- **Cybersecurity Relevance:** Lower risk than USB/Thunderbolt because they generally do not transmit data *back* to the computer in a way that allows for code execution. However, they are susceptible to physical signal interception (EMI sniffing).

---

## 3. Network Connections

### Ethernet (RJ-45)
- **Function:** The physical cabling (Copper/Fiber) used for Local Area Networks (LAN).
- **Technical Detail:** Operates at Layer 1 (Physical) and Layer 2 (Data Link) of the OSI model.
- **Cybersecurity Risks:**
    - **MAC Spoofing:** Impersonating a trusted device to bypass port security.
    - **Ethernet Tapping:** Using a "Network Tap" to physically split the cable and copy all traffic passing through it.
- **Mitigation:** Use 802.1X authentication (Port-based Network Access Control) to ensure only authorized devices can connect.

---

## Connection Matrix Summary

| Connection | Primary Use | Primary Security Threat | Threat Type |
| :--- | :--- | :--- | :--- |
| **USB** | Peripherals | BadUSB / Juice Jacking | Logic/Physical |
| **Thunderbolt**| High-Speed Data | DMA Memory Access | Hardware/Kernel |
| **HDMI** | Video/Audio | CEC Exploitation | Protocol |
| **Ethernet** | Networking | Packet Sniffing / Tapping | Network |
| **VGA** | Legacy Video | EMI Signal Interception | Physical |
