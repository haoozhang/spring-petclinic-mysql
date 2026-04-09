# Architecture Diagram

Spring PetClinic is a Spring Boot 3.3 web application using Thymeleaf for server-side rendering, Spring Data JPA for data access, and MySQL as the primary database with Caffeine cache for performance.

## Application Architecture

```mermaid
flowchart TD
    subgraph Client["Client Layer"]
        Browser["Web Browser"]
    end
    subgraph App["Application Layer - Spring Boot 3.3"]
        Web["Spring MVC + Thymeleaf"]
        Cache["Caffeine Cache"]
        Actuator["Spring Boot Actuator"]
    end
    subgraph Data["Data Layer"]
        JPA["Spring Data JPA + Hibernate"]
        MySQL[("MySQL")]
        H2[("H2 (test/dev)")]
    end

    Browser -->|"HTTP requests"| Web
    Web -->|"serve pages"| Browser
    Web -->|"cache reads"| Cache
    Web -->|"data operations"| JPA
    JPA -->|"SQL queries"| MySQL
    JPA -->|"SQL queries (dev)"| H2
    Browser -->|"health metrics"| Actuator
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
    subgraph DataAccess["Data Access"]
        OwnerRepo["OwnerRepository"]
        VetRepo["VetRepository"]
    end
    subgraph Entities["Entities / Model"]
        Owner["Owner"]
        Pet["Pet"]
        PetType["PetType"]
        Visit["Visit"]
        Vet["Vet"]
        Specialty["Specialty"]
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
    OwnerRepo -->|"returns"| Owner
    OwnerRepo -->|"returns"| Pet
    OwnerRepo -->|"returns"| Visit
    VetRepo -->|"returns"| Vet
    PetCtrl -->|"validates"| PetValidator
    PetCtrl -->|"formats"| PetTypeFormatter
    PetTypeFormatter -->|"queries"| OwnerRepo
    CacheConfig -.->|"caches"| VetRepo
```
