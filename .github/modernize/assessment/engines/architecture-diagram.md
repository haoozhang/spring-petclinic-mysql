# Architecture Diagram

Spring PetClinic (MySQL) is a Spring Boot 3.3.2 web application using Spring MVC with Thymeleaf for the UI, Spring Data JPA for persistence with MySQL (via Azure Spring Cloud JDBC), and Caffeine for in-process caching.

## Application Architecture

```mermaid
flowchart TD
    subgraph Client["Client Layer"]
        Browser["Web Browser"]
    end
    subgraph App["Application Layer - Spring Boot 3.3.2 / Java 17"]
        Web["Spring MVC + Thymeleaf"]
        Service["Business Logic / Formatters"]
        Actuator["Spring Boot Actuator"]
    end
    subgraph Cache["Caching Layer"]
        Caffeine["Caffeine Cache"]
    end
    subgraph Data["Data Layer"]
        JPA["Spring Data JPA"]
        DB[("MySQL")]
        H2[("H2 - dev/test")]
    end
    subgraph Azure["Azure Integration"]
        AzureJDBC["Azure Spring Cloud JDBC MySQL"]
    end

    Browser -->|"HTTP requests"| Web
    Web -->|"delegates"| Service
    Service -->|"reads cached data"| Caffeine
    Service -->|"CRUD operations"| JPA
    JPA -->|"SQL queries"| DB
    JPA -->|"SQL queries - dev"| H2
    DB -->|"managed connection"| AzureJDBC
    Actuator -->|"health and metrics"| App
```

## Component Relationships

```mermaid
flowchart LR
    subgraph Presentation["Presentation"]
        OwnerCtrl["OwnerController"]
        PetCtrl["PetController"]
        VisitCtrl["VisitController"]
        VetCtrl["VetController"]
        WelcomeCtrl["WelcomeController"]
    end
    subgraph Business["Business Logic"]
        PetTypeFmt["PetTypeFormatter"]
        PetValidator["PetValidator"]
        CacheConfig["CacheConfiguration"]
    end
    subgraph DataAccess["Data Access"]
        OwnerRepo["OwnerRepository"]
        VetRepo["VetRepository"]
    end
    subgraph Model["Domain Model"]
        Owner["Owner"]
        Pet["Pet"]
        Visit["Visit"]
        Vet["Vet"]
        Specialty["Specialty"]
    end

    OwnerCtrl -->|"queries"| OwnerRepo
    PetCtrl -->|"queries"| OwnerRepo
    VisitCtrl -->|"queries"| OwnerRepo
    VetCtrl -->|"queries"| VetRepo
    PetCtrl -->|"formats"| PetTypeFmt
    PetCtrl -->|"validates"| PetValidator
    OwnerRepo -->|"manages"| Owner
    OwnerRepo -->|"manages"| Pet
    OwnerRepo -->|"manages"| Visit
    VetRepo -->|"manages"| Vet
    VetRepo -->|"manages"| Specialty
    CacheConfig -.->|"caches"| VetRepo
```
