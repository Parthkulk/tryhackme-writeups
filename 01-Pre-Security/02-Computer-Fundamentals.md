# Computer Fundamentals

## 🖥️ Inside a Computer System
### 🧠 What is it?
A computer system is made up of physical hardware components that work together to process data and execute instructions.

### 📌 Key Concepts
- **CPU (Central Processing Unit):** The "brain" of the computer. It executes instructions.
- **RAM (Random Access Memory):** Temporary, fast memory. Data is lost when power goes off.
- **Storage (HDD/SSD):** Permanent storage for files, OS, and applications.
- **Motherboard:** The main circuit board connecting all components.
- **PSU (Power Supply Unit):** Provides power to all components.
- **GPU (Graphics Processing Unit):** Handles graphics and rendering.

### 🎯 Pentester Perspective
- **RAM Scraping:** Attackers can dump RAM to extract credentials (like passwords or encryption keys) since they exist in plaintext temporarily.
- **Physical Access:** If an attacker has physical access to the hardware, they can steal the hard drive, install hardware keyloggers, or boot from a malicious USB.
- **Firmware Attacks:** Malware can infect the BIOS/UEFI, persisting even after an OS reinstall.

---

## 💻 Computer Types
### 🧠 What is it?
Computers come in various forms, from massive data center servers to tiny microcontrollers embedded in everyday devices.

### 📌 Key Concepts
- **Desktop/Laptop:** Personal computers for general use.
- **Servers:** Powerful computers that provide services to other computers over a network.
- **IoT (Internet of Things) Devices:** Smart devices (cameras, thermostats, coffee machines) connected to the internet.
- **Embedded Systems:** Specialized computers inside larger systems (cars, medical devices).

### 🎯 Pentester Perspective
- **IoT Weaknesses:** IoT devices often have default credentials, unpatched firmware, and insecure network services, making them easy targets for botnets (e.g., Mirai).
- **Servers = High Value:** Pentesters focus heavily on servers because they hold critical data and services.

---

## 🌐 Client-Server Basics
### 🧠 What is it?
The Client-Server model is a network architecture where clients (users) request resources or services, and servers provide them.

### 📌 Key Concepts
- **Client:** The device requesting a service (e.g., your browser).
- **Server:** The device providing the service (e.g., a web server).
- **Request-Response Cycle:** Client sends a request, Server processes it and sends back a response.
- **Protocols:** HTTP/HTTPS, FTP, DNS, SSH.

### 🎯 Pentester Perspective
- **Web App Pentesting:** Understanding the client-server model is crucial for testing web apps (intercepting requests with Burp Suite).
- **Server-Side vs Client-Side Attacks:** Some vulnerabilities happen on the server (SQL Injection), while others happen on the client (XSS).
- **Man-in-the-Middle (MITM):** Attackers can intercept the communication between client and server.

---

## 📦 Virtualisation Basics
### 🧠 What is it?
Virtualization is the process of creating a software-based (virtual) version of something, such as a server, storage, or network. It allows multiple operating systems to run on a single physical machine.

### 📌 Key Concepts
- **Hypervisor:** Software that creates and runs virtual machines (VMs). (Type 1: Bare-metal, Type 2: Hosted).
- **Virtual Machine (VM):** An isolated environment that acts like a physical computer.
- **Containers (Docker):** Lightweight virtualization that shares the host OS kernel.
- **Snapshots:** Saving the state of a VM to restore later.

### 🎯 Pentester Perspective
- **Isolation for Safety:** Pentesters use VMs to safely run malware or test exploits without infecting their main OS.
- **VM Escape:** A critical vulnerability where an attacker breaks out of the VM to access the host OS.
- **Container Breakout:** Similar to VM escape, escaping a container to access the host.

---

## ☁️ Cloud Computing Fundamentals
### 🧠 What is it?
Cloud computing is the delivery of computing services (servers, storage, databases, software) over the internet ("the cloud").

### 📌 Key Concepts
- **IaaS (Infrastructure as a Service):** Renting virtual machines, storage, and networks (e.g., AWS EC2).
- **PaaS (Platform as a Service):** Renting a platform to develop and deploy apps (e.g., Heroku).
- **SaaS (Software as a Service):** Using software over the internet (e.g., Gmail, Office 365).
- **Public vs Private vs Hybrid Cloud:** Deployment models based on who uses the cloud.

### 🎯 Pentester Perspective
- **Cloud Misconfigurations:** The #1 cause of cloud breaches (e.g., public S3 buckets, overly permissive IAM roles).
- **Identity is the New Perimeter:** In the cloud, IAM (Identity and Access Management) is everything. Escalating privileges there means full compromise.
- **Shared Responsibility Model:** The cloud provider secures the cloud, but YOU secure what's IN the cloud.

---

## 📌 Module Key Takeaway
"Understanding the hardware, types of computers, client-server model, virtualization, and cloud basics forms the bedrock of cybersecurity. You cannot secure what you don't understand."
