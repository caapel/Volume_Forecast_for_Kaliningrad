# Algoritm forecasting Power Consumption in Kaliningrad 2023 (XGBoost only)

Проблемы в этой версии:
1) Отсутствует полный датасет за 2023 год, валидация условная
2) ~~Аномальные выбросы влияют на корректность прогнозирования последующего дня~~

В этой версии:
1) Полная копия логики репозитория: https://github.com/caapel/ForecastPowerEnergy.git
2) Добавлена возможность автоматической фильтрации двух крайних малозначимых признаков (с последующим корректным формированием графика `MAPE Limits at different sample periods`)

Заметки для дальнейшей работы:
1) Попробовать обрезать дерево до 4-х ветвей
2) Попробовать поменять тип интерполяции температуры (linear, polynomial = 2)
3) Попробовать вернуть фильтрацию данных
4) Попробовать округлить прогнозный результат до 1 знака после запятой
5) Попробовать добавить новый признак – рабочий, выходной, праздничный и послепраздничный дни
6) Попробовать вернуть остальные погодные условия
7) Уточнить с какого часа (0 или 1) начинаются сутки