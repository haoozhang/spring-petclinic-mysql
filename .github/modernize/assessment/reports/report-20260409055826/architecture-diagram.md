# Architecture Diagram

Spring PetClinic MySQL is a Spring Boot 3.3 web application using Thymeleaf for UI, Spring Data JPA for data access, and MySQL as its primary database, with Caffeine for in-memory caching.

## Application Architecture

```mermaid
flowchart TD
    subgraph Client["Client Layer"]
        Browser["Web Browser"]
    end
    subgraph App["Application Layer - Spring Boot 3.3"]
        Web["Spring MVC + Thymeleaf"]
        Service["Owner / Vet / Pet / Visit Logic"]
        Cache["Caffeine Cache"]
        Actuator["Spring Boot Actuator"]
    end
    subgraph Data["Data Layer"]
        JPA["Spring Data JPA / Hibernate"]
        DB[("MySQL")]
        H2[("H2 (test/dev)")]
    end

    Browser -->|"HTTP requests"| Web
    Web -->|"delegates"| Service
    Service -->|"cache lookups"| Cache
    Service -->|"CRUD operations"| JPA
    JPA -->|"SQL queries"| DB
    JPA -->|"SQL queries (test)"| H2
    Actuator -->|"health / metrics"| App
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
        CrashCtrl["CrashController"]
    end
    subgraph BusinessLogic["Business Logic"]
        PetTypeFormatter["PetTypeFormatter"]
        PetValidator["PetValidator"]
        CacheConfig["CacheConfiguration"]
    end
    subgraph DataAccess["Data Access"]
        OwnerRepo["OwnerRepository"]
        VetRepo["VetRepository"]
    end
    subgraph Entities["Entities"]
        Owner["Owner"]
        Pet["Pet"]
        PetType["PetType"]
        Visit["Visit"]
        Vet["Vet"]
        Specialty["Specialty"]
    end

    OwnerCtrl -->|"queries"| OwnerRepo
    PetCtrl -->|"queries"| OwnerRepo
    VisitCtrl -->|"queries"| OwnerRepo
    VetCtrl -->|"queries"| VetRepo
    OwnerRepo -->|"manages"| Owner
    OwnerRepo -->|"manages"| Pet
    OwnerRepo -->|"manages"| Visit
    VetRepo -->|"manages"| Vet
    VetRepo -->|"manages"| Specialty
    PetTypeFormatter -->|"lookups"| OwnerRepo
    PetValidator -.->|"validates"| PetCtrl
    CacheConfig -.->|"caches"| VetRepo
```
