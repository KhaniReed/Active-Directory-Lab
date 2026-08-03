# 🛠️ Windows Server 2022 Setup</h1>

In this stage, I installed Windows Server 2022 to be promoted and configured as the Domain Controller (DC) for my homelab environment. This process included the creation a new virtual machine in VMware Workstation Pro and installing Windows Server 2022 OS. 

---

## 💾 1. Installation

- Created a new virtual machine in VMware Workstation Pro with the following specs:

    * **60 GB Disk**
    <img width="426" height="429" alt="Step3" src="https://github.com/user-attachments/assets/19dd729c-d825-47e6-b5b2-1aac775113ab" />

    * **2 CPUs**
    <img width="758" height="714" alt="Step6" src="https://github.com/user-attachments/assets/446e1894-6e60-49c4-8a25-b44b03d3bcca" />

    * **4 GB RAM**
    <img width="755" height="713" alt="Step5" src="https://github.com/user-attachments/assets/07bae6f8-20c9-427e-8a0d-00685b70eedc" />

- **Mounted the Windows Server 2022 ISO to begin the OS installation process.**
<img width="747" height="707" alt="Step8" src="https://github.com/user-attachments/assets/bb2a0520-4ce7-4ca5-a45d-05953964494b" />

- **Selected the Datacenter Evaluation (Desktop Experience) during setup.**
<img width="1710" height="945" alt="Step13" src="https://github.com/user-attachments/assets/df585034-8fb7-4b2c-a7de-35af1c164fc5" />

--- 

## 💻 2. Initial Configuration
After installing Windows Server 2022 OS, I performed the following initial configurations:

- Changed **machine name** to ```WinServer2022-DC```
- Set a **static IP address**: ```192.168.19.131```
- Configured the **default gateway** to ```192.168.19.2```
    - This gateway configuration is based on the default configuration of the machine when running the command ipconfig in the Command Prompt before setting up a static IP. Reasoning behind this type of configuration is to still be able to access the internet while using a NAT Network Adapter instead of customized virtual network.
    - If the predefined network parameters are changed when setting up your machines network settings you will not be able to access the web. If online connectivity is not a big concern to you then make the default gateway ```192.168.19.1```.
- Configure the **Preferred DNS server** to point to itself using the local loopback address or the static IP address, in my case I used my local loopback address: ```127.0.0.1```

  <img width="1019" height="765" alt="Screenshot 2026-08-03 154716" src="https://github.com/user-attachments/assets/6ef1bc34-af3c-4ce0-80bf-c66ef47f2b3f" />


---

## 🧱 3. Installing AD DS Role

- Open **Server Manager** and select **Add Roles and Features**
- Install the **Active Directory Domain Services** role

  <img width="1024" height="769" alt="Screenshot 2026-08-03 155312" src="https://github.com/user-attachments/assets/565bc624-34ce-4d1f-9b8a-b0bd63f21f89" />
  <img width="1020" height="766" alt="Screenshot 2026-06-29 133332" src="https://github.com/user-attachments/assets/8095f1f3-f6bf-4820-934c-3e42c62ec2b3" />
  
--- 

## 📢 4. Promote Windows Server to Domain Controller (DC)

- Promote the server to a DC using the post-installation wizard
- Create a new forest name: ```khanihomelab.local```
- Accepted default NetBIOS name: ```KHANIHOMELAB```
- Once the setup is completed reboot the machine

  <img width="1022" height="770" alt="Screenshot 2026-06-29 135042" src="https://github.com/user-attachments/assets/175c5260-03c0-4dff-8569-ef5ff2961b3d" />

📸 **Confirmation of Successful Promotion**
<img width="1026" height="773" alt="Screenshot 2026-06-29 140451" src="https://github.com/user-attachments/assets/5cf41912-18b4-4638-81d3-77843f1bd154" />

--- 

## 📝 5. Summary

| Item Configured | Value |
| --- | --- |
| Server Name | WinServer2022-DC |
| Static IP | 192.168.19.131 |
| Default Gateway | 192.168.19.2 |
| DNS Server | 127.0.0.1 |
| Domain Name | khanihomelab.local |
| AD Role Installed | Active Directory Domain Services |
| Domain Controller Type | New Forest |
