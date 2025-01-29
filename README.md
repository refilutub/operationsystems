
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
>![made-by-borsuk-maksym](https://github.com/user-attachments/assets/68d0a6b6-134b-4446-a841-61b9dc7c958b)

1. **Linux - Кращі дистрибутиви 2023**  
   [Переглянути відео](https://youtu.be/PahmJBU9HKA?si=maxRf0nZlqs2hFGU)

2. **ТОП 5 ПРИЧИН ЧОМУ АЙТІШНИКУ ВАРТО ПЕРЕЙТИ НА ЛІНУКС**  
   [Переглянути відео](https://youtu.be/bP3_mZKezvM?si=sM3Mpc9JQ_0bY9Yd)

3. **Як встановити Linux разом з Windows спосіб #1 Microsoft Store**  
   [Переглянути відео](https://youtu.be/eEdGl6HvSdM?si=WDbwa71i034D2rQj)

4. **Як встановити Linux разом з Windows спосіб #2 Dual Boot**  
   [Переглянути відео](https://youtu.be/Hfky8TEyXss?si=ilduY167LS-vKl9y)

5. **Як встановлювати програми на Linux. Linux українською #1**  
   [Переглянути відео](https://youtu.be/M8XHJME6cxI?si=L0Koom59jTRnPXnU)

6. **Як зробити панель завдань Linux як у Windows. Linux українською #2**  
   [Переглянути відео](https://youtu.be/9szAz-A4gaM?si=LxaVueluI3tKRb1r)

7. **Як встановити Ubuntu на VirtualBox**  
   [Переглянути відео](https://youtu.be/ADOaHm1VZII?si=hG5kDRsajFn7se8d)

8. **The Shell (Linux)**  
   [Переглянути матеріал](https://drive.google.com/open?id=0B0PV0_SM0LoDSVNPWUVRdUxaN2s)

9. **Linux Desktop Environments: XFCE vs GNOME vs KDE**  
   [Переглянути відео](https://youtu.be/2JBGQfPR5xQ?si=euswD7IHrODd-6JH)

---
2. Дайте відповіді на наступні питання. 

>[!IMPORTANT]
> 1

---



### Відповіді на контрольні запитання

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
> 1
