<div align="center">
  <img src="https://github.com/user-attachments/assets/dcdd0d7c-164c-4a93-a6d8-84b6015c07aa" height="200" width="300" alt="exolutioneast">
</div>

### 1. При роботі з персональним комп’ютером дуже часто виникає необхідність підключати периферійне обладнання. На прикладі принтера та флешки опишіть який механізм має ОС Linux для роботи з ними.

  In Linux, peripheral devices such as printers and USB flash drives are managed through a combination of device drivers, mounting mechanisms, and system services like CUPS (for printers) and udev (for detecting devices).
  
  When a USB flash drive is connected, the Linux kernel detects it as a block device (e.g., `/dev/sdb1`) and can automatically or manually mount it to a specific directory so the user can access its files. For printers, Linux uses the **CUPS (Common UNIX Printing System)** to manage print jobs and interact with various printer drivers.
  
  ---
  
  ### **- What is the purpose of the mounting operation, what is it used for, and how?**
  
  The **mounting operation** in Linux is the process of making a storage device (like a USB flash drive) accessible through the system’s file hierarchy. Unlike Windows, where each drive appears as a separate letter (e.g., D:\, E:\), Linux integrates devices into a single directory tree.
  
  Mounting means attaching the device’s filesystem to a mount point (e.g., `/media/usb` or `/mnt/usb`) so users can read and write files. This can be done automatically by the system (with tools like `udisks` or file managers) or manually via the terminal:
  ```bash
  sudo mount /dev/sdX1 /mnt/usb
  ```
  
  ---
  
  ### **- What is the difference in working with peripherals in Linux and Windows?**
  
  | Aspect | Linux | Windows |
  |--------|-------|---------|
  | **Mounting** | Manual or automatic, device must be mounted to access | Automatic, device appears as a drive letter |
  | **Device Recognition** | Uses system logs (`dmesg`), `lsblk`, `udev` rules | Plug and play, recognized by Windows Explorer |
  | **Printer Setup** | Requires CUPS and manual configuration of drivers | Usually automatic via built-in drivers |
  | **Filesystem Support** | Supports many filesystems (ext4, NTFS, FAT32) but may require additional packages | Primarily NTFS and FAT32, full support out of the box |
  | **User Control** | High level of control and customization | More user-friendly but less customizable |
  
  --- 

>[!IMPORTANT]
> ![made-by-borsuk-maksym](https://github.com/user-attachments/assets/68d0a6b6-134b-4446-a841-61b9dc7c958b)

### 2. Підключіть до вашої віртуальної машини зі встановленою ОС Linux флешку та принтер (за можливості) та через графічний інтерфейс скопіюйте один файл з флешки на віртуальну машину та роздрукуйте його (такі ж самі дії повторіть, але з іншим файлом через команди в терміналі).

  - На фото відображена віртуальна машина з вже підключеною флешкою. Флешка підлкючена до самого комп'ютера. Також одразу було скопійовано файл з флешки на віртуальну машину
   ![image](https://github.com/user-attachments/assets/54c493ed-f612-4106-92a1-d52cf02a3bf3)

  - Далі йде встановлення монтування флешки до файлів віртуалки. Спочатку потрібно виконати команду `lsblk` для того, щоб дізнатися як ОС підключила флешку. Ми бачимо назву `sdb1` і робимо відподвіне монтування пристрою до новоствореної папки.
  
    ![image](https://github.com/user-attachments/assets/1ee5d0f4-d32e-4863-a018-1b6c233f8270)
  
  - Далі просто перевіряємо чи правильно у нас під'єдналась флешка, та копіюємо з неї довільний файл в теку :)

    ![image](https://github.com/user-attachments/assets/95774fb8-de97-4368-b02b-119ae4b07d7a)
 
