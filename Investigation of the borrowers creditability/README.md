# Исследование надежности заемщика

## Задача

Необходимо выяснить, влияют ли семейное положение, количество детей, уровень дохода клиента и цель кредита на факт погашения кредита в срок. Заказчик - банк, и ему важно иметь возможность до одобрения кредита предсказать вероятность возврата кредита в срок. Результат работы в этом проекте будет учтен при построении модели кредитного скоринга.

### Входные данные

Датасет содержащий данные о возрасте клиента, стаже, семейном положении, образовании, доходе, цели кредита. Целевой признак - наличие задолженности по кредиту. 

## Библиотеки и методы

`pandas` `matplotlib` `pymystem3`
- Обработка пропусков в наборе данных
- Категоризация данных
- Лемматизация
- Сводные таблицы
- Анализ данных

## Описание решения

Чтобы ответить на поставленные вопросы, необходимо проследить зависимости между анкетными параметрами клиента и наличием задолженности. Исходные данные имеют пропуски, неподходящие типы данных. На первом этапе требуется предобработка данных:
- Заполнил пропуски средними и медианными значениями признаков в зависимости от других признаков (для дохода по типу дохода, для стажа по возрасту клиентов). 
- Удалил из датасета объекты, имеющие аномальные значения
- Привел типы данных для числовых признаков
- Удалил дубликаты
- Использовал лемматизацию и унифицировал список целей кредита до 4 целей

На следующем этапе разделил клиентов на 4 категории по доходу, создав новый категориальный признак. 

В результате получил таблицу данных, удобную для анализа. Чтобы ответить на вопросы заказчика составил сводные таблицы по каждому признаку и агрегировал по количество просрочек платежа. Таблицы представляют наглядную статистику, по которой сделал выводы для заказчика.
