# Operating Systems Basics

## 🖥️ Operating Systems: Introduction
### 🧠 What is it?
An Operating System (OS) is the software that acts as an interface between the user and the computer hardware. It manages hardware resources and provides services for applications.

### 📌 Key Concepts
- **Kernel:** The core of the OS. It manages memory, processes, and hardware.
- **Process Management:** Handles running applications and multitasking.
- **Memory Management:** Allocates RAM to different processes.
- **File System:** Organizes data on storage drives (e.g., NTFS, ext4).
- **User Interface:** GUI (Graphical) or CLI (Command Line).
- **Common OS:** Windows, Linux, macOS.

### 🎯 Pentester Perspective
- Knowing the OS architecture helps in understanding where vulnerabilities might exist (e.g., kernel exploits).
- Different OS require different tools and exploitation techniques.

---

## 🪟 Windows Basics
### 🧠 What is it?
Windows is the most widely used desktop OS, developed by Microsoft. It dominates corporate environments.

### 📌 Key Concepts
- **GUI Navigation:** Start Menu, Taskbar, File Explorer.
- **Task Manager:** Monitor processes, performance, and startup apps.
- **Control Panel / Settings:** Configure hardware, network, and users.
- **File System:** NTFS (New Technology File System).
- **Registry:** Central database storing low-level settings for the OS and applications.

### 🎯 Pentester Perspective
- Windows is a primary target in corporate networks.
- Attackers abuse features like PowerShell, WMI, and the Registry for persistence and execution.
- Understanding Active Directory (AD) is crucial for Windows pentesting.

---

## 🐧 Linux CLI Basics
### 🧠 What is it?
Linux is an open-source OS widely used for servers, cloud infrastructure, and cybersecurity. The CLI (Command Line Interface) is the primary way to interact with it.

### 📌 Key Concepts & Commands
- **Navigation:** `pwd` (print working directory), `ls` (list), `cd` (change directory).
- **File Management:** `mkdir`, `rm`, `cp`, `mv`, `cat`, `nano`.
- **Permissions:** `chmod` (change mode), `chown` (change owner), `rwx` (read, write, execute).
- **Searching:** `grep`, `find`.

### 🎯 Pentester Perspective
- Most web servers, cloud instances, and containers run Linux.
- Mastery of the Linux CLI is mandatory for pentesting.
- Attackers use Bash scripts for automation, reverse shells, and privilege escalation.

---

## 💻 Windows CLI Basics
### 🧠 What is it?
Windows provides two main command-line interfaces: Command Prompt (CMD) and PowerShell.

### 📌 Key Concepts & Commands
- **CMD Basics:** `dir`, `cd`, `ipconfig`, `ping`, `netstat`, `tasklist`, `whoami`.
- **PowerShell:** An advanced scripting language and shell built into Windows (`Get-Process`, `Get-ChildItem`, `Invoke-WebRequest`).
- **Batch Scripts (.bat/.cmd):** Simple automation scripts.

### 🎯 Pentester Perspective
- **PowerShell is King:** Attackers heavily abuse PowerShell for fileless malware, downloading payloads, and lateral movement.
- **Living off the Land (LotL):** Using built-in Windows tools to avoid detection by antivirus/EDR.
- **CMD:** Still useful for basic enumeration and legacy systems.

---

## 🔒 Operating System Security
### 🧠 What is it?
OS security involves protecting the OS from threats, ensuring authentication, and managing permissions properly.

### 📌 Key Concepts
- **Authentication:** Verifying identity (Username/Password, SSH Keys, Biometrics).
- **Authorization:** Determining what an authenticated user can do.
- **Principle of Least Privilege:** Users should only have the minimum permissions needed.
- **SSH (Secure Shell):** A cryptographic network protocol for secure remote login (default port 22).
- **Patching:** Keeping the OS updated to fix known vulnerabilities.

### 🎯 Pentester Perspective
- **Credential Harvesting:** Attackers look for weak passwords, SSH keys, or hashes.
- **Privilege Escalation:** Gaining higher privileges (e.g., from user to root/SYSTEM) due to misconfigurations.
- **SSH Misconfigurations:** Weak passwords, exposed private keys, or allowing root login can lead to full compromise.

---

## 📌 Module Key Takeaway
"An OS is the foundation of everything a computer does. To hack or secure a system, you must first understand how it operates, how it manages permissions, and how to interact with it via the CLI."
