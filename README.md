
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
>Made by Didusenko Didusenko

1. ### Робота в графічному режимі в ОС сімейства Linux (робота з інтернет-джерелами):
- Оберіть графічну оболонку для ОС сімейства Linux, яку  ви хочете розглянути (**Розглядаємо графічну оболонку GNOME**). Розгляньте структуру робочого простору користувача, та опишіть основні його компоненти:  
  - Основне меню
  - Панелі швидкого доступу
  - Пошук 
  - Доступ до нових робочих столів тощо

Основні компоненти робочого простору GNOME

**Основне меню ("Activities" / "Діяльність")**   
Основне меню в GNOME розташоване у верхньому лівому куті екрану й активується натисканням на кнопку "Діяльність" (Activities) або натисканням клавіші Super (Windows key).  
 У меню містяться:
  - Огляд відкритих вікон та віртуальних робочих столів
  - Поле пошуку для швидкого доступу до програм та файлів
  - Список часто використовуваних та запущених програм

**Панель швидкого доступу (Top Bar)**  
Верхня панель (Top Bar) виконує кілька функцій:
       - Відображення поточного часу та дати
       - Іконки системного стану (Wi-Fi, звук, батарея тощо)
       - Меню користувача (вихід, налаштування, блокування екрану)
       - Кнопка "Діяльність", яка відкриває огляд робочого простору

**Пошук**  
Функція пошуку активується при відкритті меню "Діяльність" або введенні тексту після натискання Super. Вона дозволяє знаходити:
       - Програми
       - Файли та папки
       - Системні параметри
       - Веб-результати (залежно від налаштувань)

**Доступ до нових робочих столів (Virtual Desktops / Workspaces)**   
    GNOME підтримує віртуальні робочі столи, які допомагають організувати роботу з великою кількістю вікон.
       - Відкрити список доступних робочих столів можна через меню "Діяльність"
       - Новий стіл створюється автоматично при перетягуванні вікна на вільний робочий простір
       - Перемикання між столами можливе за допомогою жестів, гарячих клавіш або миші

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

Android – це мобільна операційна система, що використовує графічний інтерфейс на основі GUI (Graphical User Interface). Інтерфейс Android побудований на основі Material Design, який розробила компанія Google. Він відрізняється плавними анімаціями, простими іконками та зручним доступом до всіх функцій.
Головне меню Android

Головне меню Android – це екран програм, де знаходяться всі встановлені додатки. Воно може бути представлено у двох варіантах:

   - Класичний стільничний режим – всі іконки програм розташовані безпосередньо на робочих столах.
   - Окреме меню програм – доступ до всіх додатків здійснюється через кнопку "Меню" або свайпом вгору з головного екрану.

Компоненти головного меню:

   - Панель швидкого доступу – містить основні додатки (телефон, камеру, браузер тощо).
   - Панель пошуку – використовується для швидкого знаходження додатків та файлів.
   - Віджети – інтерактивні елементи, такі як погода, годинник, замітки.
   - Папки – для групування додатків за категоріями.

Меню налаштувань компонентів мобільного телефону

Меню "Налаштування" (Settings) в Android надає доступ до всіх системних параметрів пристрою. Основні розділи:

  - Мережа та підключення
     - Wi-Fi, мобільний інтернет, Bluetooth, NFC
     - VPN та точка доступу

   - Пристрій
     - Налаштування дисплея, звуку, жестів, сповіщень
     - Підключення аксесуарів (навушники, смарт-годинники)

   - Особисті дані та безпека
     - Облікові записи Google, паролі, розпізнавання обличчя або відбитка пальця
     - Дозволи додатків та конфіденційність

   - Система
     - Оновлення Android
     - Резервне копіювання
     - Мова та введення

Використання комбінацій клавіш для виконання спеціальних дій

На Android-пристроях передбачені гарячі клавіші для виконання різних дій:

   - Знімок екрану – натискання Power + Зменшення гучності
   - Перезавантаження – довге утримання Power
   - Безпечний режим – при включенні пристрою утримувати кнопку зменшення гучності
   - Доступ до Google Асистента – довге натискання Home (кнопка або жест)
   - Режим розробника – 7 разів натиснути на "Номер збірки" у "Про телефон"

Вхід у систему та завершення роботи пристрою

   - Увімкнення пристрою
        - Натиснути і утримувати кнопку Power до появи логотипу.
        - Ввести PIN-код, графічний ключ або використати біометричну авторизацію.

   - Вимкнення пристрою
        - Натиснути та утримувати Power, потім вибрати "Вимкнути" або "Перезавантажити".

   - Блокування та розблокування екрану
        - Блокування – коротке натискання Power
        - Розблокування – свайп по екрану або біометричне розпізнавання

Особливості налаштувань живлення батареї

Android має розширені функції енергозбереження, щоб збільшити час автономної роботи:

   - Режим енергозбереження – обмежує фонові процеси та зменшує яскравість екрану.
   - Адаптивна батарея – система аналізує використання додатків і обмежує активність тих, що рідко використовуються.
   - Оптимізоване заряджання – зменшує зношення батареї, сповільнюючи зарядку після 80%.
   - Детальна статистика використання батареї – можна побачити, які додатки найбільше споживають енергію.

Завдяки цим функціям Android-пристрої можуть ефективно використовувати заряд батареї та працювати довше без підзарядки.

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
> This part made by Didusenko Oleksandr

## Висновки  
Ми успішно ознайомилися з принципами роботи віртуальних машин та особливостями різних операційних систем.Набули практичних навичок встановлення та налаштування віртуальних середовищ, а також базових команд в середовищі Linux.
