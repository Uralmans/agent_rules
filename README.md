# Cursor-Optimized Agent Rules Collection
# Коллекция правил агентов, оптимизированная для Cursor

[English](#english) | [Русский](#russian)

---

## English

### Overview

This repository is a **Cursor-optimized fork** of the original [wshobson/agents](https://github.com/wshobson/agents) collection, specifically adapted for use with [Cursor IDE](https://cursor.sh/). 

The original repository contains 50+ specialized AI subagents for Claude Code, and this fork has been enhanced with Cursor-specific optimizations and intelligent rule application.

### Key Features

- **🔄 Smart Rule Application**: Rules are applied automatically based on context and necessity, not all at once
- **📝 Enhanced Metadata**: Optimized `.mdc` format with `alwaysApply` field for flexible configuration
- **🎯 Context-Aware**: Agents are invoked only when relevant to the current task
- **⚡ Performance Optimized**: Reduced overhead by applying rules selectively
- **🛠️ Cursor Integration**: Seamless integration with Cursor IDE workflow

### Source Repository

This collection is based on the excellent work from:
- **Original Repository**: [wshobson/agents](https://github.com/wshobson/agents)
- **Original Author**: [@wshobson](https://github.com/wshobson)
- **License**: MIT

### How It Works

Unlike the original collection where all rules are applied simultaneously, this Cursor-optimized version:

1. **Analyzes Context**: Determines which agents are relevant to the current task
2. **Selective Application**: Applies only the necessary rules based on file type, project structure, and user intent
3. **Dynamic Loading**: Loads and unloads agents as needed to maintain performance
4. **Smart Suggestions**: Recommends relevant agents based on the current development context

### Available Agents

#### Development & Architecture
- **[backend-architect](backend-architect.mdc)** - Design RESTful APIs, microservice boundaries, and database schemas
- **[frontend-developer](frontend-developer.mdc)** - Build React components, implement responsive layouts, and handle client-side state management
- **[ui-ux-designer](ui-ux-designer.mdc)** - Create interface designs, wireframes, and design systems
- **[mobile-developer](mobile-developer.mdc)** - Develop React Native or Flutter apps with native integrations
- **[graphql-architect](graphql-architect.mdc)** - Design GraphQL schemas, resolvers, and federation
- **[architect-reviewer](architect-review.mdc)** - Reviews code changes for architectural consistency and patterns

#### Language Specialists
- **[python-pro](python-pro.mdc)** - Write idiomatic Python code with advanced features and optimizations
- **[golang-pro](golang-pro.mdc)** - Write idiomatic Go code with goroutines, channels, and interfaces
- **[rust-pro](rust-pro.mdc)** - Write idiomatic Rust with ownership patterns, lifetimes, and trait implementations
- **[c-pro](c-pro.mdc)** - Write efficient C code with proper memory management and system calls
- **[cpp-pro](cpp-pro.mdc)** - Write idiomatic C++ code with modern features, RAII, smart pointers, and STL algorithms
- **[javascript-pro](javascript-pro.mdc)** - Master modern JavaScript with ES6+, async patterns, and Node.js APIs
- **[typescript-pro](typescript-pro.mdc)** - Master TypeScript with advanced types, generics, and strict type safety
- **[php-pro](php-pro.mdc)** - Write idiomatic PHP code with modern features and performance optimizations
- **[java-pro](java-pro.mdc)** - Master modern Java with streams, concurrency, and JVM optimization
- **[ios-developer](ios-developer.mdc)** - Develop native iOS applications with Swift/SwiftUI
- **[sql-pro](sql-pro.mdc)** - Write complex SQL queries, optimize execution plans, and design normalized schemas

#### Infrastructure & Operations
- **[devops-troubleshooter](devops-troubleshooter.mdc)** - Debug production issues, analyze logs, and fix deployment failures
- **[deployment-engineer](deployment-engineer.mdc)** - Configure CI/CD pipelines, Docker containers, and cloud deployments
- **[cloud-architect](cloud-architect.mdc)** - Design AWS/Azure/GCP infrastructure and optimize cloud costs
- **[database-optimizer](database-optimizer.mdc)** - Optimize SQL queries, design efficient indexes, and handle database migrations
- **[database-admin](database-admin.mdc)** - Manage database operations, backups, replication, and monitoring
- **[terraform-specialist](terraform-specialist.mdc)** - Write advanced Terraform modules, manage state files, and implement IaC best practices
- **[incident-responder](incident-responder.mdc)** - Handles production incidents with urgency and precision
- **[network-engineer](network-engineer.mdc)** - Debug network connectivity, configure load balancers, and analyze traffic patterns
- **[dx-optimizer](dx-optimizer.mdc)** - Developer Experience specialist that improves tooling, setup, and workflows

#### Quality & Security
- **[code-reviewer](code-reviewer.mdc)** - Expert code review with deep configuration security focus and production reliability
- **[security-auditor](security-auditor.mdc)** - Review code for vulnerabilities and ensure OWASP compliance
- **[test-automator](test-automator.mdc)** - Create comprehensive test suites with unit, integration, and e2e tests
- **[performance-engineer](performance-engineer.mdc)** - Profile applications, optimize bottlenecks, and implement caching strategies
- **[debugger](debugger.mdc)** - Debugging specialist for errors, test failures, and unexpected behavior
- **[error-detective](error-detective.mdc)** - Search logs and codebases for error patterns, stack traces, and anomalies
- **[search-specialist](search-specialist.mdc)** - Expert web researcher using advanced search techniques and synthesis

#### Data & AI
- **[data-scientist](data-scientist.mdc)** - Data analysis expert for SQL queries, BigQuery operations, and data insights
- **[data-engineer](data-engineer.mdc)** - Build ETL pipelines, data warehouses, and streaming architectures
- **[ai-engineer](ai-engineer.mdc)** - Build LLM applications, RAG systems, and prompt pipelines
- **[ml-engineer](ml-engineer.mdc)** - Implement ML pipelines, model serving, and feature engineering
- **[mlops-engineer](mlops-engineer.mdc)** - Build ML pipelines, experiment tracking, and model registries
- **[prompt-engineer](prompt-engineer.mdc)** - Optimizes prompts for LLMs and AI systems

#### Specialized Domains
- **[api-documenter](api-documenter.mdc)** - Create OpenAPI/Swagger specs and write developer documentation
- **[payment-integration](payment-integration.mdc)** - Integrate Stripe, PayPal, and payment processors
- **[quant-analyst](quant-analyst.mdc)** - Build financial models, backtest trading strategies, and analyze market data
- **[risk-manager](risk-manager.mdc)** - Monitor portfolio risk, R-multiples, and position limits
- **[legacy-modernizer](legacy-modernizer.mdc)** - Refactor legacy codebases and implement gradual modernization
- **[context-manager](context-manager.mdc)** - Manages context across multiple agents and long-running tasks

#### Business & Marketing
- **[business-analyst](business-analyst.mdc)** - Analyze metrics, create reports, and track KPIs
- **[content-marketer](content-marketer.mdc)** - Write blog posts, social media content, and email newsletters
- **[sales-automator](sales-automator.mdc)** - Draft cold emails, follow-ups, and proposal templates
- **[customer-support](customer-support.mdc)** - Handle support tickets, FAQ responses, and customer emails
- **[legal-advisor](legal-advisor.mdc)** - Draft privacy policies, terms of service, disclaimers, and legal notices

### Usage

1. **Copy Rules**: Copy `.mdc` files to your project's `.cursor/rules/` directory
2. **Configure**: Set `alwaysApply: true` for rules that should always be active
3. **Reference**: Use `AGENTS_INDEX.md` as a reference for available agents
4. **Enjoy**: Agents will be applied intelligently based on your current context

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Русский

### Обзор

Этот репозиторий представляет собой **оптимизированную для Cursor версию** оригинальной коллекции [wshobson/agents](https://github.com/wshobson/agents), специально адаптированную для использования с [Cursor IDE](https://cursor.sh/).

Оригинальный репозиторий содержит 50+ специализированных AI-агентов для Claude Code, и эта версия была улучшена с оптимизациями для Cursor и интеллектуальным применением правил.

### Ключевые особенности

- **🔄 Умное применение правил**: Правила применяются автоматически на основе контекста и необходимости, а не все сразу
- **📝 Улучшенные метаданные**: Оптимизированный формат `.mdc` с полем `alwaysApply` для гибкой настройки
- **🎯 Контекстно-ориентированный**: Агенты вызываются только когда это релевантно текущей задаче
- **⚡ Оптимизированная производительность**: Сниженная нагрузка за счет выборочного применения правил
- **🛠️ Интеграция с Cursor**: Бесшовная интеграция с рабочим процессом Cursor IDE

### Исходный репозиторий

Эта коллекция основана на отличной работе:
- **Оригинальный репозиторий**: [wshobson/agents](https://github.com/wshobson/agents)
- **Оригинальный автор**: [@wshobson](https://github.com/wshobson)
- **Лицензия**: MIT

### Как это работает

В отличие от оригинальной коллекции, где все правила применяются одновременно, эта оптимизированная для Cursor версия:

1. **Анализирует контекст**: Определяет, какие агенты релевантны текущей задаче
2. **Выборочное применение**: Применяет только необходимые правила на основе типа файла, структуры проекта и намерений пользователя
3. **Динамическая загрузка**: Загружает и выгружает агентов по мере необходимости для поддержания производительности
4. **Умные предложения**: Рекомендует релевантных агентов на основе текущего контекста разработки

### Доступные агенты

#### Разработка и архитектура
- **[backend-architect](backend-architect.mdc)** - Проектирование RESTful API, границ микросервисов и схем баз данных
- **[frontend-developer](frontend-developer.mdc)** - Создание React компонентов, реализация адаптивных макетов и управление состоянием на клиенте
- **[ui-ux-designer](ui-ux-designer.mdc)** - Создание дизайнов интерфейсов, макетов и дизайн-систем
- **[mobile-developer](mobile-developer.mdc)** - Разработка React Native или Flutter приложений с нативными интеграциями
- **[graphql-architect](graphql-architect.mdc)** - Проектирование GraphQL схем, резолверов и федерации
- **[architect-reviewer](architect-review.mdc)** - Обзор изменений кода на предмет архитектурной согласованности и паттернов

#### Специалисты по языкам
- **[python-pro](python-pro.mdc)** - Написание идиоматичного Python кода с продвинутыми возможностями и оптимизациями
- **[golang-pro](golang-pro.mdc)** - Написание идиоматичного Go кода с горутинами, каналами и интерфейсами
- **[rust-pro](rust-pro.mdc)** - Написание идиоматичного Rust с паттернами владения, временами жизни и реализациями трейтов
- **[c-pro](c-pro.mdc)** - Написание эффективного C кода с правильным управлением памятью и системными вызовами
- **[cpp-pro](cpp-pro.mdc)** - Написание идиоматичного C++ кода с современными возможностями, RAII, умными указателями и STL алгоритмами
- **[javascript-pro](javascript-pro.mdc)** - Мастерство современного JavaScript с ES6+, асинхронными паттернами и Node.js API
- **[typescript-pro](typescript-pro.mdc)** - Мастерство TypeScript с продвинутыми типами, дженериками и строгой типизацией
- **[php-pro](php-pro.mdc)** - Написание идиоматичного PHP кода с современными возможностями и оптимизациями производительности
- **[java-pro](java-pro.mdc)** - Мастерство современной Java с потоками, конкурентностью и оптимизацией JVM
- **[ios-developer](ios-developer.mdc)** - Разработка нативных iOS приложений с Swift/SwiftUI
- **[sql-pro](sql-pro.mdc)** - Написание сложных SQL запросов, оптимизация планов выполнения и проектирование нормализованных схем

#### Инфраструктура и операции
- **[devops-troubleshooter](devops-troubleshooter.mdc)** - Отладка проблем в продакшене, анализ логов и исправление сбоев развертывания
- **[deployment-engineer](deployment-engineer.mdc)** - Настройка CI/CD пайплайнов, Docker контейнеров и облачных развертываний
- **[cloud-architect](cloud-architect.mdc)** - Проектирование AWS/Azure/GCP инфраструктуры и оптимизация облачных затрат
- **[database-optimizer](database-optimizer.mdc)** - Оптимизация SQL запросов, проектирование эффективных индексов и управление миграциями БД
- **[database-admin](database-admin.mdc)** - Управление операциями БД, резервным копированием, репликацией и мониторингом
- **[terraform-specialist](terraform-specialist.mdc)** - Написание продвинутых Terraform модулей, управление state файлами и реализация IaC лучших практик
- **[incident-responder](incident-responder.mdc)** - Обработка инцидентов в продакшене с срочностью и точностью
- **[network-engineer](network-engineer.mdc)** - Отладка сетевого подключения, настройка балансировщиков нагрузки и анализ трафика
- **[dx-optimizer](dx-optimizer.mdc)** - Специалист по Developer Experience, улучшающий инструменты, настройку и рабочие процессы

#### Качество и безопасность
- **[code-reviewer](code-reviewer.mdc)** - Экспертный обзор кода с глубоким фокусом на безопасность конфигурации и надежность продакшена
- **[security-auditor](security-auditor.mdc)** - Обзор кода на уязвимости и обеспечение соответствия OWASP
- **[test-automator](test-automator.mdc)** - Создание комплексных тестовых наборов с unit, integration и e2e тестами
- **[performance-engineer](performance-engineer.mdc)** - Профилирование приложений, оптимизация узких мест и реализация стратегий кэширования
- **[debugger](debugger.mdc)** - Специалист по отладке ошибок, сбоев тестов и неожиданного поведения
- **[error-detective](error-detective.mdc)** - Поиск паттернов ошибок в логах и кодовых базах, стек трейсов и аномалий
- **[search-specialist](search-specialist.mdc)** - Эксперт по веб-исследованиям с использованием продвинутых техник поиска и синтеза

#### Данные и ИИ
- **[data-scientist](data-scientist.mdc)** - Эксперт по анализу данных для SQL запросов, операций BigQuery и инсайтов данных
- **[data-engineer](data-engineer.mdc)** - Создание ETL пайплайнов, хранилищ данных и потоковых архитектур
- **[ai-engineer](ai-engineer.mdc)** - Создание LLM приложений, RAG систем и пайплайнов промптов
- **[ml-engineer](ml-engineer.mdc)** - Реализация ML пайплайнов, обслуживание моделей и инженерия признаков
- **[mlops-engineer](mlops-engineer.mdc)** - Создание ML пайплайнов, отслеживание экспериментов и реестры моделей
- **[prompt-engineer](prompt-engineer.mdc)** - Оптимизация промптов для LLM и ИИ систем

#### Специализированные области
- **[api-documenter](api-documenter.mdc)** - Создание OpenAPI/Swagger спецификаций и написание документации для разработчиков
- **[payment-integration](payment-integration.mdc)** - Интеграция Stripe, PayPal и платежных процессоров
- **[quant-analyst](quant-analyst.mdc)** - Создание финансовых моделей, бэктестинг торговых стратегий и анализ рыночных данных
- **[risk-manager](risk-manager.mdc)** - Мониторинг рисков портфеля, R-мультипликаторов и лимитов позиций
- **[legacy-modernizer](legacy-modernizer.mdc)** - Рефакторинг устаревших кодовых баз и реализация постепенной модернизации
- **[context-manager](context-manager.mdc)** - Управление контекстом между множественными агентами и длительными задачами

#### Бизнес и маркетинг
- **[business-analyst](business-analyst.mdc)** - Анализ метрик, создание отчетов и отслеживание KPI
- **[content-marketer](content-marketer.mdc)** - Написание постов в блоге, контента для соцсетей и email рассылок
- **[sales-automator](sales-automator.mdc)** - Составление холодных писем, follow-up'ов и шаблонов предложений
- **[customer-support](customer-support.mdc)** - Обработка тикетов поддержки, ответов на FAQ и писем клиентов
- **[legal-advisor](legal-advisor.mdc)** - Составление политик конфиденциальности, условий использования, отказов и юридических уведомлений

### Использование

1. **Копирование правил**: Скопируйте `.mdc` файлы в директорию `.cursor/rules/` вашего проекта
2. **Настройка**: Установите `alwaysApply: true` для правил, которые должны быть всегда активны
3. **Справочник**: Используйте `AGENTS_INDEX.md` как справочник по доступным агентам
4. **Наслаждайтесь**: Агенты будут применяться интеллектуально на основе вашего текущего контекста

### Лицензия

Этот проект лицензирован под MIT License - см. файл [LICENSE](LICENSE) для деталей.
