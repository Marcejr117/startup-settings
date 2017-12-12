Language: **Русский|[English](/README.md)**

# Startup Settings

По умолчанию в GNOME 3 отсутствуют удобные инструменты для управления автозагрузкой.
Для добавления пользовательской команды в автозагрузку необходимо вручную создать
файл `~/.config/autostart/file.desktop`. Эта небольшая программа, написанная на C++ и
GTK 3, предоставляет удобный графический интерфейс для управления автозагрузкой.
Программа разработана специально для GNOME 3, однако может быть использована и в
любой другой среде рабочего стола.

### Установка

Если вы используете Debian/Ubuntu, вы можете установить приложение из пакета.

Для amd64: <br />
`wget https://github.com/hant0508/startup-settings/raw/master/debian/startup-settings-amd64.deb` <br />
`sudo dpkg -i startup-settings-amd64.deb` <br />
Для i386: <br />
`wget https://github.com/hant0508/startup-settings/raw/master/debian/startup-settings-i386.deb` <br />
`sudo dpkg -i startup-settings-i386.deb`

Если вы установили пакет, то вам не нужно собирать программу из исходного кода, переходите к [использованию](#Использование).

### Сборка

- Установка зависимостей <br />
Debian/Ubuntu: `sudo apt-get install g++ make git libgtk-3-dev` <br />
Arch/Manjaro x32: `sudo pacman -S gcc git make gtk3` <br />
Arch/Manjaro x64: `sudo pacman -S gcc-multilib git make gtk3` <br />
- Сборка <br />
`git clone https://github.com/hant0508/startup-settings.git` <br />
`cd startup-settings` <br />
`make`
- Установка приложения <br />
`sudo make install`

Для освобождения места на диске вы можете удалить все загруженные файлы и зависимости
после установки приложения. 

### Использование

После установки вы сможете найти программу в меню приложений или запустить
`startup-settings` из терминала.

Введите в поле `Command` команду автозагрузки. Это может быть:
- полный путь к файлу: `/usr/bin/file.sh`
- относительный путь к файлу в домашней папке: `scripts/file.sh`
- команда из [$PATH](https://ru.wikipedia.org/wiki/PATH_(%D0%BF%D0%B5%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D0%B0%D1%8F)): `firefox`

В зависимости от оконного менеджера, вы так же можете использовать drag-and-drop
(перетаскивание). GNOME 3 разрешает даже перетаскивать файлы.

### Скриншоты

![img](https://raw.githubusercontent.com/hant0508-zz/tmp/master/startup-settings/gif%201.gif) | ![img](https://raw.githubusercontent.com/hant0508-zz/tmp/master/startup-settings/gif%202.gif)
:---:|:---:
Usage on GNOME 3 | Drag and drop on GNOME 3

![alt-text](https://raw.githubusercontent.com/hant0508-zz/tmp/master/startup-settings/kde.png "KDE 5") | ![alt-text](https://raw.githubusercontent.com/hant0508-zz/tmp/master/startup-settings/cinnamon.png "Cinnamon 3") |  ![alt-text](https://raw.githubusercontent.com/hant0508-zz/tmp/master/startup-settings/xfce4.png "XFCE 4")
:-------------------------:|:-------------------------:|:-------------------------:
KDE 5                      | Cinnamon 3                | XFCE 4          

### Обратная связь

Если у вас возникли проблемы при работе с программой, сообщите о них на
[GitHub](https://github.com/hant0508/startup-settings/issues/new) или
[Вконтакте](https://vk.com/im?sel=116615188). Пишите мне [по электронной
почте](mailto:hant0508@gmail.com?subject=GitHub%20issue%20|%20Startup), если у вас нет
аккаунта на GitHub. 
