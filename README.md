## Мой проект нужен для того чтобы:

предоставить пользователям набор утилит для обработки и анализа транзакций. Основные функции включают фильтрацию транзакций по статусу и сортировку по дате.

## Использование

Ниже представлены примеры использования основных функций проекта.

### Функция filter_by_state нужна для:

Фильтрует список транзакций по указанному состоянию, по умолчанию EXECUTED.

from transaction_processor import filter_by_state

transactions = [
    {"id": 1, "state": "EXECUTED", "date": "2023-10-01"},
    {"id": 2, "state": "PENDING", "date": "2023-10-02"}
]

executed_transactions = filter_by_state(transactions)
print(executed_transactions)


### Функция sort_by_date нужна для:

Сортирует транзакции по дате. По умолчанию сортирует в порядке убывания.

from transaction_processor import sort_by_date

transactions = [
    {"id": 1, "state": "EXECUTED", "date": "2023-10-01"},
    {"id": 2, "state": "PENDING", "date": "2023-10-02"}
]

sorted_transactions = sort_by_date(transactions)
print(sorted_transactions)


## Примеры моего проекта

1. Фильтрация транзакций:
   
   from transaction_processor import filter_by_state

   transactions = [
       {"id": 1, "state": "EXECUTED", "date": "2023-10-01"},
       {"id": 2, "state": "PENDING", "date": "2023-10-02"}
   ]

   executed_transactions = filter_by_state(transactions)
   print(executed_transactions)  # [{'id': 1, 'state': 'EXECUTED', 'date': '2023-10-01'}]
   

2. Сортировка транзакций:
   
   from transaction_processor import sort_by_date

   transactions = [
       {"id": 1, "state": "EXECUTED", "date": "2023-10-01"},
       {"id": 2, "state": "PENDING", "date": "2023-10-02"}
   ]

   sorted_transactions = sort_by_date(transactions)
   print(sorted_transactions)  # [{'id': 2, 'state': 'PENDING', 'date': '2023-10-02'}, {'id': 1, 'state': 'EXECUTED', 'date': '2023-10-01'}]
   

##  Вклад в проект

Если вы хотите внести свой вклад в проект, пожалуйста, следуйте этим шагам:

1. Новая версия репозитория.
2. Создайте новую ветку (git checkout -b feature-branch).
3. Внесите свои изменения и зафиксируйте их (git commit -m 'Add new feature').
4. Запушьте изменения в свою ветку (git push origin feature-branch).
5. Откройте Pull Request.

## Тестирование

Этот проект использует `pytest` для написания и выполнения тестов. Следуйте инструкциям ниже, чтобы настроить и запустить тесты.

### Установка Pytest

Если `pytest` еще не установлен, вы можете установить его с помощью pip:


### Запуск тестов

Чтобы запустить все тесты, выполните следующую команду в корневой директории проекта:


Это выполнит все тесты, которые находятся в файлах, начинающихся с `test_` или заканчивающихся на `_test.py`. Вы также можете запустить конкретный тестовый файл:
