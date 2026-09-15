# Максим Цепаев | Portfolio
### Go Backend Developer (Junior / Intern)

[![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/maximtsepaev)<br>
<img src="https://cdn.simpleicons.org/gmail/D14836" width="16" height="16" align="absmiddle"> [tsepaevmaxim@gmail.com](mailto:tsepaevmaxim@gmail.com)

* **О себе**: Студент 2 курса МИИГАиК (направление «Информационные системы и технологии»). Успешно окончил курс «Go-разработчик» от Яндекс Практикума. Пишу чистый и безопасный код на Go, умею работать с многопоточностью (concurrency) и проектировать логику взаимодействия микросервисов с реляционными базами данных и брокерами сообщений.
* **Статус занятости**: Ищу стажировку (Golang-разработчик). Готов к гибридному формату работы в Москве.
* **Контакты и соцсети**:
  * Telegram: [@maximtsepaev](https://t.me/maximtsepaev) 
  * Email: tsepaevmaxim@gmail.com
 


## Технологический стек

* **Язык**: Go (Golang)
* **Конкурентность**: Goroutines, channels, mutex, waitgroup, context, предотвращение race condition и безопасная работа с общими данными.
* **Сеть и API**: HTTP, REST API, gRPC, JWT-аутентификация, написание middleware, логирование.
* **Базы данных**: PostgreSQL (чистый SQL, миграции, транзакции, блокировки), Apache Kafka.
* **Окружение и Инфраструктура**: Linux, Bash, Docker, Docker-compose, Git, CI/CD (GitHub Actions).



## Ключевые проекты


### [Flashsale](https://github.com/maximtsepaev/flashsale/tree/dev)

**Микросервисная система обработки заказов для flash-распродаж**
Проект решает классическую проблему highload-распродаж: защиту от оверселла (продажи в минус) и эффективную обработку пиковой нагрузки. Архитектура разделена на 3 компонента: API Gateway, Inventory Service и Order Worker.

**Технические решения:**
* **gRPC-коммуникация**: Реализовано синхронное взаимодействие между Gateway и Inventory Service для валидации и резервирования складских остатков.
* **Асинхронность через Apache Kafka**: Сформированные заказы публикуются в топик Kafka и асинхронно обрабатываются консьюмером (Order Worker) для снижения нагрузки на БД.
* **Транзакционная целостность**: Настроена безопасная работа со складскими остатками в PostgreSQL с использованием SQL-constraints и транзакций для исключения race conditions.
* **Отказоустойчивость**: Внедрен паттерн Graceful Shutdown для перехвата системных сигналов, корректного завершения HTTP/gRPC серверов и закрытия коннектов к БД и Kafka.
* **Инфраструктура**: Проект и все зависимости (PostgreSQL, Kafka KRaft) полностью контейнеризованы с помощью многоэтапных сборок (multi-stage) и запускаются через Docker Compose.


### [Task Planner (REST API)](https://github.com/maximtsepaev/go-final-project)

**Сервер планировщика задач с продвинутой логикой повторений**

* Разработано REST API для управления задачами (CRUD) с полнотекстым поиском и фильтрацией.
* Спроектирован и реализован кастомный алгоритм вычисления следующих дат для повторяющихся задач (учет дней недели, месяцев и високосных годов).
* Настроена JWT-аутентификация и middleware для защиты эндпоинтов.



## Практический опыт (учебные проекты в Яндекс Практикум)

В ходе обучения я реализовал более 10 тренировочных проектов, направленных на отработку конкретных навыков бэкенд-разработки. Основные из них:

* **[go-goroutines-final](https://github.com/maximtsepaev/go-goroutines-final) — Работа с многопоточностью, управление пулами горутин, каналами и синхронизация данных.**
* **[go-db-sql-final](https://github.com/maximtsepaev/go-db-sql-final) — Интеграция с СУБД, проектирование таблиц, оптимизация SQL-запросов и миграции.**
* **[go-http-final](https://github.com/maximtsepaev/go-http-final) — Написание HTTP-серверов, парсинг JSON, маршрутизация запросов и обработка ошибок.**
* **[docker-final](https://github.com/maximtsepaev/docker-final) — Контейнеризация приложений, написание Dockerfile и сборка сред через Docker Compose.**
* [go-ci-cd-final](https://github.com/maximtsepaev/go-ci-cd-final) — Автоматизация тестирования и деплоя кода с использованием GitHub Actions.
* [go-structures-final](https://github.com/maximtsepaev/go-structures-final) — Изучение базовых структур данных, указателей и интерфейсов.
* [go-workflow](https://github.com/maximtsepaev/go-workflow) — Организация процесса разработки, работа с ветками и контроль версий.
* [go-linux-final](https://github.com/maximtsepaev/go-linux-final) — Настройка окружения, работа с терминалом и написание Bash-скриптов для автоматизации.

