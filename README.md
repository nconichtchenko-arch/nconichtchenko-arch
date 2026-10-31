## Добрый день! Я Павел Онищенко

**Аналитик данных с опытом построения DWH**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=for-the-badge&logo=dbt&logoColor=white)
![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=for-the-badge&logo=apache-airflow&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

*Меняю стэк на Аналитика / Инженерию данных. 14+ лет опыта в телекоммуникационной отрасли.*

Специализируюсь на анализе данных, визуализации и построении DWH/ETL-пайплайнов. Ищу удалённую позицию аналитика данных или инженера DWH.

### Что я уже сделал для перехода:
- Прошёл переподготовку по аналитике данных (ТГУ, 256 ч) и программу «Инженер по большим данным» (Университет Иннополис, 256 ч), чтобы закрыть теоретическую базу.
- Реализовал 7 проектов на GitHub — от DWH (модель «Звезда») и ETL-пайплайнов до dbt-моделей с тестами и аналитики Parquet через DuckDB. Это код с реальными результатами (397к строк, ускорение SQL в 6 раз).
- Освоил современный стек: dbt, Apache Airflow, ClickHouse, DuckDB, Parquet (и Docker — базово). Готов применять их в реальных DWH-задачах.
- Применяю инженерный подход: оптимизация SQL через EXPLAIN ANALYZE, контроль качества (Data Governance), автоматизация на Python и Airflow.

### Почему я полезен команде:
Я инженер с 14-летним опытом, который понимает бизнес-процессы изнутри (телеком, инфраструктура) и умеет строить пайплайны данных. Мой GitHub — это проекты с реальными результатами (397к строк, ускорение SQL в 6 раз, бенчмарк ClickHouse 6.8x, сжатие CSV в Parquet в 11,4 раза).

---

## 🛠 Навыки

- **Анализ данных и BI:** Python (Pandas, NumPy, SciPy), статистический анализ (t-тест, A/B), EDA. Визуализация: Matplotlib, Seaborn, Plotly, Power BI, Panel.
- **Базы данных и SQL:** PostgreSQL, MySQL, ClickHouse (базово). Сложные запросы (JOIN, CTE, оконные функции), оптимизация (индексы, EXPLAIN ANALYZE). PL/pgSQL (триггеры, функции), рекурсивные CTE.
- **Инженерия данных:** dbt (модели, тесты), Apache Airflow (DAG, оркестрация), ETL на Python (Pandas, SQLAlchemy), DuckDB, Parquet, Docker (базово).
- **Базы данных (MPP):** Greenplum (развертывание в Docker, загрузка данных, витрины), ClickHouse, PostgreSQL.
- **Разработка и инструменты:** Git, GitHub, Jupyter, Python CLI, BeautifulSoup, REST API, JSON.

---

## 📊 Мои проекты

## DWH Marketplace Analytics
Pet-проект: DWH для e-commerce на реальном датасете (397 924 строки). Полный цикл: ETL, Airflow, dbt, ClickHouse, DuckDB.

- Спроектировал модель данных «Звезда» (Star Schema): таблица фактов `fact_sales` и измерения `dim_customers`, `dim_products`, `dim_dates`.
- Написал ETL-пайплайн на Python (Pandas, SQLAlchemy), загрузил и очистил **397 924 строки** транзакций.
- Провел оптимизацию SQL (EXPLAIN ANALYZE): создал индексы, ускорив агрегационные запросы **в 6 раз** (с 6.3 до 0.9 сек).
- Построил дашборд в **Power BI** для визуализации выручки по странам.
- Внедрил элементы **Data Governance**: разработал скрипт автоматической генерации каталога данных (Data Catalog) в JSON.
- Настроил **оркестрацию ETL-процесса** через Apache Airflow (Docker): написал DAG, который ежедневно запускает пайплайн.
- Интеграция **dbt**: написал модели `stg_sales` и `fct_sales`, добавил тесты (`not_null`, `relationships`), сделал `fct_sales` **инкрементальной**.
- Продвинутый **ClickHouse**: партиционирование (`MergeTree`), TTL, материализованные представления (`SummingMergeTree`).
- Data Quality & Drift Monitoring: скрипт `data_quality_checks.py` (Great Expectations), результаты в `metadata_catalog.data_quality_results`, дашборд в Metabase (круговая диаграмма + таблица дрифта).
- **Data Vault 2.0:** в схеме `data_vault` реализованы Hub (`hub_customer`), Link (`link_order_customer`), Satellite (`sat_customer_details`). Показывает знание архитектуры Enterprise DWH.

🔗 [marketplace-dwh-analytics](https://github.com/nconichtchenko-arch/marketplace-dwh-analytics)

**См. также:** [duckdb-parquet-analytics](https://github.com/nconichtchenko-arch/duckdb-parquet-analytics) — аналитика Parquet через DuckDB (без ETL).

**Стек:** Python (Pandas), PostgreSQL, ClickHouse, SQL, Power BI, Apache Airflow, dbt, DuckDB, Parquet, Docker.

---

### 🐘 Greenplum DWH Demo
Pet-проект по развертыванию MPP-СУБД **Greenplum** в Docker.

- Развернул Greenplum (образ `woblerr/greenplum:6.27.1`) в Docker, проверил MPP-архитектуру (1 Master + 2 Segment).
- Загрузил 1000 строк из основного проекта (`fct_sales`) в таблицу `sales_raw` с распределением по `stock_code`.
- Построил витрину `sales_mart` (топ-10 товаров по выручке) через `CREATE TABLE AS ... DISTRIBUTED BY`.

**Стек:** Greenplum, PostgreSQL, Docker, SQL.

🔗 [greenplum-dwh-demo](https://github.com/nconichtchenko-arch/greenplum-dwh-demo)

---

### 🦆 DuckDB + Parquet Analytics
Мини-проект по аналитике данных **без развёртывания СУБД** (Data Lake / Analytics on Files).

- Прочитал CSV (45,5 МБ) напрямую через DuckDB без ETL.
- Конвертировал в Parquet — сжатие в **11,4 раза** (3,8 МБ).
- Подтвердил идентичность данных повторным запросом.

**Стек:** DuckDB, Python, Parquet, SQL

🔗 [Ссылка на проект](https://github.com/nconichtchenko-arch/duckdb-parquet-analytics)

---

## 🌐 Airflow E2E Pipeline (Курсы валют)

Проект демонстрирует end-to-end пайплайн оркестрации данных с использованием Apache Airflow. DAG автоматически забирает курсы валют через REST API, сохраняет их в PostgreSQL и отправляет уведомление на Email.

- Развернул Apache Airflow 2.8.1 (LocalExecutor, Docker) и настроил связи с PostgreSQL.
- Написал DAG: PythonOperator для работы с REST API (open.er-api.com) и записи в БД, EmailOperator для отправки уведомлений через SMTP Mail.ru.
- Решил проблемы сетевого взаимодействия (VirtualBox NAT, доступ к БД по 10.0.2.2) и настроил SMTP (SSL, отключение STARTTLS).
- Подтвердил работу скриншотами: граф DAG, данные в pgAdmin, лог задачи и полученное письмо.

Стек: Apache Airflow, Python, PostgreSQL, psycopg2, Docker, SMTP.

[Ссылка на проект](https://github.com/nconichtchenko-arch/airflow-e2e-api-pipeline)

---

### 🤖 Job Finder Agent — автоматизированный поиск вакансий
Агент для автоматического сбора и фильтрации вакансий с hh.ru после закрытия публичного API.

- Реализовал парсинг HTML-страниц через BeautifulSoup (обход ограничения API).
- Спроектировал схему БД PostgreSQL с дедупликацией по hh_id.
- Разработал алгоритм скоринга релевантности вакансий по ключевым словам с весами.
- Настроил разделение прав БД: владелец (postgres) и пользователь приложения (course).
- Добавил систему учёта откликов: таблица applications, команды applied и list, VIEW v_my_applications.
- Использую инструмент ежедневно: за один день обработал 20+ вакансий, отправил 4 отклика, прошёл скрининг.

**Стек:** Python, PostgreSQL, SQLAlchemy, BeautifulSoup, psycopg3, REST/HTML parsing

🔗 [Ссылка на проект](https://github.com/nconichtchenko-arch/job-finder-agent)

---

### 🐘 PostgreSQL Advanced Engineering & Research
Репозиторий с инженерными кейсами по базам данных. Включает написание C-расширения для интеграции PostgreSQL с Telegram API, проектирование моделей Data Vault и EAV, оптимизацию запросов через pgbench и рекурсивные CTE.

**Стек:** PostgreSQL, C, libcurl, PL/pgSQL, pgbench.

🔗 [postgresql-advanced-engineering](https://github.com/nconichtchenko-arch/postgresql-advanced-engineering)

---

### 📡 IoT Real-time Anomaly Detection (Auction-Based)
Инженерный кейс по проектированию распределенной системы обнаружения аномалий в реальном времени.
*   **Архитектура:** Микросервисы на FastAPI, децентрализованный выбор координатора (Leader Election).
*   **Стек:** Python, FastAPI, PostgreSQL, Prometheus, Grafana, Docker Compose.
*   **Особенность:** Настроен мониторинг метрик (Data Observability) и визуализация в реальном времени.

🔗 [iot-auction-anomaly-detection](https://github.com/nconichtchenko-arch/iot-auction-anomaly-detection)

---

### 🔒 Сканер безопасности Python-кода
Статический анализатор Python-кода с 37 правилами проверки уязвимостей.

- Разработал сканер с 37 правилами: SQL-инъекции, XSS, CORS, слабая криптография, хардкод секретов.
- Реализовал CLI с 5 аргументами: фильтрация по severity, игнор-лист, JSON-вывод, strict-режим.
- Настроил JSON-отчёт с UTF-8, метаданными и сводкой по найденным проблемам.
- Добавил поддержку .scannerignore и код возврата для CI/CD.
- В тестовом файле обнаружил 12 проблем, включая 2 критические.

**Стек:** Python, CLI, JSON, rich, Git 

🔗 [Ссылка на проект](https://github.com/nconichtchenko-arch/python-security-scanner)

---

### 🛒 Анализ товарного ассортимента розничного магазина
Полный цикл анализа данных: загрузка, очистка, feature engineering, EDA.

- ABC-XYZ анализ 2 343 товаров: выделил 869 позиций основного ассортимента, 130 дополнительного, 999 потенциально интересных.
- Статистическая гипотеза о различии среднего чека в будни и выходные (t-тест, p-value = 0.0486) — выявил, что средний чек в будни статистически значимо выше на 636 руб.
- Сформулировал бизнес-рекомендации по оптимизации ассортимента.

**Стек:** Python, Pandas, SciPy, Seaborn, Jupyter  

🔗 [Ссылка на проект](https://github.com/nconichtchenko-arch/retail-assortment-analysis)

---

### 🍔 Анализ данных о питании в сети фастфуда
Дипломный проект «Инженер по большим данным» (Университет Иннополис). 
Полный цикл: от загрузки в PostgreSQL до интерактивного дашборда.

- Загрузил и структурировал данные в PostgreSQL, спроектировал нормализованную схему БД.
- Реализовал систему аудита на триггерах и функциях PL/pgSQL.
- Провёл EDA с визуализацией (heatmap, boxplot, scatter plot, bar chart).
- Построил интерактивный дашборд на Panel + Plotly.

**Стек:** PostgreSQL, SQLAlchemy, Python, Plotly, Panel, PL/pgSQL 

🔗 [Ссылка на проект](https://github.com/nconichtchenko-arch/fastfood-nutrition-analysis)

---

## 📫 Контакты

- **Email:** pavloni@mail.ru (предпочитаемый способ связи)
- **GitHub:** [github.com/nconichtchenko-arch](https://github.com/nconichtchenko-arch)
- **Проживание:** Воронеж
- **Формат работы:** удалённо
