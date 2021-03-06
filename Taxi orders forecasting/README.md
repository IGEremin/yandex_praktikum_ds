# Прогнозирование числа заказов по временному ряду

## Задача

Заказчик - сервис заказа такси, предоставил данные о заказах за полгода. **Задача - построить модель, способную спрогнозирвоать число заказов на следующий час по предыдущим данным**.

## Библиотеки и методы

`pandas` `statsmodel.seasonal_decompose` `scikit-learn` `lightgbm`

- Анализ данных;
- Создание новых признаков
- Декомпозиция временного ряда;
- Машинное обучение;
- Кросс-валидация.

## Описание решения

Исходные данные содержат более 26400 записей, расположенных в хронологическом порядке, с разницей в 10 минут времени. С помощью функции `seasonal_decompose` выделил компоненты тренда и сезонности, и определил закономерности изменения заказов. В качестве признаков для обучения моделей выделил скользящее среднее и ряд предыдущих значений. Применил модели линейной регрессии, случайного леса и градиентного бустинга. Подобрал гиперпараметры, используя кросс-валидацию и определил модель с наилучшим качеством.
В результате работы удалось выделить важные закономерности в изменении заказов, создать модель способную предсказывать число заказов на следующий час.