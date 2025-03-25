<div align="center">
  <img src="https://github.com/user-attachments/assets/dcdd0d7c-164c-4a93-a6d8-84b6015c07aa" height="200" width="300" alt="exolutioneast">
</div>

>[!IMPORTANT]
> ![made-by-borsuk-maksym](https://github.com/user-attachments/assets/68d0a6b6-134b-4446-a841-61b9dc7c958b)

### 1. В ході роботи досить часто виникає необхідність встановлювати нові програми та додатки. Для цього необхідно в терміналі вміти працювати з менеджерами пакетів:

- Дайте розгорнуте визначення таким поняттям як «пакет» та «репозиторій».

  ### Package
  A **package** in Linux is a compressed file that contains all the files needed to install a specific program or application. This includes:
  - Executable files
  - Configuration files
  - Dependencies
  - Metadata (version, description, etc.)
  
  Packages allow users to easily install, update, or remove software on their system. There are different package formats, such as `.deb` (for Debian-based systems) and `.rpm` (for Red Hat-based systems).
  
  ### Repository
  A **repository** is a remote or local storage location that contains collections of packages. It is maintained by Linux distributions or third-party developers. Repositories make it easier to:
  - Access a wide range of verified and tested software
  - Automatically resolve and install dependencies
  - Keep software up to date
  
  Users connect to repositories through package managers to install or update software.
  
- Надайте короткий огляд існуючих менеджерів пакетів у Linux. Охарактеризуйте їх основні можливості.

    ### 1. APT (Advanced Package Tool)
  - **Used in:** Debian, Ubuntu, and derivatives  
  - **Main command:** `apt` or `apt-get`  
  - **Features:**  
    - Install, remove, and update `.deb` packages  
    - Resolves dependencies automatically  
    - Connects to online repositories  
    - Simple to use for both beginners and advanced users  
  
  ### 2. DNF (Dandified YUM)
  - **Used in:** Fedora, Red Hat, CentOS (newer versions)  
  - **Main command:** `dnf`  
  - **Features:**  
    - Works with `.rpm` packages  
    - Faster and more efficient than old YUM  
    - Handles dependencies and transactions better  
    - Can install from multiple repositories  
  
  ### 3. YUM (Yellowdog Updater, Modified)
  - **Used in:** Older versions of Red Hat and CentOS  
  - **Main command:** `yum`  
  - **Features:**  
    - Also works with `.rpm` packages  
    - Was replaced by DNF in newer systems  
    - Simple command structure  
  
  ### 4. Zypper
  - **Used in:** openSUSE and SUSE Linux  
  - **Main command:** `zypper`  
  - **Features:**  
    - Efficient package handling with `.rpm`  
    - Advanced search and install features  
    - Good dependency resolution  
  
  ### 5. Pacman
  - **Used in:** Arch Linux and Manjaro  
  - **Main command:** `pacman`  
  - **Features:**  
    - Handles `.pkg.tar.zst` packages  
    - Very fast and lightweight  
    - Combines package installation and building from source  
  
  ### 6. Snap
  - **Used in:** Ubuntu (and available on others)  
  - **Main command:** `snap`  
  - **Features:**  
    - Universal package format  
    - Works across multiple distros  
    - Includes all dependencies (sandboxed)  
    - Slower startup time  
  
  ### 7. Flatpak
  - **Used in:** Multiple distributions  
  - **Main command:** `flatpak`  
  - **Features:**  
    - Like Snap, also cross-distro  
    - Good for sandboxed desktop apps  
    - Integrates with Flathub repository  

  | Package Manager | Used In                                  | Main Command     | Key Features                                                                 |
  |-----------------|-------------------------------------------|------------------|------------------------------------------------------------------------------|
  | **APT**         | Debian, Ubuntu, and derivatives           | `apt`, `apt-get` | - Works with `.deb` packages<br>- Resolves dependencies<br>- Online repos<br>- Easy to use |
  | **DNF**         | Fedora, Red Hat, CentOS (new versions)    | `dnf`            | - Works with `.rpm` packages<br>- Faster than YUM<br>- Better dependency handling<br>- Multiple repos support |
  | **YUM**         | Older Red Hat and CentOS                  | `yum`            | - `.rpm` support<br>- Replaced by DNF<br>- Simple commands                   |
  | **Zypper**      | openSUSE, SUSE Linux                      | `zypper`         | - `.rpm` packages<br>- Advanced search/install<br>- Good dependency management |
  | **Pacman**      | Arch Linux, Manjaro                       | `pacman`         | - `.pkg.tar.zst` format<br>- Fast and lightweight<br>- Source build support  |
  | **Snap**        | Ubuntu and others                         | `snap`           | - Universal format<br>- Cross-distro<br>- Sandboxed<br>- Slower startup      |
  | **Flatpak**     | Multiple distributions                    | `flatpak`        | - Cross-distro<br>- Sandboxed desktop apps<br>- Flathub integration          |


---

### 2. Визначте який менеджер пакетів використовує ваш дистрибутив Linux. Опишіть основні команди для роботи з ним:

  У дистрибутиві **Ubuntu** використовується менеджер пакетів **APT (Advanced Package Tool)**.  
  Він дозволяє легко встановлювати, оновлювати, шукати та видаляти пакети зі стандартних репозиторіїв.
  
  ---
  
  ## Пошук, скачування та установка необхідних пакетів
  
  ### Find package in repo 
  ```bash
  apt search <назва_пакета>
  ```
  
  ### Info about package
  ```bash
  apt show <назва_пакета>
  ```
  
  ### Package installation
  ```bash
  sudo apt install <назва_пакета>
  ```
  
  ### Adding new repo
  ```bash
  sudo add-apt-repository ppa:<назва_репозиторію>
  sudo apt update
  ```
  
  ---
  
  ## Перегляд інформації про встановлені та доступні пакети
  
  ### List of all installed packages
  ```bash
  apt list --installed
  ```
  
  ### List of avaible packages
  ```bash
  apt list
  ```
  
  ### Find update for installed packages
  ```bash
  apt list --upgradable
  ```
  
  ---
  
  ## Видалення непотрібних або застарілих пакетів
  
  ### Package delete (leave config files)
  ```bash
  sudo apt remove <назва_пакета>
  ```
  
  ### Full delelte including config files
  ```bash
  sudo apt purge <назва_пакета>
  ```
  
  ### Auto delete of unnecessary packgs
  ```bash
  sudo apt autoremove
  ```
  
  ---
  
  ## Оновлення менеджера пакетів
  
  ### Update package list from repo
  ```bash
  sudo apt update
  ```
  
  ### Update installed packages up to date
  ```bash
  sudo apt upgrade
  ```

### Full system update (including dependencies)
```bash
sudo apt full-upgrade
```

>[!IMPORTANT]
> ![made-by-borsuk-maksym](https://github.com/user-attachments/assets/68d0a6b6-134b-4446-a841-61b9dc7c958b)

### 3. Встановіть у терміналі через менеджер пакетів на свою систему:

  ``` bash
  sudo apt update
  ```
  --- 
  - Новий відео- чи аудіоплейер.

  ```bash
  sudo apt install mpv
  ```
  ![image](https://github.com/user-attachments/assets/ce51c09a-a059-42e2-98f6-1f4f11659730)

---
    
  - Середовище для мови програмування, що ви вивчаєте.

  ```bash
  sudo apt install nodejs npm
  ```
  ![image](https://github.com/user-attachments/assets/59449301-d575-4753-a4fb-b49d3c08fe82)

---

```bash
mpv -version
node -v
npm -v
```
![image](https://github.com/user-attachments/assets/03820b87-639b-4c52-adb6-32e955811ec1)

---

>[!IMPORTANT]
> ![made-by-borsuk-maksym](https://github.com/user-attachments/assets/68d0a6b6-134b-4446-a841-61b9dc7c958b)
  
###  4. Яким чином можна встановити нові програми через магазини додатків та менеджери пакетів у графічному середовищі. Наведіть свої приклади.

  ## 1. App Stores
  
  App stores are user-friendly graphical tools that allow you to search, install, update, or remove software without using the terminal.
  
  ### 🔹 **Ubuntu Software (Snap Store)**
  - Pre-installed in Ubuntu.
  - Simple interface with categories and user ratings.
  - Allows installing both **Snap packages** and some traditional `.deb` packages.
  
  **Example:**  
  To install the **Brave browser**:
  1. Open **Ubuntu Software**.
  2. Search for "Brave".
  3. Click "Install".
  
  ---
  
  ## 2. Package Managers with GUI
  
  Some distributions provide graphical frontends for traditional package managers.
  
  ### 🔹 **Synaptic Package Manager**
  - A graphical frontend for **APT**.
  - Allows searching, installing, and removing `.deb` packages from repositories.
  - Shows dependencies and detailed package info.
  
  **Example:**  
  1. Install Synaptic through Ubuntu Software or with:
     ```bash
     sudo apt install synaptic
     ```
  2. Launch Synaptic from the application menu.
  3. Search for a program (e.g., “gimp”), mark it, and click “Apply”.
  
  ---
  
  ## 3. GUI Interfaces for Flatpak and Snap
  
  ### 🔹 **GNOME Software (on some distributions)**
  - Can integrate Snap, Flatpak, and APT packages.
  - Supports **Flathub**, a popular Flatpak repository.
  
  **Example:**  
  To install **Spotify** via Flatpak:
  1. Open GNOME Software and search for “Spotify”.
  2. Choose the version from Flathub.
  3. Click "Install".
