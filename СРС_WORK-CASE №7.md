
## 2. Планування задач через Cron

Для вашої віртуальної машини зі встановленою ОС Linux здійсніть планування обраних вами задач (запуск додатків, вмикання/вимикання машини, очистка каталогів, видалення файлів, резервне копіювання, архівування тощо на ваш вибір) через планувальник Cron:

### 2.1. Виконання в чітко визначений час

**Опис:** резервне копіювання домашньої теки щодня о 08:00.

#### Команди:

```bash
# Створення скрипта backup.sh
cat << 'EOF' > ~/cron-scripts/backup.sh
#!/bin/bash
# Архівування домашньої теки
mkdir -p /home/username/backups

tar czf /home/username/backups/home_$(date +%F).tar.gz /home/username
EOF
chmod +x ~/cron-scripts/backup.sh

# Додавання задачі в crontab
crontab -e
# Додати рядок:
0 8 * * * /home/username/cron-scripts/backup.sh >> /home/username/cron.log 2>&1
```

![image](https://github.com/user-attachments/assets/0f302750-3557-4a0a-b18f-eda115f82983)


### 2.2. Виконання однієї й тієї ж задачі двічі на день

**Опис:** запуск резервного копіювання о 06:00 та 18:00.

#### Команда в crontab:

```cron
0 6,18 * * * /home/username/cron-scripts/backup.sh >> /home/username/cron.log 2>&1
```

![image](https://github.com/user-attachments/assets/c29aa20d-2794-47f3-8431-7c83007258db)


### 2.3. Виконання тільки в будні в проміжок 8:00–18:00

**Опис:** очищення тимчасових файлів `/tmp` щогодини по буднях.

#### Скрипт cleanup.sh:

```bash
cat << 'EOF' > ~/cron-scripts/cleanup.sh
#!/bin/bash
# Видалення файлів старших за 7 днів у /tmp
find /tmp -type f -mtime +7 -delete
EOF
chmod +x ~/cron-scripts/cleanup.sh
```

#### Команда в crontab:

```cron
0 8-18 * * 1-5 /home/username/cron-scripts/cleanup.sh >> /home/username/cron.log 2>&1
```

![image](https://github.com/user-attachments/assets/ea1f4974-348a-49c1-b914-907951c7c9fe)


### 2.4. Виконання задач за різними інтервалами

**Опис:** архівування раз у рік, місяць, день, щогодини, а також при перезавантаженні.

#### Записи в crontab:

```cron
# Раз у рік — 1 січня о 00:00
0 0 1 1 *   /home/username/cron-scripts/backup.sh >> /home/username/cron.log 2>&1
# Раз на місяць — 1-го числа о 02:00
0 2 1 * *   /home/username/cron-scripts/backup.sh >> /home/username/cron.log 2>&1
# Раз на день — щодня о 03:30
30 3 * * *  /home/username/cron-scripts/cleanup.sh >> /home/username/cron.log 2>&1
# Щогодини — 5 хвилин кожної години
5 * * * *   /home/username/cron-scripts/cleanup.sh >> /home/username/cron.log 2>&1
# При перезавантаженні (reboot)
@reboot     /home/username/cron-scripts/startup.sh >> /home/username/cron.log 2>&1
```
![image](https://github.com/user-attachments/assets/604474d4-ced2-47f4-8a4c-854b08b54ae0)

---

## 3. Альтернативний планувальник — systemd timers

Встановіть альтернативний Cron’у планувальник задач (на Ваш вибір). Виконані у завданні 2 дії продемонструйте через нього.

### 3.1. Створення Service Unit

```ini
# ~/.config/systemd/user/backup.service
[Unit]
Description=Резервне копіювання домашньої теки

[Service]
Type=oneshot
ExecStart=/home/username/cron-scripts/backup.sh
```

### 3.2. Створення Timer Unit

```ini
# ~/.config/systemd/user/backup.timer
[Unit]
Description=Таймер: запуск backup.service о 06:00 та 18:00

[Timer]
OnCalendar=*-*-* 06:00:00
OnCalendar=*-*-* 18:00:00
Persistent=true

[Install]
WantedBy=timers.target
```

### 3.3. Активація та перевірка

```bash
# Перезавантаження конфігурації
systemctl --user daemon-reload
# Увімкнення і старт таймера
systemctl --user enable --now backup.timer

# Перевірка таймера
systemctl --user list-timers
systemctl --user status backup.timer
```

![image](https://github.com/user-attachments/assets/1624175a-4b8f-4afe-8340-50e794f347bd)


---

