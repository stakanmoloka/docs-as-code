# Диаграммы

## Диаграмма последовательности

```mermaid
sequenceDiagram
    actor User as Пользователь
    participant System as Система
    participant Model as ML-модель

    User->>System: Открыть раздел рекомендаций
    System->>Model: Передать предпочтения пользователя
    Model-->>System: Вернуть список рекомендованных фильмов
    System-->>User: Показать рекомендации
```

## Диаграмма классов

```mermaid
classDiagram
    class User {
        +int id
        +string name
    }

    class Movie {
        +int id
        +string title
        +string genre
    }

    class UserPreference {
        +int id
        +string genre
    }

    class Recommendation {
        +int id
        +float score
    }

    User "1" --> "*" UserPreference : указывает
    User "1" --> "*" Recommendation : получает
    Recommendation "*" --> "1" Movie : рекомендует
```

