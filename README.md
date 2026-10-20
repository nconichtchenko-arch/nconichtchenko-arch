# Привет! Я Павел Онищенко 👋

### Аналитик данных / BI-аналитик

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat&logo=postgresql&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

Меняю стэк на Аналитика, 14+ лет опыта в телекоммуникационной отрасли. 
Специализируюсь на анализе данных, визуализации и построении BI-решений. 
Ищу удалённую позицию аналитика данных.

---

## 🛠 Навыки

**Анализ данных:** Python (Pandas, NumPy, SciPy), статистический анализ (t-тест, A/B), EDA.
**Базы данных:** PostgreSQL, MySQL. 
*   **SQL:** сложные запросы (JOIN, CTE, оконные функции), оптимизация (индексы, EXPLAIN ANALYZE).
*   **Продвинутый SQL (учебные кейсы):** написание C-расширений для PostgreSQL, рекурсивные CTE, PL/pgSQL.
**Визуализация и BI:** Matplotlib, Seaborn, Plotly, Power BI, Panel.
**Инструменты:** Jupyter, Git, GitHub, Docker (базово).
**Разработка:** Python CLI, BeautifulSoup, SQLAlchemy, rich, JSON.

---

## 📊 Мои проекты

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

### 🛒 Анализ товарного ассортимента розничного магазина
Полный цикл анализа данных: загрузка, очистка, feature engineering, EDA.

- ABC-XYZ анализ 2 343 товаров: выделил 869 позиций основного ассортимента, 130 дополнительного, 999 потенциально интересных.
- Статистическая гипотеза о различии среднего чека в будни и выходные (t-тест, p-value = 0.0486) — выявил, что средний чек в будни статистически значимо выше на 636 руб.
- Сформулировал бизнес-рекомендации по оптимизации ассортимента.

**Стек:** Python, Pandas, SciPy, Seaborn, Jupyter  
🔗 [Ссылка на проект](https://github.com/nconichtchenko-arch/retail-assortment-analysis)

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

### 📊 DWH Marketplace Analytics (Новый проект!)
Проектирование и разработка корпоративного хранилища данных (DWH) для e-commerce.

- Спроектировал модель данных «Звезда» (Star Schema): таблица фактов `fact_sales` и измерения `dim_customers`, `dim_products`, `dim_dates`.
- Написал ETL-пайплайн на Python (Pandas, SQLAlchemy), загрузил и очистил **397 924 строки** транзакций.
- Провел оптимизацию SQL (EXPLAIN ANALYZE): создал индексы, ускорив агрегационные запросы **в 6 раз** (с 6.3 до 0.9 сек).
- Построил дашборд в **Power BI** для визуализации выручки по странам.

**Стек:** Python (Pandas), PostgreSQL, SQL, Power BI, Docker (базово).

🔗 [marketplace-dwh-analytics](https://github.com/nconichtchenko-arch/marketplace-dwh-analytics)

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

## 📫 Контакты

- **Email:** pavloni@mail.ru (предпочитаемый способ связи)
- **GitHub:** [github.com/nconichtchenko-arch](https://github.com/nconichtchenko-arch)
- **Проживание:** Воронеж
- **Формат работы:** удалённо
