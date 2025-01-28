
<div align="center">
  <img src="https://github.com/user-attachments/assets/dcdd0d7c-164c-4a93-a6d8-84b6015c07aa" height="200" width="300" alt="exolutioneast">
</div>

<div align="center">
  <img src="https://github.com/user-attachments/assets/e07ef49b-2b7f-461c-a0da-f55f6aab7317" alt="i-need-one-more-dep">
  <img src="https://github.com/user-attachments/assets/b4a29003-d0da-4248-bf07-1f49b72ba70c" alt="linux-ubuntu">
  <img src="https://github.com/user-attachments/assets/26202f10-9dfb-45c4-a997-b90b1ea1808c" alt="linux-kde-plasma-gui">
  <img src="https://github.com/user-attachments/assets/567fb209-0cf7-41ea-ab04-948bc42783b8" alt="linux-gnome-gui">
</div>



### Basic Actions in a Hypervisor for Managing Virtual Machines:

>[!NOTE]
>We are going to use Oracle VirtualBox (later OVB)

>[!IMPORTANT]
> this part made by Maksym Borsuk



#### **1. Creating a New Virtual Machine**
1. Start the OVB.  
2. Press the "Create" button in the menu.  
3. Type the name for the virtual machine and pick the operating system:  
   - Choose the version of the OS (in our case it is Linux).  
4. Set how much RAM you want to give to the virtual machine.  
5. Make or choose a hard disk:  
   - Create a new virtual drive (formats like VHD, VDI, or VMDK).  
   - Pick if you want fixed storage size or dynamic.  
6. Hit "Finish" to create the VM.

---

#### **2. Adding Hardware to Virtual Machine**
1. Select your virtual machine from the list.  
2. Go to "Settings."  
3. There you can configure or add hardware:  
   - **System:** Set the number of CPUs or enable hardware acceleration.  
   - **Display:** Change video memory or screen settings.  
   - **Storage:** Add ISO images or new virtual hard drives.  
   - **Audio:** Turn on or off sound devices.  
   - **USB:** Enable USB support.

---

#### **3. Setting Up the Network and Connecting to Wi-Fi**
1. Open "Settings" → "Network":  
   - Choose a network mode:  
     - **NAT:** Automatically connects VM to the internet via the host.  
     - **Bridge Adapter:** Lets the VM use the same network as the host.  
     - **Host-Only:** Creates a local network only between host and VM.  
2. To use Wi-Fi:  
   - With NAT or Bridge mode, VM will use the Wi-Fi of the host system automatically.  
   - Make sure the network adapter is turned on in the settings.

---

#### **4. Using USB Flash Drives**
1. Plug the USB flash drive into your computer.  
2. In the hypervisor, open "Settings" → "USB":  
   - Add the USB device you want to use with the VM.  
   - Select the right USB version.  
3. Start your VM.  
4. In the hypervisor menu (like in VirtualBox → Devices → USB Devices), choose your USB flash drive.  
5. The drive will now appear in the VM and can be used like an external device.

---
