# Tesla-Menu

Tesla-Menu — это оверлейное меню, разработанное [WerWolv](https://github.com/WerWolv). Tesla-Menu можно сравнить с меню Rosalina на 3DS, и его цель — возможность загружать созданные сообществом оверлеи для Homebrew приложений и системных модулей, которые можно использовать в любое время. Ниже приведены распространенные случаи использования Tesla-Menu. Официальная страница GitHub для Tesla-Menu доступна [здесь](https://github.com/WerWolv/Tesla-Menu).

!!! note "Зависимости"
    Tesla-Menu зависит от [системного модуля](index.md#terminologies) под названием `nx-ovlloader`, который отвечает за загрузку `ovlmenu.ovl` из `sd:/switch/.overlays`.

#### Распространенные случаи использования Tesla-Menu:
- Загрузка созданных сообществом оверлеев Tesla-Menu
- Просмотр температур/частот процессора вашего оборудования
- Редактирование конфигураций системных модулей на лету (если применимо)
- Редактирование конфигураций Homebrew приложений на лету (если применимо)
- Легкое включение и отключение читов
- Легкое включение и отключение системных модулей

-----

#### Требования к установке:
- Архиватор, например, [7-Zip](https://www.7-zip.org/)
- Последняя версия [Tesla-Menu](https://github.com/WerWolv/Tesla-Menu/releases/tag/v1.2.3) (файл `ovlmenu.zip`)
- Последняя версия [nx-ovlloader](https://github.com/WerWolv/nx-ovlloader/releases/tag/v1.0.7) (файл `nx-ovlloader.zip`)

#### Инструкции по установке:
1. Загрузитесь в Hekate и перейдите в `Tools` > `USB Tools` > `SD Card`, затем подключите свою консоль к ПК через USB.
2. Ваша microSD-карта теперь должна быть доступна на вашем ПК, откройте ее.
3. Извлеките оба `.zip` файла в папку на вашем компьютере.
    - Если ваш архиватор позволяет, вы можете открыть `.zip` файлы напрямую.
4. Скопируйте *содержимое* каждого (извлеченного) `.zip` файла в корень вашей microSD-карты.
    - **Необязательно:** Вы можете проверить, правильно ли вы установили Tesla-Menu и nx-ovlloader. У вас должна быть папка с именем `420000000007E51A` (nx-ovlloader) в `sd:/atmosphere/contents` и файл `ovlmenu.ovl` (Tesla-Menu) в `sd:/switch/.overlays`.
5. Загрузитесь в CFW.

-----

### **Открытие Tesla-Menu**
Tesla-Menu можно открыть, нажав `L` + `R Stick press (R3)` + `DPAD down`, если вы используете конфигурацию по умолчанию.

![tesla](img/tesla-menu.jpg)

#### Изменение комбинации кнопок

Если вы хотите изменить конфигурацию кнопок по умолчанию, следуйте инструкциям ниже:

1. Перейдите в `sd:/config` на вашей microSD-карте.
2. Создайте папку с именем `tesla`, если она еще не существует.
3. Создайте файл с именем `config.ini` в `sd:/config/tesla`.
4. Вставьте следующий текст в `config.ini`:
    ```
    [tesla]
    key_combo=L+R+RS
    # A, B, X, Y, LS, RS, L, R, ZL, ZR, PLUS, MINUS, DLEFT, DUP, DRIGHT, DDOWN, SL, SR
    ```
5. Измените значение `key_combo` на любое желаемое и сохраните файл. Допустимые значения указаны на третьей строке.

-----

### **Распространенные оверлеи Tesla-Menu**
- [Status-Monitor-Overlay](https://github.com/masagrator/Status-Monitor-Overlay)
- [EdiZon overlay](https://github.com/proferabg/EdiZon-Overlay)
- [QuickNTP](https://github.com/nedex/QuickNTP)
- [Emuiibo](https://github.com/XorTroll/emuiibo) (это требует установки системного модуля Emuiibo)
- [TriPlayer](https://github.com/DefenderOfHyrule/TriPlayer) (это требует установки системного модуля TriPlayer)
- [ldn_mitm](https://github.com/DefenderOfHyrule/ldn_mitm) (это требует установки системного модуля ldn_mitm)
- [Fizeau](https://github.com/averne/Fizeau) (это требует установки системного модуля Fizeau)

-----

### **Устранение неполадок**
#### **Моя система выдает ошибку при загрузке после установки Tesla-Menu/nx-ovlloader!:**

**Причина:** Если ваша консоль выдает ошибку с кодом `2001-0123 (0xf601)` и идентификатором заголовка `420000000007E51A`, это означает, что вы допустили ошибку во время установки Tesla-Menu или не использовали последнюю версию Tesla-Menu. Повторите инструкции по установке выше.

&nbsp;

#### **Моя система выдает ошибку, когда я открываю оверлей через Tesla-Menu!:**

**Причина:** Если ваша консоль выдает ошибку с кодом `2001-0123 (0xf601)` и идентификатором заголовка `420000000007E51A`, это означает, что оверлей, который вы пытаетесь открыть/использовать, не обновлен. Проверьте его репозиторий для получения обновлений.

- Если у этого оверлея нет обновленной версии, возможно, вам придется искать форк (обновленную версию) или собрать его самостоятельно с использованием последней библиотеки `libtesla`. Последний вариант предназначен для разработчиков (или продвинутых пользователей).

&nbsp;

#### **Tesla-Menu отображается только на главном экране, а не в игре!:**

**Причина:** Эта проблема возникает только когда Switch находится в док-станции. Убедитесь, что вы установили "Размер экрана" в `Настройки системы` > `Выходной сигнал ТВ` на 100%. Настройте ваш телевизор/монитор, чтобы он соответствовал полному экрану вашей Switch, используя его OSD (On Screen Display) или пульт.

&nbsp;

#### **Tesla-Menu не открывается, когда я нажимаю правильную комбинацию кнопок!:**

Предполагая, что вы успешно выполнили инструкции по установке, это, вероятно, связано с тем, что архивный бит установлен на одну или несколько папок/файлов на вашей microSD-карте. Обычно это происходит при копировании файлов на microSD-карту с помощью Mac. Если вы столкнулись с этой проблемой, попробуйте запустить утилиту исправления архивного бита через Hekate для всех файлов.

Это можно сделать, загрузившись в Hekate и перейдя в `Tools` > `Arch bit • RCM Touch • Pkg1/2` > `Fix Archive Bit`.
