# **Инструкция по использованию Gitflow**

## **Введение**
Gitflow - это успешная модель ветвления Git, предназначенная для управления и организации разработки программного обеспечения. Она помогает командам эффективно управлять версиями, поддерживать стабильность кодовой базы и сделать процесс совместной разработки более прозрачным и управляемым.

## **Цели использования Gitflow:**
- Управление версиями: Легкость создания и отслеживания релизов.
- Совместная разработка: Возможность параллельной разработки новых функций и исправлений ошибок.
- Стабильность: Обеспечение стабильности кодовой базы на основной ветке `main`.
- Отслеживание функциональности: Четкое отслеживание того, какие функции находятся в разработке, на тестировании и в производстве.

### **Основные ветки**
1. `main`:
    - Основная ветка, которая содержит только стабильные версии программы.
    - Никакой прямой код не пишется в этой ветке.
    - Все коммиты должны быть помечены тегами с версией.
    - Влитие в main должно происходить только через слияние с веткой `release`.
2. `develop`:
    - Ветка, в которой разрабатывается последняя версия программы.
    - Все новые функции и исправления ошибок начинаются с этой ветки.
    - Слияния в develop могут выполняться только после успешного завершения code review и тестирования.

### **Вспомогательные ветки**
1. `feature/{feature-task-id}`:
    - Используется для разработки новых функций или улучшений.
    - Каждая функция должна начинаться с отдельной ветки.
    - После завершения разработки функции, она объединяется обратно в `develop`.
2. `hotfix/{hotfix-name}`:
    - Используется для немедленного исправления критических ошибок на продуктивной среде.
    - После исправления ошибки, изменения также сливаются обратно в `develop` и `main`.
3. `release/{release-version}`:
    - Подготавливает новую версию программы перед выпуском.
    - В этой ветке происходит окончательное тестирование и исправление ошибок.
    - После завершения тестирования, ветка объединяется в `main` и `develop`, и создается новый тег с версией.

## **Шаги для базового использования Gitflow**
1. Начало новой функции:
```bash
git checkout develop
git pull origin develop
git checkout -b feature/{feature-task-id}
### Работайте над функцией, фиксируйте изменения
git add .
git commit -m "Add comments about feature"
git push origin feature/{feature-task-id}
```
2. Завершение функции и объединение в develop:
```bash
git checkout develop
git pull origin develop
git merge --no-ff feature/{feature-task-id}
git push origin develop
```
3. Исправление критических ошибок (hotfix):
```bash
git checkout main
git pull origin main
git checkout -b hotfix/{hotfix-name}
### Исправьте ошибку
git add .
git commit -m "Add comments about what was fix"
git checkout main
git merge --no-ff hotfix/{hotfix-name}
git push origin main
git checkout main
git merge --no-ff hotfix/{hotfix-name}
git push origin main
```
4. Подготовка к релизу:
```bash
git checkout develop
git pull origin develop
git checkout -b release/{release-version}
### Тестирование и исправление ошибок
git add .
git commit -m "Release preparations"
git checkout main
git merge --no-ff release/{release-version}
git tag -a v1.0 -m "Release version 1.0"
git push origin main --tags
git checkout develop
git merge --no-ff release/{release-version}
git push origin develop
```
5. Завершение релиза:
```bash
### После успешного тестирования
git checkout main
git pull origin main
git merge --no-ff release/{release-version}
git push origin main
git checkout develop
git merge --no-ff release/{release-version}
git push origin develop
```
