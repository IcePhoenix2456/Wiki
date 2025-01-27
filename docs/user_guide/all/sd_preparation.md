# **Подготовка SD карты**

### **Информация**

Теперь мы разместим необходимые файлы для кастомной прошивки Atmosphère и некоторые дополнительные файлы homebrew на microSD карте.

Atmosphère имеет свой собственный загрузчик, называемый fusee. В рамках этого руководства мы будем использовать Hekate, чтобы иметь возможность создать резервную копию NAND (внутреннего хранилища системы) и использовать другие расширенные функции в будущем.

!!! warning "Расширения имен файлов"
    Если вы используете Windows, вам нужно включить отображение расширений имен файлов перед продолжением. Для этого можно воспользоваться [этим руководством](../../extras/showing_file_extensions.md).


-----

#### **Что вам нужно:**
- Последняя версия <a href="https://github.com/CTCaer/Hekate/releases/" target="_blank">Hekate</a> (Скачайте релиз `hekate_ctcaer_(версия).zip`)
- Конфигурационный файл Hekate: <a href="../../../files/emu/hekate_ipl.ini" download>hekate_ipl.ini</a>
- Конфигурация DNS.MITM для перенаправления DNS: <a href="../../../files/emummc.txt" download>emummc.txt</a>
- Папка с bootlogo в формате zip: <a href="../../../files/bootlogos.zip" download>bootlogos.zip</a>
- Последняя версия <a href="https://github.com/Atmosphere-NX/Atmosphere/releases" target="_blank">Atmosphere</a>. Скачайте релиз `atmosphere-(версия)-master-(версия)+hbl-(версия)+hbmenu-(версия).zip`
- Последняя версия <a href="https://github.com/J-D-K/JKSV/releases" target="_blank">JKSV</a> (Скачайте релиз `JKSV.nro`)
- Последняя версия <a href="https://github.com/mtheall/ftpd/releases" target="_blank">FTPD</a> (Скачайте релиз `ftpd.nro`)
- Последняя версия <a href="https://github.com/exelix11/SwitchThemeInjector/releases" target="_blank">NXThemesInstaller</a> (Скачайте релиз `NXThemesInstaller.nro`)
- Последняя версия <a href="https://github.com/joel16/NX-Shell/releases" target="_blank">NX-Shell</a> (Скачайте релиз `NX-Shell.nro`)
- Последняя версия <a href="https://github.com/XorTroll/Goldleaf/releases" target="_blank">Goldleaf</a> (Скачайте релиз `Goldleaf.nro`)


#### **Инструкции:**
1. Перейдите на доступный диск.
2. Скопируйте *содержимое* архива Atmosphère`.zip` в корень вашей microSD карты.
3. Скопируйте папку `bootloader` из архива Hekate `.zip` в корень вашей microSD карты.
    - Если вас попросят заменить файлы или объединить папки, согласитесь.
4. Скопируйте папку `bootloader` из архива `bootlogos.zip` в корень вашей microSD карты.
    - Если вас попросят объединить папки bootloader, согласитесь.
5. Скопируйте файл `hekate_ipl.ini` в папку `bootloader` на вашей microSD карте.
    - Если вас попросят заменить файл, согласитесь.
6. Создайте папку с именем `hosts` внутри папки `atmosphere` на вашей microSD карте и поместите в нее файл `emummc.txt`.
7. Скопируйте файлы `JKSV.nro`, `ftpd.nro`, `NxThemesInstaller.nro`, `NX-Shell.nro` и `Goldleaf.nro` в папку `switch` на вашей microSD карте.
8. Если вы уже использовали свою microSD карту для хранения игр и сделали резервную копию папки Nintendo перед разделением карты, верните её в корень microSD карты.
    - Если вы создали emuMMC на предыдущей странице, не забудьте скопировать папку Nintendo в `sd:/emuMMC/RAW1/`!

!!! danger "О файле emummc.txt"
    Помещение файла `emummc.txt`, предоставленного в этом руководстве, в папку `/atmosphere/hosts` предотвратит подключение вашего emuMMC (emuNAND) к сети Nintendo. Несоблюдение этого может привести к бану.

!!! tip ""    
    Ваша microSD карта должна выглядеть как на изображении ниже. Папка `Nintendo` не будет присутствовать, если ваш Switch еще не был загружен с microSD картой, а папка `emuMMC` не будет присутствовать, если вы следуете пути sysCFW в этом руководстве/если вы не создавали emuMMC!
    Файл `payload.bin` не будет присутствовать, если вы используете не уязвимый Switch.

    ![sdfilesimg](img/sdfiles3.png)

[Перейти к созданию бэкапа :material-arrow-right:](making_essential_backups.md){ .md-button .md-button--primary }
