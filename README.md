
# TelegramCallsStream

Трансляция музыки в видеочат telegram.


## Запуск проекта
1.1. Установка пакетов.

Для запуска проекта на linux используйте следующие шаги:

```bash
  sudo apt update
  sudo apt upgrade
```
Установка nodejs: https://www.digitalocean.com/community/tutorials/how-to-install-node-js-on-ubuntu-20-04

После установки необходимых компоненов установите библиотеки:

```bash
  pip3 install py-tgcalls -U
```
```bash
  pip3 install pyrogram
```
```bash
  pip3 install beautifulsoup4
```

Установите FFmpeg:
```bash
  sudo apt update && sudo apt upgrade
```
```bash
  sudo apt install ffmpeg
```
```bash
  ffmpeg -version
```

1.2. Запуск скрипта.

Установите в config.py свои значения:

```python
api_id = 1234567
api_hash = "24b12...31nb2"
number = '+79008007060'
```

Запустите client.py:

```bash
  python3 client.py
```

2.1. Добавление в telegram.

Выполните следующие шаги:

- Сделайте пользователя из config.py администратором чата.
- Запустите видеочат.
- Напишите в чат /stream для запуска трансляции. (Возможно, сработает не с первого раза)
- Наслаждайтесь музыкой.


## FAQ

#### Как переключить трек?

Для переключения треков существует несколько команд:

- /next (1)
- /song {sognNumber} (2)
Команда /next используется для перехода к следующему по списку треку. Не принимает никаких аргументов.

Команда /sogn {sognNumber} используется для перехода к треку с определённым номером в списке.

Принимает аргумент songNumber (integer).
