User Service Config

Внешний репозиторий конфигураций для микросервисной платформы User Service. Реализует паттерн External Configuration - отделение кода приложения от настроек.

Использование: Конфигурации загружаются автоматически через Spring Cloud Config Server.

Основной проект: https://github.com/Ogr2049/Task_Eigth_Ig

Структура:
1)config/user-service-module.yml - настройки основного сервиса;

2)config/api-gateway.yml - настройки API Gateway;

3)config/discovery-server.yml - настройки Eureka Server;

4)config/notification-service.yml - настройки сервиса notification-service.


Для тестирования отправки писем с MailHog оставьте настройки по умолчанию. Для работы с реальной почтой установите переменные окружения:
- `EMAIL_USERNAME` - email отправителя
- `EMAIL_PASSWORD` - пароль приложения


Каждая конфигурация имеет два профиля:
- "default" - для локального запуска (localhost)
- "docker" - для запуска в Docker-сети (имена сервисов)

При запуске через docker-compose автоматически активируется профиль `docker`.