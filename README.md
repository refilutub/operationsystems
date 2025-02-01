
<div
 align="center">
  <img src="https://github.com/user-attachments/assets/dcdd0d7c-164c-4a93-a6d8-84b6015c07aa" alt="exolutioneast">
</div>
<div align="center">

### **Київський фаховий коледж зв’язку**  
### *Циклова комісія комп’ютерної та програмної інженерії*  

<br/><br/><br/><br/>


### **ЗВІТ ПО ВИКОНАННЮ** 
### **ЛАБОРАТОРНОЇ РОБОТИ №4**  
### *з дисципліни: «Операційні системи»*  

  
### **Тема:** *«Команди Linux для управління процесами»*  

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
1. Отримання практичних навиків роботи з командною оболонкою Bash.
2. Знайомство з базовими командами для управління процесами.

---

## Матеріальне забезпечення занять  
1. ЕОМ типу IBM PC.
2. ОС сімейства Windows та віртуальна машина Virtual Box (Oracle).
3. ОС GNU/Linux (будь-який дистрибутив).
4. Сайт мережевої академії Cisco netacad.com та його онлайн курси по Linux


---

## Завдання для попередньої підготовки  
>[!IMPORTANT]
>![made-by-borsuk-maksym](https://github.com/user-attachments/assets/68d0a6b6-134b-4446-a841-61b9dc7c958b)

# Словник термінів для роботи з командами та параметрами

| Англійський термін       | Український переклад / Опис                                                                 |
|--------------------------|--------------------------------------------------------------------------------------------|
| **Process**              | Програма, яка виконується на системі.                                                       |
| **ps command**           | Утиліта для перегляду інформації про процеси.                                               |
| **PID**                  | Унікальний номер процесу.                                                                  |
| **TTY**                  | Пристрій, з якого запущено процес.                                                         |
| **CPU time**             | Час, витрачений процесом на виконання.                                                     |
| **Unix-style parameters**| Параметри з дефісом, наприклад, `-e`.                                                       |
| **BSD-style parameters** | Параметри без дефісу, наприклад, `a`.                                                      |
| **GNU long parameters**  | Довгі параметри з подвійним дефісом, наприклад, `--help`.                                   |
| **-A**                   | Показує всі процеси.                                                                        |
| **-e**                   | Показує всі процеси (аналогічно `-A`).                                                      |
| **-f**                   | Виводить повну інформацію про процеси.                                                     |
| **-l**                   | Виводить довгий список інформації про процеси.                                             |
| **-u userlist**          | Показує процеси, які належать користувачам зі списку `userlist`.                            |
| **-p pidlist**           | Показує процеси з певними PID зі списку `pidlist`.                                          |
| **UID**                  | Власник процесу.                                                                            |
| **PPID**                 | Ідентифікатор батьківського процесу.                                                      |
| **STIME**                | Час запуску процесу.                                                                        |
| **CMD**                  | Назва програми, яка запустила процес.                                                     |
| **F**                    | Прапори системи, призначені ядром для процесу.                                            |
| **S**                    | Стан процесу (наприклад, R = виконується, S = спить, Z = зомбі).                           |
| **PRI**                  | Пріоритет процесу (чим вище число, тим нижчий пріоритет).                                  |
| **NI**                   | Значення "nice" - впливає на пріоритет процесу.                                           |
| **SZ**                   | Розмір пам'яті, який займає процес.                                                        |
| **WCHAN**                | Адреса функції ядра, де процес "спить".                                                    |
| **top command**          | Інструмент для моніторингу процесів у реальному часі.                                      |
| **Load average**         | Середнє навантаження системи (1, 5, 15 хвилин).                                            |
| **VIRT**                 | Загальний обсяг пам'яті, який використовує процес.                                          |
| **RES**                  | Обсяг оперативної пам'яті, який використовує процес.                                       |
| **SHR**                  | Обсяг пам'яті, який процес ділить з іншими процесами.                                      |
| **%CPU**                 | Частка процесорного часу, яку використовує процес.                                         |
| **%MEM**                 | Частка фізичної пам'яті, яку використовує процес.                                          |
| **TIME+**                | Загальний час CPU, використаний процесом з моменту запуску.                               |
| **kill command**         | Надсилає сигнали процесам за їх PID.                                                       |
| **killall command**      | Зупиняє процеси за їх іменами.                                                              |
| **Signal**               | Повідомлення, яке надсилається процесу для керування його роботою.                         |
| **HUP (1)**              | Перезавантажує процес.                                                                    |
| **INT (2)**              | Перериває процес.                                                                           |
| **KILL (9)**             | Примусово завершує процес.                                                                 |
| **TERM (15)**            | Просить процес завершитися.                                                               |
| **STOP (17)**            | Призупиняє виконання процесу.                                                              |
| **CONT (19)**            | Продовжує виконання призупиненого процесу.                                                 |

## Answers to the Questions

### 2.1. Commands for Monitoring Process Status
To check what processes are running on a Linux system, the `ps` command is commonly used. It provides details about active processes and allows filtering with different options. Some useful parameters are:
- `-A`: Show all processes
- `-e`: Display all running processes
- `-u userlist`: Filter processes by user
- `-F`: Show detailed output
- `-l`: Show extended listing format
- `-H`: Show processes in a tree format

To see all available options, use:
```sh
man ps
```
or:
```sh
ps --help
```

### 2.2. Real-time Process Monitoring with `ps`
The `ps` command provides a one-time snapshot of running processes, meaning it does not update in real-time. If you need continuous monitoring, use the `top` command.

### 2.3. Sorting Processes in `top`
The `top` command sorts processes dynamically, usually by CPU usage. You can change sorting by pressing:
- `P`: Sort by CPU usage
- `M`: Sort by memory usage
- `T`: Sort by total CPU time used
- `N`: Sort by process ID (PID)
- `f`: Customize displayed fields and sorting

To change the update interval, press `d`. To exit `top`, press `q`.

### 2.4. Commands for Stopping Processes
If a process becomes unresponsive or consumes too many resources, you can stop it using these commands:

1. **kill**: Stop a process using its PID.
   ```sh
   kill 3940  # Sends a request to terminate the process
   kill -9 3940  # Forces termination
   ```
2. **killall**: Stop all instances of a process by name.
   ```sh
   killall firefox  # Kills all Firefox processes
   killall -9 chrome  # Forcefully stops all Chrome processes
   ```
3. **pkill**: Kill processes based on name or pattern.
   ```sh
   pkill -f apache  # Stops any process matching "apache"
   ```
4. **htop**: An interactive tool to manage processes.
   - Use arrow keys to select a process
   - Press `F9`, then choose a termination signal

These tools help keep system performance stable and allow easy management of running applications.




---

## Хід роботи  
>[!IMPORTANT]
>![made-by-borsuk-maksym](https://github.com/user-attachments/assets/68d0a6b6-134b-4446-a841-61b9dc7c958b)

1. **Як вивести вміст директорії /proc? Де вона знаходиться та для чого призначена? Охарактеризуйте інформацію про її вміст?**

   The `/proc` directory is a virtual filesystem located in the root directory (`/`). It provides a mechanism for the kernel to communicate information about the system to user space. The contents of this directory represent runtime system information such as system memory, devices, processes, and kernel parameters. The data in `/proc` is not stored on disk but generated in real-time by the kernel.

   To view its contents, you can use the `ls` command:
   ```
   ls /proc
   ```

   Some of the notable entries include:
   - `/proc/cpuinfo`: Information about the processor.
   - `/proc/meminfo`: Information about system memory usage.
   - `/proc/uptime`: The system's uptime and idle time.
   - `/proc/[pid]`: Directories for each running process, where `[pid]` is the process ID.

2. **Як вивести інформацію про поточні сеанси користувачів. Якою командою це можна зробити?**

   To display information about the current user sessions, you can use the `w` or `who` command. These commands show who is logged in and what they are doing.
   
   Example:
   ```
   w
   ```

   or
   
   ```
   who
   ```

3. **Які дії можна зробити в терміналі за допомогою комбінацій <kbd>Ctrl + C</kbd>, <kbd>Ctrl + D</kbd> та <kbd>Ctrl + Z</kbd>?**

   - <kbd>**Ctrl + C**</kbd>: Terminates the current running process.
   - <kbd>**Ctrl + D**</kbd>: Logs out of the current shell or closes the terminal window.
   - <kbd>**Ctrl + Z**</kbd>: Suspends the currently running process and puts it in the background.

4. **Чим відрізняється фоновий процес від звичайного. Де вони використовуються?**

   A foreground process is one that runs in the terminal and occupies it until it finishes. You interact with it directly. A background process, on the other hand, runs without occupying the terminal, allowing you to continue using the terminal for other tasks. Background processes are often used for long-running tasks that don’t require user interaction.

   You can move a process to the background by appending `&` when running a command or by suspending it with <kbd>Ctrl + Z</kbd> and then using the `bg` command.

5. **Опишіть наступні команди та поясніть що вони виконують – команда jobs, bg, fg.**

   - **jobs**: Displays the list of jobs running in the background, along with their job IDs and statuses.
     ```
     jobs
     ```

   - **bg**: Resumes a suspended job in the background, allowing it to continue running while the terminal is free for other tasks.
     ```
     bg %1  # %1 is the job ID
     ```

   - **fg**: Brings a background job into the foreground, making it the active process in the terminal.
     ```
     fg %1  # %1 is the job ID
     ```

6. **Якою командою можна переглянути інформацію про запущені в системи фонові процеси та задачі?**

   The `ps` command can be used to view information about running background processes and tasks in the system. You can combine it with the `aux` option for detailed information.

   Example:
   ```
   ps aux
   ```

7. **Як призупинити фоновий процес, як його потім відновити та при необхідності перезапусти?**

   - To suspend a background process, use <kbd>Ctrl + Z</kbd> or the `kill -STOP <pid>` command, where `<pid>` is the process ID.
   - To resume it in the background, use the `bg` command with the job ID or PID.
   - To restart a process, you can stop it and then run the command again in the background or foreground.
     ```
     kill -STOP <pid>  
     bg %1             
     kill -CONT <pid>  
     ```


1. **запустіть команду top, проаналізуйте отриманий в цій команді результат та охарактеризуйте найбільш активні процеси у системі**

   To run the `top` command, simply type:
   ```
   top
   ```
   This will display a dynamic, real-time list of processes. The most active processes typically consume the most CPU and memory resources. Look for processes with high `%CPU` and `%MEM` values, as these are the ones consuming the most resources. For example, a process like a web server or a database server might be highly active, using significant CPU and memory.
   

3. **Призупинити виконання команди top (треба використати комбінацію клавіш)**

   To stop the execution of `top`, press
   <kbd>Ctrl + C</kbd>
   This will terminate the `top` command and return you to the shell prompt.

4. **вивести інформацію про процеси за допомогою команди ps;**

   To view a snapshot of current processes, use:
   ```
   ps
   ```
   This will display a list of processes running in your session, showing their PID (Process ID), TTY (terminal type), and command that started them.

5. **наведіть 5 прикладів з використанням різних параметрів команди ps (наприклад, вивести тільки системні процеси, вивести процеси конкретного користувача, вивести дерево процесів тощо). Опишіть, що саме роблять обрані Вами параметри**

   - **`ps aux`**: Shows all processes running on the system, along with detailed information like CPU and memory usage, user, and more.
     ```
     ps aux
     ```
   
   - **`ps -u <username>`**: Displays processes running by a specific user.
     ```
     ps -u username
     ```
   
   - **`ps -e`**: Displays all running processes on the system, similar to `ps aux`, but with less detail.
     ```
     ps -e
     ```
   
   - **`ps -f`**: Shows processes in a full-format listing, providing additional details like the parent process ID (PPID).
     ```
     ps -f
     ```
   
   - **`ps --forest`**: Displays processes in a tree-like structure to visualize parent-child relationships between processes.
     ```
     ps --forest
     ```

6. **Передивіться чи є у Вас запущені фонові процеси, які саме?**

   To check for background processes, use the `jobs` command:
   ```
   jobs
   ```
   This will list the background jobs in your current terminal session, showing their job ID and status.

7. **Відновити виконання призупиненого фонового процесу спочатку у позиції “на передньому плані” (foreground), потім ще раз його призупинити, а потім відновити його виконання у позиції “на задньому плані” (background)**

   - To bring a background process to the foreground, use:
     ```
     fg %1
     ```

   - To suspend a process running in the foreground, press:
     <kbd>Ctrl + Z</kbd>
     

   - To move the suspended process back to the background, use:
     ```
     bg %1
     ```

8. **Завершити роботу даного фонового процесу.**

   To kill the background process, use:
   ```
   kill %1
   ```
   Or, if you know the process ID, you can also use:
   ```
   kill <pid>
   ```
   This will terminate the specified process.

---

### Відповіді на контрольні запитання  
>[!IMPORTANT]
> 1

---

## Висновки  

>[!IMPORTANT]
> 1
