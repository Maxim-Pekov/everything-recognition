# everything-recognition

Это скрипт нужен для распознования людей, лиц ( в анфас и профиль ), глаз, улыбок и морды кошек в режиме реального времени на видео.

## Как он работает:

1. Вы запускаете скрипт командой ниже, если камера неисправна или отсутствует, вы увидете сообщение `"Couldn't find your webcam... Sorry "`, для завершения работы программы нажмите `q`.

```python
python3 run.py
```

## Инструкция по установке

Используйте данную инструкцию по установке этого скрипта, на компьютере с установленным python3.

1. Установить

```python
git clone https://github.com/Maxim-Pekov/everything-recognition.git
```

2. Создайте виртуальное окружение:

```python
python -m venv venv
```

3. Активируйте виртуальное окружение:
```python
.\venv\Scripts\activate`    # for Windows
```
```python
source ./.venv/bin/activate    # for Linux
```

4. Перейдите в `everything-recognition` директорию.

3. Установите зависимости командой ниже:
```python
pip install -r requirements.txt
```

---

## Инструкция по настройке

Используйте данную инструкцию для настройки параметров поиска по видео.

1. Для детальной настройки откройте скрипт `config.py`.
2. Внутри этого файла есть словарь, ключи которого, это параметры по которым будет проходить поиск по видео.
    
    Для включения поиска по выбранному ключу пропишите напротив ключа 'draw':  значение True3. 

    Для отключения поиска по выбранному ключу, пропишите напротив ключа 'draw':  значение False

    Пример кода:
    
```python
   "Face front": {
        "path": "haarcascades/faces/haarcascade_frontalface_default.xml",
        "color": (255, 0, 0),
        "draw": True
    },
```