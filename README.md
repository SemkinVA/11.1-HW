# 11.1-HW

### Домашнее задание к занятию 11.1 - "Базы данных, их типы" - Семкин Вячеслав
***

### Задание 1. СУБД

### Кейс
Крупная строительная компания, которая также занимается проектированием и девелопментом, решила создать 
правильную архитектуру для работы с данными. Ниже представлены задачи, которые необходимо решить для
каждой предметной области. 

Какие типы СУБД, на ваш взгляд, лучше всего подойдут для решения этих задач и почему? 
 
1.1. Бюджетирование проектов с дальнейшим формированием финансовых аналитических отчётов и прогнозирования рисков. СУБД должна гарантировать целостность и чёткую структуру данных.

1.2. Под каждый девелоперский проект создаётся отдельный лендинг, и все данные по лидам стекаются в CRM к маркетологам и менеджерам по продажам. Какой тип СУБД лучше использовать для лендингов и для CRM? СУБД должны быть гибкими и быстрыми.

1.3. Отдел контроля качества решил создать базу по корпоративным нормам и правилам, обучающему материалу и так далее, сформированную согласно структуре компании. СУБД должна иметь простую и понятную структуру.

1.4. Департамент логистики нуждается в решении задач по быстрому формированию маршрутов доставки материалов по объектам и распределению курьеров по маршрутам с доставкой документов. СУБД должна уметь быстро работать со связями.

*Приведите ответ в свободной форме.* 

**Ответ:**

1.1. Реляционный тип СУБД. Обеспечит надежность и неизменность данных. Например: PostgreSQL, MySQL, Microsoft SQL.

1.2. Реляционный тип СУБД. Обеспечит минимальное время отклика и гибкость работы с данными. Например: PostgreSQL, MySQL, Microsoft SQL.

1.3. NoSQL Документо-ориентированный тип СУБД. Обеспечит хранение обектов в одной сущности. Например: CouchDB, MongoDB.

1.4. NoSQL Графовый тип СУБД. Обеспечит быструю работу со вязями. Например: Neo4j, Amazon Neptune, InfiniteGraph, InfoGrid.

***

### Задание 2. Транзакции

2.1. Пользователь пополняет баланс счёта телефона, распишите пошагово, какие действия должны произойти для того, чтобы транзакция завершилась успешно. Ориентируйтесь на шесть действий.

*Приведите ответ в свободной форме.*

**Ответ:**

1. Проверить, является ли пользователь клиентом банка.
2. Произвести запрос у пользователя требуемой суммы для пополнения телефонного счета.
3. Проверить наличие на банковском счету необходимой суммы.
4. Произвести перевовод средств с банковского счета на телефонный счет.
5. Скорректировать баланс банковского счета пользователя.
6. Произвести уведомление пользователя о проведении банковской операции.

***

### Задание 3. SQL vs NoSQL

3.1. Напишите пять преимуществ SQL-систем по отношению к NoSQL. 

*Приведите ответ в свободной форме.*

**Ответ:**

1. Имеют высокую производительность при работе с сильно структурированными данными и большими объёмами информации.
2. Имеют лучшую поддержку транзакционности, что позволяет автоматически откатывать изменения при обнаружении проблемных транзакций.
3. Имеют более развитое индексирование, чем NoSQL-базы, что обеспечивает более высокую производительность при выполнении сложных запросов.
4. Легкая установка ограничений на доступ к данным для разных пользователей, а также применение различных аутентификационных механизмов для обеспечения безопасности данных.
5. Имеют большую структурированность и лучшее соответствие этикету ACID.

***
### Задание 4. Кластеры

Необходимо производить большое количество вычислений при работе с огромным количеством данных, под эту задачу выделено 1000 машин. 
На основе какого критерия будете выбирать тип СУБД и какая модель *распределённых вычислений* здесь справится лучше всего и почему?

*Приведите ответ в свободной форме.*

**Ответ:**

В данной ситуации я бы использовал **"Колоночные СУБД"**, такие как: Sybase IQ (ныне SAP IQ), Vertica, ClickHouse, Google BigTable, InfoBright, Cassandra. 

Критерием данного выбора было бы основные преимущества колоночных СУБД – эффективное выполнения сложных аналитических запросов на больших объемах, и легкое, практически мгновенное, изменение структуры таблиц с данными, плюс существенная компрессия и сжатие, которое позволяет значительно экономить место.

