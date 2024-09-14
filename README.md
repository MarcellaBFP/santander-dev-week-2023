#Santander Dev Week 2023
JSON RESTful API criada para a Santander Dev Week.

## Diagrama de classes

```mermaid
classDiagram
    class User {
        +String name
    }
    class Account {
        +String number
        +String agency
        +float balance
        +float limit
    }
    class Feature {
        +String icon
        +String description
    }
    class Card {
        +String number
        +float limit
    }
    class News {
        +String icon
        +String description
    }

    User "1" *-- "1" Account
    User "1" *-- "1" Card
    User "1" *-- "N" Feature : has many
    User "1" *-- "N" News : has many
