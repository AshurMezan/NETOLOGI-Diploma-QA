# Отчёт по итогам автоматизации

## Что было запланировано и что было сделано

- проведено исследовательское тестирование функционала веб-сервиса покупки тура "Путешествие дня".
- настроен удобный запуск SUT с быстрым подключением к необходимой БД.
- запущена и настроена CI, запускающая тесты на обеих заявленных БД: MySQL и PostgreSQL.
- составлен [план автоматизации]() предусматривающий 53 тестовых сценария (16 сценариев API тестирования и 37 на 
UI тестирование).
- написан необходимый для автоматизации тестовый фреймворк (
[page objects]() для взаимодествия с 
элементами веб-сервиса и 
[helpers]() для управления тестовыми данными). 
При этом тестовые данные независимы от текущей даты и генерируются случайно для избежания эффекта пестицида.
- автоматизированы все 53 заявленных в плане тестовых сценария. Помимо заявленных было добавлено ещё 7 дополнительных
сценария тестирования UI.
- составлен [отчет]() по результату прогона тестов.
- созданы 15 [issue]() по найденным дефектам.

## Сработавшие риски

- Из-за отсутствия техдокументации было трудно определить ожидаемый результат в тестах
- требование поддержки двух СУБД добавило сложности в настройках запуска SUT и CI.
- отсутствие у веб-элементов приложения атрибута test-id создало сложности с локаторами элеметов при составление page objects.

## Общий итог по времени

|                  | Запланировано, ч  | Потрачено, ч |                                  Обоснование расхождения                                   |
|:-----------------|    :----:   |   :----:   |:------------------------------------------------------------------------------------------:|
| Настройка SUT, создание тестового фреймворка | 12  | 16 |             Переписал часть фреймворка, чтобы улучшить восприятие кода              |
| Создание автотестов  | 12  | 16 |                         Поправил тесты для нового фреймворка                          |
| Создание баг-репортов и отчёта | 8 | 9 | Пытался сруктурировать найденные дефекты, оформить их понятным языком и ещё разбирался как работать с багтрекенговой системой |  
| Отчёт по результатам автоматизации | 5 | 6 |                                             -                                              |  
| Подключение CI | 4 | 4 |                                             -                                              |  
| Всего | 41 | 51 |                                                                                            |