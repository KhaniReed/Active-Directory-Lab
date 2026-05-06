# Network Design

## 🌐 Overview
This lab uses a simple internal network to allow communication between the Domain Controller and the client machine.

---

## 📡 Network Configuration

| Component          | IP Address     | Role                  |
|-------------------|---------------|------------------------|
| Domain Controller | 192.168.56.10 | DNS, AD DS             |
| Client Machine    | 192.168.56.20 | Domain Member          |

---

## 🧭 Subnet Details
- Network: 192.168.56.0/24
- Subnet Mask: 255.255.255.0
- Gateway: (Optional depending on setup)

---

## 🔑 DNS Configuration
- Primary DNS: Domain Controller IP (192.168.56.10)
- Required for domain join and authentication

---

## 🖥️ Domain Information
- Domain Name: khanihomelab.local
- NetBIOS Name: KhaniHomeLab

---

## 🔄 Communication Flow
1. Client sends authentication request
2. DNS resolves Domain Controller
3. Domain Controller validates credentials
4. Policies are applied via GPO

---

## 📌 Notes
- Static IP is required for Domain Controller
- Client can use static or DHCP (if configured later)
- DNS must always point to the Domain Controller
