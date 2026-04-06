# Labs: Computer Hardware Components

## Lab 1: The Hardware Audit (Self-Guided)
**Goal:** Identify the physical specifications of your own machine and understand their security implications.

**Steps:**
1. **Install CPU-Z** (or use `system_profiler` on macOS / `msinfo32` on Windows).
2. **Identify:** 
    - Your CPU model and number of cores.
    - Your total RAM and its speed.
    - Your storage type (SSD vs HDD).
3. **Analysis:** 
    - Research if your CPU model has any known "Spectre" or "Meltdown" patches.
    - Check if your storage drive is encrypted (BitLocker on Windows / FileVault on macOS).
4. **Deliverable:** Write a short note in your vault about your system's "Physical Security Posture."

## Lab 2: The "Deleted" Data Recovery
**Goal:** Understand that "deleted" does not mean "gone."

**Steps:**
1. Create a small USB drive or a dedicated folder on a VM.
2. Create a text file called `secret.txt` with some random text.
3. Delete the file and empty the trash/recycle bin.
4. Use a tool like **Recuva** (Windows) or **PhotoRec** (Cross-platform) to attempt to recover the file.
5. **Observation:** Notice how the data was still there. This is why "Secure Erasure" or "Wiping" is necessary for cybersecurity.

## External Lab Recommendations
- **TryHackMe:** Look for the "Pre-Security" path. It contains modules on how computers work.
- **LabEx:** Check out their "Cybersecurity Labs for Beginners" for interactive hardware-software interaction exercises.
