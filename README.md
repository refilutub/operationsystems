
<div align="center">
  <img src="https://github.com/user-attachments/assets/dcdd0d7c-164c-4a93-a6d8-84b6015c07aa" height="200" width="300" alt="exolutioneast">
</div>
<div>
  <img src="https://github.com/user-attachments/assets/b892ad7e-8842-4b58-9b43-ca318ffc4ef1" height=50 width=50>
</div>

---

### Знайомство з робочим середовищем віртуальних машин та особливостями операційної системи Linux

>[!IMPORTANT]
> this part was made by Maksym Borsuk
### Терміни

1. **Virtual Machine (VM)**  
   A VM is a software-based simulation of a physical computer. It allows multiple operating systems to run on the same physical machine by emulating hardware and running a guest OS.

2. **Hypervisor**  
   A hypervisor is software that manages VM. It allows for the creation, execution, and management of VMs on a host machine, either directly (Type 1) or using a host OS (Type 2).

3. **Type 1 Hypervisor**  
   A type 1 hypervisor runs directly on the host machine’s hardware, with no underlying operating system. It's more efficient as it doesn’t rely on a host OS to manage resources.

4. **Type 2 Hypervisor**  
   A type 2 hypervisor runs on top of a host OS, relying on the host OS for resource management and access to hardware. It is typically slower than type 1 but easier to set up and use.

5. **VirtualBox**  
   VirtualBox is a Type 2 hypervisor by Oracle that allows users to run multiple guest operating systems on a single physical machine. It provides features like snapshots and seamless window integration.

6. **Kernel**  
   The kernel is the core part of an operating system, responsible for managing system resources, hardware, and communication between software and hardware.

7. **Binary Translation**  
   Binary translation is a method used by some VM monitors to convert non-native instructions into instructions that the host machine can understand, improving performance.

8. **Guest OS**  
   A guest OS is the operating system running inside a virtual machine, separate from the host operating system. It behaves as though it is running on its own physical machine.

9. **Host OS**  
   The host OS is the operating system running on the physical machine, providing resources for virtual machines and managing hardware.

10. **JVM (Java Virtual Machine)**  
   The JVM is a VM that enables Java applications to run on any platform. It interprets bytecode into machine code that can be executed on different hardware architectures.

---

### Гіпервізор та його типи

A **hypervisor** is a software layer that allows multiple operating systems to run on a single physical machine. It works by abstracting the hardware to create VMs. There are two main types of hypervisors:

- **Type 1 Hypervisor**: This runs directly on the host's hardware and does not require an underlying operating system. It is more efficient and secure because it has direct control over the hardware.
- **Type 2 Hypervisor**: This runs on top of an existing OS and uses the resources managed by the host OS. It is generally easier to use but less efficient compared to Type 1.

---

### Компоненти та можливості Oracle VirtualBox

Oracle **VirtualBox** is a Type 2 hypervisor with the following key components and capabilities:

- **VMs**: VirtualBox allows to create and manage VMs, each running its own guest OS.
- **Snapshots**: VirtualBox lets to take snapshots of a VM's state, enabling you to return to a previous state if needed.
- **Seamless Mode**: This feature integrates the guest OS windows directly into the host desktop, creating a seamless user experience.
- **Virtual Network**: VirtualBox supports creating virtual networks between VMs, enabling them to communicate with each other.
- **USB Device Support**: It allows for USB device passthrough, enabling the VM to use USB devices connected to the host machine.
- **Guest Additions**: These are additional tools installed inside the guest OS to improve performance and enable features like shared folders and mouse pointer integration.

---

---

### Відповіді на контрольні запитання
1. **Comparison of Type 1 and Type 2 Hypervisors:**
   - **Type 1** hypervisors run directly on hardware, offering better performance and security. 
   - **Type 2** hypervisors run on top of an existing OS, making them easier to install but less efficient. 
   - **Type 1** is used in data centers and enterprise environments, while **Type 2** is suitable for personal use and testing.

2. **GNU GeneralPublicLicense:**
   - The **GNU GPL** is a free software license that ensures users can run, modify, and share software.
   - Its main concept is that any software using GPL must also be open source and share any modifications.

3. **Open-Source Software:**
   - **Open-source software** is software whose source code is available to the public for free. 
   - It allows anyone to inspect, modify, and distribute the software.

4. **What is a Distribution?**
   - A **distribution** is a complete version of an operating system based on the Linux kernel, including software and packages.
   - Examples include **Ubuntu**, **Fedora**, and **Debian**.

5. **System Administration Tasks on Linux:**
   - On Linux, system administrators can perform tasks like:
     - User management
     - Network configuration
     - File system maintenance
     - Security configuration
     - Software installation

6. **Connection Between Android and Linux:**
   - **Android** is based on the **Linux kernel** but includes additional software layers for mobile devices, such as application frameworks and libraries.

7. **Embedded Linux:**
   - **Embedded Linux** is a lightweight version of Linux used in devices like routers, smart TVs, and industrial machines.
   - It offers flexibility, low resource requirements, and customizability for embedded systems.

8. **Changing Linux Boot Modes:**
   - To can change the boot level by editing the **GRUB** bootloader. 
     - For **text mode**, modify the GRUB configuration to set the default runlevel to 3. 
     - For **graphical mode**, change it to 5.
   - **CLI** is text-based, while **GUI** is more user-friendly with visual elements.




