
<div
 align="center">
  <img src="https://github.com/user-attachments/assets/dcdd0d7c-164c-4a93-a6d8-84b6015c07aa" alt="exolutioneast">
</div>
<div align="center">

### **Київський фаховий коледж зв’язку**  
### *Циклова комісія комп’ютерної та програмної інженерії*  

<br/><br/><br/><br/>


### **ЗВІТ ПО ВИКОНАННЮ** 
### **ЛАБОРАТОРНОЇ РОБОТИ №2**  
### *з дисципліни: «Операційні системи»*  

  
### **Тема:** *«Ознайомлення з робочим середовищем віртуальних машин та операційних систем різних сімейств»*  

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
1. Знайомство з гіпервізорами різного типу, віртуалізацією при роботі з операційними системами.
2.  Знайомство з основними видами сучасних ОС, короткий огляд їх можливостей.


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

### 1. Прочитайте короткі теоретичні відомості до лабораторної роботи та зробіть невеликий словник базових англійських термінів з питань призначення команд та їх параметрів.


| English Term              | Український Термін                         |
|---------------------------|-------------------------------------------|
| Command Line Interface (CLI) | Командний інтерфейс (CLI)               |
| Terminal                  | Термінал                                  |
| Virtual Terminal          | Віртуальний термінал                      |
| Kernel                    | Ядро                                      |
| Application               | Додаток / Програма                        |
| API (Application Programming Interface) | API (Інтерфейс програмування додатків) |
| Process                   | Процес                                    |
| Multitasking              | Багатозадачність                          |
| Resource Allocation       | Розподіл ресурсів                         |
| Parsing Scripts           | Обробка скриптів                          |


### 4. Definitions  

- **CLI Mode (Command Line Interface Mode)**  
  A mode of interaction with the operating system where users enter text-based commands to perform tasks instead of using a graphical user interface. It allows direct control over the system through typed commands.  

- **Graphical User Interface-Based Terminal**  
  A terminal emulator that runs within a graphical environment, allowing users to interact with the command line through a windowed application. Examples include GNOME Terminal, Windows Command Prompt, and macOS Terminal.  

- **Virtual Terminal**  
  A text-based terminal session that runs independently of the graphical user interface. It provides direct access to the system and requires user login before executing commands. Virtual terminals can be accessed using key combinations like <kbd>Ctrl + Alt + F1</kbd> to <kbd>Ctrl + Alt + F6</kbd> on Linux systems.  


---

## Хід роботи  
>[!IMPORTANT]
>

1. ### Робота в графічному режимі в ОС сімейства Linux (робота з інтернет-джерелами):
- Оберіть графічну оболонку для ОС сімейства Linux, яку  ви хочете розглянути (в 401 ауд. це Gnome). Розгляньте структуру робочого простору користувача, та опишіть основні його компоненти:
  - Основне меню
  - Панелі швидкого доступу
  - Пошук 
  - Доступ до нових робочих столів тощо
- Запуск програм. Дослідіть можливості запуску додатків різними способами (описати спосіб і по-можливості показати скріншоти):
  - Запуск програм через панель швидкого запуску
  - Запуск програм через пошук в меню / глобальне меню 
  - Запуск програм через віджет запуску 
- Вихід з системи та завершення роботи в Linux. Як виконати в графічному інтерфейсі наступні дії (наведіть скріни)
  - Зміна користувача на root 
  - Перезавантаження системи
  - Вимкнення системи
2. Робота в середовищі мобільної ОС.
- Опишіть головне меню вашої мобільної ОС, який графічний інтерфейс вона використовує?
- Опишіть меню налаштувань компонентів мобільного телефону.
- Використання комбінацій клавіш для виконання спеціальних дій.
- Вхід у систему та завершення роботи пристрою. Особливості налаштувань живлення батареї.

---

### Відповіді на контрольні запитання  
>[!IMPORTANT]
>![made-by-borsuk-maksym](https://github.com/user-attachments/assets/68d0a6b6-134b-4446-a841-61b9dc7c958b)

## 1. Наведіть приклади серверних додатків Linux для сервера баз даних, серверів розсилки повідомлень та файлообмінників.

- **Database server**: MySQL, PostgreSQL, MariaDB
- **Mail server**: Postfix, Sendmail, Exim
- **File server**: Samba, NFS, FTP servers (vsftpd, proftpd)

### 2. Порівняйте оболонки Bourne, C, Bourne Again (Bash), the tcsh, Korn shell (Ksh) та zsh.

- **Bourne Shell (sh)**: Simple and reliable but lacks some advanced features.
- **C Shell (csh)**: Syntax similar to C programming language, supports job control.
- **Bash (Bourne Again Shell)**: Most popular, supports advanced features like command history, scripting.
- **tcsh**: An improved version of C shell with better features like command-line editing.
- **Ksh**: Similar to Bash, but with some unique features for scripting.
- **zsh**: Highly customizable, features advanced autocompletion and improved globbing.

### 3. Для чого потрібен менеджер пакетів? Які менеджери пакетів ви знаєте у Linux?

A package manager is used to install, update, remove, and manage software packages on a Linux system. It simplifies software management by handling dependencies and package versions.  
Known package managers:  
- **Debian/Ubuntu**: APT  
- **Red Hat/CentOS**: YUM/DNF  
- **Arch**: Pacman  
- **SUSE**: Zypper  

### 4. Які засоби безпеки використовуються в Linux?

- **Firewall**: iptables, firewalld  
- **AppArmor/SELinux**: Mandatory access control systems  
- **SSH key-based authentication**  
- **Rootkit detection tools**: rkhunter, chkrootkit  

### 5. Чому використання віртуалізації зараз стало таким актуальним?

Virtualization allows better resource utilization, isolation, and scalability. It's used to run multiple OSes on a single hardware, making it easier to manage different environments, especially for cloud services and testing.

### 6. Як ви розумієте поняття контейнеризації?

Containerization is about running applications in isolated environments called containers. These containers share the same OS kernel but have their own filesystem, which makes them lightweight and portable.

### 7. Які переваги/недоліки використання програмного забезпечення з відкритим кодом?

**Advantages**:
- Free and open for modification
- Active community support
- Transparency

**Disadvantages**:
- May lack user-friendly interfaces
- Less commercial support

### 8. Скільки активних віртуальних консолей (терміналів) може бути у процесі роботи Linux по замовчуванню. Як їх викликати та між ними перемикатися? Наведіть приклади?

By default, Linux has 6 active virtual consoles. You can switch between them using <kbd>Ctrl + Alt + F1</kbd> to <kbd>Ctrl + Alt + F6</kbd>. To return to the GUI, use <kbd>Ctrl + Alt + F7</kbd>.

### 9. Яка віртуальна консоль (термінал) виконує функцію графічної оболонки?

The graphical shell typically runs on **tty7** (or tty1 in some systems).

### 10. Чи можлива реєстрація в системі Linux декілька разів під одним і тим же системним ім’ям? Які переваги це може надати?

Yes, it's possible to log in multiple times under the same username. This allows multiple sessions, which can be useful for multitasking or running different processes in parallel without logging out.



---

>[!IMPORTANT]
> 1

## Висновки  
