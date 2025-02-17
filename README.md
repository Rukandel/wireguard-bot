<h1 align="center">VPN bot</h1>
<p align="center">
<img src = "https://github.com/Rukandel/wireguard-bot/blob/master/logo.jpg" width = 70%>
</p>

<div align="center">

[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Packaged with Poetry](https://img.shields.io/badge/packaging-poetry-cyan.svg)](https://python-poetry.org/)<br>
[![!Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)](https://ubuntu.com/)
[![!Debian](https://img.shields.io/badge/Debian-A81D33?style=for-the-badge&logo=debian&logoColor=white)](https://www.debian.org/)
[![!Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![!PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![!Wireguard](https://img.shields.io/badge/Wireguard-88171A?style=for-the-badge&logo=wireguard&logoColor=white)](https://www.wireguard.com/)
[![!AdGuard](https://img.shields.io/badge/AdGuard-00A6D6?style=for-the-badge&logo=adguard&logoColor=white)](https://adguard.com/)
[![!Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://telegram.org/)

</div>

## Описание

 Бот сделан в качестве пет проекта, задачей было сделать чат-бота в телеграмме, с помощью которого было бы можно управлять ВПН сервером

## Stack

python 3.10, aiogram <br/>
Database: postgresql<br/>
VPN: WireGuard<br/>


### Скрипт для установки(необходимо копировать и запустить в терминале сервера)
```bash
   wget https://raw.githubusercontent.com/Rukandel/wireguard-bot/master/SemiAutoInstall.sh && chmod +x SemiAutoInstall.sh && ./SemiAutoInstall.sh
   ```



### Команды

1. `/give <user_id> <days>` - Дает подписку пользователю на определенное количество дней \<days> days.<br/>
   Также можете использовать \<@username> instead of \<user_id>.<br/>
 Если хотите отключить пользователя от бота, то: `/give <user_id> -9999` or any negative number that will be higher than user's access expiration date.<br/>
   <b>WARNING:</b> disconnecting user will not remove his access from database, so you can give him access again later.<br/>
   Пример: `/give 123456789 30` - give user with id 123456789 access to VPN for 30 days.
2. `/stats` - показывает статистику по серверу.<br/>
   Aviable options: `/stats active` - show active users.<br/>
   `/stats inactive` - show inactive users.<br/>
   `/stats` without options will show all users.<br/>
   `/wgrestart` - restart wireguard service


## TODO
1. Для получения автоматического сервиса необходимо подключить эквайринг(не техническая работа)
2. Подключить nginx и сделать балансировку нагрузки по серверам


