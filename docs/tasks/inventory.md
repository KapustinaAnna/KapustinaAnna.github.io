# Инвентаризация

[UC-12: Инвентаризацияя](../requirements.md#_11)



### Основной сценарий Выполняется переход на экран 
| Шаг | Описание шага                                                              | Результат                                                                                                      |
|-----|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 1   | Открыть экран для создание нового процесса инвентаризации [WF4](../uiux.md#wf4-c)| Пользователь видит экран для ввода информации |
| 2   | Ввести название и дату инвентаризации                                | Пользователь видит заполненные данные  |
| 3   | Нажать кнопку "OK"                               | Отправляется запрос POST/inventory Пользователь видит главный экран  [WF5](../uiux.md#wf5-)  |
| 4   | Сканировать штрихкод продукта                                   | Отправляется запрос GET/products/{barcode},  Открывается экран [WF1](../uiux.md#wf1), Система отображает информацию о продукте, соответствующую сканированному штрихкоду                            |
| 5  | Сверить информацию с фактическим продуктом                    | Информация на экране совпадает с фактическим состоянием продукта                                               |
| 6   | Нажать кнопку "ОК" подтверждая, что информация верная                           | Система позволяет пользователю перейти к следующему продукту                                                 |                                                  


### Негативный сценарий
| Шаг | Описание шага                                                              | Результат                                                                                                      |
|-----|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 1   | Открыть экран для создание нового процесса инвентаризации [WF4](../uiux.md#wf4-c)| Пользователь видит экран для ввода информации |
| 2   | Ввести название и дату инвентаризации                                | Пользователь видит заполненные данные  |
| 3   | Нажать кнопку "OK"                               | Отправляется запрос POST/inventory Пользователь видит главный экран  [WF5](../uiux.md#wf5-)  |
| 4   | Пользователь сканирует штрихкод продукта                                   | Отправляется запрос GET/products/{barcode}, Открывается экран [WF1](../uiux.md#wf1), Система не может найти продукт по сканированному штрихкоду                                                   |
| 5  | Система выдает сообщение об ошибке "Продукт не найден" [WF3](../uiux.md#wf3)                   | Пользователь видит сообщение об ошибке и возможность добавить информацию о продукте в систему                 |
| 6   | Нажать кнопку "Добавить продукт"                      | Пользователь видит экран   [WF2](../uiux.md#wf2)                  |
| 7   |Добавить информацию о продукте                     | Пользователь видит заполненные поля                    |
| 8   | Нажать кнопку  "Сохранить"                                  | Отправляется запрос Post/products/ Пользователь видит информацию о продукте [WF1](../uiux.md#wf1)                                          |


### Альтернативный сценарий
| Шаг | Описание шага                                                              | Результат                                                                                                      |
|-----|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 1   | Открыть экран для создание нового процесса инвентаризации [WF4](../uiux.md#wf4-c)| Пользователь видит экран для ввода информации |
| 2   | Ввести название и дату инвентаризации                                | Пользователь видит заполненные данные  |
| 3   | Нажать кнопку "OK"                               | Отправляется запрос POST/inventory Пользователь видит главный экран  [WF5](../uiux.md#wf5-)  |
| 4   | Сканировать штрихкод продукта                                   | Отправляется запрос GET/products/{barcode}, Открывается экран [WF1](../uiux.md#wf1)
|5     |Просмотреть информацию о продукте, соответствующую сканированному штрихкоду      | Система отображает информацию о продукте, но с некорректными данными                                                |
| 6   | Сверить информацию с фактическим продуктом                    | Информация не совпадает с фактическим состоянием продукта                                                      |
| 7   | Нажать кнопку "Редактировать "   | Открывается форма для редактирования информации о продукте   [WF6](../uiux.md#wf6)                                                   |
| 8   | Внести изменения                                           | Измененная информация о продукте отображается в форме                                                           |
| 9   | Нажать кнопку "Сохранить"                                                | Система подтверждает успешное сохранение новой информации. Пользователь  видит экран Открывается экран [WF1](../uiux.md#wf1) с новой информацией                                                       |


