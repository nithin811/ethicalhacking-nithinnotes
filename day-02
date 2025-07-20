# Running Kali Linux in Oracle VirtualBox

This guide provides a step-by-step walkthrough on downloading Oracle VirtualBox and Kali Linux, setting them up, and running Kali Linux in a virtual environment.

---

## 🧰 Prerequisites

- A working computer (Windows, macOS, or Linux)
- Internet connection
- At least 20 GB of free disk space and 4 GB of RAM (recommended)

---

## 🔽 Step 1: Download Oracle VirtualBox

1. Go to the official VirtualBox website: [https://www.virtualbox.org](https://www.virtualbox.org)
2. Click on `Download VirtualBox`.
3. Choose the version appropriate for your operating system:
   - Windows hosts
   - macOS hosts
   - Linux distributions
4. Download the installer and run it.
5. Follow the on-screen instructions to complete the installation.

---

## 🔽 Step 2: Download Kali Linux ISO

1. Go to the official Kali Linux downloads page: [https://www.kali.org/get-kali/](https://www.kali.org/get-kali/)
2. Under the **Installer Images**, download the `.iso` file for **Kali Linux (64-bit)**.
   - Recommended: Use the "Installer" or "Live" ISO.
3. Save the `.iso` file to your computer.

---

## ⚙️ Step 3: Create a New Virtual Machine in VirtualBox

1. Open **Oracle VM VirtualBox**.
2. Click on `New`.
3. Enter a name (e.g., `KaliLinux`).
4. Set:
   - Type: `Linux`
   - Version: `Debian (64-bit)`
5. Click `Next`.

---

## 🧠 Step 4: Allocate Memory (RAM)

1. Choose how much RAM to allocate.
   - Recommended: At least **2 GB (2048 MB)** or more.
2. Click `Next`.

---

## 💾 Step 5: Create a Virtual Hard Disk

1. Choose `Create a virtual hard disk now`.
2. Click `Create`.
3. Choose the following:
   - Hard disk file type: `VDI (VirtualBox Disk Image)`
   - Storage: `Dynamically allocated`
   - Size: **20 GB** or more
4. Click `Create`.

---

## 📂 Step 6: Mount Kali Linux ISO

1. Select your new VM and click `Settings`.
2. Go to `Storage`.
3. Under `Controller: IDE`, click on the empty disk icon.
4. On the right, click the disk icon and choose `Choose a disk file`.
5. Browse and select the downloaded **Kali Linux ISO** file.
6. Click `OK`.

---

## 🚀 Step 7: Start Kali Linux Installation

1. Select your Kali Linux VM and click `Start`.
2. The VM will boot from the ISO.
3. Choose `Graphical Install` or `Install`.
4. Follow the installation steps:
   - Language, Location, Keyboard layout
   - Set hostname (e.g., kali)
   - Create a user account and password
   - Configure disk partitioning (use defaults for guided partitioning)
   - Finish installation and allow system to reboot

---

## 🛑 Step 8: Remove ISO (After Installation)

1. After installation and reboot, shut down the VM.
2. Go to `Settings > Storage`.
3. Under the optical drive, click the ISO and choose `Remove disk from virtual drive`.
4. Click `OK`.

---

## 🖥️ Step 9: Start Kali Linux VM

1. Select your VM and click `Start`.
2. Kali Linux should now boot from the installed virtual hard disk.
3. Log in using the username and password you created during installation.

---

## 🎉 You’re Done!

You now have Kali Linux running inside VirtualBox. You can begin using it for penetration testing, security research, or learning ethical hacking.

---

## 🧩 Optional: Install Guest Additions

1. With the VM running, go to `Devices > Insert Guest Additions CD image`.
2. Follow the prompts in Kali to install.
3. This will enable:
   - Clipboard sharing
   - Drag-and-drop
   - Full-screen mode
   - Better graphics support

---

## 🛠 Troubleshooting

- **Black Screen on Boot?** Try enabling/disabling EFI under `Settings > System`.
- **No 64-bit option?** Make sure virtualization is enabled in your BIOS/UEFI.

---

## 📝 Notes

- Always keep your VirtualBox and Kali Linux up-to-date for security.
- Use snapshots to save the state of your VM before major changes.
