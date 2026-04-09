# Architecture Diagram

Spring PetClinic MySQL is a Spring Boot 3.3 web application using Thymeleaf for server-side rendering, Spring Data JPA for data access, and MySQL as the primary database, with Caffeine cache for vet data.

## Application Architecture

```mermaid
flowchart TD
    subgraph Client["Client Layer"]
        Browser["Web Browser"]
    end
    subgraph App["Application Layer - Spring Boot 3.3"]
        Web["Spring MVC + Thymeleaf"]
        Service["Business Logic"]
        Cache["Caffeine Cache"]
    end
    subgraph Data["Data Layer"]
        JPA["Spring Data JPA / Hibernate"]
        MySQL[("MySQL Database")]
        H2[("H2 In-Memory DB (dev)")]
    end
    subgraph Ops["Observability"]
        Actuator["Spring Boot Actuator"]
    end

    Browser -->|"HTTP requests"| Web
    Web -->|"delegates"| Service
    Service -->|"cache vets"| Cache
    Service -->|"CRUD operations"| JPA
    JPA -->|"SQL queries"| MySQL
    JPA -->|"SQL queries (dev)"| H2
    Web -->|"metrics/health"| Actuator
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
    subgraph Domain["Domain / Entities"]
        Owner["Owner"]
        Pet["Pet"]
        Visit["Visit"]
        Vet["Vet"]
        PetType["PetType"]
        Specialty["Specialty"]
    end
    subgraph DataAccess["Data Access"]
        OwnerRepo["OwnerRepository"]
        VetRepo["VetRepository"]
    end
    subgraph Infra["Infrastructure"]
        CacheConfig["CacheConfiguration"]
        PetTypeFormatter["PetTypeFormatter"]
        PetValidator["PetValidator"]
    end

    OwnerCtrl -->|"queries"| OwnerRepo
    PetCtrl -->|"queries"| OwnerRepo
    VisitCtrl -->|"queries"| OwnerRepo
    VetCtrl -->|"queries"| VetRepo
    OwnerRepo -->|"manages"| Owner
    OwnerRepo -->|"manages"| Pet
    OwnerRepo -->|"manages"| Visit
    VetRepo -->|"manages"| Vet
    PetCtrl -->|"uses"| PetTypeFormatter
    PetCtrl -->|"uses"| PetValidator
    CacheConfig -.->|"caches"| VetRepo
```
