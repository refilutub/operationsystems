<div
 align="center">
  <img src="https://github.com/user-attachments/assets/dcdd0d7c-164c-4a93-a6d8-84b6015c07aa" alt="exolutioneast">
</div>
<div align="center">

### **Київський фаховий коледж зв’язку**  
### *Циклова комісія комп’ютерної та програмної інженерії*  

<br/><br/><br/><br/>


### **ЗВІТ ПО ВИКОНАННЮ** 
### **ЛАБОРАТОРНОЇ РОБОТИ №5**  
### *з дисципліни: «Операційні системи»*  

  
### **Тема:** *«Знайомство з командами навігації по файловій системі та керування файлами та каталогами»*  

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
2. Знайомство з базовими командами навігації по файловій системі.
3. Знайомство з базовими командами для керування файлами та каталогами.

---

## Матеріальне забезпечення занять  
1. ЕОМ типу IBM PC.
2. ОС сімейства Windows та віртуальна машина Virtual Box (Oracle).
3. ОС GNU/Linux (будь-який дистрибутив).
4. Сайт мережевої академії Cisco netacad.com та його онлайн курси по Linux


---

## Завдання для попередньої підготовки  
>[!IMPORTANT]
>This part made by Didusenko Oleksandr  
1. **Read the brief theoretical information before the lab and make a small glossary of basic English terms on the purpose of commands and their parameters. **
**Main commands: **  
ls – view the contents of the directory  
cd – directory change  
cp – used to copy files  
mv – move and rename file  
rm – used to delete a file  
mkdir – create new directory  
rmdir – deleting empty directory  
touch – create empty file  
2. **Based on the material reviewed, answer the following questions:**  
 2.1 **Compare the file structures of a Windows-like and a Linux-like system.**   

| **Feature**                 | **Windows**                                        | **Linux**                                   |
|-----------------------------|---------------------------------------------------|---------------------------------------------|
| **Root Directory**          | `My Computer` or `C:\`                           | `/` (root directory)                        |
| **Device Locations**        | Each device has a letter (`C:`, `D:` etc.)       | All devices are mounted in directories (`/mnt`, `/media`) |
| **User Home Directory**     | `C:\Users\Username\`                             | `/home/Username/`                           |
| **System Files**            | `C:\Windows\System32\`                           | `/bin`, `/sbin`, `/etc`                     |
| **Configuration Files**     | Windows Registry (`regedit`) and `.ini` files    | Text-based configuration files in `/etc`   |
| **Programs**                | `C:\Program Files\`, `C:\Program Files (x86)\`   | `/usr/bin/`, `/opt/`, `/usr/local/bin/`     |
| **Device Drivers**          | `C:\Windows\System32\Drivers\`                   | `/dev/` (virtual device files)             |
| **Logs (Event Logs)**       | `C:\Windows\System32\winevt\Logs\`               | `/var/log/`                                |
| **Temporary Files**         | `C:\Users\Username\AppData\Local\Temp\`          | `/tmp/`                                    |
| **File System**             | NTFS, FAT32, exFAT                               | ext4, XFS, Btrfs, ZFS                      |

 2.2 **Explain the concept of FHS. How is this standard used in the context of file systems?**  
**The Filesystem Hierarchy Standard (FHS)** - is a standard for file hierarchy in Unix-like operating systems such as Linux. It defines how directories and files are organized in an operating system to ensure consistency across different Linux distributions.  

The main goals of FHS:  
    **Consistency** - files and directories have the same location on all FHS-compliant systems.  
    **Compatibility** - software developed for one FHS-compliant system will work on other systems.  
    **Ease of administration** - administrators can easily find the files they need.  
 The FHS standard defines which directories must be present in the system and what they contain.  
 
 2.3 **List the basic commands for working with files and directories in Linux: create, move, copy, delete.**  

touch filename – Create an empty file.  
mkdir directory_name – Create a new directory.  
mv source destination – Move or rename a file/directory.  
cp source destination – Copy a file.  
rm filename – Delete a file.  
rm -r directory_name – Delete a directory and its contents.  
rmdir directory_name – Remove an empty directory.  

---

## Хід роботи  
>[!IMPORTANT]
>![made-by-borsuk-maksym](https://github.com/user-attachments/assets/68d0a6b6-134b-4446-a841-61b9dc7c958b)

2. Опрацюйте всі приклади команд, що представлені у лабораторних роботах курсу NDG Linux Essentials - Lab 7: Navigating the Filesystem та Lab 8: Managing Files and Directories. Створіть таблицю для опису цих
 команд

| **Команда**                        | **Опис команди**                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------|
| `pwd`                              | Показує поточну директорію                                                                       |
| `echo $HOME`                       | Показує шлях домашньої директорії поточного користувача                                          |
| `cd /`                             | Переходить до кореневої директорії (`/`)                                                         |
| `pwd`                              | Показує поточну директорію (тепер `/`)                                                           |
| `cd`                               | Переходить до домашньої директорії поточного користувача                                         |
| `pwd`                              | Показує поточну директорію (домашня)                                                             |
| `cd /home`                         | Переходить у директорію `/home`                                                                  |
| `pwd`                              | Показує поточну директорію (`/home`)                                                             |
| `cd ~`                             | Переходить у домашню директорію поточного користувача                                            |
| `pwd`                              | Показує домашню директорію користувача                                                            |
| `echo ~ ~sysadmin ~root ~mail ~nobody` | Показує домашні директорії користувачів sysadmin, root, mail, nobody                          |
| `cd ~root`                         | Переходить до домашньої директорії користувача `root`                                            |
| `cd /usr/bin`                      | Переходить у директорію `/usr/bin`                                                               |
| `pwd`                              | Показує `/usr/bin`                                                                               |
| `cd /usr`                          | Переходить у директорію `/usr`                                                                   |
| `pwd`                              | Показує `/usr`                                                                                   |
| `cd /usr/share/doc`                | Переходить у директорію `/usr/share/doc`                                                         |
| `pwd`                              | Показує `/usr/share/doc`                                                                         |
| `cd bash`                          | Переходить у піддиректорію `bash`                                                                |
| `pwd`                              | Показує `/usr/share/doc/bash`                                                                    |
| `cd ..`                            | Переходить на одну директорію вгору (`/usr/share/doc`)                                           |
| `pwd`                              | Показує `/usr/share/doc`                                                                         |
| `cd ../dict`                       | Переходить до директорії `/usr/share/dict`                                                       |
| `pwd`                              | Показує `/usr/share/dict`                                                                        |
| `cd`                               | Переходить у домашню директорію поточного користувача                                            |
| `ls`                               | Виводить список файлів і каталогів у поточній директорії                                         |
| `ls -a`                            | Виводить усі файли (включно з прихованими)                                                       |
| `ls -l /etc/hosts`                 | Виводить детальну інформацію про файл `/etc/hosts`                                               |
| `ls -R /etc/udev`                  | Виводить рекурсивно вміст каталогу `/etc/udev`                                                   |
| `ls -d /etc/s*`                    | Виводить тільки назви каталогів та файлів в `/etc`, що починаються на "s"                        |
| `ls -d /etc/????`                  | Виводить тільки імена файлів та каталогів в `/etc`, що складаються з рівно 4 символів            |
| `ls -d /etc/[abcd]*`               | Виводить файли та каталоги, що починаються з літер a, b, c або d в `/etc`                        |
| `echo *`                           | Показує усі файли та каталоги в поточній директорії                                              |
| `echo D*`                          | Виводить файли та каталоги, що починаються з літери "D"                                          |
| `echo P*`                          | Виводить файли та каталоги, що починаються з літери "P"                                          |
| `echo *s`                          | Виводить файли та каталоги, що закінчуються літерою "s"                                          |
| `echo D*n*s`                       | Виводить файли, що починаються на "D", мають "n" всередині та закінчуються на "s"                |
| `echo ??????`                      | Виводить імена файлів та каталогів рівно з 6 символів                                            |
| `echo D????????`                   | Виводить імена файлів та каталогів, що починаються з "D" та мають 8 символів загалом             |
| `echo ?????*s`                     | Виводить імена файлів та каталогів з не менше ніж 6 символами, що закінчуються на "s"            |
| `echo [DP]*`                       | Виводить файли та каталоги, що починаються на літери "D" або "P"                                 |
| `echo [!DP]*`                      | Виводить файли та каталоги, що не починаються з літер "D" або "P"                                |
| `echo [D-P]*`                      | Виводить файли та каталоги, що починаються з будь-яких літер від "D" до "P"                      |
| `echo [!D-P]*`                     | Виводить файли та каталоги, що не починаються на літери від "D" до "P"                           |
| `cp /etc/hosts hosts`              | Копіює файл `/etc/hosts` у поточну директорію під ім'ям `hosts`                                  |
| `rm hosts`                         | Видаляє файл `hosts`                                                                             |
| `cp -v /etc/hosts hosts`           | Копіює файл `/etc/hosts` у поточну директорію з повідомленням                                    |
| `cp -v /etc/hosts .`               | Копіює `/etc/hosts` у поточну директорію з повідомленням                                         |
| `cp -p /etc/hosts /home/sysadmin`  | Копіює файл, зберігаючи права доступу та мітки часу                                             |
| `cp -p /etc/hosts ~`               | Копіює файл з правами в домашню директорію                                                       |
| `cp hosts newname`                 | Копіює файл під новим іменем                                                                     |
| `mkdir Myetc`                      | Створює новий каталог `Myetc`                                                                    |
| `cp -R /etc/udev Myetc`            | Рекурсивно копіює каталог `/etc/udev` в каталог `Myetc`                                         |
| `touch premove`                    | Створює порожній файл `premove`                                                                  |
| `mv premove postmove`              | Перейменовує файл з `premove` на `postmove`                                                      |
| `rm postmove`                      | Видаляє файл `postmove`                                                                          |

3.
- Визначте ваш поточний каталог
  ```pwd``` 
![image](https://github.com/user-attachments/assets/3923c962-6f5e-4dc1-8851-4aa340b6ffe1)

- Перейдіть до кореневого каталогу та визначте Ваш поточний робочий каталог (дві команди);
``` cd ```
![image](https://github.com/user-attachments/assets/292fb02c-e220-4093-b40c-d36123aaa8ef)


- Перегляньте вміст поточного каталогу у довгому форматі (скористайтесь відповідним ключем команди ls);
``` ls -l```
  ![зображення](https://github.com/user-attachments/assets/9bfe8503-b2fa-4f21-bb0f-cdcb99625c9e)

- Перейдіть до каталогу /usr/share та визначте Ваш поточний робочий каталог (дві команди)
  ![зображення](https://github.com/user-attachments/assets/d8858ad9-6ec6-4aab-b1b2-ee575b1bc4d1)
``` cd /usr/share/ pwd```
- Перегляньте вміст поточного каталогу включаючи і приховані файли (hidden files) (скористайтесь відповідним ключем команди ls);
![зображення](https://github.com/user-attachments/assets/0669eb15-80f0-4dc5-97f9-dc1f7822c87a)
``` ls -la```
- *Перейдіть до каталогу /etc;
  ![зображення](https://github.com/user-attachments/assets/a4660579-21e0-45fc-a817-f7653410cfe4)
``` cd /etc```
- *Перегляньте вміст даного каталогу, але щоб виводило тільки назви файлів, що починаються з літери вашого імені;
![зображення](https://github.com/user-attachments/assets/8c702bf7-63b7-4da9-816a-e6f8b615a40f)
``` ls -d M*```
- *Перегляньте вміст даного каталогу, але щоб виводило тільки файли, назви яких складаються з 6 літер;
![зображення](https://github.com/user-attachments/assets/1eb27a63-7683-48d1-89f5-65675c9939c0)
``` ls -d ??????```
- **Перегляньте вміст даного каталогу, але щоб виводило тільки файли, назви яких закінчуються на літери ваших імен, наприклад якщо ваші імена Ivan, Anna, Maks, то вибірку робиму, щоб назви файлів закінчувались на літери [i,a,m];
![зображення](https://github.com/user-attachments/assets/694ac498-12b7-4a5d-9f1e-d941e4981cff)
``` ls -d *[mo]```
- **Перейдіть до домашнього каталогу поточного користувача та перегляньте його вміст у рекурсивному (зворотному до алфавітного) форматі (виконати цю дію через конвеєр команд);
![зображення](https://github.com/user-attachments/assets/b41896ca-3e6c-4bbb-a84e-ef9b2627f0fe)
``` cd ls -1R | sort -r```
- В поточній директорії створити директорію з назвою вашої групи;  
![зображення](https://github.com/user-attachments/assets/c34df9a7-5d44-43d0-88ac-33685c9c8c20)
```mkdir rpz23a```
- Переглянути оновлений вміст домашнього каталогу поточного користувача. Скористайтесь ключем -r команди ls, яку інформацію ви отримаєте?
![зображення](https://github.com/user-attachments/assets/220690ee-017d-45bb-9634-2d78ebc17a47)
```ls -r```
- Перейдіть у створену вами директорію з назвою Вашої групи та створіть у ній порожній файл lab5
![зображення](https://github.com/user-attachments/assets/06aba7ad-46cb-448d-83c7-12b5ae282397)
``` cd rpz23a touch lab5```
- Створити в даній директорії 3 директорії з прізвищами студентів вашої команди surname1, surname2, surname3 (команда mkdir мульти аргумента, тому всі три каталоги можна створити однією командою);
![зображення](https://github.com/user-attachments/assets/bb9608ad-1caf-4453-949d-894dfd339135)
``` mkdir borsuk didusenko```
- Перейдіть у перший підкаталог surname1 та створіть порожній файл з ім'ям першого студента name1;  
![зображення](https://github.com/user-attachments/assets/956b247e-c346-41c7-bcf7-88fd11981615)
``` cd borsuk touch maksym```
- За допомогою команди echo "Hello, my name is Name1" > name1 внесіть у цей файл дані про студента (символ > дозволяє вивід команди echo перенаправити одразу у файл name1;
![зображення](https://github.com/user-attachments/assets/25c2ad63-5820-410e-9c4e-cc225fa0203d)
``` echo "Hello, my name is Maksym" > maksym```
- Перегляньте вміст файлу name1 за допомогою команди cat name1 (має містити щойно введену Вами інформацію)
![зображення](https://github.com/user-attachments/assets/16db000e-2b68-46b2-86de-6de954e1ec34)
``` cat maksym```
- Зробіть копію першого файлу name1 та перейменуйте її у файл з другим ім'ям студенту Вашої команди name2;
![зображення](https://github.com/user-attachments/assets/4f84ab87-cef1-4008-9d35-0016c1a4fbc7)
``` cp maksym oleksandr```
- Перегляньте вміст каталогу, обидва файли мають з'явитися; 
![зображення](https://github.com/user-attachments/assets/4e4426ac-fa89-4e25-98b7-eb5d06a53e68)
``` ls```
- Перегляньте вміст другого файлу cat name2 (він має поки що містити повну копію вмісту файлу name1)  
![зображення](https://github.com/user-attachments/assets/77dc0c03-e9bf-43f5-9ea1-2e490d1312aa)
``` cat oleksandr```
- Замініть зміст файлу name2, щоб він містив відповідне ім'я другого студента за допомогою команди echo "Hello, my name is Name2" > name2
![зображення](https://github.com/user-attachments/assets/f602346c-b858-4167-87b9-d09e3663b6b3)
``` echo "Hello, my name is Oleksandr" > oleksandr```
- Перегляньте вміст другого файлу cat name2 (він вже має містити оновлену інформацію)
![зображення](https://github.com/user-attachments/assets/28df0fdf-7431-465c-b200-7a12c4ab34f9)
``` cat oleksndr```
- Перемістіть файл name2 у директорію surname2;
![зображення](https://github.com/user-attachments/assets/a3615903-2441-4387-b50c-a70b61d9e009)
``` mv oleksandr ../didusenko/```
Для виконання завдань цих пунктів у нас немає третього студента, але ми вловили суть як це створювати :D
- Зробіть копію першого файлу name1 та перейменуйте її у файл з третім ім'ям студенту Вашої команди name3;
- Перемістіть файл name3 у директорію surname3;
- Перейдіть до директорії  surname3;
- Перегляньте вміст третього файлу командою cat name3 (він має містити дані про другого студента)
- Замініть зміст файлу name3, щоб він містив відповідне ім'я третього студента за допомогою команди echo "Hello, my name is Name3" > name3
- Перегляньте вміст файлу за допомогою  cat name3 (він вже має містити оновлену інформацію) 

- Поверніться до домашнього каталогу користувача;
  ![зображення](https://github.com/user-attachments/assets/bca21d3e-b93b-466d-bd2c-49e520a76ef4)
``` cd```
- **Перегляньте вміст даного каталогу, але щоб виводило тільки Ваш підкаталог з назвою групи та весь його вміст (підкаталоги surname1, surname2, surname3 та файли name1, name2, name3) до того ж файли та катлоги були відкоремлені кольорами (скористайтесь відповідним ключем -R команди ls та не забудьте використати спеціальний glob-шаблон [імя каталогу])
![зображення](https://github.com/user-attachments/assets/e5515b77-440f-4327-a848-6b0ef4aad0c1)
``` ls -R --color=auto rpz23a```
5. Опишіть дії, які виконують команди для переміщення по системі каталогів:

Опис дій, які виконують зазначені команди для переміщення по системі каталогів:

| **Команда**      | **Опис дії**                                                  |
|------------------|----------------------------------------------------------------|
| `cd /`           | Переміщує користувача у **кореневий каталог системи** (`/`). Корінь є найвищою точкою в ієрархії директорій. |
| `cd /home`       | Переміщує користувача у каталог `/home`, де зазвичай розташовані домашні директорії усіх користувачів системи. |
| `cd ~`           | Переміщує користувача у його особистий домашній каталог (наприклад `/home/username`). Знак `~` є скороченням домашньої директорії поточного користувача. |
| `cd` (без аргумента) | Переміщує користувача у його домашній каталог. Еквівалент команди `cd ~`. |
| `cd ..`          | Переміщує користувача **на один рівень вгору**, тобто у батьківський каталог. |
| `cd ../..`       | Переміщує користувача **на два рівні вгору** відносно поточного каталогу. |
| `cd -`           | Переміщує користувача назад у попередній каталог, де він знаходився раніше. Це дозволяє швидко повернутися до останньої директорії. |

---

### Відповіді на контрольні запитання  
>[!IMPORTANT]
>This part made by Didusenko Oleksandr  
1.**How can I view the path to a user's home directory using the echo command? There are 2 ways, please see both examples in the terminal**  
echo $HOME
echo ~  
2.**Is it possible to view the contents of the root directory while in the user's home directory without going to the root directory? Demonstrate this on the command line.**  
ls /  
3.**How can I add information to an empty file in the terminal?**  
echo "This is a test" >> myfile.txt  
4.**How do I copy and delete an existing directory? Will there be a difference in commands if the directory is not empty at the same time?**  
If directory is empty:  
`rmdir myfolder`  
If directory have files:  
`rm -r myfolder`  
5.**In which of the following examples is the file moved, renamed, or both?
mv /work/tech/comp.png. /Desktop 
mv /work/tech/comp.png. /work/tech/my_car.png 
mv /work/tech/comp.png. /Desktop/computer.png**  
Moves a file to /Desktop while keeping its name:  
mv /work/tech/comp.png /Desktop
Rename the file , leaving it in the same directory.  
mv /work/tech/comp.png /work/tech/my_car.png  
Move and rename at the same time:  
mv /work/tech/comp.png /Desktop/computer.png
---

## Висновки  

>[!IMPORTANT]
> This part made by Didusenko Oleksandr

During the laboratory work, the basic commands for navigating the file system and managing files and directories in the Linux environment were considered. Practical skills of working in the Bash command shell were consolidated, including:  
    File system navigation - cd, pwd, ls commands allow you to navigate between directories and view their contents.
    Work with files - create (touch), browse (cat), edit (echo), copy (cp), move and rename (mv), and delete (rm).
    Work with directories - create (mkdir), delete (rmdir and rm -r), copy (cp -r).
    Globbing - using the characters *, ?, [] to work with groups of files.
    Understanding of FHS (Filesystem Hierarchy Standard) - a standard that defines the location of system files in Linux.

The acquired knowledge and skills allow you to work effectively with the command line in Linux, which is important for system administration, task automation, and working with server environments.

