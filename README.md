# Zapret (обход блокировки Discord'а и Youtube'а а также всех заблокированных сайтов в РФ)

 [!NOTE]  
> Данный репозиторий кастомный и работает почти на все заблокированные сайты в РФ. Так как zapret open-source, вы всегда можете сами собрать эти бинарники и не бояться вирусов. \
Будут рад [⭐ поставленной звезде](https://github.com/Flowseal/zapret-custom/stargazers) (в правом верхнем углу) у репозитория 🙂

##

> [!CAUTION]  
> **Многие антивирусники** в данный момент жалуются на ***HackTool/RiskTool*** и ***WinDivert*** - это нормальное поведение, так как программа изменяет сетевые пакеты. Что с этим делать? Собрать бинарники самому из исходников, довериться уже собранным, либо не использовать вовсе.

## Guides
### Windows
> [!IMPORTANT]  
> Если всё еще не скачан, то скачайте последний [релиз](https://github.com/sillycat-org/zapret-custom/releases), разархивируйте в отдельную папку.

Запустите **от имени администратора** то, что вам нужно:
- **`discord.bat`** - запустить обход дискорда.
- **`general.bat`** - запустить обход дискорда и ютуба.
  * Если обход не работает, пробуйте по порядку **`general (ALT ..).bat`** (также можете проверить стратегию на **МГТС**)
###
- **`service_install.bat`** - установить на автозапуск (в сервисы) любую стратегию из этого репозитория (стратегия **НЕ** должна начинаться со слова `service`)
###
- **`service_goodbye_discord.bat`** - запустить, если вы используете **СЕРВИС goodbyedpi**, и хотите, чтобы zapret обходил **только discord**.
  * **ВНИМАНИЕ**: Запускать ПОСЛЕ создания сервиса goodbyedpi. Первый раз goodbyedpi может вылететь - просто перезапустите устройство!
###
- **`service_remove.bat`** - остановить и удалить сервисы выше
- **`general.bat`** - рекомендуется к установке

## Решение проблем

- Проверьте, запускаете ли вы файлы от **ИМЕНИ АДМИНИСТРАТОРА**
- Не запускаются bat файлы? Попробуйте запустить **`service_remove.bat`** от **ИМЕНИ АДМИНИСТРАТОРА**
  * Также отключите программы, которые могут мешать созданию сервиса *(Антивирусы, клинеры с доп. защитой)*.
- <p style="text-align: left;">
    <img src="https://cdn-icons-png.flaticon.com/16/3670/3670147.png" alt="discord" style="vertical-align: middle;"/>
    Не работает <strong>Youtube</strong>? Попробуйте найти ответ здесь - 
    <a href="https://github.com/Flowseal/zapret-discord-youtube/discussions/251">Обсуждение YouTube</a>
  </p>
- <p style="text-align: left;">
    <img src="https://cdn-icons-png.flaticon.com/16/906/906361.png" alt="discord" style="vertical-align: middle;"/>
    Не работает <strong>Discord</strong>? Попробуйте найти ответ здесь - 
    <a href="https://github.com/Flowseal/zapret-discord-youtube/discussions/252">Обсуждение Discord</a>
  </p>
##
- Не работает вместе с **VPN**? Отключите функцию **TUN** (Tunneling) в настройках VPN.
- Не работает **`service_goodbye_discord`**? Удостовертесь, что сервис goodbyedpi запущен и имеет название GoodbyeDPI. После снова запустите `service_goodbye_discord.bat` и перезапустите устройство.
- Попробуйте обновить бинарники с оригинального репозитория.

### Остановка и удаление обхода
Для этого запустите **`service_remove.bat`**.
- Если WinDivert так и не удалился, узнайте его название с помощью команды `driverquery | find "Divert"` в cmd, а затем удалите данными командами (заместо WinDivert введите название, которые вы узнали):
```
sc stop WinDivert
sc delete WinDivert
```

### Добавление дополнительных адресов заблокированных сайтов 
- Список можно дополнить используя `list-general.txt` (для файлов `general`) и в список `list-discord` (для файлов `discord`).
> [!IMPORTANT]  
> После добавления сервис нужно перезапустить.

## Linux
К сожалению на данный момент нету установки на линукс.

* Many thanks to [bol-van](https://github.com/bol-van/), creator of original [zapret](https://github.com/bol-van/zapret/) repository.
