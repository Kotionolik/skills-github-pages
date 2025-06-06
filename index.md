---
title: Welcome to my blog
---
# Фомин Фёдор Вадимович, задание 1

## Задание 2 ЛР№3

**«Программное обеспечение»**: id, название; название компании производителя; год выхода; версия; период поддержки; цена.

Выполнить запросы:

* Вывести данные о программном обеспечении, которое дороже 60 рублей и период поддержки которого более 3 лет.

* Используя инструкцию alter, добавить дополнительные столбцы, один из которых category_id (тип integer и содержит идентификаторы категорий программного обеспечения).

* Создать таблицу category (id, cat_name, cat_description) для категорий «Прикладное ПО» и «Системное ПО».

* Вывести данные обо всех ПО в форме идентификатор программного обеспечения, названия, год выхода, название категории ПО.

* подсчет количества ПО с помощью count, если период поддержки <=5 лет.

* суммарная стоимость ПО с помощью sum, если год выхода>2011

* максимальная и минимальная стоимость с помощью max и min.

* Используя инструкцию inner join вывести полные сведения о ПО и категории для категории «Прикладное программное обеспечение».

## Диаграмма вариантов использования

![Диаграмма вариантов использования](https://github.com/user-attachments/assets/d9097f51-362d-480e-a56e-fed80517a075)

### Пример текстового сценария для варианта использования:

**Вариант использования «Формирование отчетов»:**

**Краткое описание:** Данный вариант использования позволяет пользователю сформировать отчеты по базам данных ПО и их категорий с учетом заданных условий.

**Область:** Система.

**Уровень:** Цель пользователя.

**Основной актер:** Пользователь.

**Предусловия:**
* Пользователь должен быть авторизован в системе;
* В БД "Программное Обеспечение" есть записи о ПО.

**Успешное постусловие:** Отчет успешно сгенерирован и отображён.

**Минимальные гарантии:** Отчет не сформирован.

**Триггер:** Нажатие кнопки "Сформировать Отчет."

**Основной Сценарий:**
1. Пользователь вводит нужные параметры формирования отчета.
2. Пользователь запускает формирование отчета.
3. Система проверяет параметры формирования отчета.
4. Система формирует SQL-запрос согласно параметрам.
5. Система выполняет SQL-запрос.
6. Система отображает полученный отчет.

**Расширения:**

* **2.a. Пользователь не вошел в систему:**
  - 2.а.1. Переход к сценарию входа в систему, завершение сценария формирования отчета.

* **3.a. Пользователь не ввел параметры формирования отчета:**
  - 3.а.1. Система формирует SQL-запрос для вывода всей таблицы "Программное Обеспечение".
  - 3.а.2. Переход сценария на пункт 5.

* **3.б. Пользователь неверно ввел параметры формирования отчета:**
  - 3.б.1. Система информирует пользователя о неправильности введенных параметров.
  - 3.б.2. Возврат сценария на пункт 1.

* **5.a. В таблице отсутствуют записи, удовлетворяющие условию:**
  - 5.а.1. Система информирует пользователя об отсутствии данных для отображения.
  - 5.а.2. Возврат сценария на пункт 1.

## Диаграммы деятельности
![Диаграмма аутентификации в приложении](https://github.com/user-attachments/assets/ca3df25a-bb42-4892-ad4c-dc347f0ecba0)

Данная диаграмма показывает действия программы при аутентификации в приложении.

![Диаграмма взаимодействия с БД](https://github.com/user-attachments/assets/7189b6c4-9f5b-4501-93d4-c65dbe9d37e4)

Данная диаграмма показывает действия программы при добавлении новой строки в таблицу БД.

## Диаграмма Классов
![Диаграмма Классов](https://github.com/user-attachments/assets/9f83a768-ba78-4d28-bec6-8451b7ef56c3)

Данная диаграмма показывает классы и взаимодействия между ними.

## Диаграмма Последовательности
![Диаграмма Последовательности](https://github.com/user-attachments/assets/c9aca730-6448-48e9-9587-1819faef0653)

Данная диаграмма показывает последовательность действий при работе программы
