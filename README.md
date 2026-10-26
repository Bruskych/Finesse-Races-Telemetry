<div align="center">

# EN ```Version```

</div>

# Finesse Races Telemetry API

A REST API microservice for collecting and analyzing anonymous gameplay statistics from the Minecraft mod **Finesse Races**. The project is built with Spring Boot and is designed to balance asymmetric game design as part of a bachelor's thesis at Constantine the Philosopher University in Nitra.

## 🎯 Architectural Goal
The server receives lightweight, asynchronous JSON payloads from game clients, processes them, and stores the data in a relational database (PostgreSQL). This makes it possible to collect reliable gameplay meta-data without affecting game server performance (0 ms latency on the Minecraft side).

## ⚙️ Technology Stack
* **Language:** Java 17
* **Framework:** Spring Boot 4.1.x
* **Data Layer:** Spring Data JPA, Hibernate
* **Database:** PostgreSQL (with JSONB support)
* **Build Tool:** Maven

## 📊 Collected Metrics (Event Log)
1. **Pick Rate & Switch Rate:** Race selection when first entering a world and the frequency of race changes using the Orb.
2. **Survival Analytics (Telemetry of Death):** Causes of death (lava, falls, mobs) to verify the effectiveness of race-specific debuffs.
3. **Progression Timestamps:** Measurement of in-game time (`PLAY_TIME`) required to achieve key vanilla milestones (entering a mine, reaching the Nether) to identify imbalances in race-specific progression and resource economies.

**Privacy (GDPR Compliance):** The project does not collect IP addresses or raw UUIDs. All player identifiers are hashed using the SHA-256 algorithm on the client side before transmission.

---

<div align="center">

# RU ```Version```

</div>

# Finesse Races Telemetry API

REST API микросервис для сбора и анализа анонимной игровой статистики из Minecraft-мода **Finesse Races**. Проект разработан на базе Spring Boot и предназначен для балансировки асимметричного геймдизайна в рамках бакалаврской работы (Университет имени Константина Философа в Нитре).

## 🎯 Архитектурная цель
Сервер принимает легковесные асинхронные JSON-пакеты от игровых клиентов, обрабатывает их и сохраняет в реляционную базу данных (PostgreSQL). Это позволяет собирать чистую «мету» без ущерба для производительности игровых серверов (0 ms задержки на стороне Minecraft).

## ⚙️ Стек технологий
* **Язык:** Java 17
* **Фреймворк:** Spring Boot 4.1.x
* **Слой данных:** Spring Data JPA, Hibernate
* **База данных:** PostgreSQL (JSONB поддержка)
* **Сборка:** Maven

## 📊 Собираемые метрики (Event Log)
1. **Pick Rate & Switch Rate:** Выбор расы при первом заходе в мир и частота смены расы через Сферу.
2. **Survival Analytics (Telemetry of Death):** Причины смерти (лава, падение, мобы) для проверки работы классовых дебаффов.
3. **Progression Timestamps:** Замер игрового времени (`PLAY_TIME`) до получения ключевых ванильных достижений (спуск в шахту, Незер) для выявления перекосов в экономике рас.

**Приватность (GDPR Compliance):** Проект не собирает IP-адреса или чистые UUID. Все идентификаторы игроков хэшируются алгоритмом SHA-256 на стороне клиента перед отправкой.
