## 1. Термінальні утиліти (Terminal Utilities)

При роботі з серверними системами або на комп’ютерах, що досить обмежені у ресурсах, досить часто графічну оболонку вимикають або взагалі не встановлюють. Іноді виникають задачі, які здається, що без графічної оболонки виконати не можливо, проте для ОС Linux це не так. Спробуйте через термінал виконати наступні дії та поясніть за допомогою яких команд (пакетів) їх можна виконати

### 1.1 Перегляд файлів та папок (File Manager in Terminal)

**Опис:** Використовуємо *file manager* у терміналі для навігації по файловій системі.

```bash
sudo apt update
sudo apt install -y ranger
ranger
```

![image](https://github.com/user-attachments/assets/df132499-cd6b-44fe-80c1-135b1af048cc)


---

### 1.2 Перегляд веб-сторінок (Web Browser in Terminal)

**Опис:** *Terminal web browser* дозволяє відкрити сайти без графічного інтерфейсу.

```bash
sudo apt install -y w3m
w3m https://www.google.com
```

![image](https://github.com/user-attachments/assets/370cf456-270c-4430-865a-e3431c79dbf2)


---

### 1.3 Перегляд електронної пошти (Email Client in Terminal)

**Опис:** Використовуємо *email client* у терміналі для читання та надсилання пошти.

```bash
sudo apt install -y mutt
mutt
```

![image](https://github.com/user-attachments/assets/a6d3f290-602f-4cda-9011-9838ff91855d)


---

### 1.4 Відтворення музики (Music Player in Terminal)

**Опис:** *Terminal music player* для прослуховування аудіофайлів.

```bash
sudo apt install -y cmus
cmus
```

Всередині `cmus`:

* <kbd>5</kbd> — Перехід до бібліотеки (Library)
* <kbd>Enter</kbd> — Відтворення вибраного файлу
* <kbd>q</kbd> — Вихід з програми

![image](https://github.com/user-attachments/assets/e8729b66-ee4b-43d5-9d19-af6de4807e68)


---

### 1.5 Завантаження торрентів (Torrent Client in Terminal)

**Опис:** *Terminal torrent client* для завантаження .torrent-файлів.

```bash
sudo apt install -y rtorrent
rtorrent
```

Всередині `rtorrent`:

* <kbd>Enter</kbd> на рядку з `.torrent` — Додавання трекера
* <kbd>Ctrl</kbd>+<kbd>q</kbd> — Вихід з програми

![image](https://github.com/user-attachments/assets/71c6bfa7-d595-4aa5-9e31-d758624cab59)


---

### 1.6 Планувальник подій (Calendar & Task Scheduler in Terminal)

**Опис:** *Calendar and task scheduler* у терміналі для планування подій і нагадувань.

```bash
sudo apt install -y calcurse
calcurse
```

Всередині `calcurse`:

* <kbd>a</kbd> — Додати подію (Add appointment)
* <kbd>C</kbd> — Перехід у календар (Calendar view)
* <kbd>h</kbd> — Виклик довідки (Help)

![image](https://github.com/user-attachments/assets/bf5fea7d-468a-4740-9109-ddc47af89788)


---

### 1.7 Перегляд зображень (Image Viewer in Terminal)

**Опис:** *Terminal image viewer* для перегляду графічних файлів в консолі.

```bash
sudo apt install -y fim
fim /шлях/до/файлу/картинка.png
```

У `fim`:

* <kbd>q</kbd> — Вихід

![image](https://github.com/user-attachments/assets/af3f8f1c-0ad2-4053-abcf-46729fddd387)

---

## 2. Адміністраторські інструменти (Admin Tools)

Існують також дії які є класичними для більшості адміністраторів та мають досить різноманітний функціонал. Опишіть різні програми (команди, пакети) та встановіть по одній на кожну дію у терміналі:Вводити, редагувати, видаляти текст (редактори файлів)

### 2.1 Редактор тексту (Text Editor)

**Опис:** *Text editor* для введення, редагування та видалення тексту у файлах.

**Вибір:** `vim` — потужний модальний редактор.

```bash
sudo apt update
sudo apt install -y vim
vim /path/to/file.txt
```

Основні клавіші у `vim`:

* <kbd>i</kbd> — Режим вставки (Insert mode)
* <kbd>Esc</kbd> — Вихід у командний режим (Command mode)
* <kbd>:</kbd><kbd>w</kbd> — Зберегти зміни (write)
* <kbd>:</kbd><kbd>q</kbd> — Вийти (quit)
* <kbd>:</kbd><kbd>wq</kbd> — Зберегти й вийти

![image](https://github.com/user-attachments/assets/43db2fe9-a7b3-44da-90a8-77004220b6f5)


---

### 2.2 Моніторинг системи (System Monitoring)

**Опис:** *Process and resource monitor* для спостереження за процесами й завантаженням системи.

**Вибір:** `htop` — інтерактивний монітор.

```bash
sudo apt update
sudo apt install -y htop
htop
```

Основні клавіші у `htop`:

* <kbd>F2</kbd> — Налаштування (Setup)
* <kbd>F3</kbd> — Пошук процесів (Search)
* <kbd>F4</kbd> — Фільтрація (Filter)
* <kbd>F6</kbd> — Сортування (Sort by)
* <kbd>F9</kbd> — Завершити процес (Kill)
* <kbd>q</kbd> — Вихід

![image](https://github.com/user-attachments/assets/5bed15e8-c7cf-496e-8fe3-a792e793c5d4)


---

## 3. Пасхалки (Easter Eggs)

Задачі, щоб підняти настрій посеред робочого процесу ☺ – так звані «пасхалки» (нажаль підтримуються не всіма дистрибутивами)

### 3.1 Паровий локомотив (Train Easter Egg)

**Команда:**

```bash
sl
```

Виконайте замість `ls`, щоб побачити анімацію потяга.

![image](https://github.com/user-attachments/assets/9613114b-e592-4d6a-af0b-7624e2ad4eae)


---

### 3.2 Зоряні Війни (Star Wars ASCII)

**Команда:**

```bash
telnet towel.blinkenlights.nl
```

На жаль пасхалко вже не підтримується :( . На реддіті знайшов обговорення 4-ти річної давнини, то деякі кажуть що ще працює, але не не можна встановити з'єднання :0 

---

### 3.3 Діалог із коровою (Cowsay)

**Команда:**

```bash
cowsay "Lets watch deMO"
```

Виводить текст у "хмарці" від імені корови.

![image](https://github.com/user-attachments/assets/7f8341d7-b01b-4a0e-80d4-c8a4cf6852b3)


---

### 3.4 Інші інтерактиви (Other Interactives)

**Установка:**

```bash
sudo apt install -y fortune cmatrix nyancat oneko
```

* `fortune` — випадкові цитати
  ![image](https://github.com/user-attachments/assets/e79760c3-c449-4356-a92b-f967dffe75a5)
  
* `cmatrix` — ефект зеленого дощу символів
  ![image](https://github.com/user-attachments/assets/3096e7e3-14a2-4871-acf0-4abd5e00dc49)

* `nyancat` — анімація Nyan Cat
  ![image](https://github.com/user-attachments/assets/c481079f-9a40-498e-8355-589c95ed9611)

* `oneko` — кішка за курсором
  ![image](https://github.com/user-attachments/assets/da9e25c6-158d-4e79-a117-a6168f38fc72)


