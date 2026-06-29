# Architecture Diagram

## 🏗️ Overview
This diagram represents the Active Directory home lab environment, including a Domain Controller, internal client machine(s), and optional internet connectivity through a virtualized network.

---

## 📊 Diagram

```
                           🌐 Internet
                                   |
                                   |
                        ┌──────────────────────┐
                        │ External NIC (DHCP)  │
                        │ Gets IP from Router  │
                        └─────────┬────────────┘
                                  |
                                  |
                         ┌────────▼───────────┐
                         │  Domain Controller │
                         │      (DC01)        │
                         │ Windows Server 2022│
                         ├────────────────────┤
                         │ AD DS + DNS + GPO  │
                         │ Domain:            │
                         │ khanihomelab.local │
                         │ IP: 192.168.19.131  │
                         └────────┬───────────┘
                                  |
                   Internal Network (Host-Only / Internal)
                                  |
        ┌─────────────────────────┼────────────────────────┐
        |                                                  |
┌───────▼────────┐                                ┌────────▼────────┐
│   CLIENT01     │                                │   CLIENT02      │
│ Windows 11     │                                │ Windows 11      │
├────────────────┤                                ├─────────────────┤
│     Static     │                                │ DHCP or Static  │
│ preferred DNS: 172.0.0.1 │                      │ DNS: 192.168.19.131 │
│ Alternate DNS: 8.8.8.8 │                        │ Alternate: 8.8.8.8 │
│ Domain Joined  │                                │ Domain Joined   │
└────────────────┘                                └─────────────────┘
```

---

## 🔧 Network Configuration

| Component          | IP Address     | Role                  |
|-------------------|---------------|------------------------|
| Domain Controller | 192.168.19.131 | AD DS, DNS, GPO        |
| Client Machines   | DHCP / Static | Domain Members         |

---

## 🔐 Core Services

- **Active Directory Domain Services (AD DS)**  
  Centralized authentication and authorization  

- **DNS Server**  
  Resolves `khanihomelab.local` domain  

- **Group Policy (GPO)**  
  Enforces security configurations across domain  

- **Windows Defender Firewall**  
  Controls inbound/outbound traffic  

---

## 📌 Key Design Decisions

- Domain Controller uses **static IP**  
- All clients point to **DC as DNS server**     

---

## 🚀 Future Expansion

- Add secondary Domain Controller (redundancy)  
- Implement DHCP role on server  
- Add SIEM/log monitoring system  
- Simulate attack/defense scenarios  
