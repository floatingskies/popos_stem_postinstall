# popos_stem_postinstall

> 🇧🇷 [Português](#português) · 🇺🇸 [English](#english) · 🇪🇸 [Español](#español)

---

## Português

### O que é?

Script de pós-instalação para **Pop!_OS** (22.04 LTS ou superior) focado em ambientes de **desenvolvimento de software**, **STEM**, **design**, **ciência de dados**, **robótica** e **gaming**.

Instala, configura e limpa o sistema de uma só vez — incluindo ferramentas APT, Flatpaks, .NET, NVM, JetBrains Toolbox, DBeaver, ROS 2 e muito mais.

### O que o script faz?

- Remove pacotes desnecessários ou substituídos por versões Flatpak (GIMP, Inkscape, VLC, etc.)
- Adiciona repositórios externos: Microsoft (VS Code, VS Code Insiders), GitHub CLI, MySQL
- Instala todos os pacotes APT de uma vez (mais rápido que um por um)
- Baixa e instala `.deb` externos: Google Chrome, DBeaver CE
- Instala o **.NET SDK LTS** via script oficial da Microsoft
- Instala Flatpaks em lote por categoria: mídia, produtividade, sistema, dev, STEM, gaming
- Instala a **JetBrains Toolbox** com URL resolvida dinamicamente via API oficial
- Configura Docker sem sudo, NVM, Git LFS, ROS 2 Humble (se jammy)
- Instala ferramentas Python via pip: JupyterLab, scikit-learn, OpenCV, etc.
- Cria pastas de produtividade e atalhos no Nautilus

### Como executar?

**Requisitos:** Pop!_OS 22.04+ · conexão com a internet · `sudo`

```bash
# Clone ou baixe o script
git clone https://github.com/seu-usuario/popos_stem_postinstall.git
cd popos_stem_postinstall

# Torne executável e rode
chmod +x popos_stem_postinstall.sh
./popos_stem_postinstall.sh
```

> ⚠️ **Atenção:** O script usa `sudo` internamente. Não execute com `sudo ./script.sh` — isso pode quebrar paths de usuário (`$HOME`, `$USER`).

> 🔁 **Idempotente:** pode ser executado mais de uma vez com segurança. Pacotes já instalados são pulados; pacotes desnecessários são removidos mesmo que tenham sido instalados por um script anterior.

### Principais ferramentas instaladas

| Categoria | Ferramentas |
|---|---|
| **Editores / IDEs** | VS Code, VS Code Insiders, JetBrains Toolbox |
| **Dev** | GCC, Clang, CMake, Docker, Git, GitHub CLI, Node.js + NVM, Python 3, Java (JDK + Maven + Gradle) |
| **.NET** | .NET SDK LTS (`~/.dotnet`) |
| **Banco de dados** | MySQL, PostgreSQL, Redis, DBeaver CE |
| **Ciência de dados** | NumPy, Pandas, Matplotlib, Scikit-learn, JupyterLab, R |
| **STEM / Engenharia** | Octave, Scilab, GnuPlot, FreeCAD, OpenSCAD, KiCad, LibreCAD, GeoGebra, Maxima |
| **Robótica** | Arduino IDE, ROS 2 Humble (jammy) |
| **Design** | GIMP, Inkscape, Krita, Blender, Kdenlive, Scribus (via Flatpak) |
| **Gaming** | Steam, Lutris, Wine, MangoHud, RetroArch |
| **Produtividade** | Obsidian, OnlyOffice, Telegram, Discord, Zoom, Thunderbird, Kolibri |

---

## English

### What is it?

A post-installation script for **Pop!_OS** (22.04 LTS or later), focused on **software development**, **STEM**, **design**, **data science**, **robotics**, and **gaming** environments.

It installs, configures, and cleans the system in one run — including APT tools, Flatpaks, .NET, NVM, JetBrains Toolbox, DBeaver, ROS 2, and more.

### What does the script do?

- Removes unnecessary packages or those replaced by Flatpak versions (GIMP, Inkscape, VLC, etc.)
- Adds external repositories: Microsoft (VS Code, VS Code Insiders), GitHub CLI, MySQL
- Installs all APT packages at once (faster than one-by-one)
- Downloads and installs external `.deb` files: Google Chrome, DBeaver CE
- Installs **.NET LTS SDK** via the official Microsoft script
- Installs Flatpaks in bulk by category: media, productivity, system, dev, STEM, gaming
- Installs **JetBrains Toolbox** with the download URL resolved dynamically from the official API
- Configures Docker without sudo, NVM, Git LFS, ROS 2 Humble (if on jammy)
- Installs Python tools via pip: JupyterLab, scikit-learn, OpenCV, etc.
- Creates productivity folders and Nautilus bookmarks

### How to run?

**Requirements:** Pop!_OS 22.04+ · internet connection · `sudo`

```bash
# Clone or download the script
git clone https://github.com/your-username/popos_stem_postinstall.git
cd popos_stem_postinstall

# Make it executable and run
chmod +x popos_stem_postinstall.sh
./popos_stem_postinstall.sh
```

> ⚠️ **Warning:** The script uses `sudo` internally. Do **not** run it as `sudo ./script.sh` — that may break user-level paths (`$HOME`, `$USER`).

> 🔁 **Idempotent:** safe to run multiple times. Already-installed packages are skipped; unnecessary packages are removed even if they were installed by a previous script run.

### Main tools installed

| Category | Tools |
|---|---|
| **Editors / IDEs** | VS Code, VS Code Insiders, JetBrains Toolbox |
| **Dev** | GCC, Clang, CMake, Docker, Git, GitHub CLI, Node.js + NVM, Python 3, Java (JDK + Maven + Gradle) |
| **.NET** | .NET LTS SDK (`~/.dotnet`) |
| **Databases** | MySQL, PostgreSQL, Redis, DBeaver CE |
| **Data Science** | NumPy, Pandas, Matplotlib, Scikit-learn, JupyterLab, R |
| **STEM / Engineering** | Octave, Scilab, GnuPlot, FreeCAD, OpenSCAD, KiCad, LibreCAD, GeoGebra, Maxima |
| **Robotics** | Arduino IDE, ROS 2 Humble (jammy only) |
| **Design** | GIMP, Inkscape, Krita, Blender, Kdenlive, Scribus (via Flatpak) |
| **Gaming** | Steam, Lutris, Wine, MangoHud, RetroArch |
| **Productivity** | Obsidian, OnlyOffice, Telegram, Discord, Zoom, Thunderbird, Kolibri |

---

## Español

### ¿Qué es?

Script de post-instalación para **Pop!_OS** (22.04 LTS o superior), enfocado en entornos de **desarrollo de software**, **STEM**, **diseño**, **ciencia de datos**, **robótica** y **gaming**.

Instala, configura y limpia el sistema en una sola ejecución — incluyendo herramientas APT, Flatpaks, .NET, NVM, JetBrains Toolbox, DBeaver, ROS 2 y más.

### ¿Qué hace el script?

- Elimina paquetes innecesarios o reemplazados por versiones Flatpak (GIMP, Inkscape, VLC, etc.)
- Agrega repositorios externos: Microsoft (VS Code, VS Code Insiders), GitHub CLI, MySQL
- Instala todos los paquetes APT de una vez (más rápido que uno por uno)
- Descarga e instala `.deb` externos: Google Chrome, DBeaver CE
- Instala el **.NET SDK LTS** mediante el script oficial de Microsoft
- Instala Flatpaks en lote por categoría: multimedia, productividad, sistema, dev, STEM, gaming
- Instala **JetBrains Toolbox** con la URL resuelta dinámicamente desde la API oficial
- Configura Docker sin sudo, NVM, Git LFS, ROS 2 Humble (si es jammy)
- Instala herramientas Python vía pip: JupyterLab, scikit-learn, OpenCV, etc.
- Crea carpetas de productividad y accesos directos en Nautilus

### ¿Cómo ejecutarlo?

**Requisitos:** Pop!_OS 22.04+ · conexión a internet · `sudo`

```bash
# Clona o descarga el script
git clone https://github.com/tu-usuario/popos_stem_postinstall.git
cd popos_stem_postinstall

# Dale permisos y ejecútalo
chmod +x popos_stem_postinstall.sh
./popos_stem_postinstall.sh
```

> ⚠️ **Atención:** El script usa `sudo` internamente. **No** lo ejecutes como `sudo ./script.sh` — eso puede romper paths de usuario (`$HOME`, `$USER`).

> 🔁 **Idempotente:** puede ejecutarse más de una vez de forma segura. Los paquetes ya instalados se omiten; los paquetes innecesarios se eliminan aunque hayan sido instalados por una ejecución anterior.

### Principales herramientas instaladas

| Categoría | Herramientas |
|---|---|
| **Editores / IDEs** | VS Code, VS Code Insiders, JetBrains Toolbox |
| **Dev** | GCC, Clang, CMake, Docker, Git, GitHub CLI, Node.js + NVM, Python 3, Java (JDK + Maven + Gradle) |
| **.NET** | .NET SDK LTS (`~/.dotnet`) |
| **Bases de datos** | MySQL, PostgreSQL, Redis, DBeaver CE |
| **Ciencia de datos** | NumPy, Pandas, Matplotlib, Scikit-learn, JupyterLab, R |
| **STEM / Ingeniería** | Octave, Scilab, GnuPlot, FreeCAD, OpenSCAD, KiCad, LibreCAD, GeoGebra, Maxima |
| **Robótica** | Arduino IDE, ROS 2 Humble (solo jammy) |
| **Diseño** | GIMP, Inkscape, Krita, Blender, Kdenlive, Scribus (vía Flatpak) |
| **Gaming** | Steam, Lutris, Wine, MangoHud, RetroArch |
| **Productividad** | Obsidian, OnlyOffice, Telegram, Discord, Zoom, Thunderbird, Kolibri |

---

<p align="center">
  Feito com ❤️ para a comunidade Pop!_OS
</p>
