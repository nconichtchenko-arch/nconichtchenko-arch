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

## Что я уже сделал для перехода:

- Прошёл переподготовку по аналитике данных (ТГУ, 256 ч) и программу «Инженер по большим данным» (Университет Иннополис, 256 ч), чтобы закрыть теоретическую базу.
- Реализовал **16 проектов на GitHub** — от DWH (модель «Звезда», Data Vault 2.0) и трехслойной архитектуры (Raw → Clean → Analytics) до E2E-пайплайна качества (dbt + Great Expectations + CI/CD), Data Contracts, оптимизации ClickHouse, аналитики Parquet через DuckDB, глубокого анализа данных (RFM, Retention, ABC-XYZ, Market Basket) и анализа рынка вакансий (Job Market Analytics) и машинного обучения (Customer Churn Prediction).
- Освоил современный стек: dbt, Apache Airflow, ClickHouse, DuckDB, Parquet, Docker, Streamlit, CI/CD (GitHub Actions). Готов применять их в реальных DWH-задачах.
- Применяю инженерный подход: оптимизация SQL через EXPLAIN ANALYZE, контроль качества (Data Governance, Data Contracts), автоматизация на Python и Airflow.

### Почему я полезен команде:
Я инженер с 14-летним опытом, который понимает бизнес-процессы изнутри (телеком, инфраструктура) и умеет строить пайплайны данных. Мой GitHub — это проекты с реальными результатами (397к строк, ускорение SQL в 6 раз, бенчмарк ClickHouse 6.8x, сжатие CSV в Parquet в 11,4 раза).

---

## 🛠 Навыки

- **Анализ данных и BI:** Python (Pandas, NumPy, SciPy), статистический анализ (t-тест, A/B), EDA, **RFM-анализ, когортный анализ (Retention), ABC-XYZ, анализ оттока (Churn)**. Визуализация: Matplotlib, Seaborn, Plotly, Power BI, Panel, **Streamlit**.
- **Базы данных и SQL:** PostgreSQL, MySQL, ClickHouse (базово). Сложные запросы (JOIN, CTE, оконные функции), оптимизация (индексы, EXPLAIN ANALYZE). PL/pgSQL (триггеры, функции), рекурсивные CTE.
- **Инженерия данных:** dbt (модели, тесты), Apache Airflow (DAG, оркестрация), ETL на Python (Pandas, SQLAlchemy), DuckDB, Parquet, Docker (базово), Data Contracts, Data Quality (Great Expectations).
- **Базы данных (MPP):** Greenplum (развертывание в Docker, загрузка данных, витрины), ClickHouse, PostgreSQL.
- **Разработка и инструменты:** Git, GitHub, Jupyter, Python CLI, BeautifulSoup, REST API, JSON, Streamlit, GitHub Actions (CI/CD).

---

## 📊 Мои проекты

### 🏗️ DWH Marketplace Analytics
Pet-проект: DWH для e-commerce на реальном датасете (397 924 строки). Полный цикл: ETL, Airflow, dbt, ClickHouse, DuckDB.

- Спроектировал модель данных «Звезда» (Star Schema): таблица фактов `fact_sales` и измерения `dim_customers`, `dim_products`, `dim_dates`.
- Написал ETL-пайплайн на Python (Pandas, SQLAlchemy), загрузил и очистил **397 924 строки** транзакций.
- Провел оптимизацию SQL (EXPLAIN ANALYZE): создал индексы, ускорив агрегационные запросы **в 6 раз** (с 6.3 до 0.9 сек).
- Построил дашборд в **Power BI** для визуализации выручки по странам.
- Внедрил элементы **Data Governance**: разработал скрипт автоматической генерации каталога данных (Data Catalog) в JSON.
- Настроил **оркестрацию ETL-процесса** через Apache Airflow (Docker): написал DAG, который ежедневно запускает пайплайн.
- Интеграция **dbt**: написал модели `stg_sales` и `fct_sales`, добавил тесты (`not_null`, `relationships`), сделал `fct_sales` **инкрементальной**.
- Продвинутый **ClickHouse**: партиционирование (`MergeTree`), TTL, материализованные представления (`SummingMergeTree`).
- Data Quality & Drift Monitoring: скрипт data_quality_checks.py (Great Expectations), кастомные проверки (уникальность комбинации, формат даты, аномалии > 100 000), dbt-тесты (not_null, relationships). Результаты в metadata_catalog.data_quality_results, дашборд в Metabase. Найдены и удалены «сиротские» данные, почищены «хвосты» от CDC. Все тесты проходят (PASS=5).
- **Алертинг Data Quality (01.11.2026):** В Metabase настроен ежедневный алерт на график «Data Quality Status» (условие: есть результаты; получатель: pavloni@mail.ru). В README добавлен раздел про алертинг.
- Data Vault 2.0: в схеме data_vault реализована полная модель: Hub (hub_customer, hub_order, hub_product), Link (link_order_customer, link_order_product), Satellite (sat_customer_details, sat_order_details, sat_product_details). Загружено 18 536 заказов, 3 665 товаров, 387 875 связей. Обновлена ER-диаграмма (полная модель) и README.
- **Витрина воронки продаж** (`mart_sales_funnel`): агрегация заказов по дням с расчетом конверсии и выручки.
- **Metadata Management (углубление, 31.10.2026):** В каталог добавлены поля `owner` (владелец) и `tags` (автоопределение слоя: fact, dim, staging). Скрипт обновляет записи через `ON CONFLICT DO UPDATE`. В главном профиле добавлен соответствующий пункт.
- **Веб-интерфейс Data Catalog (01.11.2026):** Написан скрипт `data_catalog_ui.py` (Streamlit) для просмотра каталога данных. Фильтры по тегам и владельцам, отображение описания и Lineage. Исправлена ошибка с самоссылками в Lineage (убран самоссылочный цикл).

🔗 [marketplace-dwh-analytics](https://github.com/nconichtchenko-arch/marketplace-dwh-analytics)

**См. также:** [duckdb-parquet-analytics](https://github.com/nconichtchenko-arch/duckdb-parquet-analytics) — аналитика Parquet через DuckDB (без ETL).

**Стек:** Python (Pandas), PostgreSQL, ClickHouse, SQL, Power BI, Apache Airflow, dbt, DuckDB, Parquet, Docker.

---

### 📊 E-commerce Analytics: RFM & Retention
Pet-проект: Аналитика e-commerce на реальном датасете (397к строк). 
- **Задачи:** RFM-сегментация клиентов, когортный анализ (Retention).
- **Стек:** SQL (оконные функции), Python (Pandas), Streamlit, Metabase.
- **Результат:** Выявлены VIP-сегменты, приносящие основную выручку, и рассчитано удержание клиентов по месяцам.

🔗 [ecommerce-analytics-rfm](https://github.com/nconichtchenko-arch/ecommerce-analytics-rfm)

---

### 📈 Job Market Analytics
Pet-проект по анализу рынка вакансий в сфере Data / DWH / BI.
- **Задачи:** Выявление топ-навыков, анализ зарплатных вилок, топ компаний-работодателей.
- **Стек:** Python (Pandas), SQL (PostgreSQL), Streamlit, Plotly.
- **Результат:** Подтвержден фокус на DWH, SQL и Python. Медианная зарплата на рынке — 144 175 ₽.

🔗 [job-market-analytics](https://github.com/nconichtchenko-arch/job-market-analytics)

---

### 📜 Data Contracts Demo (Streamlit Dashboard)

Демонстрация подхода Data Contracts для контроля качества данных в DWH.

- YAML-контракт для таблицы `fct_sales` (описание колонок, типов, ограничений).
- Python-валидатор (PyYAML, psycopg2) с сохранением результатов в JSON.
- Streamlit-дашборд для визуализации статуса контракта (пройден/не пройден).
- CI/CD (GitHub Actions) для проверки YAML-контракта при пуше.

**Стек:** Python, PostgreSQL, Streamlit, GitHub Actions.

🔗 [Ссылка на проект](https://github.com/nconichtchenko-arch/data-contracts-demo)

---

### 🧠 Customer Churn Prediction (ML)
Pet-проект по прогнозированию оттока клиентов с использованием Machine Learning.
- **Задачи:** Разработка модели (Random Forest) для предсказания ухода клиента на основе RFM-метрик.
- **Стек:** Python (Pandas, Scikit-learn), Seaborn.
- **Результат:** Достигнут Recall 80% (модель выявляет 4 из 5 уходящих клиентов). Устранена утечка данных (Data Leakage) путем разделения данных по времени.

🔗 [customer-churn-prediction](https://github.com/nconichtchenko-arch/customer-churn-prediction)

---

### ⚙️ dbt CI/CD Demo

Демонстрация настройки **CI/CD для dbt-проекта** с использованием GitHub Actions.

- **dbt-модель** `sales_summary.sql` (агрегация продаж по дням).
- **dbt-тесты** (`not_null`, `unique`).
- **GitHub Actions**: автоматический запуск `dbt run` и `dbt test` при каждом пуше.
- **Временная PostgreSQL** в CI (создание тестовой таблицы `fct_sales`).

**Стек:** dbt-core, PostgreSQL, GitHub Actions.

🔗 [Ссылка на проект](https://github.com/nconichtchenko-arch/dbt-ci-cd-demo)

---

### 🏗 Raw → Clean → Analytics: Трехслойный DWH пайплайн

Демонстрация классической трехслойной архитектуры хранилища данных (DWH) с оркестрацией в Apache Airflow.

- **Raw-слой:** Python-скрипт забирает данные из API и сохраняет их в `raw.currency_rates` (JSONB).
- **Clean-слой:** Python-скрипт нормализует данные в `clean.currency_rates_clean`.
- **Analytics-слой:** Python-скрипт строит витрину `analytics.currency_rates_mart`.
- **Оркестрация:** DAG в Apache Airflow (`raw_clean_analytics_pipeline`).

**Стек:** Python, PostgreSQL, Apache Airflow (Docker), REST API.

🔗 [Ссылка на проект](https://github.com/nconichtchenko-arch/raw-clean-analytics-demo)

---

### 🧪 E2E Data Quality Pipeline: dbt + Great Expectations + CI/CD

Демонстрация сквозного пайплайна качества данных: dbt-модель + проверки Great Expectations + автоматизация в GitHub Actions.

- **dbt-модель** `sales_summary.sql` (агрегация продаж по дням).
- **Great Expectations** (проверки на NULL, диапазоны, уникальность).
- **CI/CD**: при каждом пуше запускается `dbt run` и проверки GX.

**Стек:** dbt-core, Great Expectations, PostgreSQL, GitHub Actions.

🔗 [Ссылка на проект](https://github.com/nconichtchenko-arch/dbt-great-expectations-demo)

---

### 🚀 ClickHouse Optimization Demo

Демонстрация оптимизации запросов в ClickHouse: партиционирование, `ORDER BY`, сравнение производительности на 1 млн строк.

- Таблица `sales_raw` (без оптимизации) vs `sales_optimized` (партиционирование + `ORDER BY`).
- Скрипты для загрузки данных, оптимизации и бенчмарка.
- **Ускорение:** ~1.4x (на 1 млн строк).

**Стек:** ClickHouse, Python, Docker.

🔗 [Ссылка на проект](https://github.com/nconichtchenko-arch/clickhouse-optimization-demo)

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

Агент для автоматического сбора и фильтрации вакансий с **hh.ru** (через парсинг HTML) и **Хабр Карьеры** (через API) после закрытия публичного API hh.ru.

- Реализовал парсинг HTML-страниц hh.ru через BeautifulSoup (обход ограничения API) и интеграцию с открытым API Хабр Карьеры.
- Спроектировал схему БД PostgreSQL с дедупликацией по `hh_id` (для hh) и `habr_id` (для Хабра).
- Разработал алгоритм скоринга релевантности вакансий по ключевым словам с весами (фокус на Data Quality, DWH, SQL, Python).
- Настроил разделение прав БД: владелец (`postgres`) и пользователь приложения (`dwh_user`).
- Добавил систему учёта откликов: таблица `applications`, команды `applied` и `list`.
- **Экономия времени:** автоматизирует рутинный поиск и отсев нерелевантных вакансий, позволяя фокусироваться только на подходящих предложениях.

**Стек:** Python, PostgreSQL, SQLAlchemy, BeautifulSoup, psycopg2, REST API, HTML-парсинг

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
