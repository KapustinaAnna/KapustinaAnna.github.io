# Просмотреть информацию о продукте

[Просмотреть информацию о продукте](../requirements.md#_21)

## Задачи

## Задача 1: Добавить фильтр поиска продукта и форму с информацией о продукте
 
**Критерии приемки:**

  - Пользователь должен иметь возможность ввести информацию о продукте в поле фильтра для поиска.
  - Система должна возвращать результаты поиска, соответствующие введённым критериям.

### Основной сценарий

|Шаг|Описание шага|Результат|
|-------|---------------------------------------------------------------|----------------------------------------------------|
|1|Открыть страницу поиска продуктов|Пользователь видит поле для ввода информации о продукте и кнопку для поиска|
|2|Ввести корректное название продукта в поле фильтра ( молоко)|Пользователь видит список релевантных результатов поиска, соответствующих введённому названию продукта (молоко 3,2%, Молоко 2,5%)|
|3|Нажать кнопку "Поиск"|<p>Система выполняет поиск и отображает результаты на странице</p><p></p>|

-----

### Негативный сценарий

|Шаг|Описание шага|Результат|
|-------|---------------------------------------------------------------|----------------------------------------------------|
|1|Открыть страницу поиска продуктов|Пользователь видит поле для ввода информации о продукте и кнопку для поиска|
|2|Ввести некорректное название продукта (например, "телефон Айфон 15")|Поле фильтра заполняется названием "Телефон Айфон 15"|
|3|Нажать кнопку "Поиск"|Система отображает сообщение "Продукт не найден"|


-----