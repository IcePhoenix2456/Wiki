---
hide:
  - navigation
---
# Переход на новую памяти

## Определения типа Эмунанда
Для начала нам надо определить какой у вас тип Эмунанда. Сделать это можно, используя Hekate.

1. Выключите вашу консоль и зайдите в hekate(кнопка уменьшения громкости при включении консоли, если консоль с чипом)
![Hekate](res/sysnand_wipe/hekate.bmp)
2. Перейдите во вкладку **emuMMC**
3. Обратите внимание на строчку `Type:`
=== "SD File"
    Так выглядит **файловый Эмунанд**
    ![Файловый Эмунанд](res/new_sd/file_emuMMC.bmp)

=== "SD Raw Partition"
    Так выглядит **Эмунанд на разделе**
    ![Эмунанд на разделе](res/new_sd/partition_emuMMC.bmp)

=== "Disabled"
    Так выглядит **отсутствие эмунанда**
    ![Отсутствие Эмунанда](res/new_sd/no_emuMMC.bmp)
    !!! danger "Эмунанд"
    У вас отсутствует Эмунанд. Настоятель рекомендуется сделать [очистку системы от следов](sysnand_wipe.md) пиратства и [создать Эмунанд](..ultra_wiki/backup_emuMMC.md#emunand-emunand).

## Переход на другую SD карту

=== "Файловый эмунанд"
    1. Скачайте программу [Rufus](https://rufus.ie/)
    2. Вставьте новую карту памяти в картридер и подключите его в ПК
    3. Откройте **Rufus** и настройки для форматирования SD карты, как на скриншоте
    ![Настройки форматирования](res/new_sd/rufus_settings.bmp)
    4. Нажмите на кнопку **Старт**
    5. Скопируйте всё содержимое прошлой карты памяти на новую
    
=== "Эмунанд на разделе"
    1. Войдите в **Hekate**(кнопка уменьшения громкости при включении консоли, если консоль с чипом)
    ![hekate](res/new_sd/hekate.bmp) 
    2. Перейдите в раздел **Tools**
    ![hekate tools](res/new_sd/hekate_tools.bmp)
    3. Перейдите в **Backup eMMC**
    ![Backup eMMC](res/new_sd/backup_eMMC.bmp)
    4. Переключите SD emuMMC RAW Partition на ON
    ![SD emuMMC RAW Partition backup](res/new_sd/switch_backup.bmp)
    5. Сделайте бэкап Эмунанда выбрав по порядку **SD emuMMC BOOT0 & BOOT1** и **SD emuMMC RAW GPP**
    ![Backup emuMMC](res/new_sd/backup_emuMMC.bmp)
    6. Скачайте **[Ultra-Nx](https://github.com/Ultra-NX/UltraNX/releases/latest/download/Ultra.zip)**
    7. Распакуйте архив на карту памяти
    8. Карта памяти должна выглядеть так
    ![Содержимое карты памяти](res/new_sd/sd_card.png)
    9. Скопируйте папку `backup` на новую карту памяти
    10. На новой карте перейдите в папку `backup/NAND_ID/emummc` скопируйте все файлы из этой папки в `backup/NAND_ID/restore`
    11. Вставьте SD карту в консоль и войдите в **Hekate**(кнопка уменьшения громкости при включении консоли, если консоль с чипом)
    ![hekate](res/new_sd/hekate.bmp)
    12. Перейдите в раздел **Tools**
    ![hekate tools](res/new_sd/hekate_tools.bmp)
    13. Перейдите в **Partition SD Card**
    ![Partition SD Card](res/new_sd/partition_sd_card.bmp)
    14. Нажмите **OK**
    ![Бэкап файлов](res/new_sd/partition_backup.bmp)
    15. Потяните ползунок **emuMMC** выбрав размер Эмунанда на прошлой карте памяти
    16. Нажмите **Next Step** и согласитесь на создание раздела под Эмунанд
    ![Создание раздела под Эмунанд](res/new_sd/next_step.bmp)
    17. После создания раздела вернитесь на вкладку **Tools**
    18. Перейдите в **Restore eMMC**
    ![Restore eMMC](res/new_sd/restore_eMMC.bmp)
    19. Переключите SD emuMMC RAW Partition на ON
    ![SD emuMMC RAW Partition backup](res/new_sd/switch_restore.bmp)
    20. Восстановите бэкап Эмунанда выбрав по порядку **SD emuMMC BOOT0 & BOOT1** и **SD emuMMC RAW GPP**
    ![Backup emuMMC](res/new_sd/restore_emuMMC.bmp)
    21. Удалите всё с новой карты памяти
    22. Переместите всё содержимое с прошлой карты на новую
    
=== "Без Эмунанда"
    1. Скачайте программу [Rufus](https://rufus.ie/)
    2. Вставьте новую карту памяти в картридер и подключите его в ПК
    3. Откройте **Rufus** и настройки для форматирования SD карты, как на скриншоте
    ![Настройки форматирования](res/new_sd/rufus_settings.bmp)
    4. Нажмите на кнопку **Старт**
    5. Скопируйте всё содержимое прошлой карты памяти на новую