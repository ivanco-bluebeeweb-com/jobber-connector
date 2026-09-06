# Jobber Connector — Connector Discovery

**Category:** C47. Construction & Field Service Management  
**Vendor:** Jobber  
**Official Website:** https://getjobber.com

## 1. Официальный API
- **Базовый URL API:** `https://api.getjobber.com/api/graphql`
- **Поддерживаемая модель авторизации:** OAuth 2.0 Bearer Token

## 2. Архитектура сущностей
- Ключевые ресурсы платформы Jobber:
  - клиенты (clients)
  - заявки/лиды (requests)
  - сметы (quotes)
  - работы (jobs)
  - счета (invoices)

## 3. Требования к отказоустойчивости и безопасности
- Соблюдение вендорных лимитов запросов (Rate Limiting) с экспоненциальной задержкой.
- Строгая валидация Pydantic-схем на входе и выходе каждого запроса.
- Тестовая точка проверки подключения: `POST /api/graphql (Query: { clients { totalCount } })`.
