# Architecture Diagram

A Spring Boot 3.3 web application implementing a veterinary clinic management system with Thymeleaf UI, Spring MVC controllers, Spring Data JPA repositories, and a MySQL backend with H2 for development.

## Application Architecture

```mermaid
flowchart TD
    subgraph Client["Client Layer"]
        Browser["Web Browser"]
    end
    subgraph App["Application Layer - Spring Boot 3.3"]
        Web["Spring MVC + Thymeleaf"]
        Service["Business Logic (Controllers)"]
        Cache["Caffeine Cache"]
        Actuator["Spring Boot Actuator"]
    end
    subgraph Data["Data Layer"]
        JPA["Spring Data JPA / Hibernate"]
        DB[("MySQL (prod)")]
        H2[("H2 (dev/test)")]
    end

    Browser -->|"HTTP requests"| Web
    Web -->|"delegates"| Service
    Service -->|"CRUD operations"| JPA
    JPA -->|"SQL queries"| DB
    JPA -->|"SQL queries"| H2
    Service -->|"caches vet list"| Cache
    Actuator -->|"health metrics"| App
```

## Component Relationships

```mermaid
flowchart LR
    subgraph Presentation["Presentation"]
        WelcomeCtrl["WelcomeController"]
        OwnerCtrl["OwnerController"]
        PetCtrl["PetController"]
        VisitCtrl["VisitController"]
        VetCtrl["VetController"]
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
    subgraph Entities["Domain Model"]
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
    PetTypeFormatter -->|"looks up"| OwnerRepo
    PetValidator -.->|"validates"| Pet
    CacheConfig -.->|"caches"| VetRepo
```
