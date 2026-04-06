# Quiz: Connection Types and Their Functions

**Instructions:** This quiz tests your ability to identify connection types and the specific vulnerabilities associated with them.

### Section 1: Multiple Choice

**1. Which attack involves a USB device masquerading as a keyboard to execute rapid-fire commands?**
- A) Juice Jacking
- B) DMA Attack
- C) HID Payload (BadUSB)
- D) CEC Exploitation

**2. Why is Thunderbolt considered more dangerous than standard USB in terms of memory security?**
- A) It transmits data faster.
- B) It allows Direct Memory Access (DMA), bypassing the CPU to read RAM.
- C) It can carry more voltage to destroy the motherboard.
- D) It uses the CEC protocol to control peripherals.

**3. You are at an airport and use a public USB charging kiosk. You are worried about "Juice Jacking." What is actually happening during this attack?**
- A) The kiosk is sending a power surge to fry your phone.
- B) The kiosk is using the data pins of the USB cable to exfiltrate data.
- C) The kiosk is spoofing your MAC address.
- D) The kiosk is using HDMI-CEC to see your screen.

**4. In a corporate environment, which technology is used to prevent unauthorized devices from connecting to an Ethernet port?**
- A) Full Disk Encryption
- B) 802.1X (Port-based Network Access Control)
- C) DMA Protection
- D) USB Condoms

### Section 2: Scenario Analysis

**Scenario:** An attacker plugs a modified HDMI cable into a boardroom projector. They are attempting to use the **CEC (Consumer Electronics Control)** protocol. What is their likely goal?
*Write your answer below.*
__________________________________________________________________

---
**Answer Key:**
1: C | 2: B | 3: B | 4: B
Scenario Answer: The attacker is likely trying to send control commands to other devices connected to the HDMI network or gain unauthorized control over the display system.
