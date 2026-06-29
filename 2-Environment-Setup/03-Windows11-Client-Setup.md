# 💻 Windows 11 Client Setup
This section details how I installed my Windows 11 Pro client VM.

---

## 🖥️ 1. Virtual Machine Creation
I created a new Windows 11 Virtual Machine in VMware Workstation Pro with the following specs:

- **Windows 11 Pro OS**
<img width="1701" height="943" alt="Step20" src="https://github.com/user-attachments/assets/89855e09-56d0-466f-a6df-69121c38604e" />

- **4 GB RAM**
<img width="748" height="714" alt="Step8" src="https://github.com/user-attachments/assets/16564ffe-602b-4fff-8667-91be62c8d8d1" />

- **2 CPUs**
<img width="744" height="704" alt="Step9" src="https://github.com/user-attachments/assets/91206137-dc29-46c5-8a0f-6cf352172ad2" />

- **64 GB Disk**
<img width="420" height="426" alt="Step6" src="https://github.com/user-attachments/assets/f6aae473-2fd2-4b69-9bc9-154908f88682" />

---

**⚠️ To be able to install Windows 11 VM you must ensure you have TPM (Trusted Platform Module) enabled as it is a baseline hardware requirement. If when setting up your VM TPM is not automatically enabled please follow the below steps to ensure it is active:**

1. Click **"Edit virtual machine settings"**
<img width="1915" height="1026" alt="Step11" src="https://github.com/user-attachments/assets/9b18f7d3-fd69-4318-a8f0-4a35e94acfc5" />

2. **Virtual Machine Settings > Options > Access Control**
    - Set a password for the encprytion of the VM
    <img width="754" height="727" alt="Step15" src="https://github.com/user-attachments/assets/30b308d7-5a3b-47d4-914a-b4b88df9d47a" />

3. **Virtual Machine Settings > Hardware**
    - Click **"Add"**
    <img width="759" height="724" alt="Step13" src="https://github.com/user-attachments/assets/e36cfb1f-9655-496b-8df1-1a59405b411a" />

    - In the "Add Hardware Wizard" select **"Trusted Platform Module"** then select finish
    <img width="441" height="430" alt="Step14" src="https://github.com/user-attachments/assets/e8ab8633-a193-47b2-9350-b1bfc33c0445" />

- **To verify that you have successfully added TPM, in the Hardware tab of virtual machine settings that TPM now shows the status of present.**
<img width="749" height="724" alt="Step12" src="https://github.com/user-attachments/assets/7949886c-75a0-4a0f-949e-13c71cc4f092" />

---
