# МИНИСТЕРСТВО ОБРАЗОВАНИЯ, НАУКИ И МОЛОДЕЖНОЙ ПОЛИТИКИ РЕСПУБЛИКИ КОМИ

Государственное профессиональное образовательное учреждение "Сыктывкарский политехнический техникум"

## Курсовая работа

Тема: База данных центра по продаже автомобилей.

 Срок представления работы к защите: 15 ноября 2024 года. 

Профессия/специальность

09.02.07 "Информационные системы и программирование" 

Выполнил

Шергин Даниил Максимович 
Дневная, 4 курс, 414 группа

"11" ноября 2024г.

Руководитель

Пунгин И.В.

__________________________________________
"11" ноября 2024г.

Сыктывкар 2024

## Содержание


## Ведение:

Актуальность темы создания базы данных центра по продаже автомобилей обусловлена растущей потребностью в эффективной организации и управлении информацией об автомобиле и его продажах. В условиях конкурентного рынка автомобильной торговли, эффективное администрирование клиентской информации, данных по автомобилям и сделкам становится необходимостью для достижения оптимальных результатов.

Целью данной курсовой работы является разработка базы данных, которая позволит централизованно хранить информацию о продаже автомобилей, клиентах и сделках, а также обеспечить простоту доступа к этой информации для сотрудников центра.

Задачи курсовой работы включают в себя:

1. Анализ требований: Изучение потребностей пользователей и формирование требований к базе данных.
2. Проектирование базы данных: Создание схемы базы данных с выделением ключевых сущностей и их атрибутов.
3. Реализация: Разработка базы данных с использованием системы управления базами данных (СУБД).
4. Тестирование: Проверка работоспособности базы данных и ее соответствия требованиям пользователей.
5. Документация: Подготовка документации по использованию и администрированию базы данных.

Реализация данной базы данных позволит улучшить управление продажами, оптимизировать рабочие процессы и повысить уровень сервиса для клиентов, что, в свою очередь, приведет к росту конкурентоспособности центра по продаже автомобилей.
База данных центра по продаже автомобилей: Анализ предметной области и постановка задачи




Содержание основной части курсовой работы включает:

## Анализ предметной области. Постановка задачи.

##  1.1. Описание предметной области и функции решаемых задач.
Предметная область включает в себя процесс продажи автомобилей, который охватывает взаимодействие с клиентами, управление запасами автомобилей, а также обработку сделок. База данных позволит автоматизировать следующие функции:

- Учёт автомобилей: Хранение информации о каждом автомобиле, включая марку, модель, год выпуска, цену, технические характеристики и статус (на складе, продан и т.д.).
- Управление клиентами: Сбор и хранение информации о клиентах, включая контактные данные, историю покупок и предпочтения.
- Обработка сделок: Учет всех продаж, включая даты, суммы, проданные автомобили, а также информацию о сотрудниках, которые произвели сделки.
- Анализ данных: Генерация отчетов по продажам, запасам и клиентской базе для выявления трендов и оптимизации бизнеса.
##  1.2. Перечень входных данных.
- Информация об автомобилях: марка, модель, год выпуска, VIN, цвет, цена, цена закупки, технические характеристики.
- Данные о клиентах: ФИО, контактная информация (телефон, электронная почта), адрес.
- Данные о сделках: дата продажи, цена продажи, способ оплаты, документы сделки.
##  1.3. Перечень выходных данных
- Отчеты по продажам (периодические, по моделям, по сотрудникам).
- Списки текущих автомобилей на складе с деталями.
- Информация о клиентах, включая историю покупок.
- Статистика по продажам (количество проданных автомобилей, выручка и т.д.).

## 1.4. Ограничения предметной области (если таковые имеются).
- Ограничение по количеству автомобилей, которые могут быть в продаже одновременно (например, в зависимости от размера склада).
- Необходимость соблюдения юридических норм и правил (например, регистрация автомобилей, налоги на продажу).
- Ограничения на хранение или обработку персональных данных клиентов в соответствии с законами о защите данных.
## 1.5. Взаимодействие с другими программами.
- CRM-системы: Для управления взаимоотношениями с клиентами и автоматизации процесса продаж.
- Бухгалтерские программы: Для учета финансовых операций и отчетности.
- Системы управления складами: Для контроля запасов автомобилей и управления поставками.
- Веб-сайты: Для интеграции с онлайн-продажами, включая отображение доступных автомобилей и принятие заявок от клиентов.

  Таким образом, анализ предметной области и постановка задачи позволяют четко определить цели и функциональность базы данных, что является основой для ее успешной реализации и использования.
База данных центра по продаже автомобилей: Инфологическая (концептуальная) модель базы данных

  Инфологическая (концептуальная) модель базы данных.

## 2.1. Выделение информационных объектов.
В рамках разработки базы данных центра по продаже автомобилей можно выделить следующие ключевые информационные объекты:

- Автомобиль
- Клиент
- Сделка
- Сотрудник
- Производитель
- Категория автомобиля

 ## 2.2. Определение атрибутов объектов.
Каждый из информационных объектов можно описать следующими атрибутами:

- Автомобиль
  - ID автомобиля (уникальный идентификатор)
  - Марка
  - Модель
  - Год выпуска
  - VIN (идентификационный номер)
  - Цвет
  - Цена
  - Статус (на складе, продан, зарезервирован)
  - Технические характеристики

- Клиент
  - ID клиента (уникальный идентификатор)
  - ФИО
  - Телефон
  - Электронная почта
  - Адрес
  - История покупок

- Сделка
  - ID сделки (уникальный идентификатор)
  - Дата продажи
  - Цена продажи
  - Способ оплаты
  - ID автомобиля (связь с автомобилем)
  - ID клиента (связь с клиентом)
  - ID сотрудника (связь с сотрудником)

- Сотрудник
  - ID сотрудника (уникальный идентификатор)
  - ФИО
  - Должность
  - Контактная информация

- Производитель
  - ID производителя (уникальный идентификатор)
  - Наименование
  - Страна

- Категория автомобиля
  - ID категории (уникальный идентификатор)
  - Название категории (например, легковые, внедорожники и т.д.)
 ## 2.3. Определение отношений и мощности отношений между объектами.
- Автомобиль - Производитель
  - Отношение: Один ко многим (один производитель может производить много автомобилей).
  
- Автомобиль - Категория автомобиля
  - Отношение: Один ко многим (одна категория может включать множество автомобилей).
  
- Клиент - Сделка
  - Отношение: Один ко многим (один клиент может совершить несколько сделок).
  
- Автомобиль - Сделка
  - Отношение: Один к одному (один автомобиль может быть продан в одной сделке).
  
- Сотрудник - Сделка
  - Отношение: Один ко многим (один сотрудник может оформлять несколько сделок).

## 2.4. Построение концептуальной модели.
онцептуальная модель базы данных может быть представлена в виде ER-диаграммы (сущность-связь), где каждую сущность вместе с её атрибутами и отношениями можно визуализировать. 

Поскольку текстовый формат не позволяет создавать графические изображения, следует представить концептуальную связь объектов в текстовом варианте:

- Автомобиль
  - ID автомобиля, Марка, Модель, Год выпуска, VIN, Цвет, Цена, Статус, Технические характеристики
    - связан с Производитель (ID производителя)
    - связан с Категория автомобиля (ID категории)

- Клиент
  - ID клиента, ФИО, Телефон, Электронная почта, Адрес
    - связан с Сделка (ID сделки)

- Сделка
  - ID сделки, Дата продажи, Цена продажи, Способ оплаты
    - связан с Автомобиль (ID автомобиля)
    - связан с Клиент (ID клиента)
    - связан с Сотрудник (ID сотрудника)

- Сотрудник
  - ID сотрудника, ФИО, Должность, Контактная информация

- Производитель
  - ID производителя, Наименование, Страна

- Категория автомобиля
  - ID категории, Название категории

Данная концептуальная модель задает основу для дальнейшей разработки реляционной модели базы данных и ее последующей реализации.
Логическая структура БД центра по продаже автомобилей**

Логическая структура базы данных представляет собой более детализированное представление концептуальной модели, которое включает таблицы, их атрибуты и связи между ними. 

**1. Таблицы и их атрибуты**

- **Таблица: Автомобили**
  - ID_автомобиля (PK)
  - Марка
  - Модель
  - Год_выпуска
  - VIN
  - Цвет
  - Цена
  - Статус
  - Технические характеристики
  - ID_производителя (FK)
  - ID_категории (FK)

- **Таблица: Клиенты**
  - ID_клиента (PK)
  - ФИО
  - Телефон
  - Электронная_почта
  - Адрес

- **Таблица: Сделки**
  - ID_сделки (PK)
  - Дата_продажи
  - Цена_продажи
  - Способ_оплаты
  - ID_автомобиля (FK)
  - ID_клиента (FK)
  - ID_сотрудника (FK)

- **Таблица: Сотрудники**
  - ID_сотрудника (PK)
  - ФИО
  - Должность
  - Контактная_информация

- **Таблица: Производители**
  - ID_производителя (PK)
  - Наименование
  - Страна

- **Таблица: Категории_автомобилей**
  - ID_категории (PK)
  - Название_категории

**2. Связи между таблицами**

- **Автомобили**:
  - Связаны с **Производителями**: ID_производителя в таблице «Автомобили» является внешним ключом (FK), ссылающимся на ID_производителя в таблице «Производители».
  - Связаны с **Категориями_автомобилей**: ID_категории в таблице «Автомобили» является внешним ключом (FK), ссылающимся на ID_категории в таблице «Категории_автомобилей».

- **Сделки**:
  - Связаны с **Автомобилями**: ID_автомобиля в таблице «Сделки» является внешним ключом (FK), ссылающимся на ID_автомобиля в таблице «Автомобили».
  - Связаны с **Клиентами**: ID_клиента в таблице «Сделки» является внешним ключом (FK), ссылающимся на ID_клиента в таблице «Клиенты».
  - Связаны с **Сотрудниками**: ID_сотрудника в таблице «Сделки» является внешним ключом (FK), ссылающимся на ID_сотрудника в таблице «Сотрудники».

  ## 3. Логическая структура БД.

Автомобили
  ID_автомобиля (PK)
  Марка
  Модель
  Год_выпуска
  VIN
  Цвет
  Цена
  Статус
  Технические характеристики
  ID_производителя (FK)
  ID_категории (FK)

Клиентыс
  Технические характеристики
  ID_производителя (FK)
  ID_категории (FK)

Клиенты
  ID_клиента (PK)
  ФИО
  Телефон
  Электронная_почта
  Адрес

   ID_клиента (PK)
  ФИО
  Телефон
  Электронная_почта
  Адрес

Сделки
  ID_сделки (PK)
  Дата_продажи
  Цена_продажи
  Способ_оплаты
  ID_автомобиля (FK)
  ID_клиента (FK)
  ID_сотрудника (FK)

Сотрудники
  ID_сотрудника (PK)
  ФИО
  Должность
  Контактная_информация

Производители
  ID_производителя (PK)
  Наименование
  Страна

Категории_автомобилей
  ID_категории (PK)
  Название_категории


Эта логическая структура базы данных служит основой для создания реляционной модели и впоследствии может быть использована для реализации базы данных на выбранной СУБД.
Физическая структура базы данных центра по продаже автомобилей**

Физическая структура базы данных определяет, как данные будут храниться на уровне сервера. Она включает в себя таблицы, индексы, типы данных и другие элементы, которые влияют на производительность и доступность.

**1. Таблицы и их физические параметры**

  - **Таблица: Автомобили**
  - **Имя таблицы:** `cars`
  - **Индексы:** 
    - Первичный ключ на `ID_автомобиля`
    - Индекс по `VIN` для быстрого поиска
    - **Типы данных:** 
    - `ID_автомобиля` INT AUTO_INCREMENT
    - `Марка` VARCHAR(50)
    - `Модель` VARCHAR(50)
    - `Год_выпуска` YEAR
    - `VIN` VARCHAR(17)
    - `Цвет` VARCHAR(30)
    - `Цена` DECIMAL(10, 2)
    - `Статус` ENUM('в наличии', 'продан', 'зарезервирован')
    - `Технические характеристики` TEXT
    - `ID_производителя` INT (FK)
    - `ID_категории` INT (FK)

- **Таблица: Клиенты**
  - **Имя таблицы:** `customers`
  - **Индексы:** 
    - Первичный ключ на `ID_клиента`
    - Уникальный индекс на `Электронная_почта`
  - **Типы данных:** 
    - `ID_клиента` INT AUTO_INCREMENT
    - `ФИО` VARCHAR(100)
    - `Телефон` VARCHAR(15)
    - `Электронная_почта` VARCHAR(100)
    - `Адрес` VARCHAR(255)

- **Таблица: Сделки**
  - **Имя таблицы:** `sales`
  - **Индексы:** 
    - Первичный ключ на `ID_сделки`
    - Индекс по `ID_клиента` и `ID_автомобиля`
  - **Типы данных:** 
    - `ID_сделки` INT AUTO_INCREMENT
    - `Дата_продажи` DATE
    - `Цена_продажи` DECIMAL(10, 2)
    - `Способ_оплаты` ENUM('наличные', 'кредит', 'лизинг')
    - `ID_автомобиля` INT (FK)
    - `ID_клиента` INT (FK)
    - `ID_сотрудника` INT (FK)

- **Таблица: Сотрудники**
  - **Имя таблицы:** `employees`
  - **Индексы:** 
    - Первичный ключ на `ID_сотрудника`
  - **Типы данных:** 
    - `ID_сотрудника` INT AUTO_INCREMENT
    - `ФИО` VARCHAR(100)
    - `Должность` VARCHAR(50)
    - `Контактная_информация` VARCHAR(100)

- **Таблица: Производители**
  - **Имя таблицы:** `manufacturers`
  - **Индексы:** 
    - Первичный ключ на `ID_производителя`
  - **Типы данных:** 
    - `ID_производителя` INT AUTO_INCREMENT
    - `Наименование` VARCHAR(100)
    - `Страна` VARCHAR(50)

- **Таблица: Категории_автомобилей**
  - **Имя таблицы:** `car_categories`
  - **Индексы:** 
    - Первичный ключ на `ID_категории`
  - **Типы данных:** 
    - `ID_категории` INT AUTO_INCREMENT
    - `Название_категории` VARCHAR(50)

  ## 4. Физическая структура базы данных.
 **Хранение**:
  - Все таблицы хранятся в одной базе данных с именем, например, `car_dealership`.
  - Каждый из столбцов имеет заданный размер и тип данных, что позволяет оптимизировать использование пространства.
  
- **Индексы**:
  - Индексы обеспечивают быструю выборку данных и улучшение производительности запросов. Они хранятся отдельно от данных таблиц и могут потребовать дополнительного дискового пространства.
    Реализация проекта в среде конкретной СУБД.

    5.1. Создание таблиц.

    5.2. Создание запросов.

    5.3. Разработка интерфейса.

    5.4. Назначение прав доступа.

    5.5. Создание индексов.

    5.6. Разработка стратегии резервного копирования базы данных