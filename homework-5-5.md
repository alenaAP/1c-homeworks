# Задание к занятию "Виртуальные таблицы регистров накопления"

## Задача 1 Добавить контроль остатков в проведение документа "Реализация товаров и услуг"

### Описание задачи

Добавляем контроль остатков товара при проведении документа "Реализация товаров и услуг".

Продавать можно товар, который есть наличии.

Для этого сначала его необходимо оприходововать товар или иметь в остатках.

### Требования к результату

Выгрузка информационной базы (.dt). При проведении реализации система контролирует наличие остатков.

Если товара нет в наличии, система не формирует движения, отказ на проведение и сообщает о причине пользователю.

В сообщении указывается какого товара и в каком количестве не хватает.

### Процесс выполнения

в процедуру ОбработкаПроведения добавить запрос на проверку наличия остатка по номенклатуре из ТЧ документа

Если не хватает, то возвращаем Отказ = Истина

Иначе даем возможность системе провести документ


## Задача 2 Создать отчет СКД "Остатки товаров"

### Описание задачи

Создадим отчет для формирования остатков товаров

### Требования к результату

Выгрузка информационной базы (.dt) с Отчетом. 

Остатки формируются на указанную дату

Можно выбрать дату, отбор по номенклатуре

### Процесс выполнения

0. Удобнее будет отладить отчет как внешний и далее загрузить в конфигурацию уже рабочий. Можно сразу в конфигурации.

1. Создадим новый отчет - нажмем "Открыть схему компановки данных" - добавить Набор данных запрос - из Регистра накопления Товары 

добавим 
- Номенклатура
- Количество

2. Количество добавим в ресурсы, выражение Сумма

3. вкладка Настройки - добавим новую группировку, пустую

4. выбранные поля - добавим номенклатуру и количество

5. отбор - добавим Номенклатура. Правой кнопкой мыши нажмем на нее - откроем Свойства элемента пользовательских настроек - поставим галочку Включать пользовательские настройки

### Подсказка: [результат выполнения домашнего задания](Examples/homework-5-5-example.md)
