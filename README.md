
<div
 align="center">
  <img src="https://github.com/user-attachments/assets/dcdd0d7c-164c-4a93-a6d8-84b6015c07aa" alt="exolutioneast">
</div>
<div align="center">

### **Київський фаховий коледж зв’язку**  
### *Циклова комісія комп’ютерної та програмної інженерії*  

<br/><br/><br/><br/>


### **ЗВІТ ПО ВИКОНАННЮ** 
### **ЛАБОРАТОРНОЇ РОБОТИ №1**  
### *з дисципліни: «Операційні системи»*  

  
### **Тема:** *«Знайомство з робочим середовищем віртуальних машин та особливостями операційної системи Linux»*  

<br/>

</div>

<div align="right">

### **Виконали студенти:**  
**Групи РПЗ-23а**  
**Команда:** Борсук М.Г., Дідусенко О.Ю.  
**Перевірила:** Сушанова В.С.  

</div>

<div align="center">

<br/>

### **Київ – 2025**  

</div>


---

### Робота студентів групи РПЗ-23а Команда 1: Борсука М.Г., Дідусенка О.Ю.


## Мета роботи:  
1. Знайомство з інтерфейсами ОС Linux.
2. Отримання практичних навиків роботи в середовищах ОС Linux та мобільної ОС – їх графічною оболонкою, входом і виходом з системи, ознайомлення зі структурою робочого столу, вивчення основних дій та налаштувань при роботі в системі


---

## Матеріальне забезпечення занять  
1. ЕОМ типу IBM PC.
2. ОС сімейства Windows та віртуальна машина Virtual Box (Oracle).
3. ОС GNU/Linux (будь-який дистрибутив).
4. Сайт мережевої академії Cisco netacad.com та його онлайн курси по Linux

---

## Завдання для попередньої підготовки  

### 
>[!IMPORTANT]
> ![made-by-borsuk-maksym](https://github.com/user-attachments/assets/68d0a6b6-134b-4446-a841-61b9dc7c958b)

### Терміни
### 1. Прочитайте короткі теоретичні відомості до лабораторної роботи та зробіть невеликий словник базових англійських термінів з питань призначення команд та їх параметрів.


| English Term                    | Ukrainian Term                   |
|----------------------------------|-----------------------------------|
| Virtual Machine                  | Віртуальна машина                 |
| Hypervisor                       | Гіпервізор                        |
| Binary Translation               | Бінарний переклад                 |
| Linux Kernel                     | Ядро Linux                        |
| Open Source                      | Відкритий код                     |
| Distribution                     | Дистрибутив                       |
| Command Line Interface (CLI)     | Інтерфейс командного рядка (CLI)  |
| Graphical User Interface (GUI)   | Графічний інтерфейс користувача   |
| JVM (Java Virtual Machine)       | Віртуальна машина Java (JVM)      |
| Guest Operating System           | Гостьова операційна система       |

---

### 2. Гіпервізор та його типи

- **hypervisor**
  Іs a software layer that allows multiple operating systems to run on a single physical machine. It works by abstracting the hardware to create VMs. There are two main types of hypervisors:

- **Type 1 Hypervisor**
  This runs directly on the host's hardware and does not require an underlying operating system. It is more efficient and secure because it has direct control over the hardware.
  
- **Type 2 Hypervisor**
  This runs on top of an existing OS and uses the resources managed by the host OS. It is generally easier to use but less efficient compared to Type 1.

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


# Хід роботи

>[!IMPORTANT] 
>![made-by-didusenko-oleksandr](https://github.com/user-attachments/assets/5659ba1e-9a2b-4c70-a617-173d94c180d0)

---
2.  Дайте відповіді на наступні питання. 
 1.1. Open VirtualBox and click "New"

 1.2. Enter a name and select the operating system type and version.
 
 1.3. Allocate RAM and create virtual hard disk

 1.4. Start the virtual machine.Follow the OS installation steps, selecting disk partitions and configurations.Complete the installation and restart.  
 
 2. # Hardware Limitations for Installing 32-bit and 64-bit Operating Systems

## 1. CPU Architecture
- **32-bit CPUs** can only run **32-bit operating systems**.
- **64-bit CPUs** can run both **32-bit and 64-bit operating systems**.
- If your processor is **x86 (32-bit only)**, you are limited to a 32-bit OS.
- If your processor is **x86-64 (AMD64, Intel64)**, you can install a 64-bit OS.

## 2. Virtualization Support
- Many **64-bit OSes** (especially in virtual machines like VirtualBox) require **hardware virtualization** (VT-x for Intel, AMD-V for AMD).
- If your CPU does not support VT-x/AMD-V or it is disabled in BIOS/UEFI, you might not be able to install a **64-bit OS in a virtual machine**.

## 3. RAM (Memory) Limitations
- **32-bit operating systems** can use a maximum of **4GB of RAM** (realistically around **3.2 - 3.5GB** due to hardware and OS limitations).
- **64-bit operating systems** can utilize more than **4GB of RAM** (e.g., Windows 10 x64 supports up to **2TB of RAM** in server editions).

## 4. Driver Compatibility
- **32-bit OS** requires **32-bit drivers**.
- **64-bit OS** requires **64-bit drivers**, which may not be available for very old hardware.

## 5. BIOS vs. UEFI Boot Mode
- Some modern **64-bit operating systems** (e.g., Windows 11 x64) require **UEFI boot mode**.
- Older computers with **BIOS-only firmware** may not support newer 64-bit OS versions.

## 6. File System Requirements
- **32-bit Windows** supports **FAT32** and **NTFS**.
- **64-bit Windows** requires **NTFS** for installation.

## Conclusion
- If you have a **64-bit processor and more than 4GB of RAM**, a **64-bit OS** is the best choice.
- If your hardware is **older (less than 4GB RAM, 32-bit CPU)**, a **32-bit OS** is necessary.
- For **virtual machines**, ensure that **VT-x/AMD-V is enabled** in BIOS to run a 64-bit OS.

Do you have a specific system in mind? I can help determine the best OS choice for it! 🚀


### Відповіді на контрольні запитання
1.Hypervisors are software or firmware that allow multiple virtual machines (VMs) to run on a single physical machine. They are categorized into Type 1 (bare-metal) and Type 2 (hosted) hypervisors.  
| Feature            | Type 1 Hypervisor (Bare-Metal) | Type 2 Hypervisor (Hosted) |
|--------------------|--------------------------------|----------------------------|
| **Architecture**   | Runs directly on the physical hardware without an underlying OS. | Runs on top of an existing operating system. |
| **Performance**    | High performance due to direct hardware access. | Slightly lower performance due to OS overhead. |
| **Security**       | More secure since it minimizes attack surfaces by eliminating the host OS. | Less secure as it relies on the security of the host OS. |
| **Resource Efficiency** | More efficient in managing system resources. | Less efficient due to additional OS layer. |
| **Use Case**       | Enterprise data centers, cloud computing, virtualization in production environments. | Personal use, software testing, and small-scale virtualization. |
| **Examples**       | VMware ESXi, Microsoft Hyper-V, KVM, Xen. | VMware Workstation, Oracle VirtualBox, Parallels Desktop. |
| **Scalability**    | Highly scalable, supporting multiple VMs on powerful hardware. | Limited scalability due to host OS constraints. |
| **Ease of Use**    | Requires specialized knowledge to set up and manage. | Easier to install and use, similar to regular applications. |

Scope of Application
   - Type 1 Hypervisors are used in enterprise and cloud environments where performance, security, and scalability are critical (e.g., data centers, cloud platforms like AWS, Azure, Google Cloud).
   - Type 2 Hypervisors are mainly used for development, testing, and running multiple OS environments on personal computers.
2. The GNU General Public License (GNU GPL) is a widely used free software license created by the Free Software Foundation (FSF). Its main concept is to ensure that software remains free (as in freedom, not necessarily price) and can be freely used, modified, and distributed by anyone.  
Main Concept:
The GNU GPL ensures that software remains open-source and free by requiring that any modified versions must also be open-source and licensed under GPL. This prevents companies from turning open-source projects into proprietary software.  
3. The essence of open-source software is freedom and collaboration. It allows anyone to view, modify, and distribute the source code, promoting transparency, innovation, and community-driven development.

4. A distribution kit (or software distribution) is a packaged version of software that includes all necessary files, libraries, and installation scripts needed to install and run the program on a specific system.
      
 5.1. User and Access Management
  - Creating, modifying, and deleting users/groups (`useradd`, `usermod`, `passwd`, `groupadd`)
  - Managing permissions (`chmod`, `chown`, `umask`)
  - Configuring sudo privileges (`visudo`)
    
 5.2. File System Management
  - Mounting and unmounting storage (`mount`,`umount`)
  - Managing partitions (`fdisk`, `parted`)
  - Checking disk usage (`df`, `du`)
  - Setting up and managing file systems (`fsck`, `mkfs`)
    
 5.3. Process and System Monitoring
  - Viewing running processes (`ps`,`top`,`htop`)
  - Managing processes (`kill`, `nice`, `renice`)
  - Checking system logs (`journalctl`,`dmesg`,`syslog`)
    
 5.4. Network Administration
  - Configuring network interfaces (`ip`,`ifcondig`,`nmcli`)
  - Checking network connections (`ping`,`netstat`,`ss`)
  - Managing firewall rules (`iptables`,`firewalld`,`ufw`)
    
 5.5. Software Management
  - Installing and updating software (`apt`, `yum`, `dnf`, `zypper`)
  - Managing services (`systemctl`, `service`)
  - Automating tasks (`cron`, `systemd timers`)
    
 6 **Key Relationships Between Android and Linux:**
  - **Shared Kernel** – Android is based on a modified Linux kernel.
  - **No GNU Utilities** – Uses Android Runtime (ART) instead of standard Linux tools.
  - **Different File System & Security** – Uses SELinux and app sandboxing.
  - **No Standard Linux Software** – Runs APK files, not Linux packages.
  - **Different Development Focus** – Linux is for servers/desktops, Android is for mobile devices.
    
 7. **Main Features of Embedded Linux**
  - Lightweight & Modular – Optimized for low-resource devices.
  - Customizable – Can be stripped down to essential components.
  - Real-Time Capabilities – Supports RTOS-like behavior for critical tasks.
  - Hardware Support – Works on ARM, x86, MIPS, and more.
  - Open Source – Free to modify and distribute.  
 **Scope of Embedded Linux**
  - Consumer Electronics – Smart TVs, routers, cameras.
  - Industrial Automation – PLCs, IoT controllers.
  - Automotive Systems – Infotainment, ADAS.
  - Medical Devices – Monitoring systems, diagnostic tools.
  - Robotics & Aerospace – Drones, satellites.
 
 8. **Change Boot Mode (Text Mode or Graphical Mode):**  
 For Systemd-based Systems:
  - Text Mode (Multi-user.target):  
 Run sudo systemctl set-default multi-user.target to set default to text mode.
  - Graphical Mode (Graphical.target):
 Run sudo systemctl set-default graphical.target to set default to graphical mode.
 **Difference Between CLI and GUI Modes:**
  - CLI (Command-Line Interface) – Mode with no graphical environment. Users interact via a terminal and commands. It's lightweight and often used in servers, embedded systems, and for administrative tasks.
  - GUI (Graphical User Interface) – Mode with a graphical environment like GNOME or KDE. Users interact with windows, icons, and menus, offering a more user-friendly experience, suitable for desktop usage.

>[!IMPORTANT]
>![made-by-borsuk-maksym](https://github.com/user-attachments/assets/68d0a6b6-134b-4446-a841-61b9dc7c958b)

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


# Висновки
>[!IMPORTANT]
>![made-by-didusenko-oleksandr](https://github.com/user-attachments/assets/5659ba1e-9a2b-4c70-a617-173d94c180d0)


In the course of the laboratory work, we got acquainted with the peculiarities of working in the environment of virtual machines and the Linux operating system. We studied the basic principles of hypervisors, the difference between their types, and the capabilities of Oracle VirtualBox to create and manage virtual machines.  

We learned how to install and configure Linux in a virtual environment, explored its graphical interface and command line. We also reviewed the basic commands for managing files, users, and processes, which is essential for effective work in Linux.  

In addition, we learned the basics of network administration, access configuration, file system management, and system health monitoring. The relationship between Linux and Android was discussed, as well as the specifics of using embedded Linux in various fields.  

As a result, we have gained practical skills in using Linux in a virtual environment, which is an important step in the study of operating systems and system administration.
