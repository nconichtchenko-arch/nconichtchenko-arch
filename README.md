# Добрый день! Я Павел Онищенко

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
- Реализовал **30+ pet-проектов на GitHub**: от построения DWH и Data Governance до маркетинговой аналитики и прогнозирования спроса. Все проекты — с реальными данными и измеримыми результатами.
- Освоил современный стек: dbt, Apache Airflow, ClickHouse, DuckDB, Parquet, Docker, Streamlit, CI/CD (GitHub Actions). Готов применять их в реальных DWH-задачах.
- **Разработал платформу Data Governance (`data-governance-platform`):** объединил каталогизацию (парсинг dbt manifest), валидацию Data Contracts (нашел 2 инцидента дрейфа схемы на реальных данных) и визуализацию Lineage (с восстановлением потерянных рёбер) в едином Streamlit-дашборде.
- Применяю инженерный подход: оптимизация SQL через EXPLAIN ANALYZE, контроль качества (Data Contracts), автоматизация на Python и Airflow.

## Почему я полезен команде:

Я инженер с 14-летним опытом, который понимает бизнес-процессы изнутри (телеком, инфраструктура) и умеет строить пайплайны данных. Мой GitHub — это проекты с реальными результатами (397к строк, ускорение SQL в 6 раз, бенчмарк ClickHouse 6.8x, сжатие CSV в Parquet в 11.4 раза).

---

## 🛠 Навыки

- **Анализ данных и BI:** Python (Pandas, NumPy, SciPy), статистический анализ (t-тест, A/B), EDA, **RFM-анализ, когортный анализ (Retention), ABC-XYZ, анализ оттока (Churn)**. Визуализация: Matplotlib, Seaborn, Plotly, Power BI, Panel, **Streamlit**.
- **Базы данных и SQL:** PostgreSQL, MySQL, ClickHouse (базово). Сложные запросы (JOIN, CTE, оконные функции), оптимизация (индексы, EXPLAIN ANALYZE). PL/pgSQL (триггеры, функции), рекурсивные CTE.
- **Инженерия данных:** dbt (модели, тесты), Apache Airflow (DAG, оркестрация), ETL на Python (Pandas, SQLAlchemy), DuckDB, Parquet, Docker (базово), **Data Contracts, Data Quality (Great Expectations)**.
- **Базы данных (MPP):** Greenplum (развертывание в Docker, загрузка данных, витрины), ClickHouse, PostgreSQL.
- **Разработка и инструменты:** Git, GitHub, Jupyter, Python CLI, BeautifulSoup, REST API, JSON, Streamlit, GitHub Actions (CI/CD).

---

## 📊 Покрытие архитектуры данных (Data Platform)

Мои pet-проекты — это не разрозненные скрипты, а компоненты единой современной архитектуры данных. В таблице ниже показано, как они закрывают ключевые слои платформы (от источников до продуктов из данных).

| Слой архитектуры | Реализовано в проектах |
| :--- | :--- |
| **Источники (OLTP, API, Files)** | `airflow-e2e-api-pipeline`, `job-finder-agent` |
| **Транспорт и стриминг** | `kafka-clickhouse-demo`, `iot-auction-anomaly-detection` |
| **Хранение (DWH, Lake, MPP)** | `marketplace-dwh-analytics` (PostgreSQL + ClickHouse), `greenplum-dwh-demo`, `duckdb-parquet-analytics` |
| **Трансформация (ETL/ELT)** | `dbt-ci-cd-demo`, `dbt-great-expectations-demo`, `dbt-semantic-layer-demo`, `dagster-orchestration-demo`, `prefect-orchestration-demo` |
| **Data Governance (Каталог, Lineage)** | `data-governance-platform`, `dbt-data-lineage-demo`, `neo4j-data-lineage`, `data-observability-demo` |
| **Data Quality & Contracts** | `soda-data-quality-demo`, `data-contracts-demo`, `api-data-contracts`, `data-quality-agent` |
| **BI и Визуализация** | `executive-dashboard`, `ecommerce-analytics-rfm`, `grafana-postgres-monitoring`, `marketing-analytics-demo`, `demand-forecasting-demo` |
| **Retention / Оптимизация** | `clickhouse-optimization-demo` (TTL, партиционирование) |
| **Цифровые продукты и сервисы** | `data-as-a-service-api`, `marketing-analytics-api` (REST API) |
| **AI-агенты (MCP)** | `data-quality-agent` (мульти-базовый агент на MCP + Ollama) |

---

## 📊 Аналитика и BI (Data Analytics & BI)

Проекты, ориентированные на извлечение бизнес-инсайтов, визуализацию и статистику.

### 🛒 E-commerce & Маркетинг
- [Marketing Analytics Demo (ROMI & CTR)](https://github.com/nconichtchenko-arch/marketing-analytics-demo) — анализ эффективности рекламных кампаний.
- [E-commerce Analytics: RFM & Retention](https://github.com/nconichtchenko-arch/ecommerce-analytics-rfm) — сегментация клиентов, удержание.
- [Executive Dashboard](https://github.com/nconichtchenko-arch/Executive-Dashboard) — дашборд для руководства (KPI, динамика, топ стран).
- [Анализ товарного ассортимента](https://github.com/nconichtchenko-arch/retail-assortment-analysis) — ABC-XYZ, t-тест.
- [Анализ питания в фастфуде](https://github.com/nconichtchenko-arch/fastfood-nutrition-analysis) — EDA, визуализация, дашборд.

### 📈 Прогнозирование и ML
- [Demand Forecasting Demo](https://github.com/nconichtchenko-arch/demand-forecasting-demo) — прогнозирование спроса (Moving Average, Holt-Winters, Croston).
- [E-commerce Sales Forecast (Time Series)](https://github.com/nconichtchenko-arch/ecommerce-sales-forecast) — Prophet, прогноз выручки.
- [Customer Churn Prediction](https://github.com/nconichtchenko-arch/customer-churn-prediction) — ML (Random Forest), Recall 80%.

### 📊 Статистика и A/B-тесты
- [A/B Testing Simulation](https://github.com/nconichtchenko-arch/ab-testing-simulation) — Z-тест для двух групп.
- [A/B Testing ANOVA](https://github.com/nconichtchenko-arch/ab-testing-anova) — ANOVA для трех и более групп.

---

## ⚙️ Инженерия данных и Инфраструктура (Data Engineering)

Проекты, ориентированные на построение хранилищ, оркестрацию, качество данных и инфраструктуру.

### 🏗 Ядро: DWH и Хранилища
- [Marketplace DWH Analytics](https://github.com/nconichtchenko-arch/marketplace-dwh-analytics) — **ГЛАВНЫЙ ПРОЕКТ.** DWH, Data Vault 2.0, GX, Data Catalog, Streamlit, Airflow, dbt, ClickHouse, CI/CD.
- [Raw → Clean → Analytics](https://github.com/nconichtchenko-arch/raw-clean-analytics-demo) — трехслойная архитектура.
- [Greenplum DWH Demo](https://github.com/nconichtchenko-arch/greenplum-dwh-demo) — MPP СУБД (+ бенчмарк с ClickHouse).
- [ClickHouse Optimization Demo](https://github.com/nconichtchenko-arch/clickhouse-optimization-demo) — ускорение в 1.4x (+ бенчмарк с Greenplum).
- [PostgreSQL Advanced Engineering](https://github.com/nconichtchenko-arch/postgresql-advanced-engineering) — C-расширения, Data Vault, EAV.
- [DuckDB + Parquet Analytics](https://github.com/nconichtchenko-arch/duckdb-parquet-analytics) — аналитика Parquet через DuckDB (сжатие в 11.4 раза).

### 🔄 Оркестрация и ETL/ELT
- [Airflow E2E Pipeline](https://github.com/nconichtchenko-arch/airflow-e2e-api-pipeline) — E2E пайплайн (курсы валют -> PostgreSQL -> Email).
- [Dagster Orchestration Demo](https://github.com/nconichtchenko-arch/dagster-orchestration-demo) — оркестрация данных на Dagster (asset-centric).
- [Prefect Orchestration Demo](https://github.com/nconichtchenko-arch/prefect-orchestration-demo) — ETL-пайплайн на Prefect (@flow, @task).
- [dbt CI/CD Demo](https://github.com/nconichtchenko-arch/dbt-ci-cd-demo) — CI/CD для dbt.
- [Kafka + ClickHouse Demo](https://github.com/nconichtchenko-arch/kafka-clickhouse-demo) — стриминг.

### 🛡 Data Governance & Quality
- [Data Governance Platform](https://github.com/nconichtchenko-arch/data-governance-platform) — Каталог + Контракты + Lineage.
- [API Data Contracts](https://github.com/nconichtchenko-arch/api-data-contracts) — защита DWH от изменений API.
- [Soda Data Quality Demo](https://github.com/nconichtchenko-arch/soda-data-quality-demo) — Data Quality проверки.
- [Data Contracts Demo](https://github.com/nconichtchenko-arch/data-contracts-demo) — YAML-контракт, валидатор.
- [dbt + Great Expectations Demo](https://github.com/nconichtchenko-arch/dbt-great-expectations-demo) — E2E пайплайн качества.
- [Data Quality Agent (MCP)](https://github.com/nconichtchenko-arch/data-quality-agent) — AI-агент для проверки качества данных через MCP (LLM + PostgreSQL).

### 🚀 Data Products & API
- [Data-as-a-Service API](https://github.com/nconichtchenko-arch/data-as-a-service-api) — микросервис на FastAPI для отдачи метрик из DWH.
- [Marketing Analytics API](https://github.com/nconichtchenko-arch/marketing-analytics-api) — REST API для маркетинговых метрик (ROMI, CTR).

### 📡 Мониторинг и Lineage
- [Grafana + Prometheus + Loki](https://github.com/nconichtchenko-arch/grafana-postgres-monitoring) — мониторинг PostgreSQL.
- [Data Observability Demo](https://github.com/nconichtchenko-arch/data-observability-demo) — мониторинг пайплайнов Airflow.
- [dbt Data Lineage Demo](https://github.com/nconichtchenko-arch/dbt-data-lineage-demo) — визуализация Lineage для dbt.
- [Neo4j Data Lineage](https://github.com/nconichtchenko-arch/neo4j-data-lineage) — Data Lineage в Neo4j.

### 🧪 Учебные кейсы и эксперименты
- [IoT Anomaly Detection](https://github.com/nconichtchenko-arch/iot-auction-anomaly-detection) — распределенная система обнаружения аномалий (FastAPI, Prometheus, Grafana).
- [Python Security Scanner](https://github.com/nconichtchenko-arch/python-security-scanner) — статический анализатор кода (37 правил).
- [Job Market Analytics](https://github.com/nconichtchenko-arch/job-market-analytics) — парсинг, SQL-агрегация, Streamlit.
- [Retail Assortment Analysis](https://github.com/nconichtchenko-arch/retail-assortment-analysis) — ABC-XYZ, t-тест (p-value = 0.0486).
- [Fastfood Nutrition Analysis](https://github.com/nconichtchenko-arch/fastfood-nutrition-analysis) — EDA, PL/pgSQL, дашборд на Panel.

---

## 📫 Контакты

- **Email:** pavloni@mail.ru (предпочитаемый способ связи)
- **GitHub:** [github.com/nconichtchenko-arch](https://github.com/nconichtchenko-arch)
- **LinkedIn:** [linkedin.com/in/pavel-onichtchenko](https://linkedin.com/in/pavel-onichtchenko)
- **Проживание:** Воронеж
- **Формат работы:** удалённо
