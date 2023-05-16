# Космо-телеграмм

Этот проект поможет вам загрузить в телеграмм канал фото от NASA_APOD, spaceX и NASA_EPIC.

### Как получить API-ключ от NASA и  ID от spaceX

Для того, чтобы получить API-ключ от NASA_APOD, Вам нужно зарегистрироваться на [сайте](https://api.nasa.gov/#apod). API-ключ отправят Вам на почту. А как его добавлять в переменную окружения, Вы можете прочитать [тут](https://github.com/NikaKurnakov/bitly) в разделе "Переменные окружения".

После вам надо получить API-ключ от NASA_EPIC. Вам также надо зарегистрироваться [здесь](https://api.nasa.gov/#epic). API-ключ Вам так же отправят на почту. Его тоже надо записать в переменную окружения.

ID для spaceX можете использовать вот этот `5eb87d46ffd86e000604b388`. Тип данных ID `str`. Он должен храниться в переменной окружения.
Файл `.env`, в который вы записывали переменные окружения, надо добавить в файл `.gitignore`. 

### Запуск файла get_epic_image.py

Затем, когда разобрались с переменными, надо запустить код. Если у вас Windows и есть API-ключ, то он запускается так:

```
py get_epic_image.py.py --token_epic ваш_токен
```

Если у вас Linux, то код будет запускаться почти так же, только вместо `py` будет `python`:

```
python get_epic_image.py.py --token_epic ваш_токен
```

### Запуск файла get_nasa_image.py

Запуск этого файла будет похож на запуск файла `get_epic_image.py`, только название будет другое:

```
py get_nasa_image.py --token_nasa ваш_токен
```

Так же и на Linux:

```
python get_nasa_image.py --token_nasa ваш_токен
```

### Запуск файла get_spaceX.py

Для этого запуска вам нужен id:

```
py get_spaceX.py --id ваш_id
```

### Зависимости

Python3 должен быть уже установлен.
Затем используйте `pip` (или `pip3`, есть конфликт с Python2) для 
установки зависимостей:

```
pip install -r requirements.txt
```
