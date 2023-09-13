## **8. Запитання для співбесіди на тему CI CD**

---

## 8. CI CD
[Back to top ⬆️](#8-ci-cd)

- [1. Що таке CI/CD](#1-ci-cd)
- [2. Послідовність виконання CI/CD процесу на проекті](#2-cd)
- [3. Як автоматичне тестування інтегрується в CI](#3-ci)
- [4. Які інструменти для генерації репорту після виконання автоматичних тестів ви знаєте](#4)
- [5. Яку інформацію має містити звіт про виконання автоматичних тестів](#5)

---

# Відповіді - 'CI/CD'

[Back to top ⬆️](#8-ci-cd)
### 1. Що таке CI/CD
* Безперервна інтеграція (Continuous Integration/CI)* - методологія розробки та набір практик, у яких код вносяться невеликі зміни з частими комитами. Оскільки більшість сучасних додатків розробляються з використанням різних платформ та інструментів, то виникає потреба в механізмі інтеграції та тестуванні змін, що вносяться.
Мета CI — забезпечити послідовний та автоматизований спосіб складання, пакування та тестування додатків.

* Безперервне постачання (Continuous Delivery/CD)* - ґрунтується на автоматизації складання та тестування, яке вводить безперервна інтеграція. Вона передбачає переведення ручних кроків, необхідних для випуску складання додатків у продакшн, на автоматизований процес.

*Безперервне розгортання (Continuous Deployment/CD)* - після автоматизації релізу залишається один ручний етап: схвалення та запуск розгортання в продакшен. Практика безперервного розгортання скасовує це, не вимагаючи безпосереднього затвердження з боку розробника. Усі зміни автоматично розгортаються.


[Back to top ⬆️](#8-ci-cd)
### 2. Послідовність виконання CI/CD процесу на проекті

1. Написання коду
2. Складання
3. Тестування
4. Реліз
5. Розгортання
6. Підтримка та моніторинг
7. Планування

![IMG](images/CI_CD.png)


[Back to top ⬆️](#8-ci-cd)
### 3. Як автоматичне тестування інтегрується в CI
Безперервна інтеграція та безперервне постачання потребують безперервного тестування. Безперервне тестування часто реалізується у вигляді набору різних автоматизованих тестів (регресійних, продуктивності та інших), які виконуються у CI/CD-конвеєрі.


[Back to top ⬆️](#8-ci-cd)
### 4. Які інструменти для генерації репорту після виконання автоматичних тестів ви знаєте
* Allure, Serenity *


[Back to top ⬆️](#8-ci-cd)
### 5. Яку інформацію має містити звіт про виконання автоматичних тестів
Виходячи з пріоритетів цільової аудиторії, ми маємо визначити, яку інформацію має містити звіт. Відповідно, в ході проекту інформація повинна консолідуватися за тим напрямком, який необхідно відобразити.
Ми можемо виділити три групи цільових аудиторій:
1. Технічні користувачі - Test-manager. Для них пріоритетне розуміння ходу тестування, які виникають проблеми, як вони вирішуються, побудова самого процесу тестування, опис методів і технологій, що застосовуються.
2. Product Manager, вони ж Менеджери продукту. Їх фокус сконцентрований на термінах виконання, вичавках із результатів тестування без зайвих технічних подробиць та на загальній статистиці (цифрові та порівняльні метрики).
3. Бізнес-користувачі. Зазвичай це є ті люди, які приймають рішення щодо завершення тестування. Вони ж визначають якість виконаної роботи. Для них, насамперед, важливим є кінцевий результат у максимально короткому та ясному форматі (так\ні), наочне подання інформації (графіки, діаграми), експертна думка про можливість випуску продукту в промислове середовище тощо, без поглиблення в деталі .