# Labs: Connection Types and Their Functions

## Lab 1: The "USB Condom" Experiment
**Goal:** Understand the difference between Power-only and Data+Power connections.

**Steps:**
1. Obtain a USB Data Blocker (USB Condom).
2. Plug a USB drive into the blocker, then plug the blocker into your PC.
3. **Observation:** Notice that the PC does *not* recognize the drive.
4. **Analysis:** Why did this happen? (The data pins were physically disconnected). Explain why this is the only 100% effective defense against Juice Jacking.

## Lab 2: Analyzing Hardware Identifiers
**Goal:** Learn how the OS identifies connection types and devices.

**Steps:**
1. Plug in various devices (USB mouse, Keyboard, HDMI monitor, Ethernet cable).
2. **On Windows:** Open `Device Manager` $\rightarrow$ `View` $\rightarrow$ `Devices by connection`.
3. **On macOS:** Go to `About This Mac` $\rightarrow$ `System Report` $\rightarrow$ `USB` / `Ethernet`.
4. **Analysis:** Find the "Vendor ID" (VID) and "Product ID" (PID) for your USB devices. 
5. **Research:** Look up your VID/PID online. Can you find if there are known malicious versions of this hardware?

## Lab 3: Simulating a HID Attack (Safe Mode)
**Goal:** Understand how the OS trusts keyboards.

**Steps:**
1. Open a simple text editor (Notepad or TextEdit).
2. Use a tool like **AutoHotKey** (Windows) or **AppleScript** (macOS) to write a script that types "Hacked!" and presses Enter.
3. Run the script.
4. **Reflection:** Notice how the computer doesn't ask "Is this keyboard trusted?" before executing the typing. This is the fundamental flaw that BadUSB exploits.
