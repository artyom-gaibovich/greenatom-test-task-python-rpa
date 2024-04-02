# Проект FastAPI и SQLite

Тестовое задание на позицию Python RPA, Компания Greenatom

## Установка

1. git clone https://github.com/yourusername/yourrepository.git
2. python -m venv venv
3. venv/Scripts/activate
4. pip install -r requirements.txt

## Запууск

uvicorn main:app --reload

## Тестирование

1. Swagger - http://127.0.0.1:8000/docs
2. `/start_robot/{start_number:int}` - Эндпоинт для запуск робота
3. `/stop_robot` - Эндпоинт для остановки робота
4. `/runs` - Эндпоинт для получения информации о id, start_number, start_time(время запуска), duration(длительность)



## Описание задания
### Задание:
* Программа должна работать и запускаться под Windows.
* Перед началом работы необходимо инициализировать git-репозиторий, чтобы мы могли посмотреть, как шла работа над проектом. 
* Необходимо написать бекэнд веб-сервиса на FastAPI, который способен запускать и останавливать робота.
* Робот – это Python-скрипт, который также необходимо написать. Он должен работать отдельно и независим
* Робот при запуске должен принимать параметр командной строки – с какого числа начинать отсчет (по умолчанию – с нуля). В веб-сервисе на FastAPI должна быть возможность передать это число.
* Программа должна хранить информацию о времени и длительности каждого запуска в базе данных (SQLite), а также информацию о том, с какого числа был начат отсчёт. FastAPI должен иметь дополнительный эндпоинт для вывода этой информации.