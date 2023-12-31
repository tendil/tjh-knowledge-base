---
search:
  exclude: true
---

# Инструкция по использованию парсеров в телеграм боте @TJH_parser_bot

## Как запустить телеграм бот?
1. **Перейдите в телеграм по ссылке [TJH_parser_bot](https://t.me/TJH_parser_bot).**  

2. **Пройдите минимальную авторизацию, используя пароль, который можно получить у администратора - [ссылка на администратора](https://t.me/XllrepoDewelloper). Если не работает или вас заблокировал бот, обратитесь к администратору.**

3. **В главном меню доступны 7 кнопок:**
     - Djinni парсер
     - GlassDoor парсер
     - DOU парсер
     - Telegram chat парсер
     - Help
     - Список чатов Telegram
     - Цитатка

## 4. **Запуск парсера Djinni:**
      1. Нажмите на кнопку Djinni парсер.
      2. Выберите один из вариантов запуска.
         - Запуск с указанием своего URLS
      3. Если вы хотите указать ссылку на страницу со своими фильтрами, нажмите 'Указать свой URLS'.
      4. Введите ссылку в формате, например: `salary=3500&primary_keyword=Artist`.
      5. Бот отправит уведомление о начале парсинга и по окончании удалит его.
      6. После завершения, бот покажет сообщение с ссылкой на Google Sheets, количеством новых вакансий и отправит лог файл.
      7. После завершения, вернетесь в главное меню.

## 5. **Запуск парсера GlassDoor:**
      1. Нажмите на кнопку GlassDoor парсер.
      2. Выберите вариант запуска: Стандартный запуск или Запуск с указанием своего URLS.
      3. Для стандартного запуска, дождитесь завершения и получите уведомление.
      4. Для своих фильтров, введите ссылку, например: `Job/human-resources-jobs-SRCH_KO0,15.htm`.
      5. Бот отправит уведомление о начале парсинга и по окончании удалит его.
      6. После завершения, бот покажет сообщение с ссылкой на Google Sheets, количеством новых вакансий и отправит лог файл.
      7. После завершения, вернетесь в главное меню.

## 6. **Запуск парсера DOU:**
      1. Нажмите на кнопку DOU парсер.
      2. Выберите вариант запуска: Запуск с указанием своего URLS.
      3. Для своих фильтров, введите ссылку, например: `category=QA&exp=3-5`.
      4. Бот отправит уведомление о начале парсинга и по окончании удалит его.
      5. После завершения, бот покажет сообщение с ссылкой на Google Sheets, количеством новых вакансий и отправит лог файл.
      6. После завершения, вернетесь в главное меню.

## 7. **Информационная кнопка Help:**
    - Нажмите на кнопку 'Help' для получения инструкции и описания бота.
    - Бот отправит сообщение с описанием функционала и инструкцией в текстовом файле.
    - После прочтения, данные сообщения удалятся автоматически.

## 8. Запуск парсера сообщений с телеграмм чата:
      1. В главном меню нажмите на кнопку 'Telegram chat парсер'.
      2. Введите ссылку на телеграмм чат в формате, например: [https://t.me/itrecruit_ua](https://t.me/itrecruit_ua).
      3. Затем введите ключевые слова, по которым бот будет искать сообщения, например: python, php, laravel, java.
      4. Укажите количество сообщений, которое вы хотите записать в таблицу.
      5. Бот начнет процесс сбора сообщений и записи их в Google Sheets на лист 'telegram'.

## 9. **Кнопка 'Цитатка':**
      1. При нажатии на нее, бот отправит случайную шутку, мотивирующую цитату или анекдот про программистов для поднятия настроения.

***Все данные парсинга сохраняются в Google Sheets и доступны по ссылкам в сообщениях бота.***


### ПРИМЕЧАНИЕ:

### **1. Автоматические функции для комфортного пользования:**
    - Автоматическое удаление ненужных сообщений, включая сообщение с паролем при старте, сообщение о начале работы парсера и информационное сообщение после нажатия на кнопку 'Help'.
    - Отправка ботом Log файла для отслеживания его работы.
    - Возможность вернуться в главное меню с любого шага парсинга (кроме периода активной работы парсера).
    - Минимальная авторизация при первом запуске бота и при дальнейших вызовах команды /start для защиты данных.


### **2. Что не надо делать, чтобы не сбить работу парсеров:**
     - Не нажимать на кнопку старта парсера без соответствующего сообщения от бота, чтобы избежать запуска нескольких процессов парсинга.
     - Не отправлять текстовые сообщения боту, использовать только кнопки для управления.
     - Не менять названия колонок, порядок колонок и другие параметры, так как они привязаны к коду и могут вызвать сбой парсера.
     - Не запрещать доступ боту к Google Sheets, который используется для хранения данных.
     - Не менять название рабочего листа в таблице.

***Если вам потребуется внести изменения, в коде оставлены комментарии, которые помогут вам внести необходимые корректировки, чтобы код продолжал работать корректно.***
