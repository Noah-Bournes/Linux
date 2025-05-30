# 🔧 Complete Kali Linux Setup Guide
*Setting up Kali Linux from scratch for TarbhTech*

---

## 📋 Prerequisites

- A computer or virtual machine ready for installation
- Kali Linux ISO downloaded and burned to USB
- Basic understanding that you'll be erasing the target drive

---

## 🚀 Installation Process

### Step 1: Boot and Initial Setup

1. **Boot from your Kali Linux installation media**
2. **Select "Graphical Install"** from the boot menu
   - *This provides an easier, visual installation process*

### Step 2: Language and Location Settings

3. **Language Selection**
   - Choose: **English**

4. **Country Selection**
   - Choose: **Ireland**

5. **Keyboard Layout**
   - Choose: **British English**
   - *This matches Irish keyboard layouts*

### Step 3: Network Configuration

6. **Network Interface Selection**
   - Choose your network interface:
     - **eth0** (for wired ethernet connection)
     - **wlan0** (for wireless connection)
   - *If using wireless, you'll need to enter WiFi credentials*

7. **Hostname Configuration**
   - **Hostname**: Enter your device name (this will be displayed on the network)
   - *Example: kali-laptop, pentest-01, etc.*

8. **Domain Name** *(Optional)*
   - Leave blank unless you're part of a specific domain
   - *Most home/office setups can skip this*

### Step 4: User Account Setup

9. **Username Creation**
   - **Username**: `TarbhTech`
   - *This will be your primary user account*

10. **Password Setup**
    - Create a strong password for the TarbhTech user
    - **Important**: Remember this password - you'll need it frequently

### Step 5: Disk Partitioning

11. **Partitioning Method**
    - Select: **Use entire disk**
    - ⚠️ **Warning**: This will erase everything on the selected drive

12. **Disk Selection**
    - Choose your **SSD** from the list of available drives
    - Double-check you're selecting the correct drive

13. **Partition Structure**
    - Select: **Separate /home, /var, and /tmp partitions**
    - This provides better security and performance:
      - `/home` - User files and data
      - `/var` - System logs and variable data
      - `/tmp` - Temporary files

14. **Review Partition Structure**
    - The installer will show you the partition layout
    - Review carefully, then click **Continue**

15. **Confirm Changes**
    - Click **Yes** to "Write changes to disks"
    - ⚠️ **Final warning**: This is your last chance before data is erased

### Step 6: Desktop Environment Selection

16. **Software Selection**
    - **IMPORTANT**: Only select **XFCE Desktop Environment**
    - **Uncheck all other desktop environments** (GNOME, KDE, etc.)
    - *Having multiple desktop environments can cause system instability*

17. **Complete Installation**
    - Wait for the installation to complete
    - The system will reboot automatically

---

## ⚡ Post-Installation Setup

### Step 7: Opening the Terminal
Once your system boots up, you need to open a terminal (command line interface):

#### Method 1: Using the Applications Menu
1. Click on the **Applications** menu (usually in the top-left corner)
2. Navigate to **System** → **Terminal Emulator**
3. Click to open the terminal

#### Method 2: Using Keyboard Shortcut
- Press **Ctrl + Alt + T** simultaneously
- This will open a terminal window instantly

#### Method 3: Right-click Desktop
- Right-click on an empty area of the desktop
- Select **"Open Terminal Here"** from the context menu

You'll see a black window with white text and a command prompt that looks like:
```
TarbhTech@hostname:~$
```

### Step 8: Terminal Commands
Now run these commands **in order** by copying and pasting them into the terminal:

#### 1. Update Package Lists
```bash
sudo apt update
```
*This downloads the latest package information from repositories*

#### 2. Upgrade All Packages
```bash
sudo apt full-upgrade -y
```