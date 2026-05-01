# Active Directory Home Lab

## 📌 Overview
This project is a hands-on Active Directory home lab designed to simulate a real-world enterprise environment using Windows Server 2022. The lab focuses on deploying and managing a Domain Controller, integrating a client machine into the domain, enforcing security policies through Group Policy Objects (GPOs), and implementing infrastructure hardening techniques.

The goal of this lab is to strengthen practical skills in system administration, cybersecurity, and enterprise network security while documenting the entire process in a structured and reproducible format.

---

## 🎯 Objectives
- Deploy Windows Server 2022 as a Domain Controller
- Create and manage an Active Directory domain environment
- Join a Windows client machine to the domain
- Configure Organizational Units (OUs), users, and groups
- Implement GPO-based security policies
- Apply infrastructure security (firewall rules, network protections, service hardening)
- Develop PowerShell automation scripts for administrative tasks
- Validate configurations and troubleshoot common issues

---

## 🏗️ Lab Architecture

**Environment Setup:**
- **Domain Controller:** Windows Server 2022
- **Client Machine:** Windows 11
- **Virtualization:** VMware Workstation
- **Network Type:** Internal Network (isolated lab environment)

**Basic Architecture:**
```
[ Client Machine ]  <---->  [ Domain Controller (DC01) ]
        |                            |
     Domain Joined           Active Directory, DNS, GPO
```

---

## 🛠️ Tools & Technologies
- **Operating Systems:** Windows Server 2022, Windows 10/11  
- **Directory Services:** Active Directory Domain Services (AD DS)  
- **Security Tools:** Windows Defender Firewall, Group Policy Management  
- **Scripting:** PowerShell  
- **Virtualization:** VirtualBox / VMware  
- **Networking:** DNS, TCP/IP
  
---

## 📁 Project Structure

```
active-directory-lab/
│
├── README.md
├── /planning
├── /environment-setup
├── /configuration
├── /security-hardening
├── /automation
├── /validation
├── /troubleshooting
├── /screenshots
└── /scripts
```

### 📂 Folder Breakdown

#### `/planning`
- Lab overview and objectives  
- Architecture diagram  
- Prerequisites and system requirements  

#### `/environment-setup`
- Virtual machine creation  
- Windows Server installation  
- Client machine setup  
- Network configuration  

#### `/configuration`
- Installing Active Directory Domain Service  
- Promoting server to Domain Controller  
- Creating and configuring the domain  
- Joining client to domain  
- Creating users, groups, and OUs  

#### `/security-hardening`
- Password and account lockout policies  
- GPO security configurations  
- Firewall rules and network security  
- Service hardening and restrictions  

#### `/automation`
- PowerShell scripts for:
  - User creation  
  - Bulk user import  
  - GPO configuration  

#### `/validation`
- Domain join verification  
- GPO application testing  
- Security policy validation  

#### `/troubleshooting`
- Common issues and fixes:
  - DNS misconfiguration  
  - Domain join failures  
  - GPO not applying  

#### `/scripts`
- PowerShell automation scripts used in the lab  

#### `/screenshots`
- Visual documentation of setup, configuration, and results  

---

## 🚀 Key Features
- Full Active Directory deployment in a lab environment  
- Domain Controller configuration and management  
- GPO-based security baseline implementation  
- Network and firewall hardening  
- PowerShell automation for administrative efficiency  
- Step-by-step documentation for reproducibility  

---

## 🔐 Security Implementation Highlights
- Enforced password complexity and expiration policies  
- Configured account lockout thresholds to prevent brute-force attacks  
- Implemented audit policies for monitoring user activity  
- Applied Windows Firewall rules to restrict unnecessary traffic  
- Disabled insecure protocols and hardened system services  

---

## 🤖 Automation
PowerShell is used to automate administrative tasks, including:
- Bulk user creation and management  
- Group assignment  
- GPO configuration  

Scripts can be found in the `/scripts` directory with explanations in `/automation`.

---

## ✅ Validation & Testing
- Verified domain connectivity and authentication  
- Tested GPO enforcement using `gpresult` and policy updates  
- Simulated account lockouts and security controls  
- Confirmed firewall and network configurations  

---

## 🛠️ Troubleshooting
Common issues encountered and resolved:
- DNS misconfiguration preventing domain join  
- Incorrect network settings between client and server  
- GPOs not applying due to OU or scope issues  

Detailed solutions are documented in the `/troubleshooting` folder.

---

## 📸 Screenshots
Screenshots documenting each phase of the lab can be found in the `/screenshots` directory.

---

## 📈 Future Improvements
- Simulate attack scenarios and detection (Blue Team focus)  
- Integrate SIEM tools for log monitoring
---

## 📌 Status
🚧 **This project is currently in progress and actively being updated.**
