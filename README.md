Weather Utility
Description
This Python utility fetches current weather information for a specified location using the wttr.in service. It can display weather details in the terminal and optionally save a weather forecast image (PNG format).

Features
Get current weather data in JSON format from wttr.in
Display key weather information (temperature, description, wind, humidity, pressure, visibility)
Save the weather forecast as a PNG image
Command-line argument support
Error handling for network requests and data parsing
Requirements
Python 3.x
requests library (pip install requests)
Usage
Run the script from the command line:

bash


1
python weather_utility.py [-h] [-c CITY] [--image] [--filename FILENAME]
Arguments
-h, --help: Show help message and exit
-c CITY, --city CITY: Location for which to get weather (default: Томск)
--image: Save the weather forecast as a PNG image
--filename FILENAME: Filename for the saved image (default: <city>.png)
Examples
Get weather for the default city (Томск):
bash


1
python weather_utility.py
Get weather for a specific city:
bash


1
python weather_utility.py -c "Moscow"
Get weather and save the forecast image:
bash


1
python weather_utility.py -c "Saint Petersburg" --image
Get weather, save the image with a custom filename:
bash


1
python weather_utility.py -c "Novosibirsk" --image --filename "nsk_weather.png"
Code Structure
get_weather(location): Fetches and prints weather data
save_image(location, filename): Downloads and saves the weather image
main(): Parses command-line arguments and runs the utility
Notes
The utility uses the Russian language (lang=ru) for weather descriptions by default.
Weather data is also saved to a local file named data.txt.
Ensure you have an internet connection to fetch data from wttr.in.
Русская версия:

Утилита для получения прогноза погоды
Описание
Эта утилита на Python получает текущую информацию о погоде для указанного места с помощью сервиса wttr.in . Она может отображать данные о погоде в терминале и при необходимости сохранять изображение прогноза погоды (формат PNG).

Возможности
Получение текущих данных о погоде в формате JSON с wttr.in
Отображение основной информации о погоде (температура, описание, ветер, влажность, давление, видимость)
Сохранение прогноза погоды в виде изображения PNG
Поддержка аргументов командной строки
Обработка ошибок сетевых запросов и разбора данных
Требования
Python 3.x
Библиотека requests (pip install requests)
Использование
Запустите скрипт из командной строки:

bash


1
python weather_utility.py [-h] [-c CITY] [--image] [--filename FILENAME]
Аргументы
-h, --help: Показать справку и выйти
-c CITY, --city CITY: Местность, для которой нужно узнать погоду (по умолчанию: Томск)
--image: Сохранить прогноз погоды в виде изображения PNG
--filename FILENAME: Имя файла для сохранения изображения (по умолчанию: <city>.png)
Примеры
Получить погоду для города по умолчанию (Томск):
bash


1
python weather_utility.py
Получить погоду для определенного города:
bash


1
python weather_utility.py -c "Москва"
Получить погоду и сохранить изображение прогноза:
bash


1
python weather_utility.py -c "Санкт-Петербург" --image
Получить погоду, сохранить изображение с пользовательским именем файла:
bash


1
python weather_utility.py -c "Новосибирск" --image --filename "nsk_weather.png"
Структура кода
get_weather(location): Получает и выводит данные о погоде
save_image(location, filename): Загружает и сохраняет изображение погоды
main(): Анализирует аргументы командной строки и запускает утилиту
Примечания
Утилита по умолчанию использует русский язык (lang=ru) для описания погоды.
Данные о погоде также сохраняются в локальный файл data.txt.
Убедитесь, что у вас есть подключение к Интернету для получения данных с wttr.in.
