# Тестовое задание

Реализовать REST API со следующим функционалом

Необходимо создать сервис для хранения и подачи объявлений. Объявления должны храниться в базе данных. Сервис должен предоставлять API, работающее поверх HTTP в формате JSON.

## Требования
- Язык программирования Go
- Финальную версию нужно выложить на github.com;
- Простая инструкция для запуска (в идеале — с возможностью запустить через docker-compose up;
- 3 метода: получение списка объявлений, получение одного объявления, создание объявления;

Если есть сомнения по деталям — решение принять самостоятельно, но в своём README.md рекомендуем выписать вопросы и принятые решения по ним.

## Детали

### Метод получения списка объявлений
- Пагинация: на одной странице должно присутствовать 10 объявлений;
- Cортировки: по цене (возрастание/убывание) и по дате создания (возрастание/убывание);
- Поля в ответе: название объявления, цена.

### Метод получения конкретного объявления
- Обязательные поля в ответе: название объявления, цена;
- Опциональные поля (можно запросить, передав параметр fields): описание.

### Метод создания объявления:
- Принимает все вышеперечисленные поля: название, описание, цена;
- Возвращает ID созданного объявления и код результата (ошибка или успех).

### Усложнения
Не обязательно, но задание может быть выполнено с любым числом усложнений:
- Юнит тесты: постарайтесь достичь покрытия в 70% и больше;
- Контейнеризация: есть возможность поднять проект с помощью команды docker-compose up;
- Документация: swagger.
