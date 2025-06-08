---
hide:
  - navigation
---
# Обновление и откат HOS

!!! question "Что такое HOS?"
     HOS расшифровывается как Horizon Operating System — это операционная система, на базе которой работает консоль Nintendo Switch.

## Обновление HOS

### Загрузка файлов обновления

1. Запустите [**Homebrew menu**] (Зажав R зайти в игру/альбом), затем откройте **All in One Updater**.
2. В разделе **Загрузить прошивку** выберите и загрузите версию прошивки на которую вы будете обновлять консоль. Желательно загружать rebootless версию прошивки, так как она новее(в ней есть изменения, которые не требовали перезагрузки консоли при обновлении).
![aio_download](res/hos_update/aio_download.jpg)

### Установка обновления

1. Запустите [**Homebrew menu**] (Зажав R зайти в игру/альбом), затем откройте **Daybreak**.
2. Следуйте примеру ниже, выбирая пункты, выделенные синим цветом.
![daybreak_entry](res/hos_update/daybreak_entry.jpg)
![choose_folder](res/hos_update/choose_folder.jpg)
![up_1](res/hos_update/up_1.jpg)
![up_2](res/hos_update/up_2.jpg)
![up_3](res/hos_update/up_3.jpg)
![up_4](res/hos_update/up_4.jpg)

## Откат HOS

!!! warning "Сброс до заводских настроек"
     При откате с 20 HOS необходимо выбрать сброс до заводских настроек в Daybreak, во избежании ошибок после отката. Это приведет к потере всех пользовательских данных. Вы можете предварительно сделать бэкап сохранений в DBI и [бэкап своего профиля в Linkalho](../useful_guides/linkalho_nnid.md), чтобы восстановить их после отката. Все установленные игры к сожалению будут утеряны.

1. Убедитесь что вы используете версию Ultra NX не ниже 2.4|R2x, или [обновите ее через All in One Updater](../ultra_wiki/installing_update.md#obnovlenie-cherez-aio).
2. Загрузите через All in One Updater файлы прошивки, на которую вы будете делать откат.
3. Запустите [**Homebrew menu**] (Зажав R зайти в игру/альбом), затем откройте **Daybreak**.
4. Следуйте примеру ниже, выбирая пункты, выделенные синим цветом.
![daybreak_entry](res/hos_update/daybreak_entry.jpg)
![choose_folder](res/hos_update/choose_folder.jpg)
![down_1](res/hos_update/down_1.jpg)
![down_2](res/hos_update/down_2.jpg)
![down_3](res/hos_update/down_3.jpg)
![down_4](res/hos_update/down_4.jpg)