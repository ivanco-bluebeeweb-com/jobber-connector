# Jobber Connector — Auth & Credentials Standard

**Compliance:** AUTH_AND_CREDENTIALS_STANDARD.md (B1–B10)

## Схема аутентификации
- **Метод:** OAuth 2.0 Bearer Token
- **Хранение:** Секреты сохраняются изолированно в хранилище секретов платформы Imperal.
- **Валидация:** При сохранении ключа выполняется тестовый запрос `POST /api/graphql (Query: { clients { totalCount } })`.
- **Отключение:** Удаление локальных ключей без воздействия на аккаунт вендора.
