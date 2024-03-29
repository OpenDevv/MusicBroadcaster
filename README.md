﻿
# MusicBroadcaster

Трансляция музыки в видеочат telegram.


## Запуск проекта
1.1. Установка пакетов.

Для запуска проекта на linux используйте следующие шаги:

```bash
  sudo apt update
  sudo apt upgrade
```
Установка nodejs: 

```bash
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh
```

```
  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
```

```bash
  source ~/.bashrc
```

```bash
  nvm install v19.0.0
```

Проверьте правильнось установки:

```bash
  nvm list
  
  # Output
  # ->     v19.0.0
  #        v19.0.0
  # default -> v19.0.0
  # iojs -> N/A (default)
  # unstable -> N/A (default)
  # node -> stable (-> v19.0.0) (default)
  # stable -> 19.0 (-> v19.0.0) (default)
  # . . .
```

Если установка прошла некорректно, или была установлена версия ниже 15, выполните:
```bash
  sudo apt remove nodejs
```

```bash
  sudo apt autoremove
```

После установки необходимых компоненов установите библиотеки:

```bash
  pip3 install -r requirements.txt
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

Перейдите на https://my.telegram.org/apps.

Заполните форму и получите значения для config.py

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
