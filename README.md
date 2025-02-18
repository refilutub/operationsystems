
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
1. Знайомство з базовими командами CLI-режиму в Linux.
2. Знайомство з базовими текстовими командами в термінальному режимі роботи в різних ОС.


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
| Англійською              | Українською                                                   |
|--------------------------|---------------------------------------------------------------|
| Command Line Interface (CLI) | Інтерфейс командного рядка                                    |
| The Shell                | Оболонка (Командний інтерпретатор)                            |
| Command                  | Команда                                                       |
| Option                   | Опція                                                         |
| Argument                 | Аргумент                                                      |
| Command History          | Історія команд                                                |
| Inline Editing           | Вбудоване редагування                                          |
| Scripting                | Скриптування                                                   |
| Alias                    | Псевдонім (коротке ім'я для довших команд)                    |
| Variable                 | Змінна                                                        |
| Prompt                   | Підказка (Запрошення до введення команди)                     |
| Internal Command         | Вбудована команда                                             |
| External Command         | Зовнішня команда                                              |
| Function                 | Функція                                                       |
| Quotation Marks          | Кавычки                                                       |
| Control Statement        | Контрольна інструкція                                         |
| Semicolon (;)            | Точка з комою                                                 |
| Double Ampersand (&&)    | Подвійний амперсанд (логічне "І")                              |
| Double Pipe (||)         | Подвійний пайп (логічне "АБО")                                 |

### 4. Терміни:

1. **Command Interpreter**:  
   A program that processes and interprets commands entered by the user in a command-line interface (CLI), executing them on the operating system.

2. **Shell**:  
   A user interface that allows interaction with the operating system through command-line instructions. It acts as a command interpreter, translating user commands into actions performed by the system.

3. **Command**:  
   A specific instruction or program executed by the command-line interface (CLI) to perform a particular action, such as listing files, navigating directories, or managing system resources.

### 5. Відповіді на питання:

1. **What basic information does the prompt line provide?**  
   The prompt typically provides the following basic information:  
   - **Username**: The user currently logged into the system.  
   - **System name**: The name of the system or host.  
   - **Current Directory**: The directory the user is currently in.  
   This information helps users quickly identify their environment and the current location in the file system.

2. **Why does a command need parameters and arguments?**  
   - **Parameters** modify the behavior of the command, allowing for more specific functionality (e.g., display output in a different format).  
   - **Arguments** provide necessary additional information that the command acts upon (e.g., filenames, directory names, or other input data).

3. **What is the purpose of the `ls` command, and what parameters and arguments can it have? Provide 3 examples.**  
   The `ls` command is used to list the contents of a directory.  
   - **Parameters** modify the output format (e.g., `-l` for a long listing).  
   - **Arguments** specify the directories or files to list.  
   
   Examples:  
   - `ls` – Lists contents of the current directory.  
   - `ls -l` – Provides a detailed listing of files (permissions, ownership, size, etc.).  
   - `ls /home/user` – Lists the contents of the `/home/user` directory.

4. **How can you use the command history, and what advantages does it provide?**  
   The command history allows users to access previously entered commands using the arrow keys or the `history` command. This saves time by avoiding the need to retype long or complex commands, improving workflow efficiency.

5. **What is the purpose of the `echo` command?**  
   The `echo` command is used to display a line of text or variable content in the terminal. It is commonly used for printing output, debugging, or setting values in scripts.

6. **What is a variable in the Bash shell, and what types of variables does it support?**  
   A variable is a container that stores data that can be used within commands or scripts. There are two types of variables in Bash:  
   - **Local variables**: Defined within a script or function, only accessible in the scope where they are defined.  
   - **Environment variables**: Available to all programs and processes in the system.

7. **What is the purpose of the `env`, `export`, and `unset` commands?**  
   - `env` – Displays the current environment variables.  
   - `export` – Sets environment variables, making them available to child processes.  
   - `unset` – Removes a variable or function.

8. **Which commands can be used to get help about commands in the terminal?**  
   - `man <command>` – Displays the manual page for the specified command.  
   - `info <command>` – Displays detailed information about the command.  
   - `--help` – A common option for most commands that provides a quick reference about their usage (e.g., `ls --help`).



---

## Хід роботи  
>[!IMPORTANT]
>![made-by-borsuk-maksym](https://github.com/user-attachments/assets/68d0a6b6-134b-4446-a841-61b9dc7c958b)

## 1. Опрацюйте всі приклади команд, що представлені у лабораторній роботі курсу NDG Linux Essentials - Lab 5: Command Line Skills та Lab 6: Getting Help. Створіть таблицю для опису цих команд
| **Command**        | **Purpose and Functionality**                                                                 |
|--------------------|---------------------------------------------------------------------------------------------|
| `ls`               | Lists files and directories in the current working directory.                               |
| `ls -l`            | Lists files and directories in long format, displaying additional file information.         |
| `ls -l /home`      | Lists files and directories in long format in the specified directory.                      |
| `whoami`           | Displays the current user’s username.                                                       |
| `uname`            | Displays basic information about the system (e.g., kernel name).                            |
| `uname -n`         | Displays the network node hostname.                                                         |
| `uname --nodename` | Displays the network node hostname (same as `-n` option).                                   |
| `pwd`              | Prints the current working directory.                                                       |
| `history`          | Displays the list of recently executed commands.                                            |
| `history 5`        | Displays the last 5 commands from the history list.                                          |
| `!9`               | Executes the command listed at position 9 in the history list.                              |
| `echo`             | Prints text or the value of variables to the terminal.                                      |
| `echo $PATH`       | Displays the value of the PATH environment variable.                                        |
| `which`            | Shows the full path of an executable program.                                               |
| `type`             | Displays information about a command's type (e.g., internal or external).                  |
| `which ls`         | Shows the path to the `ls` command.                                                         |
| `type -a ls`       | Displays all locations of the `ls` command, including any aliases.                         |
| `alias`            | Displays all aliases currently set in the shell.                                            |
| `cd`               | Changes the current directory.                                                              |
| `type vi`          | Displays information about the command `vi`.                                               |
| `cd /bin`          | Changes the current directory to `/bin`.                                                    |
| `cd`               | Returns to the home directory.                                                              |
| `echo 'Hello'`     | Prints the text 'Hello', using single quotes to prevent shell expansion.                   |
| `echo "Hello"`     | Prints the text 'Hello', using double quotes for possible variable expansion.               |
| `echo \*`          | Prints the literal asterisk `*`, escaping its special meaning.                              |
| `type vlc`         | Displays information about the command `vlc`.                                               |
| `type cp`          | Shows the type of the `cp` command (usually external).                                      |
| `date`                      | Displays the current date and time.                                                  |
| `man`                       | Opens the manual page for a given command, providing details on how to use it. Example: `man date` opens the manual for the `date` command. |
| `less`                      | A pager program used to view the output of `man` and other commands. You can navigate through it using various keys like space, arrow keys, etc. |
| `h`                         | Shows the help for navigation within the `less` command.                              |
| `q`                         | Exits the `less` pager and returns to the terminal prompt.                           |
| `Spacebar`, `f`, `PageDown` | Scrolls forward one page in the `less` viewer.                                       |
| `b`, `PageUp`               | Scrolls backward one page in the `less` viewer.                                      |
| `Enter`, `down arrow`       | Moves down one line in the `less` viewer.                                            |
| `Up arrow`                  | Moves up one line in the `less` viewer.                                              |
| `/ followed by text`        | Starts a forward search within the `less` viewer. For example, `/file` searches for the word "file". |
| `? followed by text`        | Starts a backward search within the `less` viewer.                                   |
| `n`                         | Moves to the next match of the search term in `less`.                                |
| `N`                         | Moves to the previous match of the search term in `less`.                            |
| `man -k`                    | Searches for all `man` pages that match a specific keyword. Example: `man -k password` shows `man` pages related to "password". |
| `apropos`                   | Another command to search for `man` page summaries based on a keyword. Example: `apropos password`. |
| `man -f`                    | Displays the sections for a given command, showing all `man` pages for a command or keyword. Example: `man -f passwd` lists all the `man` pages for "passwd". |
| `whatis`                    | Displays a short description of a command. Example: `whatis passwd` shows a summary of the `passwd` command. |
| `info`                      | Displays info pages, which are more detailed than `man` pages. Example: `info date` displays detailed information about the `date` command. |
| `-r`, `--reference=FILE`    | Used with `date` to display the last modification time of a specified file.         |
| `-R`, `--rfc-2822`          | Outputs the date and time in RFC 2822 format, often used in email headers.          |
| `--rfc-3339=TIMESPEC`       | Outputs date and time in RFC 3339 format with a specified level of precision (e.g., seconds or nanoseconds). |
| `-s`, `--set=STRING`        | Used to set the system date and time to a specified string.                          |
| `-u`, `--utc`, `--universal`| Prints or sets the Coordinated Universal Time (UTC) instead of the local time zone. |
| `--help`                    | Displays help information for a command. Example: `date --help`.                     |

## 2. Робота в в терміналі (закріплення практичних навичок) обов'язково представити свої скріншоти:

<details>
 <summary><h3>Робота зі змінними (Variables) та псевдонімами (Aliases) в терміналі</h3></summary>
 <div>
 <img src="assets/1varname.jpg">
 <img src="assets/1alias.jpg">
 <img src="assets/1cal.jpg">
</div>
</details>

<details>
 <summary><h3>Робота з функціями (Functions) в терміналі</h3></summary>
 <div>
 <img src="assets/2studentsreport.jpg">
</div>
</details>

<details>
 <summary><h3>Робота з лапками (Quoting) в терміналі.</h3></summary>
 <div>
 <img src="assets/3calendar.jpg">
</div>
</details>

<details>
 <summary><h3>Робота з інструкціями керування (Control Statements) в термінал</h3></summary>
 <div>
 <img src="assets/isit.jpg">
</div>
</details>

<details>
 <summary><h3>Робота з командами довідки (Man Pages) в терміналі</h3></summary>
 <div>
 <img src="assets/uname.jpg">
</div>
</details>

---

### Відповіді на контрольні запитання  
>[!IMPORTANT]
> 

---

## Висновки  

>[!IMPORTANT]
> 1
